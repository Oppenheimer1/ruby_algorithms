# Array Product
#### This method takes an array as input and returns the mode of the numbers.
```
def mode(array)     
  x = Hash.new(0)         
  array.each { |y| x[y] += 1 }   
  r = x.select{ |y, z| z == x.values.max }   
  r.map{|a| a[0] }    
end

p mode([22,34,35,36,36,37])
p mode([1,2,2,3,4,5,5,5,6,7,7,7])
```