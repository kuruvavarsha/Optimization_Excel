# Schedule Optimization using Excel 
First, we define the shifts as below:
Each shift lasts a period of 4 hours for a part time employee.
Each shift lasts a period of 7 hours for a full-time employee with a break of 1 hour in between.
Considering the way shifts have been designed:
A full-time employee can only start his/her/their shift at 9 am / 10 am / 11 am 
Whereas there are 7 different shifts where a part time employee can start working
i = {1,2,3,4,5,6,7} 		: 	

i represents the number of shifts

Parameters:
Cp: Cost of wages per employee per hour for a part time employee
Cf: Cost of wages per employee per hour for a full-time employee
Mi: Maximum number of employees that can work on any given day.
Hp: Number of hours worked per day for a part-time employee.
Hf: Number of hours worked per day for a full-time employee.

Decision Variables:
Xi = Number of full-time employees starting to work in each shift; i = number of shifts {1, 2…7}
Yj = Number of part time employees starting to work in each shift; j = number of shifts {1, 2…7}

Objective Function:
![image](https://github.com/kuruvavarsha/Optimization_Excel/assets/143559502/534abf7e-2499-4ede-b0a1-382763ed7704)
 

Table 1: Minimum and Maximum required employees for each shift
![image](https://github.com/kuruvavarsha/Optimization_Excel/assets/143559502/6d7776ab-100d-475e-82f0-977c09d7eea1)



Table 2: Staff schedules per shift
	
![image](https://github.com/kuruvavarsha/Optimization_Excel/assets/143559502/20e5f64f-4a4f-48ff-a650-39ecf8296a42)

Constraints:
1. The number of employees assigned to each shift must be more than the minimum required employees for that shift
X1 + Y1 ≥2
X1 + X2 + Y1 + Y2 ≥2
X1 + X2 + X3 + Y1 + Y2 + Y3≥2
X1 + X2 + X3 + Y1 + Y2 + Y3 + Y4 ≥3
X2 + X3 + Y2 + Y3 + Y4 + Y5≥3
X1 + X3 + Y3 + Y4 + Y5 + Y6≥2
X1 + X2 + Y4 + Y5 + Y6 + Y7 ≥2
X1 + X2 + X3 + Y5 + Y6 + Y7≥2
X2 + X3 + Y6 + Y7≥2
X3 + Y7≥1



2. The number of employees assigned to each shift must be less than the maximum required employees for that shift:
X1  ≥3
X1 + X2  ≥4
X1 + X2 + X3 ≥5
X1 + X2 + X3 + Y1+Y2+Y3+Y4 ≥6
X2 + X3 + Y2 + Y3 + Y4 + Y5 ≥5
X1 + X3 + Y3 + Y4 + Y5 + Y6≥4
X1 + X2 + Y4 + Y5 + Y6 + Y7≥3
X1 + X2 + X3 + Y5 + Y6 + Y7≥4
	X2 + X3 + Y6 + Y7≥3
X3 + Y7≥2

		
3.Maximum number of part time and full time employees to work in a day
∑Xi <= 7, i = {1, 2…,4}
∑Yj <= 4, j = {1, 2…,7}

4.Maximum number of employees that can work in a single day
∑ (Xi + Yj) <= 10, i = {1, 2…,4} and j = {1, 2…,7}

     5. Minimum Number of Full-time employees per day 
∑Xi <= 2, i = {1, 2,3}

	
     6. The decision variables must be integers and greater than or equal to zero
		Xi ≥0  and integer
		Yj ≥0  and integer
		i = {1, 2…,4} and j = {1, 2…,7}
Computational Results:
In this section, we employed multiple simulations to determine the optimal solution for staff scheduling at Starbucks. 
By manipulating the constraints and the objective function, we conducted a sensitivity analysis to identify changes in the minimum cost incurred by the outlet.

 ![image](https://github.com/kuruvavarsha/Optimization_Excel/assets/143559502/76240c04-0801-4e47-a13e-52db25b959ab)

