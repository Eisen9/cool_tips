### How to add a Junit test to your existing JAVA code in Eclipse?

Inside the class and outside the main method (and probably other methods),
Create the following testing method:

```
@Test
Public void Test1(){
Print("this is my first test")
}
```

Note: you will have an error saying that you don’t have an imported library, so you need to see the suggestions to import a library.<br>


To see what libraries you have and to add more libraries, here is what you can do:

	1. Right click your folder where you have your test stored
	2. Click properties
		a. Select: Java build path



What is the difference between failure and error in Junit?

Failure: when the test fails to run a given code.
Error: when the block of test has a logic / semantic problem.
