
# Constant Diagram Functor

Let $F: J \to C$ be a [[Diagrams (Category Theory)|diagram]] on $C$ of shape $J$. For any $c \in C$, one may consider the constant functor at $c$ to be the functor $\Delta c: J \to C$ such that every element of $J$ is mapped to $c$. The constant diagram functor $\Delta: C \to C^J$ is the functor such that $\Delta: c \mapsto \Delta c$, where morphisms $f: c \to c'$ in $C$ are mapped to the constant natural transformation $\Delta f: \Delta c \Rightarrow \Delta c'$.

## Cones

Constant diagram functors have particular relevance in the study of [[Cone|cones]] and [[Limit|limits]]. A cone over a diagram $F: J \to C$  with summit $c \in C$ is a natural transformation $\lambda: \Delta c \Rightarrow F$, which is to say a natural transformation whose domain is a constant functor at the summit.