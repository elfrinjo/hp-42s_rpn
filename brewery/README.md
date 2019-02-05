# Brewery calculations

## SPND - Spundungsdruck
This is a **solver-program** to calculate the carbonization pressure according
to this formula:
```
                                          2617.25
                          (- 10.73797) + ----------
                                         t + 273.15
 c(p, t) := (p + 1.013) %e                          10
```

c: CO₂ concentration in g/l  
p: Carbonization gauge pressure in bar  
ϑ: Temperature in °C  

https://elfring.ms/blog/rpn-karbonisierungsrechner


