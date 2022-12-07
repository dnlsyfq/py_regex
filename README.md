* Read Txt
```
file = open('names.txt',encoding='utf-8') // create pointer
data = file.read()
file.close()
print(data)
```

* Regex
```
import re

re.match(r'str',data) // beginning of text
re.search(r'str',data) // search somewhere

```

* Match char
```
\w   # any unicode
\W   # any non unicode
\s   # any whitespace
\S   # any non whitespace
\d   # any number
\D   # any non number
\b   # any word boundaries / edges of word
\B   # any non word boundaries / edges of word
\    # escape char
```

```
(555) 555-5555

re.search(r'\(\d\d\d\) \d\d\d-\d\d\d\d',data) // return first row
re.search(r'\(\d{3}\) \d{3}-\d{4}',data)
re.findall(r'\(?\d{3}\)? -?\s \d{3}-\d{4}',data)


def numbers(count, user_string):
  return re.search(r'\d' * count, user_string)

```

* count
```
{3,}  // occur 3 or more
{3,5} // occure 3 - 5 times
? // 0 or 1 or more times
* // 0 or infinite times
+ // at least 1

re.search(r'\w+, \w+',data)

def find_words(count, string):
  re_string = re.findall(r'\w+' * count, string)
  return re_string
```

