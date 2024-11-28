
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

…

## Definition

…

## Universal commutativity

In a locally $\lambda$-presentable [[(∞,1)-category]], $\lambda$-filtered (∞,1)-colimits commute with $\lambda$-small (∞,1)-limits.

In particular, in a locally finitely presentable [[(∞,1)-category]], filtered (∞,1)-colimits commute with finite (∞,1)-limits.

In an algebraic (∞,1)-category, i.e., one that is equivalent to the category of finite product-preserving functors from a small (∞,1)-category with finite products to the (∞,1)-category of spaces,
sifted (∞,1)-colimits commute with finite (∞,1)-products.

## Special commutativity: model ∞-categories

From a [MathOverflow answer](https://mathoverflow.net/questions/287091/why-do-we-need-model-categories/287234#287234):

Model categories provide a powerful framework for commuting (homotopy) limits and colimits,
and, more generally, for commuting left adjoint functors and (homotopy) limits,
as well as right adjoint functors and (homotopy) colimits.
(In what follows, I omit the adjective “homotopy” before limits and colimits.)

In finitely presentable ∞-categories filtered colimits commute with finite limits
and in finitely presentable ∞-categories with a set of compact projective generators
sifted colimits commute with finite products.
However, many other situations of interest are not covered by such statements.
For instance, one might want to commute a sifted colimit past an infinite product, a pullback,
or a cosifted limit (e.g., a cosimplicial totalization).
One might also want to commute sifted colimits past finite products
in ∞-categories that do not have a set of compact projective generators,
e.g., the ∞-category of small ∞-categories.

In all such situations the relevant statement is false at least for some diagrams,
so whatever criterion we devise must analyze the specific diagrams at question.
This is precisely what model categories achieve.

For example, one might want to commute $K$-indexed colimits (for some small diagram $K$)
past some right adjoint functor $F: C\to B$.
(For instance, one can take $F$ to be 
$$lim_L: Fun(L,B)\to B,$$
the limit functor for $L$-indexed diagrams,
which will allows us to commute $K$-indexed colimits past $L$-indexed limits.)

We would like to devise a condition on a diagram $D: K\to C$ that would guarantee that the canonical
comparison map 
$$colim_K F(D) \to  F(colim_K D)$$
is an equivalence in the ∞-category $B$.
This is achieved by the following creative procedure.
First, consider the relative ∞-category (i.e., ∞-category equipped with a class of maps (weak equivalences) closed under composition)
$Fun(K,C)$ whose weak equivalences are created by the functor $colim_K$ (i.e., a natural transformation of functors $K\to C$
is a weak equivalence if its $K$-colimit is an equivalence in the ∞-category $C$).
The ∞-category $Fun(K,B)$ is turned into a relative ∞-category in the same way.
The functor 
$$Fun(K,F): Fun(K,C)\to Fun(K,B)$$
is a functor between ∞-categories that need not preserve weak equivalences.

Now comes the (potentially) creative part: equip the relative ∞-categories $Fun(K,C)$ and $Fun(K,B)$
with model structures such that $Fun(K,F)$ is a right Quillen functor.
In many situations of interest this can be done immediately using existing tools.

Our criterion now says that if $D: K\to C$ is a _fibrant_ diagram,
then the comparison map 
$$colim_K F(D) \to  F(colim_K D)$$
is an equivalence in the ∞-category B,
i.e., the colimit of $D$ over $K$ commutes with $F$.
Different choices of model structures give us different criteria.

For instance, one can take $K=\Delta^{op}$, $B=spaces$ (alias ∞-groupoids),
$C=Fun(L,B)$ (i.e., $L$-indexed diagrams of spaces)
and 
$$F=lim_L: Fun(L,B)\to B,$$
the $L$-indexed limit functor,
where $L$ can be taken to be the pullback diagram or the infinite discrete category
and the model structure can be taken to be the projective model structure.
In this case we obtain a criterion for commuting
$\Delta^{op}$-indexed colimits past $L$-indexed limits.
This recovers, for example, the traditional methods
for computing homotopy pullbacks of simplicial sets (replace one of the legs by a fibration),
infinite homotopy products of simplicial sets (fibrantly replace all terms), etc.

There are many variations on the above theme, for instance,
one can consider *weighted* limits (in the sense of enriched category theory)
and then derive the limit functor with respect to both the functor and the weight,
which yields even more powerful computational tools etc.

Many classical results on model categories fit in the above framework.
For instance, if $M$ is a simplicial model category,
$X$ is a cofibrant object,
and $Y$ is a fibrant object,
then the simplicial mapping space $Map(X,Y)$ from $X$ to $Y$
computes the mapping space in the ∞-localization of $M$ with respect to its weak equivalences.
We can fit this in the above framework by taking
$$F=Map(-,Y): Fun(\Delta^op,M)\to Fun(\Delta^op,Spaces),$$
and observing that a cofibrant object $X$ has a cofibrant cosimplicial resolution $X\otimes\Delta^n$.

Textbook accounts include Chapter 7 of [Cisinski](#Cisinski).

## Related concepts

* [[commutativity of limits and colimits]]

* [[π-Kan condition]]

## References

### Universal commutativity

* [[Jacob Lurie]], *[[Higher Topos Theory]]* (2009)

### Special commutativity

On conditions that [[base change]] via [[homotopy pullback]] commutes with [[geometric realization of simplicial topological spaces|realization]] (cf. *[[π-Kan condition]]* and [this Prop.](geometric+realization+of+simplicial+topological+spaces#SufficientConditionsForRealizationToPreserveHomotopyPullback)):

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], _Homotopy theory of $\Gamma$-spaces, spectra, and bisimplicial sets_, Springer Lecture Notes in Math. **658** Springer (1978) 80-130 &lbrack;[pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/bousfield-friedlander.pdf), [[BousfieldFriedlanderSpectra.pdf:file]]&rbrack;

* {#Lurie11} [[Jacob Lurie]], *Simplicial spaces*, Lecture 7 of: *[Algebraic L-theory and Surgery](https://www.math.ias.edu/~lurie/287x.html)* (2011) &lbrack;[pdf](https://www.math.ias.edu/~lurie/287xnotes/Lecture7.pdf)&rbrack;

* {#Rezk14} [[Charles Rezk]], *When are homotopy colimits compatible with homotopy base change?* (2014) &lbrack;[i-hate-the-pi-star-kan-condition.pdf](https://faculty.math.illinois.edu/~rezk/i-hate-the-pi-star-kan-condition.pdf), [[RezkHomotopyColimitsBaseChange.pdf:file]]&rbrack;

* [[Jacob Lurie]], §A.5, esp. Def. A.5.2.1, Thms. A.5.3.1, A.5.4.1, A.5.6.1 in  *[[Spectral Algebraic Geometry]]* (2018) &lbrack;[pdf](https://math.harvard.edu/~lurie/papers/SAG-rootfile.pdf)&rbrack;

{#ForATreatment} For a treatment without ∞-categories, see also [BEBP19, Def. 3.2, Ex. 3.10, Thm. 3.17](#BEBP19) below.

An even larger class of maps of so-called _weak Kan fibrations_ is studied in Section 3 of

* {#BEBP19} [[Daniel Berwick-Evans]], [[Pedro Boavida]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_, Algebraic & Geometric Topology  &lbrack;[arXiv:1912.10544](https://arxiv.org/abs/1912.10544)&rbrack;  

The general theory of [[model (∞,1)-categories]] that allows one to commute homotopy colimits past homotopy limits is developed in a series of papers by Aaaron Mazel-Gee:

* [[Aaron Mazel-Gee]], *Model ∞-categories I: some pleasant properties of the ∞-category of simplicial spaces* &lbrack;[arXiv:1412.8411](https://arxiv.org/abs/1412.8411)&rbrack;
 
* [[Aaron Mazel-Gee]], *Model ∞-categories II: Quillen adjunctions*, New York Journal of Mathematics **27** (2021) 508-550.  &lbrack;[arXiv:1510.04392](https://arxiv.org/abs/1510.04392), [nyjm:27-21](http://nyjm.albany.edu/j/2021/27-21.html)&rbrack;

* [[Aaron Mazel-Gee]], *Model ∞-categories III: the fundamental theorem*, New York Journal of Mathematics **27** (2021) 551-599 &lbrack;[arXiv:1510.04777](https://arxiv.org/abs/1510.04777), [nyjm:27-22](http://nyjm.albany.edu/j/2021/27-22.html)&rbrack;

and in 

* {#Cisinski} [[Denis-Charles Cisinski]], Chapter 7 of: *[[Higher Categories and Homotopical Algebra]]*, Cambridge Studies in Advanced Mathematics **180**, Cambridge University Press (2019) &lbrack;[doi:10.1017/9781108588737](https://doi.org/10.1017/9781108588737), [pdf](https://cisinski.app.uni-regensburg.de/CatLR.pdf)&rbrack;

In particular, see Propositions 7.5.5, 7.7.4, 7.7.5.

[[!redirects commutativity of homotopy colimits and limits]]


