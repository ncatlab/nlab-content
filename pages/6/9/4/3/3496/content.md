
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A [[geometric morphism]] $f : E \to F$ between [[topos]]es is a [[functor]] of the underlying categories that is consistent with the interpretation of $E$ and $F$ as generalized [[topological space]]s. 

If $F = Set = Sh(*)$ is the terminal [[sheaf topos]], then $E \to Set$ is essential if $E$ is a [[locally connected topos]]. In general, $f$ being essential is a necessary (but not sufficient) condition to ensure that $f$ behaves like a map of topological spaces whose [[fiber]]s are locally connected: that it is a [[locally connected geometric morphism]].


## Definition

Given a geometric morphism $(f^* \dashv f_*) : E \to F$, it is an **essential geometric morphism** if the [[inverse image]] functor $f^*$ has not only the [[right adjoint]] $f_*$, but also a [[left adjoint]] $f_!$:

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  F
  \,.
$$


### Refinements

There are various further conditions that can be imposed on a geometric morphism:

* If $f_!$ can be made into an $E$-[[indexed functor]] and $f^*$ satisfies some extra conditions, the geometric morphism $f$ is a [[locally connected geometric morphism]] (see there for details).

* If $f_!$ preserves finite [[product]]s then $f$ is called **connected surjective**.

* If $f_!$ preserves finite [[product]]s and moreover there is a further functor $f^! : F \to E$ which is  [[right adjoint]] $(f_* \dashv f^!)$ and [[full and faithful functor|full and faithful]], i.e. if we have a sequence of adjunctions

  $$
    (f_! \dashv f^* \dashv f_* \dashv f^!)
  $$

  with full and faithful $f^!$ then the geometric morphism $f$ is called **[[local geometric morphism]]**.

  In this case in particular $F \stackrel{\overset{p_*}{\leftarrow}}{\underset{p^!}{\hookrightarrow}} E$

  is a [[geometric embedding]] and hence makes $F$ a subtopos of $E$.

## Properties

+-- {: .un_prop}
###### Proposition

For every $\phi : X \to f^* f_* A$ in $E$ the diagram

$$
  \array{
    X &\stackrel{\phi}{\to}& f^* f_* A
    \\
    \downarrow && \downarrow
    \\
    f^* f_! X &\stackrel{}{\to}& A
  }
$$

commutes, where the vertical morphisms are unit and counit, respectively, and where the bottom horizontal morphism is the [[adjunct]] of $\phi$ under the composite adjunction $(f^* f_! \dashv f^* f_*)$.

=--

+-- {: .proof}
###### Proof

The morphism $\phi : X \to f^* f_* A$ is the component of a [[natural transformation]]

$$
  \array{
    *&&\overset{X}{\to}&& E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow 
    \\
    E &\underset{f_*}{\to}&F
  }
  \,.
$$

The composite $X \stackrel{\phi}{\to}  f^* f_* A \to A$ is the component of this composed with the counit $f^* f_* \Rightarrow Id$.

We may insert the 2-identity given by the zig-zag law

$$
  \cdots \;\;\; = \;\;\;
  \array{
    *&&\overset{X}{\to}&& E && = && E
    \\
    {}^{\mathllap{A}}\downarrow
    &\Downarrow^\phi&& {}^{\mathllap{f^*}}\nearrow &\Downarrow& \searrow^{f_!} 
    &\Downarrow& \nearrow_{\mathrlap{f^*}}
    \\
    E &\underset{f_*}{\to}&F &&=&& F   
  }
  \,.
$$

Composing this with the counit $f^* f_* \Rightarrow Id$ produces the transformation whose component is manifestly the morphism $X \to f^* f_! X \to A$.

=--


## Examples

### Etale geometric morphisms

For any morphism $f\colon A\to B$ in a topos $E$, the induced geometric morphism $f\colon E/A \to E/B$ of [[overcategory]] [[topos]]es is essential. 

For the case $B = *$ the [[terminal object]], the geometric morphism

$$
  \pi : E/A \to E
$$

is also called an [[etale geometric morphism]].

### Locally connected toposes

A [[locally connected topos]] $E$ is one where the [[global section]] [[geometric morphism]] $\Gamma : E \to Set$ is essential. 

$$
  (f_! \dashv f^* \dashv f_*) \;\;\; : \;\;\;
  E
    \stackrel{\overset{\Pi_0}{\to}}{\stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}}}
  Set
  \,.
$$

In this case, the functor $\Gamma_! = \Pi_0 : E \to Set$ sends each object to its set of connected components.  More on this situation is at [[homotopy groups in an (∞,1)-topos]].  

Note, though that if $p\colon E\to S$ is an arbitrary geometric morphism through which we regard $E$ as an $S$-topos, i.e. a topos "in the world of $S$," the condition for $E$ to be locally connected as an $S$-topos is not just that $p$ is essential, but that the left adjoint $p_!$ can be made into an $S$-[[indexed functor]] (which is automatically true for $p^*$ and $p_*$).  This is automatically the case for $Set$-toposes (at least, when our [[foundation]] is [[material set theory]]---and if our foundation is [[structural set theory]], then our large categories and functors all need to be assumed to be $Set$-indexing anyway). For more see [[locally connected geometric morphism]].


## References

The definition of geometric morphism appears before Lemma A.4.1.5 in

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ 

Connected surjective and local geometric morphisms are discussed in 

* [[Peter Johnstone]], [[Ieke Moerdijk]], _Local maps of toposes_ Proceedings London Mathematical Society 58 (1989), 281-305.

Further refinements are in 

* [[Bill Lawvere]], _Axiomatic cohesion_ Theory and Applications of Categories, Vol. 19, No. 3, 2007, pp. 41&#8211;49. ([pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf))


[[!redirects essential geometric morphisms]]