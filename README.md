# -Stack-and-Queue-using-List
class Stack:
    def __init__(self):
        self.items = []

    def push(self, item):
        self.items.append(item)
        print(f"Pushed: {item}")

    def pop(self):
        if not self.is_empty():
            return self.items.pop()
        return "Stack is empty"

    def peek(self):
        if not self.is_empty():
            return self.items[-1]
        return "Stack is empty"

    def is_empty(self):
        return len(self.items) == 0

    def display(self):
        print("Stack:", self.items)
print("--- Stack ---")
stack = Stack()
stack.push(10)
stack.push(20)
stack.push(30)
stack.display()
print("Pop:", stack.pop())
stack.display()
print("Peek:", stack.peek())
class Queue:
    def __init__(self):
        self.items = []

    def enqueue(self, item):
        self.items.append(item)
        print(f"Enqueued: {item}")

    def dequeue(self):
        if not self.is_empty():
            return self.items.pop(0)
        return "Queue is empty"

    def is_empty(self):
        return len(self.items) == 0

    def display(self):
        print("Queue:", self.items)
print("\n--- Queue ---")
queue = Queue()
queue.enqueue(10)
queue.enqueue(20)
queue.enqueue(30)
queue.display()
print("Dequeue:", queue.dequeue())
queue.display()

output:
--- Stack ---
Pushed: 10
Pushed: 20
Pushed: 30
Stack: [10, 20, 30]
Pop: 30
Stack: [10, 20]
Peek: 20

--- Queue ---
Enqueued: 10
Enqueued: 20
Enqueued: 30
Queue: [10, 20, 30]
Dequeue: 10
Queue: [20, 30]
