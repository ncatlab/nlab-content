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

[[!redirects natural numbers objects]]
[[!redirects natural number object]]
[[!redirects natural number objects]]
[[!redirects NNO]]