# Circuit design and SPICE simulations

## Circuit Design

## SPICE simulations

![alt text](image.png)

![alt text](image-5.png)

![alt text](image-6.png)

![alt text](image-7.png)

Source of these tables: 

Are these models actually accurate: match with spice.

How to verify STA is correct?

![alt text](image-8.png)

Vbs can tune Vth

### Threshold Voltage

![alt text](image-10.png)

![alt text](image-11.png)

#### futher Vgs increased

1. channel width increases
2. depletion region width unchanged
3. e- from n+ move to region under gate
4. Continuous n-channel formation from S-D, whose conductivity is modulated by 'Vgs'

#### Vsb = +ve

1. RB between S and B
2. depletion width increases in this area.

![alt text](image-12.png)

![alt text](image-16.png)

## Resistive region of operation 

### with small drain-source voltage

![alt text](image-17.png) 

![alt text](image-18.png)

### Drift current theory

volate gradient due to Vds

![alt text](image-19.png)

![alt text](image-20.png)

![alt text](image-21.png)

Id = vel. of charge carriers * available charge

![alt text](image-22.png)

### Drain current model for linear region of operation

![alt text](image-23.png)

![alt text](image-24.png)

if Vds <=Vgs-Vt 
linear region since Vds ^2 is ignored

### SPICE conclusion to resistive operation

![alt text](image-25.png)

![alt text](image-26.png)

### Pinch-off region condition

![alt text](image-27.png)

: pinch off phenomenon started, channel partly dissapears due to Vds

further Vds increasing, saturation region

![alt text](image-28.png)

### Drain current model for saturation region of operation

![alt text](image-29.png)

![alt text](image-30.png)

## SPICE 

### Basic SPICE setup

derive waveforms.   
accurate delays.    

feeds the models correctly to spice engine. 

![alt text](image-31.png)

![alt text](image-32.png)

### Circuit description in SPICE syntax

![alt text](image-33.png)

-> define nodes, Mxx D G S B name W L        
![alt text](image-34.png)

![alt text](image-35.png)

### Define technology parameters

1. get model file for "nmos", it will have its own models.  
2. model parameters like Vto, gamma, Cox, Kn, lambda.  
3. these model param come as a package. 

![alt text](image-36.png)
![alt text](image-40.png)
![alt text](image-42.png)

### First SPICE simulation

```bash
git clone https://github.com/kunalg123/sky130CircuitDesignWorkshop.git
cd sky130CircuitDesignWorkshop/design/sky130_fd_pr/cells/nfet_01v8/
less sky130_fd_pr__nfet_01v8__tt.pm3.spice
less sky130_fd_pr__nfet_01v8__tt.corner.spice
```

W and L to be in one of these values only for simulation.   

```bash
cd ../../models
less sky130.lib.spice
```

![alt text](image-43.png)

```bash
cd ../..
```

for different corners, tt,sf, ff/       

```bash
ngspice day1_nfet_idvds_L2_W5.spice
```

```ngspice
plot -vdd#branch
```

![alt text](image-44.png)



