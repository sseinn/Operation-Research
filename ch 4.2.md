# A basic solution has the followting properties

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

