**References:**

**[1]** Kenkre et. al. Simple Solutions of the Torrey–Bloch Equations
in the NMR Study of Molecular Diffusion : https://physics.unm.edu/kenkre/papers/Art164.pdf



---

# **Solving Torrey-Bloch Equations via Physics-Informed Neural Networks (PINNs)**

Trying to reproduce the results in **[1]** using PINNs (deepxde library)

Bloch-Torrey equation for the magnetization density $M(\mathbf{r},t)$ with diffusion coefficient $D$ and arbitrary time-dependent liear gradient field is

$$M_t(\mathbf{r},t) = -igf(t)xM(\mathbf{r},t) + D\nabla^2M(\mathbf{r},t)$$

In 1-D

$$M_t(x,t) = -igf(t)xM(x,t) + D M_{xx}(x,t)$$

NMR signal is defined by

$$M(t) = \int_{-∞}^∞ M(x,t)dx$$

Denoting real and imaginary parts of $M(x,t) = u(x, t) + iv(x, t)$ we have

$$u_t - v(x, t) g f(t) x - Du_{xx}=0$$
$$v_t + u(x, t) g f(t) x - Dv_{xx}=0$$

where $f(x)$ is the envelope function of the external magnetic field.

![PINN Performance](https://github.com/ucoskun/bloch-torrey-pinn/blob/main/plot.png?raw=true)
