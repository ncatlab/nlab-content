

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In [[homological algebra]] a _homological resolution_ of a [[vector space]] or more generally of a [[module]] $N$ is a [[chain complex]] $V_\bullet$ whose [[chain homology]] $H_\bullet(V)$ reproduces $N$, in that 

$$
  H_n(V)
  \;\simeq\;
  \left\{
    \array{
       N &\vert& n = 0
       \\
       0 &\vert& \text{otherwise}
    }
  \right.
$$

Of course if one regards $N$ itself as a chain complex $N_\bullet$ which is concentrated in degree 0, then $N_\bullet$ has this property, trivially. Therefore, typically when asking for a homological resolution $V_\bullet$ of $N$, it is understood that the entries of $V_\bullet$ have certain nice properties that $N$ is lacking. 

For instance if $V_\bullet$ consists of [[projective modules]], then it is called a _[[projective resolution]]_ of $N$, or if it consists of [[injective modules]] then it is called an _[[injective resolution]]_, or if it consists of [[free modules]], then it is called a _[[free resolution]]_, etc. The module $N$ itself may be far from being projective or injective or free, etc. and so the corresponding resolution, if it exists, allows to nevertheless regard $N$ with tools applicable to these particularly nice classes of modules, up to chain homology

Typically in these constructions one demands not just that the [[chain homology]] of the resolution reproduces $N$ via _any_ isomorphism $H_0(V) \simeq N$, but that there exists a [[chain map]] $f_\bullet$ from $V$ to $N$ or from $N$ to $V$, such that it is this chain map which under passage to [[chain homology]] induces this isomorphism. A chain map which induces isomorphisms on chain homology groups is called a _[[quasi-isomorphism]]_, and so typically a _homological resolution_ means a choice of quasi-isomorphism from a module to a (particularly nice) chain complex.

Famous classes of examples of such resolutions are the injective and projective resolutions that are used to construct _[[derived functors in homological algebra]]_, see there for more.

Phrased this way, there is nothing special about starting with a single module, and more generally one may speak of [[resolutions]] of one chain complex by another chain complex with some better properties. The theory of [[homotopical categories]] such as [[model categories]] or [[fibration categories]]/[[cofibration categories]] is used to handle homological resolutions in this generality, see at _[[model structure on chain complexes]]_ for more on this.

Viewed from this general perspective of [[homotopical categories]], homological resolutions are a special case of the general concept of [[resolutions]] in [[homotopy theory]]. (In fact [[homological algebra]] may be understood as a fragment of [[stable homotopy theory]], see at _[[Dold-Kan correspondence]]_ and _[[stable Dold-Kan correspondence]]_ for more on this.)



## Examples

The ur examples of homological resolutions are the [[Koszul complexes]] or more generally [[Koszul-Tate resolutions]] of an $A$-[[module]] by [[free modules]] ove or of an $A$-[[associative algebra|algebra]] by free $A$-algebras. 

For example, consider $A$ is a commutative [[augmented algebra]] over a [[field]] $k$ and $I$ an ideal in $A$. Resolve the [[quotient]] $A/I$ by a free $A$-algebra $R$ with a [[derivation]] [[differential]] so that $H(R) = A/I$ is concentrated in degree $0$ and all other homology vanishes. Iff $I$ is a [[regular ideal]], the [[Koszul complex]] will do; if $I$ is not regular, continue the process forming the [[Koszul-Tate resolution]], the algebraic analog of a [[Moore-Postnikov system]], which was indeed Tate's inspiration.

If the original object is itself [[graded object|graded]] or differential graded, the resolution will be bigraded by resolution degree and _internal degree_.

By **homological resolution of a quotient**, one means a _weak quotient_ or _homotopy quotient_ in some $\infty$-categorical [[homotopy theory]] context which is equivalent to a category of (co)chain complexes. This means: a homological resolution of a quotient is a (co)chain complex $C^\bullet$ of abelian groups whose _(co)homology_ $H^\bullet(C^\bullet)$ in some degree, usually in degree 0, is the desired quotient, $H^0(C) = desired quotient$. 
Depending on the situation one may want to demand that the (co)homology in all other degrees vanish, in which case $C^\bullet$ would be [[homotopy theory|weakly equivalent]] to the desired quotient.

## Related concepts

* [[simplicial resolution]]

## References

Discussion for an audience of physicists in the context of [[BV-BRST formalism]] is in


* [[Marc Henneaux]], [[Claudio Teitelboim]], section 8.3 of _Quantization of gauge systems_, Princeton University Press, 1992


[[!redirects homological resolutions]]

[[!redirects Homological resolution]]
[[!redirects Homological resolutions]]
