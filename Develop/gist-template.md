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
The OR operator is exactly the same as it is intended in Javascript. The OR operator, also called the Pipe symbol '|', means the either the first condition or the second. For example if the Regex is '/A|B' then the matching characters would be both either A OR B. In this same example if the string was '123ABC!@#ABC' then the matching characters would be A OR B.

### Character Classes
A character class is the prime exactly I am using for this study guide, '/[0-9a-zA-Z]'. It is simply the range within the brackets that will match the string. You can specify the range to match what you desire. If the Regex was to be '/[0-9]' indicating I would like to match only numbers within the string then the previous example string '123ABC!@#ABC' would match numbers 123 only, returning 3 matches. The user can customize the range with the hyphen to limit or widen his or her search.

### Flags
An example of flag is the letter 'g' after the expression. It is optional but if the user would like to widen his or her search for matches then he or she can perform a global search with the flag. In my previous example in the summary, I used the replace method with the '/[^0-9a-zA-Z]/g'. This is a good way to search for edge cases that are unexpected. There are several other flags that can be used specifically for edge cases but I've used the 'g' after an expression and it has been extremely helpful in limiting my matches.

### Grouping and Capturing
Grouping and capturing are related topics when matching expressions. They can be stored and extracted for usage. This is done by using parentheses, (). For example, '/(ABC)/g', being used to match the following string '123ABC!@#ABC' will match both the ABC in the string. This will display the matches into an array for the user to access. [ABC, ABC].

### Bracket Expressions
A bracket expression, [], is simply a bracket that will contain the characters that the user would like to match within the bracket. In this study guide, we talked about '/[0-9a-zA-Z]' which means the bracket expression contains all numerical values, all alphabetical values case insensitive. In the same example we have been using, if the string is '123ABC!@#ABC' then the bracket will match all values that are numerical and alphabetical resulting in 123ABCABC.

### Greedy and Lazy Match
A greedy and lazy, non-greedy, match are the opposite of one another. A greedy match would match the longest possible string while the lazy, also known as non-greedy, will match the shortest possible string. For example, a greedy match 'a.*b' on a string 'aasabbqweohagbadsbbb' would make the entire string from a to b from the first letter a to the last better b making it a greedy match. On the other hand, a lazy match 'a.*?b', using the same string 'aasabbqweohagbadsbbb' would make the match up until it reaches the first letter b resulting in aasab.

### Boundaries
Boundaries are used in assertions. There are several types of boundary type assertions. One of these cases are the caret symbol, ^, which is used to indicate whether to match the first character of the string if it is outside of a bracket expression or to match with all characters that are not inside the bracket expression. For example '/^[0-9a-zA-Z]' on a string '123ABC!@#ABC' would match with the first character which is 1 while '/[^0-9a-zA-Z]' would match with all the non-numerical and non-alphabetical characters which is !@#.

### Back-references
A back-reference is a way to say that something was matched previously and reuse it. The expression is used by the back slash symbol, '\'. For example if the Regex was '/hello\sworld' for the string 'hello world this is regex!' then the matching characters would be hello world.

### Look-ahead and Look-behind
Look ahead and look behind are assertions that seems very useful in some cases. The look ahead will only match characters by looking for the match ahead of the characters the user has chosen. The look ahead uses the expression '(?= pattern)' while the look behind uses the expression '(?<= pattern)'. Here are some examples, imagine the string is 'orange juice is better than apple juice'. For the look ahead, if we want to match orange but also look ahead of orange to match the pattern otherwise there is no match. We simply use the Regex /orange(?= juice)/ such that orange is a match but we have to look at the next string if it is juice. Similar with look behind, we use the Regex, /(?<=orange )juice/, to match the juice and look behind if the string is orange.

## Author
This is a short summary of myself who had no knowledge of Regex until I started writing up this study guide on one of the most common used Regex I have encountered, /[0-9a-zA-Z]. I've been using this Regex without the full knowledge of how it actually works and so I wanted to start digging deeper into depth of Regex. Now I have some knowledge of how Regex works and hopefully this study guide will help guide you towards success as well. 

Here is a link of my GitHub Profile: https://github.com/Michaelx626.

