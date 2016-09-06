# Array Product
#### This method takes an array as input and returns the product of all the numbers in the array.
```
def calculate_product(array)
    if array.length == 0
      nil
    else
      product = 1
      array.each do |i|
      product *=i
      end
      product
  end
end

puts calculate_product([1,3,5,7,9,11,13,15,19,21])
```

