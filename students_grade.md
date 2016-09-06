# Students Grades
#### This method takes an array of student grades as input in the form of numbers and returns the letter grade.
```
def student_grade(array)
sum =  array.inject{|total,n| total + n }
num = array.length
avg = sum/num
    case
        when avg >= 90
            "A"
        when avg >= 80 
            "B"
        when avg >= 70
            "C"
        when avg >= 60
            "D"
        when avg < 60
            "F"
      end
end
```