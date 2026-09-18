
# Equalizer

An equalizer is the [[Limit|limit]] of a [[Diagrams (Category Theory)|diagram]] indexed by the [[Parallel Pair Category|parallel pair category]].

## The Equalizer as a Limit Cone

Consider a diagram $F: J \to C$, where $J$ is the parallel pair category. $F$ is simply a choice of two parallel morphisms, $(f, g: c \to c') \in C$. A [[Cone|cone]] over such a diagram with summit $c''$ is a pair of morphisms $a: c'' \to c$, $b: c'' \to c'$ such that $fa = ga = b$.

### The Category of Groups

Consider the category of groups. Let $G$ and $H$ be groups, $\phi: G \to H$ be a generic homomorphism, and $e: G \to H$ be the trivial homomorphism. The equilizer of these two homomorphisms is the kernel of $\phi$, and the leg of the limit cone is the inclusion map $\ker \phi \hookrightarrow G$. Generically, the equalizer of two parallel homomorphisms $\phi, \psi: G \to H$ is the subgroup of elements $g \in G$ such that $\phi(g) = \psi(g)$.