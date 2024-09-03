# Menu Based Calculator
# Revised by Johnathan Rodriguez
# Date: July 29, 2024

# Define the main function
("start here")


def displayMenu():
  print()
  print('================================')
  print('     My Personal Calculator'     )
  print('================================')
  print('   1. Addition')
  print('   2. Subtraction')
  print('   3. Multiplication')
  print('   4. Division')
  print('   5. Modulus/Remainder')
  print('================================')
  print('   Make your selection:> ', end = '')


def getMenuChoice():
  myChoice = eval(input())
  return myChoice


def getNumbers():
  a = eval(input('  Enter the first number: '))
  b = eval(input('  Enter the second number: '))
  return a, b


def getResults(choice, val1, val2):
  if choice == 1:
    print(f"  You selected Addition\n  {val1} + {val2} = ", end='')
    print(addThem(val1, val2))
  elif choice == 2:
    print(f"  You selected Subtraction\n  {val1} - {val2} = ", end='')
    print(subtractThem(val1, val2))
  elif choice == 3:
    print(f"  You selected Multiplication\n  {val1} * {val2} = ", end='')
    print(multiplyThem(val1, val2))
  elif choice == 4:
    print(f"  You selected Division\n  {val1} / {val2} = ", end='')
    print(divideThem(val1, val2))
  elif choice == 5:
    print(f"  You selected Modulus\n  {val1} % {val2} = ", end='')
    print(modulusThem(val1, val2))


def addThem(a, b):
  return a + b


def subtractThem(a, b):
  return a - b


def multiplyThem(a, b):
  return a * b


def divideThem(a, b):
  if b == 0:
    b = 1
    print('Oops! Divide by zero...bad answer', end='...')
  return a / b


def modulusThem(a, b):
  if b == 0:
    b = 1
  return a % b

# The main part of the program should be here
while True:
  displayMenu()
  choice = getMenuChoice()
  num1, num2 = getNumbers()
  getResults(choice, num1, num2)

  # Ask the user if they want to continue
  continue_calc = input("Do you want to continue? (y/n): ")
  if continue_calc.lower() != 'y':
    break
