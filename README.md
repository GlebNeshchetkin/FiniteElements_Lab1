# FiniteElements_Lab1

## u_exact
$$u(z) = \frac{1}{E} \left[ - \int_{0}^{z} \int_{0}^{y}fdxdy + E\frac{du}{dx}|_0z+Eu_0 \right]$$

$$\int_{0}^{z}\int_{0}^{y}fdxfdy=\int_{0}^{z}\left(\overline{f}\frac{x^2}{2}\right)|_0^ydy=\left(\overline{f}\frac{y^3}{6}\right)|_0^z=\overline{f}\frac{z^3}{6}$$

### Dirichelt-Dirichlet problem
$$u(z)=\frac{1}{E}\left(-\overline{f}\frac{z^3}{6}+E\frac{du}{dx}|_0z+Eu_0\right)\Rightarrow \left[ z= L\Rightarrow u(L)=u_g\right]\Rightarrow u_g=-\frac{fL^3}{6E}+\frac{du}{dx}|_0L+u_0 \Rightarrow$$

$$\Rightarrow \frac{du}{dx}|_0=\frac{u_g+\frac{\overline{f}L^3}{6E}-u_0}{L}\Rightarrow u(z)=-\overline{f}\frac{z^3}{6E}+\left( \frac{u_g+\frac{\overline{f}L^3}{6E}-u_0}{L} \right)z+u_0$$

### Dirichlet-Neumann problem
$$\frac{du(z)}{dz}=\frac{1}{E}\left( -\frac{3\overline{f}z^2}{6}+E\frac{du}{dx}|_0 \right)=\frac{\sigma(z)}{E}\Rightarrow \sigma(z)=\left( -\frac{\overline{f}z^2}{2}+E\frac{du}{dx}|_0 \right)\Rightarrow \sigma(L)=-\frac{\overline{f}L^2}{2}+E\frac{du}{dx}|_0=h\Rightarrow$$

$$\Rightarrow \frac{du}{dx}|_0=\frac{h+\frac{\overline{f}L^2}{2}}{E}\Rightarrow u(z)=-\overline{f}\frac{z^3}{6E}+\left( \frac{h+\frac{\overline{f}L^2}{2}}{E} \right)z+u_0$$


## Basis_gradient

### basisFunctionOrder = 2

#### 1) node = 0

$$N=\left(\frac{\xi-\xi_1}{\xi_0-\xi_1}\right)\left(\frac{\xi-\xi_2}{\xi_0-\xi_2}\right)$$

$$N'=\frac{2\xi-\xi_2-\xi_1}{\left(\xi_0-\xi_1\right)\left(\xi_0-\xi_2\right)}=\frac{\left( \xi-\xi_1 \right)+\left( \xi-\xi_2 \right)}{\left(\xi_0-\xi_1\right)\left(\xi_0-\xi_2\right)}$$

#### 2) node = 1

$$N=\left(\frac{\xi-\xi_0}{\xi_1-\xi_0}\right)\left(\frac{\xi-\xi_2}{\xi_1-\xi_2}\right)$$

$$N'=\frac{\left( \xi-\xi_0 \right)+\left( \xi-\xi_2 \right)}{\left(\xi_1-\xi_0\right)\left(\xi_1-\xi_2\right)}$$

#### 3) node = 2

$$N=\left(\frac{\xi-\xi_0}{\xi_2-\xi_0}\right)\left(\frac{\xi-\xi_1}{\xi_2-\xi_1}\right)$$

$$N'=\frac{\left( \xi-\xi_0 \right)+\left( \xi-\xi_1 \right)}{\left(\xi_2-\xi_0\right)\left(\xi_2-\xi_1\right)}$$

### basisFunctionOrder = 3

#### 1) node = 0

$$N=\frac{\left( \xi-\xi_1 \right)}{\left( \xi_0-\xi_1 \right)}\frac{\left( \xi-\xi_2 \right)}{\left( \xi_0-\xi_2 \right)}\frac{\left( \xi-\xi_3 \right)}{\left( \xi_0-\xi_3 \right)}$$

$$N'=\frac{\left( \xi-\xi_2 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_1 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_1 \right)\left( \xi-\xi_2 \right)}{\left( \xi_0-\xi_1 \right)\left( \xi_0-\xi_2 \right)\left( \xi_0-\xi_3 \right)}$$

#### 2) node = 1

$$N=\frac{\left( \xi-\xi_0 \right)}{\left( \xi_1-\xi_0 \right)}\frac{\left( \xi-\xi_2 \right)}{\left( \xi_1-\xi_2 \right)}\frac{\left( \xi-\xi_3 \right)}{\left( \xi_1-\xi_3 \right)}$$

$$N'=\frac{\left( \xi-\xi_2 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_0 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_0 \right)\left( \xi-\xi_2 \right)}{\left( \xi_1-\xi_0 \right)\left( \xi_1-\xi_2 \right)\left( \xi_1-\xi_3 \right)}$$

#### 3) node = 2

$$N=\frac{\left( \xi-\xi_0 \right)}{\left( \xi_2-\xi_0 \right)}\frac{\left( \xi-\xi_1 \right)}{\left( \xi_2-\xi_1 \right)}\frac{\left( \xi-\xi_3 \right)}{\left( \xi_2-\xi_3 \right)}$$

$$N'=\frac{\left( \xi-\xi_1 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_0 \right)\left( \xi-\xi_3 \right)+\left( \xi-\xi_0 \right)\left( \xi-\xi_1 \right)}{\left( \xi_2-\xi_0 \right)\left( \xi_2-\xi_1 \right)\left( \xi_2-\xi_3 \right)}$$
