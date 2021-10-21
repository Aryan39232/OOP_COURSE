class Queue:
    def _init_(self):
        self.items = []

    def isEmpty(self):
        return self.items == []

    def enqueue(self, item):
        self.items.insert(0,item)

    def dequeue(self):
        return self.items.pop()

    def size(self):
        return len(self.items)
q = Queue()
q.enqueue(3)
q.enqueue(5)
q.enqueue(8)
q.enqueue(9)
q.dequeue()
