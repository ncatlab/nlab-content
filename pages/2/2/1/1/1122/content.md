+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}

##Idea

Much has been said about **inverting a class of morphisms** in a category (see [[localization]]), and there are many different settings in which one wants to, and can, do this. Homotopical algebra is largely concerned with how to compute the [[homotopy category]] so it is locally small. One the other hand, we have [[simplicial localization]] which retains all the homotopy information and returns an $(\infty,1)$-category. 

If we have a 2-category with a notion of weak equivalence, one could localize the underlying 1-category in a way hopefully compatible with the 2-arrows, or extend the result fully into the 2-dimensional setting. In general this will require bicategories, and is the subject of the paper [Etendues and stacks as bicategories of fractions](Pronk96) by [[Dorette Pronk]].

#Definition#

Let $B$ be a  [[bicategory]] with a class $W$ of 1-[[morphism|cells]]. $W$ is said to **admit a right calculus of fractions** if it satisfies the following conditions

* [2CF1.] $W$ contains all equivalences
* [2CF2.]
   * a) $W$ is closed under composition
   * b) If $a\in W$ and a iso-2-cell $a \stackrel{\sim}{\Rightarrow} b$ then $b\in W$
* [2CF3.] For all $w: A' \to A$, $f: C \to A$ with $w\in W$ there exists a 2-commutative square
$$
\begin{matrix}
  P& \stackrel{g}{\to} & A' \\
  v \downarrow&\Rightarrow &\, \downarrow w\\
  C &\underset{f}{\to} & A
\end{matrix}
$$
with $v\in W$.
* [2CF4.] If $\alpha: w \circ f \Rightarrow w \circ g$ is a 2-cell and $w\in W$ there is a 1-cell $v \in W$ and a 2-cell $\beta: f\circ v \Rightarrow g \circ v$ such that $\alpha\circ v = w \circ \beta$. Moreover: when $\alpha$ is an iso-2-cell, we require $\beta$ to be an isomorphism too; when $v'$ and $\beta'$ form another such pair, there exist 1-cells $u,\,u'$ such that $v\circ u$ and $v'\circ u'$ are in $W$, and an iso-2-cell $\epsilon: v\circ u \Rightarrow v' \circ u'$ such that the following diagram commutes:
$$
\begin{matrix}
f \circ v \circ u & \stackrel{\beta\circ u}{\Rightarrow} & g\circ v \circ u \\
f\circ \epsilon \Downarrow \simeq && 
\simeq \Downarrow g\circ \epsilon \\
\\
f\circ v' \circ u' &\underset{\beta'\circ u'}{\Rightarrow}& g\circ v' \circ u'
\end{matrix}
$$

If $B$ is a category, then these axioms reduce to the ones of Gabriel and Zisman for a [[calculus of fractions]].


Given such a setup, Pronk constructs the [[localization]] of $B$ at $W$ and the universal functor sending elements of $W$ to equivalences.



#Example#

Let $S$ be a category with binary products and pullbacks together with a class of [[davidroberts:class of admissible maps|admissible maps]] $E$.

+-- {: .un_theorem}
######Theorem: 
The 2-categories $Cat(S)$ and $Gpd(S)$ of categories and groupoids internal to $S$ admit [[bicategory of fractions|bicategories of fractions]] for the class of $E$-[[davidroberts:weak equivalence|equivalences]].
=--

The resulting localization is equivalent to the bicategory of [[anafunctor|anafunctors]] in $S$. For details, see [Roberts (2012)](#Roberts12).

##Related entries

* [[category of fractions]]
* [[localization]]
* [[bicategory]]
* [[anafunctor]]
* [[orbifold]]
* [[stack]]
* [[étendue]]

##References

* O. Abbad, [[Enrico Vitale|E. M. Vitale]], _Faithful Calculus of Fractions_ , Cah. Top. G&#233;om. Diff. Cat&#233;g. **54** No. 3 (2013) pp.221-239. ([preprint](perso.uclouvain.be/enrico.vitale/FrazioniFedeli.pdf))

* [[Dorette A. Pronk]], _Etendues and stacks as bicategory of fractions_ , Comp. Math. **102** 3 (1996) pp.243-303. ([pdf](http://archive.numdam.org/ARCHIVE/CM/CM_1996__102_3/CM_1996__102_3_243_0/CM_1996__102_3_243_0.pdf))

* [[David Roberts]], _Internal categories, anafunctors and localisations_, TAC **26** (2012) pp.788-829. ([pdf](http://www.tac.mta.ca/tac/volumes/26/29/26-29.pdf)) {#Roberts12}

* M. Tommasini, _A bicategory of reduced orbifolds from the point of view of differential geometry_ , arXiv:1304.6959 (2013). ([pdf](http://arxiv.org/pdf/1304.6959))

* M. Tommasini, _Some insights on bicategories of fractions I_ , arXiv:1410.3990 (2014). ([pdf](http://arxiv.org/pdf/1410.3990))