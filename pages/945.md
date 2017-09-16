##Idea##

A subcategory $S$ of category $C$ is dense if every object $c$ of $C$ is a colimit of a diagram of objects in $S$, in a canonical way. 

##Definition##
A functor $i:S\to C$ is _dense_ if every object $C$ is the 
vertex of the following colimit over the comma category $(i/c)$:
$$
\mathrm{colim}((i/c)\stackrel{\mathrm{pr}_S}{\longrightarrow} S \stackrel{i}{\to} C)
$$

##Characterization##
 
Proposition. A functor is dense iff it is (left) adequate in the sense of Isbell i.e. if the corresponding [[nerve|nerve functor]] is fully faithful. 

##Warning##

There is a different notion of a dense subcategory, often used in [[shape theory]], which has a bit of the same spirit. A full subcategory $D\subset C$ is
dense in this second sense, if every object in $C$ admits a $D$-expansion. 

A $D$-expansion of an object $X$ in $C$ is a morphism
$X\to \mathbf{X}$ in $\mathrm{pro}C$ such that $\mathbf{X}$
is in $\mathrm{pro}D$ and $X$ is the rudimentary system (constant inverse system) corresponding to $X$; moreover one asks that the morphism is universal among all such morphisms $X\to\mathbf{Y}$. 

Given a dense subcategory $D\subset C$ one defines
an abstract shape category $\mathrm{Sh}(C,D)$ which has the same objects as $C$, but the morphisms are the equivalence classes of morphisms in $\mathrm{pro}D$ of $D$-expansions.