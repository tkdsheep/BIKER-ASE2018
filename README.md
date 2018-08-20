# BIKER-ASE2018
The dataset and source code for paper "API Method Recommendation without Worrying About the Task-API Knowledge Gap"

The code is based on Python 2.7.12. The required packages are listed below:

numpy 1.13.3
gensim 3.2.0
nltk 3.2.5

In the main package, running test.py will output the evaluation result of BIKER (method-level recommendation) with our dataset. Running test_api_class.py will output the result of class-level recommendation.

The online.py file allows you to input any query online, and output the recommended top-5 API methods, along with the API summary. This file may take 30~60 seconds to preprocess the data (just once) before receiving your queries.

Below we listed two examples, the output for query "run linux commands in java code" and query "Check if a class is subclass of another class in Java?"

Query 1: run linux commands in java code

Rank 1 : java.lang.Runtime.exec
>>>JavaDoc<<<
Executes the specified string command in a separate process.
>>>Relevant Questions<<<
1.Run cmd commands through java
2.use cmd commands in java program
3.Unable to execute Unix command through Java code
>>>Code Snippets<<<
/**********code snippet 1 **********/
Process p = Runtime.getRuntime().exec(command);

/**********code snippet 2 **********/
Runtime.exec( -whatever cmd command you need to execute- )

/**********code snippet 3 **********/
String command1 = "mv $FileName /bgw/feeds/ibs/incoming/";
Runtime.getRuntime().exec(command1);

-----------------------------------------------

Rank 2 : java.lang.System.exit
>>>JavaDoc<<<
Terminates the currently running Java Virtual Machine.
>>>Relevant Questions<<<
1.See java exit code in Unix

-----------------------------------------------

Rank 3 : java.lang.ProcessBuilder.command
>>>JavaDoc<<<
Sets this process builder's operating system program and arguments.
>>>Relevant Questions<<<
1.Running a bash shell script in java

-----------------------------------------------

Rank 4 : java.lang.ProcessBuilder.inheritIO
>>>JavaDoc<<<
Sets the source and destination for subprocess standard I/O to be the same as those of the current Java process.
>>>Relevant Questions<<<
1.Running CMD from Java

-----------------------------------------------

Rank 5 : java.lang.ProcessBuilder.start
>>>JavaDoc<<<
Starts a new process using the attributes of this process builder.
>>>Relevant Questions<<<
1.Running a bash shell script in java
>>>Code Snippets<<<
/**********code snippet 1 **********/
Process p = new ProcessBuilder("myCommand", "myArg").start();

-----------------------------------------------

Query 2: Check if a class is subclass of another class in Java?

Rank 1 : java.lang.Class.getSuperclass
>>>JavaDoc<<<
Returns the Class representing the superclass of the entity (class, interface, primitive type or void) represented by this Class.
>>>Relevant Questions<<<
1.How do I determine if a class extends another class in Java?
>>>Code Snippets<<<
/**********code snippet 1 **********/
Class<?> c = obj.getClass();
System.out.println(c.getSuperclass() == Some.class);

-----------------------------------------------

Rank 2 : java.lang.Class.isAssignableFrom
>>>JavaDoc<<<
Determines if the class or interface represented by this Class object is either the same as, or is a superclass or superinterface of, the class or interface represented by the specified Class parameter.
>>>Relevant Questions<<<
1.Check in compile time if someClass.class is derived from a anotherClass.class?
2.How to check if a subclass is an instance of a class at runtime?
>>>Code Snippets<<<
/**********code snippet 1 **********/
anotherClass.class.isAssignableFrom( someClass.class );

-----------------------------------------------

Rank 3 : java.lang.Class.isInterface
>>>JavaDoc<<<
Determines if the specified Class object represents an interface type.
>>>Relevant Questions<<<
1.Check in compile time if someClass.class is derived from a anotherClass.class?

-----------------------------------------------

Rank 4 : java.lang.Class.forName
>>>JavaDoc<<<
Returns the Class object associated with the class or interface with the given string name.
>>>Relevant Questions<<<
1.Check if a string is instance of a Class in Java

-----------------------------------------------

Rank 5 : java.lang.Class.isEnum
>>>JavaDoc<<<
Returns true if and only if this class was declared as an enum in the source code.
>>>Relevant Questions<<<
1.Checking if a class is java.lang.Enum
>>>Code Snippets<<<
/**********code snippet 1 **********/
if (obj.getClass().isEnum()) {

...
}

-----------------------------------------------

