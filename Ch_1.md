# CH_1

## 1.1 Signals

### communication system

a function conveys information about the behavior or attributes of some phenomenon

### physical world

quantity exhibiting variation in time or variation in space

**signals are mathematical functions**

- Independent variable = time

- Dependent variable = voltage, flow rate, sound pressure, ...

**signals can be represented by graph**

<div align = center><img src ="./assets/Ch_1_figure_1.png"></div>

## 1.2 Classifications of Signals

### continuous-time and discrete-time signals

- continuous-time signals' independent variable is continuous

$$
x(t)=e^t
$$

- discrete-time signals are defined only at discrete times:

$$
x[n]=2^n
$$

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

$$
x(t)=x(t+T)
$$

- for discrete-time

$$
x[n]=x[n+N]
$$

### determinate and random signals

- **a determinate signal**: _x(t)_

- a random signal: cannot find a function to represent it

        E.g.: noise, speech

### energy and power signals

- energy signals $0<E<\infty$, $P\to 0$

<div align=center><img src = "./assets/Ch_1_figure_6.png"></div>

- power signals $0<P<\infty$, $E\to\infty$

<div align=center><img src="./assets/Ch_1_figure_7.png"></div>

- signals with neither finite E nor finite P $E\to\infty$, $P\to \infty$

<div align = center><img height = 200 src = "./assets/Ch_1_figure_8.png"></div>

## 1.3 Transformations of the Independent Variable of Signals

### time shift

$$
x(t)\to x(t-t_0)
$$

### time reversal _(left +, right -)_

$$
x(t)\to x(-t)
$$

### time scaling

$$
x(t)\to x(k_0t)
$$


**First Scaling, Second Shift**

**先尺缩，再平移**

## 1.4 Some Useful Signal Modes

### Real Exponential Signals

$$
x(t)=Ce^{at}
$$

<div align = center><img src = "./assets/Ch_1_figure_9.png"></div>

### Periodic Complex Exponential and Sinusoidal Signals

$$
x(t)=Ce^{j\omega_0t}
$$

### General Complex Exponential Signals

$$
\begin{aligned}
  C&=|C|e^{j\theta},\;a=r+j\omega_0\\[2ex]
  Ce^{at}&=|C|e^{j\theta}e^{(r+j\omega_0)t}=|C|e^{rt}e^{j(\omega_0t+\theta)}\\[2ex]
  Ce^{at}&=|C|e^{rt}(\cos(\omega_0t+\theta)+j\sin(\omega_0t+\theta))
\end{aligned}
$$

- When r = 0, both parts are sinusoidal;
- When r > 0, both parts are growing sinusoidal;
- When r < 0, both parts are decaying sinusoidal (damped sinusoids).

### Sampling Signals


$$
Sa(t)=\frac{\sin{t}}{t}
$$
<div align = center>
<img src = "./assets/Ch_1_figure_16.png"></div>

## 1.5 The Unit Impulse and Unit Step Functions

### Unit Step Function

<div align = center><img height =150 src = "./assets/Ch_1_figure_10.png"></div>

### Unit Impulse Function

<div align = center><img height = 360 width = 600 src = "./assets/Ch_1_figure_11.png"></div>

1. **Sampling Property**

<div align = center><img height = 200 src = "./assets/Ch_1_figure_12.png"></div>

2. Even Function

$$
\delta(t)=\delta(-t)
$$

3. Time Scaling

$$
\delta(kt)=\frac{1}{|k|}\delta(t)
$$

4. **Relationship to Unit Step Function**

$$
\begin{aligned}
  u(t)&=\int_{-\infty}^{t}{\delta(\tau)\mathrm{d}\tau}\\[2ex]
  \delta(t)&=\frac{\mathrm{d}u(t)}{\mathrm{d}t}
\end{aligned}
$$


### Impulse Doublet Signal

<div align = center><img height = 200 src = "./assets/Ch_1_figure_13.png"></div>

1. **Sampling Property**
$$
\begin{aligned}
x(t)=\delta'(t-t_0)&=x(t_0)\delta'(t-t_0)-x'(t_0)\delta(t-t_0)\\[2ex]
\int_{-\infty}^{\infty}{x(t_0)\delta'(t-t_0)\mathrm{d}t}&=-x'(t_0)
\end{aligned}
$$

2. Scaling


$$
\delta'(kt)=\frac{1}{k|k|}\delta'(t),k\neq0
$$

3. Odd Function

$$
\delta'(t)=-\delta'(-t)
$$

## 1.6 Signal Decompositions and Components of a Signal

### Even and Odd Components

<div align = center><img height = 200 src = "./assets/Ch_1_figure_14.png"></div>

### Real and Imaginary Components

<div align = center><img height = 200 src = "./assets/Ch_1_figure_15.png"></div>

## 1.7 Systems

a process in which **input signals** are transformed by the system or cause the system to respond in some way, resulting in other signals as **outputs**

### Descriptions

- input and output description
  N-order linear differential equation
- state-space description
  N first-order differential equations

### Interconnections

- series interconnection

  <div align = center><img height = 150 src = "./assets/Ch_1_figure_17.png"></div>

- parallel interconnection

  <div align = center><img height = 180 src = "./assets/Ch_1_figure_18.png"></div>

- feedback connection

  <div align = center><img src = "./assets/Ch_1_figure_19.png"></div>

- complicated connection which combine the former two interconnections

  <div align = center><img src = "./assets/Ch_1_figure_20.png"></div>

## 1.8 Basic System Properties

### Linearity

- additivity

<div align = center><img height = 100 src ="./assets/Ch_1_figure_21.png"></div>

- homogeneity

<div align = center><img height = 80 src = "./assets/Ch_1_figure_22.png"></div>
<div align = center><img height = 160  src = "./assets/Ch_1_figure_23.png"></div>

### Time-Invariant

<div align = center><img height = 120 src = "./assets/Ch_1_figure_24.png"></div>

<div align = center><img height = 200 src = "./assets/Ch_1_figure_25.png"></div>

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

<div align = center><img height = 100 src = "./assets/Ch_1_figure_26.png"></div>

### Stability

if the input to a stable system is bounded, then the output must also be bounded

<div align = center><img src = "./assets/Ch_1_figure_27.png"></div>
