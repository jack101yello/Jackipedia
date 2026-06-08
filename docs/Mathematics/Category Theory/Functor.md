# Functor

A functor is a mapping from one [[Category]] to another.

In particular, a functor $F: C \to D$ for categories $C, D$ must map objects $c \in C$ to objects $Fc \in D$, and morphisms $f \in C$ to morphisms $Ff \in D$, preserving sources, targets, identities, and composition. This last fact, equivalent to the statement that for all morphisms $f, g \in C$ , $Ff \circ Fg = F(f \circ g)$, is known as the functoriality axiom.

## Examples of Functors

There are many, many examples of functors. Some simple examples include:

1. The "[[Forgetful Functor]]" $U: \text{Grp} \to \text{Set}$ which maps a group to its underlying set and group homomorphisms to their respective functions. Likewise, there is an analogous functor from $\text{Top}$ to $\text{Set}$.
2. The fundamental group of a topological space defines a functor $\pi_1: \text{Top} \to \text{Grp}$, and the $n$-cycles $Z_n$, $n$-boundaries $B_n$, and $n$-th [[Homology]] $H_n$ all define functors from the category of chain complexes to the category of graded $R$-modules.
3. The there a [[Free Functor]] from the category of sets to the category of groups which maps a set $X$ to the free group on $X$.
4. There is an opposite functor $(-)^{\text{op}}: \text{Cat} \to \text{Cat}$ which maps a category to its [[Opposite Category]].

### Examples of the Functoriality Axiom

There are many seemingly unrelated corollaries of the functoriality axiom.

#### The Chain Rule

The derivative can be thought of as an endofunctor on $\text{Diff}$, mapping manifolds to their tangent bundles and functions to their derivatives.

Suppose $A, B, C$ are smooth manifolds, and $f: A \to B$ and $g: B \to C$ are differentiable functions. Then $f \circ g: A \to C$ is a smooth function, and functoriality implies that $d(f \circ g) = d(f) \circ d(g)$. However, this is simply the statement that $f'(g(x)) = f'(x) g'(x)$, which is the ordinary chain rule from introductory calculus.

#### Brouwer's Fixed Point Theorem

Consider the unit disk $D^2$. Suppose that there exists a continuous function $f: D^2 \to D^2$ that does not admit any fixed points. Then there must exist a function $r: D^2 \to S^1$ which maps a point $x \in D^2$ to the point on the boundary circle $S^1$ intersected by a ray from $f(x)$ through $x$. The points on the unit circles are fixed points of $r$, and so if we compose with the inclusion mapping $i: S^1 \to S^2$, $r \circ i$ must be the identity morphism on $S^1$. Functoriality of the fundamental group functor then implies $\pi_1(r) \circ \pi_1(i) = \pi_1(r \circ i) = \pi_1(id_{S^1}) = id_{\pi_1(S^1)}$, which is simply the identity homomorphism.

However, the homotopy groups of both the circle and the disk are well known: $\pi_1(D^2) = 0$ and $\pi_1(S^1) = Z$. Therefore, because $i: S^1 \to D^2$, $\pi_1(i): Z \to 0$ can only be the trivial/zero homomorphism, in turn implying $\pi_1(i) \circ \pi_1(r)$ is the trivial homomorphism.

$\pi_1(r) \circ \pi(i)$ cannot be both the identity homomorphism and the trivial homomorphism, and so there is a contradiction. Therefore, no such function can exists. The statement that every continuous endomorphism on the disk must admit a fixed point is precisely Brouwer's Fixed Point Theorem.

## Natural Transformations

A [[Natural Transformation]] is a mapping from one functor to another, sharing the same domain and codomain, subject to certain naturality constraints. The original goal of [[Category Theory]] was to study natural transformations, and categories and functors were a means by which to do so.