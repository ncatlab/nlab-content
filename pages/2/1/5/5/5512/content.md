
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

In [[representation theory]], **Frobenius reciprocity** (sometimes _Frobenious_) is the statement that the [[induction functor]] for [[group representation|representations of groups]] (or in some other [[algebraic categories]]) is [[left adjoint]] to the [[restriction]] functor.  Sometimes it is used for a [[decategorification|decategorified]] version of this statement as well, on [[characters]].

Specifically for $H \hookrightarrow G$ an [[subgroup]] inclusion, there is an [[adjunction]]

$$
  (Ind \dashv Red) \;\colon\;
  Rep_G
    \stackrel{\overset{Ind}{\leftarrow}}{\underset{Red}{\longrightarrow}} 
  Rep_H
$$

between the [[categories]] of $G$-[[representations]] and $H$-[[representations]], where for $\rho$ an $H$-representation, $Ind(\rho) \in Rep(G)$ is the [[induced representation]].

Sometimes also the _[[projection formula]]_

$$
  Ind(Red(W) \otimes V) \simeq W \otimes Ind(V)
$$

is referred to as _Frobenius reciprocity_ in representation theory (e.g. [here on PlanetMath](http://planetmath.org/frobeniusreciprocity)). See below the general discussion [in Wirthm&#252;ller contexts](#InWirthmuellerContexts).

### In category theory
 {#InCategoryTheory}

In [[category theory]], Frobenius reciprocity is a condition on a pair of [[adjoint functors]] $f_! \dashv f^*$.  If both categories are [[cartesian closed]], then the adjunction is said to satisfy **Frobenius reciprocity** if the right adjoint $f^* \colon Y \to X$ is a [[cartesian closed functor]]; that is, if the canonical map $f^*(B^A) \to f^*(B)^{f^*(A)}$ is an [[isomorphism]] for all objects $B,A$ of $Y$.

Each of the functors $-^A$, $-^{f^*A}$ and $f^*$ has a [[left adjoint]], so by the calculus of [[mates]], this condition is equivalent to asking that the canonical "[[projection formula|projection]]" morphism 

$$
  f_!(C \times f^*A) \to (f_! C) \times A
$$ 

is an isomorphism for each $A$ in $Y$ and $C$ in $X$.  

This clearly makes sense also if the categories are [[cartesian monoidal category|cartesian]] but not necessarily [[closed category|closed]], and is the usual formulation found in the literature.  It is equivalent to saying that the adjunction is a [[Hopf adjunction]] relative to the cartesian monoidal structures.



This terminology is most commonly used in the following situations:

* When $f^*$ and $f_!$ are the [[inverse image|inverse]] and [[direct image]] functors along a map $f$ in a [[hyperdoctrine]].  Here $S$ is a category and $P \colon S^{op} \to Cat$ is an $S$-[[indexed category]] such that each category $P X$ is [[cartesian closed]] and each functor $f^* = P f$ has a [[left adjoint]] $\exists_f$ ([[existential quantifier]], also written $f_!$).  Then $P$ is said to satisfy Frobenius reciprocity, or the **Frobenius condition**, if each of the [[adjunctions]] $\exists_f\dashv f^*$ does. If the categories $P X$ are cartesian but not closed then it still makes sense to ask for Frobenius reciprocity in the second form above, and in that case its logical interpretation is that $\exists x . (\phi \wedge \psi)$ is equivalent to $(\exists x.\phi) \wedge \psi$ if $x$ is not free in $\psi$.

* When $f^*$ is the [[inverse image]] part of a [[geometric morphism]] between [[(n,1)-topoi]] and $f_!$ is a [[left adjoint]] of it, if the [[adjunction]] $f_!\dashv f^*$ satisfies  Frobenius reciprocity, then the geometric morphism is called [[locally n-connected (n+1,1)-topos|locally (n-1)-connected]].  In particular, if $n=0$ so that we have a [[continuous map]] of [[locales]], then a left adjoint $f_!$ satisfying Frobenius reciprocity makes it an [[open map]], and if $n=1$ so that we have 1-[[topoi]], then it is [[locally connected geometric morphism|locally connected]] (see also _[[open geometric morphism]]_).  This usage of "Frobenius reciprocity" is sometimes also extended to the dual situation of [[proper map]]s of locales and topoi.

### In Wirthm&#252;ller contexts of six-operations yoga
 {#InWirthmuellerContexts}

Generally, an [[adjoint triple]] $(f_! \dashv f^\ast \dashv f_\ast)$
between [[symmetric monoidal category|symmetric]] [[closed monoidal categories]]
is called a _[[Wirthmüller context]]_ ([May 05](#May05)) of _[[six operations]]_ yoga, if $f^\ast$ is a strong [[closed monoidal functor]]. 

+-- {: .num_prop}
###### Proposition


In a [[Wirthmüller context]], the projection formula/Frobenius reciprocity holds as a [[natural equivalence]]

$$
  \overline{\pi}
  \;\colon\;
  f_!(f^\ast(B)) \stackrel{\simeq}{\longrightarrow} B \otimes f_! A
$$

=--

+-- {: .proof}
###### Proof 

For all $A \in \mathcal{X}$ and $B,C \in \mathcal{Y}$ we have
by the $(f_! \dashv f^\ast)$-[[adjunction]] and the
tensor$\dashv$hom-adjunction a [[commuting diagram]] of the form


$$
  \array{
    \mathcal{Y}(f_! ((f^\ast B) \otimes A),\, C)
     &
      \stackrel{
        \mathcal{Y}(\overline{\pi}(A,B), C)
      }{
        \longrightarrow
     }
     &
    \mathcal{Y}(B \otimes f_! A, \, C  )
    \\
    \downarrow^{\mathrlap{\simeq}}
     &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \mathcal{X}(A, [(f^\ast B), (f^\ast C)])
    &\stackrel{}{\longrightarrow}&
    \mathcal{X}(A, f^\ast [B,C])
  }
  \,.
$$

By naturality in $A$ and by the [[Yoneda lemma]] this shows
that $\overline{\pi}$ is an equivalence precisey if 
$f^\ast$ is strong closed.

=--


## Properties

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



## References 
 {#References}

The term 'Frobenius reciprocity', in the context of hyperdoctrines, was introduced by Lawvere in

* F.W. Lawvere, _Equality in hyperdoctrines and comprehension schema as an adjoint functor_, Proceedings of the AMS Symposium on Pure Mathematics XVII (1970), 1-14.

Lawvere defines Frobenius reciprocity by either of the two equivalent conditions (see "Definition-Theorem" on p.6), and notes that "one of these kinds of identities is formally similar to, and reduces in particular to, the Frobenius reciprocity formula for permutation representations of groups" (p.1).

A textbook source is around lemma 1.5.8 in 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_

General discussion in the context of projection formulas in [[monoidal categories]] (not necessarily cartesian) is in 

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_, Theory and Applications of Categories , Vol. 11, 2003, No. 4, pp 107-131. ([TAC](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

Manifestations of the Frobenius reciprocity formula, [in the sense of category theory](#InCartegoryTheory), recur throughout mathematics in various forms (push-pull formula, projection formula); see for example this Math Overflow post: 

* Andrea Ferretti, Ubiquity of the push-pull formula, MO Question 18799, March 20, 2010. [(link)](http://mathoverflow.net/questions/18799/ubiquity-of-the-push-pull-formula)

Further MO discussion includes

* [Wrong-way Frobenius reciprocity for finite groups representations](http://mathoverflow.net/questions/132272/wrong-way-frobenius-reciprocity-for-finite-groups-representations)


[[!redirects Frobenius reciprocity]]
[[!redirects Frobenious reciprocity]]
[[!redirects Frobenius law]]
[[!redirects Frobenius condition]]
[[!redirects Frobenius axiom]]