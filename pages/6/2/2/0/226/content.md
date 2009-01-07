We assume you know the [usual definition](http://en.wikipedia.org/wiki/Vector_space#Definition) of a vector space over a field $k$.

The [[category]] of vector spaces is called [[Vect]], or 
$Vect_k$ if we wish to make the field $k$ explicit.  This category has vector spaces over $k$ as objects, and linear maps between these as morphisms.

Vector spaces over fields are a special case of [[module|modules]] of [[ring|rings]]. A vector space over the field $F$ is just an $R$-module where the ring $R$ happens to be the field $k$, and a linear map between vector spaces is then an $R$-module morphism.  So, the category $Vect_k$ is the same as the category $R Mod$ when $R = k$.  There is a lot of nice abstract stuff to be said about the category $R Mod$ --- see the entry on [[module|modules]].

#Discussion#

_[[Eric Forgy]] says_: Is there a nice _arrow theoretic_ way to define vector spaces?

_[[Urs Schreiber|Urs]] says_: There is comparatively nice abstract nonsense to be said about _rings_. For instance, a [[ring]] is a category with one object [[enriched category|enriched in]] the category of abelian groups. From that starting point the concepts of ring theory develop rather naturally from pure category theoretic reasoning. In particular [[module|modules]] over rings appear naturally.

For some reason this is different when rings are refined to _fields_ and modules to vector spaces. The very concept of a _field_ is somehow not as natural from a category theoretic perspective, or at least I don't see how it is. This problem becomes very manifest when one tries to categorify fields and vector spaces: it is very straightforward to categorify rings and their modules, but their refinement to categorified fields  and vector spaces is harder.

    The remainder of this discussion has been moved to [[field]].

***

_[[Eric Forgy|Eric]] says_: Could you somehow define a vector space as a "degroupoidified" groupoid? That would be pretty.