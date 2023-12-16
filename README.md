#لیست ها
#اضافه کردن به ابتدای لیست یک طرفه
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def display(self):
        t = node()
        t = self.head
        while(t != None):
            print(t.data, end='-->')
            t = t.next
        print('none')
______________________________________________
#اضافه کردن انتهای لیست یک طرفه
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
        
    def addinend(self, data):
        n = node(data)
        t = self.head
        while(t.next != None):
            t = t.next
        t.next = n
        if(t == None):
            self.head = n
        else:
            while(t.next! =none):
                t = t.next
            t.next = n
______________________________________________
#اضافه کردن میانه لیست یک طرفه 
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def addafter(self, m, d):
        n = node(d) 
        t = self.head
        while (t.data != m):
            t = t.next
        n.next = t.next
        t.next = n
______________________________________________
#تابع پاک کردن ابتدای لیست یک طرفه
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
        
    def delete_first(self):
        if(self.head == None):
            return 'empty'
        else:
            self.head = self.head.next
______________________________________________
#پاک کردن انتهای لیست یک طرفه
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def dellast(self):
        t = self.head
        if(t == None):
            return
        elif(t.next == None):
            self.head = None
        else:
            while(t.next.next != None):
                t = t.next
            t.next = None
______________________________________________
#تابع پاک کردن میانه لیست یک طرفه 
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def delafter(self, m):
        t = self.head
        while(t.data != m):
            t = t.next
        t.next = t.next.next
______________________________________________
#لیست ها
#اضافه کردن به ابتدای لیست
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def display(self):
        t = node()
        t = self.head
        while(t != None):
            print(t.data, end='-->')
            t = t.next
        print('none')
______________________________________________
#اضافه کردن انتهای لیست
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
        
    def addinend(self, data):
        n = node(data)
        t = self.head
        while(t.next != None):
            t = t.next
        t.next = n
        if(t == None):
            self.head = n
        else:
            while(t.next! =none):
                t = t.next
            t.next = n
______________________________________________
#اضافه کردن میانه لیست 
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def addafter(self, m, d):
        n = node(d) 
        t = self.head
        while (t.data != m):
            t = t.next
        n.next = t.next
        t.next = n
______________________________________________
#تابع پاک کردن ابتدای لیست
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
        
    def delete_first(self):
        if(self.head == None):
            return 'empty'
        else:
            self.head = self.head.next
______________________________________________#پاک کردن انتهای لیست
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def dellast(self):
        t = self.head
        if(t == None):
            return
        elif(t.next == None):
            self.head = None
        else:
            while(t.next.next != None):
                t = t.next
            t.next = None
______________________________________________
#تابع پاک کردن میانه لیست
class node:
    def __init__(self, d):
        self.data = d
        self.next = None

class linkedlist:
    def __init__(self):
        self.head = None
    
    def delafter(self, m):
        t = self.head
        while(t.data != m):
            t = t.next
        t.next = t.next.next
______________________________________________
مثال لیست های (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delmid(self):
        t = self.head
        count = 0
        while(t != None):
            t = t.next
            count += 1
        if count % 2 == 0:
            for i in range(count // 2):
                t = t.next
        else:
            for i in range(count // 2 + 1):
                t = t.next
        t.next.prev = t.prev
        t.prev.next = t.next
        t = next
        t.prev = None
______________________________________________
#تابع پاک شدن میانه لیست(دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def delete(self, data):
        t = self.head
        while(t and t.data != data):
            t = t.next
        if t:
            t.next.prev = t.prev
            t.prev.next = t.next
            t.next = None
            t.prev = None
______________________________________________
#تابع پاک شدن انتهای لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def dellast(self):
        if self.head is None:
            return 1
        t = self.head
        while t.next is not None:
            t = t.next
        t.prev.next = None
        t.prev = None
______________________________________________
تابع پاک شدن ابتدای لیست ‌(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delfirst(self):
        if self.head is None:
            return 1
        self.head = self.head.next
        self.head.prev = None
______________________________________________
تابع اضافه شدن به میانه لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def addafter(self, m, data):
        n = dnode(data)
        t = self.head
        while t.data != m:
            t = t.next
        n.next = t.next
        n.prev = t
        if t.next:
            t.next.prev = n
        t.next = n
______________________________________________
#تابع اضافه شدن به انتهای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_end(self, d):
        n = DNode(d)
        if not self.head:
            self.head = n
        else:
            t = self.head
            while t.next:
                t = t.next
            t.next = n
            n.prev = t
______________________________________________
#تابع اضافه شدن به ابتدای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_start(self, data):
        n = DNode(data) 
        n.next = self.head
        self.head.prev = n
        self.head = n 
______________________________________________
# تابع اضافه‌ شدن به ابتدای لیست (دو طرفه همراه باشرط) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def add_in_start(self, data):
        n = DNode(data)
        if self.head != None:
            n.next = self.head
            self.head.prev = n
        self.head = n
______________________________________________مثال لیست های (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delmid(self):
        t = self.head
        count = 0
        while(t != None):
            t = t.next
            count += 1
        if count % 2 == 0:
            for i in range(count // 2):
                t = t.next
        else:
            for i in range(count // 2 + 1):
                t = t.next
        t.next.prev = t.prev
        t.prev.next = t.next
        t = next
        t.prev = None
______________________________________________
#تابع پاک شدن میانه لیست(دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def delete(self, data):
        t = self.head
        while(t and t.data != data):
            t = t.next
        if t:
            t.next.prev = t.prev
            t.prev.next = t.next
            t.next = None
            t.prev = None
______________________________________________
#تابع پاک شدن انتهای لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def dellast(self):
        if self.head is None:
            return 1
        t = self.head
        while t.next is not None:
            t = t.next
        t.prev.next = None
        t.prev = None
______________________________________________
تابع پاک شدن ابتدای لیست ‌(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delfirst(self):
        if self.head is None:
            return 1
        self.head = self.head.next
        self.head.prev = None
______________________________________________
تابع اضافه شدن به میانه لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def addafter(self, m, data):
        n = dnode(data)
        t = self.head
        while t.data != m:
            t = t.next
        n.next = t.next
        n.prev = t
        if t.next:
            t.next.prev = n
        t.next = n
______________________________________________
#تابع اضافه شدن به انتهای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_end(self, d):
        n = DNode(d)
        if not self.head:
            self.head = n
        else:
            t = self.head
            while t.next:
                t = t.next
            t.next = n
            n.prev = t
______________________________________________
#تابع اضافه شدن به ابتدای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_start(self, data):
        n = DNode(data) 
        n.next = self.head
        self.head.prev = n
        self.head = n 
______________________________________________
# تابع اضافه‌ شدن به ابتدای لیست (دو طرفه همراه باشرط) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def add_in_start(self, data):
        n = DNode(data)
        if self.head != None:
            n.next = self.head
            self.head.prev = n
        self.head = n
______________________________________________مثال لیست های (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delmid(self):
        t = self.head
        count = 0
        while(t != None):
            t = t.next
            count += 1
        if count % 2 == 0:
            for i in range(count // 2):
                t = t.next
        else:
            for i in range(count // 2 + 1):
                t = t.next
        t.next.prev = t.prev
        t.prev.next = t.next
        t = next
        t.prev = None
______________________________________________
#تابع پاک شدن میانه لیست(دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def delete(self, data):
        t = self.head
        while(t and t.data != data):
            t = t.next
        if t:
            t.next.prev = t.prev
            t.prev.next = t.next
            t.next = None
            t.prev = None
______________________________________________
#تابع پاک شدن انتهای لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def dellast(self):
        if self.head is None:
            return 1
        t = self.head
        while t.next is not None:
            t = t.next
        t.prev.next = None
        t.prev = None
______________________________________________
تابع پاک شدن ابتدای لیست ‌(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delfirst(self):
        if self.head is None:
            return 1
        self.head = self.head.next
        self.head.prev = None
______________________________________________
تابع اضافه شدن به میانه لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def addafter(self, m, data):
        n = dnode(data)
        t = self.head
        while t.data != m:
            t = t.next
        n.next = t.next
        n.prev = t
        if t.next:
            t.next.prev = n
        t.next = n
______________________________________________
#تابع اضافه شدن به انتهای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_end(self, d):
        n = DNode(d)
        if not self.head:
            self.head = n
        else:
            t = self.head
            while t.next:
                t = t.next
            t.next = n
            n.prev = t
______________________________________________
#تابع اضافه شدن به ابتدای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_start(self, data):
        n = DNode(data) 
        n.next = self.head
        self.head.prev = n
        self.head = n 
______________________________________________
# تابع اضافه‌ شدن به ابتدای لیست (دو طرفه همراه باشرط) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def add_in_start(self, data):
        n = DNode(data)
        if self.head != None:
            n.next = self.head
            self.head.prev = n
        self.head = n
______________________________________________مثال لیست های (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delmid(self):
        t = self.head
        count = 0
        while(t != None):
            t = t.next
            count += 1
        if count % 2 == 0:
            for i in range(count // 2):
                t = t.next
        else:
            for i in range(count // 2 + 1):
                t = t.next
        t.next.prev = t.prev
        t.prev.next = t.next
        t = next
        t.prev = None
______________________________________________
#تابع پاک شدن میانه لیست(دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

class DoublyLinkedList:
    def __init__(self):
        self.head = None
    
    def delete(self, data):
        t = self.head
        while(t and t.data != data):
            t = t.next
        if t:
            t.next.prev = t.prev
            t.prev.next = t.next
            t.next = None
            t.prev = None
______________________________________________
#تابع پاک شدن انتهای لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def dellast(self):
        if self.head is None:
            return 1
        t = self.head
        while t.next is not None:
            t = t.next
        t.prev.next = None
        t.prev = None
______________________________________________
تابع پاک شدن ابتدای لیست ‌(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
        
    def delfirst(self):
        if self.head is None:
            return 1
        self.head = self.head.next
        self.head.prev = None
______________________________________________
تابع اضافه شدن به میانه لیست (دوطرفه) 
class dnode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def addafter(self, m, data):
        n = dnode(data)
        t = self.head
        while t.data != m:
            t = t.next
        n.next = t.next
        n.prev = t
        if t.next:
            t.next.prev = n
        t.next = n
______________________________________________
#تابع اضافه شدن به انتهای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_end(self, d):
        n = DNode(d)
        if not self.head:
            self.head = n
        else:
            t = self.head
            while t.next:
                t = t.next
            t.next = n
            n.prev = t
______________________________________________
#تابع اضافه شدن به ابتدای لیست(دوطرفه) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None
    def add_in_start(self, data):
        n = DNode(data) 
        n.next = self.head
        self.head.prev = n
        self.head = n 
______________________________________________
# تابع اضافه‌ شدن به ابتدای لیست (دو طرفه همراه باشرط) 
class DNode:
    def __init__(self, data):
        self.data = data
        self.next = None
        self.prev = None

    def add_in_start(self, data):
        n = DNode(data)
        if self.head != None:
            n.next = self.head
            self.head.prev = n
        self.head = n
______________________________________________
#صف ها و استک ها
#عمل نمایش دادن صف 
def disqueue(self):
    if self.Front == -1:
        print('empty')
    for i in range(self.Front, self.rear+1):
        print(self.queue[i])
______________________________________________
#عمل اضافه شدن صف
def insqueue(self, data):
    if self.inqueue:
        if self.rear == -1:
            self.front = 0
            self.rear = 0
            self.queue[0] = data
        elif self.rear+1 == self.k:
            print('is full')
        else:
            self.rear += 1
            self.queue[self.rear] = data
______________________________________________
#عمل پاک شدن صف
def dqueue(self):
    if self.front == -1:
        print('empty')
    elif self.front == self.rear:
        t = self.queue[self.front]
        self.front = -1
        self.rear = -1
        return t
    else:
        t = self.queue[self.front]
        self.front += 1
        return t
______________________________________________
#تابع اضافه شدن صف حلقوی
def inqueue_c(self, data):
    if (self.rear + 1) % k == self.front:
        print('full')
    elif self.front == -1:
        self.front = 0
        self.rear = 0
        self.queue[self.rear] = data
    else:
        self.rear += 1
        self.queue[self.rear] = data
______________________________________________
#تابع پاک شدن حلقوی
def dqueue_c(queue, front, rear, k):
    if front == -1:
        print('empty')
    elif front == rear:
        t = queue[front]
        front = -1
        rear = -1
        return t
    else:
        t = queue[front] 
        front = (front + 1) % k
        return t
______________________________________________
#تابع نمایش حلقوی
def disqueue_c(self):
    if self.front == -1:
        print('empty')
    elif (self.front <= self.rear):
        for i in range(self.front, self.rear + 1):
            pass
    else:
        for j in range(self.front, k):
            for i in range(self.rear + 1):
                print(self.queue[i])
______________________________________________
#تابع نمایش استک ها
class Stack:
 def __init__(self):
 self.items = []
def display(self):
    if len(self.stack) <= 0:
        return -1
    else:
        for i in self.stack:
            print(i)
______________________________________________
#مثال استک ها (1)
class Stack:
 def __init__(self):
 self.items = []
def 2_bin(self, number):
    s = Stack()
    while number > 0:
        r = number % 2
        s.push(r)
    b = ""
    while not s.is_empty():
        b = b + str(s.pop())
    return b
______________________________________________
#مثال استک ها (2) 
class Stack: 
def __init__(self): 
self.items = []
def reverse(lst):
    s = []
    for e in lst:
        s.push (e)
    for i in range(len(lst)):
        lst[i] = s.pop()
______________________________________________
#مثال استک ها (3)
class Stack:
    def __init__(self):
        self.items = []
def reverse_stack(s):
    s1 = Stack()
    while not s.is_empty():
        s1.push(s.pop())
    
    s2 = Stack()
    while not s1.is_empty():
        s2.push(s1.pop())
    
    while not s2.is_empty():
        s.push(s2.pop())
______________________________________________
#مثال استک ها (4)
class Stack: 
def __init__(self): 
self.items = []
def match_s(string):
s = []
for i in string:
if i in '([{':
s.append(i)
elif i in ')]}':
if not s:
return False
if i == ')' and s[-1] == '(':
s.pop()
elif i == ']' and s[-1] == '[':
s.pop()
elif i == '}' and s[-1] == '{':
s.pop()
else:
return False
return len(s) == 0
______________________________________________
