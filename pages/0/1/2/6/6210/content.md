
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $c$ any [[characteristic class]], its [[homotopy fibers]] on [[cocycle]] [[∞-groupoid]]s represent $c$-[[twisted cohomology]] (for instance [[twisted bundle]]s, [[twisted spin structures]], etc.).

If $c$ is refined to a characteristic class $\mathbf{c}$ in [[Smooth∞Grpd]] there may exist further refinements $\hat {\mathbf{c}}$ to [[ordinary differential cohomology]]. The twisted cohomology of these _differential characteristic classes_ may be called _twisted differential structures_ . For instance _[[differential string structure]]s_ . See [below](#Examples) for more examples.

These structures have a natural interpretation and play a natural roles as _[[physical fields]]_ (see there for a comprehensive discussion).



## Definition

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]], usually $\mathbf{H} = $ [[Smooth∞Grpd]] or [[SynthDiff∞Grpd]] or the like.

Let $K, G$
be [[∞-group]] objects in $\mathbf{H}$ and let 


$$
  \mathbf{c} : \mathbf{B}G \to \mathbf{B}K
$$

be a morphism of their [[delooping]] objects / [[moduli stacks]].

+-- {: .num_defn}
###### Definition

For $X \in \mathbf{H}$ any object and $P \to X$
an $K$-[[principal ∞-bundle]] over $X$, the [[∞-groupoid]]

$$
  \mathbf{c}Struc_{[P]}(X)
  :=
  \mathbf{H}(X, \mathbf{B}G) \times_{\mathbf{H}(X, \mathbf{B}K)} \{P\}
  \,,
$$

hence the [[(∞,1)-pullback]]

$$
  \array{
    \mathbf{c}Struc_{[P]}(X)
    &\to&
    *
    \\
    \downarrow^{\mathrlap{P}} && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}G)
    &\stackrel{\mathbf{H}(X, \mathbf{c})}{\to}&
    \mathbf{H}(X, \mathbf{B}K)
  }
$$

we may call equivalently

* the $\infty$-groupoid of $K$-structures on $P$ (with respect to the given $\mathbf{c}$);

* the $\infty$-groupoid of $[P]$-twisted $\mathbf{c}$-structures.

=--

+-- {: .num_remark}
###### Remark

As discussed at _[[twisted cohomology]]_, we may think of an object in 
$\mathbf{c}Struc_{[P]}(X)$ as a [[section]] (up to [[homotopy]]) $\sigma$

$$
  \array{
    && \mathbf{B}G
    \\
    & {}^{\sigma}\nearrow& \downarrow^{\mathbf{c}}
    \\
    X &\stackrel{g}{\to}& \mathbf{B}K
  }
$$

where we think of $\mathbf{c}$ as being the **universal twisting $\infty$-bundle** and where $g : X \to \mathbf{B}K$ is a morphism presenting $P$.

=--

The following definition looks at a differential refinement of this situation.

+-- {: .num_defn}
###### Definition

For $\mathbf{c} : \mathbf{B}G \to \mathbf{B}^n U(1)$ a [[characteristic class|characteristic map]]
in $\mathbf{H}$ and $\hat {\mathbf{c}} : \mathbf{B}G_{\mathrm{conn}}
  \to \mathbf{B}^n U(1)_{\mathrm{conn}}$ its differential refinement,
sending [[connections on ∞-bundles]] to [[circle n-bundles with connection]] (see [[∞-Chern-Weil homomorphism]], we may think of this also as an [[extended Lagrangian]] for a [[higher gauge theory]]).

We write $\hat {\mathbf{c}}\mathrm{Struc}_{\mathrm{tw}}(X)$ for the 
  corresponding [[twisted cohomology]], 

$$
  \array{
    \hat {\mathbf{c}}Struc_{tw}(X) &\stackrel{tw}{\to}& 
    H^{n+1}_{diff}(X)
    \\
    {}^{\mathllap{\chi}}\downarrow && \downarrow
    \\
    \mathbf{H}(X, \mathbf{B}G_{conn})
     &
     \stackrel{\hat \mathbf{c}}{\to}
     &
    \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
  }
  \,.
$$  

=--

## Examples
 {#Examples}

Twisted differential $\mathbf{c}$-structures appear in various guises in the [[background gauge field]]s of  [[string theory]] application. 

* [[reduction of structure groups]]

  * [[orthogonal structure]] / [[Riemannian metric]]; see the discussion at _[[vielbein]]_ . 

  * [[generalized complex geometry]]

  * [[exceptional generalized geometry]]

* [[lift of structure groups]]

* Higher differential spin structures 

  * [[twisted spin structure]], [[differential spin structure]]

  * [[twisted spin^c-structure]]

  * [[twisted differential string structure]]

  * [[supergravity C-field]]

  * [[twisted differential fivebrane structure]]

  * [[twisted Wu structure]]

* [[p1-structure]] 

  [[2-framing]]
  
* [[w4-structure]] 

  [[w4-orientation of EO(2)-theory]]

* [[differential T-duality]]

## Related concepts

* [[reduction and lift of structure groups]]

* [[field (physics)]]


## References

The notion was introduced in

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_
  {#SSSIII}

and expanded on in

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech cocycles for differential characteristic classes]]_
 {#FSS}

An exposition is in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_ 

Lecture notes include

* [[Urs Schreiber]], _[[twisted smooth cohomology in string theory]]_, Lectures at the ESI-institute (June 2012)

A general account is in section 5.2 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

In 

* [[Daniel Freed]], [[Constantin Teleman]], _Relative quantum field theory_ ([arXiv:1212.1692](http://arxiv.org/abs/1212.1692))
 {#FreedTeleman}

it is proposed to call such twisted structures "relative fields". 

[[!redirects c-structure]]

[[!redirects twisted differential c-structure]]
[[!redirects twisted differential c-structures]]
[[!redirects tiwsted differential c-structure]]

[[!redirects twisted differential structure]]
[[!redirects twisted differential structures]]