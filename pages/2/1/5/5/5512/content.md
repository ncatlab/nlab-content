
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Definition

The term _Frobenius reciprocity_ has a meaning

* [In representation theory](#InRepresentationTheory)

* [In category theory](#InCategoryTheory).

(For different statements of a similar name see the disambiguation at _[[Frobenius theorem]]_.)

### In representation theory
 {#InRepresentationTheory}

In [[representation theory]], **Frobenius reciprocity** is the statement that the [[induction functor]] for [[group representation|representations of groups]] (or in some other [[algebraic categories]]) is [[left adjoint]] to the [[restriction]] functor.  Sometimes it is used for a [[decategorification|decategorified]] version of this statement as well, on [[characters]].

Specifically for $H \hookrightarrow G$ an [[subgroup]] inclusion, there is an [[adjunction]]

$$
  (Ind \dashv Res) \;\colon\;
  Rep_G
    \stackrel{\overset{Ind}{\leftarrow}}{\underset{Red}{\longrightarrow}} 
  Rep_H
$$

between the [[categories]] of $G$-[[representations]] and $H$-[[representations]], where for $\rho$ an $H$-representation, $Ind(\rho) \in Rep(G)$ is the [[induced representation]].

Sometimes also the _[[projection formula]]_

$$
  Ind(Res(W) \otimes V) \cong W \otimes Ind(V)
$$

is referred to as _Frobenius reciprocity_ in representation theory (e.g. [here on PlanetMath](http://planetmath.org/frobeniusreciprocity)).  

### In cartesian categories
 {#InCategoryTheory}

In [[category theory]], Frobenius reciprocity is a condition on a pair of [[adjoint functors]] $f_! \dashv f^*$.  If both categories are [[cartesian closed]], then the adjunction is said to satisfy **Frobenius reciprocity** if the [[right adjoint]] $f^* \colon \mathcal{Y} \to \mathcal{X}$ is a [[cartesian closed functor]]; that is, if the canonical map $f^*(b^a) \to f^*(b)^{f^*(a)}$ is an [[isomorphism]] for all objects $a,b$ of $\mathcal{Y}$.

Each of the functors $-^a$, $-^{f^*(a)}$ and $f^*$ has a [[left adjoint]], so by the calculus of [[mates]], this condition is equivalent to asking that the canonical "[[projection formula|projection]]" morphism 

\[
  \label{ProjectionMorphism}
  \pi 
  \,\colon\, 
  f_! (f^*a \times c) 
  \longrightarrow 
  a \times f_!(c) 
\] 

is an isomorphism for each $a$ in $\mathcal{Y}$ and $c$ in $\mathcal{X}$.  

This holds for instance for the [[base change]] between [[slice categories]] $\mathcal{C}_{/b}$, $\mathcal{C}_{/b'}$ of a [[finitely complete category]] $\mathcal{C}$ along a morphism $f \colon b' \to b $ -- by the [[pasting law]] in $\mathcal{C}$:
\[
  \label{PastingLawForLexCategories}
  \array{
    f^\ast a \times_{b'} c
    &\longrightarrow&
    f^\ast a 
    &\longrightarrow&
    a
    \\
    \big\downarrow
    &&
    \big\downarrow
    &&
    \big\downarrow
    \\
    c 
    &\underset{p_C}{\longrightarrow}&
    b'
    &\underset{f}{\longrightarrow}&
    b
  }
  \;\;\;\;\;\;\;\;
  \simeq
  \;\;\;\;\;\;\;\;
  \array{
    a
      \times_b 
    f_! c 
    &\longrightarrow&
    a
    \\
    \big\downarrow && \big\downarrow
    \\
    c &\underset{ f \circ p_c }{\longrightarrow}& b
    \mathrlap{\,.}
  }
\]

The condition (eq:ProjectionMorphism) clearly makes sense also if the categories are [[cartesian monoidal category|cartesian]] but not necessarily [[closed category|closed]], and is the usual formulation found in the literature.  It is equivalent to saying that the adjunction is a [[Hopf adjunction]] relative to the cartesian monoidal structures.

This terminology is most commonly used in the following situations:

* When $f^*$ and $f_!$ are the [[inverse image|inverse]] and [[direct image]] functors along a map $f$ in a [[hyperdoctrine]].  Here $S$ is a category and $P \colon S^{op} \to Cat$ is an $S$-[[indexed category]] such that each category $P X$ is [[cartesian closed]] and each functor $f^* = P f$ has a [[left adjoint]] $\exists_f$ ([[existential quantifier]], also written $f_!$).  Then $P$ is said to satisfy Frobenius reciprocity, or the **Frobenius condition**, if each of the [[adjunctions]] $\exists_f\dashv f^*$ does. If the categories $P X$ are cartesian but not closed then it still makes sense to ask for Frobenius reciprocity in the second form above, and in that case its logical interpretation is that $\exists x . (\phi \wedge \psi)$ is equivalent to $(\exists x.\phi) \wedge \psi$ if $x$ is not free in $\psi$.

* When $f^*$ is the [[inverse image]] part of a [[geometric morphism]] between [[(n,1)-topoi]] and $f_!$ is a [[left adjoint]] of it, if the [[adjunction]] $f_!\dashv f^*$ satisfies  Frobenius reciprocity, then the geometric morphism is called [[locally n-connected (n+1,1)-topos|locally (n-1)-connected]].  In particular, if $n=0$ so that we have a [[continuous map]] of [[locales]], then a left adjoint $f_!$ satisfying Frobenius reciprocity makes it an [[open map]], and if $n=1$ so that we have 1-[[topoi]], then it is [[locally connected geometric morphism|locally connected]] (see also _[[open geometric morphism]]_).  This usage of "Frobenius reciprocity" is sometimes also extended to the dual situation of [[proper map]]s of locales and topoi.

### In six operations yoga
 {#InWirthmuellerContexts}

The projection formula plays a notable role in Grothendieck's yoga of [[six operations]].  For example if an [[adjoint triple]] $(f_! \dashv f^\ast \dashv f_\ast)$ between [[symmetric monoidal category|symmetric]] [[closed monoidal categories]] is a _[[Wirthmüller context]]_ ([May 05](#May05)), $f^\ast$ is a strong [[closed monoidal functor]].  This implies the projection formula, i.e. the existence of a [[natural isomorphism]] of the form

$$
  \pi 
    \;\colon\;
  f_!
  \big(
     f^\ast a \otimes c
  \big) 
  \overset{\sim}{\longrightarrow} 
  a \otimes (f_! c)
  \,.
$$

The [[projection formula]] also holds in a [[Grothendieck context]] or a [[Verdier-Grothendieck context]] ([May 05](#May05)).

### In weak factorization systems
 {#InWeakFactorizationSystems} 

A [[weak factorization system]] $(\mathcal{L},\mathcal{R})$ on a [[finitely complete category]] is said to satisfy the **Frobenius condition** when $\mathcal{L}$ is closed under [[pullback]] (i.e.,  [[base change]]) along morphisms in $\mathcal{R}$.

The property seems to have been named by [Van den Berg and Garner (2012)](#VanDenBergGarner2012).
This usage is related to [Frobenius reciprocity for adjoint functors](#InCategoryTheory) by the following observation ([Clementino, Giuli & Tholen 1996, Proposition 1.3](#ClementinoGiuliTholen1996)):

+-- {: .num_prop}
###### Proposition

A [[orthogonal factorization system|proper orthogonal factorization system]] $(\mathcal{E},\mathcal{M})$ in a [[finitely complete category]] $\mathcal{C}$ satisfies the Frobenius condition if and only if for all $f \colon X \to Y$, the adjunction $Sub_{\mathcal{M}}(X) : f_! \dashv f^* : Sub_{\mathcal{M}}(Y)$ satisfies the Frobenius condition (where $Sub_{\mathcal{M}}(X)$ is the poset of subobjects of $X$ in $\mathcal{M}$, $f^*$ is pullback along $f$, and $f_!$ sends $m$ to the $\mathcal{M}$ part of the factorization of $f m$).

=--

When the category is [[locally cartesian closed category|locally cartesian closed]], the Frobenius condition has an equivalent formulation in terms of [[dependent product]]:

+-- {: .num_prop}
###### Proposition

A weak factorization system $(\mathcal{L},\mathcal{R})$ on a [[locally cartesian closed category]] $\mathcal{C}$ satisfies the Frobenius condition if and only if for every $f : Y \to X$ in $\mathcal{R}$ and $g : Z \to Y$ in $\mathcal{R}$, the [[dependent product]] $\prod_f g \to X$ is in $\mathcal{R}$.

=--

In [[categorical models of dependent type theory]] where types are interpreted as maps in a right class (as in ([Van den Berg & Garner 2012](#VanDenBergGarner2012))), the Frobenius condition can thus be used to interpret [[dependent product types]].
See for example [Kapulkin & Lumsdaine 2021, Lemma 2.3.1](#KapulkinLumsdaine2021).

In the context of [[Quillen model categories]], the Frobenius condition is related to [[proper model category|right properness]] ([Gambino & Sattler 2017](#GambinoSattler2017)):

+-- {: .num_prop}
###### Proposition

A [[Quillen model category]] whose [[cofibrations]] are closed under pullback is [[proper model category|right proper]] if and only if its (trivial cofibration, fibration) weak factorization system satisfies the Frobenius condition.

=--

A model category which has cofibrations closed under pullback and a (trivial cofibration, fibration) wfs satisfying the Frobenius condition is a [[locally cartesian closed model category]] and thus presents a [[locally cartesian closed (∞,1)-category]].

## Properties

### Closed monoidal functors and the projection formula

The following result isolates the connection between [[closed functor|closed functors]] and the projection formula.  We begin with some context.

Recall that a monoidal category $\mathcal{Y}$ is **[left closed](https://ncatlab.org/nlab/show/closed+monoidal+category#left_right_and_biclosed_monoidal_category)** if each functor $a \otimes - \colon \mathcal{Y} \to \mathcal{Y}$ has a right adjoint $[a, -] \colon  \mathcal{Y} \to \mathcal{Y}$, called the internal hom.   We can similarly define right closed monoidal categories.   A symmetric or even braided monoidal category is left closed if and only if it is right closed, and one then simply calls it [[closed monoidal category|closed]], but for maximum generality we consider the merely monoidal case.   

A functor $F$ between left closed monoidal categories is **lax closed** it if preserves the internal hom and the unit object up to a specified map  

$$ 
  \hat{F}
  \;\colon\; 
  F[a,b] \to [F a,F b], 
  \qquad  
  F_0 \colon I \to F(I)
  \,,
$$

[[natural transformation|natural]] in both variables and obeying some [[coherence laws]] listed at *[[closed functor]]*.  If these are [[natural isomorphisms]] we call the functor **[[strong closed functor|strong closed]]**.  

Any [[lax monoidal functor]] betweeen left [[closed monoidal categories]] is lax closed (for a sketch of the argument see *[[closed functor]]*), but a [[strong monoidal functor]] may not be [[strong closed functor|strong closed]].   

+-- {: .num_prop}
###### Proposition

Suppose $f_! \dashv f^\ast$ is an [[adjoint functor|adjunction]] between left [[closed monoidal categories]]. Then [[natural transformations]]

$$ 
  \phi 
   \;\colon\; 
  f^*[a,b] \to [f^*a, f^*b]  
$$

correspond [[bijection|bijectively]] to [[natural maps]]

$$
  \pi 
    \;\colon\;
  f_!
  \big(
    (f^\ast a) \otimes c
  \big) 
    \longrightarrow 
  a \otimes (f_! c)
  \,.
$$

Furthermore, $\phi$ is an isomorphism if and only if $\pi$ is, in which case we say the **[[projection formula]]** holds.

=--

+-- {: .proof}
###### Proof 

Suppose $\mathcal{X}$ and $\mathcal{Y}$ are left closed monoidal categories and $f_! \colon \mathcal{X} \to \mathcal{Y}$ is left adjoint to $f^* \colon \mathcal{Y} \to \mathcal{X}$.    Suppose we have a natural map 

$$ \phi \colon f^*[a,b] \to [f^*a, f^*b]  $$

for $a,b \in \mathcal{Y}$.  Thus we obtain a natural map

$$ \mathcal{X}(c, f^*[a,b]) \to \mathcal{X}(c, [f^*a, f^*b]), $$

for arbitrary $c \in \mathcal{X}$ (now natural in all three variables).   By hom-tensor adjointness and the fact that $f_!$ is the left adjoint of $f^*$ we can rewrite this as

$$ \mathcal{Y}(f_! c, [a,b]) \to \mathcal{X}(f^*a \otimes c,f^*b). $$

Using both these facts again we obtain

$$ \mathcal{Y}(a \otimes f_! c, b) \to \mathcal{X}(f_!(f^\ast a \otimes c), b)\,. $$

By the [[Yoneda lemma]] this gives the desired natural map

$$
  \pi \colon\;
  f_!(f^\ast a \otimes c) \longrightarrow a \otimes f_! c\,.
$$

By running through this calculation one can see that if $\phi$ is a invertible then all the other natural maps listed above are too, including $\pi$.  Conversely, starting with $\pi$ we can run the argument backwards and get $\phi$, and if $\pi$ is invertible then so is $\phi$.

=--

It follows that if $f^*$ is strong closed, the projection formula holds.  Also if $f$ is strong monoidal and the projection formula holds, $f^*$ is strong closed.

### Relation to Frobenius laws (in Frobenius algebras)

The name "Frobenius" is sometimes used to refer to other conditions on adjunctions, known as "Frobenius laws". The formal structure of the Frobenius law appears in the notion of [[Frobenius algebra]], in the axiom which relates multiplication to comultiplication, and recurs in another form isolated by Carboni and Walters in their studies of cartesian bicategories and bicategories of relations. Namely, if $\delta \colon 1 \to \otimes \Delta$ denotes the diagonal transformation on a cartesian bicategory (e.g., $Rel$), with right adjoint $\delta^\dagger$, then there is a canonical map 

$$\delta \delta^\dagger \stackrel{\phi}{\to} (1 \otimes \delta^\dagger)(\delta \otimes 1)$$ 

mated to the coassociativity isomorphism 

$$(1 \otimes \delta)\delta \to (\delta \otimes 1)\delta$$ 

and the **Frobenius law** here is the assumption that _the 2-cell $\phi$ is an isomorphism_. (There are two Frobenius laws actually; the other is that a similar canonical map 

$$\delta \delta^\dagger \stackrel{\phi'}{\to} (\delta^\dagger \otimes 1)(1 \otimes \delta),$$ 

mated to the inverse coassociativity, is also an isomorphism. However, it may be shown that if one of the Frobenius laws holds, then so does the other; see the article [[bicategory of relations]].) 

It is very easy to make a slip and call the Frobenius law "Frobenius reciprocity", perhaps all the more because there are close connections between the two. One example occurs in the context of bicategories of relations, as follows. 

Given a locally posetal [[cartesian bicategory]] $B$ and any object $c$ of $B$, one may construct a hyperdoctrine of the form

$$\hom_B(i-, c)\colon Map(B)^{op} \to Semilat$$ 

where $i: Map(B) \to B$ is the inclusion, and $Semilat$ is the 2-category of meet-semilattices. Here $r \in \hom(i b, c)$ is thought of as a relation from $b$ to $c$, and for a map $f: a \to b$, the relation $f^\ast r$ is the pulling back 

$$f^\ast r \coloneqq (a \stackrel{f}{\to} b \stackrel{r}{\to} 1)$$ 

along $f$, and one may show that $f^\ast-$ preserves finite local meets. Indeed, the pushforward or quantification along $f$ takes $q: a \to 1$ to 

$$\exists_f q \coloneqq (b \stackrel{f^\dagger}{\to} a \stackrel{q}{\to} 1)$$ 

and $\exists_f \dashv f^\ast$ because $f^\dagger$ is _right_ adjoint to the map $f$. Because $f^\ast-$ is a right adjoint, it preserves local meets. 

Frobenius reciprocity in this context, ordinarily written as 

$$r \wedge \exists_f q = \exists_f (f^\ast r \wedge q),$$

can then be restated for the hyperdoctrine $\hom_B(i-, c)$; it takes the form 

$$r \wedge q f^\dagger = (r f \wedge q)f^\dagger$$  

for any map $f: a \to b$ and predicates $q \in \hom(a, c)$, $r \in \hom(b, c)$. 

Meanwhile, recall that a **bicategory of relations** is a (locally posetal) cartesian bicategory in which the Frobenius laws hold. 

+-- {: .num_prop #FLtoFR}
###### Proposition

Frobenius reciprocity holds in each hyperdoctrine $\hom_B(i-, c)$ associated with a bicategory of relations. 
=-- 

+-- {: .proof}
###### Proof (sketch)
One first proves that a bicategory of relations is a compact closed bicategory in which each object $b$ is self-dual. The unit here is given by 

$$\eta_b = (1 \stackrel{\varepsilon^\dagger}{\to} b \stackrel{\delta}{\to} b \otimes b)$$ 

and the counit by 

$$\theta_b = (b \otimes b \stackrel{\delta^\dagger}{\to} b \stackrel{\varepsilon}{\to} 1).$$

Using this duality, each relation $r: b \to c$ has an opposite relation $r^{op} \colon c \to b$ given by 

$$c \stackrel{c \otimes \eta_b}{\to} c \otimes b \otimes b \stackrel{1 \otimes r \otimes 1}{\to} c \otimes c \otimes b \stackrel{\theta_c \otimes b}{\to} b.$$

It may further be shown that in a bicategory of relations, if $f: a \to b$ is a map, then its right adjoint $f^\dagger$ equals the opposite $f^{op}$. Therefore Frobenius reciprocity becomes the equation  
$$r \wedge q f^{op} = (r f \wedge q)f^{op}$$ 
but in fact this is just a special case of the more general modular law, which holds in a bicategory of relations as shown [here](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) in a blog post by Walters. The modular law in turn depends crucially upon the Frobenius laws. 
=-- 

Thus, in this instance, _Frobenius reciprocity follows from the Frobenius laws_. 

+-- {: .num_prop #FRtoFL} 
###### Proposition
In a locally posetal cartesian bicategory, the Frobenius laws follow from Frobenius reciprocity. 
=-- 

+-- {: .proof} 
###### Proof 
Again, Frobenius reciprocity in a (locally posetal) cartesian bicategory $B$ means that for any map $f: a \to b$ and any two relations $q \in B(a, c)$, $r \in B(b, c)$, the canonical inclusion 
$$(q \wedge r f)f^\dagger \leq q f^\dagger \wedge r$$ 
is an equality. One (and therefore both) of the Frobenius laws will follow by taking the following choices for $f$, $q$, and $r$: 

$$f = \delta_x, \qquad q = \varepsilon_{x}^{\dagger} \otimes 1_x, \qquad r = \varepsilon_x \otimes 1_x \otimes \varepsilon_{x}^{\dagger}$$ 

where $\delta_x: x \to x \otimes x$ is the diagonal map and $\varepsilon_x: x \to 1$ is the projection. The remainder of the proof is best exhibited by a string diagram calculation, which is given here: [[Frobenius-reciprocity.pdf:file]]. 
=--

## Examples

+-- {: .num_example}
###### Example

Generally, for $\mathbf{H}$ a [[topos]] and $f \;\colon\; X \longrightarrow Y$ any [[morphism]], then the induced [[base change]] [[etale geometric morphism]]

$$
  (f_! \dashv f^\ast \dashv f_\ast)
  \;\colon\;
  \mathbf{H}_{/X}
  \to 
  \mathbf{H}_{/Y}
$$

has [[inverse image]] $f^\ast$ a [[cartesian closed functor]] and hence (see there) exhibits Frobenius reciprocity.

=--


## Related concepts

* [[Beck-Chevalley condition]]

* [[Wirthmüller context]]


## References 
 {#References}



Discussion in [[representation theory]]:

* {#Hristova19} Katerina Hristova: *Frobenius Reciprocity for Topological Groups*, Communications in Algebra **47** 5 (2019) &lbrack;[doi:10.1080/00927872.2018.1529773](https://doi.org/10.1080/00927872.2018.1529773), [arXiv:1801.00871](https://arxiv.org/abs/1801.00871)&rbrack;


The term 'Frobenius reciprocity', in the context of [[hyperdoctrines]], was introduced in

* [[Bill Lawvere]], _[[Equality in hyperdoctrines and comprehension schema as an adjoint functor]]_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970) 1-14 &lbrack;[pdf](https://ncatlab.org/nlab/files/LawvereComprehension.pdf)&rbrack;

Lawvere defines Frobenius reciprocity by either of the two equivalent conditions (see "Definition-Theorem" on p.6), and notes that "one of these kinds of identities is formally similar to, and reduces in particular to, the Frobenius reciprocity formula for permutation representations of groups" (p.1).

Related discussion is in:

* {#Seely83} [[Robert A. G. Seely]], p. 511 of: *Hyperdoctrines, Natural Deduction and the Beck Condition*, Zeitschr. f. math. Logik und Grundlagen d. Math. **29** (1983) 505-542 &lbrack;[doi:10.1002/malq.19830291005]( https://doi.org/10.1002/malq.19830291005), [pdf](https://www.math.mcgill.ca/seely/ZML/ZML.PDF)&rbrack;

* {#Pavlović96} [[Duško Pavlović]], p. 164 in: *Maps II: Chasing Diagrams in Categorical Proof Theory*, Logic Journal of the IGPL, **4** 2 (1996) 159–194 &lbrack;[doi:10.1093/jigpal/4.2.159](https://doi.org/10.1093/jigpal/4.2.159), [pdf](http://www.isg.rhul.ac.uk/dusko/papers/1996-mapsII-IGPL.pdf)&rbrack;

A textbook source is around lemma 1.5.8 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

General discussion in the context of projection formulas in [[monoidal categories]] (not necessarily cartesian) is in 

* {#May05} [[Halvard Fausk]], [[Po Hu]], [[Peter May]],  *Isomorphisms between left and right adjoints*, Theory and Applications of Categories, **11** 4 (2003) 107-131 &lbrack;[tac:11-04](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf)&rbrack;

 

Manifestations of the Frobenius reciprocity formula, [in the sense of category theory](#InCategoryTheory), recur throughout mathematics in various forms (push-pull formula, projection formula); see for example this Math Overflow post: 

* Andrea Ferretti, Ubiquity of the push-pull formula, MO Question 18799, March 20, 2010. [(link)](http://mathoverflow.net/questions/18799/ubiquity-of-the-push-pull-formula)

Further MO discussion includes

* [Wrong-way Frobenius reciprocity for finite groups representations](http://mathoverflow.net/questions/132272/wrong-way-frobenius-reciprocity-for-finite-groups-representations)

Relating to the Frobenius condition for weak factorization systems:

* {#ClementinoGiuliTholen1996} [[Maria Manuel Clementino]], Eraldo Giuli, [[Walter Tholen]], *Topology in a category: compactness*, Portugaliae Mathematica **53**(4) 397--433 (1996) &lbrack;[url](https://www.emis.de/journals/PM/53f4/2.html)&rbrack;

* {#VanDenBergGarner2012} [[Benno van den Berg]], [[Richard Garner]], *Topological and Simplicial Models of Identity Types*, ACM Transactions on Computational Logic (TOCL) **13**(1) 1--44 (2012) &lbrack;[doi:10.1145/2071368.207137](https://www.emis.de/journals/PM/53f4/2.html),[arXiv:1007.4638](https://arxiv.org/abs/1007.4638)&rbrack;

* {#GambinoSattler2017} [[Nicola Gambino]] and [[Christian Sattler]], *The Frobenius condition, right properness, and uniform ﬁbrations*, Journal of Pure and Applied Algebra **221** (2017). &lbrack;[doi:10.1016/j.jpaa.2017.02.013](https://dx.doi.org/10.1016/j.jpaa.2017.02.013),[arXiv:1510.00669](https://arxiv.org/abs/1510.00669)&rbrack; -- beware of section numbering discrepancy between the published and arXiv versions.

* {#KapulkinLumsdaine2021} [[Chris Kapulkin]], [[Peter LeFanu Lumsdaine]], *The Simplicial Model of Univalent Foundations (after Voevodsky)*, Journal of the European Mathematical Society **23** (2021) 2071–2126  $[$[arXiv:1211.2851](https://arxiv.org/abs/1211.2851), [doi:10.4171/jems/1050](https://doi.org/10.4171/jems/1050)$]$

[[!redirects Frobenius reciprocity]]
[[!redirects Frobenious reciprocity]]
[[!redirects Frobenius law]]
[[!redirects Frobenius condition]]
[[!redirects Frobenius axiom]]