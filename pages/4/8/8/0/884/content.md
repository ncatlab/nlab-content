#Whitehead's algebraic homotopy programme


In his talk at the 1950 ICM in Harvard, Henry Whitehead introduced the idea of *algebraic homotopy* theory and said

_"The ultimate aim of algebraic homotopy is to construct a purely
  algebraic theory, which is equivalent to homotopy theory in the same sort of 
  way that 'analytic' is equivalent to 'pure' projective geometry."_

A statement of the aims of 'algebraic homotopy' might thus include the
following homotopy classification problem (from the same source,
J.H.C.Whitehead, (ICM, 1950)):

_Classify the homotopy types of polyhedra, $X$, $Y$, $\ldots$ , by algebraic data._

_Compute the set of homotopy classes of maps, $[X,Y]$, in terms of the
classifying data for $X$, $Y$._

These aims are still valid, but, within the context of these webpages, with the  enlargement of the class of objects of study to
include many other types of spaces, and ultimately $\infty$-[[infinity-groupoid|groupoids]]. 

One may summarise them, optimistically,
by saying that one searches for a nice "algebraic" category $\mathbf{A}$ together 
with a functor or functors

$$\mathbf{F} : \mathbf{Spaces }\rightarrow \mathbf{A}$$

and an algebraically defined notion of 'homotopy' in  $\mathbf{A}$ such that

a) if $X\simeq Y$ in $\mathbf{Spaces}$, then $F(X) \simeq F(Y)$ in  $\mathbf
A$;

b) if $f \simeq g$ in $\mathbf{Spaces}$, then $F(f)\simeq F(g)$ in  $\mathbf
A$,

and $F$ induces an equivalence of [[homotopy category|homotopy categories]]

$$Ho(\mathbf{Spaces}) \simeq Ho(\mathbf{A}).$$

[Here $\mathbf{Spaces}$ is a category, perhaps of topological spaces such as
polyhedra or CW-complexes, but it may be larger than this and may contain the
sort of 'generalised space', [[topos]], etc., used in other contexts such as algebraic
geometry, and, of course, $\infty$-[[infinity-groupoid|groupoids]].]

#More recent developments

*  Baues has developed an approach to Whitehead's basic programme using a mix of [[cofibration category|cofibration categories]] and categories with a particular type of [[cylinder functor]], that he calls [[I-category|I-categories]]. These are treated in separate entries. Cofibration categories are very similar to the dual of K.S. Brown's Abstract homotopy theory, as discussed in [[category of fibrant objects]] and [[BrownAHT]].

*  Ronnie Brown's [[nonabelian algebraic topology]] has developed Whitehead's theory of crossed complexes along the lines suggested by the original papers of Whitehead, but extending that, in particular, using generalisations of van Kampen's theorem. (This is discussed in detail in the entry: [[nonabelian algebraic topology]].)
