In a [[closed category]] $C$ (for instance a [[closed monoidal category]]) for any two objects $X,Y$ there is an object $hom(X,Y)$ representing the collection of morphisms from $X$ to $Y$. This is called the **internal hom**, expressing the idea that this the perspective on the collection of morphisms from $X$ to $Y$ from the inside of $C$.

You can distinguish this from the external [[hom-set]] $Hom(x,y)$.  Note that if $I$ is the unit object of the closed category $C$, then
$$Hom(I,hom(x,y)) \cong Hom(x,y)$$
given by a [[natural isomorphism]].

More generally, if $C$ is an [[enriched category]], you get a [[hom-object]].

 

+-- {: .query}

[[Ronnie Brown|Ronnie]] I have found it convenient in a number of categories to use the convention that if say the set of morphisms is $hom(x,y)$ then the internal hom when it exists is $HOM(x,y)$. In particular we have the exponential law for categories 

$$Cat(x \times y,z) \cong Cat(x,CAT(y,z)).$$ 

Then one can get versions such as $CAT_a(y,z)$ if $y,z$ are objects over $a$. 

Of course to use this the name of the category needs more than one letter. Also it obviates the use of those fonts which do not have upper and lower case, so I have tended to use mathsf, which does not work here! 

How do people like this? Of course, panaceas do not exist.

=--