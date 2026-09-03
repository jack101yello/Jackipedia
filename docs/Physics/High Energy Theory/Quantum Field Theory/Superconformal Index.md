# The Superconformal Index

The superconformal index is the [[Witten Index|Witten index]] of a [[Superconformal Field Theory|superconformal field theory]] in the radial quantization.

## $\mathcal{N} = 1$

The superconformal index is schematically

$$
\mathcal{I}(\mu_i) = \text{Tr}\: (-1)^F x^\delta \mu_i^{\mathcal{M}_i}
$$

where $\delta = \frac{1}{2} \{Q, Q^\dagger\}$. Only $\delta = 0$ states can contribute, and so the index is independent of $x$. The Fermi-Bose cancellation can only occur if the [[Fugacity|fugacities]] are those for which the charges $\mathcal{M}_i$ commute with the supercharge $Q$. This theory has an infinite number of states with $\delta = 0$, and in fact an infinite number of single letter states with $\delta = 0$. The fugacities help to regulate this divergence.

The supercharges are $\{ Q_\alpha, S^\alpha \equiv Q^{\dagger \alpha}, \tilde{Q}_{\dot{\alpha}}, \tilde{S}^{\dot{\alpha}} \equiv \tilde{Q}^{\dagger \dot{\alpha}} \}$, where $\alpha = \pm$ and $\dot{\alpha} = \dot{\pm}$ are $SU(2)_{1}$ and $SU(2)_2$ indices, respectively, with $SU(2)_1 \times SU(2)_2 = \text{Spin}(4)$ the isometry group of $S^3$. The superconformal algebra satisfies:

$$
\{Q_\alpha, Q^{\dagger \beta}\} = \Delta + 2 M_{\alpha}^{\beta} + \frac{3}{2} r, \quad \{\tilde{Q}_{\dot{\alpha}}, \tilde{Q}^{\dagger \dot{\beta}}\} = \Delta + 2 \tilde{M}_{\alpha}^{\beta} - \frac{3}{2} r
$$

where $\Delta$ is the conformal dimension, $M$ and $\tilde{M}$ are the $SU(2)_1$ and $SU(2)_2$ generators, and $r$ is the generator of the $U(1)_r$ R-symmetry. Here $Q$ has $r = -1$ and $\tilde{Q}$ has $r = 1$, with daggers flipping the sign of $r$.

Choosing $Q \equiv Q_-$ to define the index, we have $\delta = \Delta - 2j_1 + \frac{3}{2} r$. $Q$ commutes with $SU(2, 1)$ within the superconformal algebra $SU(2, 2|1)$, which has rank $2$. We choose the charges $\mathcal{M}_i = \frac{1}{3} (\Delta + j_1) \pm j_2$ by convention. The index is then:

$$
\mathcal{I}(p, q) \equiv \text{Tr}\: (-1)^F p^{\frac{1}{3} (\Delta + j_1) + j_2} q^{\frac{1}{3} (\Delta + j_1) - j_2} = \text{Tr}\: (-1)^F p^{j_1 - \frac{1}{2} r +  j_2} q^{j_1 - \frac{1}{2} r - j_2}
$$

because $\delta = \Delta - 2j_1 + \frac{3}{2} r$, but only $\delta = 0$ states contribute.

### The Chiral Multiplet

Consider the free chiral multiplet $\Phi$ obeying $\bar{Q} \Phi = 0$, which has superspace expansion

$$
\Phi = \phi + \sqrt{2} \theta \phi + i \theta^\dagger \bar{\sigma}^\mu \theta \partial_\mu \phi
$$

The r-charge of $\phi$ is $\frac{2}{3}$. The spectrum of local operators are constructed from our chiral multiplet and its derivatives, and so our creation operators are $\phi, \partial_\mu \phi, \partial_\mu \partial_\nu \phi, \dots, \psi, \partial_\mu \psi, \partial_\mu \partial_\nu \psi, \dots$ and their conjugates, though note $\partial_\mu \partial^\mu \phi = 0$ and $\partial_{\alpha \dot{\alpha}} \phi^{\alpha} = 0$. We can now tabulate the letters and compute the single letter index:

| Letter                                            | $\Delta$ | $j_1$ | $j_2$ | $r$  | $\delta$ | $\mathcal{I}$ |
| ------------------------------------------------- | -------- | ----- | ----- | ---- | -------- | ------------- |
| $\phi$                                            | 1        | 0     | 0     | 2/3  | 2        | -             |
| $\psi_+$                                          | 3/2      | 1/2   | 0     | -1/3 | 0        | $-(pq)^{2/3}$ |
| $\psi_-$                                          | 3/2      | -1/2  | 0     | -1/3 | 2        | -             |
| $\partial_{\dot{+}}^{\alpha} \psi_{\alpha}$       | 5/2      | 0     | 1/2   | -1/3 | 2        | -             |
| $\partial_{\dot{-}}^{\alpha} \psi_{\alpha}$       | 5/2      | 0     | -1/2  | -1/3 | 2        | -             |
| $\Box \phi$                                       | 3        | 0     | 0     | 2/3  | 4        | -             |
| $\bar{\phi}$                                      | 1        | 0     | 0     | -2/3 | 0        | $(pq)^{1/3}$  |
| $\psi_{\dot{+}}$                                  | 3/2      | 0     | 1/2   | 1/3  | 2        | -             |
| $\psi_{\dot{-}}$                                  | 3/2      | 0     | -1/2  | 1/3  | 2        | -             |
| $\partial_{+}^{\dot{\alpha}} \psi_{\dot{\alpha}}$ | 5/2      | 1/2   | 0     | 1/3  | 2        | -             |
| $\partial_{-}^{\dot{\alpha}} \psi_{\dot{\alpha}}$ | 5/2      | -1/2  | 0     | 1/3  | 4        | -             |
| $\Box \bar{\phi}$                                 | 3        | 0     | 0     | -2/3 | 2        | -             |
| $\partial_{+\dot{+}}$                             | 1        | 1/2   | 1/2   | 0    | 0        | p             |
| $\partial_{-\dot{+}}$                             | 1        | -1/2  | 1/2   | 0    | 0        | q             |
| $\partial_{+\dot{-}}$                             | 1        | 1/2   | -1/2  | 0    | 2        | -             |
| $\partial_{-\dot{-}}$                             | 1        | -1/2  | -1/2  | 0    | 2        | -             |

and so

$$
i_\phi(p, q) = \frac{(pq)^{1/3} - (pq)^{2/3}}{(1-p)(1-q)}
$$

If we refine this with the fugacities of the Cartan generators, then we have:

$$
i_\phi(a_i; p, q)= \frac{(pq)^{1/3} \chi_{\bar{R}}(a_i) - (pq)^{2/3} \chi_R (a_i)}{(1-p)(1-q)}
$$

The full index, obtained via [[Plethystic Exponentiation|plethystic exponentiation]], is

$$
\mathcal{I}_\phi(a; p, q) = \Gamma\left( (pq)^{1/2} a^{-1}; p, q \right)
$$

where $\Gamma(z; p, q)$ is the [[Elliptic Gamma Function|elliptic gamma function]].

#### The Superpotential

A superpotential interaction will change the $R$-charge of the chiral multiplet, which is determined by requiring that the superpotential itself have $R$-charge $2$. If the chiral multiplet has $R$-charge $r$, then the right-handed fermion $\psi_+$ and the conjugate boson $\bar{\phi}$ (the only two particles contributing to the index) will have $R$-charges $r-1$ and $-r$, respectively. Therefore, the index will be:

$$
i_{\phi r}(p, q) = \frac{(pq)^{r/2} - (pq)^{1-r/2}}{(1-p)(1-q)} \implies \mathcal{I}_{\phi r}(a; p, q) = \Gamma\left( (pq)^{r/2} a ; p, q\right)
$$

For instance, a massive chiral multiplet has $W(\Phi) = m \Phi^2$, which fixes the $\phi$ $R$-charge at $1$, giving $\mathcal{I}_{\phi 1}(a; p, q) = \Gamma\left((pq)^{1/2}; p, q\right) = 1$, which is consistent with the expectation that the massive theory have a unique supersymmetric ground state. In fact, a theory with two chiral multiplets and $W(\Phi_1, \Phi_2) = m \Phi_1 \Phi_2$ will also have an index of identically $1$.

Consider another example with linear superpotential $W(\Phi) = \eta \Phi$, which spontaneously breaks supersymmetry. The $R$-charge of $\Phi$ is necessarily $2$, and so we have $\mathcal{I}_{\phi 2}(p, q) = \Gamma(pq; p, q) = 0$. This is sensible, as the $\phi_+ \vert 0 \rangle$ state will have the same energy as $\vert 0 \rangle$, and so the ground state drops out of the index. This also means that $\phi_+$ acts as a Goldstino mode for spontaneous supersymmetry breaking. Any such theory has a neutral chiral multiplet with $R$-charge $2$, and therefore vanishing superconformal index.

### The Vector Multiplet

We are also generically interested in gauge theory and therefore the vector multiplet. The letters with $\delta = 0$ are:

| Letter                                                     | $\Delta$ | $j_1$ | $j_2$ | $r$ | $\delta$ | $\mathcal{I}$ |
| ---------------------------------------------------------- | -------- | ----- | ----- | --- | -------- | ------------- |
| $\bar{\lambda}_{\dot{+}}$                                  | 3/2      | 0     | 1/2   | -1  | 0        | -p            |
| $\bar{\lambda}_{\dot{-}}$                                  | 3/2      | 0     | -1/2  | -1  | 0        | -q            |
| $F_{++}$                                                   | 2        | 1     | 0     | 0   | 0        | pq            |
| $\partial_{+}^{\dot{\alpha}} \bar{\lambda}_{\dot{\alpha}}$ | 5/2      | 1/2   | 0     | -1  | 0        | pq            |
| $\partial_{+\dot{+}}$                                      | 1        | 1/2   | 1/2   | 0   | 0        | p             |
| $\partial_{-\dot{+}}$                                      | 1        | -1/2  | 1/2   | 0   | 0        | q             |

The single letter index is therefore:

$$
i_V(a_i; p, q) = \frac{-p -q + 2pq}{(1-p)(1-q)} \chi_{\text{adj}}(a_i) = \left( -\frac{p}{1-p} - \frac{q}{1-q} \right) \left( \sum_{\alpha} a^{\alpha} + N \right)
$$

### Gauge Theory

In gauge theories, we are only interested in operators which transform trivially under the gauge group, and so the index is:

$$
\mathcal{I}(b_k; p, q) = \frac{1}{\vert W \vert} \oint \left(\prod_{i=1}^{N} \frac{da_i}{2\pi i a_i}\right) \Delta(a_i) \mathcal{I}_V(a_i; p, q) \prod_{\phi_i} \mathcal{I}_{\phi_i}(a_i, b_k; p, q)
$$

where $a_i$ are the gauge symmetry fugacities and $b_k$ are the fugacities of the other symmetries under which the chiral multiplets transform. However:

$$
\Delta(a_i) \mathcal{I}_V(a_i; p, q) = \text{PE}\left[ \left( -\frac{p}{1-p} - \frac{q}{1-q} \right) \chi_{\text{adj}}(a_i) - \sum_{\alpha} a^{\alpha} \right]
= \kappa^N \prod_{\alpha} \Gamma(pqa^\alpha; p, q)
$$

for

$$
\kappa \equiv (p, p)(q, q), \quad (a, q) \equiv \prod_{i=0}^{\infty} (1-aq^i)
$$

We then have:

$$
\mathcal{I}(b_k; p, q) = \frac{\kappa^N}{\vert W \vert} \oint \frac{da_i}{(2\pi i)^N} \Gamma(pqa^\alpha; p, q) \prod_{\phi_i} \prod_{\rho \in R_i^G, \rho' \in {R'}_{i}^{G}} \Gamma\left( (pq)^{r_i/2} a^\rho b^{\rho'} ; p, q\right)
$$

For instance, consider $\mathcal{N} = 1$ $SU(2)$ gauge theory with three flavors of (anti-)quarks in the (anti-)fundamental representation. The right $R$ charges are $1/3$, and so the index is

$$
\mathcal{I} = \kappa \oint \frac{dz}{4\pi i z} \frac{1}{\Gamma(z^{\pm 2}; p, q)} \prod_{i=1}^{3} \Gamma\left( (pq)^{1/6} b u_i z^{\pm 1} \right) \Gamma\left( (pq)^{1/6} b^{-1} v_i z^{\pm 1}l p, q \right)
$$

where $\prod_{i=1}^{3} u_i = \prod_{i=1}^{3} v_i = 1$, where these fugacities $u_i$ and $v_i$ parameterize the $SU(3)_u \times SU(3)_v$ flavor symmetry, while $b$ parameterizes the baryonic $U(1)_b$. This integral happens to have closed form solution

$$
\mathcal{I} = \prod_{i < j} \Gamma\left( (pq)^{1/3} t_i t_j \right), \quad \left\{ t_i \right\} = \left\{ b u_i, b^{-1} v_i \right\}
$$

This is equivalent to the index of a theory with fifteen chiral multiplets and a superpotential yielding and $R$-charge of $2/3$. Indeed, there is a duality between gauge theory and a theory of only chiral multiplets.