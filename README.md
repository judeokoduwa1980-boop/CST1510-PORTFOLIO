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



