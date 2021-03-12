# How to generate javadocs for your JAVA project?

### STEPS:

1. Comment your Java code with javadocs comments.
E.g. /**
       @author
       @param
       etc.
        */.

Make sure that all your methods are commented (right above the method decleration) with javadocs comments.


2. Using the command line, navigate to the folder in which your Java files are saved. If you are using IDE, then this would be the src folder.

3. Once you're in your desired fodlder, run: `javadoc file.java` or `javadoc *java` to document all your java file.


*Note: your files generated documents will be saved in a directory named out with the follwoing path: `out/yourProject`*.

*Your generated docs will also appear in your src directory unless you specify otherwise*.
