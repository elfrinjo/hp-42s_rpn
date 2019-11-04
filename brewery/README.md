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

## GFWtr - Grainfather Water Calculator
Asks for the batchvolume in l (Aussschlahmenge / Asslg) and grainbill in kg (Malz) and 
calculates the amount of mash- and sparge-water for grain bills > 4,5 kg according to
this formula from the Grainfather manual:
```
MashWater = GB * 2.7 + 3.5
SpargeWater = (BV + WL) - MashWater + (GB * 0.8)
```
GB: Grainbill in kg  
BV: Batchvolume in l  
WL: Waterloss in boil & trub in l (defaults to 5)  
Adjust waterloss in line 10

