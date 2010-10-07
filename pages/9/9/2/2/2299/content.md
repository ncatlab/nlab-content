
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Higher geometry studies [[vertical categorification]]s of the notions of [[space]] and [[geometry]].

What exactly the rules of higher geometry are is still a bit in the making. A very encompassing framework has been proposed in

* [[Jacob Lurie]], _[[Structured Spaces]]_ .

Here the notion of [[geometry (for structured (∞,1)-toposes)|geometry is formalized]]  in the form of an [[(∞,1)-category]] $\mathcal{G}$ whose objects play the role of test-spaces on which all other [[space]]s are modeled, in a hierarchy of generalized objects:

* [[geometry (for structured (∞,1)-toposes)|test spaces]] $\hookrightarrow$
  [[generalized scheme|spaces locally equivalent to test spaces]]
  $\hookrightarrow$
  [[structured (∞,1)-topos|concrete spaces with structure sheaves taking values in test spaces]]
  $\hookrightarrow$
  [[∞-stack|spaces probeable by test spaces]].

technically modeled by:

* [[geometry (for structured (∞,1)-toposes)]] $\mathcal{G}$
  $\hookrightarrow$
  [[generalized scheme]]s
  $\hookrightarrow$
  formal duals to $\mathcal{G}$-[[structured (∞,1)-topos]]es
  $\hookrightarrow$
  [[(∞,1)-topos]] of [[∞-stack]]s on $\mathcal{G}$.

A plethora of proposals for formalizations of higher geometry find their home in this pattern, for instance most of the concepts listed at [[generalized smooth space]].

A notable exception to this is possibly the program by [[Maxim Kontsevich]] and others where under the term [[noncommutative geometry]] and [[derived noncommutative geometry]] spaces are modeled as the formal dual to [[A-∞-categories]]. But $A_\infty$-categories are presentations for [[stable (∞,1)-categories]] and by the <a href="http://ncatlab.org/nlab/show/stable+(infinity%2C1)-category#StabGiraud">stable Giraud theorem</a> _presentable_ stable $(\infty,1)$-categories play a very similar role to (unstable) [[∞-stack]] [[(∞,1)-topos]]es. In particular they may be obtained from the latter by [[stabilization]]. 

## Derived geometry {#derived}

Higher geometry has been particularly popularized in terms of **derived geometry**, notably [[derived algebraic geometry]].

In typical usage the qualifier _derived_ here (which otherwise can mean many things in [[homotopy theory]] and [[higher category theory]]) is meant to emphasize that the collection $\mathcal{G}$ of test spaces is a genuine [[(∞,1)-category]] instead of just a plain 1-[[category]]. Accordingly [[∞-stack]]s on $\mathcal{G}$ are then called [[derived stack]]s (see there for more on this).

The point of amplifying this, historically, is that typically only with a suitble higher category $\mathcal{G}$ of test spaces, the [[limit]]s and the [[intersection theory]] of the generalized spaces behaves nicely.

The standard and motivating example for this to keep in mind is the case of  [[derived algebraic geometry]] where the [[site]] $\mathcal{G} = $ [[CRing]]${}^{op}$ of formal duals to ordinary commutative rings is generalized to the site $\mathcal{G} = sCRing^{op}$ of formal duals to [[simplicial ring]]s (and then further to that of formal duals of [[E-∞-ring]]s):

where an ordinary [[affine scheme]] $Spec R$ has a [[ring]] $R$ of functions on it, a [[derived scheme]] $Spec R_\bullet$ has a [[simplicial ring]] of functions on it. Under the [[monoidal Dold-Kan correspondence]] this is equivalently a non-positively graded cochain [[dg-algebra]] $N^\bullet(R_\bullet)$:

$$
  functions\;on\;Spec R_\bullet \simeq
  ( \cdots \stackrel{d}{\to}R_{-2}\stackrel{d}{\to}R_{-1} \stackrel{d}{\to} R_0)
  \,.
$$

If this complex has vanishing cohomology everywhere except in degree 0, it is a homological resolution of the quotient $R_0/ d(R_1)$, which may not itself exist, dually, as a test object in $\mathcal{G}$.

In many fields it is a traditionally a well-known tool that such resolutions encode important information. Standard examples include the [[bar complex]] used to define [[Hochschild cohomology|Hochschild homology]] or the homological resolutuions used in [[BV theory]]. Derived geometry may be understood from this perspective as providing a _geometrical interpretation_ of these techniques. 

For instance from the point of view of derived geometry, the [[Hochschild cohomology|Hochschild homology]] of a ring of functions on an object $X$ is the functions on the [[free loop space object]] $\mathcal{L}X$ of $X$. And the corresponding [[cyclic cohomology]] is the $S^1$-equivariant part of this, where the circle acts in the natural way on the derived loop space $\mathcal{L}X$. If nothing else, this geometric picture makes transparent all of the algebraic structures in [[Hochschild cohomology]] and [[cyclic cohomology]]. See there for more details.


