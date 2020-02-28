# CH_1

## signals

### communication system

a function conveys information about the behavior or attributes of some phenomenon

### physical world

quantity exhibiting variation in time or variation in space

**signals are mathematical functions**

- Independent variable = time

- Dependent variable = voltage, flow rate, sound pressure, ...

**signals can be represented by graph**

<div align = center><img src ="/assets/Ch_1_figure_1.png"></div>
## classifications of signals

### continuous-time and discrete-time signals

- continuous-time signals' independent variable is continuous

<div align=center><img src="https://latex.codecogs.com/svg.latex?x%28t%29%20%3D%20e%5Et"/></div>
- discrete-time signals are defined only at discrete times:

<div align=center><img src="https://latex.codecogs.com/svg.latex?x%5Bn%5D%20%3D%202%5En"/></div>
![Ch_1_figure_2](assets/Ch_1_figure_2.png)

- the independent variable is inherently discrete

![Ch_1_figure_3](assets/Ch_1_figure_3.png)

- sampling of continuous-time signals

![Ch_1_figure_4](assets/Ch_1_figure_4.png)

### analog and digital signals

- analog signals: continuous in both time and amplitude
- digital signals: discrete in both time and amplitude

![Ch_1_figure_5](assets/Ch_1_figure_5.png)

### periodic and aperiodic signals

- for continuous-time

  <div align = center><img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20x%28t%29%20%3D%20x%28t&plus;T%29"></div>

- for discrete-time
  
  <center><img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20x%5Bn%5D%3Dx%5Bn&plus;N%5D"></div>

### determinate and random signals

- **a determinate signal**: _x(t)_

- a random signal: cannot find a function to represent it

        E.g.: noise, speech

### energy and power signals

- energy signals <img src = "https://latex.codecogs.com/svg.latex?%5Cinline%200%3CE%3C%5Cinfty%2C%5C%3BP%5Cto0">

<div align=center><img src = "/assets/Ch_1_figure_6.png"></div>
- power signals <img src="https://latex.codecogs.com/svg.latex?%5Cinline%200%3CP%3C%5Cinfty%2C%5C%3BE%5Cto%5Cinfty">

<div align=center><img src="/assets/Ch_1_figure_7.png"></div>
- signals with neither finite E nor finite P <img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20E%5Cto%5Cinfty%2C%5C%3BP%5Cto%5Cinfty">

<div align = center><img height = 200 src = "/assets/Ch_1_figure_8.png"></div>
## Transformations of the Independent Variable of Signals

- time shift

<div align = center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28t-t_0%29"></div>
- time reversal _(left +, right -)_

<div align = center><img src="https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28-t%29"></div>
- time scaling

<div align = center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28k_0t%29">

**First Scaling, Second Shift**

**先尺缩，再平移**</div>

## Some Useful Signal Modes

1. Real Exponential Signals

<div align = center><img src="https://latex.codecogs.com/svg.latex?x%28t%29%20%3D%20Ce%5E%7Bat%7D">

<img src = "/assets/Ch_1_figure_9.png"></div>

2. Periodic Complex Exponential and Sinusoidal Signals

<div align = center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%3D%20Ce%5E%7Bj%5Comega_0t%7D"></div>
3. General Complex Exponential Signals

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5C%5CC%20%3D%20%7CC%7Ce%5E%7Bj%5Ctheta%7D%2C%5C%3Ba%3Dr&plus;j%5Comega_0%5Cvspace%7B3ex%7D%20%5C%5CCe%5E%7Bat%7D%3D%7CC%7Ce%5E%7Bj%5Ctheta%7De%5E%7B%28r&plus;j%5Comega_0%29t%7D%3D%7CC%7Ce%5E%7Brt%7De%5E%7Bj%28%5Comega_0t&plus;%5Ctheta%29%7D%5Cvspace%7B3ex%7D%20%5C%5CCe%5E%7Bat%7D%3D%20%7CC%7Ce%5E%7Brt%7D%28%5Ccos%7B%28%5Comega_0t&plus;%5Ctheta%29%7D&plus;j%5Csin%7B%28%5Comega_0t&plus;%5Ctheta%29%7D%29"></div>
- When r=0, both parts are sinusoidal;
- When r>0, both parts are growing sinusoidal;
- When r<0, both parts are decaying sinusoidal (damped sinusoids).

4. Sampling Signals

<div align = center>
<img src = "https://latex.codecogs.com/svg.latex?Sa%28t%29%20%3D%20%5Cfrac%7B%5Csin%7Bt%7D%7D%7Bt%7D">

<img src = "/assets/Ch_1_figure_16.png"></div>

## The Unit Impulse and Unit Step Functions

- Unit Step Function

<div align = center><img src = "/assets/Ch_1_figure_10.png"></div>
- Unit Impulse Function

<div align = center><img src = "/assets/Ch_1_figure_11.png"></div>
1. **Sampling Property**

<div align = center><img src = "/assets/Ch_1_figure_12.png"></div>
2. Even Function

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%28t%29%3D%5Cdelta%28-t%29"></div>
3. Time Scaling

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%28kt%29%3D%5Cfrac%7B1%7D%7B%7Ck%7C%7D%5Cdelta%28t%29"></div>
4. **Relationship to Unit Step Function**

<div align = center><img src = "https://latex.codecogs.com/svg.latex?u%28t%29%3D%5Cint_%7B-%5Cinfty%7D%5E%7Bt%7D%7B%5Cdelta%28%5Ctau%29%5Cmathrm%7Bd%7D%5Ctau%7D%20%5Cquad%20%5Cdelta%28t%29%3D%5Cfrac%7B%5Cmathrm%7Bd%7Du%28t%29%7D%7B%5Cmathrm%7Bd%7Dt%7D"></div>
- Impulse Doublet Signal

<div align = center><img src = "/assets/Ch_1_figure_13.png"></div>
1. **Sampling Property**

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5C%5Cx%28t%29%20%3D%20%5Cdelta%27%28t-t_0%29%3Dx%28t_0%29%5Cdelta%27%28t-t_0%29-x%27%28t_0%29%5Cdelta%28t-t_0%29%5Cvspace%7B3ex%7D%20%5C%5C%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7Dx%28t_0%29%5Cdelta%27%28t-t_0%29%5Cmathrm%7Bd%7Dt%3D-x%27%28t_0%29"></div>
2. Scaling

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%27%28kt%29%3D%5Cfrac%7B1%7D%7Bk%7Ck%7C%7D%5Cdelta%27%28t%29%2C%5C%3Bk%5Cneq0"></div>
3. Odd Function

<div align = center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%27%28t%29%3D-%5Cdelta%27%28-t%29"></div>
## Signal Decompositions and Components of a Signal

### Even and Odd Components

<div align = center><img height = 200 src = "/assets/Ch_1_figure_14.png"></div>
### Real and Imaginary Components

<div align = center><img height = 200 src = "/assets/Ch_1_figure_15.png"></div>
## Systems

a process in which **input signals** are transformed by the system or cause the system to respond in some way, resulting in other signals as **outputs**

### Descriptions

- input and output description
  N-order linear differential equation
- state-space description
  N first-order differential equations

### Interconnections

- series interconnection
  
  <div align = center><img src = "/assets/Ch_1_figure_17.png"></div>
- parallel interconnection
  
  <div align = center><img src = "/assets/Ch_1_figure_18.png"></div>
- feedback connection
  
  <div align = center><img src = "/assets/Ch_1_figure_19.png"></div>
- complicated connection which combine the former two interconnections
  
  <div align = center><img src = "/assets/Ch_1_figure_20.png"></div>

## Basic System Properties

### Linearity

- additivity

<div align = center><img height = 100 src ="/assets/Ch_1_figure_21.png"></div>
- homogeneity

<div align = center><img height = 80 src = "/assets/Ch_1_figure_22.png"></div>
<div align = center><img  src = "/assets/Ch_1_figure_23.png"></div>
### Time-Invariant

<div align = center><img height = 120 src = "/assets/Ch_1_figure_24.png">

<img height = 200 src = "/assets/Ch_1_figure_25.png"></div>

### With Memory

- memoryless

  its output for each value of the independent variable at a given time is dependent **only on the input at that same time**

- system with memory

  it **retains or stores information** about input values at time other than the current time
  _E.g.: Accumulator, Delay;_

### Causality

- casual system

  output depends **only on the input at present time** and in the past

  _All memoryless systems are casual systems_

- non-casual system
  _E.g.: Data Smoothing_

### Invertibility

distinct input lead to distinct output

<div align = center><img src = "/assets/Ch_1_figure_26.png"></div>
### Stability

if the input to a stable system is bounded, then the output must also be bounded

<div align = center><img src = "/assets/Ch_1_figure_27.png"></div>
