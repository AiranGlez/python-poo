# 📌 Python OOP

> **Project description:** Learn and practice Python object oriented programming.

---

## 🗂️ Index

1. [Description](#description)
2. [Installation](#installation)
3. [Content](#content)
4. [License](#license)

---

## 📝 Description

- Classes and objects.
- Decorators
- Iterators
- Inheritance
- Polymorphism

---

## ⚙️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AiranGlez/python-oop
   cd app_name
2. Execute python main file:
   ```bash
   python src/main.py
---

## 🚀 Content

Summary of basic fundamental concepts:

1. **Classes and objects**

2. **Decorators**

   - Decorators allows to modify the behavior of a function/class. Decorators can encapsulate a function to extend its functionality without modifying it permanently.

      ```python
      def make_pretty(func):
         # define the inner function
         def inner():
            # add some additional behavior to decorated function
            print("Now I got decorated")
            # call the original function
            func()
            return inner
      
      def ordinary():
         print("Hi, I'm ordinary")
      
      # decorate the ordinary function
      decorated_func = make_pretty(ordinary)

      decorated_func()

   - Instead of assigning the function call to a variable, Python provides a much more elegant way to achieve this functionality using the '@' symbol: 

      ```python
      def make_pretty(func):
         def inner():
            print("I got decorated")
            func()
            return inner
      
      @make_pretty
      def ordinary():
         print("I am ordinary")

      ordinary()
   - Decorating functions with parameters:

      ```python
      def smart_divide(func):
         def inner(a, b):
            print(f"I am going to divide {a} and {b}")
            if b == 0:
               print("Wrong value, cannot divide by 0")
               return
            return func(a,b)
         return inner

      @smart_divide
      def divide(a, b):
         print(a/b)

      divide(2, 5) # --> I am going to divide 2 and 5 0.4
      divide(2, 0) # --> Wrong value, cannot divide by 0
---

## 📄 License

This project is under the MIT License. This means you are free to use, modify, and distribute the code, as long as you include a copy of the license in any distribution or modification of the code.

### Terms:

Permission is granted to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software.
The code is provided "as is," without any warranty of any kind, express or implied, including but not limited to warranties of merchantability or fitness for a particular purpose.

### Purpose:

This code is provided for educational and training purposes. You may use it to learn, modify, and share it, but it should not be used for commercial purposes without additional authorization.

For more information, refer to the LICENSE file for the full details of the MIT License.