
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Natural numbers object
* tic
{: toc}

##Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set]]s.  

A **natural numbers object** (NNO) in a topos is an [[object]] that behaves in that topos like the set $\mathbb{N}$ of [[natural number]]s does in [[Set]]; thus it provides a formulation of the "axiom of infinity" in structural [[set theory]] (such as [[ETCS]]).  The definition is due to [[William Lawvere]].


##Definition

### In a topos or CCC

A **natural numbers object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbb{N}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $z :1 \to \mathbb{N}$ from the [[terminal object]] $1$;

  * a [[morphism]] $s : \mathbb{N} \to \mathbb{N}$ (successor);

* such that 

  * for every other [[diagram]] $1 \stackrel{q}{\to}A \stackrel{f}{\to} A$

  * there is a unique morphism $u : \mathbb{N} \to A$ such that

$$
  \array{
    1 &\stackrel{z}{\to}& \mathbb{N} &\stackrel{s}{\to}& \mathbb{N}
  \\
   & {}_q\searrow & \downarrow^{u} && \downarrow^{u}
   \\
  && A &\stackrel{f}{\to} & A
  }
$$

All this may be summed up by saying that a natural numbers object is an [[initial algebra|initial]] [[algebra for an endofunctor|algebra for the endofunctor]] $X \mapsto 1 + X$.
Equivalently, it is an initial [[algebra for an endo-profunctor|algebra for the endo-profunctor]]  $Hom_E(1,=) \times Hom_E(-,=)$.

By the universal property, the natural numbers object is unique up to [[isomorphism]].

### In a general category with finite products

Note that this definition actually makes sense in any category $E$ having finite [[product]]s.  However, if $E$ is not [[cartesian closed category|cartesian closed]], then it is better to explicitly assume a stronger version of this definition "with parameters" (which follows automatically when $E$ is cartesian closed, such as when $E$ is a topos). What this amounts to is demanding that $(\mathbb{N}, z, s)$ not only be a natural numbers object (in the above, unparametrized sense) in $E$, but that also, for each object $A$, this is preserved by the free coalgebra functor into the [[Kleisli category]] of the [[comonad]] $X \mapsto A \times X$ (which may be thought of as the category of maps parametrized by $A$). (Put another way, the finite product structure of $E$ gives rise to a canonical [[self-indexing]], and we are demanding the existence of an (unparametrized) NNO within this [[indexed category]], rather than just within the base $E$).

The functions which are constructable out of the structure of a category with finite products and such a "parametrized NNO" are precisely the [[primitive recursive function|primitive recursive]] ones. Specifically, the unique structure-preserving functor from the free such category $F$ into [[Set]] yields a bijection between $Hom_F(1, \mathbb{N})$ and the actual natural numbers, as well as surjections from $Hom_F(\mathbb{N}^m, \mathbb{N})$ onto the primitive recursive functions of arity $m$ for each finite $m$. With cartesian closure, however, this identification no longer holds, since non-primitive recursive functions (such as the [[Ackermann function]]) become definable as well.


##Finite colimit characterization

In a topos, the natural numbers object $\mathbb{N}$ is uniquely characterized by the following [[colimit]] conditions due to [[Peter Freyd]]: a triple $(\mathbb{N}, 0: 1 \to \mathbb{N}, s: \mathbb{N} \to \mathbb{N})$ is a natural numbers object if and only if 

1. The morphism $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ is an [[isomorphism]]; 

1. The diagram 
$$\mathbb{N} \stackrel{\overset{s}{\to}}{\underset{1}{\to}} \mathbb{N} \to 1$$ 
is a [[coequalizer]]. 

The necessity of the first condition holds in any category with binary coproducts and a terminal object, and the necessity of the second holds in any category whatsoever. 

+-- {: .proof}
###### Proof of necessity
For a category $C$ with binary coproducts and 1, the natural numbers object can be equivalently described as an [[initial algebra]] structure $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ for the endofunctor $F(c) = 1 + c$ defined on $C$. Then condition 1 is a special case of [[initial algebra|Lambek's theorem]], that the algebra structure map of an initial algebra is an isomorphism. 

As for condition 2, given $f: \mathbb{N} \to X$ such that $f = f \circ s$, the claim is that $f$ factors as 

$$\mathbb{N} \overset{!}{\to} 1 \overset{x}{\to} X$$

for some unique $x$, in fact for $x = f(0)$. Uniqueness is clear since $!: \mathbb{N} \to 1$, being a retraction for $0: 1 \to \mathbb{N}$, is epic. On the other hand, substituting either $f$ or $f(0) \circ !$ for $g$ in the diagram 

$$\array{ 
1 & \overset{0}{\to} & \mathbb{N} & \overset{s}{\to} & \mathbb{N} \\ 
 & f(0) \searrow & \downarrow g & & \downarrow g \\ 
 & & X & \underset{1_X}{\to} & X
}$$ 

this diagram commutes, so that $f = f(0) \circ !$ by the uniqueness clause in the universal property for $\mathbb{N}$.
=--

+-- {: .proof}
###### Proof of sufficiency
To be filled in. For a topos in which there is an isomorphism $\alpha: F(X) \to X$, it should be possible to construct a natural numbers object as the intersection of all $F$-subalgebras of $(X, \alpha)$. On the other hand, there are no nontrivial subalgebras of any such algebra satisfying condition 2. 
=--

## Examples

In any [[Grothendieck topos]] $E = Sh(C)$ the natural numbers object is given by the [[constant sheaf]] on the [[set]] of ordinary natural numbers, i.e. by the [[sheafification]] of the [[presheaf]] $C^{op} \to Set$ that is constant on the set $\mathbb{N}$.

There are interesting cases in which such sheaf toposes contain objects that look like they ought to be natural numbers objects but do not satisfy the above axioms: for instance some of the models described at [[Models for Smooth Infinitesimal Analysis]] are sheaf toposes that contain besides the standard natural number object a larger object of **[[smooth natural numbers]]** that has [[generalized element]]s which are "infinite natural numbers" in the sense of [[nonstandard analysis]].

## Properties

Let $f = (f^* \dashv f_*) : E \underoverset{f_*}{f^*}{\leftrightarrows} F$ be a [[geometric morphism]] of toposes. If $N \in F$ is a natural numbers object, then $f^* N$ is a natural numbers object in $E$. ([[Elephant|Elephant, lemma 4.1.14]]). 

In particular, if $E$ is a [[Grothendieck topos]], then there is a unique [[geometric morphism]] $(E^* \dashv \Gamma): E \underoverset{\Gamma}{E^*}{\leftrightarrows} Set$, the [[global section]] geometric morphism. If $E^*$ is the [[exact functor|left exact]] [[left adjoint]], it follows that 

$$E^*(\mathbb{N}) \cong E^*(\sum_{n: \mathbb{N}} 1) \cong \sum_{n: N} E^* 1 \cong \sum_{n: \mathbb{N}} 1,$$ 

with the evident successor and constant $0$, is the natural nunbers object in $E$.  


[[!redirects natural numbers object]]
[[!redirects natural numbers objects]]
[[!redirects natural number object]]
[[!redirects natural number objects]]
[[!redirects NNO]]
