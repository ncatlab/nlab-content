[[!redirects tubular neighbourhood]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn #TubularNeighbourhood}
###### Definition

For $i : X \hookrightarrow Y$ an [[embedding]] of [[manifold]]s, a **tubular neighbourhood** of $X$ in $Y$ is

* a real [[vector bundle]] $E \to X$;

* an extension of $i$ to an [[isomorphism]]

  $$
    \hat i \;\colon\; E \to U_{i(X)}
  $$

  with an [[open neighbourhood]] of $X$ in $Y$.

=--

+-- {: .num_remark}
###### Remark

The [[derivative]] of $\hat i$ provides an [[isomorphism]] of $E$ with the [[normal bundle]] $\nu_{X/Y}$ of $X$ in $Y$.

=--

## Properties

### General

+-- {: .num_prop}
###### Proposition
**([[tubular neighbourhood theorem]])**

Every [[embedding]] of [[smooth manifolds]] does admit a tubular neighbourhood, def. \ref{TubularNeighbourhood}.

=--

For instance ([DaSilva, theorem 3.1](#DaSilva)).

Moreover, tubular neighbourhoods are unique _up to [[homotopy]]_ in a suitable sense:

+-- {: .num_defn}
###### Definition

For an embedding $i : X \to Y$, write $Tub(i)$ for the [[topological space]] whose underlying set is the set of tubular neighbourhoods of $i$ and whose [[topology]] is the [[subspace topology]] of $Hom(N_i X, Y)$ equipped with the [[C-infinity topology]].

=--

+-- {: .num_prop}
###### Proposition

If $X$ and $Y$ are [[compact space|compact]] [[manifold]]s, then $Tub(i)$ is [[contractible]] for all [[embedding]]s $i : X \to Y$.

=--

This appears as ([Godin, prop. 31](#Godin)).

These statements generalize to [[equivariant differential topology]]:


+-- {: .num_prop #ExistenceOfGInvariantTubularNeighbourhoods}
###### Proposition
**(existence of $G$-invariant [[tubular neighbourhoods]])**

Let $X$ be a [[smooth  manifold]], $G$ a [[Lie group]] and $\rho \;\colon\; G \times X \to X$ a _[[proper action|proper]]_ [[action]] by [[diffeomorphisms]].

If $\Sigma \overset{\iota}{\hookrightarrow} X$ is a [[closed manifold|closed]] [[smooth manifold|smooth]] [[submanifold]] inside the $G$-[[fixed locus]]

\begin{center}
  \begin{xymatrix}
    \Sigma 
    \ar@{^{(}->}[rr]^-{\iota^G}
    \ar@{^{(}->}[dr]_{\iota}
    &&
    X^G
    \ar@{^{(}->}[dl]
    \\
    & 
    X
  \end{xymatrix}
\end{center}


then $\Sigma$ has a [[tubular neighbourhood]] $\Sigma \subset U \subset X$ which is "$G$-invariant" in that the $G$-[[action]] [[restriction|restricts]] to an [[action]] $G \times U \longrightarrow U$.

Moreover, any two choices of such $G$-invariant tubular neighbourhoods are $G$-equivariantly [[isotopy|isotopic]].

=--

([Bredon 72 VI Theorem 2.2](#Bredon72), [Kankaanrinta 07, theorem 4.4, theorem 4.6](equivariant+differential+topology#Kankaanrinta07))


### Pullbacks of tubular neighbourhoods



(...) [[propagating flow]] (...) ([Godin](#Godin)).


## Related concepts

* [[tubular neighbourhood of a mapping space]]

* key application: [[Pontrjagin-Thom collapse map]]

## References

Basics on tubular neighbourhoods are reviewed for instance in

* {#DaSilva} [[Ana Cannas da Silva]], section 3 of _Prerequisites from differential geometry_ ([pdf](http://www.math.princeton.edu/~acannas/appendix_dg.pdf))

* {#Kochmann96} [[Stanley Kochmann]], section 1.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996
 
Discussion in the generality of [[equivariant differential topology]] includes

* {#Bredon72} [[Glen Bredon]], Chapter VI.2 of _Introduction to compact transformation groups_, Academic Press 1972 ([pdf](http://www.indiana.edu/~jfdavis/seminar/Bredon,Introduction_to_Compact_Transformation_Groups.pdf))



The homotopical uniqueness of tubular neighbourhoods is discussed in

* {#Godin} [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 

For an analogue in homotopical algebraic geometry see

* [[Marc Levine]], _Motivic tubular neighborhoods_, [pdf](http://www.uni-due.de/~bm0032/publ/TubNbdDocumenta.pdf)

see also

* wikipedia [tubular neighborhood](http://en.wikipedia.org/wiki/Tubular_neighborhood)


[[!redirects tubular neighbourhoods]]

[[!redirects tubular neighborhood]]
[[!redirects tubular neighborhoods]]


