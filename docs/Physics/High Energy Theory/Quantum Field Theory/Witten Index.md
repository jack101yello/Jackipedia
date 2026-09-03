# Witten Index

The Witten index is a partition-function-like object defined on a supersymmetric theory. For a radially quantized superconformal field theory, the Witten index is called the [[Superconformal Index|superconformal index]].

## Motivating the Witten Index

### The Supersymmetric Harmonic Oscillator

Consider a supersymmetric harmonic oscillator

$$
L = \frac{1}{2} \dot{x}^2 - \frac{1}{2} x^2 + i \bar{\psi} \dot{\psi} - \bar{\psi} \psi, \quad H = \frac{1}{2} p^2 + \frac{1}{2} x^2 + \bar{\psi} \psi
$$

Quantizing this system gives creation and annihilation operators

$$
a_B^\dagger = \frac{\sqrt{2}}{2} (-ip + x), \quad a_B = \frac{\sqrt{2}}{2} (ip + x), \quad A_F^\dagger = \bar{\psi}, \quad a_F= \psi
$$

obeying $[a_, a_B^\dagger] = \{a_F, a_F^\dagger\}= 1$. The Hamiltonian is then $H = a_B^\dagger a_B + a_F^\dagger a_F$, which has supersymmetric $Q = a_B^\dagger a_F$ and $\bar{Q} = a_F^\dagger a_B$, with algebra

$$
[Q, H] = [\bar{Q}, H] = 0, \quad \{Q, \bar{Q}\}= H
$$

This is a generic feature of supersymmetry algebras. There is also a $\mathbb{Z}_2$ symmetry: the Fermion number. What is the spectrum of this theory? The ground state has $H \vert 0 \rangle = Q \vert 0 \rangle = 0$, and excited states are defined by:

$$
\vert \chi_B, n \rangle = \left(a_B^\dagger\right)^n \vert 0 \rangle, \quad \vert \chi_F, m \rangle = \left(a_B^\dagger\right)^n a_F^\dagger \vert 0 \rangle
$$

The former tower of states has $F = 0$ and the latter $F = 1$. The partition function is

$$
Z[x] = \text{Tr}\: x^H = 1 + (x + x^2 + \dots) + (x + x^2 + \dots) = \frac{1 + x}{1-x}, \quad x = e^{-\beta}
$$

The single letter partition function $z(x)$ is the partition function over states with only one particle. Separating out bosons and fermions:

$$
z_B(x) = \text{Tr}_{\text{bosons}}\: x^H = x, \quad z_F(x) = \text{Tr}_{\text{fermions}}\: x^H = x, \quad z(x) = z_B(x) + z_F(x)
$$

The full partition function is:

$$
z_B(x) = x \mapsto \frac{1}{1-x} \equiv Z_B(x), \quad z_F(x) = x \mapsto 1+x \equiv Z_F(x), \quad Z = Z_B Z_F = \frac{1+x}{1-x}
$$

This is because the spectrum of boson states is indexed by the natural numbers of bosonic creation operators, whereas the spectrum of fermion states is indexed only by the presence or absence of a fermionic creation operator. This replacement operation is encoded in [[Plethystic Exponentiation|plethystic exponentiation]]. Here, we see:

$$
Z_B(x) = \text{PE}[z_B(x)], \quad Z_F(x, f) = \tilde{\text{PE}}[z_F(x, f)], \quad Z = Z_B Z_F
$$

In an interacting theory, computing the partition function is much harder. The generic supersymmetric interacting Lagrangian is

$$
L = \frac{1}{2} \dot{x}^2 - \frac{1}{2} W'(x)^2 + i \bar{\psi} \dot{\psi} - W''(x) \bar{\psi} \psi
$$

where $W(x)$ is called the superpotential. $W(x) = \frac{x^2}{2}$ recovers the aforementioned supersymmetric harmonic oscillator, and higher-order terms will give rise to interactions. While the partition function and spectrum are hard to compute, there is a nicely behaved and more accessible quantity.

Notice that all excited states have degeneracy two: one fermionic and one bosonic state, by supersymmetry: $H(\bar{Q} \vert \psi \rangle) = \bar{Q} H \vert \psi \rangle = E(\bar{Q} \vert \psi \rangle)$. Because states can only become or cease to be zero energy in pairs, the Witten index is defined as:

$$
I = \text{Tr}\: (-1)^F x^H
$$

This causes cancellation for all but the ground state. For instance, the supersymmetric harmonic oscillator has

$$
I = 1 + (x + x^2 + \dots) - (x + x^2 + \dots) = 1
$$

Even if we turn on (supersymmetry-preserving) interactions, the index must remain $1$. Conversely, one may set the interaction strength to zero before computing the index, to which only the ground state contributes.

Define the single letter indices:

$$
i_B(x) = \text{Tr}_{\text{bosonic letters with $H = 0$}}\: x^H, \quad i_F(x) = \text{Tr}_{\text{fermionic letters with $H = 0$}}\: x^H
$$

$$
i(x) = i_B(x) - i_F(x), \quad I = \text{PE}[i(x)]
$$

For instance, the supersymmetric harmonic oscillator has:

$$
i_B(x) = 0, i_F(x) = 0 \implies i(x) = 0 \implies I(x) = \text{PE}[0] = 1
$$

Consider instead $2N$ copies of the supersymmetric harmonic oscillator:

$$
L = \frac{1}{2} \vert \dot{x}_i \vert^2 - \frac{1}{2} \vert x_i \vert ^2 + i \bar{\psi}_i \dot{\psi}_i - \bar{psi}_i \psi_i
$$

This has $SO(2N)$ symmetric, which is preserved by interactions of the form:

$$
L = \frac{1}{2} x_i^2 - \frac{1}{2} \left\vert \frac{\partial W(x_i)}{\partial x_i} \right\vert^2 + i \bar{\psi}_i \dot{\psi}_i - \bar{\psi}_i \psi_i
$$

Let us consider the free theory, as we are interested in the index. The partition function has:

$$
z_B(x) = 2Nx, z_F(x) = 2Nx \implies Z(x) = \left(\frac{1+x}{1-x}\right)^{2N}
$$

### Fugacity

We are often interested in keeping track of the representations of the states under global symmetries, such as the $SO(2N)$ symmetric in the multi-copy supersymmetric harmonic oscillator. We can do this by turning on [[Fugacity|fugacities]] with respect to the [[Cartan Algebra|Cartan generators]], as so:

$$
Z(x, a_i) = \text{Tr}\: x^H a_i^{J_i}, \quad i = 1, \dots, N
$$

Because the bosons transform in the fundamental representation, their single letter partition function is then

$$
z_B(x, a_i) = x \left( a_1 + \frac{1}{a_1} + \dots + a_n + \frac{1}{a_n} \right) = x\: \chi_{\text{fund}} (a_i)
$$

where $\chi_{\text{fund}}(a_i)$ is the character of the fundamental representation, which is generically:

$$
\chi_{R}(a_i) = \sum_{\rho \in R} \prod_i a_i^{\rho_i} \equiv \sum_{\rho \in R} a^{\rho}
$$

where $\rho = (\rho_1, \dots, \rho_N)$ is a weight vector. We then have:

$$
z_B(x, a_i) = z_F(x, a_i) = x\: \chi_{\text{fund}}(a_i)
$$

$$
Z_B(x, a_i) = \prod_{i=1}^{N} \frac{1}{(1-x a_i)(1-x/a_i)}, \quad Z_F(x, a_i) = \prod_{i = 1}^{N} (1+xa_i)(1+x/a_i)
$$

$$
Z(x, a_i) = \prod_{i=1}^{N} \frac{(1+xa_i)(1+x/a_i)}{(1-xa_i)(1-x/a_i)} \equiv \prod_\rho \frac{1+xa^\rho}{1-xa^\rho}
$$

Orthogonality of characters lets us isolate the partition function over states which transform under a given representation:

$$
\frac{1}{\vert W \vert} \oint \prod_{i=1}^{N} \frac{da_i}{2\pi i a_i} \Delta(a_i) \chi_R(a_i) \chi_{R'}(a_i) = \delta_{RR'}
$$

where $\vert W \vert$ is the cardinality of the Weyl group and $\Delta(a_i)$ is the Van-der-Monde determinant:

$$
\Delta(a_i) = \frac{1}{\text{PE}\left[\sum_{\alpha} a^\alpha \right]} = \prod_{\alpha} (1-a^\alpha)
$$

where $\alpha = (\alpha_1, \dots, \alpha_N)$ are the roots of the [[Lie Algebra|Lie algebra]]. Using this, we have the partition function over states in the representation $R$ as:

$$
Z(x, a_i) \vert_{R} = \frac{1}{\vert W \vert} \oint \prod_{i=1}^{N} \frac{da_i}{2\pi i a_i} \Delta(a_i) Z(x, a_i) \chi_R(a_i)
$$