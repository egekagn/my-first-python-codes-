# Simple calculator program
import random
x = input("enter the number assigened to operation you want "
          "1 for addition, 2 for subtraction, 3 for multiplication, 4 for division:")
y = input("enter the first number: ")
z = input("enter the second number: ")
if x == '1':
    print(f'{y} + {z} = {int(y) + int(z)}')
elif x == '2':
    print(f'{y} - {z} = {int(y) - int(z)}')
elif x == '3':
    print(f'{y} * {z} = {int(y) * int(z)}')
elif x == '4':
    print(f'{y} / {z} = {int(y) / int(z)}')
else:
    print("Invalid operation selected. Please choose a number between 1 and 4.")
print("Thank you for using the calculator!")


# Simple equality check program
x = input("enter a number")
y = input("enter another number")
if int(x.strip()) == int(y.strip()):
    print("The numbers are equal.")
else:
    print("The numbers are not equal.")


# Simple text printer program
x = input("number of copys you want to print: ")
y = input("enter the text you want to print: ")
for a in range(int(x)):
    print(y)
a = input("Press Enter to exit.")
print("Thank you for using the text printer!")


# Simple dice rolling program


def roll_dice():
    return random.randint(1, 6)


while True:
    input("Press Enter to roll the dice...")
    result = roll_dice()
    print(f"You rolled a {result}.")

    again = input("Do you want to roll again? (yes/no): ").strip().lower()
    if again != 'yes':
        print("Thank you for playing!")
        break


# Simple even number counter program
count = 0
for number in range(1, 100):
    if number % 2 == 0:
        count += 1
        print(number)
print(f"total even numbers:! {count}")

#volume calc

import math

def mult(a, b, c):
    return a * b * c


def mults(x, y):
    return x**2 * y * math.pi


def multp(e, r, h):
    return e * r * h * 1/3


def multc(f):
    return f**3 * math.pi * 4/3

while True:
    print("\n" + "=" * 30)
    print("Volume Calculator")
    print("Choose a shape:")
    print("1. Cube")
    print("2. Cylinder")
    print("3. pyramid")
    print("4. sphere")
    print("0. Exit")
    chose = input("Enter your choice (1 - 2 - 3 - 4 - 0): ")

    if chose == '1':
        a = int(input("Enter height: "))
        b = int(input("Enter width: "))
        c = int(input("Enter depth: "))

        print(f"volume: {mult(a, b, c)} cm³")

    elif chose == '2':
        x = int(input("Enter radius: "))
        y = int(input("Enter height: "))

        print(f"volume: {round(mults(x, y))} cm³")

    elif chose == '3':
        e = int(input("Enter lenght: "))
        r = int(input("Enter width: "))
        h = int(input("Enter height: "))

        print(f"volume: {round(multp(e, r, h))} cm³")

    elif chose == '4':
        f = int(input("Enter radius: "))

        print(f"volume: {round(multc(f))} cm³")

    elif chose == "0":
        print("Exiting the calculator.")
        break
