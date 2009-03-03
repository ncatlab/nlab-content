The notion of a constant morphism in a category generalises the notion of [[constant function]].

+-- {: .num_defn #ConstMorph}
###### Definition
A _constant morphism_ in a category $\mathcal{C}$ is a morphism $c : B \to C$ with the property that for any morphisms $f,g : A \to B$ then $c \circ f = c \circ g$.
=--

Using the two-point set, it is simple to show that the constant morphisms in [[Set]] are precisely the constant functions.  As with $Set$, any morphism which factors through a terminal object is constant but although this is an "if and only if" in $Set$ it need not be in a general category.