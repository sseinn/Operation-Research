# A basic solution has the following properties

1. Each variable is designated as either a nonbasic variable or a basic variable.

2. The number of **basic variables** equals the the number of functional constraints **(= equations)**.

   Therefore, **the number of nonbasic variables** equals the total of variables minus the number of functional constraints.

3. The nonbasic variables are set equal to zero.

4. The values of the **basic variables** are obtained as the simultaneous solution of the system fo equations(functional constraints in augmented form).

5. (The set of basic variables is often referred to as the basis)

6. If the basic variables satisfy the nonnegativity constraints, the basic solution is **BF solution**.


### Illustrate these definition

- eg. BF solution = (0, 6, 4, 0, 6)

  => x1, x4 = nonbasic variables, so the two variables are set equal to zero.

     The three equations then yield, respectively, x3 = 4, x2 = 6, x5 = 6

     Because all three of these basic variables are **nonnegative**, this basic solution (0, 6, 4, 0, 6) is indeed a BF sloution.


# CPF sloutions are adjacent

Two BF solutions are **adjacent** if all but one of their **nonbasic variables** are the same.

This implies that all but **one of their basic variables are the same**, although perhaps with different numerical values.


Consequently, **moving from the current BF solution to an adjacent one** involves switching one variable from nonbasic to basic and vice versa for one other.

# entering basic variable

At any iteration of the simplex method, the purpose of step 1 is to choose one nonbasic variable to increase from zero (while the values of the basic variables are adjusted to continue satisfying the system of equations). Increasing this nonbasic variable from zero wil convert it to a basic vatiable for the next BF solution. Therefore, this variable is called **entering basic variable** for the current iteration (because it is entering the basis).

# minimun ratio test

These calculations are referred to as the **minimun ratio test**. The objective of this test is to determine which basic variable drops to zero first as the entering basic variable is increased. 

# leaving basic variable

At any iteration of the simplex method, step 2 uses the minimun ratio test to determine which basic variable drops to zero first as the entering basic variable is increased. Decreasing this basic variable o zero will convert it to a nonbasic variable for the nest BF solution. Therefore, this variable is called the **leaving basic variable** for the current iteration (because it is leaving the basis).

# Simplex Method In Tabular Form

When you need to solve a problem by hand (or interactively with your IOR Tutorial), we recommend the tabular form described in this section.

The tabular form of the simplex method recored only the essential information, namely, **(1) the coefficients of the variables**, **(2) the constants on the right-hand sides of the equations**, **(3) the basic variable appearing in each equation**.

# Simplex Method In Tabular Form (and Iteration 1 for the Example)

**Initialization**. Introduce slack variables. Select the **decision variables** to be the **initial nonbasic variables** (set equal to zero) and the **slack variables** to be the **initial basic variables**.


**Optimality Test**. The current BF solution is optimal if and only if every coefficient in row 0 is nonnegative(>=0). If is is, stop; otherwise, go to an iteration to obtain the next BF solution, which involves changing one nonbasic variable to a basic variable (step 1) and vice versa (step 2) and then solving for the new solution (step 3).

**Iteration** Step 1: Determine the entering basic variable by selecting the variable (automatically a nonbasic variable) with the negative coefficient having the largest absolute value(i.e., the "most negative" coefficient) in Eq (0). Put a box around the column below this coefficient, and call this the **pivot column**.

Step 2: Determine the leaving basic variable by applying the minimun ratio test.

**Minimum Ratio Test**

1. Pick out each coefficient in the pivot column that is strictly positive (>0).

2. Divide each of these coefficients into the right side entry for the same row.

3. Identify the row that has the smallest of these ratios.

4. The basic variable for that row is the leaving basic variable, so replace that variable by the entering basic variable in the basic variable column of the next simplex tableau.

Step 3: Solve for the new BF solution by using **elementary row operartions** (multiply or divide a row by a nonzero constant; add or substract a multiple of one row to another row) to construct a new simplex tableau in proper form from Gussian elimination below the current one, and then return to the optimality test. The specifi elementary row operations that need to be performed are listed below.





