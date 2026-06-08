# Natural Transformation

Natural transformations are, along with the [[Category]] and the [[Functor]], a fundamental concept in [[Category Theory]]. A natural transformation is a mapping from one functor to another with the same domain and codomain as the first, subject to a naturality constraint.

In particular, let $C$ and $D$ be categories, and let $F, G: C \to D$. A natural transformation $\alpha: F \Rightarrow G$ is a map from $F$ to $G$ such that for each object $c \in C$, there is an arrow, called a component of the natural transformation, $\alpha_c: Fc \to Gc$, such that the [[Square Diagram]] commutes[^1].

## Vector Spaces and Linear Duals

The most common motivating example for the natural transformation is that of vector spaces and their linear duals. Let $V$ be a finite-dimensional vector space over the field $k$. It admits a linear dual space $V^* = \text{Hom}(V, k)$ of linear maps from $V$ to $k$. (This is to say, it is the [[Hom-Set]] between $V$ and $k$ in the category of vector spaces.)

We can show that $V$ is isomorphic to $V^*$ by constructing a dual basis. Let $e_i \in V$ define a basis on $V$, and let $e_i^* \in V^*$ such that $e_i^* e_j = \delta_{ij}$. Then $e_i^*$ define a basis on $V^*$, and the map between the basis defines an isomorphism. However, it is somewhat unsatisfying that we must adopt a particular basis in order to arrive at this conclusion.

In a more categorical view, we have a dual-space functor $(-)^*: \text{Vect}_k^{\text{op}} \to \text{Vect}_k$. This is a [[Contravariant Functor]] because linear maps will be reversed when switching to the dual description. For instance, mappings $\mathbb{R}^2 \to \mathbb{R}^3$ are $3 \times 2$ matrices, but these are mapped to $2 \times 3$ matrices under the dual-space functor.

Pushing this further, we can consider the double-dual $V^{**} = \text{Hom}(\text{Hom}(V, k), k)$ and the double-dual functor $(-)^{**}: \text{Vect}_k \to \text{Vect}_k$. We can certainly construct this by composing the dual-space functor with itself, but there is a more "natural" construction.

Define the evaluation function $f(v): V^* \to k$, which maps an element $u^* \in V^*$ to $u^* v \in k$. Given an element $v \in V$, this is a mapping from $V^*$ to $k$, which means that the evaluation function is an element of $\text{Hom}(V^*, k) = \text{Hom}(\text{Hom}(V, k), k) = V^{**}$ for each $v \in V$. That is to say, the evaluation function generically is a mapping $V \to V^{**}$. This mapping is in fact an isomorphism, and so $V \cong V^{**}$ without the need to refer to a basis.

The fact that the process of showing that $V \cong V^*$ required an appeal to a particular basis but showing that $V \cong V^{**}$ did not reflects that the latter is a natural isomorphism, whereas the former is not.

## Examples of Natural Transformations

There are many further examples of natural transformations, but some especially interesting ones are listed here.

1. There exists a pair of functors from $\text{Top}$ to $\text{Set}$ which map topological spaces to the set of their [[Open Set]]s or [[Closed Set]]s. While topologists generally opt to speak about open Sets as the natural framework for topology, it is well-known that all theorems could equally be converted into statements about closed sets. This fact is a consequence of the fact that the two functors are not only isomorphic, but naturally isomorphic.
2. Consider the category whose objects are [[Hilbert Space]]s and whose morphisms are linear operators between them, and an [[Endofunctor]] on this category such that a Hilbert space $\mathcal{H}$ is mapped to $\mathcal{H} \otimes \mathcal{H}$. It turns out that there is only one natural transformation from the identity endofunctor to this functor: the one whose components are the zero maps. This is a categorical statement of the [[No-Cloning Theorem]]. 
3. Let $A$ and $B$ be sets, let $\times$ and $+$ denote their Cartesian product and disjoint union (respectively), and let $A^B$ denote the set of functions from $B$ to $A$. Then the following are natural isomorphisms:

$$
A \times (B + C) \cong (A \times B) + (A \times C), \quad (A \times B)^C \cong A^C \times B^C
$$
$$
A^{B+C} \cong A^B \times A^C, \quad \left(A^B\right)^C \cong A^{B \times C}
$$
reflecting the standard arithmetic relations. There exists a functor from the category of sets to the category of partially-ordered real numbers which makes this analogy manifest.

---
[^1] This wiki does not yet support graphical commutative diagrams, but they will hopefully be introduced in an update soon.