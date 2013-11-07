### Data Envelopment Analysis (DEA)
- special case of linear programming
- Comparative technique
 - use weights to solve optimization problems for a particular case.  
 - Then see whether other cases are more efficient using those weights.
 - 100% efficient is input = output

### Integer Linear Programming
- Sometimes rounding is sufficient since you may round to an infeasible solution
- rounding away from the optimum solution may mean you can add more of another output
- However, *breach and bound* is the most typical method for finding optimal solution
 - breach step creates subproblems
- in optmodel just add "integer" in the var statement

### Binary Choice Models
