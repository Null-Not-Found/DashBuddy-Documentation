
# Coding conventions



## Pascal Case

Use pascal casing when naming a **class** or **method**.

```cs
Public Class NewClass();

public void NewMethod();
```
***

Use pascal casing when naming an **interface** and prefix it with a capital **I**.
```cs
Public Interface INewInterface();
```
***

## camel Casing

Use camel casing when naming **variables**.

```cs
string newVariable = "text";
int anotherVariable = 3;
```
***

When naming **parameters** , use camel casing and prefix them with **\_**.

```cs
public void NewMethod(_methodParamater);
```
***

## CAPITAL_SNAKE_CASING

For **constant variables** use snake casing with al capital letters.

```cs
const string NEW_CONSTANT = "text";
const int ANOTHER_CONSTANT = 3;
```
***

## Layout conventions

Only write one **statement** per line.

Only write one **declaration** per line.

```cs
const string newConstant = "text";
newConstant = "number";
```
***

Add at least one blank line between **method definitions** and **property definitions**.

```cs
bool Method1()
{

}

bool Method2()
{

}
```
***

When writing **if** or **if else** statements use **brackets ()** for the Hypotheses and use **braces {}** for the conclusion when possible.

```cs
if (Statement == true)
{
  DoThis();
}
```
***

Immediately return **if** statements when using methods where possible, as of the following example.

```cs

string apple = "apple";
string apple = "pear";

DoThis()
{
  return (apple == pear);
}

NotThis()
{
  if (apple == pear)
  {
    return true;
  }

  return false;
}

```
***

When writing multiple **if** statements use **defensive programming**.

```cs
if ()
{
  // exception
}

if ()
{
  // exception
}

if ()
{
  // exception
}

// Usual program

```
***

## Commenting conventions

Place the commented line in a separate line of the code.

Always start the comment with an uppercase letter.

Place a blank line on either side between the comment and the lines of code.

Place one space between the **comment delimiter (// or \* for example)** and the commented text.

```cs

// Comment with capital c
// And with a space of cource

```

When commenting **methods** or **statements** , always put the comment directly above the **method** or **statement** in question.

```cs
bool Method()
{

}

// This method s*cks

bool Method2()
{

}
```

## Data type

When assigning a **data type** to a **variable** , don't use **unsigned data types** if possible.


```cs
// Use

string newVariable = "text";

// Don't use

var newVariable = "text";

```

## Exception handling

Only write **exceptions** for parts of the program the user shouldn't be able to reach in normal use.

Always provide an **error message** when making an **exception**.

Provide the data of **variables** that could cause the **exception** in the **error message** when possible.

```cs
string thisMayFail = "it failed";

throw new Exception("code failed becouse variable was + ");

```

Try to avoid **catching** an **exception** as much as possible but use **if statements** instead.

```cs

DoThis()
{
  return (apple == pear);
}

if (DoThis())
{
  // It failed
}

void NotThis()
{
  if (apple == pear)
  {
    throw new Exception();
  }
}

try
{
  NotThis()
}
catch
{
  // It failed
}
```

### Made by [Bram Verkuijlen](https://github.com/BramVerkuijlen)
