# Regex /[0-9a-zA-z]

Regex is a useful tool that developers can use to match certain strings based on what he or she specifies. It is widely used to simplify a string to your liking without the need of additional codes. This creates a better experience for the developer in terms of time and space complexity. An experienced developer will tend to use Regex over a novice because it cuts down the time and space complexity needed to run your code.

## Summary

In this tutorial, I will be talking about the Regex '/[0-9a-zA-Z]/g' as I have used this in the past and it is extremely useful in some cases. This specific Regex, '/[0-9a-zA-Z]', will allow the user to match the string only containing numerical and alpabetical values non-case sensitive, 0-9, a-z, and A-Z. As you can see in the brackets, '[0-9a-zA-Z]', this array contains what the user wants to match for his or her string so any non-numerical and non-alphabetical values will not be matched. For example, if the string was to be '123ABC!@# ABC', the Regex match would match '123ABCABC'. In addition, there is an assertion, caret symbol (^), plays an important role as well. If the caret symbol is outside of the brackets then it would match all of the things specified within the brackets. However, if the caret symbol is inside the brackets then it would match everything that is NOT those specified within the brackets. I like to use this for isPalindrome algorithm problems because if the string contains anything non-numerical, non-alphabetical and/or spaces, then I can use a simple replaceAll('/[^0-9a-zA-Z]/g', '') to replace everything except 0-9, a-z, and A-Z.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors
Anchors are a way to specify if you want to match something starting from the beginning of the string versus the end of the string. There are two examples of anchors that are widely used. These are '^' and '$'. These are called assertions. The ^ symbol will start from the beginning of the string versus the $ symbol will start from the end of the string.

The ^ symbol is called caret. Here is an example, if the string is '123ABC!@# ABC'. By using the Regex '/^[0-9a-zA-Z], this will start from the beginning which is the number 1 and it satisfies the Regex condition. The match will be the number 1.

The $ symbol is called what I like to call it as the 'end point' or 'end of the string'. Using as the same example, if the string is '123ABC!@# ABC'. By using the Regex '/$[0-9a-zA-Z], this will start from the end of the string which is the letter C and it satisifies the Regex condition. The match will be the letter C.

### Quantifiers
Quantifiers are ways to indicate how many of the characters to appear on the string or expression. An example of a quantifier is 'x+'.
This specific quantifier checks for a match depending on the character before the plus sign. For example if the Regex is '/A+' then it looks for all A's in the string. If the string was '123ABC!@#ABC' then it would match both A's. There are other quantifiers that can be useful in some cases.

### OR Operator


### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
