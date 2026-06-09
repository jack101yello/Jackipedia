# Representable Functor

In [[Category Theory]], a representable functor is a [[Functor]] which is [[Natural Transformation|naturally isomorphic]] to the [[Hom-Set]] functor from a particular element.

More explicitly, let $C$ be locally small category and $F$ be a [[Set-Valued Functor]] on $C$. A representation for $F$ is a choice of $c \in C$ together with a natural isomorphism $C(c, -) \cong F$. If such a natural isomorphism exists, then $F$ is said to be representable, and $c$ is said to represent $F$.

## Examples of Representable Functors

1. Let $\star: C \to \text{Set}$ be the constant functor, which maps every object in $C$ to the singleton set $\{1\}$. $C$ has an [[Initial Object]] if and only if $\star$ is representable, and a [[Terminal Object]] if and only if its contravariant twin is representable.
2. The identity functor on [[The Category of Sets]] is represented by any singleton set. This is to say that for any set $X$, there is a natural isomorphism $\text{Set}(\{1\}, X) \cong X$, which defines a bijection between elements $x \in X$ and functions $x: 1 \to X$, taking the singleton element of $x$.
3. The [[Forgetful Functor]] $U: \text{Grp} \to \text{Set}$ is represented by the group $\mathbb{Z}$. That is to say, for any group $G$, there is a natural transformation $\text{Grp}(\mathbb{Z}, G) \cong UG$ which associates every element $g \in UG$ to the homomorphism $\mathbb{Z} \to G$ which maps $1$ to $G$.
4. Likewise, the forgetful functor $U: \text{Top} \to \text{Set}$ is represented by the singleton space, and the functor $\text{ob}: \text{Cat} \to \text{Set}$ which takes categories to the set of their elements is represented by the terminal category $1$, which has one element.
5. The [[Sierpinski Space]] $S$ represents the [[Open Set]] functor. The natural bijection associates continuous functions $X \to S$ with the preimages open sets.
6. The functor $\text{Hom}(- \times A, B): \text{Set}^{\text{op}} \to \text{Set}$ which sends a set $X$ to the set of functions $X \times A \to B$ is represented by the set $B^A$ of functions from $A$ to $B$. I.e. there is a natural bijection between functions $X \times A \to B$ and functions $X \to B^A$. Computer scientists call this currying.

## The Yoneda Lemma

One of the most prevalent uses of the idea of a representable functor is in [[The Yoneda Lemma]], which states that a set-valued functor $F$ on a locally-small category $C$ obeys
$$
\text{Hom}(C(c, -), F) \cong Fc
$$
for all $c \in C$.

## Initial Elements, Terminal Elements, and the Category of Elements

A covariant set-valued functor is representable if and only if its [[Category of Elements]] has an initial object, and a contravariant set-valued functor (a [[Pre-Sheaf]]) is representable if and only if its category of elements has a terminal object.