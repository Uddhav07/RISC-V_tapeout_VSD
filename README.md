# RISC-V Tapeout - STA and Transistor Analysis

## 1. Introduction

### Purpose of Experiments

#### Id vs Vds Characteristics

#### Id vs Vgs Characteristics

#### Voltage Transfer Characteristics (VTC)

#### Transient Analysis

#### Process Variation Analysis

## 2. SPICE Netlists

### Id vs Vds Netlist

```spice

```

### Id vs Vgs Netlist

```spice

```

### VTC Netlist

```spice

```

### Transient Analysis Netlist

```spice

```

### Variation Analysis Netlist

```spice

```

## 3. Results

### Id vs Vds Characteristics

#### Plots

#### Analysis

### Id vs Vgs Characteristics

#### Plots

#### Threshold Voltage Extraction

### Voltage Transfer Characteristics

#### Plots

#### Switching Point Analysis

#### Noise Margins

### Transient Analysis

#### Waveforms

#### Propagation Delays

### Process Variation Effects

#### VTC Under Variation

#### Parameter Shifts

## 4. Summary Tables

### Extracted Parameters

| Parameter | Value | Units |
|-----------|-------|-------|
| Threshold Voltage (Vth) | | V |
| Switching Point (VM) | | V |
| NM_L | | V |
| NM_H | | V |
| Rise Delay (tpdr) | | ns |
| Fall Delay (tpdf) | | ns |

### Variation Impact

| Corner | Switching Point | NM_L | NM_H | Delay |
|--------|----------------|------|------|-------|
| TT | | | | |
| FF | | | | |
| SS | | | | |

## 5. Device Physics Observations

### Saturation Behavior

### Threshold Shifts

### Temperature Effects

### Supply Voltage Impact

## 6. STA Implications

### Delay Models

### Timing Margins

### Critical Path Analysis

### Variation Impact on Timing

## 7. Conclusions

### Transistor-Level Constraints

### Variation Effects

### Design Margins

## 8. References
