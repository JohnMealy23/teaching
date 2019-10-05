## Syntax
"Syntax" just means "the ordering of words."  The concept of syntax is important here, because computers are inflexible dummies.  They only understand what you're trying to tell them if you say it just right.  If anything is wrong about the syntax, they throw a little fit, and refuse to do as they're told.


## Operators
Operators are the do-ers of programming.  There are a ton of them, and they all tell the computer to carry out some sort of operation.  `+`, for instance, is an operator that tells the computer to add two things together.  `-`, `*` and `/` are other operators you'll recognize.

There are other operators you might not be so familiar with.  Examples of these are...
  *  `typeof` - an operator to tell you the type of a value
  * `<`, `>`, `===` and `!=` - operators for telling if values are greater than, less than, equal to, or not equal to each other
  * `const` - an operator that tells the computer to make a variable.

"A variable?" you say.  "And what, prey tell, is a variable?"

Well, I'll tell you...


## Variables
Variables are the most basic bucket.  Everything is stored inside of them.  They can store just about any type of information - numbers, words, boolean (true|false), and more complex objects.

To define a variable, use the following syntax:
1. Begin by writing the operator `const` or the operator `let`.  (We'll get to the difference between these later.)
2. Immediately follow your `const` or `let` with the name of your variable.  The name of your variable shouldn't have any spaces, and also is prohibited from having certain special characters.  Try sticking to letters to begin with, to keep things simple.
3. After your variable name, add an `=`.
4. Finally, on the right-hand side of your `=`, add whatever value you'd like to store in the variable.  Whatever happens on the right-hand side of the equals is captured in your variable.

```javascript
const yourVariable = 12345
```

`yoVariableName` now holds the value `12345`

```javascript
const anotherVariable = yourVariable - 5
```

`anotherVariable` now equals `12340`

## Types
Variables all have types.  Examples of types are numbers, strings (words), boolean (true/false), arrays, and more complex objects.

Computers deal with each sort of type differently.  For instance, when you add strings together like this `'string1' + 'string2'` you get `'string1string2'`, but when you add two numbers together in the same manner (`5 + 1`), you get their sum (`6`).

Because of this, depending on the type, you'll need to know different rules, and use different tools.  We'll get more into these rules and tools later.  

One tool that's useful when trying to understand types is the operator `typeof`.  `typeof` can be used to identify what type a variable is. 

```javascript
const yourVariable = 'hello there'
const typeOfVariable1 = typeof yourVariable 
```

`typeOfVariable1` now equals `'string'`.

```javascript
const yourBool = true
const typeOfVariable2 = typeof yourBool 
```

`typeOfVariable2` now equals `'boolean'`.

### Numbers
Numbers are numbers.  Add them, subtract them, multiply them - you know the drill.  And remember that nomatter what you do with them, you can hold the result inside a variable.

```javascript
const result = 5 + 2 + 1 - 19 / 2
```

`result` now equals `1.5`

### String
A string is a series of characters.  That's all.  Just words.

Strings are created by putting single or double quotes around the necessary characters.  

Strings can be manipulated in many ways.  Two or more strings can be added together (concatenated), or searched through for "substrings".

Here's an example of concatenation:

```javascript
const str1 = 'words words'
const str2 = 'what a wonderful world'

const str3 = str1 + ' ' + str2
```

`str3` now equals `'words words what a wonderful world'`

Note how I dropped that `' '` in the middle?  I did this because computers are very literal. If I'd simply said `str1 + str2`, the computer would have taken me very seriously, and created this: `'words wordswhat a wonderful world'`. I told the computer to drop a space in between the two strings, so `'words'` and `'what'` wouldn't be fused togther.

## Arrays
Arrays are variables that can hold zero or more values.  They're buckets where you can hold as many other values as you'd like.  They're a good mechanism for putting groups of like things you'll need to reference later.

To make an array, use an opening square bracket (`[`), followed by a comma-separated list of variables or values, followed by a closing square bracket (`]`).  Here's an array that holds a bunch of strings:

```javascript
const thingsILike = [ 'ponies', 'swedish death metal', 'flowers', 'my mommy', 'teacher']
```

To reference something you've already added to an array, you need to reference it by its "index".  A item's "index" in an array is the number of where it occurs in the order of the array.  Indexes are zero-based, though, so the first item in an array is the zero-ith item.  It's index is `0`.  The array above has five items, so the last one has the index of `4`.

Here's how you'd access `'my mommy'` in the array above:

```javascript
const aLikeableThing = thingsILike[3]
```

The variable `aLikeableThing` now holds the value `'my mommy'`.

## Object (or "object literal")
An object is a mechanism for holding and organized information and functionality.  They are something of a bullet-point list that computers can read.

To make an object, use an opening curley bracket (`{`), followed by a closing curley bracket `}`.  

```javascript 
const emptyObject = {}
```

This creates an empty object - an object that holds no information.

To hold information in an object, one specifies the "key" or "index" for the each datum.  If the object is a neighborhood to the computer, the key is the data's home address.  You need to tell the computer the key, in order to add or access data in an object.  For every value you add to an object, there will also be a key.  

Here is the syntax for including a single key and value in an object when you create the object:

```javascript
const myObj = {
    myKey: 'some words'
}
```

`myObj` now holds a single key - `myKey`.  When you tell the computer you'd like to access the `myKey` key of `myObj`, the computer will give you the value `myKey` holds.  Here's the syntax for doing this:

```javascript
const result = myObj.myKey
```

The variable `result` now equals `'some words'`, because the computer knew to look into `myObj` at the `myKey` key, where we initially put the `'some words'` value.

Your object can also hold multiple key/value pairs.  Just separate them with commas as you include them:
```javascript
const myObj = {
    myKey: 'some words',
    anotherKey: 'some more words'
}
```

There are are also two ways of adding keys/values to objects, well after you've created the object - "dot notation" and "bracket notation."  Here's the rundown on these two bad boys:

#### Dot Notation:

Use `.`s (dots) followed by the key you'd like to use, and then tell the computer what that particular key should equal:

```javascript
const myObj = {}

myObj.aNumber = 5

myObj.anotherNumber = 6
```

`aNumber` and `anotherNumber` are now keys of the `myObj` object.  They hold the values `5`, and `6`, respectively.  Now that you've defined them, you can access them as follows:

```javascript
const theSum = myObj.aNumber + myObj.anotherNumber
```

Can you tell what the value of `theSum` variable is, above?  Give you a hint - it's a single number.

#### Bracket Notation

Another way of adding and accessing keys on an object is by using "bracket notation."  The following results in the exact same output as the dot notation example above.

```javascript
const myObj = {}

myObj['aNumber'] = 5

myObj['anotherNumber'] = 6
```

Note how you use a string (words surrounded by quotes) inside of the brackets.  Here's a slightly more abstract way to write *the exact same thing*!

```javascript
const myObj = {}

const key1 = 'aNumber'
const key2 = 'anotherNumber'

myObj[key1] = 5
myObj[key2] = 6
```

Because the variables `key1` and `key2` are each strings, they can be used as keys in your object.

Finally, note that dot notation and bracket notation can be used in tandem/interchangeably:

```javascript

const myObj = {}

myObj['aNumber'] = 5

const result = myObj.aNumber
```

In the above example, `result` will equal `5`, despite using bracket notation to define `aNumber` and dot notation to access it.

#### Nested Objects
This is gonna blow your goddam mind.  Objects can also hold other objects in their keys!

Whaaaaaaaaaaat?!

I know - what does that even mean?!  I'll tell you!

To nest an object within an object...
1. Define an object
2. Add a key to that object
3. Make the value of that key *another object*.  

Check it out:

```javascript
const myObj = {
    deeperObj: {
        value: 'hello there',
        value2: 'salutations'
    }
}
```

Looks a little busy, doesn't it?  Here's another way to write the same thing:

```javascript
const childObj = {
    value1: 'hello there',
    value2: 'salutations'
}

const myObj = {
    deeperObj: childObj
}
```

In the above example, we first define the `childObj` variable as an object with two keys - `value1` and `value2`.  We then create another object, `myObj` with a single key.  We make the value of that single key `childObj`, the initial object!

To access the values of `value1` and `value2`, use dot notations to walk down the levels of the object keys:

```javascript
const result = myObj.deeperObj.value2
```

`result` in the above example now equals `'salutations'`.


If objects aren't quite making sense, try thinking of them as bulletpoint lists.  Here's a bulletpoint list we can use as an example:

* todo:
    * groceries
        * produce
            * carrots
            * peaches
            * durian
        * meats
            * duck
            * unicorn
    * mall
        * shoes
        * corndog on a stick

Pretty simple, right?  We've got our over-arching bucket, "Todo", and under it we have subsections.  If we were to represent this with an object, it would look something like this:

```javascript
const todo = {
    groceries: {
        produce: [
            'carrots',
            'peaches',
            'durian'
        ],
        meats: [
            'duck',
            'unicorn'
        ]
    },
    mall: [
        'Shoes',
        'corndog on a stick'
    ]
}
```

This is a big one.  You'll note we're using arrays here - lists of items that start with an opening square bracket (`[`) and end with a closing square bracket (`]`).  

### If statements


let what
const swich = callToTheServerWithLoginInformation()

if (swich) {
  what = 'hello'
} else {
  what = 'goodbye'
}

// What does `what` equal?

