# Python Fundamentals

## Variables (Storage Containers)
- We use variables to store information or data.
- We declare a variable in Python: `x = "4"` — this means `x` is a variable and `x` holds the value `"4"`.
- Python reads code from left to right, and executes code from top to bottom.

```python
name = "William"   # variable = value
print(name)        # William
print(x)           # 4
```

### Rules for Naming Variables
1. Variables must start with a letter or an underscore character (`_`).
2. Variables must be explainable/descriptive (e.g. `name = "Moscow"`, `surname = "William"`).
3. No spaces between words in a variable name — separate using an underscore (e.g. `name_surname = "Moscow William"`).
4. A variable name cannot be a Python keyword or built-in function (e.g. `def`, `import`).
5. A variable name should be defined based on the kind of data it holds.
6. No separating a variable name with a dash — only use an underscore.

### Variable Naming Conventions
1. **Camel Case** — each word, except the first letter, starts with a capital letter.
   `myFirstName = "Suzuki"`
2. **Pascal Case** — each word starts with a capital letter.
   `MyNameSurname = "Moscow William"`
3. **Snake Case** — separates each word with an underscore.
   `my_name_surname = "Moscow William"`

## Print & Type Functions
- `print()` — allows you to display results.
- `type()` — used to check the data type of a variable, e.g. `print(type(name))` → `str`.

## Data Types

- **Text Type:** `str`
- **Numeric Types:** `int`, `float`, `complex` (imaginary number)
- **Sequence Types:** `list`, `tuple`, `range`
- **Mapping Type:** `dict` (dictionary)
- **Boolean Type:** `bool`

| Type | Example |
|---|---|
| Text (str) | `name = "Moscow"` |
| Integer (int) | `age = 26` |
| Float (decimal) | `price = 19.20` |
| Complex | imaginary number |
| Boolean | `True` / `False` |
| Datetime | any date, `"YYYY-MM-DD"` |
| List | `["Toyota", "BMW", "Haval"]` |
| Tuple | `("Moscow", "John")` |
| Range | `range(0, 10)` — e.g. coordinates |
| Dictionary | `{"name": "Doe", "age": 26}` — key : value |

- A string is a combination of characters, and we use single or double quotes when we have a string.
- Other words: **float** = decimal; **boolean** = True or False.

### Functions Applied to Strings
- `len()` — counts the number of words/characters in a string.
- `.upper()` — changes words in a string to be upper case.
- `.lower()` — changes words in a string to be lower case.
- `.strip()` — removes unnecessary/empty spaces in a string.
- `.split()` — separates words by a comma (or given delimiter).

```python
name_surname = "Moscow William"
len(name_surname)                    # counts the letters/characters
print(name_surname.upper())          # changes the words to upper case
```

### f-strings
```python
name = "Moscow"
message = f"Hello {name}, how are you?"
print(message)
```

## Lists
- Used to store multiple values in a single variable.
- The first index value is `0`.
- Ordered, changeable (mutable), indexed, and allow duplicates.

```python
list_names = ["John", "Lisa", "Moscow"]
list_ages = [26, 35, 40]
```

### Common List Functions
- `.append()` — `list_names.append("Sally")`
- `.count()` — `list_names.count()`
- `.extend()` — `list_names.extend(list_names_2)`
- `.remove()` — `list_names.remove("Rofhiwa")`
- `.reverse()` — `list_names.reverse()`
- `.sort()` — sorts the elements of a list in ascending order.
  ```python
  price = [50, 20, 80, 10, 40]
  price.sort()
  print(price)             # ascending order
  price.sort(reverse=True)
  print(price)             # descending order
  ```
- Sorting strings works the same way:
  ```python
  fruits = ["Banana", "Apple", "Orange"]
  fruits.sort()
  print(fruits)
  ```

## Tuples
- Used to store multiple items in a single variable.
- **Not** changeable (immutable), ordered, written with round brackets `()`, allows duplicates.

```python
tuple1 = ("Jane", "John")
tuple1[1]                 # access by index
tuple1.index("John")      # find index of an item
```

## Dictionaries
- Used to store **key : value** pairs.
- Changeable, ordered, and does **not** allow duplicate keys.

```python
my_profile = {
    "name": "William",
    "surname": "Mathabuana",
    "age": 28,
    "location": "SA"
}
print(my_profile)
```

### Accessing Values
```python
my_car = {
    "name": "Suzuki",
    "model": "Baleno",
    "year": 2023,
    "dealership": "SoWeTo"
}
print(my_car["name"])          # Suzuki
print(my_car.get("name"))      # Suzuki
```

### Dictionary Functions
- `.keys()` — gives all key values in a dictionary.
- `.values()` — gives all the values in a dictionary.
- `.items()` — puts your key:value pairs into a list.
- `.get()` — extract a value by specifying the key.
- `.pop("key")` — removes the specified key:value pair.
- `.popitem()` — deletes the last key:value pair.
- `.clear()` — empties the dictionary.

### Changing a Value in a Dictionary
```python
my_car = {
    "name": "Suzuki",
    "model": "Baleno",
    "year": 2023,
    "dealership": "SoWeTo"
}
my_car["name"] = "BMW"
print(my_car)
```

## Booleans
- `bool` → `True` or `False`.

## Conditional Statements

- Used to execute a certain block of code based on a specific condition.
- Leave a space between the condition and the code, and comment code with `#`.

```python
if condition:
    # code

age = 10
if age >= 18:
    print("Eligible to vote")
    print("You're an adult")
```

### if / elif / else
```python
if age > 18:
    print("You can vote!")
elif age > 16:
    print("Youth")
else:
    print("Child")
```

### More Examples
```python
marks = 45
if marks >= 50:
    print("Pass")
else:
    print("Fail")

score = 75
if score >= 80:        # range 80 -> 100
    print("Distinction")
elif score >= 60:      # range 60 -> 80
    print("Merit")
elif score >= 50:      # range 50 -> 60
    print("Pass")
else:
    print("Fail")

age = 25
salary = 10000
if age > 18 and salary > 5000:
    print("Loan approved at capitec")
```

### Comparison Operators
- `==` equal, `!=` not equal, `<` less than, `<=` less than or equal to.
- `=` assigns a value to a variable, `==` compares two things.

### OR Truth Table

| Condition 1 | Condition 2 | Result |
|---|---|---|
| True | True | True |
| True | False | True |
| False | True | True |
| False | False | False |

## Loops

Loops allow a program to repeat a block of code multiple times.

- **For loop** — use when the number of repetitions is known.
- **While loop** — use when repetitions depend on a condition.
- **Infinite loop** — a loop with no terminating condition.
- **Break statement** — used to stop a loop early.
- **Continue statement** — used to skip unwanted iterations.
- **Zip()** — used to work with multiple lists simultaneously (combines items from multiple sequences into pairs).
- **Enumerate()** — used to access both indexes and values together.

| Concept | Purpose |
|---|---|
| For loop | Repeat a known number of times |
| While loop | Repeat while a condition is true |
| enumerate() | Get index and value together |
| zip() | Combines multiple sequences |
| break | Stops the loop completely |
| continue | Skips the current iteration |

### For Loop Structure
```python
for variable in collection:
    # code
```

```python
products = ["Bread", "Milk", "Egg"]
for item in products:
    print(item)

numbers = [10, 20, 30]
for x in numbers:
    print(x)

prices = [100, 200, 300, 250]
for price in prices:
    vat = price + 0.15
    print(vat)
```

### Loop with if Statement
```python
balances = [10, 2, 30, 1]
for balance in balances:
    if balance < 5:
        print(balance)
```

### Loop with Counter/Range
```python
balances = [10, 2, 30, 1]
counter = 0
for balance in range(len(balances)):
    if balances[balance] < 5:
        print(balances[balance], counter)
    counter = counter + 1
```

### Loop Through a Dictionary
```python
customers = {
    "Alice": 10,
    "Bob": 20,
    "David": 20
}

for customer in customers:
    print(customer)

# Loop through values
for quantity in customers.values():
    print(quantity)
```

### Enumerate
```python
customers = ["Amanda", "Sean", "James"]
for index, customer in enumerate(customers, start=1):
    print(index, customer)
```

### Zip (pair items)
Combines items from multiple sequences into pairs.

```python
stores = ["Hell's Kitchen", "Astoria", "Lower Manhattan"]
revenues = [45000, 20000, 54000]

for store, rev in zip(stores, revenues):
    print(store, rev)
```

```python
import pandas as pd
list_stores = ["Hell's Kitchen", "Astoria", "..."]
list_revenues = [45000, 20000, "..."]
list_products = ["Coffee", "Tea", "Mocha"]
df = pd.DataFrame({
    "Stores": list_stores,
    "Revenue": list_revenues,
    "Product": list_products
})
```
