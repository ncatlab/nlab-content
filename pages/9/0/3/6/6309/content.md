
# The small cardinality selection axiom
* table of contents
{: toc}

## Idea

The small cardinality selection axiom (SCSA) is a weak form of the [[axiom of choice]], which asserts in a certain precise way that choice fails "in at most a [[small set|small]] way".  It was introduced by [[Michael Makkai]] for the study of [[anafunctors]], and thus it also has consequences for the existence of [[stack]] completions.


## Definition

The "global version" of SCSA states:

* The ([[large category|large]]) [[category]] [[Set]] of [[sets]] is [strongly equivalent](/nlab/show/equivalence+of+categories#StrongEquivalence) to a full subcategory of itself, each of whose isomorphism classes contains only a set of objects.

Therefore, we have a [[class]] [[function]] assigning to each set $A$, another set ${\Vert A\Vert}$ and a [[bijection]] $A \cong {\Vert A \Vert}$, in such a way that ${\Vert{-}\Vert}$ takes only set-many values on each isomorphism class in [[Set]].

There is also a "local version" of SCSA which can be stated as follows.  Given a function $f:A\to I$, say that a function $g:B\to J$ equipped with $\phi:J\to I$ is a *local pullback* of $f$ if there is a pair of pullback squares
\begin{tikzcd}
B \ar[d,"g"'] & C \ar[d] \ar[l] \ar[r] \ar[dl,phantom,near start,"\llcorner"] \ar[dr,phantom,near start,"\lrcorner"] & A \ar[d,"f"]\\
J & K \ar[l,"p"] \ar[r,"\phi p"'] & I
\end{tikzcd}
in which $p$ is surjective.  Then the local SCSA states:

* For any $f:A\to I$, the category whose objects are local pullbacks of $f$ and whose morphisms are pullback squares over $I$ has a [[weak limit|weakly terminal object]].

In more set-theoretic language, given a family of sets $(A_i)_{i\in I}$, define a family of sets $(B_j)_{j\in J}$ equipped with $\phi:J\to I$ to be a *local reindexing* of $(A_i)$ if for each $j\in J$ there exists an isomorphism $B_j \cong A_{\phi(j)}$ (but there is not necessarily a function picking out such an isomorphism).  Then the local SCSA states that for any $(A_i)_{i\in I}$ has a local reindexing $(B_j)_{j\in J}$ with $\phi:J\to I$ such that for any other local reindexing $(C_k)_{k\in K}$ with $\psi:K\to I$, there exists a function $\chi : K\to J$ such that $\phi\chi = \psi$ and a specified family of isomorphisms $C_k \cong B_{\chi(k)}$.

To deduce the local version from the global version, given $(A_i)_{i\in I}$ let $J$ be the set of pairs $(i, Y)$ such that $Y = \Vert X\Vert$ for some $X\cong A_i$, with $\phi$ the first projection and $B_{(i,Y)} = Y$.  Then given $(C_k)_{k\in K}$ with $\psi:K\to I$ such that $C_k \cong A_{\psi(k)}$, define $\chi(k) = (\psi(k),\Vert C_k\Vert)$.


## Relationship to other forms of choice

* In the presence of the [[axiom of global choice]] in [[material set theory]], the category [[Set]] has a [[skeleton]], namely the category of [[von Neumann ordinals|von Neumann cardinals]], which of course implies the global SCSA.  Similarly, the ordinary axiom of choice implies that every set is bijective to a unique von Neumann cardinal, and we can choose such a bijection uniformly for any small family of sets, which implies the local SCSA.

* Global SCSA also follows from the "global" version of the axiom of [[small violations of choice]], as proven in [Makkai's paper](#Makkai) (attributed to the referee).  Makkai claims there is a local form of SCSA that follows from the local SVC.  I have not attempted to show that this is true for the above local SCSA, although it is a guess at the sort of axiom Makkai might have had in mind.


## Consequences

* SCSA implies that the [[anabicategory]] of categories and [[anafunctors]] is [[locally small category|locally essentially small]] and [[cartesian closed category|cartesian closed]].  Specifically, local SCSA implies that for any two categories $X,A$ there is a small set of anafunctors from $X$ to $A$ such that any such anafunctor is isomorphic to one in this set.  The idea is that we can replace any anafunctor by a saturated one, in which case the set of "specifications that $F(x)=a$" for any $x\in X, a\in A$ is, if nonempty, a [[torsor]] over $Iso(a,a)$, and hence isomorphic to it.  Thus, applying local SCSA to the family $(Iso(a,a))_{a\in A}$, we obtain a "universal" set of specifications for saturated anafunctors.

  This implies that there exists a full subcategory of $Cat_{ana}(X,A)$ whose inclusion is a weak equivalence, and that an exponential $A^X$ exists.  If local SCSA holds in "functional" form, meaning there is a class-function specifying weakly terminal local reindexings, then this implies that $Cat_{ana}$ is weakly equivalent (i.e. ana-equivalent) to a locally small bicategory and that it admits a functor $(X,A) \mapsto A^X$.  (Of course, global SCSA implies functional local SCSA.)

## Models

[Makkai](#Makkai) states only the global SCSA, but claims that there is a local version of it that holds in all Grothendieck toposes.  The local form of SCSA stated above is a guess at the one Makkai might have had in mind.  I have not attempted to verify that it is true in all Grothendieck toposes.


## References

* {#Makkai} [[Michael Makkai]], _Avoiding the axiom of choice in general category theory_, Journal of Pure and Applied Algebra **108** isse 2 (1996) pp 109-173, doi:[10.1016/0022-4049(95)00029-1](https://doi.org/10.1016/0022-4049%2895%2900029-1), ([author's page](http://www.math.mcgill.ca/makkai/anafun/)) 


[[!redirects SCSA]]

category: foundational axiom

[[!redirects small cardinality selection axiom]]
[[!redirects axiom of small cardinality selection]]
[[!redirects small cardinality selection]]
[[!redirects SCSA]]
