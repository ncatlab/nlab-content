## Idea ## 

A club is a particular sort of [[doctrine]] or monad on categories, one which encapsulates the following phenomenon: that to describe the free structured categories (i.e., free algebras), it is often sufficient to describe the free algebra on one generator, with general free algebras being describable as certain wreath products involving the free algebra on one generator. Examples of this phenomenon include the monad for monoidal categories and the monad for closed symmetric monoidal categories. 

Clubs were introduced by Max Kelly, and are akin in spirit to [[operad|operads]]. 

## Wreath products ## 

Let $Cat$ denote the category of small categories, and let $CAT$ denote the category of locally small categories. We define a functor 

$$\int: CAT/Cat \times CAT \to CAT$$ 

called **wreath product**. At the object level, 

$$(U: C \to Cat) \int D$$ 

is the category whose objects are pairs $(c \in Ob(C), F: U(c) \to D)$, and where morphisms $(c, F) \to (c', F')$ are pairs $(f: c \to c', \phi: F \to F' \circ U(f))$, in which $\phi$ is a [[natural transformation]] valued in $D$. 