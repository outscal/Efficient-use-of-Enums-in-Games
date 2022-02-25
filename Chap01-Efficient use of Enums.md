# Efficient-use-of-Enums-in-Games

```csharp
public enum Levels {LevelOne,LevelTwo,LevelThree};
```

In the above code “Levels” is the typename that we used to define the levels of the game. To understand what’s inside the brackets { }, let’s see another example here.

Suppose we would want to declare a ****variable's value as constant and tell the compiler to prevent the programmer from modifying it. Say, we want to have LevelOne variable as constant. 

.

```csharp
const int LevelOne=3;
const int LevelTwo=23;
const int LevelThree=56;
```

These are the constants that we want to initialize in our program (Must be for a reason). This is because we wanted each of the variables to identify them uniquely. Following up with conditions, each of the levels would do some operation. Let’s summarize this. What are we doing here????? haaaa??????? We are actually maintaining game states. This is where we will learn about the uses of enums in games. It’s like, LevelOne would do something, LevelTwo would do something, and likewise LevelThree. To pick them up and use them accordingly we gave some constant values to them. 

```csharp
if(LevelOne==3){
	Debug.Log("You are in Level One");
}
else if(LevelTwo==23){
	Debug.Log("You are in Level two");
}
else if(LevelThree==56){
	Debug.Log("You are in Level Three");
}
```

Now, what if some other guy comes in and changes the value of LevelTwo=7 in the initialization without looking at the whole code. What would happen??? 🤔

The whole code would crash right? The follow-up condition for LevelTwo would become wrong. So, to not have those changes we can replace those constant variables with enums.

```csharp
public enum Levels {LevelOne,LevelTwo,LevelThree};
```

In enums, the variables inside the brackets { } store values 0 from left to 65,536 serially, just like an array. These integer values are actually constants and you can’t change them later on in the program. This way it makes it easier to maintain the game states in a game.

```csharp
public Levels levelState=Levels.LevelOne;
```

This is an easy way to keep track of the current state of a behaviour, entity, or class.

```csharp
switch(levelState){
	case LevelOne:
				Debug.Log("You are in Level One");
				break;
	case LevelTwo:
				Debug.Log("You are in Level two");
				break;
	case LevelThree:
				Debug.Log("You are in Level Three");
				break;
}
```

Here, you can’t even change the values of LevelOne, LevelTwo, and LevelThree later on after initializing it with enums.

Enums are mainly used to maintain game states in games. It makes the code look a lot cleaner and much readable. Do play around with it. It’s a lot exciting than you think!! 🤪
