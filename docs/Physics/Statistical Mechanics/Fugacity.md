
# Fugacity

Fugacity is a quantity in statistical mechanics which allows one to factor conserved quantities into the partition function. In the context of the [[Superconformal Index|superconformal index]], fugacity is used to take into account symmetries of the system, including gauge invariance.

## Fugacity in Supersymmetric Theories

For instance, consider a supersymmetric theory with $2N$ bosons and $2N$ fermions having generic Lagrangian

$$
\mathcal{L} = \frac{1}{2} \dot{x}_i^2 - \frac{1}{2} \left\vert \frac{\partial W(x_i)}{\partial x_i} \right\vert^2 - i \bar{\psi}_i \dot{\psi}_i - \frac{\partial^2 W(x)}{\partial x_i \partial x_j} \bar{\psi}_i \psi_j
$$

The bosonic and fermionic one-letter partition functions are $z_B(x) = z_F(x) = 2 N x$, which through [[Plethystic Exponentiation|plethystic exponentiation]] gives

$$
Z(x) = \left(\frac{1+x}{1-x}\right)^{2N}
$$

However, we should like to keep track of how the states in this system transform, in this case under our global $SO(2N)$ symmetry. We do this by turning on fugacities with respect to the Cartan generators:

$$
z_B(x, a_i) = \text{Tr}\: x^H a_i^{J_i} = x \left( a_1 + \frac{1}{a_1} + \dots + a_n + \frac{1}{a_n} \right) = x \chi_{\text{fund}}(a_i)
$$

where $\chi_{\text{fund}}(a_i)$ is the [[Character of a Representation|character]] of the fundamental representation, in which these states transform. We have the same for the fermionic single-letter partition function, and so:

$$
Z(x, a_i) = \text{PE}[z_B(x, a_i)]\: \tilde{\text{PE}}[z_F(x, a_i)] = \prod_{i=1}^{N} \frac{(1+x a_i)(1 + x/a_i)}{(1-x a_i)(1 - x/a_i)}
$$

Setting the fugacities $a_i$ to $1$ recovers the standard partition function $Z(x)$. However, keeping these fugacities allows us to compute the partition function over only those states which transform under a gives representation of our group of interest, due to the orthogonality of characters of group representations.

## Fugacity in Statistical Mechanics

Consider a statistical system with temperature $T$, pressure $P$, volume per mole $V_m$, entropy per mole $S_m$ , and [[Chemical Potential|chemical potential]] $\mu$. The differential of chemical potential is $d\mu = V_m dP$. For an ideal gas, this is:

$$
d\mu = V_m dP = \frac{RT}{P} dP = RT\: d \log P
$$

but this is untrue for a real gas. However, we can define the fugacity $f$ such that

$$
d\mu = RT\: d\log f
$$

such that $\lim_{P \to 0} \frac{f}{P} = 1$. The ratio $\phi \equiv \frac{f}{P}$ is called the figacity coefficient. This is to say, the fugacity is an effective pressure such that the chemical potential of a real gas varies the same as for an ideal gas with that fugacity as its pressure.