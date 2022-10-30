
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[full subcategory|inclusion]] of actual [[spectra]] (e.g. [[sequential spectrum|sequential]] [[Omega-spectra]] or [[excisive functors]] on $(\infty Grpd_{fin}^{\ast/})^{op}$) into [[pre-spectra]] (e.g. [[sequential spectrum|sequential]] pre-spectra or all functors on on $(\infty Grpd_{fin}^{\ast/})^{op}$) has a ([[adjoint (infinity,1)-functor|infinity]]-)[[left adjoint]], "spectrification".

## Existence


### For sequential spectra

An original account is ([Lewis 86](#Lewis86)). The following is the approach due to ([Joyal 08](#Joyal08)), in the generality of [[parameterized spectra]] (which happens to make the analysis easier instead of harder).

+-- {: .num_defn}
###### Definition

Let $seq$ be the [[diagram]] category as follows:

$$
  seq 
  \coloneqq
  \left\{
    \array{
    && \vdots && \vdots
    \\
    && \downarrow && 
    \\
    \cdots &\to& x_{n-1} &\stackrel{p_{n-1}}{\longrightarrow}& \ast
    \\
    &&{}^{\mathllap{p_{n-1}}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_n}} & \searrow^{\mathrm{id}}
    \\
    &&\ast &\underset{i_n}{\longrightarrow}& x_n &\stackrel{p_n}{\longrightarrow}& \ast
    \\
    && &{}_{\mathllap{id}}\searrow& {}^{\mathllap{p_n}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_{n+1}}}
    \\
    && && \ast &\stackrel{i_{n+1}}{\longrightarrow}& x_{n+1} &\to& \cdots
    \\
     && && && \downarrow
     \\
     && && && \vdots
    }
  \right\}_{n \in \mathbb{N}}
  \,.
$$

=--

([Joyal 08, section 35.5](#Joyal08))

Let $\mathbf{H}$ be an [[(∞,1)-topos]], for instance $\mathbf{H} = $ [[∞Grpd]] for purposes of traditional [[stable homotopy theory]].  

+-- {: .num_remark}
###### Remark

An [[(∞,1)-functor]]

$$
  X_\bullet \;\colon\; seq \longrightarrow \mathbf{H}
$$

is equivalently 

1. a choice of [[object]] $B \in \mathbf{H}$ (the image of $\ast \in seq$);

1. a sequence of objects $\{X_n\} \in \mathbf{H}_{/B}$ in the [[slice (∞,1)-topos]] over $B$;

1. a sequence of [[morphisms]] $X_n \longrightarrow \Omega_B X_{n+1}$ from $X_n$ into the [[loop space object]] of $X_{n+1}$ in the slice.

This is a [[prespectrum object]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/B}$. 

A [[natural transformation]] 
$f \;\colon \;X_\bullet \to Y_\bullet$ between two such functors with components

$$
  \left\{
  \array{
    X_n &\stackrel{f_n}{\longrightarrow}& Y_n
    \\
    \downarrow^{\mathrlap{p_n^X}} && \downarrow^{\mathrlap{p_n^Y}}
    \\
    B_1 &\stackrel{f_b}{\longrightarrow}& B_2
  }
  \right\}
$$

is equivalently a morphism of base objects $f_b \;\colon\; B_1 \longrightarrow B_2$ in $\mathbf{H}$ together with morphisms $X_n \longrightarrow f_b^\ast Y_n$ into the [[(∞,1)-pullback]] of the components of $Y_\bullet$  along $f_b$.


Therefore the [[(∞,1)-presheaf (∞,1)-topos]] 

$$
  \mathbf{H}^{seq}
  \coloneqq
  Func(seq, \mathbf{H})
$$ 

is the [[codomain fibration]] of $\mathbf{H}$ with "fiberwise pre-stabilization".

A genuine [[spectrum object]] is a [[prespectrum object]] for which all the structure maps $X_n \stackrel{\simeq}{\longrightarrow} \Omega_B X_{n+1}$ are [[equivalence in an (∞,1)-category|equivalences]]. The [[full sub-(∞,1)-category]] 

$$
  T \mathbf{H} \hookrightarrow \mathbf{H}^{seq}
$$

on the genuine [[spectrum objects]] is therefore the "fiberwise [[stabilization]]" of the self-indexing, hence the tangent $(\infty,1)$-category.

=--

+-- {: .num_lemma #SpectrificationLemma}
###### Lemma
**(spectrification is left exact reflective)**

The inclusion of [[spectrum objects]] into $\mathbf{H}^{seq}$  is [[left exact (infinity,1)-functor|left]] [[reflective sub-(infinity,1)-category|reflective]], hence it has a [[left adjoint]] [[(∞,1)-functor]] $L$ -- [[spectrification]] --  which preserves [[finite (∞,1)-limits]].

$$
  T \mathbf{H}
  \stackrel{\overset{L_{lex}}{\leftarrow}}{\hookrightarrow}
  \mathbf{H}^{seq}
  \,.
$$


=--

([Joyal 08, section 35.1](#Joyal08))

+-- {: .proof}
###### Proof 

Forming degreewise [[loop space objects]] constitutes an [[(∞,1)-functor]] $\Omega \colon \mathbf{H}^{seq} \longrightarrow \mathbf{H}^{seq}$ and by definition of $seq$ this comes with a [[natural transformation]] out of the identity

$$
  \theta \;\colon\; id \longrightarrow \Omega
  \,.
$$

This in turn is compatible with $\Omega$ in that

$$
  \theta \circ \Omega \simeq \Omega \circ \theta
  \;\colon\;
  \rho \longrightarrow \rho \circ \rho = \rho^2
  \,.
$$

Consider then a sufficiently deep [[transfinite composition]] $\rho^{tf}$. By the [[small object argument]] available in the [[presentable (∞,1)-category]] $\mathbf{H}$ this stabilizes, and hence provides a [[reflective sub-(infinity,1)-category|reflection]] $L \;\colon\; \mathbf{H}^{seq} \longrightarrow T \mathbf{H}$.

Since [[transfinite composition]] is a [[filtered (∞,1)-colimit]] and since in an [[(∞,1)-topos]] these commute with [[finite (∞,1)-limits]], it follows that spectrum objects are an [[exact (∞,1)-functor|left exact]] [[reflective sub-(∞,1)-category]].

=--

See also at _[[tangent (∞,1)-topos]]_.

### For excisive functors

See at _[n-excisive functor -- n-Excisive approximation and reflection](n-excisive+functor#nExcisiveApproximation)_


## Construction

### For sequential spectra

For $E$ a [[sequential spectrum|sequential]] [[CW-spectrum|CW-]][[pre-spectrum]], its spectrification to an [[Omega-spectrum]] may be constructed

$$
  (L E)_n = \underset{\longrightarrow}{\lim}_k \Omega^k E_{n+k}
  \,.
$$

([Lewis-May-Steinberger 86, p. 3](#LewisMaySteinberger86))

In the special case that $E = \Sigma^\infty X$ a [[suspension spectrum]], i.e. with $E_n = \Sigma^n X$, then  $(L E)_0$ is the [[free infinite loop space]] construction.

If the pre-spectrum $E$ is not a [[CW-spectrum]] then the construction of the spectrification is more involved ([Lewis 86](#Lewis86)).

For $E$ a [[sequential spectrum|sequential]] [[prespectrum]] in [[pointed object|pointed]] [[simplicial sets]] the spectrification may be constructed by ([Bousfield-Friedlander 78, section 2.3](#BousfieldFriedlander78))

$$
  (L E)_n = \underset{\longrightarrow}{\lim}_k Sing {\Omega^k {\vert E_{n+k} \vert}}
$$

(i.e. by the previous formula combined with [[geometric realization]]/[[Kan fibrant replacement]]).

The spectrificatin functor on sequential prespectra satisfies the conditions of the [[Bousfield-Friedlander theorem]], and hence the [[left Bousfield localization]] of pre-spectra with degree-wise fibrations weak equivalences at the morphisms of prespectra that become weak equivalences under spectrification exists. This is the stable _[[Bousfield-Friedlander model structure]]_.




### For coordinate-free spectra

Similarly for a [[coordinate-free spectrum]] $E$, if all the structure maps are inclusions

$$
  E_V \hookrightarrow \Omega^{W-V}E_W
$$

then the spectrification is 

$$
  (L E)_V = \underset{V\subset W}{\lim} \Omega^{W-V}E_V
  \,-
$$

([Elmendorf-Kriz-May 95, p. 7](#ElmendorfKrizMay95))

## References

* {#BousfieldFriedlander78} [[Aldridge Bousfield]], [[Eric Friedlander]], _Homotopy theory of 