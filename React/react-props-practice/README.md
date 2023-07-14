

# React Props Usage

This README file provides an overview of how React props are used in the provided files.

## Files

The following files demonstrate the usage of React props:

1. **Card.jsx**: This file defines the `Card` component. It accepts props to customize the content of the card, such as `name`, `src` (avatar image URL), `tel` (telephone number), and `email` (email address).

2. **App.jsx**: This file showcases the usage of the `Card` component by rendering multiple contact cards. It imports the `contacts` array from the `contacts.js` file and passes the necessary props to each `Card` component instance.

3. **contacts.js**: This file exports an array of contact objects. Each contact object represents an individual and contains properties like `name`, `imgURL` (avatar image URL), `phone`, and `email`.

## Usage

To use React props and render contact cards with customized data, follow these steps:

1. Import the `Card` component and the `contacts` array into your desired file:
   ```javascript
   import Card from "./Card.jsx";
   import contacts from "./contacts.js";
   ```

2. Pass the required props to the `Card` component instance, based on the data from the `contacts` array:
   ```javascript
   <Card
     name={contacts[0].name}
     src={contacts[0].imgURL}
     tel={contacts[0].phone}
     email={contacts[0].email}
   />
   ```

3. Repeat the above step for each contact in the `contacts` array, providing the appropriate props to each `Card` component instance.

4. Customize the rendering of the `Card` component by accessing the props within the component definition. For example, you can access the name prop as `props.name` and the imgURL prop as `props.src`.

## Example

Here's an example usage of React props in the `App` component:

```javascript
import React from "react";
import contacts from "./contacts.js";
import Card from "./Card.jsx";

function App() {
  return (
    <div>
      <h1 className="heading">My Contacts</h1>
      {contacts.map((contact, index) => (
        <Card
          key={index}
          name={contact.name}
          src={contact.imgURL}
          tel={contact.phone}
          email={contact.email}
        />
      ))}
    </div>
  );
}

export default App;
```

In the above example, the `App` component renders multiple contact cards using the `Card` component. It maps over the `contacts` array and passes the corresponding contact's data as props to each `Card` component instance.

## License

This project is licensed under the [MIT License](LICENSE).

---
