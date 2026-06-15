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

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)



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

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)

## Week 3

This week, I learnt about **Slicing in lists** **Defining and using functions** **Lambda expressions for concise coding** **Working with multidimensional lists (nested lists)**

## Example 01


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
This code is used to calculate **Body mass index (BMI)** 
It prompts users to input their weight in pounds and also their height in inches, then it converts weight into metrics by multiplying by 0.45359237, also coverts heights in inches into meters by multiplying by 0.0254. The resultant weight is then didvided by the height to give the BMI and the result printed. if the bmi < 18.5, it prints overweight, else if it is <= 25, it prints normal, else it prints obese.

```python

def sublist(list1, list2, list3):
    return True if list2 in list1 else False

list1 = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
list2 = [1, 2, 3]
list3 = [4, 5, 6]

print(sublist(list1, list2, list3))



```

## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License

[MIT](https://choosealicense.com/licenses/mit/)


