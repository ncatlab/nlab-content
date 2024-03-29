[[!redirects Steenrod-Wockel approximation theorem]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Steenrod-approximation theorem_ states mild conditions under which an extension of a [[smooth function]] on a [[closed subset]] by a [[continuous function]] may itself be improved to an extension by a smooth function.

This is a smooth enhancement of the [[Tietze extension theorem]].

## Statement


+-- {: .num_theorem }
{#GeneralizedSteenrodTheorem}
###### Theorem


Let $X$ be a finite [[dimension]]al [[connected]] [[smooth manifold]] [[manifold with corners|with corners]]. Let $\pi : E \to X$ be a locally trivial [[Diff|smooth]]  [[bundle]] with a [[locally convex]] [[manifold]] $N$ as typical [[fiber]] and $\sigma : X \to E$ a [[continuous function|continuous]] [[section]].

If $L \subset X$ is a [[closed subset]] and $U \subset X$ is an [[open subset]] such that $\sigma$ is [[smooth function|smooth]] in a [[neighbourhood]] of $L \setminus U$, then:

1. for each [[open neighbourhood]] $O$ of $\sigma(X)$ in $E$ there exists a [[section]] $\tau : X \to O$ 

   * which is [[smooth function|smooth]] in a neighbourhood of $L$;

   * and which equals $\sigma$ on $X \setminus U$;

1. there exists a [[homotopy]] $F : [0,1] \times X \to O$ between $\sigma$ and $\tau$ such that

   * each $F(t,-)$ is a section of $\pi$;

   * for $(t,x) \in [0,1] \times (X \setminus U)$ we have $F(t,x) = \sigma(x) = \tau(x)$.

=--

See ([Wockel](#Wockel))


$$
  \array{
    && O &\stackrel{id}{\to} & O &  \stackrel{id}{\to}& O
    \\
    & {}^{\mathllap{smooth}}\nearrow
    &
    {}_{\mathllap{\sigma|_{X \setminus U}}}\uparrow
     = \uparrow_{\mathrlap{\tau|_{X \setminus U}}} 
    && 
   \uparrow^{\mathrlap{\sigma}}
    & \swArrow_F& 
    \uparrow^{\exists \tau}
    & \nwarrow^{\mathrlap{smooth}}
    \\
    L \setminus U &\hookrightarrow & X \setminus U 
    &\hookrightarrow& X 
    &\stackrel{id}{\to}&
   X
   &\stackrel{}{\hookleftarrow}& L
  }
$$

## Examples

### Smoothing of delayed homotopies {#SmoothingOfDelayedHomotopies}

+-- {: .un_corollary}
###### Corollary

Let $f,g : Z \to Y$ be two [[smooth function]]s between [[smooth manifold]]s. Let  $\eta : Z \times [0,1] \to Y$ be a continuous [[delayed homotopy]] between them, constant in a [[neighbourhood]] $Z \times ([0,\epsilon) \coprod (1-\epsilon,1])$.

Then there exists also smooth homotopy between $f$ and $g$ which is itself continuously homotopic to $\eta$.

=--


+-- {: .proof}
###### Proof


To apply the [generalized Steenrod theorem](#GeneralizedSteenrodTheorem) with the notation as stated there, make the following identifications

* set $X \coloneqq Z \times [0,1]$;

* set $N = Y$;

* let $E = Z \times [0,1] \times Y$ be the trivial $Z$-bundle over $X$

  (so that sections of $E$ are equivalently functions $Z \times[0,1] \to Y$)

* let $(\sigma : X \to E) := (\eta : Z \times [0,1] \to Y)$ be the given continuous homotopy;

* set $L \coloneqq Z \times [0,1]$;

* let $U \coloneqq Z \times (0,1)$.

Then because by assumption $\eta$ is a continuous [[delayed homotopy]] between [[smooth function]]s, it follows that $\sigma$ is smooth in a neighbourhood $Z \times ([0,\epsilon) \coprod (1-\epsilon,1])$ of $L$.

So the theorem applies and provides a smooth  homotopy

$$
  \tau \colon [0,1] \times Z \to Y
$$

which moroever is itself (continuously) homotopic to $\eta$ via some continuous $F : [0,1] \times [0,1] \times Z \to Y$.

=--


## Related theorems

* the [[Hadamard lemma]]

* [[Borel's theorem]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* [[embedding of smooth manifolds into formal duals of R-algebras]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]





## References

* [[Norman Steenrod]], Section 6.7 of: _The topology of fibre bundles_, Princeton Mathematical Series **14**, Princeton Univ. Press (1951) &lbrack;[jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5)&rbrack;

* [[Morris Hirsch]], Chapter 2.2 (Thm. 2.5) in: _Differential topology_, Springer Graduate Texts in Mathematics **33** (1976) &lbrack;[doi:10.1007/978-1-4684-9449-5](https://link.springer.com/book/10.1007/978-1-4684-9449-5), [gBooks](http://books.google.com/books/about/?id=iSvnvOodWl8C)&rbrack;

* {#Wockel} [[Christoph Wockel]], _A Generalisation of Steenrod's Approximation Theorem_, Archivum mathematicum **45** 2 (2009) &lbrack;[arXiv:0610252](http://arxiv.org/abs/math/0610252)&rbrack;



