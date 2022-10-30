
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--


***


Write

1. $CartSp$ for the [[site]] of [[Cartesian spaces]] and [[smooth functions]] between them;

1. $InfPoint$ for the [[site]] of [[infinitesimally thickened points]];

1. $CartSp_{th} \hookrightarrow SmoothLocus$ for the [[full subcategory]] of that of [[smooth loci]] on those of the form $\mathbf{U} = U \times D$ with $U \in CartSp$ and $D \in InfPoint$.

$$
  CartSp
   \stackrel{\overset{i}{\hookrightarrow}}{\underset{p}{\leftarrow}}
  CartSp_{th}
   \stackrel{\iota}{\leftarrow}
  InfPoint
$$

where 

* $i \colon U \mapsto U \times *$;

* $p \colon U \times D \mapsto U$

* $\iota \colon D \mapsto * \times D$


$$
  Sh(CartSp)
   \stackrel{}{\stackrel{\overset{Lan_i}{\hookrightarrow}}{\stackrel{\overset{(-)\circ i}{\leftarrow}}{\stackrel{\overset{(-)\circ p}{\hookrightarrow}}{\underset{Ran_p}{\leftarrow}}}}}
  Sh(CartSp_{th})
   \stackrel{\overset{Lan_\iota}{\leftarrow}}{\underset{(-)\circ \iota}{\to}}
  Sh(InfPoint)
$$


+-- {: .num_prop }
###### Proposition

The sequence of [[geometric morphisms]]

$$
  Sh(CartSp) \stackrel{p^*}{\to} Sh(CartSp_{th}) \stackrel{\iota^*}{\to} Sh(InfPoint)
$$

exhibit a [[homotopy cofiber sequence]] in [[(∞,1)Topos]].

=--

+-- {: .proof}
###### Proof

By the discussion at _[(∞,1)Topos -- Existence of limits and colimits](%28infinity%2C1%29Topos#ExistenceOfLimitsAndColimits)_ the statement is equivalently that the [[inverse image]] functors

$$
  Sh(CartSp) 
    \stackrel{Lan_p}{\leftarrow}
  Sh(CartSp_{th})
    \stackrel{Lan_\iota}{\leftarrow}
  Sh(InfPoint)
$$

form a [[homotopy fiber sequence]] in [[(∞,1)Cat]]. Computing this is the [[model structure for quasi-categories]] after passing to [[nerves]], the morphism $N(Lan_p)$ is clearly an [[inner Kan fibration]] because of the [[subcategory]] inclusion $Sh(CartSp) \hookrightarrow Sh(CartSp_{th})$, and so by the general discussion at [[homotopy pullback]] the homotopy fiber is given by the 1-categorical fiber of $N(Lan_p)$ in [[sSset]]. By the discussion at _[Left Kan extension - on representables](http://ncatlab.org/nlab/show/Kan+extension#LeftKanOnRepresentables)_ $Lan_p$ acts as $p$ on [[representable functor|representables]]. The 1-categorical fiber of $N(p) \colon N(CartSp_{th}) \to N(CartSp)$ is evidently $N(InfPoint)$.

=--


category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects ??? ????]]
[[!redirects Featured math : Quora]]
