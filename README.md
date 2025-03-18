# Basic-calculator-program
# Simple calculator program

# Function to perform the chosen operation
def calculate(num1, num2, operation):
    if operation == 'addition':
        return num1 + num2
    elif operation == 'subtraction':
        return num1 - num2
    elif operation == 'multiplication':
        return num1 * num2
    elif operation == 'division':
        if num2 != 0:
            return num1 / num2
        else:
            return "Error: Division by zero is not allowed."
    else:
        return "Error: Invalid operation."

# Main program
def main():
    try:
        # Asking user for input
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
        operation = input("Enter the operation (addition, subtraction, multiplication, division): ").lower()

        # Performing the calculation
        result = calculate(num1, num2, operation)

        # Displaying the result
        if isinstance(result, str):
            print(result)
        else:
            print(f"The result of {num1} {operation} {num2} is: {result}")

    except ValueError:
        print("Error: Please enter valid numbers.")

# Running the main program
if __name__ == "__main__":
    main()
