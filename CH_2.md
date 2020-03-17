# CH_2

[TOC]

## Intro Linear Time-invariant system

- linear
- time-invariant

## 2.1 Linear Constant-Coefficient Differential Equation

**Linear constant-coefficient differential equation** is the mathematical repression of a continuous-time LTI system.

### Classical Solution of Differential Equations

$$
\begin{aligned}
    &C_0\frac{d^nr(t)}{dt^n}+C_1\frac{d^{n-1}r(t)}{dt^{n-1}}+\cdots+C_{n-1}\frac{dr(t)}{dt}+C_nr(t)\\[2ex]
    &=E_0\frac{d^me(t)}{dt^m}+E_1\frac{d^{m-1}e(t)}{dt^{m-1}}+\cdots+E_{m-1}\frac{de(t)}{dt}+E_me(t)\\[2ex]
\end{aligned}\tag{1}
$$

$$
\begin{aligned}
    C_0\frac{d^nr(t)}{dt^n}+C_1\frac{d^{n-1}r(t)}{dt^{n-1}}+\cdots+C_{n-1}\frac{dr(t)}{dt}+C_nr(t)=0
\end{aligned}\tag{2}
$$

- Homogeneous solution (natural response)
  1. **Characteristic equation**
     $$C_0\alpha^n+C_1\alpha^{n-1}+\cdots+C_{n-1}\alpha+C_n=0\tag{3}$$
  2. **Characteristic roots** $\;\alpha_1,\alpha_2,\cdots,\alpha_n\;$ satisfy tje characteristic equation
   ---
  (**the basic solution to characteristic solutions**)
  3. **Homogeneous solution**
     $$\;r_h(t)=\sum_{i=1}^{n}{A_ie^{\alpha_it}}$$
     _If $\alpha_1$ is the k-th repeated roots, then there will be k number of $\alpha_1$:_$\sum_{i=1}^{k}{A_i t^{k-i}}e^{\alpha_1t}$
- Particular solution (forced response)
  1. Table look-up
     | Exciting $e(t)$ | Response $r(t)$ |
     | :-------------------------------------------------------------: | :-------------------------------------------------------------------------------------------------------------------------: |
     | $t^p$ | $B_1t^p+B_2t^{p-1}+L+B_pt+B_{p+1}$ |
     | $e^{\alpha t}$ | $Be^{\alpha t}$ |
     | $\sin(\omega t)$/$\cos(\omega t)$ | $B_1\sin(\omega t)+B_2\cos (\omega t)$ |
     | $t^pe^{\alpha t}\sin(\omega t)$/$t^pe^{\alpha t}\cos(\omega t)$ | $(B_1t^p+B_2t^{p-1}+L+B_pt+B_{p+1})e^{\alpha t}\sin(\omega t)+(D_1t^p+D_2t^{p-1}+L+D_pt+D_{p+1})e^{\alpha t}\cos(\omega t)$ |
- Auxiliary conditions (initial conditions)
  
  1. Determine the coefficients

$$
  r(t_0),\frac{dr(t_0)}{dt},\frac{d^2r(t_0)}{dt^2},L,
  \frac{d^{n-1}r(t_0)}{dt^{n-1}}
$$

## 2.2 Partial Initial Conditions

### The Law of Switching

$$
\begin{aligned}
  v_c(0_-)=v_c(0_+),\;i_L(0_-)=i_L(0_+)
\end{aligned}
$$

### Impulse Function Matching Method

$$
\delta(t)\quad\delta'(t)\quad\delta''(t)\quad\cdots
$$

### The Laplace Transform

$$
X(s)=\int_{0}^{\infty}{x(t)e^{-st}\mathrm{d}t}
$$

## 2.3 System Response

$$
\begin{aligned}
  \text{Total Response }&=\\[2ex]
  & = \text{Natural Response}+\text{Forced Response}\\[2ex]
  & = \text{Zero-input Response}+\text{Zero-state Response}\\[2ex]
  & = \text{Transient Response}+\text{Steady-state Response}\\[2ex]
\end{aligned}
$$

---

- **Zero-input Response**: results only from the initial state (_energy storage_)
- **Zero-state Response**: results only from the external inputs

---

- _Transient Response_: when $t\to\infty$, the response that approaches to 0
- _Steady-state Response_: when $t\to\infty$, the response that keeps

---

$$
\begin{aligned}
r(t)=r_{zi}(t)+r_{zs}(t)&=\sum_{k=1}^{n}{A_{zik}e^{\alpha_kt}+\sum_{k=1}^n{A_{zsk}e^{\alpha_kt}+B(t)}}\\[2ex]
&=\text{Zero-input Response}+\text{Zero-state Response}\\[2ex]
&=\sum_{k=1}^{n}{A_{k}e^{\alpha_kt}}+B(t)\\[2ex]
&=\text{Natural Response}+\text{Forced Response}
\end{aligned}
$$

## 2.4 The Unit Impulse Response

$$
\begin{aligned}
&C_0\frac{\mathrm{d}^nr(t)}{\mathrm{d}t^n}+C_1\frac{\mathrm{d}^{n-1}r(t)}{\mathrm{d}t^{n-1}}+\cdots+C_{n-1}\frac{\mathrm{d}r(t)}{\mathrm{d}t}+C_nr(t)\\[2ex]
&= E_0\frac{\mathrm{d}^me(t)}{\mathrm{d}t^m}+E_1\frac{\mathrm{d}^{m-1}e(t)}{\mathrm{d}t^{m-1}}+\cdots+E_{m-1}\frac{\mathrm{d}e(t)}{\mathrm{d}t}+E_me(t)
\end{aligned}\tag{1}
$$

if $e(t)=\delta(t)$, then $r(t)=h(t)$

$$
\Rightarrow\qquad
\begin{aligned}
  &C_0h^{(n)}(t)+C_1h^{(n-1)}(t)+\cdots+C_{n-1}h^{(1)}(t)+C_nh(t)\\[2ex]
  &=E_0\delta^{(m)}(t)+E_1\delta^{(m-1)}(t)+\cdots+E_{m-1}\delta^{(1)}(t)+E_m\delta(t)
\end{aligned}\tag{4}
$$

| Conditions |                             $h(t)$                              |
| :--------: | :-------------------------------------------------------------: |
|   $n>m$    |            $[\sum_{i=1}^{n}{A_ie^{\alpha_it}}]u(t)$             |
|   $n=m$    |       $[\sum_{i=1}^{n}{A_ie^{\alpha_it}}]u(t)+B\delta(t)$       |
|   $n<m$    | $[\sum_{i=1}^{n}{A_ie^{\alpha_it}}]u(t)+B\delta(t)+C\delta'(t)$ |

## 2.5 The Convolution Integral

$$
y(t)=x(t)*h(t)=\int_{-\infty}^{\infty}{x(\tau)h(t-\tau)\mathrm{d}\tau}
$$

- time reversal: $h(\tau)\rightarrow h(-\tau)$
- time shift: $h(-\tau)\rightarrow h(t-\tau)$
- multiplication: $x(\tau)h(t-\tau)$
- integrating: $y(t)=\int_{-\infty}^{\infty}{x(\tau)h(t-\tau)\mathrm{d}\tau}$

## 2.6 Properties of Convolution

### The Commutative Property

$$
x(t)*h(t)=h(t)*x(t)
$$

### The Distributive Property

$$
x(t)*[h_1(t)+h_2(t)]=x(t)*h_1(t)+x(t)*h_2(t)
$$

### The Associative Property

$$
[x(t)*h_1(t)]*h_2(t)=x(t)*[h_1(t)*h_2(t)]
$$

### The Differential and Integral Property

$$
\begin{aligned}
&\text{differential}\\[2ex]
y'(t)&=x(t)*h'(t)=x'(t)*h(t)\\[2ex]
y^{(n)}(t)&=x(t)*h^{(n)}(t)=x^{(n)}(t)*h(t)\\[2ex]
\end{aligned}\\[8ex]
\begin{aligned}
&\text{integral}\\[2ex]
y^{(-1)}(t)&=x(t)*h^{(-1)}(t)=x^{(-1)}(t)*h(t)\\[2ex]
y^{(-m)}(t)&=x(t)*h^{(-m)}(t)=x^{(-m)}(t)*h(t)\\[2ex]
\end{aligned}\\[8ex]
\begin{aligned}
&\text{generally}\\[2ex]
y^{(n-m)}(t)&=x^{(n)}(t)*h^{(-m)}(t)=x^{(-m)}(t)*h^{(n)}(t)\\[2ex]
&\text{specially, }n = 1\;m=1\\[2ex]
y(t)&=x^{(-1)}(t)*h'(t)=x'(t)*h^{(-1)}(t)\\[2ex]
\end{aligned}
$$

## 2.7 System Properties

### Stability

**Bounded Input Bounded Output (BIBO)**

$$\int_{-\infty}^{\infty}{|h(t)|\mathrm{d}t}<\infty$$

_Proof:_

$$
\begin{aligned}
&y(t)=x(t)*h(t)=h(t)*x(t)\\[2ex]
&\text{Let }|x(t)|\leq B\\[2ex]
&|y(t)|=|h(t)*x(t)|=|\int_{-\infty}^{\infty}{h(\tau)\cdot x(t-\tau)\mathrm{d}\tau}|\\[2ex]
&\leq \int_{-\infty}^{\infty}{|h(\tau)|\cdot |x(t-\tau)|\mathrm{d}\tau}\leq B\int_{-\infty}^{\infty}{|h(\tau)|\mathrm{d}\tau}\\[2ex]
&\text{If }|y(t)|<\infty\text{, then }\int_{-\infty}^{\infty}{|h(\tau)|\mathrm{d}\tau}<\infty
\end{aligned}
$$
