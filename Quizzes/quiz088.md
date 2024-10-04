# Quiz 088

<img width="max" alt="Screenshot 2024-10-04 at 9 29 50 AM" src="https://github.com/user-attachments/assets/599efdda-2506-432f-8385-17852467ce43">

## Code

```py
class Stack:
    def __init__(self):
        self.data = Queue()

    def isEmpty(self):
        return self.data.isEmpty()

    def push(self, value):
        self.data.enqueue(value)

    def pop(self):
        temp_queue = Queue()
        while not self.data.isEmpty():
            value = self.data.dequeue()
            if not self.data.isEmpty():
                temp_queue.enqueue(value)
            else:
                last_value = value

        self.data = temp_queue
        return last_value


print(Stack().push('bob')) 
```

## Proof of work
<img width="max" alt="Screenshot 2024-10-04 at 9 34 31 AM" src="https://github.com/user-attachments/assets/fad55e63-a650-45c7-9689-69e5870ea7e0">
