# Statistics Tools

## SnCk
Sum of combinations.  
The usual nCk function returns the number of combinations for k elements out of n.
This program sums up the combinations for 1 .. k out of n.

```
      k
     ====
     \          1
  n!  >    -----------
     /     k! (n - k)!
     ====
      k = 1
```
