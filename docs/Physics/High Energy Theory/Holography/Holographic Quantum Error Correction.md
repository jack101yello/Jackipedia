# Holographic Quantum Error Correction

Lorem ipsum dolor sit amet...

## Operator Reconstruction in Holography

Consider a conformal field theory which satisfies, for primary operators $\theta_i$ and local effective action $S$:

$$
\langle \theta_1(t_1, \Omega_1) \dots \theta_n(t_n, \Omega_n) \rangle_{\text{CFT}} = \int \mathcal{D}\phi_i\: e^{i S(\phi_i, \Lambda)}\: \theta_1(t_1, \Omega_1) \dots \theta_n(t_n, \Omega_n) + \mathcal{O}(e^{-\Lambda})
$$
with the extrapolate dictionary

$$
\theta_i(t_i, \Omega_i) = \lim_{r \to \infty} r^{\Delta}\: \phi_i(r, t, \Omega)
$$
where $\frac{1}{\ell_{\text{AdS}}} \ll \Lambda \ll \frac{1}{\ell_{p}}$.

This can be used to compute arbitrary correlation functions corresponding to scattering experiments in the gravitational theory. There are some experiments which cannot be described this way, such as scattering experiments in the [[The Thermofield Double|thermofield double]] which don't return to the boundary because they approach a horizon.

### Bulk Reconstruction

Consider a scalar field $\phi$ on the vacuum in the [[Poincaré Patch|Poincaré patch]] of AdS, which can be decomposed as:

$$
\phi(z, x) = \int \frac{d^dk}{(2\pi)^d} \theta(-k^2) e^{ik \cdot x} \psi_k(z) a_k, \quad \psi_k \sim z^{d/2} J_{\frac{1}{2}\sqrt{d^2 + 4m^2}}\left(z\sqrt{-k^2}\right)
$$

The extrapolate dictionary constrains that $\lim_{z \to 0} \psi_k \to \mathcal{N}_{k^2}\: z^{\Delta}$ for $\Delta = \frac{d}{2} + \frac{1}{2} \sqrt{d^2 + 4m^2}$. We find that

$$
\phi(z, x) = \int dx'\: K(z, x; x') \theta(x')
$$

This $K(z, x; x')$ is called the smearing function, and defines our bulk field in terms of CFT operators.

#### The AdS-Rindler Reconstruction

A convenient reconstruction is the AdS-Rindler reconstruction. A nice subregion of AdS involves taking a bulk timeslice at $t = 0$, cutting it in half, and looking at the wedge formed by the lightcone from there to the boundary. On this "Rindler wedge", the metric is:

$$
ds^2 = -(\rho^2 - 1) d\tau^2 + \frac{d\rho^2}{\rho^2 - 1} + \rho^2 dH_{d-1}^2
$$

where $dH_{d-1}^2$ is the metric on the hyperbolic $(d-1)$-dimensional plane. Here $\rho = \infty$ is the boundary.

There is a set of modes $f_{\omega, \lambda} = e^{-i\omega\tau} Y_{\lambda}(\alpha)\psi_{\omega\lambda}(\rho)$ . For some bulk point $y$ within the Rindler wedge:

$$
\phi(y) = \int_{\partial \text{Rindler}} dY K(y, Y) \theta(Y)
$$

In the bulk, we can define the causal wedge $C(R)$ of any spatial boundary region $R$ as the intersection of the future $J^+(D_\partial(R))$ of the domain of dependence $D(R)$ of $R$ and the past $J^-(D_\partial(R))$. Here we are using operators PDEs to reconstruct bulk information from boundary data. It will turn out that there exist a better construction via a different method: quantum information theory.

One would assume that $\left[ \phi(y), \theta(Y) \right] = 0$, since these are spacelike separated operators.

## Quantum Error Correction

### Classical Error Correction

Generically, when sending information which may become corrupted, one can send multiple copies of each bit and take a majority vote. The no-cloning theorem implies that this will not work in quantum computing.

### The Three Qutrit Code

Consider a qutrit $\vert \psi \rangle = \sum_{i=0}^{2} c_i \vert i \rangle$. We can encode this information in three qutrits as $\vert \tilde{\psi} \rangle = \sum_{i=0}^{2} c_i \vert \tilde{i} \rangle$ where:

$$
\vert \tilde{0} \rangle = \frac{1}{\sqrt{3}} \left( \vert 000 \rangle + \vert 111 \rangle + \vert 222 \rangle \right), \quad
\vert \tilde{1} \rangle = \frac{1}{\sqrt{3}} \left( \vert 012 \rangle + \vert 120 \rangle + \vert 201 \rangle \right), \quad
\vert \tilde{2} \rangle = \frac{1}{\sqrt{3}} \left( \vert 021 \rangle + \vert 102 \rangle + \vert 210 \rangle \right)
$$

Thus, we have stored the same information in the entanglement of three qutrits, as a subspace of the 27-dimensional three qutrit Hilbert space. We can define an encoding map which acts only on the first two qutrits:

$$
\vert \tilde{i} \rangle = \left( U_{12} \otimes I_3 \right) \left( \vert i \rangle \otimes \vert \chi \rangle_{23} \right), \quad \vert \chi \rangle_{23} = \frac{1}{\sqrt{3}} \left( \vert 00 \rangle + \vert 11 \rangle + \vert 22 \rangle \right)
$$

Then $U_{12} \vert i, l \rangle = \vert k+i, k+2i \rangle$. Then we can create a state $\vert \tilde{\psi} \rangle = U_{12} \left( \vert \psi \rangle_1 \otimes \vert \chi \rangle_{23} \right)$. If we lose the third qutrit in transit, then we can still apply $U_{12}^\dagger$ and measure the state:

$$
U_{12}^\dagger \vert \tilde{\psi} \rangle = \vert \psi \rangle_1 \otimes \vert \chi \rangle_{23}
$$

However, cyclic permutation symmetry implies that we can do this for any of the qutrits! Thus, we have a way around the no-cloning theorem to error correct.

A logical operator is one which applies a transformation in the code subspace (and its transformation otherwise is irrelevant):

$$
\tilde{O} \vert \tilde{i} \rangle = (O)_{ij} \vert \tilde j \rangle, \quad \tilde{O}^\dagger \vert \tilde{i} \rangle = (O^\dagger)_{ij} \vert \tilde j \rangle
$$

We can also define $O_{12} = U_{12} O_1 U_{12}^\dagger$, and it will indeed be a logical operator. Therefore, we can represent local operators as operators on the first physical qutrit. It's important that $\vert \chi \rangle$ be a maximally entangled state and not a product state.

## The Connection to Holography

Let us construct a holographic system. By analogy, the three physical qutrits correspond to local CFT degrees of freedom, and the one logical qutrit corresponds to a bulk effective field theory degree of freedom.

Consider the physics qutrits as lying on a circle, corresponding to the boundary. The bulk qutrit then sits at the center of the bulk. We know from the earlier bulk reconstruction picture that given any two boundary operators, we can reconstruct the bulk operator.

Consider computing $\langle \tilde{\psi} \vert \left[ \tilde{O}, X_3 \right] \vert \tilde{\phi} \rangle$. We can replace $\tilde{O}$ with $O_{12}$, but that must commute with $X_3$, and so this matrix element vanishes. In the orthogonal complement of the code subspace, the bulk picture is that of a black hole in the bulk which has "eaten" our bulk state. This is where gravity enters the picture.