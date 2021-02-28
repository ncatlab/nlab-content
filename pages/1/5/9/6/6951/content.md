
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

**Kripke--Joyal semantics** is a higher order generalization of the [[semantics|semantic]] interpretation proposed initially by Beth, Gregorczyk, and Kripke for [[intuitionistic logic|intuitionistic predicate logic]]. It provides a notion of _'local truth'_ or _'validity at a stage'_ in a [[topos]].

Since it is closely related to [[Paul Cohen|Paul Cohen's]] [[forcing]] technique in [[set theory]], a connection that was already observed by Gregorczyk and Kripke, it is sometimes called _forcing_ semantics. Other terms in use for it are _external_ semantics, _cover_ semantics or _Beth--Kripke--Joyal_ semantics.

By giving a semantics to formulas written in the [[higher-order logic|higher-order]] [[type theory]] used to express [[ordinary mathematics]] in a topos, the Kripke--Joyal semantics serves as [[semantics|semantic]] interface between the [[internalisation|internal (syntactic) description]] of mathematical objects using the [[Mitchell–Bénabou language]] and the external description.  

Kripke--Joyal semantics provide rules and prescriptions for semantic interpretation for general toposes but these prescriptions may simplify for special classes of toposes e.g. the rules resulting for [[presheaf toposes]] over posets (when restricted to first-order formulas) correspond to the original notion of model for IPL considered by [[Saul Kripke|Kripke]] et al.

There should be a version of Kripke--Joyal semantics for [[homotopy type theory]], as claimed [here](n-types+cover#InModels). 

## Formulation

Let $\mathcal{E}$ be an [[elementary topos]]. We will now specify the Kripke--Joyal semantics for formulas $\varphi$ in the [[Mitchell–Bénabou language]] of $\mathcal{E}$ restricting ourselves mainly to formulas $\varphi (x)$ with one free variable $x$ of type $X$. The straightforward generalization to the case with (less or) more free variables can be found in Johnstone ([1977](JT77)) or Borceux ([1994](#Borceux94)).

Recall that such a formula $\varphi (x)$ is interpreted by a morphism $X\overset{\varphi(x)}{\to}\Omega$ and gets an extension $\{x|\varphi(x)\}$ assigned to by the pullback

$$
\array{
\{x|\varphi(x)\}&\to & 1& \\
\downarrow &  &\downarrow &\mathsf{true} \\
X &\underset{\varphi(x)}{\to} & \Omega&
}
$$

Now a global element $1\overset{x_0}{\to} X$ satisfies $\varphi(x)$ if it is contained in $\{x|\varphi(x)\}$ in the sense that the following commutes:

$$
\array{
& &\{x|\varphi(x)\}&\to & 1 &\\
 &\nearrow&\downarrow &  &\downarrow &\mathsf{true} \\
1&\underset{x_0}{\to}& X &\underset{\varphi(x)}{\to} & \Omega&
}
$$

Kripke--Joyal semantics results from the generalization of this satisfaction relation from global elements to _generalized_ elements $U\overset{\alpha}{\to} X$.

+-- {: .num_defn #forcing}
###### Definition
A generalized element $U\overset{\alpha}{\to} X$ is said to _satisfy the formula_ $\varphi(x)$ or more suggestively, $U$ _forces_ $\varphi$, denoted $U\models \varphi (\alpha)$, when $\alpha$ factors through $\{x|\varphi(x)\}$ i.e. there exists a map $m$ making the following commute:
$$
\array{
& &\{x|\varphi(x)\}&\to & 1& \\
 &\overset{m}\nearrow&\downarrow &  &\downarrow &\mathsf{true} \\
U&\overset{\alpha}{\to}& X &\underset{\varphi(x)}{\to} & \Omega&
}
$$
=--

This is the same as to say that $im\,\alpha\subseteq \{x|\varphi(x)\}$ as subobjects of $X$.

Whereas $\{x|\varphi(x)\}$ represents the set of elements satisfying $\varphi$ internally, the collection of global elements has in general no such representation thereby motivating the terminology 'external semantics'.

## Properties

One can now unwind the [[forcing]] relation $U\models \varphi (\alpha)$ recursively over the syntactic composition of $\varphi$. This results in a collection of semantic rules that is commonly referred to as the _Kripke--Joyal semantics_ and permits to make contact with the original rules proposed by Kripke for intuitionistic logic in 1965.

These rules are often useful for translating step by step an object defined by a formula of the Mitchell–Bénabou into a concrete mathematical object in the topos.

First of all, the [[forcing]] relation is _monotone_ and _local_ :

+-- {: .num_prop #Monotone_Local}
###### Proposition
If $f:V\to U$ and $U\models \varphi (\alpha)$ then $V\models \varphi (\alpha\circ f)$. Conversely, if $f:V\to U$ is _epic_ and $V\models \varphi (\alpha\circ f)$ then $U\models \varphi (\alpha)$.
=--

The short proof can be found in MacLane--Moerdijk ([1994](#MM94), p.304).

Note that the proposition gives a first hint of the importance of epimorphisms or _covers_ in this semantics, testimony of its geometric underpinning.

+-- {: .num_prop #Kripke-Joyal}
###### Theorem
Let $\mathcal{E}$ be an elementary topos and $\alpha:U\to X\,$ a generalized element of $X\in\mathcal{E}$ . The forcing relation $\models$ satisfies

1. $U\models \varphi(\alpha)\wedge \psi(\alpha)$ iff $U\models \varphi(\alpha)$ and $U\models \psi(\alpha)\,$.

1. $U\models \varphi(\alpha)\vee \psi(\alpha)$ iff there exists maps $g:U_1\to U$ and $g_2:U_2\to U$ with $g_1+g_2:U_1+U_2\to U$ epic and such that $U_1\models \varphi(\alpha\circ g_1)$ and $U_2\models \psi(\alpha\circ g_2)\,$.

1. $U\models \varphi(\alpha)\Rightarrow \psi(\alpha)$ iff for any $g:V\to U\,$, $V\models \varphi(\alpha\circ g)$ implies $V\models\psi(\alpha\circ g)\,$.

1. $U\models\neg \varphi(\alpha)$ iff for all $g:V\to U\,$, $V\models \varphi(\alpha\circ g)$ implies that $V\simeq 0$.

Let $\varphi(x,y)$ be a formula with free variables x,y of type $X$ and $Y$ respectively. Then

1. $U\models \exists y\varphi(\alpha, y)$ iff there exists $g:V\to U$ epic and a generalized element $h:V\to Y$ such that $V\models \varphi(\alpha\circ g,h)\,$.

1. $U\models \forall y\varphi(\alpha, y)$ iff for every object $V$ and all pairs of generalized elements $g:V\to U$ and $h:V\to Y\,$, $V\models \varphi(\alpha\circ g,h)\,$.

=--

For a proof see MacLane--Moerdijk ([1994](#MM94), pp.305f).

## Lawvere on Kripke--Joyal semantics

> To workers in algebraic geometry and analysis, it may appear somewhat excessive to detour through an elaborate Mitchell–Bénabou language which in turn requires a Kripke--Joyal semantics in order to get back at the mathematical content of a specific topos. (That sometimes-recommended procedure is strictly analogous to defining a group to be the quotient of the free group generated by itself, which analogously is sometimes useful). The key clause in that semantics was presupposed in the title 'Quantifiers and Sheaves', but the linear case was a theorem in Godement 1958 and indeed just expresses in terms of 20th century concepts the content of Volterra's local existence theorem. Briefly,

> a) the rule of inference for existential quantification is just a symbolic expression of the universal property enjoyed by the geometric image of any map (not only in the category of sets where the axiom of choice holds, but) in any topos,

> b) a figure lying in such an image comes in fact only locally from figures in the domain of the map.

Lawvere ([2000](#Law00), pp.717f).

## Related concepts

* [[Mitchell–Bénabou language]]

* [[internal logic]]

* [[semantics]]

* [[stack semantics]]

* [[forcing]]

## References

For the origins in the semantics of intuitionistic logic consult

* E. W. Beth, _Semantic construction of intuitionistic logic_, Mededel. Kon. Ned. Akad. Wetensch. Afd. letterkunde N. S. **19** no.13 (1956) pp.357--388.

* A. Grzegorczyk, _A philosophically plausible formal interpretation of intuitionistic logic_, Indagationes Mathematicae **26** (1964) pp.596&#8211;601.

* [[Saul Kripke|S. A. Kripke]], _Semantical analysis of intuitionistic logic I_, pp.92--130 in Crossley, Dummett (eds.), _Formal Systems and Recursive Functions_, North-Holland Amsterdam 1965.

* H. C. M. de Swart, _An intuitionistically plausible interpretation of intuitionistic logic_, JSL **42** no. 4 (1977) pp.564--578.

* W. Veldman, _An intuitionistic completeness theorem for intuitionistic predicate calculus_, JSL **41** no. 1 (1976) pp.159--166.

A categorical-constructive take on these completeness results is in

* [[Erik Palmgren]], _Constructive Sheaf Semantics_, Math. Log. Quart. **43** (1997) pp.321-327.

A (non-categorical) textbook presentation of the original Kripke semantics can be found in

* [[John Lane Bell|J. Bell]], M. Machover, _A Course in Mathematical Logic_, North-Holland Amsterdam 1977. (section IX.6 pp.416--422)

A more recent overview is in

* D. van Dalen, _Intuitionistic Logic_, pp.224--257 in Goble (ed.), _The Blackwell Guide to Philosophical Logic_, Oxford 2001. (pp.237--240)

The topos-theoretic generalization is usually attributed to [[André Joyal]] who observed in the early 70s that this topos semantics subsumes various notions of forcing but his work was apparently not published. An early reference is

* [[Gerhard Osius|G. Osius]], _A note on Kripke--Joyal semantics for the internal language of topoi_, Springer LNM **445** (1975) pp.349--354.

The first section of the following sums up a 1973 talk and gives an interesting informal overview of the basics involved emphazising [[site|sites]]

* [[Anders Kock]], _Universal Projective Geometry via Topos Theory_, JPAA **9** (1976) pp.1-24.

The following texts stress the connection to Cohen and Kripke's work

* [[F. William Lawvere]], _Variable sets etendu and variable structure in topoi_, Lecture notes University of Chicago 1975.

* {#Lawvere76}[[F. William Lawvere]], _Variable quantities and variable structures in topoi_, pp.101--131 in Heller, Tierney (eds.), Algebra, Topology and Category Theory, Academic Press New York 1976. 

Most textbooks on topos theory have a section on Kripke--Joyal semantics. Particularly thorough are 

* {#Borceux94}[[Francis Borceux]], _Handbook of Categorical Algebra vol.3_, Cambridge UP 1994. (section 6.6)

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_, Springer Heidelberg 1994. (section VI.6--7)

More concise are

* [[Peter Johnstone]], _Topos Theory_, Academic Press New York 1977. (Reprinted by Dover Mineola 2014; pp.157--161)

* [[Colin McLarty]], _Elementary Categories, Elementary Toposes_, Oxford UP 1992. (chapter 18)

Freely available online are

* {#Goldblatt84} R. Goldblatt, _Topoi -- The Categorical Analysis of Logic_, 2nd ed. North-Holland Amsterdam 1984. (Dover reprint New York 2006; [project euclid](http://projecteuclid.org/euclid.bia/1403013939), section XIV.6)

* [[Ieke Moerdijk]],  [[Jaap van Oosten]], _Topos theory_, lecture notes (2007). ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/toposmoeder.pdf), page 58ff)

The above Lawvere quote stems from

* {#Law00}F. W. Lawvere, _Comments on the development of topos theory_, pp.715--734 in Pier (ed.), _Development of Mathematics 1950--2000_, Birkh&#228;user Basel 2000. Reprinted as TAC reprint **24** (2014) pp.1--22.  ([TAC](http://www.tac.mta.ca/tac/reprints/articles/24/tr24abs.html)) 

For a philosophical assessment and comparison to ordinary Tarski semantics see

* Jean Petitot, _La neige est blanche ssi… Prédication et perception
_, Mathématiques et Sciences humaines, Tome **140** (1997) pp.35--50. ([pdf](http://archive.numdam.org/article/MSH_1997__140__35_0.pdf))

A generalization to [[quantales]] is in

* R. Goldblatt, _A Kripke--Joyal Semantics for Noncommutative Logic in Quantales_, pp.209--225 in Governatori, Hodkinson, Venema (eds.), _Advances in Model Logic vol. 6_, College Publications London 2006. ([draft](http://www.mcs.vuw.ac.nz/~rob/papers/aiml11printed.pdf))

Semantics via generalized elements in categories with pullbacks is studied in

* [[Anders Kock]], _Elementwise semantics in categories with pull-backs_, arXiv:2004.14731 (2020). ([abstract](http://arxiv.org/abs/2004.14731))


[[!redirects Kripke-Joyal semantics]]
[[!redirects Kripke–Joyal semantics]]
[[!redirects Kripke--Joyal semantics]]

[[!redirects Beth-Kripke-Joyal semantics]]
[[!redirects Beth–Kripke–Joyal semantics]]
[[!redirects Beth--Kripke--Joyal semantics]]

[[!redirects Kripke model]]
[[!redirects Kripke models]]

[[!redirects external semantics]]
