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