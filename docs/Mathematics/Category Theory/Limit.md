
# Limit (Category Theory)

A limit is the [[Universal Property|universal]] [[Cone|cone]] over a [[Diagrams (Category Theory)|diagram]]. They are closely related to the concept of a [[Colimit|colimit]].

## The Category of Cones

Let $F: J \to C$ be a diagram of shape $J$ over $C$. There exists a [[Functor|functor]] $\text{Cone}(-, F) \equiv \text{Hom}(\Delta(-), F): C^{\text{op}} \to \text{Set}$. This is to say, a functor which maps the [[Opposite Category|opposite category]] of $C$ to [[The Category of Sets|the category of sets]] by mapping each element $c \in C$ to the set of [[Natural Transformation|natural transformations]] between the [[Constant Diagram Functor|constant functor]] at $c$ to $F$. That is to say, this functor maps each element $c \in C$ to the set of cones with summit $c$ over the diagram $F$. Likewise, morphisms in $C$ are mapped to morphisms which take cones with one summit to those with another summit, over the same diagram of interest $F$.

There are two ways to think about a universal cone: either as a [[Representable Functor|representation]] for such a functor, or as a [[Terminal Object|terminal object]] in its [[Category of Elements|category of elements]].

### Representations of the Cone Functor

By the [[The Yoneda Lemma|the Yoneda Lemma]], a representation for $\text{Cone}(-, F): C^{\text{op}} \to \text{Set}$ can be defined by an object $\lim F \in C$ together with the universal cone $\lambda: \Delta \lim F \Rightarrow F$, which is called the limit cone. These define a natural isomorphism $C(-, \lim F) \cong \text{Cone}(-, F)$. 

### The Category of Elements of the Cone Functor

As with any functor, we can define the category of elements of this functor, $\int \text{Cone}(-, F)$, which we call the category of cones. Because this is a [[Hom-Set|hom-set functor]], this category of elements is a [[Slice Category|slice category]]. The elements of this category are pairs $(c, x)$ where $c \in C$ and $x$ is a cone over $F$ with summit $c$.

## Special Examples of Limits and Colimits

There are many special cases for which limits and colimits have particular names due to their use in less abstract branches of mathematics. Here a few examples are provided.

- The limit of a diagram indexed by a discrete category with only identity morphisms is called a [[Product (Category Theory)|product]].
	- In the special case in which the $J$ is the empty category, the product is a terminal object. This is because a cone over an empty diagram is simply an object in the codomain category $C$, and so the category of cones is isomorphic to $C$. Limits are terminal objects in the category of cones, so these products are terminal objects in $C$.
- The limit of a diagram indexed by the [[Parallel Pair Category|parallel pair category]] is called an [[Equalizer|equalizer]].
- Consider the poset category $J$ such that $\text{Ob}(J) = \{ \alpha, \beta, \gamma \}$ and $\text{Mor}(J) = \{ f: \alpha \to \gamma, g: \beta \to \gamma \} \cup \{\text{Identity morphisms}\}$. A diagram indexed by such a category is called a [[Cospan|cospan]], and the (co)limit of a cospan is called a [[Pullback (Category Theory|pullback (pushout)]].

## Limits in the Category of Sets

Let $F: J \to \text{Set}$. A limit of such a diagram is a representation $\text{Set}(X, \lim F) \cong \text{Cone}(X, F)$ of the functor which sends a set $X$ to the set of cones over $F$ with summit $X$. The singleton set $\{1\}$ represents the identity functor on the category of sets, so $\text{Set}(X, \lim F) \cong \lim F$, which implies that $\lim F \cong \text{Cone}(\{1\}, F)$.

A product of sets $A_j$ indexed by some set $j \in J$ is the set of cones over this collection of sets with summit $\{1\}$, which is simply a $J$-tuple of elements in the sets. This is the cartesian product, as expected for the product of sets.

The terminal object in $\text{Set}$ is the set of cones over the empty diagram with summit $\{1\}$. Only one such cone exists, so the terminal object is the singleton set itself.

For two functions $f, g: X \to Y$, their equalizer is the set of maps $\{1\} \to X$ such that $fx = gx$, which is to say, it is the set $\left\{x \in X : f(x) = g(x) \right\}$.