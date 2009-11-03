> **under construction**


<div class="rightHandSide toc">
[[!include cohomology - contents]]


***

[[!include higher algebra - contents]]


</div>



+-- {: .standout}

This is a sub-entry of

* [[A Survey of Elliptic Cohomology]]

see there for background and context.

This entry sketches some basic ideas about the [[higher geometry]] version of the [[moduli stack]] of [[elliptic curve]]s: the derived moduli stack of [[derived elliptic curve]]s.

=--

Previous:

* [[A Survey of Elliptic Cohomology - cohomology theories]]

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

* [[A Survey of Elliptic Cohomology - E-infinity rings and derived schemes]]

* [[A Survey of Elliptic Cohomology - elliptic curves]]

* [[A Survey of Elliptic Cohomology - equivariant cohomology]]

 
* [[A Survey of Elliptic Cohomology - derived group schemes and (pre-)orientations]]

* [[A Survey of Elliptic Cohomology - A-equivariant cohomology]]



> **under construction**



#Contents#
* automatic table of contents goes here
{:toc}


#Idea#

In  the context of [[elliptic cohomology]] one assigns to every [[elliptic curve]] $\phi$ over a [[ring]] $R$ a [[cohomology theory]] [[Brown representability theorem|represented]] by an [[E-∞ ring]] [[spectrum]] $E_\phi$.

Since, by definition, we may identify the [[elliptic curve]] $\phi$ over $R$ with a patch $\phi : Spec R \to \mathcal{M}_{1,1}$ of the [[moduli stack]] $\mathcal{M}_{1,1}$ of elliptic curves, this assignment

$$
  \mathcal{O}^{Der} : \phi \mapsto E_\phi
$$

looks like an [[E-∞ ring]] valued [[structure sheaf]] on $\mathcal{M}_{1,1}$.

There is a very general theory of [[higher geometry]] for [[nLab:generalized scheme|generalized spaces]] with generalized [[nLab:structure sheaf|structure sheaves]]. Using this one may regard the pair $(\mathcal{M}_{1,1}, \mathcal{O}^{Der})$ as a [[structured (infinity,1)-topos|structured space]] that is a "derived" [[Deligne-Mumford stack]].

The central theorem about [[elliptic cohomology]] of [[Jacob Lurie]], refining the Goerss-Hopkins-Miller theorem says that

+-- {: .standout}

+-- {: .un_theorem }
###### Theorem
**(J. Lurie)**

$(\mathcal{M}, \mathcal{O}^{Der})$ is the _derived moduli stack_ of [[derived elliptic curve]]s in that for any [[E-∞ ring]] $R$ the space of morphisms

$$
  Spec R \to (\mathcal{M}_{1,1}, \mathcal{O}^{Der})
$$

is equivalent to the space of [[derived elliptic curve]]s over $R$.

=--

=--


# References #

A sketch of what this theorem means and how it is proven is part of the content of 

* [[Jacob Lurie]], [[A Survey of Elliptic Cohomology]].

and goes back to Jacob Lurie's PhD thesis (listed [[Jacob Lurie|here]]).

The general theory for the context of [[higher geometry]] invoked here has later been spelled out in

* [[Jacob Lurie]], [[Structured Spaces]]

but the special case of the general theory that is needed here, where the coefficient objects of structure sheaves are [[E-∞ ring]]s has been announced as

* [[Jacob Lurie]], [[Spectral Schemes]]

but isn't available yet. 

The general theory of [[E-∞ ring]]s themselves, in the [[(∞,1)-category]] theory context needed here, is developed in

* [[Jacob Lurie]], [[higher algebra|Commutative geometry]].

# theoretical background on higher geometry #

The statement that we are after really lives in the context of [[higher geometry]]. For details we have to refer you there, but here is an outline of the central aspects. 

## the most useful most general nonsense  ##

The general story of [[higher geometry]] is this:

We fix some [[(∞,1)-category]] of test spaces $\mathcal{G}$ equipped with the structure of a [[site]] (and a bit more). Such $\mathcal{G}$ is called a [[geometry (for structured (infinity,1)-toposes)]].

Using this, we have a general and a specific notion of spaces modeled on $\mathcal{G}$:

* A **general space modeled on $\mathcal{G}$** is one 

  * that is _probeable_ by objects of $\mathcal{G}$ in that it is an object in the [[(∞,1)-category of (∞,1)-presheaves]]

    $$
      X \in PSh(\mathcal{G}) = (\infty,1)Func(\mathcal{G}^{op}, \infty Grpd)
    $$

  * and consistently so, in that satisfies the [[∞-stack]]-condition that makes it sit in an [[(∞,1)-category of (∞,1)-sheaves]] on $\mathcal{G}$

    $$
      Sh(\mathcal{G}) \stackrel{\leftarrow}{\to}
      PSh(\mathcal{G})
    $$

   (See [[motivation for sheaves, cohomology and higher stacks]] for the general philosophy here).

* A **geometric space modeled on $\mathcal{G}$** -- a $\mathcal{G}$-[[generalized scheme]] -- is a space not only probeable by objects of $\mathcal{G}$, but one that is a [[structured (∞,1)-topos]] that is locally _equivalent_ to objects of $\mathcal{G}$:

  * there is a canonical way to regard every object $U \in \mathcal{G}$ as a [[structured (∞,1)-topos]] $(Sh(U), \mathcal{O}_U)$ where

    * $Sh(U)$ is the [[(∞,1)-topos]] of [[∞-stack]]s on $U$

    * $\mathcal{O}_U$ is the more or less obvious $\mathcal{G}$-valued element of $Sh_U$.

  * using this we can say when a general $\mathcal{G}$-[[structured (∞,1)-topos]] is locally equivalent to one of the form $(Sh(U), \mathcal{O}_U)$ -- these are the $\mathcal{G}$-[[generalized scheme]]s

  * and a generalized space $X$ modeled on $\mathcal{G}$ is a geometric space if it is represented by such a generalized scheme in that 

    $$
      X : U \mapsto Hom((Sh(U), \mathcal{O}_U) 
          , (\mathcal{X}, \mathcal{O}))
      \,.
    $$

**fact** (roughly) 

the inclusion of geometric spaces into all $\infty$-presheaves does land in the $\infty$-shaves, hence in the general spaces, and as such is a [[full and faithful functor]] 

**proof**

the second statement is theorem 2.4.1, the first one is lemma 2.4.13 in 

* [[Jacob Lurie]], [[Structured Spaces]]



## sheaves on $(\infty,1)$-toposes ##


In this approach we entirely switch from thinking about a space to thinking about an [[(∞,1)-topos]] thought of as the collection of [[∞-stack]]s on that space.

But we also want to be talking about generalized sheaves _on_ our generalized spaces. This is actually easy: for $\mathcal{C}$ any [[(∞,1)-category]] with finite limits, 
a $\mathcal{C}$-valued sheaf on  $(\mathcal{X}, \mathcal{O})$ is a small limit preserving functor $\mathcal{X}^{op} \to \mathcal{C}$. 

If we think of $\mathcal{X} = Sh(C)$ as being the [[∞-stack]] [[(∞,1)-topos]] on a [[site]] $C$, then
by the [[nLab:Yoneda lemma for (∞,1)-categories]] every object in the [[(∞,1)-topos]] $\mathcal{X}$ is a [[colimit]] of [[representable functor|representables]], which means that such a sheaf is fixed by its value on representables, i.e. on objects in $C$, as one would expect.


In particular, every object of $\mathcal{X}$ gives a sheaf on $\mathcal{X}$ this way.

## spaces with $E_\infty$-ring valued structure sheaves ##

For the applications to [[elliptic cohomology]] and [[derived elliptic curve]]s our [[geometry (for structured (∞,1)-toposes)|geometry]] $\mathcal{G}$ is the opposite [[(∞,1)-category]] of [[E-∞ ring]]s.

This case hasn't been fully spelled out yet, it is supposed to be the content of

* [[Jacob Lurie]], [[Spectral Schemes]].

But heuristically it is clear that everything works "as for ordinary rings, but up to homotopy". So we proceed with fingers crossed.


# the derived moduli space of elliptic curves #

With the above machinery for [[higher geometry]] in hand, we now set out to describe the particular application that we are interested in: the study of the derived [[moduli stack]] of [[derived elliptic curve]]s.

## derived elliptic curves ##


* [[derived elliptic curve]]

$$
  A \mapsto E(A)
$$

## the derived moduli stack ##

Here is in words what this is all about:

+-- {: .standout}

We do have a generalized space of derived ellictpic curves $E$. 

**Question**: is this a geometric space?

**Answer** Yes. It is represented by a derived scheme.

=--



Let $\mathcal{M}_{1,1}$ be the ordinary [[moduli stack]] of [[elliptic curve]]s. 


Using constructions in [[nLab:elliptic cohomology]] we may associate to each [[nLab:elliptic curve]] over $R$, i.e. each morphism $\phi : Spec R \to \mathcal{X}$, an [[nLab:E-infinity ring]] $E_\phi$ -- the multiplicative spectrum that represents the elliptic cohomology theory given by $T$.

This gives an $E_\infty$-ring valued structure sheaf

$$
  \mathcal{O}^{Der} : (\phi : Spec R \to \mathcal{X}) \mapsto
  E_\phi
  \,.
$$


**Question** What, if anything, is this derived stack a derived [[moduli stack]] of?




## the classification of derived elliptic curves ##


The big theorem is that the derived space $(\mathcal{X}, \mathcal{O}^{Der})$ classifies derived elliptic curves over $E_\infty$-rings

This is the theorem that we said above we wanted to consider, stated now a little bit more precisely.


+-- {: .un_theorem }
###### Theorem
**(J. Lurie)**

For

* $A$ any [[E-∞ ring]]

* and $E(A)$ is the space of [[derived elliptic curve]]s over $A$ (the realization of the topological category of elliptic curves over $A$).

we have an equivalence

$$
  Hom(Spec A, (\mathcal{X}, \mathcal{O}^{Der}))  
  \simeq
  E(A)
$$

naturally in $A$.

=--


+-- {: .proof}
###### Proof

We proceed in these steps:

1. consider the presheaf of preoriented ellitptic curves $E'(A)$ first

1. observe that this restricted to ordinary rings produces the ordinary moduli stack

1. notice that every oo-stack with good deformation theory that restricts this way is a derived Deligne-Mumford stack $(\mathcal{X}, \mathcal{O}')$ that assigns connective $E_\infty$-rings over affines

1. let $\omega$ be the line bundle on $\mathcal{M}_{1,1}$ regarded as a coheren sheaf. There is then from the preorientation of the universal curve over $(\mathcal{M}, \mathcal{O}')$ a morphism

   $$
     \beta : \omega \to \pi_2 \mathcal{O}'
   $$

1. let $\mathcal{O}$ be the sheaf obtained from $\mathcal{O}'$ by inverting $\beta$

1. show that

   1. for $n = 2 k $ we have an isomorphism $\omega^k \to \pi_{2 k}\mathcal{O}$

   1. for $n = 2 k + 1$ we have an isomorphism $0 \to \pi_{2k +1}\mathcal{O}$

      strategy: reduce to neighbourhood of a point

1. notice that this implies the desired statement

=--
