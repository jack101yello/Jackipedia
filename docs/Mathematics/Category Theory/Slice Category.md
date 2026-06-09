# Slice Category

The slice category for a [[Category]] $C$ under an element $c \in C$ is the [[Category of Elements]] of the [[Hom-Set]] functor $C(c, -)$, denoted $c/C$. Likewise, the slice category of $C$ over $c$, $C/c$, is the category of elements of $C(-, c)$. The former is often called an undercategory, whereas the latter is called an overcategory.

Let $C$ be a category and $c \in C$. The slice category $c/C$ is a category such that:

- Objects are morphisms in $C$ with domain $c$.
- A morphism from $f: c \to x$ to $g: c \to y$ is a morphism $h: x \to y$ such that $g=hf$ such that the [[Triangle Diagram]] commutes. $h$ is said to be a morphism under $c$.

## Examples of Slice Categories

1. Let $\text{Pos}$ be the [[Poset Category]] on $\mathbb{R}$, and let $x \in \mathbb{R}$. Then $x/\text{Pos}$ is the smaller poset category with $x$ as its minimum element, and $\text{Pos}/x$ is the smaller poset category with $x$ as its maximum element.
2. Let $X$ be a topological space. Then the objects in $\text{Top}/X$ are pairs $(Y, \phi)$ where $Y$ is a topological space and $\phi: Y \to X$ is a continuous map, and morphisms are continuous maps $f: Y \to Z$ where $Y, Z$ are topological spaces such that the structure over $X$ is preserved.