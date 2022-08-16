


## 二： 实现

```python 
class Solution:
    def __init__(self): 
        self.stack = []
        self.stack_min = []
        
    def push(self, node):
        # write code here
        self.stack.append(node)
        if not self.stack_min:
            self.stack_min.append(node)
        else: 
            self.stack_min.append(min(node, self.stack_min[-1]))
            
    def pop(self):
        # write code here
        self.stack_min.pop()
        return self.stack.pop()
        
        
    def top(self):
        # write code here
        return self.stack[-1]
        
        
    def min(self):
        # write code here
        return self.stack_min[-1]
```