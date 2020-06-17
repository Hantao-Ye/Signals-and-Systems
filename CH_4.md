# CH_4

[TOC]

## Table and Equations

$$
x(t)=\sum_{k=-\infty}^{\infty}{a_ke^{jk\omega_0t}}\\[2ex]
a_k = \frac{1}{T}\int_T{x(t)e^{-jk\omega_0t}\mathrm{d}t}\\[2ex]
\frac{1}{T}\int_T {|x(t)|^2\mathrm{d}t} = \sum_{-\infty}^{\infty}{|a_k|^2}
$$

|                Periodic Signal                |         Fourier Series Coefficients         |
| :-------------------------------------------: | :-----------------------------------------: |
| $x(t)$ is half-wave symmetry $x(t)=-x(t-T/2)$ |                $a_{2k}  = 0$                |
|                $x(t)$ is real                 | $a_k=a^*_{-k}$ and $ \|a_k\| = \|a_{-k}\| $ |
|            $x(t)$ is real and even            |           $a_k$ is real and even            |
|            $x(t)$ is real and odd             |      $a_k$ is purely imaginary and odd      |

## 4.1 Fourier Series Representation of Continuous-time Periodic Signals

### Trigonometric Fourier Series

Periodic Signal $x(t)$, with period $T_1$

$$
x(t)=a_0+\sum_{n=1}^{\infty}{a_n\cos{(n\omega_1t)}+b_n\sin{(n\omega_1t)}}
$$

- Constant Component: $a_0=\frac{1}{T_1}\int_{t_0}^{t_0+T_1}{x(t)\mathrm{d}t}$
- Cosine Coefficients: $a_n=\frac{2}{T_1}\int_{t_0}^{t_0+T_1}{x(t)\cos{(n\omega_1t)}\mathrm{d}t}$
- Sine Coefficients: $b_n=\frac{2}{T_1}\int_{t_0}^{t_0+T_1}{x(t)\sin{(n\omega_1t)}\mathrm{d}t}$

#### An Alternative Form for the Fourier Series

$$
x(t)=c_0+\sum_{n=0}^{\infty}{c_n\cos{(n\omega_1t+\phi_n)}}
$$

$$
\begin{split}
    c_0 = a_0\qquad c_n=\sqrt{a_n^2+b_n^2}\qquad \phi_n=\arctan(-\frac{b_n}{a_n})\\[2ex]
    a_n = c_n \cos(\phi)\qquad b_n=-c_n\sin(\phi_n)
\end{split}
$$

<div align=center><img height = 300 src = "./assets/Ch_4_figure_1.png"></div>

- x(t) is real and even

$$
b_n=0\qquad c_n=a_n\\[2ex]
\phi_n=
\begin{cases}
    0 \quad &a_n>0\\[2ex]
    \pm \pi \quad &a_n<0\\[2ex]
\end{cases}
$$

- x(t) is real and odd

$$
a_n= 0 \qquad \phi_n = \pm \frac{\pi}{2}
$$

### Complex Exponentially Fourier Series

$$
\begin{aligned}
x(t)&=a_0+\sum_{n=1}^{\infty}{a_n\cos(n\omega_1t)+b_n\sin(n\omega_1t)}\\[2ex]
    &= a_0+\sum_{n=1}^{\infty}{[\frac{a_n-jb_n}{2}e^{jn\omega_1t}+\frac{a_n+jb_n}{2}e^{-jn\omega_1t}]}
\end{aligned}
$$

Let

$$
\begin{aligned}
    F(n\omega_1)&=\frac{a_n-jb_n}{2}\\[2ex]
    F(-n\omega_1)&=\frac{a_n+jb_n}{2}\\[2ex]
\end{aligned}\\[4ex]
\because\sum_{n=1}^{\infty}{F(-n\omega_1)e^{-jn\omega_1t}}=\sum_{n=-1}^{-\infty}{F(n\omega_1)e^{jn\omega_1t}}\\[2ex]
\begin{aligned}
    \therefore\;&x(t)=\sum_{n=-\infty}^{\infty}{F(n\omega_1)e^{jn\omega_1t}}\\[2ex]
    &F(n\omega_1)=\frac{1}{T_1}\int_0^{T_1}{x(t)e^{-jn\omega_1t}\mathrm{d}t}
\end{aligned}
$$

<div align=center><img height = 300 src = "./assets/Ch_4_figure_2.png"></div>

$$
\begin{split}
    F(n\omega_1)=|F(n\omega_1)|e^{j\phi_n}\\[2ex]
    |F(n\omega_1)|=\frac{1}{2}\sqrt{a_n^2+b_n^2}=\frac{1}{2}c_n\qquad \phi_n=\arctan(-\frac{b_n}{a_n})\\[2ex]
    |F_n|=|F_{-n}|=\frac{1}{2}c_n\quad |F_n|+|F_{-n}|=c_n\quad F_n+F_{-n}=a_n
\end{split}
$$

**since the complex exponential Fourier series is**

$$
x(t)=\sum_{k=-\infty}^{\infty}{a_ke^{jk\omega_0t}}\qquad \omega_0= \frac{2\pi}{T}
$$

- $a_1e^{\pm j\omega_0t}$: fundamental components (first harmonic components)
- $a_ne^{\pm jn\omega_0t}$: Nth harmonic components

#### Names of the Equations and Coefficients

Given that $\omega_0=\frac{2\pi}{T}$

- Synthesis Equation:

$$
x(t)=\sum_{k=-\infty}^{\infty}{a_ke^{jk\omega_0t}}
$$

- Analysis Equation:

$$
    a_k = \frac{1}{T}\int_T{x(t)e^{-jk\omega_0t}\mathrm{d}t}
$$

- Fourier Series Coefficients (Spectral Coefficients): $\{a_k\}$
- Magnitude Spectrum: $|a_k|$
- Phase Spectrum: $\angle{a_k}$
  
  > the magnitude spectrum and phase spectrum all have **discrete property**, **harmonic property** and **convergence property**
- Constant Component:

$$
a_0=\frac{1}{T}\int_T{x(t)\mathrm{d}t}
$$

### The Effect of Symmetry

#### Even Function

The Fourier Series only contains **constant coefficients** and **cosine coefficients**, and $F(n\omega)$ is the **real function**

$$
b_n= 0\qquad a_n \neq 0\\[2ex]
F_n = \frac{1}{2}a_n \qquad \phi_n = 0
$$

#### Odd Function

The Fourier Series function only contains **sine coefficients**, and $F(n\omega_1)$ is the **virtual function**

$$
a_0= 0\qquad a_n = 0\\[2ex]
b_n \neq 0 \qquad F_n = -\frac{1}{2}jb_n
$$

#### Odd Harmonic Function

$$
x(t)=-x(t\pm\frac{T}{2})
$$

$$
\begin{cases}
    a_0 = 0\\[2ex]
    a_n=b_n=0\\[2ex]
\end{cases}
\quad n=2k\\[4ex]
\begin{cases}
    a_n = \frac{4}{T}\int_0^{\frac{T}{2}}{x(t)\cos(n\omega_1t)}\\[2ex]
    b_n = \frac{4}{T}\int_0^{\frac{T}{2}}{x(t)\sin(n\omega_1t)}\\[2ex]
\end{cases}
\quad n=2k-1\\[2ex]
$$

## 4.2 Convergence of the Fourier Series

### Dirichlet Conditions

- must be integrable
- bounded variation
- finite number of discontinuities

### Gibbs Phenomenon

the truncated Fourier series approximation $x_N(t)$ of a discontinuous signal $x(t)$ will in general exhibit high-frequency ripples and overshoot $x(t)$ near the discontinuities

<div align = center><img src = "./assets/Ch_4_figure_3.png"></div>

## 4.3 Parseval's Relation

the **total average power** in a periodic signal equals the sum of the average powers in **all of its harmonic components**

$$
\frac{1}{T}\int_0^T {|x(t)|^2\mathrm{d}t}= \frac{1}{T}\int_{-\frac{T}{2}}^{\frac{T}{2}} {|x(t)|^2\mathrm{d}t} = \sum_{-\infty}^{\infty}{|a_k|^2}
$$