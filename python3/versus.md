# This vs. That in Python 3
Python 3 comparisons in concepts.


## wb, rb vs. w, r
In file operations such as `open(file_name, mode)`, a mode can be specified.  

What is the difference between `w` and `wb`?

The `b` added on means 'binary'.  Reading and Writing to the file with a binary
option will read newline characters or `\n` to a literal.  By default, data is
read as text where the newline character will be encoded as a newline depending
on the platform line endings.

Binary mode should be used when the data is not text as to not encode
characters.

[docs.python.org](https://docs.python.org/3/tutorial/inputoutput.html#reading-and-writing-files)


## JSON dumps vs. loads
`dump` object to string.

`load` string to object.

`dumps` returns a string from an object.

`loads` returns an object from a string. Object is iterable like a Dictionary.


(https://stackoverflow.com/questions/32911336/what-is-the-difference-between-json-dumps-and-json-load)
