# Decipher
#### This function takes an encrypted message and deciphers it.
```
def decipher(coded_message)
    x = coded_message.gsub(/\@|\#|\$|\%|\^|\&|\*/, ' ')
    x.tr!("A-Za-z", "W-ZA-Vw-za-v")
    if x.match(/\d+/) 
        x.gsub!(/\d+/) { |num| num.to_i / 100 } 
    end  
    return x
end

p decipher("ger^wsqifshc*nywx^kix^qi&10000*fekw@sj$gssp%vergl@hsvmxsw?")
```