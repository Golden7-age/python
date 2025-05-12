Assignment on Introduction to Python

Create a simple Python program that asks the user to input two numbers and a mathematical operation (addition, subtraction, multiplication, or division).
Perform the operation based on the user's input and print the result.
Example: If a user inputs 10, 5, and +, your program should display 10 + 5 = 15.

Simple Calculator Program

def calculate(num1, num2, operation):
    """
    Perform the specified mathematical operation on two numbers.
    
    Args:
    num1 (float): First number
    num2 (float): Second number
    operation (str): Mathematical operation (+, -, *, /)
    
    Returns:
    float: Result of the operation
    """
    if operation == '+':
        return num1 + num2
    elif operation == '-':
        return num1 - num2
    elif operation == '*':
        return num1 * num2
    elif operation == '/':
        # Handle division by zero
        if num2 == 0:
            return "Error: Division by zero"
        return num1 / num2
    else:
        return "Error: Invalid operation"

def main():
    print("Simple Calculator")
    print("----------------")
    
    # Get first number input
    while True:
        try:
            num1 = float(input("Enter the first number: "))
            break
        except ValueError:
            print("Invalid input. Please enter a valid number.")
    
    # Get second number input
    while True:
        try:
            num2 = float(input("Enter the second number: "))
            break
        except ValueError:
            print("Invalid input. Please enter a valid number.")
    
    # Get operation input
    while True:
        operation = input("Enter the operation (+, -, *, /): ")
        if operation in ['+', '-', '*', '/']:
            break
        else:
            print("Invalid operation. Please enter +, -, *, or /.")
    
    # Calculate and display result
    result = calculate(num1, num2, operation)
    
    # Format and print the result
    print(f"\n{num1} {operation} {num2} = {result}")

# Run the calculator
if __name__ == "__main__":
    main()
