# Opposite Category

For a [[Category]] $C$, its opposite category $C^{\text{op}}$ is a category whose objects are the same as the objects in $C$, but whose morphisms have their directions reversed. That is to say, for every morphism $f: c \to c'$ in $C$, there exists a morphism $f^{op}: c' \to c$ in $C^{\text{op}}$.

There is no sense in which one given category is an opposite category and another is not, as every category is the opposite category of its opposite category. However, in practice it is generally clear which category is more natural, and which category should be regarded as its opposite.

## Contravariant Functors

A [[Functor]] is said to be a [[Contravariant Functor]] if its (co)domain is an opposite category. That is to say, a functor $F: C^{\text{op}} \to D$ not only maps the elements and morphisms of $C$ to elements and morphisms of $D$, but reverses the directions of arrows in doing so: if $f: c \to c'$ in $C$, then $Ff: Fc' \to Fc$ in $D$.