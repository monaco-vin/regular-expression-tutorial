Regex Tutorial
This Regex tutorial is used to help you better understand what a regular expression is and how to decipher one yourself. A regex expression helps you create and find patterns of characters within a string or to find and replace a character. They can be tricky at first but once you get some practice they can straighforward.

Summary
In my tutorial I will be explaining and showing what the components are for a Hex Value expression. Hex Values are used mainly in formating colors in coding. In the example we have one that is six character long and one that is three characters long. Once you have reviewed my tutorial below you will have a better understanding of regular expressions and how they can be used.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)

## Regex Components

### Anchors

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

There are a few anchors the the first one being the (^) which as you can see in the above example of our hex value it uses the "^" at the beginning where it is suppose to be used. The other anchor that is shown above is the ($) which is shown at the end of the expression. These both together show the beginning and end of our Hex value express.

### Quantifiers

There are quite a few quantifiers.

The first being asterisk (\*) matches the item zero or more times. The next is the plus sign (+) which matches the item one or more times. The question mark (?) matches the item zero or one time.

The curley brackets ({}) works as a limiter on what goes inside. If were have {n} this matches the item exactly n number of times. We also have {n,} this matches the items at least n number of times. Lastly we have {n, m} this matches the items between n and m number of times.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

In the example are couple of quantifiers. The first one being the (?) which matches an item zero to one time. in this case since we have an OR operation. This means that we are only using one # in this case since it will either be a hex value of six or of three. this bring me into the next quantifier. The next one being the brackets ({}) which as explained above work as a limiter on what goes inside. In our case we has one with {6} and one with {3}. This means that one hex value will have six (#00FF00) characters and the other one will have only three (#000).

### Grouping Constructs

The group constructors is used to group different sections of your expression. Each section that uses parentheses is called a subexpression.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

In the example above we have one set of parentheses ([a-f0-9]{6}|[a-f0-9]{3}) so we only have one subexpression present in our example.

### Bracket Expressions

A bracket expression is an express that use brackets([]) to indicate a set of characters that we want to match. The brackets work like a "or" operator. For example if you had [978] it would read like [9 or 7 or 8]. It works with anything that is inside of it. You will often see it with ranges of letter like [a-z] or with numbers [0-9].

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

In our example above we have two sets of brackets being used. They both are doing similar things [a-f0-9] which we are look for a character between "a" and "f" lower case and 0 and 9.

### Character Classes

There are a few character classes as well when it comes to regular expressions. The character class help differentiate the kinds of characters that are being used.

The first is the period (.) which mtaches any character except for a newline. The next is (\d) which matches any (Arabic numeral) digit. There is also the (\w) which matches any alphanumeric character. Then lastly there is the (\s) which matches a single white space character like spaces and tabs.

We also have the inverse to match the capitalization of the characters. For example the inverse of \d would be \D same with \w would be \W and so on.

### The OR Operator

The OR operator (|) is just like how it sounds, we are looking for this item "or" that item and so on. It could be something like (9|8|7) where we are looking for 9 or 8 or 7.

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

In our example above we have a OR operation in the middle of our expression. The operation is say that it could either be our six hex value ([a-f0-9]{6} or our three hex value [a-f0-9]{3}.

## Author

My name is Vincent Monaco. I'm a student at the University of Texas Austin full-stack webdev bootcamp. I like ice hockey.

https://github.com/monaco-vin
