
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $Y \to Z$ a morphism of [[pointed object|pointed]] [[∞-groupoid]]s and $X \to Y$ its [[homotopy fiber]], there is a [[long exact sequence]] of [[homotopy group]]s

$$
  \cdots \to \pi_{n+1}(Z) \to \pi_n(X) \to \pi_n(Y) \to \pi_n(Z) \to \pi_{n-1}(X) \to \cdots
  \,.
$$

In terms of [[presentable (infinity,1)-category|presentations]] this means:

for $Y \to Z$ a [[fibration]] in the [[classical model structure on topological spaces]] or in the [[classical model structure on simplicial sets]], and for $X \to Y$ the ordinary [[fiber]] of [[topological spaces]] or [[simplicial sets]], respectively, we have such a long exact sequence.

For background and details see [[fibration sequence]].


## Properties
 {#Properties}

\begin{proposition}
  **(fundamental crossed module of a fibration)**
  \label{FundamentalCrossedModuleOfAFibration}
\linebreak
  Given a [[Serre fibration]] $p \,\colon\, T \longrightarrow B$ of [[pointed topological spaces]], with [[fiber]] $\iota \,\colon\,F \longrightarrow T$, the induced [[homomorphism]] of [[fundamental groups]]
$$
  \pi_1(F)
  \xrightarrow{\phantom{--}
    \iota_\ast
  \phantom{--}}
  \pi_1(T)
$$
constitutes a [[crossed module]] with respect to the canonical [[group action]] $\alpha \,\colon\, \pi_1(T) \times \pi_1(F) \longrightarrow \pi_1(F)$.
\end{proposition}
This is discussed in [Brown, Higgins & Sivera 2011, §2.6](#BHS11), there attributed to [[Daniel Quillen]].


\begin{proposition}
\label{FirstConnectingHomomorphismFactorsThroughCenter}
Given a [[Serre fibration]] $p \,\colon\, T \longrightarrow B$ of [[pointed topological spaces]], with [[fiber]] $\iota \,\colon\,F \longrightarrow T$, the [[image]] of the first [[connecting homomorphism]] of the corresponding [[long exact sequence of homotopy groups]]
$$
  \pi_2(B) \longrightarrow \pi_1(F)
$$
is in the [[center]] $Z\big(\pi_1(F)\big) \hookrightarrow \pi_1(F)$.
\end{proposition}
\begin{proof}
  By [[exact sequence|exactness]], the image in question is the [[kernel]] of $\pi_1(F) \to \pi_1(T)$, which is the homomorphism of a [[crossed module]] by Prop. \ref{FundamentalCrossedModuleOfAFibration}, and the kernels of such homomorphisms are central (by [this Prop.](crossed+module#KernelOfDeltaIsCentral)).

Instead, textbooks usually state an analogous property for the LES of relative homotopy groups: For $(X,A)$ a "[[CW-pair|pair]]" --- hence a [[subspace]] inclusion $A \hookrightarrow X$ (here: of [[pointed topological spaces]]) --- there is a [[long exact sequence]] of the form

$$
  \cdots
  \to
  \pi_{n+1}(X,A)
  \longrightarrow
  \pi_n(A)
  \longrightarrow
  \pi_n(X)
  \longrightarrow
  \pi_n(X,A)
$$

such that 

$$
  \pi_2(A) \longrightarrow \pi_2(X,A)
$$

factors through the center (cf. [Whitehead 1978 Cor 3.5 on p. 166](#Whitehead78), [tom Dieck 2008 Cor 6.2.7](#tomDieck08)).

With a little care, this translates to the statement here by specializing $A \coloneqq T$ and taking $X \coloneqq Cyl(T \to B)$ to be the [[mapping cylinder]] of the fibration.
\end{proof}


## Related concepts

* [[long exact sequence in homology]]

  * [[long exact sequence in chain homology]]

  * [[long exact sequence in generalized homology]]

* [[fiber sequence]]

* [[Gysin sequence]]

* [[Serre long exact sequence]]

* Given a [[tower of homotopy fibers]] such as a [[Whitehead tower]] or [[Adams resolution]], the long exact sequences of homotopy groups for each stage combine to yield an [[exact couple]]. The corresponding [[spectral sequence]] is the _[[Adams spectral sequence]]_.

## References

The observation of long exact sequences of homotopy groups for [[homotopy fiber sequences]] originates (according to [Switzer 75, p. 35](#Switzer75)) in 

* M. G. Barratt, _Track groups I, II_. Proc. London Math. Soc. 5, 71-106, 285-329 (1955). 

The first exhaustive study of these is due to 

* {#Puppe58} [[Dieter Puppe]]: _Homotopiemengen und ihre induzierten Abbildungen I_, Math. Z. **69** (1958)  299-344 &lbrack;[doi:10.1007/BF01187411](https://doi.org/10.1007/BF01187411), [eudml:169745](https://eudml.org/doc/169745), [pdf](https://webhomes.maths.ed.ac.uk/~v1ranick/papers/puppe1.pdf)&rbrack;

whence the terminology _Puppe sequences_.


Textbook accounts:

* [[Norman Steenrod]], Thm. 17.4 in: _The topology of fibre bundles_, Princeton Mathematical Series **14**, Princeton Univ. Press (1951) &lbrack;[jstor:j.ctt1bpm9t5](https://www.jstor.org/stable/j.ctt1bpm9t5)&rbrack;

* {#Switzer75} [[Robert Switzer]], around 2.59 in: _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen **212** Springer (1975) &lbrack;[doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6)&rbrack;

* {#Whitehead78} [[George W. Whitehead]], section IV.2 in: *Elements of Homotopy Theory*, Springer (1978) \[<a href="https://link.springer.com/book/10.1007/978-1-4612-6318-0">doi:10.1007/978-1-4612-6318-0</a>\] 

* {#Kochmann96} [[Stanley Kochmann]], Corollary 3.2.7 in: _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, Fields Institute Monographs **7** American Mathematical Society (1996) &lbrack;[ams:fim-7](https://bookstore.ams.org/fim-7), [cds:2264210](https://cdsweb.cern.ch/record/2264210)&rbrack;

* {#Hatcher02} [[Allen Hatcher]], p. 344 of: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;

* {#tomDieck2008} [[Tammo tom Dieck]],  Thm. 6.1.2 in: _Algebraic topology_, European Mathematical Society (2008) &lbrack;[doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/diecktop.pdf)&rbrack;

* [[Anatoly Fomenko]], [[Dmitry Fuchs]], section 9.8 of: *Homotopical Topology*, Graduate Texts in Mathematics **273**, Springer (2016) \[<a href="https://doi.org/10.1007/978-3-319-23488-5">doi:10.1007/978-3-319-23488-5</a>, <a href="https://www.cimat.mx/~gil/docencia/2020/topologia_diferencial/[Fomenko,Fuchs]Homotopical_Topology(2016).pdf">pdf</a>\]


See also:

* Wikipedia, _[Long exact sequence of a fibration](http://en.wikipedia.org/wiki/Homotopy_group#Long_exact_sequence_of_a_fibration)_

* {#BHS11} [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]]: *[[Nonabelian Algebraic Topology]]*, Tracts in Mathematics **15**, European Mathematical Society (2011) &lbrack;ISBN 978-3-03719-083-8, [doi:10.4171/083](https://doi.org/10.4171/083), [pdf](https://groupoids.org.uk/pdffiles/NAT-book.pdf), [webpage](http://groupoids.org.uk/nonab-a-t.html)&rbrack;


In the generality of [[categorical homotopy groups in an (infinity,1)-topos|categorical homotopy groups in an $(\infty,1)$-topos]]:

* [[Jacob Lurie]], Rem. 6.5.1.5 of: _[[Higher Topos Theory]]_, Annals of Mathematics Studies **170**, Princeton University Press (2009) &lbrack;[pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf)&rbrack;




[[!redirects long exact sequences of homotopy groups]]

