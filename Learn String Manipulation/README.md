# Learn String Manipulation By Building a Cipher

## Author

Ivan Estropigan

## Python is a powerful and popular programming language widely used for data science, data visualization, web development, game development, machine learning and more

In this project, you'll learn fundamental programming concepts in Python, such as variables, functions, loops, and conditional statements. You'll use these to code your first programs.

## Step 1

Variables are an essential part of Python and any programming language. A variable is a name that references or points to an object. You can declare a variable by writing the variable name on the left side of the assignment operator = and specifying the value to assign to that variable on the right side of the assignment operator:

```csharp
variable_name = value
```

Create a variable called number and assign the value 5 to your new variable.

## Step 2

Variables can store values of different data types. You just assigned an integer value, but if you want to represent some text, you need to assign a string. Strings are sequences of characters enclosed by single or double quotes, but you cannot start a string with a single quote and end it with a double quote or vice versa:

```csharp
string_1 = "I am a string"
string_2 = 'I am also a string'
string_3 = 'This is not valid"
```

Delete your number variable and its value. Then, declare another variable called text and assign the string 'Hello World' to this variable.

```csharp
text = 'Hello World'
```

## Step 3

You can use the built-in function print() to print the output of your code on the terminal.

Functions are reusable code blocks that you can call, or invoke, to run their code when you need them. To call a function, you just need to write a pair of parentheses next to its name. You will learn more about functions very soon.

For now, go to a new line and add an empty call to the print() function. You should not see any output yet.

```csharp
text = 'Hello World'
print()
```

## Step 4

An argument is an object or an expression passed to a function — added between the opening and closing parentheses — when it is called:

```csharp
greet = 'Hello!'
print(greet)
```

The code in the example above would print the string 'Hello!', which is the value of the variable greet passed to print() as the argument.

Print your text variable to the screen by passing the text variable as the argument to the print() function.

```csharp
text = 'Hello World'
print(text)
```

## Step 5

Each string character can be referenced by a numerical index. The index count starts at zero. So the first character of a string has an index of 0. For example, in the string 'Hello World', 'H' is at index 0, 'e' is at index 1, and so on.

Each character of a string can be accessed by using bracket notation. You need to write the variable name followed by square brackets and add the index of the character between the brackets:

```csharp
text = 'Hello World'
r = text[8]
```

Now, instead of printing text, print just the character at index 6.

```csharp
text = 'Hello World'
print(text[6])
```

## Step 6

You can also access string characters starting from the end of the string. The last character has an index of -1, the second to last -2 and so on.

Now modify your existing print() call to print the last character in your string.

```csharp
text = 'Hello World'
print(text[-1])
```

## Step 7

You can access the number of characters in a string with the built-in len() function.

Modify your existing print() call by passing len(text) instead of text[-1].

```csharp
text = 'Hello World'
print(len(text))
```

## Step 8

You can see 11 printed on the terminal because 'Hello World' contains 11 characters.

Another useful built-in function is type(), which returns the data type of a variable. Modify your print() call to print the data type of text.

```csharp
text = 'Hello World'
print(type(text))
```

## Step 9

As you can see, the output of printing type(text) is <class 'str'>, which means that your variable is a string, indicated as str.

Now go to a new line and create another variable called shift and assign the value 3 to this variable.

```csharp
text = 'Hello World'
shift = 3
print(type(text))
```

## Step 10

And now print your new variable.

```csharp
text = 'Hello World'
print(type(text))
shift = 3
print(shift)
```

## Step 11

Modify your print(shift) call to print the data type of your shift variable.

```csharp
text = 'Hello World'
print(type(text))
shift = 3
print(type(shift))
```

## Step 12

Key aspects of variable naming in Python are:
    - Some words are reserved keywords (e.g. for, while, True). They have a special meaning in Python, so you cannot use them for variable names.
    - Variable names cannot start with a number, and they can only contain alpha-numeric characters or underscores.
    - Variable names are case sensitive, i.e. my_var is different from my_Var and MY_VAR.
    - Finally, it is a common convention to write variable names using snake_case, where each space is replaced by an underscore character and the words are written in lowercase letters.

Remove both calls to print() and declare another variable called alphabet. Assign the string 'abcdefghijklmnopqrstuvwxyz' to this variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
```

## Step 13

You are going to use the .find() method to find the position in the alphabet of each letter in your message. A method is similar to a function, but it belongs to an object.

```cs
sentence = 'My brain hurts!'
sentence.find('r')
```

Above, the .find() method is called on sentence (the string to search in), and 'r' (the character to locate) is passed as the argument. The sentence.find('r') call will return 4, which is the index of the first occurrence of 'r' in sentence.

At the end of your code, call .find() on alphabet and pass 'z' as the argument to the method.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

alphabet.find('z')
```

## Step 14

The first kind of cipher you are going to build is called a Caesar cipher. Specifically, you will take each letter in your message, find its position in the alphabet, take the letter located after 3 positions in the alphabet, and replace the original letter with the new letter.

To implement this, you will use the .find() method discussed in the previous step. Modify your existing .find() call passing it text[0] as the argument instead of 'z'.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
alphabet.find(text[0])
```

## Step 15

The print() function gives you only an output in the console, but functions and methods can have a return value that you can use in your code.

Now assign alphabet.find(text[0]) to a variable named index. In this way, index will store the value returned by alphabet.find(text[0]).

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
```

## Step 16

Next, print the index variable to the console.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
print(index)
```

## Step 17

.find() returns the index of the matching character inside the string. If the character is not found, it returns -1. As you can see, the first character in text, uppercase 'H', is not found, since alphabet contains only lowercase letters.

You can transform a string into its lowercase equivalent with the .lower() method. Add another print() call to print text.lower() and see the output.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0])
print(index)
print(text.lower())
```

## Step 18

Remove the last print() call. Then, instead of text[0], pass text[0].lower() as the argument to your .find() call and see the output.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)
```

## Step 19

Declare a new variable named shifted. Use the bracket notation to access the value of alphabet at index index and assign it to your new variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)
shifted = alphabet[index]
```

## Step 20

Print your shifted variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)
shifted = alphabet[index]
print(shifted)
```

## Step 21

As you can see from the output, 'h' is at index 7 in the alphabet string. Now you need to find the letter at index 7 plus the value of shift. For that, you can use the addition operator, +, in the same way you would use it for a mathematical addition.

Modify your shifted variable so that it stores the value of alphabet at index index + shift.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
index = alphabet.find(text[0].lower())
print(index)
shifted = alphabet[index + shift]
print(shifted)
```

## Step 22

Repeating the process of locating the letter inside the alphabet and determine the shifted letter for each character in text can be tedious. Thankfully, you can simplify it using a loop.

For now, remove all the lines of code below the declaration of the alphabet variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
```

## Step 23

A loop allows you to systematically go through a sequence of elements and execute actions on each one.

In this case, you'll employ a for loop. Here's how you can iterate over text:

```cs
for i in text:
```

for is the keyword denoting the loop type. i is a variable that sequentially takes the value of the elements in text. The statement ends with a colon, :.

Below the line where you declared alphabet, write a for loop to iterate over text. Use i as the loop variable.

Doing so, there is an error in the terminal. You will learn about it in the next step.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'
for i in text:
```

## Step 24

The code to execute at each iteration — placed after the : — constitutes the body of the loop. This code must be indented. In Python, it is recommended to use 4 spaces per indentation level. This indented level is a code block.

```cs
for i in text:
    print(i)
```

Python relies on indentation to indicate blocks of code. A colon at the end of a line is a signal that a new indented block of code will follow.

So, when no indented block is found after the final colon, the code execution stops and an IndentationError is thrown. This code will not show the output and instead raise an IndentationError:

```cs
for i in text:
print(i)
```

Give your for loop a body by adding a call to print(i). Remember to indent the loop body.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for i in text:
    print(i)
```

## Step 25

The iteration variable can have any valid name, but it's convenient to give it a meaningful name.

Rename your i variable to char.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    print(char)
```

## Step 26

Inside the for loop, before printing the current character, declare a variable called index and assign the value returned by alphabet.find(char) to this variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    index = alphabet.find(char)
    print(char)

```

## Step 27

Currently, the print() function is taking a single argument char, but it can take multiple arguments, separated by a comma.

Add a second argument to print(char) so that it prints the character and its index inside the alphabet.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text:
    index = alphabet.find(char)
    print(char, index)
```

## Step 28

find is again returning -1 for uppercase letters, and for the space character, too. You are going to take care of the space later on.

For now, instead of iterating over text, change the for loop to iterate over text.lower().

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
```

## Step 29

At the end of your loop body, declare a variable called new_index and assign the value of index + shift to this variable.

```cs
text = 'Hello World'
shift = 3
alphabet = 'abcdefghijklmnopqrstuvwxyz'

for char in text.lower():
    index = alphabet.find(char)
    print(char, index)
    new_index = index + shift
```

## Step 30

Strings are immutable, which means they cannot be changed once created. For example, you might think that the following code changes the value of my_string into the string 'train', but this is not valid:

```cs
my_string = 'brain'
my_string[0] = 't'
```

Confirm that by using the bracket notation to access the first letter in text and try to change it into a character of your choice. You will see the ouput disappear and an error appear.

```cs
text = 'Hello World'
text[0] = 'h'
```

## Step 31

When you try to change the individual characters of a string as you did in the previous step, you get a TypeError, which occurs when an object of inappropriate type is used in your code.

As you can see from the error message, strings do not support item assignment, because they are immutable. However, a variable can be reassigned another string:

```cs
message = 'Hello World'
message = 'Hello there!'
```

Delete the text[0] line and reassign text the string 'Albatross'.

## Step 32

As you can see, each character of the reassigned string gets printed inside the loop.

Go back to the original string by deleting the text reassignment.

## Step 33

Now you need to create a new_char variable at the end of your loop body. Set its value to alphabet[new_index].

## Step 34

Next, print new_char and see the output.

## Step 35

Clean the output a bit. Delete print(char, index), and turn the last print() call into print('char:', char, 'new char:', new_char).

## Step 36

At the moment, the encrypted character is updated in every iteration. It would be better to store the encrypted string in a new variable. Before your for loop, declare a variable called encrypted_text and assign an empty string ('') to this variable.

## Step 37

Now, replace new_char with encrypted_text. Also, modify the print() call into print('char:', char, 'encrypted text:', encrypted_text) to reflect this change.

## Step 38

Instead of assigning alphabet[new_index] to encrypted_text, assign the current value of encrypted_text plus alphabet[new_index] to this variable.

## Step 39

You can obtain the same effect of a = a + b by using the addition assignment operator:

```cs
a += b
```

The addition assignment operator enables you to add a value to a variable and then assign the result to that variable.
Use the += operator to add a value and assign it at the same time to encrypted_text.

## Step 40

Comparison operators allow you to compare two objects based on their values. You can use a comparison operator by placing it between the objects you want to compare. They return a Boolean value — namely True or False — depending on the truthfulness of the expression.

Python has the following comparison operators:

```cs
Operator | Meaning
== | Equal
!= | Not equal
>  | Greater than
<  | Less than
>= | Greater than or equal to
<= | Less than or equal to
```

At the beginning of your loop body, print the result of comparing char with a space (' '). Use the equality operator == for that.