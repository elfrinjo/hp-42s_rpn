# SPLIT - Split expenditures among people
Several people of a group had different expenses.
The expenditures shall be shared among the whole group.

## Usage
* Create a 1xN matrix where N is the number of people.
* Enter the expenses into the matrix.
* Execute this program.
* Z will conatin the sum.
* Y will contain amount per person.
* X will contain a matrix with the compensation cashflow.

## Annotation
```
LBL "SPLIT"
STO "m"
RSUM        ─┐ Store the sum of the whole row
DET          │ It is returned as a 1x1 matrix, the DET will be a scalar
STO 01      ─┘
RCL "m"
DIM?           The X-DIM of the matrix is the number of elements, DIM? returns into X, Y
RCL 01      ─┐
X<>Y         │ Sum / number = amount per person
÷           ─┘
STO 02         Store the amount per person
RCL 01         RCL the Sum to have it in Z later on
X<>Y           Get the amount per person back into X (Could also be RCL 02)
RCL "m"     ─┐
X<>Y         │ Matrix - amount p.p. = matrix with comp. cashflow
-           ─┘
RCL 02      ─┐ Put the amount p.p. into Y
X<>Y        ─┘
END
```
