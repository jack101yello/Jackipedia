# The Yoneda Lemma

The Yoneda Lemma is a central result in [[Category Theory]] which states a natural isomorphism between the [[Hom-Set]] of [[Natural Transformation]]s from a [[Representable Functor]] to its representation and the image of the representing element under the [[Functor]].

More explicitly, let $C$ be a locally-small [[Category]] and $F$ be a [[Set-Valued Functor]] on $C$. Then for any $c \in C$:
$$
\text{Hom}(C(c, -), F) \cong Fc
$$
is natural in both $F$ and $c$.

## The Yoneda Embedding

A corollary to the Yoneda Lemma is the Yoneda embedding. Let $F: C \to \text{Set}^{C^{\text{op}}}$ such that $c \in C$ is mapped to $C(-, C)$. The Yoneda Lemma implies that this embedding is a [[Fully Faithful Functor]]. A more colloquial way of stating this result is that natural transformations between represented functors correspond to morphisms between the representing objects.

## Applications of the Yoneda Lemma

### Row Operations on Matrices

Let $\text{Mat}_R$ be the category whose objects are positive integers and whose morphism $m \to n$ for $n, m \in \text{Mat}_R$ are $n \times m$ matrices whose entries are elements of the unital ring $R$. Composition is defined by matrix multiplication.

The elements in the image of $\text{Mat}_R(-, n)$ are matrices with $n$ rows. The standard row operations of linear algebra define natural [[Endomorphism]]s of $\text{Mat}_R(-, n)$ (where naturality follows from linearity of matrix multiplication). Therefore, every row operation must be definable by left multiplication by a suitable $n \times n$ matrix. The Yoneda Lemma tells us that this matrix is the one gained by applying the row operations to the identity matrix.