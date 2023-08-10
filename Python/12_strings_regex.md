# Regular Expressions

In Python, regular expressions are a powerful tool for working with text data. A regular expression is a sequence of characters that defines a search pattern, which can be used to match or manipulate text strings.

Regular expressions are supported in Python through the built-in re module. This module provides a set of functions and methods that allow you to search, match, and manipulate text data using regular expressions.

Some of the most commonly used functions and methods in the re module include:

* search(): Searches for a pattern in a string and returns the first occurrence.
* match(): Searches for a pattern at the beginning of a string and returns the match if found.
* findall(): Finds all occurrences of a pattern in a string and returns them as a list.
* sub(): Replaces all occurrences of a pattern in a string with a replacement string.

Regular expressions use special characters and syntax to define search patterns. For example, the . character matches any single character, the * character matches zero or more occurrences of the previous character or group, and the [] characters define a set of characters to match.

```python
>>> import re
```

Extracts the first two words of the text

```python
>>> re.match(r"(\w+) (\w+)", "Isaac Newton Physicist").groups()
('Isaac', 'Newton')
```

Extracts the starting number as long as it has 10 digits

```python
>>> re.match(r"([0-9]{10})", "0123456780 Supplier 123 X 1234567890").groups()
('0123456780',)
```

Separates the number into units and decimals

```python
>>> re.match(r"(\d+)\.(\d+)", "24.1632").groups()
('24', '1632')
```

Separates text into words using space character as a reference

```python
>>> re.split(pattern="\s", string="Isaac Newton Physicist", maxsplit=0)
['Isaac', 'Newton', 'Physicist']
```

Strip equivalent

```python
>>> w = "hello world"
>>> re.search(pattern="^[world]*(.*?)[world]*$", string=w).group(1)
'hello '
```

Removes symbols from the file name except for the dot

```python
>>> w = r"016_test,file-peter_.name_123//111\\99.pdf"
>>> re.sub(pattern=r"[^0-9a-zA-Z:.-:]+", repl="_", string=w)
'016_test_file_peter_.name_123//111_99.pdf'
```

```python
>>> w = r"016_test,file:-peter_.name_123//111\\99.pdf"
>>> re.sub(pattern=r"[^a-zA-Z0-9.]+", repl="_", string=w)
'016_test_file_peter_.name_123_111_99.pdf'
```

## Isaac Newton

```python
text = """Isaac Newton was an English physicist, mathematician, and astronomer who lived from 1643 to 1727. He is considered one of the most important figures in the history of science, and his contributions to the fields of physics and mathematics have had a profound impact on the modern world.

Newton is perhaps best known for his work on the laws of motion and universal gravitation. In 1687, he published his seminal work, "Mathematical Principles of Natural Philosophy," which laid out his three laws of motion and his law of universal gravitation. These laws formed the basis of classical mechanics, and they allowed scientists to understand the behavior of objects in motion and the force that governs the movements of the planets and other celestial bodies.

In addition to his work in physics, Newton also made significant contributions to the field of mathematics. He is credited with developing calculus, a branch of mathematics that deals with rates of change and slopes of curves. Newton's work in calculus was instrumental in the development of modern mathematics, and it has had important applications in fields such as engineering, economics, and physics.

Newton was also an accomplished astronomer, and he made several important discoveries in this field as well. He built the first reflecting telescope, which allowed for more accurate observations of the stars and planets. He also discovered that white light is actually made up of a spectrum of colors, a phenomenon now known as Newton's law of color.

Newton's work had a profound impact on the scientific community of his time, and it continues to influence scientific research and discovery today. He was widely recognized as one of the greatest minds in history, and his legacy has had a lasting impact on the fields of physics, mathematics, and astronomy."""
```

Use regex to split the text into words.

```python
>>> words = re.findall(pattern=r"\b\w+\b", string=text)
>>> words[0:7]  # first 7 words
['Isaac', 'Newton', 'was', 'an', 'English', 'physicist', 'mathematician']
```

```python
>>> len(words)
299
```

Frequency of each word.

```python
>>> freq_dict = {}
>>> for word in words:
    if word in freq_dict:
        freq_dict[word] += 1
    else:
        freq_dict[word] = 1

>>>> for word, freq in freq_dict.items():
    print(f"'{word}': {freq}")

'Isaac': 1
'Newton': 7
'was': 4
'an': 2
'English': 1
'physicist': 1
'mathematician': 1
'and': 17
'astronomer': 2
'who': 1
'lived': 1
'from': 1
'1643': 1
'to': 6
'1727': 1
'He': 5
'is': 4
'considered': 1
'one': 2
'of': 22
'the': 17
'most': 1
'important': 3
'figures': 1
'in': 8
'history': 2
'science': 1
'his': 8
'contributions': 2
'fields': 3
'physics': 4
'mathematics': 5
'have': 1
'had': 4
'a': 6
'profound': 2
'impact': 3
'on': 4
'modern': 2
'world': 1
'perhaps': 1
'best': 1
'known': 2
'for': 2
'work': 5
'laws': 3
'motion': 3
'universal': 2
'gravitation': 2
'In': 2
'1687': 1
'he': 2
'published': 1
'seminal': 1
'Mathematical': 1
'Principles': 1
'Natural': 1
'Philosophy': 1
'which': 2
'laid': 1
'out': 1
'three': 1
'law': 2
'These': 1
'formed': 1
'basis': 1
'classical': 1
'mechanics': 1
'they': 1
'allowed': 2
'scientists': 1
'understand': 1
'behavior': 1
'objects': 1
'force': 1
'that': 3
'governs': 1
'movements': 1
'planets': 2
'other': 1
'celestial': 1
'bodies': 1
'addition': 1
'also': 3
'made': 3
'significant': 1
'field': 2
'credited': 1
'with': 2
'developing': 1
'calculus': 2
'branch': 1
'deals': 1
'rates': 1
'change': 1
'slopes': 1
'curves': 1
's': 3
'instrumental': 1
'development': 1
'it': 2
'has': 2
'applications': 1
'such': 1
'as': 4
'engineering': 1
'economics': 1
'accomplished': 1
'several': 1
'discoveries': 1
'this': 1
'well': 1
'built': 1
'first': 1
'reflecting': 1
'telescope': 1
'more': 1
'accurate': 1
'observations': 1
'stars': 1
'discovered': 1
'white': 1
'light': 1
'actually': 1
'up': 1
'spectrum': 1
'colors': 1
'phenomenon': 1
'now': 1
'color': 1
'scientific': 2
'community': 1
'time': 1
'continues': 1
'influence': 1
'research': 1
'discovery': 1
'today': 1
'widely': 1
'recognized': 1
'greatest': 1
'minds': 1
'legacy': 1
'lasting': 1
'astronomy': 1
```

Use regex to split the text into sentences.

```python
>>> sentences = re.split(pattern=r"[.!?]", string=text)
>>> sentences
['Isaac Newton was an English physicist, mathematician, and astronomer who lived from 1643 to 1727',
 ' He is considered one of the most important figures in the history of science, and his contributions to the fields of physics and mathematics have had a profound impact on the modern world',
 '\n\nNewton is perhaps best known for his work on the laws of motion and universal gravitation',
 ' In 1687, he published his seminal work, "Mathematical Principles of Natural Philosophy," which laid out his three laws of motion and his law of universal gravitation',
 ' These laws formed the basis of classical mechanics, and they allowed scientists to understand the behavior of objects in motion and the force that governs the movements of the planets and other celestial bodies',
 '\n\nIn addition to his work in physics, Newton also made significant contributions to the field of mathematics',
 ' He is credited with developing calculus, a branch of mathematics that deals with rates of change and slopes of curves',
 " Newton's work in calculus was instrumental in the development of modern mathematics, and it has had important applications in fields such as engineering, economics, and physics",
 '\n\nNewton was also an accomplished astronomer, and he made several important discoveries in this field as well',
 ' He built the first reflecting telescope, which allowed for more accurate observations of the stars and planets',
 " He also discovered that white light is actually made up of a spectrum of colors, a phenomenon now known as Newton's law of color",
 "\n\nNewton's work had a profound impact on the scientific community of his time, and it continues to influence scientific research and discovery today",
 ' He was widely recognized as one of the greatest minds in history, and his legacy has had a lasting impact on the fields of physics, mathematics, and astronomy',
 '']
```

```python
>>> len(sentences)
14
```

Frequency of each phrase.

```python
>>> freq_dict = {}
>>> for phrase in sentences:
    if phrase in freq_dict:
        freq_dict[phrase] += 1
    else:
        freq_dict[phrase] = 1

>>> for phrase, freq in freq_dict.items():
    print(f"'{phrase.strip()}': {freq}"

'Isaac Newton was an English physicist, mathematician, and astronomer who lived from 1643 to 1727': 1
'He is considered one of the most important figures in the history of science, and his contributions to the fields of physics and mathematics have had a profound impact on the modern world': 1
'Newton is perhaps best known for his work on the laws of motion and universal gravitation': 1
'In 1687, he published his seminal work, "Mathematical Principles of Natural Philosophy," which laid out his three laws of motion and his law of universal gravitation': 1
'These laws formed the basis of classical mechanics, and they allowed scientists to understand the behavior of objects in motion and the force that governs the movements of the planets and other celestial bodies': 1
'In addition to his work in physics, Newton also made significant contributions to the field of mathematics': 1
'He is credited with developing calculus, a branch of mathematics that deals with rates of change and slopes of curves': 1
'Newton's work in calculus was instrumental in the development of modern mathematics, and it has had important applications in fields such as engineering, economics, and physics': 1
'Newton was also an accomplished astronomer, and he made several important discoveries in this field as well': 1
'He built the first reflecting telescope, which allowed for more accurate observations of the stars and planets': 1
'He also discovered that white light is actually made up of a spectrum of colors, a phenomenon now known as Newton's law of color': 1
'Newton's work had a profound impact on the scientific community of his time, and it continues to influence scientific research and discovery today': 1
'He was widely recognized as one of the greatest minds in history, and his legacy has had a lasting impact on the fields of physics, mathematics, and astronomy': 1
'': 1
```

Frequency of words that have the previous word the word "is" and it finishes with the letters "ed".

```python
>>> freq_dict = {}
>>> for i in range(1, len(words)):
    if words[i].endswith("ed") and words[i-1] == "is":
        word = words[i].lower()
        if word in freq_dict:
            freq_dict[word] += 1
        else:
            freq_dict[word] = 1

>>> for word, freq in freq_dict.items():
    print(f"'{word}': {freq}")
'considered': 1
'credited': 1
```
