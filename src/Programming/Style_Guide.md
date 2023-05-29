# Style Guide

Given that P1 is a large group, we will have a wide range of programmers on the team. Everyone will have different skill levels and different conventions for their programming. Hence, the style guide is one of the most important aspects to understand. This way, everyone can be on the same page when we work on tasks.
 
The style guide aims to inform you on general programming practices, naming conventions, comments, the order of members in classes, private declaration, some details for serialization in Unity, and information for using lambda delegates in C#.

## General programming practice

- Make it good, not perfect. Perfect code does not exist.
- Focus on readibility, what is understood by you might not be to others especially months or years down the line.
    - Don't worry about the length of a script and try to compact your code. 
	- Space out your lines if it provides better readibility.
- Try and keep each line less than 100 characters long.
- Keep every script relevant to itself. 
    - Don't add stuff about petting jellies in the Jelly_Bath script. Scripts that carry more than one functionality are confusing and prone to breaking.
- Don't hardcode values. Even if it shouldn't appear in the inspector declare it in a variable.

```csharp
// Do this
private const _thisVariablesDoesThis = 5; //Unmodifiable

private void Function()
{
	// Here we know what both variables are.
	thisVariableDoesSomething += thisVariablesDoesThis; 
}
// Don't do this
private void Function()
{
	thisVariableDoesSomething += 5; // Why are we increasing it by 5?
}
```

 - When you write “if” statements, instead of shortening the code without brackets “{},” it is better to include them, likewise for the other type of code where the brackets can be left out.

```csharp
// Do this
if()
{
	//Do stuff
}

while()
{
	//Do stuff
}

//Don't do this
if()
	//Do stuff
	
While() //Do stuff

//Also Don't do this
if(){
	//Do Stuff
} 
```

## Naming Convensions 

The importance of a naming convention makes the code easier to read.

### Variables

- Use camelCase to name variables.
- Private variables should start with an underscore(_).
- If your variable is a boolean the name should be asking a question.
- Avoid special characters, it can affect how the editor reads the names.
- Your variable names can be 100 characters long and should describe what it does.

```csharp
// Do this
private int _healthPoints;
private bool _hasItem;

//Don't do this:
private int PlayerChar;
private bool A;
private string PSText;
```

### Functions
- Function names will use **PascalCase**.

- If a function triggers an event it's name should start with an OnEventName.
Example:
```csharp
private void OnDoorOpened()
{
	//Do stuff
}
```
- If it returns a boolean the name should be asking a question. Example:
```csharp
private bool IsPlayerDead()
{
	return _isPlayerDead;
}
```

## Privacy/Access Modifiers

Access modifiers are the public, protected, and private keywords used before a class and any members of that class like variables, methods, enums, etc. Leaving off the access modifier it is automatically considered private. We will be requiring to explicitly say that a class and its members are private.

Try to keep your variables as private as possible. That way we have better control of when and how scripts alter them.
There is no harm in accessing a variable from another class. Be more concerned about changing the value from another class.
- Make sure if you need a class or class member protected, or public to write that access modifier. You will not find it due to it being private automatically.
- *[Here](https://methodpoet.com/why-you-need-private-variables/)* is a webpage explaining the importance of privacy and access modifiers in further detail

```csharp
// Do this
private int _variable; // safest approach

[Serialized Field, Tooltip("Can be altered in the inspector")] 
private int _variable;

//working with properties (getters and setters)
private int _variable;
public int Variable 
{
	get {return _variable;} // can be read from anywhere
	private set {_variable=value;} // set from this class only
}

[field:SerializeField, Tooltip("same as above, but Unity creates a backupfield so you can set it in the inspector")] 
public float MyFloat3 { get; private set; }
```

## Comments
Don't use comments to explain what your code and variables do. Clean code explains itself.
Most of the time comments should explain **WHY** the code does someting **NOT HOW**.

If it is necessary to write a piece of code that is not ordinary and it was the only way. 
- Make a comment why you have done it this way.

If the task you are working on still has something left to do that goes farther than your task card intended. 
- Add a TODO comment. Example: `//TODO: *what needs to be done*`
- Make a task card for the TODO comment and refer to it. Programming Task Card: *[HERE](https://trello.com/c/SKyJmHHW/1037-template-for-creating-programming-tasks)* 
    - Make sure to specify the task you were working on and that task will need to be merged first.


## Ordering of classes
The functions within classes should be arranged in a specific order.
When we write classes , there is a specific order to keep in mind. Keeping a consistent order promotes readibility. The typical order is Declarations -> Events -> Private Functions -> Public Functions. Or better illustrated with the image below.

```csharp
public class ClassName : MonoBehaviour
{
	//Variable Declarations
	private int _intVariable;
	private float _floatVariable;

	public string stringObject;
	public bool isABool;

	Enum Declarations
	
	Unity Events
	- OnValidate()
	- OnEnable()
	- Awake()
	- Start()
	- Update()
	
	Private Functions
	
	Public Functions
	- Custom functions
	- Get/Set Methods
	
}
```

## Lambda Expressions and Delegates

Lambda expressions in C# are used like anonymous functions, with the difference that in Lambda expressions you don’t need to specify the type of the value that you input thus making it more flexible to use. 

When you see “=>” in C#, you see a lambda expression. It is a way to shorthand a function call to return a value to a variable in the middle of your code.

For example:

```csharp
public Float CurrentHealth => (energy * baseHealth)-damage;
```

Acts like a function with body:

```csharp
{
  return (energy * baseHealth)-damage;
}
```

But you can call it without brackets though, like :
```csharp
 if(CurrentHealth > 0)
```

The left of the “=>” operator is the input, and to the right is the expression. Lambdas are a bit advanced, which will be better understood through the video below.
Action delegates are a unique way of writing function calls. With delegates, you can make a function like a variable that can be passed. Once again, it is advanced and better understood through the video below.
https://www.youtube.com/watch?v=3ZfwqWl-YI0