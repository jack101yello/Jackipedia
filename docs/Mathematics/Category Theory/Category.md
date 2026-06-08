# Category

A category is, in some sense, one of the most general mathematical structures possible. It consists of

1. A collection $\text{ob}(C)$ of objects.
2. A collection $\text{mor}(C)$ of Morphisms, each of which has a source object and a target object.
3. A binary operation $\circ$ on morphisms via which morphisms can be composed.

Additionally, every object $c \in C$ must have at least one [[Endomorphism]] called the identity morphism $id_c$.

## Types and Examples of Categories

### The Size of a Category

A category $C$ for which $\text{ob}(C)$ and $\text{mor}(C)$ are sets is called a small category. If instead these collections are proper classes, $C$ is said to be a large category.

Large categories are often difficult to work with, but not always. A category for which the collection of morphisms between any two objects forms a set (i.e. a [[Hom-Set]]) is called a locally small category.
### Examples of Categories

The numerous and varied examples of categories below serve to demonstrate the ubiquity of category theory and categorical thinking.

#### Examples of Small Categories

There are many useful examples of small categories.

| Category                                                   | Objects                       | Morphisms                     |
| ---------------------------------------------------------- | ----------------------------- | ----------------------------- |
| Partially-Ordered Sets                                     | Numbers (perhaps the reals)   | $\leq$                        |
| The Path Category of a Graph                               | Graph Vertices                | Paths                         |
| The Action Groupoid $G // X$ of a Group $G$ over a set $X$ | $x \in X$                     | $gx$ for $g \in G$            |
| Programming Languages                                      | n-tuples of Datatypes         | Functions                     |
| The Fundamental Groupoid                                   | Points in a Topological Space | [[Homotopy Classes]] of Paths |

#### Examples of Large Categories

There are also many useful examples of large categories, some of which are locally small.

| Category      | Objects            | Morphisms                |
| ------------- | ------------------ | ------------------------ |
| $\text{Grp}$  | Groups             | Homomorphisms            |
| $\text{Top}$  | Topological Spaces | Homeomorphisms           |
| $\text{Vect}$ | Vector Spaces      | Linear Maps              |
| $\text{Set}$  | Sets               | Functions                |
| $\text{Diff}$ | Smooth Manifolds   | Differentiable Functions |

#### Further Examples of Categories

There are many other common examples of categories:

- A category with one element (though perhaps multiple endomorphisms) is called a [[Monoid]].
- The category $\text{Cat}$ is the category of categories, with objects categories and morphisms [[Functor]]s.
- Every category $C$ admits an [[Opposite Category]] $C^{\text{op}}$, with the same objects, both with morphisms oriented the other direction.

## The Representation of Groups as Categories

There are multiple different ways to represent a group $G$ as a category. The most common is as a monoid, in which case the category is denoted $\text{B}G$. This category has one element $G$, and its endomorphisms are the group elements $g \in G$, with the identity element serving as the identity endomorphism.

Groups themselves collectively form the category $\text{Grp}$, with morphisms homomorphisms. (This is, in fact, the origin of the name "morphism".) Furthermore, a group's action on a set forms an action groupoid, which itself forms a category. For instance, the Rubik's Cube can be though of as a category in which the objects are the states of the cube and the morphisms are rotations of the faces.