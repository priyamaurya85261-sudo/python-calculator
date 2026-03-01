# python-calculator
A simple calculator built using python that performs basic arithmetic operations like addition, subtraction, multiplication, division, modulus, and power.
def add(a,b):
    return a+b
def sub(a,b):
    return a-b
def mul(a,b):
    return a*b
def div(a,b):
    if b==0:
        return "Error : can't be divide byh zero"
    return a/b
def mod(a,b):
    return a%b
def power(a,b):
    return a**b



def calcu_menu():
    print("\n-----PYTHON CALCULATOR-----")
    print("1.Addition(+)")
    print("2.Subtraction(-)")
    print("3.Multiplication(*)")
    print("4.Division(/)")
    print("5.Modulus(%)")
    print("6.Power(**)")
    print("7.Exit")

while True:
    calcu_menu()
    choice=input("Enter your choice(1-7):")
    if choice=="7":
        print("calculator closed.")
        break
    if choice not in['1','2','3','4','5','6']:
        print("invalid choice!Try again.")
        continue
    try:
        num1=float(input("Enter first number:"))
        num2=float(input("Enter second number:"))
    except valueError:
        print("invalid input!Please enter numbers only.")
        continue
    if choice=='1':
        result=add(num1,num2)
    elif choice=='2':
        result=sub(num1,num2)
    elif choice=='3':
        result=mul(num1,num2)
    elif choice=='4':
        result=div(num1,num2)
    elif choice=='5':
        result=mod(num1,num2)
    elif choice=='6':
        result=power(num1,num2)

    print("Result:",result)
