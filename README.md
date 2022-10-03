# GTEC_Algorithm_week4

```
class calculate():
    def __init__(self, arg1, arg2):
        self.first = arg1
        self.second = arg2
    
    def add(self):
        result = self.first + self.second
        
        return result
    
    def subtrct(self):
        result = self.first - self.second
        
        return result
    
    def multi(self):
        result = self.first * self.second
        
        return result
        
test = calculate(4, 8)

print("test.add: {}" .format(test.add()))
print("test.subtrct: {}" .format(test.subtrct()))
print("test.multi: {}" .format(test.multi()))

bts = []

def add_data(name):
    bts.append(name)

add_data("동1")
add_data("동2")
add_data("동3")
add_data("동4")
add_data("동5")

print("bts: {}" .format(bts))

bts = ["동1", "동2", "동3", "동4", "동5"]

def insert_data(position, name):
    bts.append(None)
    
    for i in range(len(bts) - 1, position, -1):
        bts[i] = bts[i - 1]
        bts[i - 1] = None
    
    bts[position] = name

insert_data(2, "선모")
print(bts)

def delete_data(position):
    if position > len(bts) - 1 or position < 0:
        print("check your index")
        
        return 0
    bts[position] = None
    
    for i in range(position, len(bts) - 1, 1):
        bts[i] = bts[i + 1]
        bts[i + 1] = None
    
    bts.pop()

delete_data(1)
print(bts)
```
