# 🐍 Python Method Overriding

A beginner-friendly Python lesson covering **Method Overriding**, an important concept in Object-Oriented Programming and inheritance.

Method overriding allows a **child class to provide its own implementation** of a method that already exists in the parent class.

---

## 📌 Topic Covered

* Method Overriding
* Parent and Child Classes
* Inheritance
* Same Method Name with Different Behavior
* Runtime Method Selection

---

# 1. What is Method Overriding?

Method overriding happens when a child class defines a method with the **same name** as a method in its parent class.

Example:

```python
class Animal:
    def speak(self):
        print("Animal makes a sound")


class Dog(Animal):
    def speak(self):
        print("Dog barks")


animal = Animal()
dog = Dog()

animal.speak()
dog.speak()
```

---

## 🧠 What Happens Here?

The `Animal` class has a `speak()` method:

```python
class Animal:
    def speak(self):
        print("Animal makes a sound")
```

The `Dog` class inherits from `Animal`:

```python
class Dog(Animal):
```

But `Dog` defines its **own version** of `speak()`:

```python
def speak(self):
    print("Dog barks")
```

This is called **method overriding**.

---

## 🔄 What Does Python Do?

When we create an `Animal` object:

```python
animal = Animal()
animal.speak()
```

Python uses the `speak()` method from `Animal`.

Output:

```text
Animal makes a sound
```

When we create a `Dog` object:

```python
dog = Dog()
dog.speak()
```

Python finds the `speak()` method inside `Dog` and uses that instead of the inherited version.

Output:

```text
Dog barks
```

---

## 📊 Method Overriding Flow

```text
Animal
  │
  └── speak()
       │
       ▼
   "Animal makes a sound"

       ↓ inheritance

Dog
  │
  └── speak()
       │
       ▼
   "Dog barks"
```

The child class replaces the behavior of the inherited method.

---

## 🔑 Important Point

The method name stays the same:

```python
speak()
```

But the behavior changes depending on the object calling it.

```python
animal.speak()
# Animal makes a sound

dog.speak()
# Dog barks
```

This is one of the foundations of **polymorphism** in Python.

---

## 🆚 Inheritance vs Overriding

### Inheritance

The child class gets functionality from the parent.

```python
class Dog(Animal):
```

### Method Overriding

The child class changes the implementation of an inherited method.

```python
class Dog(Animal):
    def speak(self):
        print("Dog barks")
```

---

## 🎯 Learning Outcomes

After completing this lesson, you should understand:

* What method overriding means.
* How a child class overrides a parent method.
* Why the same method can behave differently for different objects.
* How Python chooses which method to execute.
* How method overriding relates to polymorphism.

---



## 👨‍💻 Author

**Yash**

⭐ If you found this lesson useful, consider giving the repository a star.
