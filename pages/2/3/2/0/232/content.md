#The Idea#

The idea of an enriched category is that we take the definition of [[small category]] and replace the [[homset|homsets]] by objects in some [[monoidal category]] $K$.  So, a _category enriched over $K$_, say $C$, has a collection $C_0$ of objects and for each pair $x,y \in C_0$, a 'hom-object' 
$$ hom(x,y) \in K .$$
We then mimic the usual definition of category.  In particular, composition is a morphism in $K$:
$$ \circ : hom(y,z) \otimes hom(x,y) \to hom(x,z)  $$
where $\otimes$ is the tensor product in $K$.

We may similarly define a _functor enriched over $K$_
and a _natural transformation enriched over $K$_.

#The Details#

The details are an exercise for future readers of this page.   If you get stuck, try Max Kelly's book, cited in the page on [[enriched category theory]].