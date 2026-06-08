# Category Theory

Category Theory is a branch of mathematics which seek to abstract away as much underlying structure as possible. As such, many theorems from across mathematics are corollaries of results from Category Theory.

## The Category

A [[Category]] $C$ consists of the following information:

1. A collection $\text{ob}(C)$ of objects.
2. A collection $\text{mor}(C)$ of morphisms, each of which has a source object and a target object.
3. A binary operation $\circ$ on morphisms via which morphisms can be composed.

Additionally, every object $c \in C$ must have at least one [[Endomorphism]] called the identity morphism $id_c$.

## The Functor

A [[Functor]] $F: C \to D$ is a mapping from one category $C$ to another category $D$, such that

1. Every object $c \in C$ is mapped to an object $Fc \in D$.
2. Every morphism $f: c \to c'$ in $C$ is mapped to a morphism $Ff: Fc \to Fc'$ in $D$.
3. The functoriality axiom $Ff \circ Fg = F(f \circ g)$ for $f, g \in \text{mor}(C)$ is satisfied.
