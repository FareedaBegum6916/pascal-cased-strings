# pascal-cased-strings
# 🐍 Pascal/Camel Case to Snake Case Converter

This Python project is a simple yet powerful utility that converts **PascalCase** or **camelCase** strings into **snake_case** format — the standard naming convention in Python programming.

> 🏫 *This mini-project is part of my learning journey through the [Scientific Computing with Python](https://www.freecodecamp.org/learn/scientific-computing-with-python/) certification course by freeCodeCamp.*

---

## 📌 Project Overview

Different programming languages follow different naming conventions. While JavaScript or Java may use camelCase or PascalCase, Python emphasizes snake_case for readability and consistency. This converter script was built to bridge that gap and transform any mixed-case string into snake_case.

---

## 🛠️ Process

Building this project from scratch involved the following steps:

1. **Understanding the Problem**  
   I analyzed what differentiates camelCase and PascalCase from snake_case. The key insight was the presence of uppercase letters signaling word boundaries.

2. **Planning the Solution**  
   I broke the task down into small steps:
   - Iterate through each character in the string.
   - Detect uppercase letters and prepend them with an underscore.
   - Convert all letters to lowercase.
   - Join the characters and remove any leading underscore.

3. **Implementing the Logic**  
   I used a list comprehension to create a clean and Pythonic one-liner inside a function, followed by a `.strip('_')` to handle edge cases.

4. **Testing with Examples**  
   I used various test cases like `"IAmAPascalCasedString"` and `"camelCaseExample"` to ensure the function handled both naming styles properly.

---

## 📚 Lessons Learned

✅ Learned how to manipulate strings effectively in Python  
✅ Gained experience using **list comprehensions** for clean and efficient code  
✅ Understood the importance of edge case handling (like removing the initial underscore)  
✅ Improved my debugging and testing skills through manual test inputs  
✅ Appreciated the value of consistent naming conventions across codebases

---

## 👨‍💻 Code Example

```python
def convert_to_snake_case(pascal_or_camel_cased_string):
    snake_cased_char_list = [
        '_' + char.lower() if char.isupper()
        else char
        for char in pascal_or_camel_cased_string
    ]
    return ''.join(snake_cased_char_list).strip('_')

def main():
    print(convert_to_snake_case('IAmAPascalCasedString'))

main()
