# Array Product
#### This function returns the number missing in a list of sequential numbers from 1 to 10,000.
```
def find_missing_number(string)
  string_sum = 0
  x = string.split(",")
  y = x.map(&:to_i)
  y.length.times do |i|
  	string_sum = string_sum + y[i]
  end
  total_amt = (1..10000).inject { |a, b| a + b } 
  difference = total_amt - string_sum
end

puts find_missing_number(string_missing_4567)
```