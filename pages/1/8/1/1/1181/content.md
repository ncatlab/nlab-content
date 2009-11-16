#Idea#

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set]]s.  A _natural numbers object_ in a topos is an [[object]] that behaves in that topos like the set $\mathbb{N}$ of [[natural number]]s does in [[Set]]; thus it provides a formulation of the "axiom of infinity" in structural [[set theory]] (such as [[ETCS]]).  The definition is due to <a href="http://en.wikipedia.org/wiki/William_Lawvere">William Lawvere</a>.

#Definition#

A **natural numbers object** in a [[topos]] $E$ is 

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

Note that this definition actually makes sense in any category $E$ having finite [[product]]s.  However, if $E$ is not [[cartesian closed category|cartesian closed]], then it is better to explicitly assume a stronger version of this definition "with parameters" (which follows automatically when $E$ is cartesian closed, such as a topos). 

#Finite colimit characterization# 

In a topos, the natural numbers object $\mathbb{N}$ is uniquely characterized by the following colimit conditions due to Freyd: a triple $(\mathbb{N}, 0: 1 \to \mathbb{N}, s: \mathbb{N} \to \mathbb{N})$ is a natural numbers object if and only if 

1. The morphism $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ is an isomorphism; 

1. The diagram 
$$\mathbb{N} \stackrel{\overset{s}{\to}}{\underset{1}{\to}} \mathbb{N} \to 1$$ 
is a coequalizer. 

The necessity of the first condition holds in any category with binary coproducts and a terminal object, and the necessity of the second holds in any category whatsoever. 

**Proof of necessity:** For a category $C$ with binary coproducts and 1, the natural numbers object can be equivalently described as an [[initial algebra]] structure $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ for the endofunctor $F(c) = 1 + c$ defined on $C$. Then condition 1 is a special case of [[initial algebra|Lambek's theorem]], that the algebra structure map of an initial algebra is an isomorphism. 

As for condition 2, given $f: \mathbb{N} \to X$ such that $f = f \circ s$, the claim is that $f$ factors as 

$$\mathbb{N} \overset{!}{\to} 1 \overset{x}{\to} X$$

for some unique $x$, in fact for $x = f(0)$. Uniqueness is clear since $!: \mathbb{N} \to 1$, being a retraction for $0: 1 \to \mathbb{N}$, is epic. On the other hand, substituting either $f$ or $f(0) \circ !$ for $g$ in the diagram 

$$\array{ 
1 & \overset{0}{\to} & \mathbb{N} & \overset{s}{\to} & \mathbb{N} \\ 
 & f(0) \searrow & \downarrow g & & \downarrow g \\ 
 & & X & \underset{1_X}{\to} & X
}$$ 

this diagram commutes, so that $f = f(0) \circ !$ by the uniqueness clause in the universal property for $\mathbb{N}$. $\Box$ 

**Proof of sufficiency:** To be filled in. For a topos in which there is an isomorphism $\alpha: F(X) \to X$, it should be possible to construct a natural numbers object as the intersection of all $F$-subalgebras of $(X, \alpha)$. On the other hand, there are no nontrivial subalgebras of any such algebra satisfying condition 2. 
 



[[!redirects natural numbers objects]]
[[!redirects natural number object]]
[[!redirects natural number objects]]
[[!redirects NNO]]