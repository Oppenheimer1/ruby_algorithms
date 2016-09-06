# String Test
#### This method accepts a string and returns true if the brackets, parentheses, and curly braces close correctly.
```
def valid_string?(string)
  image = ['[', '(', '{']
  reflection = [']', ')', '}']
  x = []
  string.each_char do |i|
    x.push(i) if image.include?(i)
    if reflection.include?(i)
        if image.index(x.pop) != reflection.index(i)
           return false
        else
        end
    end
  end
  if x.length == 0 
    true
  else
    false
  end
end
           
p valid_string?("[ ( text ) {} ]")

```