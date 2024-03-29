
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The refinement of the notion of [[fixed point]]/[[invariant]] to [[homotopy theory]]. Also _[[homotopy invariant]]_

See at

* [Invariants -- For infinity-group actions](invariant#ForInfinityGroupActions)

* [Infinity-action -- Invariants](infinity-action#Invariants)

## Properties

### Presentation

Generally, for $G$ an [[∞-group]] and $X$ equipped with an [[∞-action]], then the homotopy fixed points is the [[base change]] along/[[dependent product]] over the [[delooping]] $\mathbf{B}G$:

$$
  (-)^{h G}
  \;\colon\;
  G Act(\mathbf{H})
  \simeq
  \mathbf{H}_{/\mathbf{B}G}
  \overset
    {\;\;\;\prod_{\mathbf{B}G}\;\;\;}
    {\longrightarrow}
  \mathbf{H}
  \,.
$$

By the general discussion at _[[dependent product]]_ this is given by forming [[sections]], which by the discussion at [[∞-action]] here means forming sections of the $X$-[[associated ∞-bundle]] to the universal [[principal ∞-bundle]]

$$
  \array{
    X 
      &\longrightarrow& 
    X \sslash G
    \\
    && \big\downarrow
    \\
    && \mathbf{B}G 
    \,.
  }
$$

Such sections

\begin{tikzcd}[column sep=6pt]
  \ast 
  \ar[r]
  &
  \mathbf{B}G
  \ar[dr]
  \ar[rr, dashed]
  &&
  X /\!/ G
  \ar[dl]
  &
  X
  \ar[l]
  \\
  &
  & 
  \mathbf{B}G
  &
\end{tikzcd}

are equivalently homotopy-[[equivariant function]] out of the point equipped with the trivial $G$-action:

$$
  X^{h G}
  \simeq
  G Act(\ast, X)
  \,.
$$

For [[geometrically discrete ∞-groupoid|geometrically discrete]] [[∞-group]] [[∞-actions]], hence for $\mathbf{H} = $ [[∞Grpd]], it is the [[Borel model structure]] which [[presentable (infinity,1)-category|presents]] the [[homotopy theory]]. By the discussion [there](Borel+model+structure#CofibrantReplacementAndHomotopyQuotientsFixedPoints), the [[derived hom space]] is computed as the hom-space out of plain [[actions]] of [[simplicial groups]] out of the total space of the simplicial [[universal principal bundle]] $\mathbf{E}G = W G$. Therefore in this case one finds

$$
  X^{h G}
  \simeq
  R Hom_G(\ast, X)
  \simeq
  Hom_G(E G, X)
  \,.
$$

This is the form in which homotopy fixed points are often defined in traditional literature (going back to [Thomason 83](#Thomason83) and as in the historical discussion of the [[Sullivan conjecture]]). 

### Relation to periodicity theorems

In the context of [[complex oriented cohomology theory]]

... ([Hill-Hopkins-Ravenel, theorem 8.4](#HillHopkinsRavenel))...

## Related concepts

* [[fixed point space]]

* [[crossed homomorphism]]

* [[Sullivan conjecture]]

* [[invariant theory]]

* [[fixed point spectrum]]

* [[geometric fixed point spectrum]]

* [[categorical fixed point spectrum]]


[[!include homotopy type representation theory -- table]]


## References

The original article:

* {#Thomason83} [[Robert Thomason]], *The homotopy limit problem*, pages 407-419 in: [[Haynes Miller]], [[Stewart Priddy]] (eds.) *Proceedings of the Northwestern Homotopy Theory Conference*, Contemporary Mathematics **19**, AMS 1983 ([doi:10.1090/conm/019](http://dx.doi.org/10.1090/conm/019), [[ThomasonHomotopyLimit.pdf:file]])

Further discussion, for [[groupoids]] and [[stacks]]:

* R. Virk, *On fixed point stacks* ([arXiv:2112.06871](https://arxiv.org/abs/2112.06871))

In the context of [[complex oriented cohomology theory]]:

* {#HillHopkinsRavenel} [[Michael Hill]], [[Michael Hopkins]], [[Douglas Ravenel]], Theorem 8.4 in: _The Arf-Kervaire problem in algebraic topology: Sketch of the proof_ ([[HHRKervaire.pdf:file]])


[[!redirects homotopy fixed points]]

[[!redirects homotopy fixed point space]]
[[!redirects homotopy fixed point spaces]]



