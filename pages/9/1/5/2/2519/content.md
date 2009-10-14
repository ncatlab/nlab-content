[[!redirects smooth topoi]]
[[!redirects smooth toposes]]

<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>

#Contents#

* automatic table of contents goes here
{:toc}

#Idea#

A __smooth topos__ or __smooth [[lined topos]]__ is 
the kind of [[topos]] studied in [[synthetic differential geometry]], a [[category]] of [[generalized smooth spaces]] for which a notion of [[infinitesimal space]] exists.

It is defined to be a [[category]] of objects that behave like [[spaces]], one of which --- the _line_ object $R$ --- is equipped with the structure of a commutative [[algebra]], such that for [[infinitesimal object]]s $S \subset R^n$ all morphisms $S \to R$ are _linear_  --- i.e. such that the [[Kock-Lawvere axiom]] holds.

# Definition #

There is a standard definition  and various straightforward variations.

## standard defnition ##


+-- {: .un_defn }
###### Definition

For $(\mathcal{T},R)$ a [[lined topos]] there is the obvious notion of $R$-algebra objects $A$
in $T$.  

For $A$ and $B$ any two $R$-algebra objects, there is the [[subobject]] $R Alg_T(A,B) \subset B^A$ of morphisms $A \to B$ that are algebra homomorphisms.

Write

$$
  Spec(A) := R Alg_{\mathcal{T}}(A,R) 
$$

for the algebra spectrum of $A$ in $\mathcal{T}$.

An **$R$-[[infinitesimal object|Weil algebra]]** $W$ is an $R$-algebra of the form $W = R \oplus J$, 
where $J$ is an $R$-finite-dimensional nilpotent ideal.

=--


+-- {: .un_defn }
###### Definition
**(smooth topos)**

A [[lined topos]] $(\mathcal{T},R)$ is a **smooth topos** if 

* the algebra spectra $Spec(W)$ of all [[infinitesimal object|Weil algebras]] $W$
  in $\mathcal{T}$  are [[infinitesimal object]]s in that
  the functor $(-)^{Spec W} : \mathcal{T} \to \maathcal{T}$ has a [[right adjoint]] (the "[[amazing right adjoint]]");

* it satisfies the [[Kock-Lawvere axiom]] in that for all $R$-Weil algebra objects $W$ the canonical morphism

  $$
    W \to R^{Spec(W)}
  $$

  is an [[isomorphism]] in $\mathcal{T}$.

=--



## variants ##

There are various immediate variants of this concepts.

### super smooth topos ###

In [[synthetic differential supergeometry]] one considers a notion of smooth topos that axiomatizes not just ordinary [[differential geometry]] but [[supergeometry]].

A **super smooth** topos is defined as a smooth topos with the notion of [[algebra]] replaced everywhere by [[superalgebra]].

So a super smooth topos is a [[topos]] $\mathcal{T}$ equipped with a [[superalgebra]] object $(R, +, \cdot)$ with even part $R_e$ and odd part $R_o$ etc.

An algebra spectrum object is now an internal object of superalgebra homomorphisms and the condition is that for every super Weil algebra $W = R \oplus m$ we have that $Spec(W) = R SAlg_{\mathcal{T}}(W,R)$ is an [[infinitesimal object]] and that $W \to R^{Spec W}$ is an [[isomorphism]]. 

This means that essentially all the standard general theory of smooth toposes goes through literally for super smooth toposes, too. The main difference is that a super smooth topos contains more types of [[infinitesimal object]]s.

There is for instance still the standard _even_ infinitesimal interval

$$
  D := D^{1|0} := \{\epsilon \in R_e | \epsilon^2 = 0\}
$$

but there is now also the _odd_ infinitesimal interval

$$
  D^{0|1} := \{\theta \in R_o \}
  \,.
$$

Notice that in the graded commutative algebra $A$ every odd element $\theta$ automatically squares to 0.

> [[Urs Schreiber]]: I'd think that the cominatorial/simplicial definition of [[differential forms in synthetic differential geometry]] applied verbatim in a super smooth topos automatically yields the right/expected notion of differential forms in supergeometry. 

# Examples #

For a list of examples see also [[Models for Smooth Infinitesimal Analysis]].

## Dubuc topos ##

## Stein topos ##

