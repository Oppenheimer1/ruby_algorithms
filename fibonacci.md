# Fibonacci
#### This function takes a number and determines if it is part of the Fibonacci Sequence.
```
def is_fibonacci?(x, y = 0, z = 1) 
    if (x == y || x == z)
        true
    else
      a = y + z
      if (a == x)
        true
      elsif (a > x)
        false
      else
        is_fibonacci?(x, z, a)
      end
    end
end
 
p is_fibonacci?(13)  	
p is_fibonacci?(55)  	
p is_fibonacci?(56)  	
p is_fibonacci?(612) 
```