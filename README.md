# Online_Sales
# 😊OnlineSales_Assignent...


/*   Task-1 SQL solution :-   */ 
SELECT DEPT_NAME, AVG(MONTHLY_SALARY) AS AVG_MONTHLY_SALARY
FROM employees
GROUP BY DEPT_NAME
ORDER BY AVG_MONTHLY_SALARY DESC
LIMIT 3;


/*   Task-2 Scripting solution :-    */
import pandas as pd
import pandas as pd
departments = pd.read_csv("C:/OnlineSales/ASDE Assignment - Departments.csv")  //we are jsut importing the daparment//
                                                                               // table from the files as copying the path// 

employees = pd.read_csv("C:/OnlineSales/ASDE Assignment - Employees.csv")  //we are jsut importing the employees //
                                                                            table from the files as copying the path//

salaries = pd.read_csv("C:/OnlineSales/ASDE Assignment - Salaries.csv")  //we are jsut importing the salaries table//
                                                                          // from the files as copying the path////

df=pd.range(departments , employees, left_on='ID' , right_on='DEPT_ID') //here we are merging the department column_ID as left//
                                                                        //column and column_ID of employees as right column.//

x=pd.merge(df,salaries , left_on='ID_y' , right_on='EMP_ID') //here again merging the the tables,above//
                                                             //merged table's l wiht the salaries table//

x=data.groupby('[NAME_X]')['AMT'].mean()  //This line performs grouping and calculates the mean of the 'AMT' column for each unique//
                                         // value in the [NAME_X] column of the data DataFrame. The result is stored in the x variable.//

x.sort_values(ascending=False).head(3) // this sorts the values in the x Series in descending order (ascending=False)/
                                       //and then retrieves the top 3 values using the head(3) method.//       

x //refers to a Pandas Series or DataFrame column that contains data.//

/*    TaskDebugging-3    */

1. If n is less than 10: Calculate its Square
  /*soluiton*/
def compute(n):
    if n < 10:
        out = n ** 2
    elif n < 20:
        out = 1
        for i in range(1, n-9):  //here is the correction we have to write n-9 instead of n-10. This ensures that the 
                        //loop runs for n-9 iterations, multiplying the numbers from 1 to n-9 to calculate the factorial.
          out *= i                
    else:
        lim = n - 20
        out = lim * lim
        out = out - lim
        out = out / 2 
    print(out)

# Example usage
compute(4)
output will be 16 that is the square of 4.


2.If n is between 10 and 20: Calculate the factorial of (n-10)
  */solution*/
def compute(n):
    if n < 10:
        out = n ** 2
    elif n < 20:
        out = 1
        for i in range(1, n-9):
            out *= i
    else:
        out = 1
        for i in range(1, n-9):
            out *= i
    print(out)

# Example usage
compute(15)
output of this code will be the 120. because 15-10 = 5 whose factorial will be the 5*4*3*2*1 =120;


3.If n is greater than 20: Calculate the sum of all integers between 1 and (n-20)
/*solution*/
def compute(n):
    if n < 10:
        out = n ** 2
    elif n < 20:
        out = 1
        for i in range(1, n-9):
            out *= i
    else:
        out = sum(range(1, n-19))  // here i write n-19 instead of n-9 because we have 
                                   //subtract the 20 from thhe number if the number is > 20   
                                    //and addup the integers
    print(out)

# Example usage
compute(25)
output of this will be 15 because 25-20=5 , which is 5+4+3+2+1.

<!-----------------------------------------------------------------Thanks------------------------------------------------------------------>



