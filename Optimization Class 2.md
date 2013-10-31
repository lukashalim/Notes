Choice of dual simplex vs Primal simplex - SAS will choose method during presolver

Allocation Models
- Maximize objective functio with respect to less than constraints
 - profit maximization
- Example: Maximizing revenue from prodcution
 - Decision variables - Number of chairs, desks, tables
- Constraints are put into matrix
 - In order to turn an inequality matrix to an equality, we add slack variables.  For example, x + y <= n can become x + y + slack = n with positive slack variable.
 - the difficulty in solving the matrix explains why we use the simplex algorithm
- Adding constraints can never improve results.  Either stays the same or gets worse.  Obviously.

- Shadow price - what will be the improvement in the objective function when the value of the objective function increases by 1.

 
