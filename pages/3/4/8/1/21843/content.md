

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

The [[cobordism cohomology theory]] for [[special unitary group]]-[[G-structure|structure]].

## Properties

We write $\Omega^{SU}_\bullet$ for the [[bordism ring]] for [[stable tangent bundle|stable]] [[special unitary group|SU]]-[[G-structure|structure]].


### Relation to $MU$

The canonical [[topological group]]-[[subgroup|inclusions]]

$$
  1
  \;\subset\;
  Sp(k)
  \;\subset\;
  SU(2k)
  \;\subset\;
  U(2k)
$$ 

([[trivial group]] into [[quaternionic unitary group]] into [[special unitary group]] into [[unitary group]]) induce [[ring spectrum]]-[[homomorphism]] of [[Thom spectra]]

$$
  M Fr
   \;\longrightarrow\;
  M Sp
   \;\longrightarrow\;
  M SU
   \;\longrightarrow\;
  M \mathrm{U}
$$

(from [[MFr]] to [[MSp]] to [[MSU]] to [[MU]])

and hence corresponding [[multiplicative cohomology theory]]-[[homomorphisms]] of [[cobordism cohomology theories]], so in particular [[ring homomorphisms]] of [[bordism rings]]

\[
  \label{HomomorphismsOfCobordismRings}
  \Omega^{fr}_{\bullet}
   \longrightarrow
  \Omega^{Sp}_{\bullet}
   \longrightarrow
  \Omega^{SU}_{\bullet}
   \longrightarrow
  \Omega^{U}_{\bullet}
\]

(e.g. [Conner-Floyd 66, p. 27 (34 of 120)](#ConnerFloyd66))



+-- {: .num_prop #KernelOfMapFromSUBordismToUBordismIsTorsion}  
###### Proposition

The [[kernel]] of the [[forgetful functor|forgetful]] morphism (eq:HomomorphismsOfCobordismRings)

$$
  \Omega^{SU}_\bullet
  \longrightarrow
  \Omega^{\mathrm{U}}_\bullet
$$

from the [[SU-bordism ring]] to the [[complex bordism ring]], is pure [[torsion subgroup|torsion]].

=--

([CLP 19, Thm. 5.8a](#CLP19))

+-- {: .num_prop #TorsionInSUBordismConcentratedInDegrees1And2Mod8}  
###### Proposition

The [[torsion subgroup]] of the [[SU-bordism ring]] is concentrated in degrees $8k+1$ and $8k+2$, for $k \in \mathbb{N}$.

=--

([CLP 19, Thm. 5.11a](#CLP19))


+-- {: .num_prop }  
###### Proposition

Every [[torsion element]] in the [[SU-bordism ring]] $\Omega^{SU}_\bullet$ has [[order of an element|order]] 2.

=--

([CLP 19, Thm. 5.8b](#CLP19))

+-- {: .num_prop #SUBordismRingAwayFromTwo}  
###### Proposition
**([[SU-bordism ring]] [[localization of a ring|away from 2]] is [[polynomial algebra]])**

The [[SU-bordism ring]] with [[localization of a ring|2 inverted]] is the [[polynomial algebra]] over $\mathbb{Z}\big[\tfrac{1}{2}\big]$ on one generator in every even degree $\geq 4$:

$$
  \Omega^{SU}\big[\tfrac{1}{2}\big]
  \;\simeq\;
  \mathbb{Z}
  \big[
    \tfrac{1}{2}
  \big]
  \big[
    \{
      y_{2i+4}
    \}_{i \in \mathbb{N}}
  \big]
  \,.
$$

=--

(due to [Novikov 62](#Novikov62), review in [LLP 17, Thm. 1.2](#LLP17))

### Relation to Calabi-Yau manifolds
 {#RelationToCalabiYauManifolds}

We discuss the classes of [[Calabi-Yau manifolds]] in the [[SU-bordism ring]]. For more see at _[[Calabi-Yau manifolds in SU-bordism theory]]_.


+-- {: .num_prop #K3SurfaceSpansSUBordismRingInDegree4}  
###### Proposition
**([[K3-surface]] spans [[SU-bordism ring]] in degree 4)**

The degree-4 generator $y_4 \in \Omega^{SU}_4$ in the [[SU-bordism ring]] (Prop. \ref{SUBordismRingAwayFromTwo}) is represented by minus the class of any (non-[[torus]]) [[K3-surface]]:

\[
  \label{K3GeneratesNonTorsionSUBordimsRing}
  \Omega^{SU}_4 
    \;\simeq\; 
  \mathbb{Z}\big\langle -[K3] \big\rangle
  \,.
\]

=--

([LLP 17, Example 3.1](#LLP17), [CLP 19, Theorem 13.5a](#CLP19))


+-- {: .num_cor #K3SurfaceInUBordismRing}  
###### Corollary
**([[K3-surface]] represents non-trivial element in [[U-bordism ring]])**

The image in the [[MU]]-[[cobordism ring]] of the class of the [[K3-surface]] $[K3] \in \Omega^{SU}_4$ (eq:K3GeneratesNonTorsionSUBordimsRing) under the canonical morphism $\Omega^{SU}_4 \to \Omega^{\mathrm{U}}_4$ (eq:HomomorphismsOfCobordismRings) is non-trivial.

In fact, the canonical morphism is an [[injection]] in this degree

$$
  \array{
    \Omega^{SU}_4 
      &\hookrightarrow& 
    \Omega^{\mathrm{U}}_4
    \\
    [K3] &\mapsto& [K3]
    \,.
  }
$$

=--

(This is vaguely indicated in [Novikov 86, p. 216 (218 of 321)](#Novikov86).)

\begin{proof}
  By Prop. \ref{KernelOfMapFromSUBordismToUBordismIsTorsion} the 
  kernel of the map to $\Omega^{\mathrm{U}}_4$ is torsion, but by Prop. \ref{K3SurfaceSpansSUBordismRingInDegree4} $[K3]$ represents a non-torsion element. Since it is in fact a non-torsion generator, the kernel vanishes (as also implied by Prop. \ref{TorsionInSUBordismConcentratedInDegrees1And2Mod8}).

\end{proof}


+-- {: .num_prop }  
###### Proposition
**([[Calabi-Yau manifolds]] generate the [[SU-bordism ring]] [[localization of a ring|away from 2]])**

The [[SU-bordism ring]] [[localization of a ring|away from 2]] is multiplicatively generated by [[Calabi-Yau manifolds]]. 

=--

([LLP 17, Theorem 2.4](#LLP17))

+-- {: .num_prop }  
###### Proposition
**([[Calabi-Yau manifolds]] in complex dim $\leq 4$ span the [[SU-bordism ring]] in $deg \leq 8$ [[localization of a ring|away from 2]])**

There are [[Calabi-Yau manifolds]] of complex dimension $3$ and $4$ whose whose SU-bordism classes equal the generators $\pm y_6$ and $\pm y_8$ in Prop. \ref{SUBordismRingAwayFromTwo}. 

Together with the [[K3 surface]] representing $- y_4$ (Prop. \ref{K3SurfaceSpansSUBordismRingInDegree4}), this means that [[CYs]] [[linear space|span]] $\Omega^{SU}_{\leq 8}\big[ \tfrac{1}{2}\big]$.

=--

([CLP 19, Theorem 13.5](#CLP19))


## Related concepts

* [[Calabi-Yau manifold]]

* [[generalized Calabi-Yau manifold]]

\linebreak

[[!include flavours of cobordism cohomology theories -- table]]




## References

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 5 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))

On the SU-bordism ring structure away from 2:

* {#Novikov62} [[Sergei Novikov]], _Homotopy properties of Thom complexes_, Mat. Sbornik 57 (1962), no. 4, 407–442, 407&#8211;442 ([pdf](http://www.mi-ras.ru/~snovikov/6.pdf), [[NovikovThomComplexes.pdf:file]])

* {#Stong68} [[Robert Stong]], Chapter X of: _Notes on Cobordism theory_, Princeton University Press, 1968 ([toc pdf](http://pi.math.virginia.edu/StongConf/Stongbookcontents.pdf), [ISBN:9780691649016](http://press.princeton.edu/titles/6465.html), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/stongcob.pdf))


Survey:

* {#Novikov86} [[Sergei Novikov]], p. 218 in: _Topology I -- General survey_, in: Encyclopedia of Mathematical Sciences Vol. 12, Springer 1986 ([doi:10.1007/978-3-662-10579-5](https://link.springer.com/book/10.1007/978-3-662-10579-5), [pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/novikovsurv.pdf))


On its [[torsion subgroups]]:

* [[Pierre Conner]], [[Edwin Floyd]], _Torsion in $SU$-bordism_, Memoirs of the American Mathematical Society 1966 ([ISBN:978-1-4704-0007-1](https://bookstore.ams.org/memo-1-60))


Relation to [[Calabi-Yau manifolds]]:

* {#LLP17} [[Ivan Limonchenko]], [[Zhi Lu]], [[Taras Panov]], _Calabi-Yau hypersurfaces and SU-bordism_, Proceedings of the Steklov Institute of Mathematics 302 (2018), 270-278 ([arXiv:1712.07350](https://arxiv.org/abs/1712.07350))

Survey:

* {#CLP19} Georgy Chernykh, [[Ivan Limonchenko]], [[Taras Panov]], _$SU$-bordism: structure results and geometric representatives_, Russian Math. Surveys 74 (2019), no. 3, 461-524 ([arXiv:1903.07178](https://arxiv.org/abs/1903.07178))

* [[Taras Panov]], _A geometric view on $SU$-bordism_, talk at Moscow State University 2020 ([webpage](https://www.math.princeton.edu/events/geometric-view-su-bordism-2020-09-17t170000), [pdf](http://higeom.math.msu.su/people/taras/talks/2019SPb-Panov.pdf), [[PanovSU-Bordism.pdf:file]])




[[!redirects SU-bordism]]
[[!redirects SU-bordism theory]]


[[!redirects SU-cobordism]]
[[!redirects SU-cobordism theory]]

[[!redirects special unitary bordism ring]]
[[!redirects special unitary bordism rings]]

[[!redirects SU-bordism ring]]
[[!redirects SU-bordism rings]]

[[!redirects special unitary cobordism ring]]
[[!redirects special unitary cobordism rings]]

[[!redirects SU-cobordism ring]]
[[!redirects SU-cobordism rings]]



