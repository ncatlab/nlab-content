
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Statement

+-- {: .num_theorem #Embedding}
###### Theorem

The [[functor]]
$$
  C^\infty(-) 
   \;\colon\; 
  SmoothMfd 
    \longrightarrow 
  Alg_{\mathbb{R}}^{op}
$$
which sends a [[smooth manifold]] ([[finite number|finite]] [[dimension|dimensional]], [[paracompact topological space|paracompact]], [[second countable topological space|second countable]]) to (the [[formal dual]] of) its $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]] is a [[full and faithful functor]].

In other words, for two [[smooth manifolds]] $X,Y$ there is a [[natural bijection]] between the [[smooth functions]] $X \to Y$ and the $\mathbb{R}$-[[associative algebra|algebra]] [[homomorphisms]] $C^\infty(X)\leftarrow C^\infty(Y)$.

In particular, the [[diffeomorphisms]] between smooth manifolds are in [[natural bijection]] to the [[isomorphisms]] between these algebras.

=--

\begin{remark}\label{Attribution}
**(attribution)**
\linebreak
For the case of [[diffeomorphisms]], Thm. \ref{Embedding} was proven by [Pursell (1952)](#Pursell52), following an announcement by [Shanks (1951)](#Shanks51). This is the case that most reviews focus on, e.g. [Grabowski (1978)](#Grabowski78), [Marsden, Ratiu & Abraham (2002)](#MarsdenRatiuAbraham02), [Grabowski (2005)](#Grabowski05).

For the case that the domain is a point the statement is an an [[exercise]] (without reference to Pursell) in [Milnor & Stasheff (1974), Problem 1-C (p. 11)](#MilnorStasheff74), sometimes now referred to as "Milnor's exercise". 

The general statement of Thm. \ref{Embedding}, with a detailed proof, is given in [Kolář, Slovák & Michor (1993), lemma 35.8, corollaries 35.9, 35.10](#KolarSlovakMichor93).
\end{remark}


+-- {: .num_remark}
###### Remark

The statement of theorem \ref{Embedding} serves as the stepping-stone for generalizations of [[differential geometry]] such as to [[supergeometry]]. On the other hand, for transporting various applications familiar from [[algebraic geometry]] to [[differential geometry]] (such as [[Kähler differentials]], see there) the above embedding is insufficient, and instead of just remembering the [[associative algebra]] structure, one needs to remember the _[[smooth algebra]]_-structure on algebras of smooth functions. See also at _[[synthetic differential geometry]]_.

=--

+-- {: .num_remark}
###### Remark

If one drops standard regularity assumptions on manifolds then theorem \ref{Embedding} may break. For instance allowing [[countable set|uncountably]] many connected components, then there are counterexamples ([MO discussion](http://mathoverflow.net/a/91445)).

=--

## Related theorems

* [[Borel's theorem]]

* [[Hadamard's lemma]]

* the [[Tietze extension theorem]]

* the [[Whitney extension theorem]]

* the [[Steenrod-Wockel approximation theorem]]

* [[smooth Serre-Swan theorem]]

* [[derivations of smooth functions are vector fields]]

The analogous statement in [[topology]] is:

* [[Gelfand duality]]

[[!include Isbell duality - table]]




## References

The case of the category of [[smooth manifolds]] with (just) [[diffeomorphisms]] between them is proved in

* {#Pursell52} [[Lyle Eugene Pursell]], _Algebraic structures associated with smooth manifolds_, PhD dissertation, Purdue University, (1952)  93 pp.  &lbrack;ISBN:978-1392-88143-9, [proquest:2327629257](https://www.proquest.com/docview/2327629257)&rbrack;

following an announcement in 

* {#Shanks51} M. E. Shanks, *Rings of functions on locally compact spaces*, 469th meeting of the AMS (1951) &lbrack;[pdf](https://www.ams.org/journals/bull/1951-57-04/S0002-9904-1951-09521-X/S0002-9904-1951-09521-X.pdf)&rbrack; 

The statement for domain a point is due to

* {#MilnorStasheff74} [[John Milnor]], [[James Stasheff]], Problem 1-C (p. 11) in: _Characteristic Classes_, Annals of Mathematics Studies, Princeton University Press (1974) &lbrack;[ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76)&rbrack;

with a proof spelled out in:

* {#Dubuc79} [[Eduardo Dubuc]], Prop. 0.7 in: *Sur les modèles de la géométrie différentielle synthétique*, [[Cahiers|Cahiers de Topologie et Géométrie Différentielle Catégoriques]] **20**  3 (1979) 231-279  &lbrack;[numdam:CTGDC_1979__20_3_231_0](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)&rbrack; 

  > (in defining the [[Cahiers topos]])


Expository accounts for the case of [[isomorphisms]] are in

* {#Grabowski78} [[Janusz Grabowski]], _Isomorphisms and ideals of the Lie algebras of vector fields_, Inventiones mathematicae volume 50, pages 13–33 (1978) ([doi:10.1007/BF01406466](https://doi.org/10.1007/BF01406466))

* {#MarsdenRatiuAbraham02} [[Jerrold Marsden]], J. Ratiu, R. Abraham, Theorem 4.2.36 in: _Manifolds, tensor analysis, and applications_, Springer 2003 ([ISBN:978-1-4612-1029-0](https://www.springer.com/gp/book/9780387967905))

* {#Grabowski05} [[Janusz Grabowski]], _Isomorphisms of algebras of smooth functions revisited_, Arch. Math. 85 (2005), 190-196 ([arXiv:math/0310295](https://arxiv.org/abs/math/0310295))

The general statement and its proof is discussed in:

* {#KolarSlovakMichor93} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], chapter 35 of: _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[book webpage](http://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;



Discussion that takes the dual algebraic formulation as the very definition of [[smooth functions]] is in

* {#Nestruev03} [[Jet Nestruev]], section 6 of: _Smooth manifolds and Observables_, Graduate Texts in Mathematics 218, Springer 2003 ([doi:10.1007/b98871](https://link.springer.com/book/10.1007/b98871))

The analog of the statement for real algebras refined to [[smooth algebras]] is theorem 2.8 in

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

[[!redirects Milnor's exercise]]

[[!redirects smooth manifolds embed into formal duals of R-algebras]]
[[!redirects Milnor duality]]