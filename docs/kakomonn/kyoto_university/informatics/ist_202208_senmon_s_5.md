---
comments: false
title: 京都大学 情報学研究科 知能情報学専攻 2022年8月実施 専門科目 S-5
tags:
  - Kyoto-University
---

# 京都大学 情報学研究科 知能情報学専攻 2022年8月実施 専門科目 S-5

## **Author**
[realball](https://github.com/realballu3u)

## **Description**
Suppose that the Fourier transform $\mathcal{F}[f(x)]$ of a function $f(x)$ and the Fourier integral representation of the Dirac delta function $\delta(x)$ are given by the following formulae, where $x$ and $k$ are real numbers, and $i=\sqrt{-1}$. Answer the following questions.

$$
\begin{align}
\mathcal{F}[f(x)]&=F(k)=\frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}f(x)\mathrm{e}^{-ikx}\text{d}x \tag{i}\\
\delta(x)&=\frac{1}{2\pi}\int_{-\infty}^{\infty}\mathrm{e}^{ikx}\text{d}k \tag{ii}
\end{align}
$$

### Q.1
Compute the Fourier transform of the function given below, where $\omega$ is a real number.

(1) $f_1(x)=\left\{\begin{array}{ll}0&(x<0) \\ 1&(0\le x\le2)\\0&(x>2)\end{array}\right.$

(2) $f_{2}(x)=\cos^{2}\omega x$

### Q.2
Compute the Fourier transform of function $f_3(x)$ by following the steps below.

$$
f_3(x)=\left\{\begin{array}{l}0 \ \ (x<-2)\\
x+2 \ \ (-2\leq x<0)\\
2-x \ \ (0\leq x<2)\\
0 \ \ (x\geq2)\end{array}\right.
$$

(1) Derive the following equation concerning convolution operation.

$$
\mathcal{F}[f(x)*g(x)]=\mathcal{F}\left[\int_{-\infty}^{\infty}f(\tau)g(x-\tau)\text{d}\tau\right]=\sqrt{2\pi}\mathcal{F}[f(x)]\mathcal{F}[g(x)]
$$


(2) Find function $f_4(x)$ whose convolution with the above $f_1(x)$ satisfies $f_3(x)=f_1(x) * f_4(x)$, and explain how the convolution gives $f_3(x)$.

(3) Compute $\mathcal{F}[f_3(x)]$.

## **Kai**
### Q.1
#### (1)

$$
F[f_1(x)]=\frac{1}{\sqrt{2\pi}} \left( \frac{e^{-2i k} - 1}{i k} \right)
$$

#### (2)

$$
F[f_2(x)]=\frac{\sqrt{2\pi}}{2}\delta(-k)+\frac{\sqrt{2\pi}}{4}\delta(2\omega-k)+\frac{\sqrt{2\pi}}{4}\delta(-2\omega-k)
$$

### Q.2
#### (1)

$$
\begin{aligned}
\mathcal{F}[f(x)\ast g(x)] 
&= \mathcal{F}
\left[\int_{-\infty}^{\infty} f(\tau) g(x - \tau) d\tau \right] \\
&= \frac{1}{\sqrt{2\pi}} \int_{-\infty}^{\infty} \int_{-\infty}^{\infty}f(\tau) g(x - \tau)d\tau\cdot e^{-ikx} dx \\
&= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}f(\tau)d\tau \int_{-\infty}^{\infty}g(x-\tau)e^{-ikx}dx\\
&= \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty} g(t) e^{-ikt} dt \cdot \int_{-\infty}^{\infty} f(\tau) e^{-ik\tau} d\tau \\
&= \sqrt{2\pi}\mathcal{F}[f(x)]\mathcal{F}[g(x)]
\end{aligned}
$$

#### (2)

$$
f_4(x)=\begin{cases} 
0 & x < -2 \\
1 & -2\leq x \leq 0\\
0 & x > 0
\end{cases}
$$

$$
f_3(x)=f_1(x)\ast f_4(x) =\int_{0}^{2}f_4(x-\tau)d\tau
$$

#### (3)

$$
\mathcal{F}[f_3(x)]=\frac{2\sin^2k}{-\sqrt{2\pi}k^2}
$$
