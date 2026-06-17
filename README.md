# My Portfolio

My name is Jude Okoduwa with student number M01113955

## Week 1
Please do make sure you install [python](https://www.python.org/downloads/) and 

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install pandas.

## Prerequesite
Make sure you have these installed before carry out reading:

```bash
pip install pandas
```

## Example 01
This code asks users for their name, interest, nationality, course and experience and then print out the corresponding user information. I learnt here how to create user inputs.,

```python
print("================================")
print("USER INFORMATION")
print("================================")
name = input("Name: ")
interest = input("Interest: ")
Nationality = input("Nationality: ")
Course = input("Course: ")
Experience = input("Experience: ")

print("Name: ", name)
print("Interest: ", interest)
print("Nationality: ", Nationality)
print("Course: ", Course)
print("Experience: ", Experience)
```

## Example 02
This code asks for a username, when its inputed, its asks for an action, either to LOGIN or LOGOUT and then it prints the date, hours, minutes and second you logged in including your username,

```python
from datetime import datetime

username = input("Enter username: ")
action = input("Enter action (LOGIN/LOGOUT): ")

timestamp = datetime.now().strftime("%Y-%m-%d %H:%M:%S")

print(f"[{timestamp}] {action} user={username}")

```





## Week 2

This week, i learnt Python's **Conditional statements (if, elif, else)**, **loops (for, while)** and basic **list** operations

## Example 01
This code is s password checker. it checks if the password inputed is weak, moderate or strong. So it asks users to input a password, if the password length is greater than or equal to 12, it displays Strong, else if the password's length is greater than or equal to 8, it displays moderate, and else it prints weak.

```python
password = input('Enter your password: ')

if len(password) >= 12:
    print('Strong')
elif len(password) >=8:
    print('Moderate')
else:
    print('Weak')
```

## Example 02
This code is used to calculate **Body mass index (BMI)** 
It prompts users to input their weight in pounds and also their height in inches, then it converts weight into metrics by multiplying by 0.45359237, also coverts heights in inches into meters by multiplying by 0.0254. The resultant weight is then didvided by the height to give the BMI and the result printed. if the bmi < 18.5, it prints overweight, else if it is <= 25, it prints normal, else it prints obese.

```python
weight_lb = input("Enter weight in pounds: ")
height_in = input("Enter height in inches: ")

# Convert to metric
weight_kg = float(weight_lb) * 0.45359237
height_m = float(height_in) * 0.0254

# BMI calculation
bmi = weight_kg / (height_m ** 2)

# Output BMI
print("\nBMI:", round(bmi, 2))

# Interpretation
if bmi < 18.5:
    print("Underweight")
elif bmi <= 25.0:
    print("Normal")
elif bmi <= 30.0:
    print("Overweight")
else:
    print("Obese")

```



## Week 3

This week, I learnt about **Slicing in lists** **Defining and using functions** **Lambda expressions for concise coding** **Working with multidimensional lists (nested lists)**

## Example 01
In this program, we are told to find the largest number, but we don't know the number of values.
so we created a function with variable-arguments length. In this code, it prompts the user to enter numbers seperated by spaces and then finds the largest number from the numbers listed.

```python

def largest_number_variable(*args):
    if not args:
        return None
    largest = args[0]
    for num in args:
        if num > largest:
            largest = num
    return largest
def main():
    print("Find the Largest Number")
    numbers = input("Enter numbers separated by spaces: ")
    num_list = [float(num) for num in numbers.split()]
    largest = largest_number_variable(*num_list)
    print(f"The largest number is: {largest}")
if __name__ == "__main__":    main()


```

## Example 02
In this code I learnt about multi-dimensional lists. The object [1, 2, 3] is not one of the main elements of list1. List1 contains only integers (1, 2, 3..) and not the list [1, 2, 3], since list2 [1, 2, 3] is not contained in list1, the result is False.

```python

def sublist(list1, list2, list3):
    return True if list2 in list1 else False

list1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
list2 = [1, 2, 3]
list3 = [4, 5, 6]

print(sublist(list1, list2, list3))



```



## Week 4

In this week 4, I learnt about **Strings and Regular Expressions** I learnt about strip(), lower(), startswith(), len(), isdigit(), split(), count(), title(), any(), in, isalpha(), all(), isupper(), islower(), ord(), chr(), find(), replace(), join(), centre().

## Example 01
In this program, we count how many times each keyword appears across all feedback, using the method lower() and count(). When the code is run, the feedback, "great" was used 3 times, "quality" was used 3 times and "delivery" 2 times.

```python

feedback = [
    "The product quality is great",
    "Fast delivery but poor quality",
    "Great product and great delivery",
    "Quality could be better"
]

keywords = ['great', 'quality', 'delivery']

# Join all feedback into one string (lowercase), then count each keyword

all_feedback = " ".join(feedback).lower()
keywords_count = {keyword: all_feedback.count(keyword) for keyword in keywords}
print(keywords_count)

**OUTPUT**

{'great': 3, 'quality': 3, 'delivery': 2} 
```

## Example 02
This program Counts how many `ERROR`, `INFO`, and `WARNING` entries there are extracts and prints the **timestamp** from each entry and returns the three counts. When the code is run, we get the output below.

```python
logs = [
    "[14:32:05] ERROR: Disk full",
    "[14:32:10] INFO: Server started",
    "[14:33:01] WARNING: High memory usage",
    "[14:33:15] INFO: Backup complete",
    "[14:34:00] ERROR: Connection refused",
    "[14:35:22] WARNING: CPU at 90%"
]



    # TODO: Loop through each log entry
    # Extract the timestamp (between the square brackets)
    # Check if the text after the timestamp starts with ERROR, INFO, or WARNING
    # Increment the appropriate counter
    # Print each log with its timestamp

    # Your code here

def classify_logs(logs):

    error_count = 0
    info_count = 0
    warning_count = 0

    for log in logs:

        log = log.strip()

        # Extract timestamp
        timestamp = log.split("]")[0] + "]"
        print("Timestamp:", timestamp)

        # Check log type
        if "ERROR" in log:
            error_count += 1

        elif "INFO" in log:
            info_count += 1

        elif "WARNING" in log:
            warning_count += 1

    return error_count, info_count, warning_count


logs = [
    "[14:32:05] ERROR: Disk full",
    "[14:32:10] INFO: Server started",
    "[14:33:01] WARNING: High memory usage",
    "[14:33:15] INFO: Backup complete",
    "[14:34:00] ERROR: Connection refused",
    "[14:35:22] WARNING: CPU at 90%"
]

errors, infos, warnings = classify_logs(logs)

print("\nERROR:", errors)
print("INFO:", infos)
print("WARNING:", warnings)

**OUTPUT**
Timestamp: [14:32:05]
Timestamp: [14:32:10]
Timestamp: [14:33:01]
Timestamp: [14:33:15]
Timestamp: [14:34:00]
Timestamp: [14:35:22]

ERROR: 2
INFO: 2
WARNING: 2

```



## Week 5

This week, I learnt about File handling and Data structure- 
## Example 01

In this example, I created a program that writes a shopping list to "shopping.txt" (5 items, one per line),
reads the file and prints "You need to buy: [item]" for each item and then counts and displays the total number of items.


```python

with open("shopping.txt", "w") as file:
    file.write("Milk\n")
    file.write("Bread\n")
    file.write("Eggs\n")
    file.write("Apples\n")
    file.write("Rice\n")

# Step 2: Read the file and print each item
with open("shopping.txt", "r") as file:
    items = file.readlines()

for item in items:
    print(f"You need to buy: {item.strip()}")

# Step 3: Count and display the total number of items
print(f"\nTotal number of items: {len(items)}")

**OUTPUT**

You need to buy: Milk
You need to buy: Bread
You need to buy: Eggs
You need to buy: Apples
You need to buy: Rice

Total number of items: 5
```

## Example 02
In this program, I created a tuple with 3 movies and their release years and printed "The oldest movie, "All movie titles" and also tried to change a year, which caused an error.

```python

movies = (
    ("Inception", 2010),
    ("Matrix", 1999),
    ("Interstellar", 2014)
)

# Find the oldest movie
oldest_movie = min(movies, key=lambda movie: movie[1])

# Print the oldest movie
print("Oldest movie:", oldest_movie[0], "-", oldest_movie[1])

# Print all movie titles
print("\nMovie titles:")
for title, year in movies:
    print(title)

# Try to change a year (this will cause an error)
try:
    movies[0][1] = 2011
except TypeError as e:
    print("\nError:", e)

**output**

Oldest movie: Matrix - 1999

Movie titles:
Inception
Matrix
Interstellar

Error: 'tuple' object does not support item assignment


```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)


