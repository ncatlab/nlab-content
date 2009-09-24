If $S\subset R$ is a left [[Ore set]] in a monoid (or a ring) $R$, then we call the pair $(j,S^{-1}R)$ where $j:R\to S^{-1}R$ is a morphism of monoids (rings) the __left Ore localization__ of $R$ with respect to $S$ if it is the  universal object in the category $C = C(R,S)$
whose objects are the pairs $(f,Y)$ where $f : R \rightarrow Y$ is a morphism of rings from $R$ into a
ring $Y$ such that the image $f(S)$ of $S$ consists of units (=multiplicatively invertible elements), and
the morphisms $\alpha : (f,Y) \rightarrow (f',Y')$
are maps of rings $\alpha : Y \rightarrow Y'$ such that $\alpha \circ f = f'$.

The definition of $C$ makes sense even if $S\subset R$ is not left Ore; the universal object in $C$ may then exist when $S$ is not left Ore, for example this is the case when $S$ is right Ore, while not left Ore. In fact, the universal object is a left Ore localization (i.e. $S$ is left Ore) iff it lies in the full subcategory $C^l$ of $C$ whose objects $(f,Y)$
satisfy two additional conditions:

(i) $f(S)^{-1}f(R) = \{(f(s))^{-1}f(r)\,|\, s \in S, r\in R\}$ is a subring in $Y$,

(ii) $ker\,f = I_S$. 

Hence $(j,S^{-1}R)$ is universal in $C^l$, and that characterizes it, but the universality in $C$, although not characteristic, appears to be more useful in practice.

For every left Ore set $S\subset R$ in a monoid or ring $R$, the left Ore localization exists and it can be defined as follows. As a set, $S^{-1}R := S\times R/\sim$, where
$\sim$ is the following relation of equivalence:
\[ (s,r) \sim (s',r') \,\,\Leftrightarrow\,\,
(\exists \tilde s\in S \,\,\exists \tilde{r}\in R) \,\,
(\tilde{s}s' = \tilde{r}s\,\,and\,\,\tilde{s}r' = \tilde{r}r).\]
A class of equivalence of $(s,r)$ is denoted $s^{-1}r$ and
called a left fraction. The multiplication is defined by
$s_1^{-1}r_1\cdot s_2^{-1}r_2 = (\tilde{s}s_1)^{-1} (\tilde{r}r_2)$ where
$\tilde{r} \in R, \tilde{s} \in S$
satisfy $\tilde{r}s_2 = \tilde{s}r_1$
(one should think of this, though it is not yet
formally justified at this point, as
$s^{-1}\tilde{r} = r_1 s_2^{-1}$, what enables to put inverses one
next to another and then the multiplication rule is obvious).
If the monoid $R$ is a ring then we can extend the addition to $S^{-1}R$ too. Suppose we are given two fractions
with representatives $(s_1,r_1)$ and $(s_2,r_2)$. Then by the left Ore
condition we find $\tilde{s} \in S$, $\tilde{r}\in R$ such that
$\tilde{s} s_1 = \tilde{r} s_2$. The sum is then defined
\[ s_1^{-1} r_1 + s_2^{-1} r_2 \,:=\,
 (\tilde{s}s_1)^{-1} (\tilde{s}r_1 + \tilde{r}r_2) \]
It is a long and at points tricky to work out all the details of this definition. One has to show that $\sim$ is indeed relation of equivalence, that the operations are well defined, and that $S^{-1}R$ is indeed
a ring. Even the commutativity of the addition needs work (there is an alternative definition of addition in which $\tilde{s}$ above is not required to be in $S$ but the  product $\tilde{s}r_1$ is in $S$; this approach is manifestly commutative but it has some other drawbacks).
At the end, one shows that the map $j = j_S : R \rightarrow S^{-1}R$ given by $i(r) = 1^{-1}r$ is a homomorphism of rings, which is 1-1 iff the 2-sided ideal $I_S = \{ n \in R \,|\,\exists s \in S,\, sn = 0\}$ is zero.

Basic property of Ore localization is flatness: $S^{-1}R$ is flat $R$-bimodule. 
The left Ore localization $j : R\to S^{-1}R$ induced a flat localization functor for the category of left $R$-modules or the category of right $R$-modules. The localization functor is the extension of scalars along $l_S: R\to S^{-1}R$, that is (in the case of left $R$-modules) $M\mapsto S^{-1}R\otimes_R M$ is the flat localization functor $Q^*_S:{}_R Mod\to {}_{S^{-1}R}Mod$ and the restriction of scalars is its right adjoint $Q_{S*}$ which is fully faithful and it has its own right adjoint (the localization functor is affine).

* K. R. Goodearl, Robert B. Warfield, _An introduction to noncommutative Noetherian rings_, London Math. Soc. Student Texts __16__ (1st ed,), 1989, xviii+303 pp.; or __61__ (2nd ed.), 2004, xxiv+344 pp.

* Z. &#352;koda, _Noncommutative localization in noncommutative geometry_,  London Math. Society Lecture Note Series 330 ([pdf](http://www.maths.ed.ac.uk/~aar/books/nlat.pdf)), ed.  A. Ranicki; pp. 220--313, <a href="http:arxiv.org/abs/math.QA/0403276">math.QA/0403276</a>.