# Style Guide

## Variables 

- Use camelCase to name variables.
- If your variable is a boolean the name should be asking a question. 
- Avoid special characters, it can affect how the editor reads the names.

		Do this: private int healthPoints;
				 private bool hasItem;
		Not this: private int PlayerChar;
				  private bool A;
				  private string PSText;

## Functions
- Function names will use **PasclaCase**.
- If it's a boolean name should be asking a question.
		Private void IsPlayerDead(){}

## Events
If a function triggers an event it's name shuold start with a ONEventName.
		private void OnDoorOpened(){}
		
## Brackets
Construction sounds

## Classes
The functions within classes should be arranged in a specific order, To be decided.

## Comments
Don't use comments to explain what your code and variables do. Clean code explains itself.
> If you want to add info on a variable consider using the [tooltip] attribute.

> You can add XML tags to describe what a function does.
>![XML tag](/images/XMLtag.jpg "XML tag")
>![XML tag in action](/images/XMLtag_2.jpg "XML tag in action")