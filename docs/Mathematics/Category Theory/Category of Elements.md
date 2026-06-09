# Category of Elements

For a [[Set-Valued Functor]] $F$ on a [[Category]] $C$, the category of elements of $F$, denoted $\int F$, is a category such that:

- The objects are pairs $(c, x)$ for $c \in C$ and $x \in Fc$.
- The morphisms are mappings $(c, x) \to (c', x')$ where $f: c \to c'$ in $C$ such that $Ff(x) = x'$.

Generically, they allow one to imbue a category with additional structure imposed by a set-valued functor on that category.

## Representable Functors

A covariant functor/[[Contravariant Functor]] is a [[Representable Functor]] if and only if its category of elements has an [[Initial Object]]/[[Terminal Object]].

## Connection to the Yoneda Lemma

[[The Yoneda Lemma]] provides an alternative definition of the category of elements. For a Set-Valued functor $F$ on a category $C$, an object in $\int F$ is a natural transformation $\alpha: C(c, -) \Rightarrow F$, and a morphism in $\int F$ from $\alpha: C(c, -) \Rightarrow F$ to $\beta: C(c', -) \Rightarrow F$ is a natural transformation $C(c', -) \Rightarrow C(c, -)$ (i.e.  a morphism $c \to c'$) such that the [[Triangle Diagram]] commutes[^1].

## The Contractible Groupoid

For any set-valued functor $F$, the full subcategory of $\int F$ spanned by the representations of $F$ is either empty if $F$ is not representable, or is a [[Contractible Groupoid]] if it is. This can be proven fairly easily:

> Assuming the law of the excluded middle, $F$ is either representable or not representable.
> 
> Suppose that $F$ is not representable. Then it has no representations, and so this full subcategory is empty.
> 
> Suppose that $F$ is representable. Any representation must define an initial object in $\int F$. Between any two initial objects in a category, there must be exactly one morphism in either direction, which must therefore compose to the identities. This forms precisely the structure of a contractible groupoid.

## Examples of the Category of Elements

1. Consider the functor $n-\text{Color}: \text{Graph}^{\text{op}} \to \text{Set}$ which carries a graph to the set of $n$-colorings of its vertices such that no adjacent vertices have the same color. In the category of elements of this functor, objects are $n$-colored graphs and morphisms are color-preserving graph homomorphisms.
2. A set $X$ and an endomorphism $f: X \to X$, together with a distinguished object $x_0$, define a discrete dynamical system. The discrete time-evolution of points are defined recursively by $x_{i+1} = f(x_i)$. The natural numbers $\mathbb{N}$ and the successor function $s: \mathbb{N} \to \mathbb{N}$ define the universal discrete dynamical system, as there exists a unique functor $r: \mathbb{N} \to X$ such that $r(n) = x_n$, such that the [[Square Diagram]] commutes. Consider the functor $U: \text{End} \to \text{Set}$, where $\text{End}$ is the category of sets equipped with an endomorphism and whose maps are functions such that the above [[Square Diagram]] commutes. This functor is represented by the universal discrete dynamical system, and the category of elements of $U$ is exactly the category of discrete dynamical system.
3. An object in the category of elements of the forgetful functor $U: \text{Vect}_k \to \text{Set}$ is a vector $v$ in some $k$-vector space $V$. A morphism $(V, v) \to (W, w)$ is a linear map $T: V \to W$ such that $T:  v \mapsto w$. Pairs $(k, c)$ for $c \in k \setminus \{0\}$ represent $U$ (and so are initial object in its category of elements), as any $c$ defines a linear isomorphism $c \cdot -: k \to k$.
4. Consider the functor $U(-)^n: \text{Grp} \to \text{Set}$. An object in the category of elements of this functor consists of a group $G$ and an $n$-tuple of elements $g_1, \dots, g_n \in G$, and a morphism $(\{g_1, \dots, g_n\}, G) \to (\{h_1, \dots, h_n\}, H)$ is a homomorphism $\phi: G \to H$ such that $\phi: g_i \mapsto h_i$. The universal group with $n$ elements $F_n$ would be the group with $x_1, \dots, x_n \in F_n$ with the [[Universal Property]] that for any $g_1, \dots, g_n \in G$, there is a unique group homomorphism $\phi: F_n \to G$ such that $\phi: x_i \mapsto g_i$. The free group with $n$ generators has exactly this property, and so it is an initial object in this category, and in turn $U$ is representable.
5. The category of elements of the functor $C(c, -)$ is the [[Slice Category]] of $C$ under the object $c$, $c/C$.

---
[^1] This version of the wiki does not support the drawing of commutative diagrams, but hopefully the functionality will be added soon.