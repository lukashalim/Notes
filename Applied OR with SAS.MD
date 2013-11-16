### Chapter 1
Special cases in LP
- Infeasibility
- unboundedness
- redundancy
- alternative optimal solutions

#### Simplex Method
Defintion: Standard form
 - Convert inequalities to equalities by adding slack variables or subtracting surplus variables
  - x <= 3 becomes x + slack = 3
  - x >= 3  becomes x - surplus = 3
 - All variables must be non-negative
Definition: basic solution - the corner points of the solution space.  Solutions to the standard form system of linear equations .
Steps in Simplex Method
2. Determine basic feasible solution using the standard form
3. Determine whether current basic feasible solution is optimal
4. If optimal, stop.  If not optimal, determine which nonbasic variable should become basic, and which basic should become nonbasic
5. Use elementary row operations to find the new basic feasible solution with a better objective function value.  Return to step 2.

Integer Program - IP
Mixed Integer Linear Programmning - MILP
- Starts by solving an IP or MILP problem as though it were a LP problem
- If the LP solution consists of integers, stop.  Otherwise, set upper and lower bounds on solution and repeat

