# Number by Commas
#### This method takes a number and adds commas to make the number more readable if the number is greater then 999.
```
def add_comma(number)
  if number >= 1000000
    number.to_s.gsub(/(\d{1,3})[^\d]?(\d{3})[^\d]?(\d{3})/, '\1,\2,\3')
  elsif number >=1000
    number.to_s.gsub(/(^\d{1,3})(\d{3}$)/, '\1,\2')
  else
    number.to_s
  end
end
  
p add_comma(1000)   
p add_comma(9876543)    
p add_comma(123456)   
p add_comma(9876543)  
```