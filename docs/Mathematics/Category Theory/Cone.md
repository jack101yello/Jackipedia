
# Cone (Category Theory)

For a [[Diagrams (Category Theory)|diagram]] $F: J \to C$, a cone over $F$ with summit (or apex) $c \in C$ is a [[Natural Transformation|natural transformation]] $\lambda: \Delta c \Rightarrow F$, where $\Delta c$ is the [[Constant Diagram Functor|constant functor]] at $c$.

## The Legs of a Cone

The components $\lambda_j: c \to Fj$  (for $j \in J$) of a cone are called the legs of the cone.

## Cocones

A natural transformation $\lambda: F \Rightarrow \Delta c$ is called a cone under a diagram $F$ with nadir $c$, or alternately is called a cocone.

## Examples of Cones

Consider a diagram $F$ indexed by the [[Poset Category|poset category]] $(\mathbb{Z}, \leq)$, where $F: (n \leq m) \mapsto (f_{n,m}: F n \to F m)$. A cone over $F$ with summit $c$ is a family of morphisms $\lambda_n: c \to Fn$ such that, for every $n \leq m$, $Ff(\lambda_j(c)) = Ff(Fj) = \lambda_k(c) = Fk$.

## Limits and Colimits

A [[Limit|limit]] is the universal cone over a diagram, while a [[Colimit|colimit]] is the universal cocone under a diagram.