
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


[[!redirects theory of $\mathbb{T}-model homomorphisms]]
[[!redirects theory of T-model homomorphisms]]
[[!redirects theory of homomorphism]]

#Contents#
* table of contents
{:toc}

##Idea
For any [[geometric theory]] $\mathbb{T}$ there exists a geometric theory $\mathbb{T}^2$, the **theory of $\mathbb{T}$-model homomorphisms**, whose models in a [[Grothendieck topos]] $\mathcal{E}$ are precisely the homomorphisms between $\mathbb{T}$-models in $\mathcal{E}$.

## Definition

Let $\mathbb{T}$ be a [[geometric theory]] over the [[signature]] $\Sigma$.

Let $\Sigma^2$ be the signature containing a pair of new sort symbols $X^0$, $X^1$ and a new function symbol $f_X:X^0\to X^1$ for any sort symbol $X$ in $\Sigma$, as well, as pairs $g^0:X_1^0\times\dots\times X_n^0\to Y^0$, $g^1:X_1^1\times\dots\times X_n^1\to Y^1$ of new functions symbols (resp. pairs $R^0\rightarrowtail X_1^0\times\dots\times X_n^0$, $R^1\rightarrowtail X_1^1\times\dots\times X_n^1$ of new relation symbols) for any function symbol $g:X_1\times\dots\times X_n\to Y$ (resp. relation symbol $R\rightarrowtail X_1\times\dots\times X_n$) in $\Sigma$.

The **theory of $\mathbb{T}$-model homomorphisms** is the theory $\mathbb{T}^2$ over the signature $\Sigma^2$ with the following sequents:

 A pair of sequents $\varphi^0\vdash \psi^0$, $\varphi^1\vdash \psi^1$ for any sequent $\varphi\vdash \psi$ in $\mathbb{T}$ where the new sequents result from replacing the function and relation symbols in $\varphi\vdash \psi$ with their 0-indexed, resp. 1-indexed pendants where necessary[^prop]. Plus a sequent

:$\top\vdash f_Y(g^0(x_1,\dots,x_n))=g^1(f_{X_1}(x_1),\dots,f_{X_n}(x_n))$

resp.

:$R^0(x_1,\dots,x_n)\vdash R^1(f_{X_1}(x_1),\dots,f_{X_n}(x_n))$

for any pair $g^0$, $g^1$ of function symbols in $\Sigma^2$ corresponding to $g:X_1\times\dots\times X_n\to Y$ in $\Sigma$ (in case $n=0\,$, the sequent reads $\top\vdash f_Y(g^0)=g^1\,$), resp. any pair $R^0$, $R^1$ of relation symbols in $\Sigma^2$ corresponding to $R\rightarrowtail X_1\times\dots\times X_n$ in $\Sigma$ (in case $n=0\,$, the sequent reads $R^0\vdash R^1\,$).

[^prop]:  It is understood that variables and contexts are updated with the new sorts e.g. the sequent $\top\vdash_{x:S} x=x$ yields two sequents $\top\vdash_{x:S^0} x=x$ and $\top\vdash_{x:S^1} x=x$ and $\top\vdash \big (\forall x:S\big ) x=x$ yields $\top\vdash \big (\forall x:S^0\big ) x=x$ and $\top\vdash \big (\forall x:S^1\big ) x=x$ etc. In case, the sequent $\varphi\vdash\psi$ contains nothing to update (e.g. the sequent $\top\vdash\bot$) one just takes the old sequent as the "new pair".

## Properties

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[Grothendieck topos]]. Then

$${\mathbb{T}^2}\text{-}Mod(\mathcal{E})=\mathbb{T}\text{-}Mod(\mathcal{E})^2=\mathbb{T}\text{-}Mod(\mathcal{E}^2)\quad.$$
=--

Cf. Johnstone ([1977](#J77), p. 203; [2002](#J02), p.425), Mac Lane-Moerdijk ([1994](#MM94), ex.X.5 p.572).

Note that the second equality determines the class of $\mathbb{T}$-model homomorphisms once the $\mathbb{T}$-models in the arrow categories $\mathcal{E}^2$ are known.

**Remark**:
This e.g. precludes the existence of geometric theories $\mathbb{T}^{op}$ or $\mathbb{T}^\times$ with the property that, given a geometric theory $\mathbb{T}$, the category of models ${\mathbb{T}^{op}}\text{-}Mod(\mathcal{E})$ and ${\mathbb{T}^{\times}}\text{-}Mod(\mathcal{E})$ coincide with the [[opposite category]] ${\mathbb{T}}\text{-}Mod(\mathcal{E})^{op}$ or the [[twisted arrow category]] ${\mathbb{T}}\text{-}Mod(\mathcal{E})^\times$ for any [[Grothendieck topos]], respectively. In particular, since the (geometric) theory of morphisms $\mathbb{O}^2$ (see the examples below) assigns the [[arrow category]] $\mathcal{E}^2$ as category of models to a Grothendieck topos $\mathcal{E}$ no geometric theory can assign all Grothendieck toposes $\mathcal{E}$ their [[twisted arrow category]] $\mathcal{E}^\times$ as category of models because the class of models coincides with the class of models for the theory of morphisms. $\qed$


Since $\mathcal{E}^2=\mathcal{E}\times Set^2$ in general and the [[Sierpinski topos]] $Set^2$ is [[exponentiable topos|exponentiable]], one gets

$${\mathbb{T}^2}\text{-}Mod(\mathcal{E})=\mathbb{T}\text{-}Mod(\mathcal{E}^2)=Hom(\mathcal{E}^2,Set[\mathbb{T}])=Hom(\mathcal{E}\times Set^2, Set[\mathbb{T}])=Hom(\mathcal{E},Set[\mathbb{T}]^{(Set^2)})$$

or in other words

+-- {: .num_prop}
###### Corollary

The [[classifying topos]] for the theory $\mathbb{T}^2$ of $\mathbb{T}$-model homorphisms is $Set[\mathbb{T}^2]= Set[\mathbb{T}]^{(Set^2)}$.
=--



**Remark**:
It is worthwhile to muse a bit how "squaring" fares as a theory operator with respect to the various subdoctrines of [[geometric logic]]:
since it does not introduce logical operators like infinitary disjunctions or quantifiers unless the operators were already present in $\mathbb{T}$, one sees that the formats of the more expressive subdoctrines like Horn, [[regular logic|regular]], and [[coherent logic]] are respected by the passage to $\mathbb{T}^2$.
Also, the square of a [[localic topos|propositional theory]] i.e. one over a signature lacking sort symbols, is again propositional - this implies e.g. via the above corollary that the exponentiation of a [[localic topos]] by $Set^2$ is again a localic topos.
The order sensitive subdoctrines like [[essentially algebraic theory|cartesian]] or [[disjunctive logic]] are also respected.
One case where squaring does not preserve the subdoctrine is [[Lawvere theory|1-sorted algebraic logic]] since then $\mathbb{T}^2$ is necessarily 2-sorted. $\qed$

By an observation of Hébert ([2010](#H10), p.1), the finitely presentable objects in arrow categories $\mathcal{K}^2$, are precisely the morphisms between finitely presentable objects in $\mathcal{K}$ whence, denoting the subcategory of finitely presentable models of a theory $\mathbb{T}$ in a topos $\mathcal{E}$ by $\mathbb{T}\text{-}Mod_{fp}(\mathcal{E})$ one has

$$\mathbb{T}^2\text{-}Mod_{fp}(\mathcal{E})=\mathbb{T}\text{-}Mod_{fp}(\mathcal{E})^2\;.$$

But since classifying toposes of cartesian theories are given by the presheaf toposes on the opposite of the category of their finitely presentable models in $Set$ (cf. Johnstone [2002b](J02b), p. 891) one has

+-- {: .num_prop}
###### Proposition

Let $\mathbb{T}$ be a [[essentially algebraic theory|cartesian theory]]. Then the theory $\mathbb{T}^2$ of $\mathbb{T}$-model homorphisms is cartesian and its [[classifying topos]] is $Set[\mathbb{T}^2]=Set^{\mathbb{T}^2\text{-}Mod_{fp}(Set)}=Set^{(\mathbb{T}\text{-}Mod_{fp}(Set)^2)}=\big (Set^{\mathbb{T}\text{-}Mod_{fp}(Set)}\big)^{(Set^2)}=Set[\mathbb{T}]^{(Set^2)}$.
=--

For an easy application of this result see at the theory $\mathbb{O}$ of objects in the examples below!

## Examples

* Let $\mathbb{T}^\emptyset_\emptyset$ and $\mathbb{T}^\emptyset_1$ be the [[empty theory]], resp., the inconsistent theory, over the empty signature. Then $\mathbb{T}^{\emptyset 2}_\emptyset=\mathbb{T}^\emptyset_\emptyset$ and $\mathbb{T}^{\emptyset 2}_1=\mathbb{T}^\emptyset_1$ in accordance with the fact that these theories have only empty models whence all model homomorphisms are [[identity|identity morphisms]] of empty models. In other words, squaring theories obeys the laws of arithmetic at 0 and 1. 

* Let $\mathbb{O}$ be the [[theory of objects]] i.e. the theory with no sequents over the signature with one sort symbol $O$. Then $\mathbb{O}^2$ is the theory with no sequents over the signature with two sort symbols $O^0$, $O^1$ and a function symbol $f_O:O^0\to O^1$. Clearly, its models in a Grothendieck topos $\mathcal{E}$ are the morphisms of $\mathcal{E}$ and, accordingly, $\mathbb{O}^2$ is called the **theory of morphisms**.

  It is the [[exponentiable topos|dual theory]] of the theory classified by the [[Sierpinski topos]] $Set^2$, or in other words, its [[classifying topos]] called the _morphism classifier_ (cf. Johnstone [1977](#J77), p.184; [2002](#J02), p.426) is
$$ Set[\mathbb{O}^2]=Set[\mathbb{O}]^{Set^2}=(Set^{FinSet})^{Set^2}=Set^{(FinSet^2)}\quad .$$

  The _generic morphism_ is given by the [[natural transformation]] $\eta\,:\,\mathbf{O}\circ dom\to\mathbf{O}\circ cod$ with $\mathbf{O}$ the _generic object_ i.e. the inclusion functor $FinSet\hookrightarrow Set$, and $dom\,:\,FinSet^2\to FinSet\, ,\, (X\to Y)\mapsto X$ the domain projection functor, and $cod\,:\,FinSet^2\to FinSet\,,\, (X\to Y)\mapsto Y$ the codomain projection functor, with components $\eta_{(X\to Y)}=\mathbf{O}(X\to Y)$.

* Let $\mathbb{K}$ be the [[theory of categories]] (e.g. Johnstone [1977](#J77), p.202) whose models in a [[Grothendieck topos]] $\mathcal{E}$ are the [[internal category|internal categories]] $\mathbf{C}\in cat(\mathcal{E})$. Then $\mathbb{K}^2$ is the **theory of functors**. $\mathbb{K}$ likely being the most famous cartesian theory, one has $Set[\mathbb{K}^2]=Set^{(\mathbb{K}\text{-}Mod_{fp}(Set)^2)}$.

## The connection to natural homotopy

The [[Sierpinski topos]] $Set^2$ is a connected, locally connected and local topos. As a result of [[Artin gluing]] along $Set\overset{id}{\to}Set$ it has two [[point of a topos|topos points]] (corresponding to the two points of the underlying [[Sierpinski space]]). Whence one can take $Set^2$ as an abstract [[interval object]] for a homotopy theory of Grothendieck toposes correlated with their nature as "generalized spaces" and view, accordingly, the exponential $\mathcal{E}^{Set^2}$ as a path space for $\mathcal{E}$.

(Cf. Beke [2000](#B00), p.11f)

## Related entries

* [[geometric theory]]

* [[theory of objects]]

* [[theory of decidable objects]]

* [[natural homotopy]]

* [[exponentiable topos]]

* [[Sierpinski topos]]

## References

* {#B00}[[Tibor Beke]], _Homotopoi_ , ms. University of Massachusetts Lowell (2000). ([dvi](http://faculty.uml.edu/tbeke/topos.dvi))

* {#H10}[[Michel Hébert]], _Finitely presentable morphisms in exact sequences_ , TAC **24** no.9 (2010) pp.209-220. ([abstract](http://tac.mta.ca/tac/volumes/24/9/24-09abs.html))

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014)

* {#J02a}[[Peter Johnstone]], _Sketches of an Elephant vol.1_ , Oxford UP 2002. 

* {#J02b}[[Peter Johnstone]], _Sketches of an Elephant vol.2_ , Oxford UP 2002. 

* {#JW84}[[André Joyal]], [[Gavin Wraith]], _Eilenberg-Mac Lane Toposes and Cohomology_ , pp.117-131 in Cont. Math. **92** AMS 1984.

* {#MM94} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _Sheaves in Geometry and Logic_ , Springer Heidelberg 1994.

