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
______________________________________________#لیست ها
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
