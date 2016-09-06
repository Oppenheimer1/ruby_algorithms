# String Test
#### This method accepts a string as a password and returns true if the string is between 6 and 20 characters long, contains at least one capital letter and contains at least one number or one of the following special characters("!, @, #, $, %, &, *, +, :, ?").
```
 def password_check(valid_password)
  if valid_password !~ (/^(?=.{6,20}$)/)
    puts 'Your Password needs to be between 6 and 20 characters long'
    false 
  elsif valid_password !~ (/^(?=.*?[A-Z])/)
    puts 'Your password needs to contain at least one capital letter'
    false
  elsif valid_password !~ (/^(?=.*?([0-9]|@|\#|\$|\%|\&|\*|\+|\:|\?)).{6,20}$/)
    puts 'Your password needs to contain a least on numer or one of the following special characters: "!, @, #, $, %, &, *, +, :, ?"'
    false
  elsif valid_password.match(/^(?=.*?[|\"|\'|\(|\)|\,|\-|\.|\/|\;|\<|\=|\>|\?|\[\|\|\]\|^\|\|\_|\`|\{|\||\}|\~|\´])/)
    puts 'You have entered an invalid character, your password may only contain the following special characers: !, @, #, $, %, &, *, +, :, ?'
    false
  else
    true
  end
end

p password_check("abc9Ada") == true
p password_check("abcdA@") == true
 
```