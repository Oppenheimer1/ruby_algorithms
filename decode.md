# Decode
#### This method accepts two bytes on input, both in the range [0x00..0x7F] and recombine them to return the corresponding integer between [-8192..+8191]

def decode(n)
   x = n.to_s
   a = ("00" + convert(x.slice(0,2).hex.to_s(2), 7) + convert(x.slice(2,4).hex.to_s(2), 7)).to_i(2) - 8192
end

def convert(r, t)
   while r.length < t
      r = "0" + r
   end
   return r
end

p decode('0A0A')
p decode('0029')
p decode('3F0F')
p decode('4400')
p decode('5E7F')
```