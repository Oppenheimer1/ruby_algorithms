# Encode
#### This method accepts a signed integer in the 14-bit range [-8192..+8191] and returns a 4 character string.
```
def encode(i)
   i = i + 8192
   x = i.to_s(2)
   n = "0" + x.slice(0,7) + "0" + x.slice(7,15)
   m = n.to_i(2).to_s(16)
   return m
end

p encode(6111)
p encode(340)
p encode(-2628)
p encode(-255)
p encode(7550)
```