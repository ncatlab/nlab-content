
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



# Contents
* table of contents
{:toc}

## Idea

In the general context of [[cohomology]], as described there, a [[cocycle]] representing a cohomology class on an object $X$ with coefficients in an object $A$ is a [[morphism]] $c : X \to A$ in a given ambient [[(∞,1)-topos]] $\mathbf{H}$.

The same applies with the object $A$ taken as the domain object: for $B$ yet another object, the $B$-valued cohomology of $A$ is similarly $H(A,B) = \pi_0 \mathbf{H}(A,B)$. For $[k] \in H(A,B)$ any cohomology class in there, we obtain an [[∞-functor]]

$$
  [k(-)] : \mathbf{H}(X,A) \to \mathbf{H}(X,B)
$$

from the $A$-valued cohomology of $X$ to its $B$-valued cohomology, simply from the composition operation

$$
  \mathbf{H}(X,A) \times \mathbf{H}(A,B) \to \mathbf{H}(X,B)
  \,.
$$

Quite generally, for $[c] \in H(X,A)$ an $A$-cohomology class, its image $[k(c)] \in H(X,B)$ is the corresponding **characteristic class**.

Notice that if $A = \mathbf{B}G$ is [[connected]], an $A$-cocycle on $X$ is a $G$-[[principal ∞-bundle]]. Hence characteristic classes are equivalently characteristic classes of principal $\infty$-bundles.

+-- {: .standout}

From the [[nPOV]], where [[cocycle]]s are elements in an [[derived hom space|(∞,1)-categorical hom-space]], forming **characteristic classes** is nothing but the _composition_ of cocycles.

=--

In practice one is interested in this notion for particularly simple objects $B$, notably for $B$ an [[Eilenberg-MacLane object]] $\mathbf{B}^n K$ for some component $K$ of a [[spectrum object]]. This serves to **characterize** cohomology with coefficients in a complicated object $A$ by a collection of cohomology classes with simpler coefficients. Historically the name _characteristic class_ came a little different way about, however (see also [[historical note on characteristic classes]]).

In that case, with the usual notation $H^n(X,K) := H(X, \mathbf{B}^n K)$, a given characteristic class in degree $n$ assigns

$$
  [k(-)] : \mathbf{H}(X,A) \to H^n(X,K)
  \,.
$$

Moreover, recall from the discussion at [[cohomology]] that to every [[cocycle]] $c : X \to A$ is associated the object $P \to X$ that it classifies -- its [[homotopy fiber]] -- which may be thought of as an $A$-[[principal ∞-bundle]] over $X$ with classifying map $X \to A$. One typically thinks of the characteristic class $[k(c)]$ as characterizing this [[principal ∞-bundle]] $P$.

## Examples

### Characteristic classes of principal bundles

This is the archetypical example: let $\mathbf{H}  =$ [[Top]] $\simeq$  [[∞Grpd]], the canonical [[(∞,1)-topos]] of [[discrete ∞-groupoid]]s, or more generally let $\mathbf{H} = $ [[ETop∞Grpd]], the [[cohesive (∞,1)-topos]] of [[Euclidean-topological ∞-groupoid]]s.

For $G$ [[topological group]] write  $B G$ for its [[classifying space]]: the ([[geometric realization]] of its) [[delooping]].

For $A$ any other [[abelian group|abelian]] [[topological group]], similarly write $B^n A$ for its $n$-fold [[delooping]]. If $A$ is a [[discrete group]] then this is the [[Eilenberg-MacLane space]] $K(A,n)$. 

Generally, 

$$
  H^n(B G, A) = \pi_0 \mathbf{H}(B G, B^n A)
$$

is the [[cohomology]] of $B G$ with coefficients in $A$. Every [[cocycle]] $k : B G \to B^n A$ represents a characteristic class $[k]$ on $B G$ with coefficients in $A$.

A $G$-[[principal bundle]] $P \to X$ is classified by some map $c: X \to B G$. For any $k \in H^n(B G, A)$ a degree $n$ cohomology class of the classifying space, the corresponding composite map
$X \stackrel{c}{\to} B G \stackrel{k}{\to} B^n A$ represents a class $[k(c)] \in H^n(X,A)$. This is the corresponding characteristic class of the bundle.

Notable families of examples include:

* for $G = O$ the [[orthogonal group]]: 

  [[Pontryagin classes]], [[Stiefel-Whitney classes]], [[Wu classes]];

  [[one-loop anomaly polynomial I8]]

* for $G = SO$ the [[special orthogonal group]]: 

  [[Euler classes]];


* for $G = U$ the [[unitary group]]: 

  [[Chern classes]], [[Conner-Floyd Chern classes]];

  [[Todd class]];

  

* for $G = \mathbf{B}U(1)$ the [[circle n-group|circle 2-group]]: 

  the [[Dixmier-Douady class]].


### Of line bundles

* [[canonical characteristic class]], [[Theta characteristic]]

### Of linear representations

* [[characteristic class of a linear representation]]

### Chern character

The [[Chern character]] is a natural characteristic class with values in real cohomology. See there for more details.

### $k$-Invariants

* [[k-invariants]]

### Level in $\infty$-Chern-Simons theory

* [[level (Chern-Simons theory)]]


### Of Lagrangian submanifolds

A characteristic class of [[Lagrangian submanifolds]] is the _[[Maslov index]]_.

### Classes in the sense of Fuks

In ([Fuks (1987), section 7](#Fuks)) an axiomatization of characteristic classes is proposed. We review the definition and discuss how it is a special case of the one given above.

#### Fuks's definition

Fuks considers a base category $\mathcal{T}$ of "spaces" and a category $\mathcal{S}$ of spaces with a structure (for example, space together with a [[vector bundle]] on it), this category should be a category over $\mathcal{T}$, i.e. at least equipped with a [[functor]] $U : \mathcal{S}\to\mathcal{T}$. 

A morphism of categories with structures is a morphism in the [[overcategory]] [[Cat]]$/\mathcal{T}$, i.e. a morphism $U\to U'$ is a functor $F: dom(U)\to dom(U')$ such that $U' F = U$. 

Suppose now the category $\mathcal{T}$ is equipped with a [[cohomology theory]] which is, for purposes of this definition, a functor of the form $H : \mathcal{T}^{op} \to A$ where $A$ is some [[concrete category]], typically category of [[algebra over an algebraic theory|T-algebras]] for some [[algebraic theory]] in [[Set]], e.g. the category of [[abelian group]]s. Define 
$\mathcal{H} = \mathcal{H}_H$ as a category whose objects are pairs $(X,a)$ where $X$ is a space (= object in $\mathcal{T}$) and $a\in H(X)$. This makes sense as $A$ is a [[concrete category]]. A morphism $(X,a)\to (Y,b)$ is a morphism $f: X\to Y$ such that $H(f)(b) = a$. We also denote $f^* = H(f)$, hence $f^*(b) = a$. 

A __characteristic class of structures of type $\mathcal{S}$ with values in__ $H$ in the sense of ([Fuks](#Fuks)) is a morphism of structures $h: \mathcal{S}\to\mathcal{H}_H$ over $\mathcal{T}$. In other words, to each structure $S$ of the type $\mathcal{S}$ over a space $X$ in $\mathcal{T}$ it assigns an element $h(S)$ in $H(X)$ such that for a morphism $t: S\to T$ in $\mathcal{S}$ the homomorphism $(U(t))^* : H(Y)\to H(X)$, where $Y = U(T)$, sends $h(S)$ to $h(T)$. 

#### Discussion

Notice that $\mathcal{H}_H \to \mathcal{T}$ in the above is nothing but the [[fibered category]] that under the [[Grothendieck construction]] is an equivalent incarnation of the [[presheaf]] $H$. In fact, since $A$ in the above is assume to be just a 1-category of sets with structure, $\mathcal{H}_H$ is just its [[category of elements]] of $H$.

Similarly in all applications that arise in practice (for instance for the structure of [[vector bundle]]s) that was mentioned, the functor $\mathcal{S} \to \mathcal{T}$ is a [[fibered category]], too, corresponding under the inverse of the [[Grothendieck construction]] to a [[prestack]] $F_{\mathcal{S}}$. 

Therefore morphisms of fibered categories over $\mathcal{T}$

$$
  c : \mathcal{S} \to \mathcal{H}_H
$$

are equivalently morphisms of [[prestack|(pre)]][[stack]]s

$$
  c : F_{\mathcal{S}} \to H
  \,.
$$

In either picture, these are morphism in a [[2-topos]] over the [[site]] $\mathcal{T}$.

So, as before, for $X \in \mathcal{T}$ some [[space]], a $\mathcal{S}$-structure on $X$ (for instance a [[vector bundle]]) is a moprhism in the topos

$$
  g : X \to F_{\mathcal{S}}
$$

(in this setup simply by the [[2-Yoneda lemma]]) and the characteristic class $[c(g)]$ of that bundle is the bullback of that [[universal characteristic class|universal class]] $c$, hence the class represented by the composite

$$
  c(g) : X \stackrel{g}{\to} F_{\mathcal{S}} \stackrel{c}{\to} H
  \,.
$$


## Related concepts

* [[characteristic differential form]]

* [[universal characteristic class]], [[universal characteristic map]];

* [[differential characteristic class]]


* [[characteristic class of a linear representation]]


## References

Textbook accounts include


* [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* {#Kochmann96} [[Stanley Kochmann]], section 2.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Dale Husemoeller]], [[Michael Joachim]], [[Branislav Jurco]], [[Martin Schottenloher]], _[[Basic Bundle Theory and K-Cohomology Invariants]]_, 
Lecture Notes in Physics, Springer 2008 ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726corr1.pdf))

* [[Peter May]], chapter 23 of _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

With an eye towards application in [[mathematical physics]]:

* {#Zhang11} [[Yang Zhang]], _A brief introduction to characteristic classes from the differentiable viewpoint_, 2011 ([pdf](http://staff.ustc.edu.cn/~yzhphy/notes/A%20brief%20introduction%20to%20characteristic%20classes%20from%20the%20differentiable%20viewpoint.pdf))


* [[Mikio Nakahara]], Chapter 11 of: _[[Geometry, Topology and Physics]]_, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


Further texts include

* Jean-Pierre Schneiders, _Introduction to characteristic classes and  index theory_ (book), Lisboa (Lisbon) 2000

* [[Johan Dupont]], _Fibre bundles and Chern-Weil theory_, Lecture Notes Series __69__, Dept. of Math., University of Aarhus, 2003, 115 pp. [pdf](http://data.imf.au.dk/publications/ln/2003/imf-ln-2003-69.pdf)

* Shigeyuki Morita, _Geometry of characteristic classes_, Transl. Math. Mon. __199__, AMS 2001

* [[Raoul Bott]], L. W. Tu, _Differential forms in algebraic topology_, GTM __82__, Springer 1982.


* D. B. Fuks, _&#1053;&#1077;&#1087;&#1088;&#1077;&#1088;&#1080;&#1074;&#1085;&#1099;&#1077; &#1082;&#1086;&#1075;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080; &#1090;&#1086;&#1087;&#1086;&#1083;&#1086;&#1075;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1093; &#1075;&#1088;&#1091;&#1087;&#1087; &#1080; &#1093;&#1072;&#1088;&#1072;&#1082;&#1090;&#1077;&#1088;&#1080;&#1089;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1077; &#1082;&#1083;&#1072;&#1089;&#1089;&#1099;_ , appendix to the Russian translation of K. S. Brown, _Cohomology of groups_, Moskva, Mir 1987.
 {#Fuks}

[[!redirects characteristic class]]
[[!redirects characteristic classes]]
