
# Product (Category Theory)

In [[Category Theory]], the product is the [[Limit|limit]] of a [[Diagrams (Category Theory)|diagram]] inexed by a discrete category $J$ with only identity morphisms.

## The Limit Cone and Universal Property

For a diagram $F: J \to C$ for such a category $J$, a [[Cone|cone]] over $F$ is a $J$-indexed family of morphisms $\lambda_j: c \to Fj$. The limit is denoted $\prod_{j \in J} Fj$, and the legs of the limit cone are maps $\pi_k: \prod_{j \in J} Fj \to Fk$ for $k \in J$, called projection maps.

The universal property is that composition with the product projection defines a natural isomorphism:

$$
C(c, \prod_{j \in J} Fj) \xrightarrow[\pi_k]{} C(c, Fk) \cong \text{Cone}(c, F)
$$

## Topological Spaces

Let $X$ and $Y$ be [[Topological Space|topological spaces]]. The product $X \times Y$ has the continuous projection functions $\pi_X: X \times Y \to X$ and $\pi_Y: X \times Y \to Y$, satisfying the universal property that for any space $Z$ with continuous maps $f: Z \to X$ and $g: Z \to Y$, there exists a unique continuous function $h: Z \to X \times Y$ such that composing $h$ with the projection maps is equivalent to applying $f$ or $g$.

### The Product Topology

Suppose $Z$ is the single point $*$, which [[Representable Functor|represents]] the [[Forgetful Functor|forgetful functor]] $U: \text{Top} \to \text{Set}$. We have the bijection $\text{Top}(*, X \times Y) \cong \text{Top}(*, X) \times \text{Top}(*, Y)$, implying that the points in $X \times Y$ are in the Cartesian product of the underlying sets.

If instead we consider $Z = X \times Y$, then we have $\text{Top}(X \times Y, X \times Y) \cong \text{Top}(X \times Y, X) \times \text{Top}(X \times Y, Y)$, and so the topology on $X \times Y$ is the coarsest topology such that the projection functions are continuous. This is indeed the correct notion of a product topology.