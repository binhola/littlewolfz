---
tags:
  - maths
  - physics
  - SMS
draft: false
---
Joseph Fourier (1768 - 1830), a French mathematician, in 1807 submitted a paper on heat conduction to Academy of Sciences in Paris and claimed that every function defined on $[-\pi, \pi]$ could be represented in the form of a trigonometric series. 
## Periodic function
If $f(x)$ is a periodic function, for a *positive* period P
$$
f(x+P) = f(x)
$$
For example, sin/cos functions. Also, for any integer $n$:
$$
f(x+nP) = f(x)
$$
## Fourier series
Fourier series of $f(x)$ in $[-\pi, \pi]$ is a trigonometric series of the form:

$$
f(x) = \dfrac{1}{2} a_0 + \sum_{=1}^\infty a_n \cos(nx) + \sum_{=1}^\infty b_n \sin(nx)
$$
where $a_n$ and $b_n$ are Fourier coefficients.

Multiplying and integrating:

$$
\int_{-\pi}^{\pi} f(x) \cos \, mx \, dx = \dfrac{a_0}{2}\int_{-\pi}^{\pi} \cos \, mx \, dx + \sum_{n=1}^\infty a_n \int_{-\pi}^{\pi} \cos \, mx \cos \,nx \, dx + \sum_{n=1}^\infty b_n \int_{-\pi}^{\pi} \cos \, mx \sin \,nx \, dx
$$
Using the properties of sine and cosines:

$$
\begin{aligned}
\int_{-\pi}^{\pi} \cos \, mx \, dx &= \int_{-\pi}^{\pi} \sin \, mx \, dx = 0 \\
\int_{-\pi}^{\pi} \cos \, mx \, \cos \, nx \, dx &= \int_{-\pi}^{\pi} \sin \, mx \, \sin \, nx \, dx = 
\begin{cases}
0 & \text{if} & n \neq m \\
\pi & \text{if} & n = m
\end{cases}
\\
\int_{-\pi}^{\pi} \sin \, mx \, \cos \, nx \, dx &= 0  
\end{aligned}
$$
So, 

$$
a_m = \dfrac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos \, mx \, dx 
$$
$a_0$ can be obtained by setting $n=0$.
Similarly, we can find

$$
b_m = \dfrac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin \, mx \, dx 
$$

Those two equation for $a_m$ and $b_m$ are known as Euler-Fourier formulas.
## Gibb's phenomena
1. At the point of discontinuity, the series yields the mean value.
2. In the region immediately adjacent to the points of discontinuity, the expansion always overshoots the original function.
## Change of interval
The period can be expanded into other interval, say $2L$, by changing the variable:

$$
z = \dfrac{\pi}{L} x
$$
If $f(z)$ expands in the interval $-\pi < z < \pi$, then $f(z) = f(\dfrac{\pi}{L}x) = F(x)$ expands in $-L < x < L$, we have: 

$$
\begin{aligned}
a_m &= \dfrac{1}{L} \int_{-L}^{L} f(x) \cos \, mx \, dx \\
b_m &= \dfrac{1}{L} \int_{-L}^{L} f(x) \sin \, mx \, dx
\end{aligned}
$$
## Parseval's identity
$$
\dfrac{1}{2L} \int_{-L}^{L} [f(x)]^2 dx = (a_0/2)^2 + 1/2 \sum_{n=1}^\infty (a_n^2 + b_n^2)
$$
### Fourier transform
$$x(j\omega) = \int_{-\infty}^{\infty} x(t) e^{-j\omega t} dt$$
### Inverse fourier transform
$$x(t) = \dfrac{1}{2\pi} \int_{-\infty}^{\infty} x(j\omega) e^{j\omega t} d\omega$$
