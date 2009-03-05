In a [[closed category]] $C$ (for instance a [[closed monoidal category]]) for any two objects $X,Y$ there is an object $hom(X,Y)$ representing the collection of morphisms from $X$ to $Y$. This is called the **internal hom**, expressing the idea that this the perspective on the collection of morphisms from $X$ to $Y$ from the inside of $C$.

You can distinguish this from the external [[hom-set]] $Hom(x,y)$; however, every closed category is a [[concrete category]], and the external hom is the underlying set of the internal hom.  To be explicit, if $I$ is the unit object of the closed category $C$, then
$$Hom(I,hom(x,y)) \cong Hom(x,y)$$
by a [[natural isomorphism]].  More generally in a [[closed monoidal category]],
$$Hom(a,hom(b,c)) \cong Hom(a \otimes b,c)$$
naturally.

Every closed category may be seen as a category [[enriched category|enriched]] over itself.  Accordingly, an internal hom is a special case of a [[hom-object]].

+-- {: .query}

_[[Ronnie Brown|Ronnie]]_: I have found it convenient in a number of categories to use the convention that if say the set of morphisms is $hom(x,y)$ then the internal hom when it exists is $HOM(x,y)$. In particular we have the exponential law for categories 

$$Cat(x \times y,z) \cong Cat(x,CAT(y,z)).$$ 

Then one can get versions such as $CAT_a(y,z)$ if $y,z$ are objects over $a$. 

Of course to use this the name of the category needs more than one letter. Also it obviates the use of those fonts which do not have upper and lower case, so I have tended to use mathsf, which does not work here! 

How do people like this? Of course, panaceas do not exist.

_Toby_:  I see, that fits with using $\CAT$ as the $2$-category of categories but $\Cat$ as the category of categories.  (But I\'m not sure if that\'s a good thing, since I never liked that convention much.)  I only used 'Hom' for the external hom here since Urs had already used 'hom' for the internal hom.

Most of the time, I would actually use the same symbol for both, just as I use the same symbol for both a group and its underlying set.  Every closed category is a [[concrete category]] (represented by $I$), and the underlying set of the internal hom is the external hom.  So I would distinguish them only when looking at the theorems that relate them, much as I would bother parenthesising an expression like $a b c$ only when stating the associative law.

=--