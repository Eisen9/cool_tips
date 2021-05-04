### Handy Tips for using IntelliJ


#### Testing with Junit
If you want to use Junit testing, just write the test (in your working JAVA project) you want to perform, e.g. `@Test1(){}`, then IntelliJ will prompt you to import/add a **Junit** library with whatever version you speicify to your code.


#### Using integrated ANT  
* make the build.xml file at the same level to src.

* when you run ant from intelliJ do: right click build.xml  > add to Ant Build > you will get a Ant Build banner > right click Ant-test > runRun Build.

* or, just right click the build.xml file and choose option `Run with ANT`.


#### Using integrated MAVEN

One way for doing it is when you create a new project, specify that you want to build your project with MAVEN. Otherwise, you can add it to your existing JAVA code, this is similary to adding ANT.
