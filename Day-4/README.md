# NgspiceSky130 - Day 4 - CMOS Noise Margin robustness evaluation

## Static behavior evaluation – CMOS inverter robustness – Noise margin

### L1: Introduction to noise margin

ideally slope = infinte
reality slope = finite
![alt text](image.png)

---

### L2: Noise margin voltage parameters

![alt text](image-1.png)

0 < Vil < Vol < Vih < Voh

---

### L3: Noise margin equation and summary

Noise margin High = Voh - Vih

Noise margin Low = Vil - Vol

![alt text](image-2.png)

![alt text](image-3.png)

---

### L4: Noise margin variation with respect to PMOS width

![alt text](image-4.png)

![alt text](image-5.png)

---

### L5: Sky130 Noise margin labs

![alt text](image-6.png)

```ngspice
x0 = 0.758197, y0 = 1.72727

x0 = 0.967213, y0 = 0.131818
```

Voh = 1.72727
Vil = 0.758197

Vol = 0.131818
Vih = 0.967213

NMh = 1.72727 - 0.967213 = 0.760057
NMl = 0.758197 - 0.131818 = 0.626379

---
