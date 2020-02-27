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

  <center><img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20x%28t%29%20%3D%20x%28t&plus;T%29"></center>

- for discrete-time
  <center><img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20x%5Bn%5D%3Dx%5Bn&plus;N%5D"></center>

### determinate and random signals

- **a determinate signal**: _x(t)_

- a random signal: cannot find a function to represent it

        E.g.: noise, speech

### energy and power signals

- energy signals <img src = "https://latex.codecogs.com/svg.latex?%5Cinline%200%3CE%3C%5Cinfty%2C%5C%3BP%5Cto0">

<center><img src = "/assets/Ch_1_figure_6.png"></center>

- power signals <img src="https://latex.codecogs.com/svg.latex?%5Cinline%200%3CP%3C%5Cinfty%2C%5C%3BE%5Cto%5Cinfty">

<center><img src="/assets/Ch_1_figure_7.png"></center>

- signals with neither finite E nor finite P <img src = "https://latex.codecogs.com/svg.latex?%5Cinline%20E%5Cto%5Cinfty%2C%5C%3BP%5Cto%5Cinfty">

<center><img height = 200 src = "/assets/Ch_1_figure_8.png"></center>

## Transformations of the Independent Variable of Signals

- time shift

<center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28t-t_0%29"></center>

- time reversal _(left +, right -)_

<center><img src="https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28-t%29"></center>

- time scaling

<center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%5Cto%20x%28k_0t%29">

**First Scaling, Second Shift**

**先尺缩，再平移**</center>

## Some Useful Signal Modes

1. Real Exponential Signals

<center><img src="https://latex.codecogs.com/svg.latex?x%28t%29%20%3D%20Ce%5E%7Bat%7D">

<img src = "/assets/Ch_1_figure_9.png"></center>

2. Periodic Complex Exponential and Sinusoidal Signals

<center><img src = "https://latex.codecogs.com/svg.latex?x%28t%29%20%3D%20Ce%5E%7Bj%5Comega_0t%7D"></center>

3. General Complex Exponential Signals

<center><img src = "https://latex.codecogs.com/svg.latex?%5C%5CC%20%3D%20%7CC%7Ce%5E%7Bj%5Ctheta%7D%2C%5C%3Ba%3Dr&plus;j%5Comega_0%5Cvspace%7B3ex%7D%20%5C%5CCe%5E%7Bat%7D%3D%7CC%7Ce%5E%7Bj%5Ctheta%7De%5E%7B%28r&plus;j%5Comega_0%29t%7D%3D%7CC%7Ce%5E%7Brt%7De%5E%7Bj%28%5Comega_0t&plus;%5Ctheta%29%7D%5Cvspace%7B3ex%7D%20%5C%5CCe%5E%7Bat%7D%3D%20%7CC%7Ce%5E%7Brt%7D%28%5Ccos%7B%28%5Comega_0t&plus;%5Ctheta%29%7D&plus;j%5Csin%7B%28%5Comega_0t&plus;%5Ctheta%29%7D%29"></center>

- When r=0, both parts are sinusoidal; 
- When r>0, both parts are growing sinusoidal;
- When r<0, both parts are decaying sinusoidal (damped sinusoids).

4. Sampling Signals

<center><img src = "https://latex.codecogs.com/svg.latex?Sa%28t%29%20%3D%20%5Cfrac%7B%5Csin%7Bt%7D%7D%7Bt%7D">

<img src = "https://www5a.wolframalpha.com/Calculate/MSP/MSP25731aggid5g7g1463ad000066e36f1193idbhha?MSPStoreType=image/gif&s=28"></center>

## The Unit Impulse and Unit Step Functions

- Unit Step Function

<center><img src = "/assets/Ch_1_figure_10.png"></center>

- Unit Impulse Function

<center><img src = "/assets/Ch_1_figure_11.png"></center>

1. **Sampling Property**

<center><img src = "/assets/Ch_1_figure_12.png"></center>

2. Even Function

<center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%28t%29%3D%5Cdelta%28-t%29"></center>

3. Time Scaling

<center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%28kt%29%3D%5Cfrac%7B1%7D%7B%7Ck%7C%7D%5Cdelta%28t%29"></center>

4. **Relationship to Unit Step Function**

<center><img src = "https://latex.codecogs.com/svg.latex?u%28t%29%3D%5Cint_%7B-%5Cinfty%7D%5E%7Bt%7D%7B%5Cdelta%28%5Ctau%29%5Cmathrm%7Bd%7D%5Ctau%7D%20%5Cquad%20%5Cdelta%28t%29%3D%5Cfrac%7B%5Cmathrm%7Bd%7Du%28t%29%7D%7B%5Cmathrm%7Bd%7Dt%7D"></center>

- Impulse Doublet Signal 

<center><img src = "/assets/Ch_1_figure_13.png"></center>

1. **Sampling Property**

<center><img src = "https://latex.codecogs.com/svg.latex?%5C%5Cx%28t%29%20%3D%20%5Cdelta%27%28t-t_0%29%3Dx%28t_0%29%5Cdelta%27%28t-t_0%29-x%27%28t_0%29%5Cdelta%28t-t_0%29%5Cvspace%7B3ex%7D%20%5C%5C%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7Dx%28t_0%29%5Cdelta%27%28t-t_0%29%5Cmathrm%7Bd%7Dt%3D-x%27%28t_0%29"></center>

2. Scaling

<center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%27%28kt%29%3D%5Cfrac%7B1%7D%7Bk%7Ck%7C%7D%5Cdelta%27%28t%29%2C%5C%3Bk%5Cneq0"></center>

3. Odd Function

<center><img src = "https://latex.codecogs.com/svg.latex?%5Cdelta%27%28t%29%3D-%5Cdelta%27%28-t%29"></center>

## Signal Decompositions and Components of a Signal

### Even and Odd Components


<center><img height = 200 src = "/assets/Ch_1_figure_14.png"></center>

### Real and Imaginary Components

<center><img height = 200 src = "/assets/Ch_1_figure_15.png"></center>

