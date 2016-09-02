# Array Odd Product
#### This function takes an array as input and returns the product of all the odd numbers in the array.
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

puts calculate_product_odd([1,2,3,4,5,6,7,8,9,10,11])
```