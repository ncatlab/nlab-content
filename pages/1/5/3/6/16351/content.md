
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The [[functor]] which sends 

1. [[smooth manifolds]] to their [[algebras of functions|algebras of]] [[smooth functions]] with values in the [[real numbers]], regarded just as $\mathbb{R}$-[[associative algebras|algebras]] (instead of, say [[smooth algebras]] aka "$C^\infty$-rings"),

1. [[smooth functions]] between these manifolds to the corresponding [[pullback of a function|pullback]]/[[precomposition]] [[algebra homomorphisms]] between these function algebras

turns out to be [[fully faithful functor|fully faithful]], hence a [[full subcategory]] embedding of [[SmthMfd]] into the [[opposite category|opposite]] of [[Alg|$\mathbb{R}Alg$]].

This is remarkable, because such a relation between [[spaces]] and their *plain* [[algebras of functions]] is (more) manifest only for [[affine varieties]] in [[algebraic geometry]], where however it holds essentially by construction. 
In contrast, nothing in the usual definition of [[smooth manifolds]] manifestly suggests that they behave to some extent similarly to [[affine varieties]] with respect to $\mathbb{R}$-algebras of smooth functions. (See also at *[[duality between algebra and geometry]]*.)

Related "miracles" in [[differential geometry]], revealing a maybe surprising [[algebraic geometry|algebro-geometric]]-nature, are the facts that:

* [[derivations of smooth functions are vector fields]],

* [[Kähler C^∞-differentials of smooth functions are differential 1-forms]],

* [[smooth differential forms form the free C^∞-DGA on smooth functions]]

* [[smooth Serre-Swan theorem|finitely generated projective modules over smooth functions are smooth vector bundles]].

Accordingly, the embedding of smooth manifolds into [[formal duality|formal duals]] of $\mathbb{R}$-algebras allows to import some constructions and tools from [[algebraic geometry]] into [[differential geometry]] *without* strengthening the notion of "algebra" to something like [[smooth algebras]].

This is useful and is used particularly for discussions in [[synthetic differential geometry]] --- cf. e.g. the emphasis on "Weil algebras", hence of would-be function algebras on [[infinitesimally thickened points]], in [Kolář, Michor & Slovák 1993 §35](#KolarSlovakMichor93).



## Statement

\begin{lemma}\label{MilnorExercise}
**([Pursell, Section 8](#Pursell52), 1952)**
\linebreak
For a [[smooth manifold]] $X \in SmthMfd$, the [[evaluation map]] (from its [[underlying]] [[set]] to the [[hom-set]])
$$
  \begin{array}{l}
   X 
     &\overset{ev}{\longrightarrow}& 
   Hom_{Alg_{\mathbb{R}}}
   \big(
     C^\infty(X)
     ,\,
     \mathbb{R}
   \big)
   \\
   x &\mapsto&
   \big(
     \phi \,\mapsto\, \phi(x)
   \big)
  \end{array}
$$
is a [[bijection]].
\end{lemma}

The statement also appears in [Milnor & Stasheff (1974) Prob. 1-C (p. 11)](#MilnorStasheff74) and a detailed proof different from the one below is given by [Kolář, Michor & Slovák 1993 Lem. 35.8 & Cor. 35.9](#KolarSlovakMichor93).

\begin{proof}
We provide a simplified proof using [[Hadamard's lemma]].
Suppose $M$ is a [[smooth manifold]] and $\phi\colon C^\infty(M)\to\mathbf{R}$ is a homomorphism of real algebras.

If $M=\mathbf{R}^n$ for some $n\ge0$, then set $y_i=\phi(x_i)$, where $x_i\colon\mathbf{R}^n\to\mathbf{R}$ is the $i$th coordinate function.
We have
$$\phi(f)=\phi(f(y)+\sum_i (x_i-y_i)\cdot g_i)=f(y)+\sum_i (\phi(x_i)-y_i)\cdot \phi(g_i)=f(y),$$
where the functions $g_i$ are provided by [[Hadamard's lemma]].

For a general $M$,
use [[Whitney's embedding theorem]] to embed $M$ into some $\mathbf{R}^n$.
Without loss of generality we can assume the embedding to be proper so that the subset $M\subset\mathbf{R}^n$ is closed.

Consider the composition
$$C^\infty(\mathbf{R}^n)\to C^\infty(M)\to \mathbf{R},$$
where the first homomorphism $\rho$ is given by restricting along the embedding.
The composition is given by evaluating at some point $p\in\mathbf{R}^n$.

If $p\notin M$, we can construct a smooth function $b$ that vanishes on $M$ and does not vanish at $p$.
For example, we can take the smooth function with zero locus $M$ constructed by the smooth Tietze extension theorem, or simply use smooth bump functions.
The function $b$ vanishes on $M$ and therefore belongs to the kernel of the map $\rho$.
The evaluation homomorphism at $p\notin M$ does not vanish on the element $b$, hence cannot factor through the map $\rho$, a contradiction.
Therefore, we must have $p\in M$.
\end{proof}

Pursell's theorem (Lemma \ref{MilnorExercise}) implies --- and also is the special case for $X = \ast$ (the [[point space|point]]) of:
\begin{theorem}\label{Embedding}
The [[functor]]
$$
  \begin{array}{ccc}
  SmthMfd 
    &\longrightarrow& 
  Alg_{\mathbb{R}}^{op}
  \\
  X &\mapsto& C^\infty(X)
  \\
  \mathllap{{}^f}\Big\downarrow
  &&  
  \Big\uparrow\mathrlap{{}^{{f^\ast}}}
  \\
  Y
  &\mapsto&
  C^\infty(Y)  
  \end{array}
$$
which sends a [[smooth manifold]] ([[finite number|finite]] [[dimension|dimensional]], [[paracompact topological space|paracompact]], [[second countable topological space|second countable]]) to (the [[formal dual]] of) its $\mathbb{R}$-[[associative algebra|algebra]] of [[smooth functions]], $C^\infty(X) \coloneqq C^\infty(X, \mathbb{R})$, is a [[full and faithful functor]].

In other words, given a [[pair]] of [[smooth manifolds]] $X,Y$ then the operation of [[precomposition]] ([[pullback of a function|pullback of functions]]) $f^\ast(g) \coloneqq g \circ f$ constitutes a [[natural bijection]] 

$$
  \begin{array}{l}
    C^\infty(X,Y)
    &\overset{\sim}{\longrightarrow}&
   Hom_{Alg_{\mathbb{R}}}\big(
     C^\infty(Y)
     ,\,
     C^\infty(X)
   \big)
   \\
   f &\mapsto& f^\ast
  \end{array}
$$

between 

1. the [[smooth functions]] $X \to Y$,

1. the $\mathbb{R}$-[[associative algebra|algebra]] [[homomorphisms]] $C^\infty(X)\leftarrow C^\infty(Y)$.

In particular, the [[diffeomorphisms]] between smooth manifolds are in [[natural bijection]] to the [[isomorphisms]] between their [[algebras of functions]].
\end{theorem}
([Kolář, Slovák & Michor 1993 Cor. 35.10](#KolarSlovakMichor93))
\begin{proof}
\label{ProofFromMilnorExercise}
It is clear that the functor is [[faithful functor|faithful]]; we need to show that it is [[full functor|full]], hence that for any $\mathbb{R}$-algebra homomorphism
$$
  \phi
  \;\colon\;
  C^\infty(Y, \mathbb{R})
  \longrightarrow
  C^\infty(X, \mathbb{R})
$$
there exists a smooth function $f \colon X \to Y$ such that $\phi = f^\ast$.

To that end, observe that given a point $x \in X$, the [[postcomposition]] of $\phi$ with the [[evaluation map]] at $x$
$$  
  C^\infty(Y, \mathbb{R})
  \overset{ \phi }{\longrightarrow}
  C^\infty(X, \mathbb{R})
  \overset{ ev_x }{\longrightarrow}
  \mathbb{R}
$$
is an algebra homomorphism of the form assumed in Pursell's theorem (Lemma \ref{MilnorExercise}) and thus given uniquely by evaluation at some point $f(x) \in Y$
$$
  ev_x \circ \phi \;=\; ev_{f(x)}
  \,.
$$
This implies that $\phi$ acts on any $g \in C^\infty(Y)$ by
$$
  \begin{array}{rcl}
    g 
     &\overset{\phi}{\mapsto}& 
    \big(
      x \mapsto \phi(g)(x)
    \big)
    \\
    &=&
    \Big(
      x \mapsto ev_x(\phi(g))
    \Big)
    \\
    &=&
    \Big(
      x \mapsto ev_{f(x)}(g)
    \Big)
    \\
    &=&
    \Big(
      x \mapsto g\big(f(x)\big)
    \Big)
    \\
    &=&
    \Big(
      x \mapsto (g \circ f)(x)
    \Big)
    \mathrlap{\,,}
  \end{array}
$$
hence that it acts by precomposition with the assignment $f$:
$$
  \phi(g) \;=\; g \circ f
  \,.
$$

It just remains to observe that this $f$ is necessarily [[smooth function|smooth]]. But since $\phi$ is given on *all* $g \in C^\infty(Y)$ this way, to see that $f$ is smooth at some $x \in X$, choose any [[coordinate chart]] $U \subset Y$ around $f(x) \in Y$ and consider a $g$ which restricts to one of the [[coordinate functions]] $x^i$ on $U$. Then $(g \circ f)_{\vert f^{-1}(U)} = f^i_{\vert f^{-1}(U)}$ is the $i$th coordinate component of $f$ restricted to a neighbourhood of $x$, and this being smooth for all $i$ means that $f$ is smooth around $x$.
\end{proof}



\begin{remark}\label{Attribution}
**(attribution)**
\linebreak
For the case of [[diffeomorphisms]], Thm. \ref{Embedding} was proven by [Pursell (1952)](#Pursell52), following an announcement by [Shanks (1951)](#Shanks51). This is the case that most reviews focus on, e.g. [Grabowski (1978)](#Grabowski78), [Marsden, Ratiu & Abraham (2002)](#MarsdenRatiuAbraham02), [Grabowski (2005)](#Grabowski05).

For the case that the domain is a point the statement is contained in the dissertation of [Pursell](#Pursell) (Section 8), see Lemma \ref{MilnorExercise}.
It is also left as an [[exercise]] (without reference to Pursell) in [Milnor & Stasheff (1974) §1, Problem 1-C (p. 11)](#MilnorStasheff74), sometimes now referred to (not entirely appropriately) as "Milnor's exercise", even though Pursell's proof was published 22 years prior in 1952.  A detailed proof is also given in [Kolář, Slovák & Michor (1993) 35.8-9](#KolarSlovakMichor93).

The general statement of Theorem \ref{Embedding} appears as [Kolář, Slovák & Michor (1993) 35.10](#KolarSlovakMichor93).
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

* {#Pursell52} [[Lyle Eugene Pursell]]: _Algebraic structures associated with smooth manifolds_, PhD dissertation, Purdue University (1952)  93 pp.  &lbrack;ISBN:978-1392-88143-9, [proquest:2327629257](https://www.proquest.com/docview/2327629257), [pdf](https://ncatlab.org/nlab/files/pursell-dissertation.pdf)&rbrack;

following an announcement in 

* {#Shanks51} M. E. Shanks, *Rings of functions on locally compact spaces*, 469th meeting of the AMS (1951) &lbrack;[pdf](https://www.ams.org/journals/bull/1951-57-04/S0002-9904-1951-09521-X/S0002-9904-1951-09521-X.pdf)&rbrack; 

See also:

* [[Janez Mrčun]]: _On isomorphisms of algebras of smooth functions_, Proceedings of the American Mathematical Society **133** 10 (2005) 3109-3113 &lbrack;[arXiv:math/0309179](https://arxiv.org/abs/math/0309179), [doi:10.1090/s0002-9939-05-07979-7](http://dx.doi.org/10.1090/s0002-9939-05-07979-7)&rbrack;

* [[Janusz Grabowski]]: _Isomorphisms of algebras of smooth functions revisited_, Arch. Math. **85** (2005) 190–196 &lbrack;[arXiv:math/0310295](https://arxiv.org/abs/math/0310295), [doi:10.1007/s00013-005-1268-3](https://doi.org/10.1007/s00013-005-1268-3)&rbrack;

The statement for domain a point appears as an exercise in:

* {#MilnorStasheff74} [[John Milnor]], [[James Stasheff]], Problem 1-C (p. 11) in: _Characteristic Classes_, Annals of Mathematics Studies, Princeton University Press (1974) &lbrack;[ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [pdf](/nlab/files/Milnor_exercise.pdf)&rbrack;

A proof is spelled out in

* {#Dubuc79} [[Eduardo Dubuc]], Prop. 0.7 in: *Sur les modèles de la géométrie différentielle synthétique*, [[Cahiers|Cahiers de Topologie et Géométrie Différentielle Catégoriques]] **20**  3 (1979) 231-279  &lbrack;[numdam:CTGDC_1979__20_3_231_0](http://www.numdam.org/item?id=CTGDC_1979__20_3_231_0)&rbrack; 
  > (in defining the [[Cahiers topos]])


Expository accounts for the case of [[isomorphisms]] are in

* {#Grabowski78} [[Janusz Grabowski]], _Isomorphisms and ideals of the Lie algebras of vector fields_, Inventiones mathematicae volume 50, pages 13–33 (1978) ([doi:10.1007/BF01406466](https://doi.org/10.1007/BF01406466))

* {#MarsdenRatiuAbraham02} [[Jerrold Marsden]], J. Ratiu, R. Abraham, Theorem 4.2.36 in: _Manifolds, tensor analysis, and applications_, Springer 2003 ([ISBN:978-1-4612-1029-0](https://www.springer.com/gp/book/9780387967905))

* {#Grabowski05} [[Janusz Grabowski]], _Isomorphisms of algebras of smooth functions revisited_, Arch. Math. 85 (2005), 190-196 ([arXiv:math/0310295](https://arxiv.org/abs/math/0310295))

The general statement and its proof is discussed in:

* {#KolarSlovakMichor93} [[Ivan Kolář]], [[Peter Michor]], [[Jan Slovák]], chapter 35 of: _[[Natural operations in differential geometry]]_, Springer (1993) &lbrack;[book webpage](http://www.emis.de/monographs/KSM/), [doi:10.1007/978-3-662-02950-3](https://link.springer.com/book/10.1007/978-3-662-02950-3), [pdf](http://www.emis.de/monographs/KSM/kmsbookh.pdf)&rbrack;



Discussion that takes the dual algebraic formulation as the very definition of [[smooth functions]] is in

* {#Nestruev03} [[Jet Nestruev]], section 6 of: *Smooth manifolds and Observables*, Graduate Texts in Mathematics **220** Springer (2002, 2020) &lbrack;[doi:10.1007/978-3-030-45650-4](https://doi.org/10.1007/978-3-030-45650-4), ISBN:0-387-95543-7, <a href="https://nzdr.ru/data/media/biblio/kolxoz/M/MD/MDdg/Nestruev%20J.%20Smooth%20Manifolds%20and%20Observables%20(ISBN%200387955437)(Springer,%202003)(224s)_MDdg_.pdf">pdf</a>&rbrack;

The analog of the statement for real algebras refined to [[smooth algebras]] is Theorem 2.8 in

* [[Ieke Moerdijk]], [[Gonzalo Reyes|Gonzalo E. Reyes]], _[[Models for Smooth Infinitesimal Analysis]]_ Springer (1991)

[[!redirects Milnor's exercise]]

[[!redirects smooth manifolds embed into formal duals of R-algebras]]
[[!redirects Milnor duality]]
[[!redirects Pursell duality]]
