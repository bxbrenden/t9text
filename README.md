# t9text
A Python package for working with T9 text messaging.

## Description
`t9text` is meant for two main purposes:
- Given a string of alphabetic text (plus `-`, `*`, `#`), `t9text` can tell a user which numeric touchtone phone buttons correspond to it, e.g.:
```python
from t9text import t9
daily_show = '1-210-WH-CRIME'  # The Daily Show's phone number for Trump to confess his crimes to :-)

buttons = t9.get_touchtone(daily_show)
print(buttons)  # prints "1-210-94-27463"
```

- Given a string of 10 or fewer digits, display all possible T9 "words", e.g.:
```python
from t9text import t9
digits = "2332" #can also be `int` such as 2332

words = t9.get_words(digits)
for word in words:
    print(word)  # ["adda", addb", "addc", "aeda" ...]
```