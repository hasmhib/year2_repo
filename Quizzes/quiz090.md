# Quiz 090

<img width="max" alt="Screenshot 2024-10-07 at 11 23 40 AM" src="https://github.com/user-attachments/assets/a9b9296b-5141-46de-8d94-423311c8837e">

## Trace Table

![image](https://github.com/user-attachments/assets/429059c8-e079-4890-9cbf-2a2395d51c5c)

## Code

```py
def calculate_RPN(expression):
    rpn = RPN(expression)
    stack = Stack()

    rpn.resetNext()

    while rpn.hasNext():
        value = rpn.getNext()

        while value not in ["+", "-", "*", "/"]:
            stack.push(int(value))
            if rpn.hasNext():
                value = rpn.getNext()
            else:
                break

        operand2 = stack.pop()
        operand1 = stack.pop()

        if value == "+":
            new_val = operand1 + operand2
        elif value == "-":
            new_val = operand1 - operand2
        elif value == "*":
            new_val = operand1 * operand2
        elif value == "/":
            new_val = operand1 / operand2

        stack.push(new_val)

    result = stack.pop()
    print("The result is:", result)


calculate_RPN("5 2 + 25 16 - * 3 /")
```


## Proof of work
<img width="max" alt="Screenshot 2024-10-07 at 11 27 54 AM" src="https://github.com/user-attachments/assets/33e0654a-e74e-41b6-a32d-a4651696ab63">


