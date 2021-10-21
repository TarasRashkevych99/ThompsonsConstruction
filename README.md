# Simple Regex Parser

The purpose of this project is to provide a basic implementation of a regex parser that is able to determine whether a word matches a particular regular expression.

## Supported regex operators

The following are the operators that are recognized by the parser :

| Symbol |               Formal Name                | Example |        Description         |
| :----: | :--------------------------------------: | :-----: | :------------------------: |
|   \*   |     Kleene Operator(or Kleene Star)      |   a\*   | 0 or more occurrences of a |
|   \|   | Alternation Operator(or Union Operator)  |  a\|b   |           a or b           |
|   .    | Concatenation Operator(Normally Omitted) |   ab    |      a followed by b       |
|   ()   |           Parenthesis Operator           |   (a)   | a with operator precedence |

## Supported characters

The parser **_should_** allow all possible characters, except for the characters that specify the operators described above in the table. Moreover, the `ε` character(formally an empty string)
and the `" "` character(useful for typing but useless for processing) are stripped out from the
input word.

## How to run the parser on your machine

Make shure that you have installed the [Python](https://www.python.org/downloads/) 3.7 interpreter or
a higher version of it.<br>
This project has been developed with the Python 3.7.10 interpreter and tested on macOS Big Sur.<br><br>

Clone the repository on your machine :

```
git clone https://github.com/TarasRashkevych99/simple-regex-parser.git
```

Move to the `simple-regex-parser/src` folder by executing the following command :

```
cd simple-regex-parser/src
```

Run inside the `src` folder one the the following command :

```
python run_regex_parser.py regex [-w|--word input_word] [-v|--verbose] [-h|--help]
```

The arguments have the following meaning:

- `regex` : positional argument that specifies the regex(i.d. the pattern to match against).
- `[-w|--word input_word]` : optional argument where `input_word` specifies the word to be tested
  against the regex.
- `[-v|--verbose]` : optional argument that specifies how detailed the output will be.
- `[-h|--help]` : optional argument that describes the purpose of the program and of each and every
  argument passed to it.

In the case of the `regex` argument, the actual regex can be written by simply escaping the
operators with the `\` character, but it is highly recommended to use double or single quotes
which don't require any type of escaping, like in the following example :

```
python run_regex_parser.py "(r|e|g|e|x)*" -w regex -v
```

The `[-w|--word input_word]` can also be specified by using double or single quotes.
