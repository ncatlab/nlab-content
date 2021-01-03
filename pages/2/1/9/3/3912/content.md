
> This entry is about the isomorphisms in [[cohomology]] induced by [[Thom classes]]. For the [[Pontrjagin-Thom isomorphism]] in [[cobordism theory]] see at _[[Thom's theorem]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $H$ being [[ordinary cohomology]] with [[coefficients]] in a [[ring]], and $V \to X$ a [[vector bundle]] of rank $n$ over a simply connected CW-complex, the **Thom isomorphism** is the morphism
 
$$
  c \cup (-)
    \;\colon\; 
  H^\bullet(X) 
     \stackrel{\simeq}{\longrightarrow} 
  \tilde H^{\bullet + n}(Th(V))
  \,.
$$

from the [[cohomology]] of $X$ to the [[reduced cohomology]] of the [[Thom space]] $Th(V)$, given by pullback to the [[Thom space]] followed by [[cup product]] with a [[Thom class]] $c \in H^n(Th(V))$. That this is indeed an [[isomorphism]] follows via the [[Leray-Hirsch theorem]] (see e.g. [Ebert 12, 2.3,2.4](#Ebert12)) or from running a [[Serre spectral sequence]] (e.g. [Kochman 96, section 2.6](#Kochman96)).

In the special case that the vector bundle is trivial of rank $n$, then its [[Thom space]] coincides with the $n$-fold [[suspension]] of the base space ([exmpl.](Thom+space#ThomSpaceConstructionReducingToSuspension)) and the Thom isomorphism coincides with the [[suspension isomorphism]]. In this sense the Thom isomorphism may be regarded as a _twisted suspension isomorphism_.

More generally for $E$ a [[multiplicative cohomology theory]], and $V \to X$ a [[vector bundle]] of rank $n$, which is $E$-[[orientation in generalized cohomology|orientable]], there is a generalization to a  **Thom-Dold isomorphism** 
 
$$
  c \cup (-)
    \;\colon\; 
  E^\bullet(X) 
     \stackrel{\simeq}{\longrightarrow} 
  \tilde E^{\bullet + n}(Th(V))
$$

(e.g. [Rudyak 98, chapter V, 1.3](#Rudyak98), [Kochman 96, prop. 4.3.6](#Kochman96))

One may think of the Thom isomorphism from left to right as [[cup product|cupping]] with a generalized [[volume form]] on the fibers, and from right to left as performing [[fiber integration]] against this volume form.

## Statement

### Concretely

#### In ordinary cohomology

+-- {: .num_prop #Smooth0TypeIsSheavesOnSmoothMfd}
###### Proposition

Let $V \to B$ be a topological [[vector bundle]] of [[rank]] $n \gt 0$ over a [[simply connected topological space|simply connected]] [[CW-complex]] $B$. Let $R$ be a [[commutative ring]]. 

There exists an element $c \in H^n(Th(V);R)$ (in the [[ordinary cohomology]], with [[coefficients]] in $R$, of the [[Thom space]] of $V$, called a **[[Thom class]]**) such that forming the [[cup product]] with $c$ induces an [[isomorphism]]

$$
  H^\bullet(B;R)
    \overset{c \cup (-)}{\longrightarrow}
  \tilde H^{\bullet + n}(Th(V);R)
$$

of degree $n$ from the unreduced [[cohomology group]] of $B$ to the [[reduced cohomology]] of the [[Thom space]] of $V$.

=--

+-- {: .proof #ProofOfThomIsomorphismViaFiberwiseThomSpaceFibration}
###### Proof 
**(of Thom isomorphism via fiberwise Thom spaces)**


Choose an [[orthogonal structure]] on $V$. Consider the _fiberwise_ [[cofiber]] 

$$
  E \coloneqq D(V)/_B S(V)
$$

of the inclusion of the [[unit sphere]] bundle into the unit disk bundle of $V$ ([def.](Thom+space#ThomSpace)).

$$
  \array{
    S^{n-1} &\hookrightarrow& D^n &\longrightarrow& S^n
    \\
    \downarrow && \downarrow && \downarrow
    \\
    S(V) &\hookrightarrow& D(V) &\longrightarrow& E
    \\
    \downarrow && \downarrow && \downarrow^{\mathrlap{p}}
    \\
    B &=& B &=& B
  }
$$

Observe that this has the following properties

1. $E \overset{p}{\to} B$ is an [[n-sphere]] [[fiber bundle]], hence in particular a [[Serre fibration]];

1. the [[Thom space]] $Th(V)\simeq E/B$ is the quotient of $E$ by the base space, because of the [[pasting law]] applied to the following pasting diagram of [[pushout]] squares

   $$
     \array{ 
       S(V) &\longrightarrow& D(V)
       \\
       \downarrow &(po)& \downarrow
       \\
       B &\longrightarrow& D(V)/_B S(V)
       \\
       \downarrow &(po)& \downarrow
       \\
       \ast &\longrightarrow& Th(V)
     }
   $$

1. hence the [[reduced cohomology]] of the Thom space is ([def.](Introduction+to+Stable+homotopy+theory+--+S#ReducedToUnreducedGeneralizedCohomology)) the [[relative cohomology]] of $E$ relative $B$

   $$
     \tilde H^\bullet(Th(V);R) \simeq H^\bullet(E,B;R)
     \,.
   $$

1. $E \overset{p}{\to} B$ has a global [[section]] $B \overset{s}{\to} E$ (given over any point $b \in B$ by the class of any point in the fiber of $S(V) \to B$ over $b$; or abstractly: induced via the above pushout by the commutation of the projections from $D(V)$ and from $S(V)$, respectively).


In the following we write $H^\bullet(-)\coloneqq H^\bullet(-;R)$, for short.

By the first point, there is the [[Thom-Gysin sequence]], an [[exact sequence]] running vertically in the following diagram

$$
  \array{
    && H^\bullet(B)
    \\
    && {}^{\mathllap{p^\ast}}\downarrow  & \searrow^{\mathrlap{\simeq}}
    \\
    \tilde H^\bullet(Th(V))
      &\longrightarrow&
    H^\bullet(E)
      &\underset{s^\ast}{\longrightarrow}&
    H^\bullet(B)
    \\
    && \downarrow
    \\
    && H^{\bullet-n}(B)
  }
  \,.
$$ 

By the second point above this is [[split exact sequence|split]], as shown by the diagonal isomorphism in the top right. By the third point above there is the horizontal exact sequence, as shown, which is the [exact sequence in relative cohomology](generalized+%28Eilenberg-Steenrod%29+cohomology#ExactnessUnreduced) $\cdots \to H^\bullet(E,B) \to H^\bullet(E) \to H^\bullet(B) \to \cdots$ induced from the section $B \hookrightarrow E$.

Hence using the splitting to decompose the term in the middle as a [[direct sum]], and then using horizontal and vertical exactness at that term yields

$$
  \array{
    && H^\bullet(B)
    \\
    && {}^{\mathllap{(0,id)}}\downarrow  & \searrow^{\mathrlap{\simeq}}
    \\
    \tilde H^\bullet(Th(V))
      &\overset{(id,0)}{\hookrightarrow}&
    \tilde H^\bullet(Th(V))
      \oplus 
    H^\bullet(B)
      &\underset{(0,id)}{\longrightarrow}&
    H^\bullet(B)
    \\
    && \downarrow^{\mathrlap{(id,0)}}
    \\
    && H^{\bullet-n}(B)
  }
$$ 

and hence an isomorphism

$$
  \tilde H^\bullet(Th(V))
    \overset{\simeq}{\longrightarrow}
  H^{\bullet-n}(B)
  \,.
$$

To see that this is the inverse of a morphism of the form $c \cup (-)$, inspect the [proof of the Gysin sequence](Thom-Gysin+sequence#ProofOfThomGysinSequence). This shows that $H^{\bullet-n}(B)$ here is identified with elements that on the second page of the corresponding [[Serre spectral sequence]] are cup products 

$$
  \iota \cup b
$$ 

with $\iota$ fiberwise the canonical class $1 \in H^n(S^n)$ and with $b \in H^\bullet(B)$ any element. Since $H^\bullet(-;R)$ is a [[multiplicative cohomology theory]] (because the [[coefficients]] form a [[ring]] $R$), cup producs are preserved as one passes to the $E_\infty$-page of the spectral sequence, and the morphism $H^\bullet(E) \to B^\bullet(B)$ above, hence also the isomorphism $\tilde H^\bullet(Th(V)) \to H^\bullet(B)$, factors through the $E_\infty$-page (see towards the end of the [proof of the Gysin sequence](Thom-Gysin+sequence#ProofOfThomGysinSequence)). Hence the image of $\iota$ on the $E_\infty$-page is the Thom class in question.


=--

#### In generalized cohomology

Let $E$ be a [[generalized (Eilenberg-Steenrod) cohomology]] theory. First observe that an [[E-orientation]] on $V \to X$ induces an $H \pi_0(E)$-orientation, i.e. in [[ordinary cohomology]] with coefficients in the degree-0 ground ring.

To see this, let's assume $E$ is [[connective spectrum|connective]]. Consider the [[relative Atiyah-Hirzebruch spectral sequence]]

$$
  \tilde H^p(Th(V), E^q(\ast))
  \simeq
  H^p(D(V),S(V), E^q(\ast))
    \;\Rightarrow\;
  E^\bullet(D(V), S(V))
  \simeq
  \tilde E^\bullet(Th(V))
$$

Since $(D(V), S(V))$ is $(n-1)$-connected for a rank $n$ vector bundle, then $E_2^{p \lt n, q} = 0$. Hence the edge homomorphism

$$
  \tilde H^k(Th(V), E^0(\ast)) \longrightarrow \tilde H^0(Th(V))
$$

is an [[isomorphism]], and one checks that it sends Thom classes to Thom classes.

For a fully detailed account see ([Pedrotti 16](#Pedrotti16)).

### Abstractly

A general abstract discussion is around page 30, 31 of ([ABGHR](#ABGHR)).

(...)

## Applications

* The Thom isomorphism is used to define [[fiber integration]] of multiplicative cohomology theories.

## Related concepts

* [[Thom-Gysin sequence]]

* [[cobordism theory]]

* [[Thom space]], [[Thom spectrum]]

* [[fiber integration]]

* [[Pontrjagin-Thom collapse map]]

## References

The original proof that the Thom isomorphism is indeed an [[isomorphism]] is due to

* [[René Thom]],   _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_  Comm. Math. Helv. , 28  (1954)  pp. 17&#8211;86

The argument via a [[Serre spectral sequence]] for a relative fibration seems to be due to

* W. H. Cockcroft, _On the Thom isomorphism Theorem_, Mathematical Proceedings of the Cambridge Philosophical Society (1962), 58 ([web](http://journals.cambridge.org/abstract_S0305004100036409), [pdf](http://journals.cambridge.org/action/displayFulltext?type=1&fid=2056796&jid=PSP&volumeId=58&issueId=02&aid=2056788&bodyId=&membershipNumber=&societyETOCSession=))

Textbook accounts:


* {#Rudyak98} [[Yuli Rudyak]], chapter V of _Thom spectra, Orientability and Cobordism_, Springer 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))

Discussion in the generality of [[complex oriented cohomology theory]]:

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], Section 6 of: _[[The Relation of Cobordism to K-Theories]]_, Lecture Notes in Mathematics __28__ Springer 1966 ([doi:10.1007/BFb0071091](https://link.springer.com/book/10.1007/BFb0071091), [MR216511](http://www.ams.org/mathscinet-getitem?mr=216511))


* {#Kochman96} [[Stanley Kochman]], Section 2.6 of: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#TamakiKono06} [[Dai Tamaki]], [[Akira Kono]], Section 3.6 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))



Lecture notes:

* [[Akhil Mathew]], _[The Thom isomorphism theorem](https://amathew.wordpress.com/2010/12/11/the-thom-isomorphism-theorem/)_, 2010

* {#Ebert12} [[Johannes Ebert]], sections 2.3, 2.4 of _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf))

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lecture 21 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])


* {#Freed13} [[Dan Freed]], lecture 8 of _Bordism: old and new_, 2013 ([pdf](http://www.ma.utexas.edu/users/dafr/bordism.pdf))

* {#Pedrotti16} [[Riccardo Pedrotti]], _Complex oriented cohomology, generalized orientation and Thom isomorphism_, 2016, 2018 ([[PedrotticECohomology2018.pdf:file]])


A discussion in [[differential geometry]] with fiberwise compactly supported differential forms is around theorem 6.17 of 

* [[Raoul Bott]], [[Loring Tu]], _[[Differential Forms in Algebraic Topology]]_ 

A comprehensive general abstract account for [[multiplicative cohomology theories]] in terms of [[E-infinity ring]] [[spectra]] is in

* {#ABGHR} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 

An alternative simple formulation in terms of geometric cycles as in [[bivariant cohomology theory]] is in 

* Martin Jakob, _A note on the Thom isomorphism in geometric (co)homology_ ([arXiv:math/0403540](http://arxiv.org/abs/math/0403540))


See also

* [[Albrecht Dold]], _Relations between ordinary and extraordinary homology_ , Colloq. Algebraic Topology, August 1&#8211;10, 1962 , Inst. Math. Aarhus Univ.  (1962)  pp. 2&#8211;9


* [[Yuli Rudyak]], _On the Thom&#8211;Dold isomorphism for nonorientable bundles_  Soviet Math. Dokl. , 22  (1980)  pp. 842&#8211;844  Dokl. Akad. Nauk. SSSR , 255 : 6  (1980)  pp. 1323&#8211;1325

* [[Robert Switzer]], _Algebraic topology - homotopy and homology_ , Springer  (1975)

* myyn.org (Planetmath) [Thom space](http://myyn.org/m/article/thom-space), [Thom class](http://myyn.org/m/article/thom-class), [Thom isomorphism theorem](http://myyn.org/m/article/thom-isomorphism-theorem)

Formalization in [[homotopy type theory]] is discussed in

* {#Brunerie16} [[Guillaume Brunerie]], _On the homotopy groups of spheres in homotopy type theory_ ([arXiv:1606.05916](http://arxiv.org/abs/1606.05916))



[[!redirects Thom isomorphisms]]

[[!redirects Thom-Dold isomorphism]]
[[!redirects Thom-Dold isomorphisms]]

