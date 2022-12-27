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
- When you make if statements **Don't** omit the braces. It makes the code more confusing.

## Classes
The functions within classes should be arranged in a specific order, To be decided.

## Comments
Don't use comments to explain what your code and variables do. Clean code explains itself.
> If you want to add info on a variable consider using the [tooltip] attribute.

> You can add XML tags to describe what a function does.
>![XML tag](/images/XMLtag.jpg "XML tag")
>![XML tag in action](/images/XMLtag_2.jpg "XML tag in action")

##General info
- Don't be afraid to type. Your variable name can be 100 characters long, as long as it explains what it does it's fine.
- Don't add stuff about petting jellies in the Jelly_Bath script. Scripts that carry more than one functionality are confusing and prone to breaking.
- Make it good, not perfect. Perfect code does not exist.
