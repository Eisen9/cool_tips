-----
# TensorFlow vs Keras vs tf.keras

This document provides a concise explanation of the differences between TensorFlow, Keras, and tf.keras, along with code examples illustrating how to solve the same problem using each approach.

## Overview of Differences

### 1. **TensorFlow**
   - TensorFlow is a comprehensive, low-level machine learning framework.
   - Provides fine-grained control over model construction and training.
   - Ideal for researchers and advanced users who require flexibility and customization.

### 2. **Keras**
   - Keras is a high-level deep learning API designed for simplicity and ease of use.
   - Originally supported multiple backends (e.g., TensorFlow, Theano, CNTK).
   - Good for beginners and rapid prototyping.

### 3. **tf.keras**
   - tf.keras is TensorFlow’s integrated version of Keras, introduced with TensorFlow 2.0.
   - Combines the simplicity of Keras with TensorFlow’s robust ecosystem.
   - Recommended for most use cases, offering both flexibility and ease of use.

## Code Examples
Below are examples solving the same problem (classifying handwritten digits from the MNIST dataset) using TensorFlow, Keras, and tf.keras.

### Using TensorFlow (Low-Level API)
```python
import tensorflow as tf
from tensorflow.keras.datasets import mnist

# Load and preprocess data
(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0
y_train, y_test = tf.one_hot(y_train, depth=10), tf.one_hot(y_test, depth=10)

# Define the model
class SimpleNN(tf.Module):
    def __init__(self):
        self.w1 = tf.Variable(tf.random.normal([784, 128]))
        self.b1 = tf.Variable(tf.zeros([128]))
        self.w2 = tf.Variable(tf.random.normal([128, 10]))
        self.b2 = tf.Variable(tf.zeros([10]))

    def __call__(self, x):
        x = tf.reshape(x, [-1, 784])
        h = tf.nn.relu(tf.matmul(x, self.w1) + self.b1)
        return tf.nn.softmax(tf.matmul(h, self.w2) + self.b2)

model = SimpleNN()

# Define loss and optimizer
def loss_fn(y_true, y_pred):
    return tf.reduce_mean(tf.keras.losses.categorical_crossentropy(y_true, y_pred))

optimizer = tf.optimizers.Adam()

# Training loop
for epoch in range(5):
    for x, y in zip(x_train, y_train):
        with tf.GradientTape() as tape:
            predictions = model(x)
            loss = loss_fn(y, predictions)
        grads = tape.gradient(loss, model.trainable_variables)
        optimizer.apply_gradients(zip(grads, model.trainable_variables))
print("Training complete!")
```

### Using Keras (Standalone High-Level API)
```python
from keras.models import Sequential
from keras.layers import Dense, Flatten
from keras.datasets import mnist
from keras.utils import to_categorical

# Load and preprocess data
(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0
y_train, y_test = to_categorical(y_train, 10), to_categorical(y_test, 10)

# Define the model
model = Sequential([
    Flatten(input_shape=(28, 28)),
    Dense(128, activation='relu'),
    Dense(10, activation='softmax')
])

# Compile and train the model
model.compile(optimizer='adam', loss='categorical_crossentropy', metrics=['accuracy'])
model.fit(x_train, y_train, epochs=5)
print("Training complete!")
```

### Using tf.keras (Integrated High-Level API)
```python
import tensorflow as tf
from tensorflow.keras import Sequential
from tensorflow.keras.layers import Dense, Flatten
from tensorflow.keras.datasets import mnist

# Load and preprocess data
(x_train, y_train), (x_test, y_test) = mnist.load_data()
x_train, x_test = x_train / 255.0, x_test / 255.0

# Define the model
model = Sequential([
    Flatten(input_shape=(28, 28)),
    Dense(128, activation='relu'),
    Dense(10, activation='softmax')
])

# Compile and train the model
model.compile(optimizer='adam', loss='sparse_categorical_crossentropy', metrics=['accuracy'])
model.fit(x_train, y_train, epochs=5)
print("Training complete!")
```

## Key Takeaways
- **TensorFlow**: Provides flexibility and control but requires more effort.
- **Keras**: Simple and intuitive, ideal for rapid development.
- **tf.keras**: Combines Keras' simplicity with TensorFlow’s power, making it the preferred choice for most scenarios.

Choose the approach that best fits your needs and project complexity!
