#### Ant Structured Build Files

Lesson's objectives:

	• Where you put your:
		○ Build files
		○ Class files
	• How to dev a build which is scalable



We want to have the class files on one dir and so on.

General Notes:

	• Java source file into a java packages

*Standard Directory Names. This structure should be followed in the lab exercises:*


  | Dir_Name              | Description                  |
  | -----------           | -----------                  |
  | Src  | Source file (human produced) |
  | Build Classes or Bin             | Intermediate output (generated; cleanable)|
  | Dist                  | Distributed file (generated; cleanable) |



  Why Packages

Example, a package for emails handling, another for payment handling and so on.

Packages:

	• Keeps files together
	• Related to scope
	• Stop naming collisions
	• Relation with domain names
		○ Reversed:
			§ Comp220.csc.liv.ac.uk
		○ Package could be
			§ Uk.ac.liv.csc.comp220.utils

Make sure your packages are in the right directory (package name has to match dir name).
