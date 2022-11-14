# URL Regex Tutorial

This is a tutorial explaining how to read or write regex (or a regular expression) using a search pattern for matching a URL.

## Summary
</br>

A regular expression, or regex, is a written search pattern. It is typically used to search for or validate certain strings or patterns of text. Regular expressions are useful because they provide flexible pattern matching while also being able to include search criteria. Regex can also be used in almost any programming language!

In this walkthrough, we will be talking about a regular expression written to match a URL string. 
Like so - `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

https://www.google

We will go through each component included in the expression, explaining what it does and the role it plays within the expression. If you need information on a particular component, use the table of contents below to skip ahead.

</br>

## Table of Contents
</br>

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping and Capturing](#grouping-and-capturing)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components
</br>

Regular expressions can match text patterns using both "literal" characters and "meta" characters. 

A literal character is used to match a character pattern literally, such as the lowercase letter "a".

A meta character is used to define the search criteria and text manipulations.

</br>

### Anchors
</br>

Anchors are a regex component that does not match a character, but instead asserts something about the searched for string or the matching process. Anchors specify a current position in the string.

Take this string of regex from our URL match for example, `/^(https?:\/\/)`. The carat `^` in the second position of the string denotes that there is a placement requirement. Here it is specifying that the pattern of characters being matched by `(https?:\/\/)`, must be at the start of the string.

Think of a typical URL, the string begins with something like: `https://`.

</br>

### Quantifiers
</br>

Quantifiers are what they sound like, specifying the quantity of the characters or group of characters being matched. This requirement can be very exact, like searching for exactly 3 lowercase letter 'a's (like so, `a{3}`). It can also cover a broader range of characters, like searching for zero or more lowercase letter 'a's (like so, `a*`).

In our regular expression example, this string - `([\da-z\.-]+)`, uses the quantifier `+` to denote that we are searching for one or more characters matching the `[\da-z\.-]` paramater (which we'll explain later in bracket expressions).

This piece of the regex string is essentially looking for any digit, lowercase letter, period, or dash. As in the letter string, `www` from the URL `https://www.google.com/`.

</br>

### Grouping and Capturing
</br>

Using parantheses or round brackets around part of the regular expression can group part of the expression together. This is done so that a quantifier, anchor, or other specification can be applied to the entire group contained within. Parentheses can also create what is called a "numbered capturing group", storing part of the string matched by a part of the regular expression inside the parentheses, so that you can apply the search pattern to the part of the string outside of the parentheses OR apply it to what is outside and what is inside the parentheses.

Using our URL matching regex, we have several examples of grouping. In our string used above to explain anchors, `(https?:\/\/)` is grouped with the `?` following. The quantifier, `?`, specifies that there should be zero or one of the entire matched expression, `https?:\/\/`, which is contained inside the parentheses.

This applies to the beginning of any url that may start with `https://`, `http://`, or even have neither (or zero) of these and follow the `www.google.com` syntax.

</br>

### Character Classes
</br>

Character classes are also sometimes known as character sets. With character classes, the regex engine can be told to match only one of many characters. All of the characters you may wish to match simply need to be included inside of square brackets.

Inside of this portion of our URL expression, `([a-z\.]{2,6})`, we can see the bracketed expression `[a-z\.]`, stating that in this place we are looking to match one of any character `a` through `z`, or the character `.`.

This string would match with the `g` from `https://www.google.com`. However, note that the group is also followed by the quantifier `{2,6}`, telling us that the `www.` should be followed by anywhere from 2 to 6 single characters included in the `[a-z\.]` parameters.

</br>

### Bracket Expressions
</br>

</br>

### Greedy and Lazy Match
</br>

</br>

## Author
</br>

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
