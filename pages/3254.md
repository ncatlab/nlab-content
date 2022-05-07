

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For every [[topological space]] $X$ there is a [[CW complex]] $Z$ and a [[weak homotopy equivalence]] $f  \colon Z\to X$. Such a map $f  \colon Z\to X$ is called a **CW approximation** to $X$.

Such CW-approximation may be constructed case-by-case by iteratively [[cell attachment|attaching cells] (starting from the [[empty space]]]) for each representative of a [[homotopy group]] of $X$ and further cells to kill off spurious homotopy groups introduced this way (e.g. [Hatcher, p. 352-353](#Hatcher)).

In the [[classical model structure on topological spaces]] $Top_{Quillen}$, the [[cofibrant objects]] are the [[retracts]] of [[cell complexes]], and hence CW approximations are in particular cofibrant replacements in this model structure.

The [[Quillen equivalence]] $Top_{Quillen} \stackrel{\overset{{\vert - \vert}}{\longleftarrow}}{\underset{Sing}{\longrightarrow}} sSet_{Quillen}$ to the [[classical model structure on simplicial sets]] ("[[homotopy hypothesis]]") yields a _functorial_ CW approximation (by [this proposition](geometric+realization#mono)) via

$$
  X \mapsto {\vert Sing X\vert}
$$

([[geometric realization]] of the [[singular simplicial complex]] of $X$) with the [[adjunction counit]]

$$
  {\vert Sing X\vert}
  \overset{\in W}{\longrightarrow}
  X
$$

a weak homotopy equivalence.

## Statement

### For topological spaces

+-- {: .num_prop #nConnectedCWApproximationOfContinuousFunction}
###### Proposition

Let $f \;\colon\; A \longrightarrow X$ be a [[continuous function]] between [[topological spaces]]. Then there exists for each $n \in \mathbb{N}$ a [[relative CW-complex]] $\hat f \colon A \hookrightarrow \hat X$ together with an [[extension]] $\phi \colon \hat X \to X$, i.e.

$$
  \array{
    A &\overset{f}{\longrightarrow}& X
    \\
    {}^{\mathllap{\hat f}}\downarrow & \nearrow_{\mathrlap{\phi}}
    \\
    \hat X
  }
$$ 

such that $\phi$ is [[n-connected continuous function|n-connected]].

Moreover:

* if $f$ itself is [[n-connected continuous function|k-connected]], then the relative CW-complex $\hat f$ may be chosen to have cells only of [[dimension]] $k + 1 \leq dim \leq n$.

* if $A$ is already a [[CW-complex]], then $\hat f \colon A \to X$ may be chosen to be a subcomplex inclusion.

=--

([tomDieck 08, theorem 8.6.1](#tomDieck08))

+-- {: .num_prop #CWApproximationForContinuousFunctions}
###### Proposition

For every [[continuous function]] $f \colon A \longrightarrow X$ out of a [[CW-complex]] $A$, there exists a [[relative CW-complex]] $\hat f \colon A \longrightarrow \hat X$ that factors $f$ followed by a [[weak homotopy equivalence]] 

$$
  \array{   
     A && \overset{f}{\longrightarrow} && X
     \\
     & {}_{\mathllap{\hat f}}\searrow && \nearrow_{\mathrlap{{\phi} \atop {\in WHE}}}
     \\
     && \hat X
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply lemma \ref{nConnectedCWApproximationOfContinuousFunction} iteratively for $n \in \mathbb{N}$ to produce a sequence with [[cocone]] of the form

$$
  \array{
    A &\overset{f_0}{\longrightarrow}& X_0 &\overset{f_2}{\longrightarrow}& X_1 &\longrightarrow & \cdots
    \\
    &{}_{\mathllap{f}}\searrow & \downarrow^{\mathrlap{\phi_0}} & \swarrow_{\mathrlap{\phi_1}} & \cdots 
    \\
    && X
  }
  \,,
$$

where each $f_n$ is a [[relative CW-complex]] adding cells exactly of dimension $n$, and where $\phi_n$ in [[n-connected continuous function|n-connected]]. 

Let then $\hat X$ be the [[colimit]] over the sequence (its [[transfinite composition]]) and $\hat f \colon A \to X$ the induced component map. By definition of relative CW-complexes, this $\hat f$ is itself a relative CW-complex.

By the [[universal property]] of the colimit this factors $f$ as

$$
  \array{
    A &\overset{f_0}{\longrightarrow}& X_0 &\overset{f_1}{\longrightarrow}& X_1 &\longrightarrow & \cdots
    \\
    &{}_{\mathllap{}}\searrow & \downarrow^{\mathrlap{}} & \swarrow_{\mathrlap{}} & \cdots 
    \\
    && \hat X
    \\
    && \downarrow^{\mathrlap{\phi}}
    \\
    && X
  }
  \,.
$$

Finally to see that $\phi$ is a weak homotopy equivalence: since [[n-spheres]] are [[compact topological spaces]], then every map $\alpha \colon S^n \to \hat X$ factors through a finite stage $i \in \mathbb{N}$ as $S^n \to X_i \to  \hat X$ (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)). By possibly including further into higher stages, we may choose $i \gt n$.  But then the above says that further mapping along $\hat X \to X$ is the same as mapping along $\phi_i$, which is $(i \gt n)$-connected and hence an isomorphism on the homotopy class of $\alpha$.


=--

### For sequential topological spectra

+-- {: .num_prop #CWApproximationForSequentialSpectra}
###### Proposition

For $X$ any [[sequential spectrum]] in [[Top]], then there exists a [[CW-spectrum]] $\hat X$ and a homomorphism $\phi \colon  \hat X \to X$ which is degreewise a [[weak homotopy equivalence]], hence in particular a [[stable weak homotopy equivalence]].

=--

+-- {: .proof}
###### Proof

First let $\hat X_0 \longrightarrow X_0$ be a CW-approximation of the component space in degree 0, via prop. \ref{CWApproximationForContinuousFunctions}. Then proceed by [[induction]]: suppose that for $n \in \mathbb{N}$ a [[CW-approximation]] $\phi_{k \leq n} \colon  \hat X_{k \leq n} \to X_{k \leq n}$ has been found such that all the structure maps are respected. Consider then the continuous function

$$
  \Sigma \hat X_n \overset{\Sigma \phi_n}{\longrightarrow} \Sigma X_n \overset{\sigma_n}{\longrightarrow} X_{n+1}
  \,.
$$

Applying prop. \ref{CWApproximationForContinuousFunctions} to this function factors it as

$$
  \Sigma X_n \hookrightarrow \hat X_{n+1} \overset{\phi_{n+1}}{\longrightarrow} X_{n+1}
  \,.
$$

Hence we have obtained the next stage of the CW-approximation. The respect for the structure maps is just this factorization property:

$$
  \array{  
    \Sigma \hat X_n 
      &\overset{\Sigma \phi_n}{\longrightarrow}& 
    \Sigma X_n
    \\
    {}^{incl}\big\downarrow && \big\downarrow^{\mathrlap{\sigma_n}}
    \\
    \hat X_{n+1} &\underset{\phi_{n+1}}{\longrightarrow}& X_{n+1}
  }
  \,.
$$

=--


## Related concepts


* in [[stable homotopy theory]]: [CW-approximation for sequential spectra](CW-spectrum#CWApproximation)

* in [[equivariant homotopy theory]]: [[G-CW approximation]]

* [[Whitehead's theorem]]

* [[cellular approximation theorem]]

## References

* {#tomDieck08} [[Tammo tom Dieck]], section 8.6 of: _Algebraic topology_, EMS (2008)

* {#Hatcher} [[Allen Hatcher]], _Algebraic topology_, Cambridge Univ. Press 2002; Chapter 4, [Section 4.1 pdf](http://www.math.cornell.edu/~hatcher/AT/AT-CWapprox.pdf)


[[!redirects CW-approximation]]

[[!redirects CW approximations]]
[[!redirects CW-approximations]]

[[!redirects CW approximation theorem]]
[[!redirects CW approximation theorems]]

[[!redirects CW-approximation theorem]]
[[!redirects CW-approximation theorems]]


