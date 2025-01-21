# Regular Expressions

In the following, you will parse information from text-based files with the command line and Unix tools and Python in the next step. Please note that even though the files are provided as structured csv files you are not supposed to simply read out the columns, but you should use regular expressions instead.

## Parsing contact information from the command line

In this directory, you will find a txt-file called `csv/contacts.csv`. Use regular expressions to extract the following information from it.

Remember that you can use different tools like `grep`, `awk`, or `sed` to use regular expressions from the command line. Pipes might also be helpful. 

You can add your command line in- and outputs directly to this README file. Alternatively, you can write a bash script with all commands and commit it to this directory.

1. Extract all email addresses from the text.
``` 
grep -oP '\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Za-z]{2,}\b' "C:\Users\user\Desktop\TH KÖLN\Semester 5\Daten Modellierung\contacts.csv"

Comment:
grep: Searches for patterns in text.
-o: Prints only the matching part of each line.
-P: Enables Perl-compatible regular expressions (needed for \b and other advanced regex features).
``` 
2. Extract all phone numbers from the text.
``` 
grep -oP '\(?\d{3}\)?[-.\s]?\d{3}[-.\s]?\d{4}' "C:\Users\user\Desktop\TH KÖLN\Semester 5\Daten Modellierung\contacts.csv"

Comment:
\(?: Matches an optional opening parenthesis (.
\d{3}: Matches exactly three digits.
[-.\s]?: Matches an optional separator (dash, dot, or space).
\d{4}: Matches exactly four digits.
``` 
3. Extract all names that start with the letter ‘J’.
``` 
grep -oP '\bJ[A-Za-z]+\b' "C:\Users\user\Desktop\TH KÖLN\Semester 5\Daten Modellierung\contacts.csv"

Comment:
\bJ: Matches a word boundary followed by J.
[A-Za-z]+: Matches one or more alphabetical characters.
``` 
4. Extract all street names that contain the word 'St'.
``` 
grep -oP '\b[A-Za-z\s]*St[A-Za-z\s]*\b' "C:\Users\user\Desktop\TH KÖLN\Semester 5\Daten Modellierung\contacts.csv"

Comment:
\b: Ensures we match full words.
[A-Za-z\s]*: Matches a sequence of letters and spaces around "St".

``` 
5. Extract all addresses in ‘USA’.
``` 
grep 'USA' "C:\Users\user\Desktop\TH KÖLN\Semester 5\Daten Modellierung\contacts.csv"

Comment:
This simple pattern searches for any line containing "USA".
``` 
6. Extract the last names of all people.
``` 
grep -oP '\b[A-Za-z]+\s\K[A-Za-z]+' contacts.csv

Comment:
Assuming the last names appear after the first name and are separated by a space: Regex: \b[A-Za-z]+\s([A-Za-z]+)\b
``` 
7. Extract all email domains (part after the @ sign).
``` 
grep -oP '@[A-Za-z0-9.-]+\.[A-Za-z]{2,}' contacts.csv | sed 's/@//'

Comment:
@: Matches the literal '@' symbol.
[A-Za-z0-9.-]+: Matches one or more characters that can be letters (uppercase or lowercase), digits, dots, or hyphens (valid domain characters).
\.: Matches the literal dot (.) symbol.
[A-Za-z]{2,}: Matches two or more alphabetic characters (to match domain extensions like .com, .org, etc.).
``` 
8.	Extract all instances of the first name ‘David’ along with their full address (street and city).
``` 
grep -oP 'David\s[A-Za-z\s]+,[A-Za-z\s]+' contacts.csv

Comment:
\s: Matches a single whitespace character (space between name and address).
[A-Za-z\s]+: Matches one or more letters (first part of the address, including spaces).
,: Matches the literal comma separating name and address.
[A-Za-z\s]+: Matches one or more letters (second part of the address, including spaces).
``` 
9.	Find all entries where the phone number ends with ‘7’.
``` 
grep -oP '\d{3}[-.\s]?\d{3}[-.\s]?\d{3}7\b' contacts.csv

Comment:
\d{3}: Matches exactly three digits (for the area code or first part of the phone number).
[-.\s]?: Matches an optional separator (dash, dot, or space).
\d{3}: Matches exactly three digits (for the second part of the phone number).
[-.\s]?: Matches another optional separator.
\d{3}: Matches exactly three digits (for the third part of the phone number).
7: Matches the literal '7' at the end of the phone number.
\b: Asserts a word boundary (ensures that '7' is the last character in the phone number).
``` 
10.	Extract all instances of first names that end with the letter 'e'.
``` 
grep -oP '\b[A-Za-z]*e\b' contacts.csv

Comment:
\b: Asserts a word boundary (ensures that we're matching full words).
[A-Za-z]*: Matches zero or more alphabetic characters (letters, both uppercase and lowercase).
e: Matches the letter 'e' (the last character of the first name).
\b: Asserts another word boundary (ensures that 'e' is the final character in the word).
``` 

## Parsing product orders with Python

In this directory, you will find another file called `csv/orders.csv` and also a short Python script that reads the file and parses all numbers with a regular expression. Please extend the script such that it also print the following extracted text pieces.

1.	Extract all order numbers from the text. 
2.	Extract all product names.
3.	Extract all prices.
4.	Extract all order dates.
5.	Find all orders for products priced over $500. (You are allowed to use Python to filter the list.)
6.	Change the date format to DD/MM/YYYY. (Note the re.sub() method)
7.	Extract product names that have more than 6 characters.
8.	Count the occurrence of each product in the text. (You may want to use the Counter class from the collections package.)
9.	Extract the orders with prices ending in .99.
10.	Find the cheapest product. (You may want to use Python's min() method.)
