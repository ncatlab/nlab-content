
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Duality
+--{: .hide}
[[!include duality - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

\begin{definition}\label{PontrjaginDualGroup}
Let $A$ be a [[abelian group|commutative]] ([[Hausdorff space|Hausdorff]]) [[topological group]]. A (continuous) *[[group character]]* of $A$ is any continuous homomorphism $\chi: A\to S^1$ to the [[circle group]]. The __Pontrjagin dual group__ 

$$
  \widehat{A}
  \;\coloneqq\;
  TopGrps
  \big(
    A
    ,\,
    S^1
  \big)
$$ 
is the [[abelian group]] of all these [[group characters]] of $A$, equipped with pointwise multiplication (that is multiplication induced by multiplication in the [[circle group]], the multiplication of norm-$1$ complex numbers in $S^1\subset\mathbb{C}$) and with the [[topological space|topology]] of [[uniform convergence]] on each [[compact space|compact]] $K\subset A$ (this is equivalent to the [[compact-open topology]]). 
\end{definition}

## Examples

\begin{example}
The Pontrjagin dual of the additive group of [[integers]] $\mathbb{Z}$ is the [[circle group]] $S^1$, and conversely, $\mathbb{Z}$ is the Pontrjagin dual of $S^1$. This pairing of dual topological groups, given by $(n,z) \mapsto z^n$, is related to the subject of [[Fourier transforms]]. 
\end{example}

In general, the dual of a [[discrete space|discrete]] group is a [[compact space|compact]] group and conversely. In particular, therefore, the dual of a [[finite group]] is again finite.

\begin{example}
The [[finite group|finite]] [[cyclic groups]] are Pontrjagin self-dual: $\widehat{\mathbb{Z}/n} \,\simeq\, \mathbb{Z}/n$.
\end{example}


\begin{prop}\label{PontrajginDualOfCompactGroupAsSecondGroupCohomologyGroup}
  **(Pontrjagin dual of compact group as second group cohomology group)**
  \linebreak
  If $G$ is a [[finite group]] (more generally: a [[compact Lie group]]) then its Pontrjagin dual is equivalently its [[cohomology group]] in degree-2 [[group cohomology]] (more generally: refined [[Lie group cohomology]]) with [[integer]] [[coefficients]]:
  $$
    \widehat{G}
    \;\simeq\;
    H^2_{grp}
    \big(
      G
      ;\,
      \mathbb{Z}
    \big)
    \;=\;
    H^2
    \big(
      B G
      ;\,
      \mathbb{Z}
    \big)
    \,.
  $$
\end{prop}
\begin{proof}
  The key point is that, by assumption on $G$, we have
  \[
    \label{RealGroupCohomologyOfCompactGroupVanishes}
    H^{\bullet \geq 1}_{grp}
    \big(
      G;\, \mathbb{R} 
    \big)
    \;=\;
    0
    \,.
  \]

Using this, the conclusion is obtained as follows:
The defining [[short exact sequence]] of [[groups]]
$$
  \mathbb{Z} \xhookrightarrow{\;} \mathbb{R} \twoheadrightarrow S^1
$$
extends to a [[homotopy fiber sequence]] of [[2-groups]] (and further of [[n-groups]])
$$
  \mathbb{Z}
    \xrightarrow{\;\;}
  \mathbb{R}
    \xrightarrow{\;\;}
  S^1 
    \xrightarrow{\;\;} 
  B \mathbb{Z}
    \xrightarrow{\;\;} 
  B \mathbb{R}
    \xrightarrow{\;\;} 
  \cdots
  \,.
$$

This induces a [[long exact sequence]] of [[cohomology groups]] induced from the [[long exact sequence of homotopy groups]] of the image of this fiber sequence under the [[derived hom-space]] $\mathbf{H}(B G,-) \coloneqq Maps(B G;\, -)$ (of $\mathbf{H} =$ [[∞Grpd]]):
$$
  \array{
  \cdots
  &\to&
  \pi_1
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{R})
  \right)
  &\xrightarrow{\;\;}&
  \pi_1
  \left(
    \mathbf{H}(B G, \, B^2 S^1)
  \right)
  &\xrightarrow{\;\;}&
  \pi_0
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{Z})
  \right)
  &\xrightarrow{\;\;}&
  \pi_0
  \left(
    \mathbf{H}(B G, \, B^2 \mathbb{R})
  \right)
  &\to&
  \cdots
  \\
  &&
  =
  &&
  =
  &&
  =
  &&
  =
  \\
  \cdots
  &\to&
  \underset{
    = 0
  }{
  \underbrace{
  H^1
  \big(
    B G
    \;,
    \mathbb{R}
  \big)
  }
  }
  &\xrightarrow{\;\;}&
  H^1
  \big(
    B G
    \;,
    S^1
  \big)
  &\xrightarrow{\;\simeq\;}&
  H^2
  \big(
    B G
    \;,
    \mathbb{Z}
  \big)
  &\xrightarrow{\;\;}&
  \underset{
    = 0
  }{
  \underbrace{
  H^2
  \big(
    B G
    \;,
    \mathbb{R}
  \big)
  }
  }
  &\to&
  \cdots
  \,.
  }
$$
Using the assumption (eq:RealGroupCohomologyOfCompactGroupVanishes) under the braces, this implies the middle isomorphism, as shown.

Now the claim follows by re-expressing $H^1(B G;\, S^1)$ as follows:

$$
  \begin{aligned}
  H^2(B G;\, \mathbb{Z})
  \;\simeq\;
  H^1(B G;\, S^1)
  &
  \;\simeq\;
  \pi_0 \mathbf{H}\big( B G, \, B S^1 \big)
  \\
  &
  \;\simeq\;
  \pi_0 Groupoids\big( G \rightrightarrows \ast, \, S^1 \rightrightarrows \ast \big)
  \\
  & \;\simeq\;
  \pi_0 
  \Big(
    Groups\big(G,S^1\big) \sslash S^1
  \Big)
  \\
  & \;\simeq\;
  \pi_0 
  \Big(
    Groups\big(G,\,S^1\big) \times B S^1
  \Big)
  \\
  & \;\simeq\;
  Groups(G,S^1)
  \;\simeq\;
  \widehat G
  \,,
  \end{aligned}
$$
where the third line expresses the [[functor groupoid]] of [[functors]] and [[natural transformations]] between [[delooping groupoids]], while the last step uses that the [[circle group]], being [[abelian group|abelian]], has [[trivial action|trivial]] [[conjugation action]] on the [[hom-set]] of [[group homomorphisms]]. (For $G$ a [[compact Lie group]] the analogous argument applies to the [[delooping]]/[[quotient stacks]] $\mathbf{B}G$ in $\mathbf{H} = $[[Smooth∞Grpd]].)
\end{proof}

\begin{example}\label{EquivariantFundamentalGroupOf3TwistOfKTheory}
**(equivariant fundamental group of 3-twists of equivariant K-theory)**
\linebreak
  For $G$ a [[finite group]], the [[fundamental group]] $\pi_1(-)$ of the $G$-[[fixed locus]] $(-)^G$ of the base space $\mathcal{B} PU(\mathcal{H})$ of the [[universal equivariant PU(H)-bundle|universal equivariant $PU(\mathbb{H})$-bundle]] ([[classifying space|classifying]] 3-[[twisted cohomology|twists]] in [[twisted equivariant K-theory]]) is
$$
  \pi_1
  \Big(
     \big(
       \mathcal{B} PU(\mathcal{H})
     \big)^G
  \Big)
  \;\simeq\;
  Grps(G, S^1)
  \,=\,
  \widehat G  
$$
(in any [[connected component]] of a "stable map" $G \to PU(\mathcal{H})$, that is) and hence is the Pontrjagin dual group (Def. \ref{PontrjaginDualGroup}) when $G$ is [[abelian group|abelian]].
\end{example}
By [BEJU 2014, Thm. 1.10](universal+equivariant+PU-bundle#BEJU14), see [this Prop.](universal+equivariant+PU-bundle#EquivariantHomotopyGroupsOfBaseSpace).

\begin{example}
The Pontrjagin dual $\hat{\mathbb{R}}$ of the additive group of [[real numbers]] is isomorphic again to $\mathbb{R}$ itself, with the pairing given by $(x,p) \mapsto \mathrm{e}^{\mathrm{i} x p}$. More generally, $\widehat{\mathbb{R}^n} \,=\, \mathbb{R}^n$.
\end{example}

## Properties

### Pontrjagin duality theorem

\begin{theorem}
For every [[abelian group|abelian]] [[Hausdorff space|Hausdorff]] [[locally compact topological group]] $A$, the natural function $A \mapsto \widehat{\widehat{A}}$ from $A$ into the Pontrjagin dual of the Pontrjagin dual of $A$, assigning to every $g\in A$ the continuous character $f_g$ given by $f_g(\chi)=\chi(g)$, is an [[isomorphism]] of topological groups (that is, a group isomorphism that is also a [[homeomorphism]]). 
\end{theorem}

Thus, the [[functor]]

$$LocCompAb^{op} \to LocCompAb: G \to \widehat{G}$$ 

is an [[equivalence of categories]], in fact an [[adjoint equivalence]] whose [[unit of an adjunction|unit]] is

$$A \to \widehat{\widehat{A}}: g \mapsto f_g$$ 

and whose [[counit of an adjunction|counit]] (the same arrow read in the opposite category) are [[isomorphisms]]. This contravariant self-equivalence restricts to equivalences 

$$Ab^{op} \to CompAb$$


$$CompAb^{op} \to Ab$$ 

where [[Ab]] is the category of ([[discrete topological space|discrete topological]]) groups and $CompAb$ is the category of abelian [[Hausdorff space|Hausdorff]] [[compact topological groups]], each 
embedded in $LocCompAb$ in the evident way. 

The [[Fourier transform]] on abelian [[locally compact groups]] is formulated in terms of Pontrjagin duals (see below). 



### Basic properties of dual groups

There are many properties of Hausdorff abelian [[locally compact groups]] that implies properties of their Pontrjagin duals.  For example:

* If $A$ is [[finite group|finite]], then $\widehat{A}$  is finite.

* If $A$ is [[compact topological group|compact]], then $\widehat{A}$ is [[discrete group|discrete]].

* If $A$ is [[discrete group|discrete]], then $\widehat{A}$  is [[compact topological group|compact]].

* If $A$ is [[torsion subgroup|torsion]]-free and [[discrete group|discrete]], then $\widehat{A}$ is [[connected topological space|connected]] and [[compact topological group|compact]].

* If $A$ is an [[abelian group|abelian]] [[torsion group]], then $\widehat A$ is an abelian [[profinite group]] (for more see at _[[Pontryagin duality for torsion abelian groups]]_)

* If $A$ is [[connected topological space|connected]] and [[compact topological group|compact]], then $\widehat{A}$ is [[torsion subgroup|torsion]]-free and [[discrete group|discrete]].

* If $A$ is a [[Lie group]], then $\widehat{A}$ is compactly generated in that there is a [[compact topological space|compact]] [[neighborhood]] of the [[neutral element]] that generates $\widehat{A}$ as a group. 

* If $A$ is compactly generated, then $\widehat{A}$ is a Lie group.

* If $A$ is [[second countable topological space|second countable]], then $\widehat{A}$ is second countable.

* If $A$ is [[separable topological space|separable]], then $\widehat{A}$ is [[metrizable topological space|metrizable]].

For a discussion of these facts see [Morris 77](#Morris77), [Armacost 81](#Armacost81), exposition in:

* Variations on Pontryagin duality, ([nCafe](http://golem.ph.utexas.edu/category/2008/11/variations_on_pontryagin_duali.html))

Another statement of this type is presented in [Mackey 1948](#Mackey48):

* $A$ is connected if and only if $\widehat{A}$ is a product of a discrete torsion-free group with a finite dimensional real vector space.

## Applications

Pontrjagin duality underlies the abstract framework of [[Fourier analysis]] on locally compact Hausdorff abelian groups $A$: by Fourier duality on $A$, there is a Hilbert space isomorphism ([[Fourier transform]])

$$\mathcal{F}_A: L^2(A, d\mu) \to L^2(\hat{A}, d\hat{\mu})\,,$$

where $d\mu$ is a suitable choice of [[Haar measure]] on $A$, and $d\hat{\mu}$ is a suitable choice of Haar measure on the dual group. Fourier duality is compatible with Pontrjagin duality in the sense that if $\hat{\hat{A}}$ is identified with $A$, then $\mathcal{F}_{\hat{A}}$ is the inverse of $\mathcal{F}_A$.

## Related concepts

* [[Pontryagin duality for torsion abelian groups]]

* [[locally compact topological group]]

* [[Fourier transform]]

* [[character group]]

* [[dual object]]

* [[Cartier duality]], [[Poincaré line bundle]]




## References

### General

The original article:

* {#Pontrjagin34} [[Lev Pontrjagin]], *Theory of topological commutative groups*, Annals of Mathematics Second Series, Vol. 35, No. 2 (Apr., 1934), pp. 361-388 ([doi:10.2307/1968438](https://doi.org/10.2307/1968438))

  Russian translation: Uspekhi Mat. Nauk, 1936, no. 2, 177–195 ([mathnet:umn8882](http://mi.mathnet.ru/eng/umn8882))



Gentle exposition:

* Partha Sarathi Chakraborty, *Pontrjagin duality for finite groups* ([[Chakraborty_PontrjaginDuality.pdf:file]])

Textbook accounts:

* {#Morris77} [[Sidney A. Morris]], _Pontryagin Duality and the Structure of Locally Compact Abelian Groups_, London Math. Soc. Lecture Notes 29, Cambridge U. Press, 1977 ([doi:10.1017/CBO9780511600722](https://doi.org/10.1017/CBO9780511600722))

* {#Armacost81} David L. Armacost, *The Structure of Locally Compact Abelian Groups*, Dekker, New York, 1981.

See also

* Wikipedia, *[Pontryagin duality](https://en.wikipedia.org/wiki/Pontryagin_duality)*

Also:

* {#Mackey48} [[George Mackey]], *The Laplace Transform For Locally Compact Abelian Groups*, Proceedings of the National Academy of Sciences of the United States of America Vol. 34, No. 4 (Apr. 15, 1948), pp. 156-162 ([jstor:87968](https://www.jstor.org/stable/87968))

* [[Michael Barr]], *On duality of topological abelian groups* ([pdf](http://www.math.mcgill.ca/barr/ftp/pdffiles/abgp.pdf), [[Barr_PontrjaginDuality.pdf:file]])

  which provides a perhaps better context for Pontryagin duality than the category of locally compact Hausdorff abelian groups (also known as 'LCA groups').  Barr explains:

  > Did you know that there is a [[star-autonomous category|*-autonomous category]] of topological abelian groups that includes all the LCA groups and whose duality extends that of Pontrjagin?  The groups are characterized by the property that among all topological groups on the same underlying abelian group and with the same set of continuous homomorphisms to the circle, these have the finest topology.  It is not obvious that such a finest exists, but it does and that is the key.

### For higher groups

Discussion of [[categorification|categorified]] Pontrjagin duality for [[2-groups]] and application to [[topological T-duality]]:

* {#BSST07} [[Ulrich Bunke]], [[Thomas Schick]], [[Markus Spitzweck]], [[Andreas Thom]], _Duality for topological abelian group stacks and T-duality_, Proceedings of the ICM 2006 satellite conference, Valladolid, Spain, 2006. Z&#252;rich: EMS. Series of Congress Reports, 227-347 (2008) ([arXiv:math/0701428](http://arxiv.org/abs/math/0701428))

* [[Calder Daenzer]], _A groupoid approach to noncommutative T-duality_, PhD, 2007 ([pdf](http://www.math.upenn.edu/grad/dissertations/DaenzerThesis.pdf))

[[!redirects Pontrjagin duals]]

[[!redirects Pontryagin dual]]
[[!redirects Pontryagin duals]]

[[!redirects Pontrjagin duality]]
[[!redirects Pontrjagin dualities]]

[[!redirects Pontryagin duality]]
[[!redirects Pontryagin dualities]]

[[!redirects Pontriagin dual]]
[[!redirects Pontriagin duals]]

[[!redirects Pontriagin duality]]
[[!redirects Pontriagin dualities]]

[[!redirects Понтрягин dual]]
[[!redirects Понтрягин duals]]

[[!redirects Понтрягин duality]]
[[!redirects Понтрягин dualities]]

