# Hello World! Explanation

To run program open ConApp in Visual Studio and click "Run"

## Main Method

C# console app must contain a 'Main' method, in which control starts and ends. Main method 
is where you create objects and execute other methods. It is a static(1) method that resides 
inside a class or a struct. In the Hello World! above it resides in a class named "Hello." You
can declare the Main method in one the following ways:

-It can return a **void**.

```C#
static void Main()
{
	//...
}
```

-It can also return an integer.

```C#
static int Main()
{
	//...
	return 0;
}

-With either of the return types it can take arguments.

```C#
static void Main(string[] args)
{
	//...
}
```
or
```C#
static int Main(string[] args)
{
	//...
	return 0;
}

The parameter of the Main method, args, is a string array that contains the command-line arguments
used to invoke the program. Unlike in C++, the array does not include the name of the exe file. 

## Input and Output

C# programs generally use the input/output services provided by the run-time library of the .NET Framework.
The statement `System.Console.WriteLine("Hello World!");` uses the WriteLine method. This is one of the 
output methods of the Console class in the run-time library. It displays its string parameter on the 
standard output stream followed by a new line. Other Console methods are available for different input
and output operations. If you include the using System; directive at the beginning of the program, you 
can directly use the System classes and methods without fully qualifying them. For example, you can 
call `Console.WriteLine` instead of `System.Console.WriteLine`:

```C#
using System;

Console.WriteLine("Hello World");

```


(1)static modifier is used to declare a static member, which belongs to the type rathe than to a 
specific object


The following is declared as **static** and contains only **static** methods

```C#
static class CompanyEmployee
{
	public static void DoSomething(){
		/*...*/
	}
	public static void DoSomethingElse(){
		/*...*/
	}
}
```

A constant or type declaration is implicitly a static member.
A static member cannot be referenced through an instance. Instead it is referenced thorugh the type name.

```C#
public class MyBaseC
{
	public struct MyStruct
	{
		public static int x=100;
	}
}
```
To refer to the static member x, use the fully qualified name, MyBaseC.MyStruct.x, unless the number is 
accessible from the same scope:

```C#
Console.WriteLine(MyBaseC.MyStruct.x);
```


For more helpful C# lessons check out Microsoft's online guide: https://msdn.microsoft.com/en-us/library/67ef8sbd.aspx