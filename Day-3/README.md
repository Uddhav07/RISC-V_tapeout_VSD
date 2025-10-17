# NgspiceSky130 - Day 3 - CMOS Switching threshold and dynamic simulations

## Voltage transfer characteristics – SPICE simulations

### L1: SPICE deck creation for CMOS inverter

ideally pmos size should be 3x the nmos  
assume output load = 10fF   
Vin = 2.5V since pmos has L of 0.25u    

![alt text](image.png)  

---

### L2: SPICE simulation for CMOS inverter

+ve terminal first in Voltage
![alt text](image-2.png)

W/L ratio of pmos slightly > than nmos  

SPICE waveform : Wn=Wp=0.375u, Ln,p=0.25u device
                (Wn/Ln=Wp/Lp = 1.5)

```ngspice
source *****.cir
setplot
dc1
display
plot out vs in
```

![alt text](image-1.png)
slightly left

SPICE waveform : Wn=0.375u, Wp=0.9375u, Ln,p=0.25u device
                (Wn/Ln=1.5, Wp/Lp = 3.75)

![alt text](image-3.png)

```ngspice
dc2
display
plot out vs in
```

![alt text](image-4.png)

---

### L3: Labs Sky130 SPICE simulation for CMOS

![alt text](image-5.png)

![alt text](image-6.png)

![alt text](image-7.png)

![alt text](image-8.png)

```rise
x0 = 2.48207e-09, y0 = 0.900003

x0 = 2.14966e-09, y0 = 0.9
```

trise = 0.33241 ns

```fall
x0 = 4.33425e-09, y0 = 0.900001

x0 = 4.05028e-09, y0 = 0.900001
```

tfall = 0.28397 ns

---

## Static behavior evaluation – CMOS inverter robustness – Switching Threshold

### L1: Switching Threshold, Vm

both the waveforms are same in shape.   
therefore, the cmos is a robust device. 
char is maintaned across, which is why its widely used. 

![alt text](image-11.png)

![alt text](image-12.png)

---

### L2: Analytical expression of Vm as a function of (W/L)p and (W/L)n

Vm is completely dependent on Idsp and Idsn 

1. from w/l to Vm
2. from Vm to w/l

ignoring lambda

Idsp + idsn = 0 

![alt text](image-13.png)

evaluating idsn + idsp = 0

![alt text](image-14.png)

---

### L3: Analytical expression of (W/L)p and (W/L)n as a function of Vm

![alt text](image-15.png) 
![alt text](image-17.png)
![alt text](image-18.png)
also calc the delays for dynamic behaviour
![alt text](image-19.png)

---

### L4: Static and dynamic simulation of CMOS inverter

dc transfer char. : Vm  

![alt text](image-22.png)

```ngspice
source .cir
setplot
tran2
display
plot out vs time in
```

![alt text](image-23.png)

---

### L5: Static and dynamic simulation of CMOS inverter with increased PMOS width

![alt text](image-25.png)

![alt text](image-26.png)

![alt text](image-27.png)

![alt text](image-28.png)

---

### L6: Applications of CMOS inverter in clock network and STA

- increasing the size of pmos has small range in change of Vm  
- for higher sizes the range decreases further.
- for a case rise and fall delay is approx equal.

![alt text](image-29.png)

diff rise timmes ---> diff low to high. 

Rpmos = 2.5 Rnmos {approx}

![alt text](image-30.png)

equal pmos and nmos:

- preffered for data path.
- combinational of diff rise time sizes useful for in the end a set rise time.

---
