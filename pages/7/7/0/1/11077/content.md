
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[stable homotopy theory]] of [[local spectra]], local with respect to [[Morava K-theory]] $K(n)$.

## Properties

### Bilimits


+-- {: .num_defn #StrictlyTame}
###### Definition

Say that an [[∞-groupoid]] is _[[groupoid cardinality|strictly tame]]_ or _of [[finite type]]_ ([Hopkins-Lurie 14, def. 4.4.1](#HopkinsLurie14)) or maybe better is a _[[homotopy type with finite homotopy groups|truncated homotopy type with finite homotopy groups]]_ if it has only finitely many nontrivial [[homotopy groups]] each of which is furthermore a [[finite group]].

=--


+-- {: .num_prop #HopkinsLurieTheorem}
###### Proposition

For $F \colon X \to Sp_{K(n)}$ a strictly tame [[diagram]], def. \ref{StrictlyTame}, of $K(n)$-local spectra, then its [[(∞,1)-limit]] and [[(∞,1)-colimit]] agree in that the canonical comparison map is an [[equivalence in an (∞,1)-category|equivalence]]

$$
  \underset{\longrightarrow}{\lim} F 
    \stackrel{\simeq}{\longrightarrow}
  \underset{\longleftarrow}{\lim} F
  \,.
$$

=--

This is ([Hopkins-Lurie 14, theorem 0.0.2](#HopkinsLurie14)).

+-- {: .num_remark}
###### Remark


So in particular $K(n)$-local spectra have _[[biproducts]]_, called _[[0-semiadditivity]]_ in ([Hopkins-Lurie 14, prop. 4.4.9](#HopkinsLurie14).

=--



+-- {: .num_example}
###### Example

For $X$ pointed [[connected]], hence $X \simeq B G$ the [[delooping]] of an [[∞-group]], a [[diagram]] in prop. \ref{HopkinsLurieTheorem} exhibits an [[∞-action]] of $G$ on some $K(n)$-local spectrum, the [[(∞,1)-colimit]] produces the [[homotopy quotient]] of the [[∞-action]] and the [[(∞,1)-limit]] the [[homotopy invariants]]. In this case ([Hovey-Sadofsky 96](#HoveySadofsky96)) show that the comparison map exhibits the homotopy invariant as the $K(n)$-[[localization of a spectrum|localization]] of the homotopy coinvariants. This in particular means that the comparison map is a $K(n)$-local equivalence, which is the statement of prop. \ref{HopkinsLurieTheorem}.

=--


### Logarithms of twists of generalized cohomology

Let $E$ be an [[E-∞ ring]] and write $GL_1(E)$ for its [[abelian ∞-group|abelian]] [[∞-group of units]]  and $gl_1(E)$ for the corresponding [[connective spectrum]]. 

Via the [[Bousfield-Kuhn functor]] there are [[natural equivalences]] between the $K(n)$-localizations of $gl_1(E)$ and $E$ itself. 

$$
  L_{K(n)} gl_1(E) \simeq L_{K(n)} E
  \,.
$$

Composed with the [[Bousfield localization of spectra|localization map]] itself, this yields [[logarithmic cohomology operations]]

$$
  gl_1(E) \longrightarrow L_{K(n)} gl_1E \stackrel{\simeq}{\to} L_{K(n)}E
  \,.
$$


## Related concepts

* [[chromatic homotopy theory]]

* [[Bousfield-Kuhn functor]]

* [[logarithmic cohomology operation]]

## References

* {#HoveySadofsky96} [[Mark Hovey]], H. Sadofsky, _Tate cohomology lowers chromatic Bouseld classes_ Proceedings of the AMS 124, 1996, 3579-3585.


* {#HopkinsLurie14} [[Michael Hopkins]], [[Jacob Lurie]], _[[Ambidexterity in K(n)-Local Stable Homotopy Theory]]_ (2014)



[[!redirects K(n)-local spectrum]]
[[!redirects K(n)-local spectra]]

[[!redirects K(n)-localization]]
[[!redirects K(n)-localizations]]
