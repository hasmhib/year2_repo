# Quiz 089

<img width="max" alt="Screenshot 2024-10-04 at 9 36 19 AM" src="https://github.com/user-attachments/assets/7e401507-7a53-44e9-b9bd-bc40a32ee0f0">


## Trace Table


## Code

```py
def rpn(expression):
    stack = Stack()

    tokens = expression.split()

    for token in tokens:
        if token not in ["+", "-", "*", "/"]:
            stack.push(int(token))
        else:
            operand2 = stack.pop()
            operand1 = stack.pop()

            if token == "+":
                new_val = operand1 + operand2
            elif token == "-":
                new_val = operand1 - operand2
            elif token == "*":
                new_val = operand1 * operand2
            elif token == "/":
                new_val = operand1 / operand2

            stack.push(new_val)

    result = stack.pop()
    print("The result is:", result)


rpn("5 2 + 25 16 - * 3 /")

```

## Proof of work
<img width="max" alt="Screenshot 2024-10-04 at 9 38 38 AM" src="https://github.com/user-attachments/assets/71ec9e5d-309c-4683-a40a-cb26f779f346">
