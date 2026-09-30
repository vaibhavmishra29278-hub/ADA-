Practical No. 1
Aim: Learn the Basics of R Programming (Data Types, Variables, Operators)  
> a = 10
> b = 15

# Data Types
> num = 100
> char = "MSC"
> logical = TRUE

# Operators
> sum = a + b
> sub = a - b
> mul = a * b
> div = a / b

> sum
[1] 25
> sub
[1] -5
> mul
[1] 150
> div
[1] 0.6666667

practical 2
Implement R Loops  
> for (i in 1:5) {
+   print(i)
+ }
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5

> j = 1
> while(j <= 5) {
+   print(j)
+   j = j + 1
+ }
[1] 1
[1] 2
[1] 3
[1] 4
[1] 5

practical 3 
Aim: Learn the basics of functions in R and implement them with examples  
# Eg 1) Function to Add Two Numbers
> add = function(a, b) {
+   res = a + b
+   return(res)
+ }
> sum = add(10, 20)
> print(sum)
[1] 30

# Eg 2) Function to Find the Square of a Number
> sq = function(x) {
+   return(x ^ 2)
+ }
> print(sq(5))
[1] 25

# Eg 3) Function Without Parameters
> greet = function() {
+   print("welcome to R Programming")
+ }
> greet()
[1] "welcome to R Programming"

# Eg 4) Function to Find Maximum of Two Numbers
> max = function(a, b) {
+   if (a > b)
+     return(a)
+   else
+     return(b)
+ }
> print(max(15, 10))
[1] 15

practical 4 
A) Implement Data Frames in R and Join Columns & Rows Using cbind() and rbind()
# First data frame
> student = data.frame(
+   rollno = c(1, 2, 3),
+   name = c("Rahul", "Priya", "Amit")
+ )
> print(student)
  rollno  name
1      1 Rahul
2      2 Priya
3      3  Amit

# Second data frame
> marks = data.frame(
+   markss = c(85, 90, 88)
+ )
> print(marks)
  markss
1     85
2     90
3     88

# Combine columns
> res = cbind(student, marks)
> print(res)
  rollno  name markss
1      1 Rahul     85
2      2 Priya     90
3      3  Amit     88

# Joining rows using rbind
> df1 = data.frame(
+   rollno = c(1, 2),
+   name = c("Rahul", "Priya")
+ )
> df2 = data.frame(
+   rollno = c(3, 4),
+   name = c("Amit", "Neha")
+ )
> new = rbind(df1, df2)
> print(new)
  rollno  name
1      1 Rahul
2      2 Priya
3      3  Amit
4      4  Neha

B) Implement a program in R using Probability distribution  
# 1. Normal Distribution
> print(dnorm(65, mean = 60, sd = 5))
[1] 0.04839414
> print(pnorm(65, mean = 60, sd = 5))
[1] 0.8413447
> print(qnorm(0.95, mean = 60, sd = 5))
[1] 68.22427
> set.seed(100)
> print(rnorm(5, mean = 60, sd = 5))
[1] 57.48904 60.65766 59.60541 64.43392 60.58486

# 2. Poisson Distribution
> print(dpois(6, lambda = 4))
[1] 0.1041956
> print(ppois(6, lambda = 4))
[1] 0.889326
> print(qpois(0.90, lambda = 4))
[1] 7
> set.seed(100)
> print(rpois(5, lambda = 4))
[1] 3 3 4 1 4

# 3. Uniform Distribution
> print(dunif(50, min = 1, max = 100))
[1] 0.01010101
> print(punif(50, min = 1, max = 100))
[1] 0.4949495
> print(qunif(0.75, min = 1, max = 100))
[1] 75.25
> set.seed(100)
> print(runif(5, min = 1, max = 100))
[1] 31.468845 26.509578 55.679921

# 4. Exponential Distribution
> print(dexp(1, rate = 2))
[1] 0.2706706
> print(pexp(1, rate = 2))
[1] 0.8646647
> print(qexp(0.90, rate = 2))
[1] 1.151293
> set.seed(100)
> print(rexp(5, rate = 2))
[1] 0.46210581 0.36191859 0.05232243 1.54868117 0.31240262

practical 5
Aim: To implement different String Manipulation Functions in R.  
> str = "R Programming Language"
> print(nchar(str))
[1] 22

> print(toupper(str))
[1] "R PROGRAMMING LANGUAGE"

> print(tolower(str))
[1] "r programming language"

> print(substr(str, 1, 5))
[1] "R Pro"

> print(strrep("R", 5))
[1] "RRRRR"

> print(sub("Programming", "Coding", str))
[1] "R Coding Language"

> print(strsplit(str, " "))
[[1]]
[1] "R" "Programming" "Language"

> print(identical("R", "R"))
[1] TRUE

> print(trimws(" R Programming "))
[1] "R Programming"

practical 6
Aim: Implement Different Data Structures in R (Vectors, Lists, Data Frames)  
# Step 1: Creation for the Vector and List
> vect = c(10, 20, 30, 40, 50)
> print(vect)
[1] 10 20 30 40 50

> listdata = list(
+   name = "Rahul",
+   age = 22,
+   percent = 85.5,
+   passed = TRUE
+ )
> print(listdata)
$name
[1] "Rahul"
$age
[1] 22
$percent
[1] 85.5
$passed
[1] TRUE

# Step 2: Using Data Frame
> studdata = data.frame(
+   roll = c(1, 2, 3),
+   name = c("Rahul", "Priya", "Amit"),
+   marks = c(85, 90, 88)
+ )
> print(studdata)
  roll  name marks
1    1 Rahul    85
2    2 Priya    90
3    3  Amit    88

> print(vect[2])
[1] 20
> print(listdata$name)
[1] "Rahul"
> print(studdata$marks)
[1] 85 90 88

practical 7
Practical No. 7
Aim: Write a program to read a csv file and analyze the data in the file in R  
> getwd()
[1] "C:/Users/Pranal PC/OneDrive/Documents"

> data = read.csv("prac7.csv")
> data
  rollno  name marks
1      1 rahul    85
2      2 priya    90
3      3  amit    88
4      4  neha    92
5      5 rohan    80

> head(data)
  rollno  name marks
1      1 rahul    85
2      2 priya    90
3      3  amit    88
4      4  neha    92
5      5 rohan    80

> tail(data)
  rollno  name marks
1      1 rahul    85
2      2 priya    90
3      3  amit    88
4      4  neha    92
5      5 rohan    80

> str(data)
'data.frame': 5 obs. of 3 variables:
 $ rollno: int 1 2 3 4 5
 $ name  : chr "rahul" "priya" "amit" "neha" ...
 $ marks : int 85 90 88 92 80

> summary(data)
     rollno      name               marks      
 Min.   :1   Length:5           Min.   :80.0  
 1st Qu.:2   Class :character   1st Qu.:85.0  
 Median :3   Mode  :character   Median :88.0  
 Mean   :3                      Mean   :87.0  
 3rd Qu.:4                      3rd Qu.:90.0  
 Max.   :5                      Max.   :92.0  

> dim(data)
[1] 5 3

> names(data)
[1] "rollno" "name"   "marks" 

> print(data[,1])
[1] 1 2 3 4 5

> mean(data$marks)
[1] 87

Practical No. 8
Aim: Write a program in R to create different graph using dataframe  
> stud = c(40, 30, 20, 10)
> dept = c("Science", "Commerce", "Arts", "Management")

# Pie Chart
pie(stud, labels = dept, main = "Student Distribution by Department")

# Bar Plot
barplot(stud, names.arg = dept, main = "Student Distribution by Department", 
        xlab = "Departments", ylab = "Number of Students", col = "lightblue")

# Line Chart / Monthly Sales Plot
plot(sales, type = "o", col = "blue", main = "Monthly Sales", xlab = "Months", ylab = "Sales")

# Scatter Plot with Dynamic Input
n = as.integer(readline(prompt = "Enter the number of data points: "))
# (Input sequence for x and y vectors)
> print(x)
[1] 1 2 3 4 5
> print(y)
[1] 5 10 15 20 25

plot(x, y, main = "Scatter Plot", xlab = "x", ylab = "y", pch = 19, col = "blue")

Practical No. 11
Aim: Advanced Data Analysis using PivotTables and Pivot Charts  
> salesdata = data.frame(
+   dept = c("science", "commerce", "arts", "science", "commerce", "arts"),
+   month = c("jan", "jan", "jan", "feb", "feb", "feb"),
+   sales = c(5000, 7000, 4000, 6000, 8000, 5000)
+ )
> print(salesdata)

> pivot <- stats::aggregate(sales ~ dept, data = salesdata, FUN = base::sum)
> print(pivot)
      dept sales
1     arts  9000
2 commerce 15000
3  science 11000

> xtabs(sales ~ dept + month, data = salesdata)
          month
dept        feb  jan
  arts     5000 4000
  commerce 8000 7000
  science  6000 5000

> barplot(pivot$sales, names.arg = pivot$dept, 
+         main = "Department wise Total sales", 
+         xlab = "Department", ylab = "Total sales", col = "lightblue")

Practical No. 9
Aim: Create a Dataset and Perform Statistical Analysis in Excel  
Excel Formulas Used:
SUM: =SUM(A2:A7)  
AVERAGE: =AVERAGE(A2:A7)  
MIN: =MIN(A2:A7)  
MAX: =MAX(A2:A7)  
COUNTIF: =COUNTIF(A2:A7, A7)  
COUNTA: =COUNTA(A2:A7)  
IF Function: =IF(B5>=$G$1/2, "pass", "fail")  
NESTED IF: =IF(B3>=75, "DISTINCTION", IF(B3>=60, "FIRST", IF(B3>=40, "PASS", "FAIL")))  
PROPER: =PROPER(D21)  
LOWER: =LOWER(D23)  
CONCAT: =CONCAT(D24, " ", E24)  
UPPER: =UPPER(D24)  
VLOOKUP: =VLOOKUP(101, A36:F41, 4, FALSE)  
HLOOKUP: =HLOOKUP(101, A45:G50, 4, FALSE)  
MATCH / INDEX: =INDEX(A35:F41, 3, 2) & =MATCH("AMIT", B36:B41, 0)  
Practical No. 10A
Aim: Sorting, Filtering, Delimiter, Data Validation  
Sorting: Table sorting based on attendance percentage (low to high or high to low).  
Filtering: Filtering data for students with attendance >= 60%.  
Delimiter: Text-to-Columns wizard usage in Excel for string splitting.  
Data Validation: Restricting input types using Text length / Numeric value range validation rules.  
Practical No. 10B
Aim: Advanced Data Analysis using PivotTables and PivotCharts  
Analysis of Sales Data by Product, Category, and Region using Pivot Tables.  
Creation of Bar Charts and Pie Charts based on Category and Region-wise price summaries.  
