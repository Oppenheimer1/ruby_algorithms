# Array Odd Product
#### This function takes valid RPN input and calculates the answer.
```
class Calculator
  def calculate(rpn)
    x = []
    rpn.lstrip!
    until rpn.length <= 0
      case rpn
        when /\A-?\d+(\.\d+)?/
          x.push($&.to_f)
        when /\S*/
          a = x.pop()
          b = x.pop()
          x.push(b.send($&, a))
      end
      rpn = $'
      rpn.lstrip!
    end
    x.pop()
  end
end

Einstein = Calculator.new
puts Einstein.calculate(' 8.2 0.8 1 + +')
puts Einstein.calculate('-9.521 -7 *')   
puts Einstein.calculate('50 20 -') 

```