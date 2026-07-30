# The Thermofield Double

The thermofield double is a formalism used to treat thermal mixed states as pure states in an overall larger system.

Consider a QFT with Hamiltonian $H$ and a complete set of energy eigenstates $\vert n \rangle$. Our goal is to describe the mixed state $\rho = e^{-\beta H}$. Consider a new QFT containing two copies of the original. States are then $\vert m \rangle_1 \otimes \vert n \rangle_2$. The thermofield double state is then:

$$
\vert \text{TFD} \rangle = \frac{1}{\sqrt{Z(\beta)}} \sum_n e^{-\beta E_n / 2} \vert n \rangle_1 \otimes \vert n \rangle_2
$$
The density matrix is $\rho_{\text{total}} = \vert \text{TFD} \rangle \langle \text{TFD} \vert$, and so in system 1 we have the reduced density matrix

$$
\rho_1 = \text{Tr}_2\: \rho_{\text{total}} = \sum_n e^{-\beta E_n} \vert n \rangle_1 {}_1\langle n \vert = e^{-\beta H_1}
$$
and so in system 1, our state is the original thermal state of interest. For some operator $\mathcal{O}_1$ made of local operators $\mathcal{O}_1 = \phi_1(x_1) \chi_1(y_1)$, one has $\langle \text{TFD} \vert \mathcal{O}_1 \vert \text{TFD} \rangle = \frac{1}{Z(\beta)} \text{Tr}_{\mathcal{H}_1} e^{-\beta H_1} \mathcal{O}_1$. The two systems are not coupled in the Lagrangian, but we're in an entangled state, so mixed operators may have non-zero expectation values.

We choose Hamiltonian $H_{\text{tot}} = H_1 - H_2$, and so the TFD state is time-independent:

$$
e^{-i H_{\text{tot}}} \vert \text{TFD} \rangle = \sum_n e^{-\beta E_n/2} e^{-i (H_1 - H_2)} \vert n_1 \rangle \otimes \vert n_2 \rangle = \vert \text{TFD} \rangle
$$
## Holography

The thermofield double state has immediate applications to [[The AdS-CFT Correspondence|holography]], as the eternal black hole in quantum gravity is dual to two copies of the CFT (in the thermofield double state), with each asymptotic boundary of AdS a copy of the dual CFT. A correlation function like $\langle \text{TFD} \vert \phi_1(x_1) \chi_2(x_2) \vert \text{TFD} \rangle$ can be computed using a single bulk field $\Phi$ whose boundary condition on the left boundary is a source for $\phi_1$ and whose boundary condition on the right is a source for $\chi_2$. The TFD Hamiltonian is dual to the bulk Hamiltonian which generated time evolution along the isometry $\partial_t$. 

Consider the AdS/CFT dictionary $Z_{\text{gravity}}[\partial M = \Sigma] = Z_{\text{CFT}}[\Sigma]$.

### The CFT Side

The Euclidean path integral which prepares the TFD state is a path integral along a cylindrical manifold $\Sigma = I_{\beta/2} \times S^{d-1}$, where $I_{\beta/2}$ is an interval of length $\frac{\beta}{2}$. The two $S^{d-1}$ rims at the ends of the cylinder correspond to states in the two subsystems.

### The AdS Side

We have a Euclidean gravity solution $M$ with conformal boundary condition $\partial M = I_{\beta/2} \times S^{d-1}$. It turns out that $M$ should be a half black hole, with a Euclidean half-disk glued to a Minkowski space ending at the singularity.

This setup is a manifestation of ER=EPR (at least in the semiclassical approximation), as entanglement between the two CFT subsystems only occurs due to the entangled TFD state. In the AdS picture, the two regions of the bulk are linked by a black hole interior/wormhole.