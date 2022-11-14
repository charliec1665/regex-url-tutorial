# URL Regex Tutorial

This is a tutorial explaining how to read or write regex (or a regular expression).

## <u>Summary</u>
</br>

A regular expression, or regex, is a written search pattern. It is typically used to search for or validate certain strings or patterns of text. Regular expressions are useful because they provide flexible pattern matching while also being able to include search criteria. Regex can also be used in almost any programming language!

In this walkthrough, we will be talking about a regular expression written to match a URL string. 
Like so - `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`
            https:// ?=one or zero 

We will go through each component included in the expression, explaining what it does and the role it plays within the expression. If you need information on a particular component, use the table of contents below to skip ahead.

</br>

## <u>Table of Contents</u>
</br>

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## <u>Regex Components</u>
</br>

Regular expressions can match text patterns using both "literal" characters and "meta" characters. 

A literal character is used to match a character pattern literally, such as the lowercase letter "a".

A meta character is used to define the search criteria and text manipulations.

</br>

### <u>Anchors</u>
</br>

Anchors are a regex component that does not match a character, but instead asserts something about the searched for string or the matching process. Anchors specify a current position in the string.

Take this string of regex from our URL match for example, `/^(https?:\/\/)`. The carat `^` in the second position of the string denotes that there is a placement requirement. Here it is specifying that the pattern of characters being matched by `(https?:\/\/)`, must be at the start of the string.

Think of a typical URL, the string begins with something like: `https://`.

</br>

### <u>Quantifiers</u>
</br>

Quantifiers are what they sound like, specifying the quantity of the characters or group of characters being matched. This requirement can be very exact, like searching for exactly 3 lowercase letter 'a's (like so, `a{3}`). It can also cover a broader range of characters, like searching for zero or more lowercase letter 'a's (like so, `a*`).

In our regular expression example, this string - `([\da-z\.-]+)`, uses the quantifier `+` to denote that we are searching for one or more characters matching the `[\da-z\.-]` paramater (which we'll explain later in bracket expressions).

This piece of the regex string is essentially looking for any digit, lowercase letter, period, or dash. As in the letter string, `google` from the URL `https://www.google.com/`.

</br>

### <u>Character Classes</u>
</br>

</br>

### <u>Bracket Expressions</u>
</br>

</br>

### <u>Greedy and Lazy Match</u>
</br>

</br>

## <u>Author</u>
</br>

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
