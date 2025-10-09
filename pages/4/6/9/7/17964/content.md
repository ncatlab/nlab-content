[[!redirects KS-model]]
[[!redirects minimal KS-extension]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea 

A _minimal dg-module_ ([Roig 92](#Roig92), [Roig 94, section 1](#Roig94)) is a [[minimal model]] in the context of the [[homotopy theory]] of [[dg-modules]]. 

Hence over [[dgc-algebras]] in non-positve degree, minimal dg-modules are the analogue of [[minimal Sullivan model]] as one passes from [[dg-algebras]] to (just) [[dg-modules]]. Minimal KS-extensions hence  play the role of formal duals of [[minimal fibration]] in some applications of [[rational homotopy theory]]. 

(In [Halperin 83](#Halperin83) it has "Koszul-Sullivan extensions" for [[relative Sullivan algebras]], and "KS" in "KS-models" refers to that usage.)


## Definition


Throughout, let $A$ be a [[dg-algebra]]. Eventually this is thought of as being a [[Sullivan model]] for the [[rationalization]] of the [[quotient]] of a [[topological space]] by a circle action.

We take all [[differentials]] to have degree +1. For $V$ a [[vector space]] and $n$ a [[natural number]], we write $V[n]$ for the [[chain complex]] concentrated on $V$ in degree $n$.

+-- {: .num_defn #HirschExtension}
###### Definition
**(Hirsch extension of dg-modules)**

Let $N$ be a [[dg-module]] over $A$ and let $n \in \mathbb{N}$ be a [[natural number]]. Then a degree $n$ **[[Hirsch extension]]** of $N$  is 
a [[monomorphisms]] of [[dg-modules]] of the form

$$
  N \hookrightarrow (N \oplus (A \otimes V[n]), d_{\phi})
$$

given by a choice of

1. a [[vector space]] $V$

1. a [[linear map]] $d_V \;\colon\; V \to N_{n+1}$

where the differential $d_{\phi}$ is $d_N$ on $N$, is $d_A$ on $A$, and is given on $V$ by $\phi$ followed by the [[action]] $\rho$ of $A$ on $V$:

$$
  d_\phi (a \otimes v) = (d_A a) \otimes v + (-1)^{\vert a \vert}  \rho(a,\phi(v))
  \,.
$$

=--

([Roig 94, def. 1.8](#Roig94))

+-- {: .num_remark}
###### Remark

It follows that for $N_1, N_2$ two $A$-[[dg-modules]] then homomorphisms $f$ out of a Hirsch extension of the former (def. \ref{HirschExtension}) 

$$
  f 
   \;\colon\;
  (N_1 \oplus (A \otimes V[n]), d_\phi)
   \longrightarrow
  N_2
$$

is equivalently

1. a homomorphism of dg-modules $h \colon N_1 \to N_2$;

1. a [[linear map]] $g \colon V \to (N_2)_{n}$

such that

* $h \circ d_{\phi} = d_{N_2} \circ g$.

=--

The following defines a kind of [[minimal cofibrations]] of dg-modules.

+-- {: .num_defn #KSFactorization}
###### Definition
**(minimal KS-extension)**

For $N$ a [[dg-module]] over $A$, then a **[[minimal KS-extension]]** of $N$ is a certain [[transfinite composition]] of Hirsch extensions, namely a [[monomorphism]]

$$
  N \hookrightarrow \hat N
$$

equipped with an [[exhaustive filtration]] $\{\hat N(n,q)\}_{n,q \in \mathbb{N}}$ such that:

1. $\hat N(0,0) \simeq N$;

1. the inclusions $\hat N(n,q) \hookrightarrow \hat N(n,q+1)$ are Hirsch extensions (def. \ref{HirschExtension}).

1. $N(n+1,0) = \underset{\longrightarrow}{\lim}_q \hat N(n,q)$ ([[colimit]] over the sequence of Hirsch extensions in the previous degree).

Accordingly, a **minimal KS-factorization** of a morphism $N_1 \to N_2$ of $A$-dg-modules is a factorization as a minimal KS-extension followed by a [[quasi-isomorphism]]

$$
  \array{
    N _1 && \longrightarrow && N_2
    \\
    & {}_{\mathllap{\text{minimal} \atop \text{KS-extension}}}\searrow && \nearrow_{\mathrlap{\text{quasi-iso}}}
    \\
    && N_1 \oplus (A \otimes V)
  }
  \,.
$$

Finally a **minimal KS-model** is a [[dg-module]] $N$ such that $0 \hookrightarrow N$ is a minimal KS-fibration.


=--

([Roig 94, def. 1.9](#Roig94))

+-- {: .num_prop}
###### Proposition

Let the [[ground field]] be of [[characteristic zero]].

Let $f \colon N_1 \longrightarrow N_2$ be a morphism of $A$-[[dg-modules]] such that it induces a [[monomorphism]] in degree-0 [[cochain cohomology]], $H^0(f) \colon H^0(N_1) \hookrightarrow H^0(N_2)$ then it admits a minimal KS-factorization (def. \ref{KSFactorization}).

In particular, every [[dg-module]] has a minimal KS-model (def. \ref{KSFactorization}).

=--

[Roig & Saralegi-Aranguren 00, theorem 1.3.1](#RoigSaralegiAranguren00)


## Examples

* [4-sphere -- circle action](4-sphere#CircleAction)


## Related entries

* [[circle action]]


## References
 {#References}




* {#Roig92} [[Agustí Roig]], _Alguns punts d'&#224;lgebra homot&#242;pica_, Barcelona (1992) &lbrack;[web](https://ddd.uab.cat/record/38587)&rbrack;

* {#Roig93} [[Agustí Roig]], _Minimal resolutions and other minimal models_, Publicacions Matem&#224;tiques **37** 2 (1993) 285-303 &lbrack;[eudml](https://eudml.org/doc/41535)&rbrack;

* {#Roig94} [[Agustí Roig]], _Formalizability of dg modules and morphisms of cdg algebras_, Illinois J. Math. **38** 3 (1994) 434-451 &lbrack;[doi:10.1215/ijm/1255986724](https://doi.org/10.1215/ijm/1255986724)&rbrack; 

* [[Igor Kriz]], [[Peter May]], section IV.3 of _Operads, Algebras, Modules and Motives_, 1994 ([pdf](http://www.math.uchicago.edu/~may/PAPERS/kmbooklatex.pdf))

* {#RoigSaralegiAranguren00} [[Agustí Roig]], [[Martintxo Saralegi-Aranguren]], _Minimal Models for Non-Free Circle Actions_, Illinois J. Math. **44** 4 (2000) 784-820 &lbrack;[arXiv:math/0004141](https://arxiv.org/abs/math/0004141), [doi:10.1215/ijm/1255984692](https://doi.org/10.1215/ijm/1255984692)&rbrack;

See also

* {#Halperin83} [[Steve Halperin]], _Lectures on minimal models_, Mem. Soc. Math. Franc. **9-10** (1983) 1-261 &lbrack;[eudml](https://eudml.org/doc/94833)&rbrack;

* {#Silveira84} [[Flavio da Silveira]], _Rational homotopy theory of fibrations_, Pac. J. Math. **113** 1 (1984) 1–34 &lbrack;[doi:10.2140/pjm.1984.113.1](http://dx.doi.org/10.2140/pjm.1984.113.1)&rbrack;





[[!redirects minimal dg-modules]]

[[!redirects Hirsch extension]]
[[!redirects Hirsch extensions]]
 
[[!redirects minimal Hirsch cofibration]]
[[!redirects minimal Hirsch cofibrations]]

[[!redirects minimal KS-extension]]
[[!redirects minimal KS-extensions]]

[[!redirects minimal KS-model]]
[[!redirects minimal KS-models]]
