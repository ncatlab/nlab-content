+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Quite generally, _automorphic forms_ are suitably well-behaved [[functions]] on a [[quotient]] space $K\backslash X$ where $K$ is typically a [[discrete group]], hence suitable functions on $X$ which are [[invariant]] under the [[action]] of a discrete group. The precise definition has evolved a good bit through time.

[[Henri Poincaré]] considered [[analytic functions]] invariant under a discrete infinite group of [[fractional linear transformations]] and called them _[[Fuchsian functions]]_ (after his advisor [[Lazarus Fuchs]]). 

More generally, automorphic forms in the modern sense are suitable functions on a [[coset space]] $K \backslash G$, hence functions on [[groups]] $G$ which are [[invariant]] with respect to the [[action]] of the [[subgroup]] $K \hookrightarrow G$. The archetypical example here are [[modular forms]] regarded as functions on $K\backslash PSL(2,\mathbb{R})$ where $K$ is a [[congruence subgroup]], and for some time the terms "modular form" and "automorphic form" were used essentially synonymously, see [below](#ModularForms). Based on the fact that a [[modular form]] is a [[section]] of some [[line bundle]] on the [[moduli stack of elliptic curves]], [[Pierre Deligne]] defined an automorphic form to be a section of a line bundle on a [[Shimura variety]].

By pullback of functions the linear space of such functions hence constitutes a [[representation]] of $G$ and such representations are then called _automorphic representations_ (e.g. [Martin 13, p. 9](#Martin13)) , specifically so if $G = GL_n(\mathbb{A}_K)$ is the [[general linear group]] with [[coefficients]] in a [[ring of adeles]] of some [[global field]] and $K = GL_n(K)$. This is the subject of the _[[Langlands program]]_. There one also considers [[unramified]] such representations, which are constituted by functions that in addition are invariant under the action of $GL_n$ with coefficients in the [[integral adeles]], see [below](#InNumberTheory). 



### Modular forms as classical automorphic forms on $PSL(2,\mathbb{R})$
 {#ModularForms}

By a standard definition, a _[[modular form]]_ is a [[holomorphic function]] on the [[upper half plane]] $\mathfrak{H}$ satisfying a specified transformation property under the [[action]] of a given [[congruence subgroup]] $\Gamma$ of the [[modular group]] $G = PSL(2,\mathbb{Z})$ (e.g. [Martin 13, definition 1](#Martin13), [Litt, def. 1](#Litt)).

But the [[upper half plane]] is itself the [[coset]] of the [[projective linear group]] $G = PSL(\mathbb{R})$ by the subgroup $K = Stab_G(\{i\}) \simeq SO(2)/\{\pm I\}$

$$
  f\colon \mathfrak{H} \simeq PSL(2,\mathbb{R})/K
  \,.
$$

In view of this, one finds that every modular function $f \colon \mathfrak{H} \to \mathbb{C}$ lifts to a function 

$$
  \tilde f \colon \Gamma\backslash PSL(2,\mathbb{R})
  \longrightarrow \mathbb{C}
  \,,
$$

hence to a function on $G$ which is actually _invariant_ with respect to the $\Gamma$-action ("automorphy"), but which instead now satisfies some transformation property with respect to the action of $K$, as well as some well-behavedness property

This $\tilde f$ is the incarnation as an _automorphic function_ of the modular function $f$ (e.g. [Martin 13, around def. 3](#Martin13), [Litt, section 2](#Litt)). For emphasis these automorphic forms on $PSL(2,\mathbb{R})$ equivalent to modular forms are called _classical modular forms_.

This is where the concept of automorphic forms originates (for more on the history see e.g. [this MO comment](http://mathoverflow.net/a/124785/381) for the history of terminology) [and this one](http://mathoverflow.net/a/21556/381).



### Modular forms as adelic automorphic forms on $GL(2,\mathbb{A})$
 {#ModularFormsAdAdelicAutomorphicForms}

Where by the [above](#ModularForms) an ordinary [[modular form]] is equivalently a suitably periodic function on $SL(2,\mathbb{R})$, one may observe that the [[real numbers]] $\mathbb{R}$ appearing as [[coefficients]] in the latter are but one of many [[p-adic number]] completions of the [[rational numbers]]. Hence it is natural to consider suitably periodic functions on $SL(2,\mathbb{Q}_p)$ of all these completions at once. This means to consider functions on $SL(2,\mathbb{A})$, for $\mathbb{A}$ the [[ring of adeles]]. These are the _adelic automorphic forms_. They may be thought of as subsuming ordinary modular forms for all [[level structures]]. 
(e.g. [Martin 13, p. 8](#Martin13), also [Goldfeld-Hundley 11, lemma 5.5.10](#GoldfeldHundley11), [Bump, section 3.6](#Bump), [Gelbhart 84, p. 22](#Gelbhart84)): we have

$$
  \Gamma \backslash PSL(2,\mathbb{R})
  \simeq
  Z(\mathbb{A}) GL_2(\mathbb{Q})\backslash GL_2(\mathbb{A})/ GL_2(\mathbb{A}_{\mathbb{Z}})
  \,,
$$

where $\mathbb{A}_{\mathbb{Z}}$ are the [[integral adeles]]. (The [[double coset]] on the right is analogous to that which appears in the [[Weil uniformization theorem]], see the discussion there and at _[[geometric Langlands correspondence]]_ for more on this analogy.)

This leads to the more general concept of _adelic automorphic forms_ [below](#InNumberTheory).

### General adelic automorphic forms
 {#InNumberTheory}


More generally, for the [[general linear group]] $G = GL_n(\mathbb{A}_F)$, for any $n$ and with [[coefficients]] in a [[ring of adeles]] $\mathbb{A}_F$ of some [[number field]] $F$, and for the subgroup $GL_n(F)$, then sufficiently well-behaved functions on $GL_n(F)\backslash GL_n(\mathbb{A}_F)$ form [[representations]] of $GL_n(\mathbb{A}_{F})$ which are called _[[automorphic representations]]_. Here "well-behaved" typically means

1. **finiteness** -- the functions [[invariant]] under the [[action]] of the [[maximal compact subgroup]] [[span]] a [[finite number|finite]] [[dimension|dimensional]] [[vector space]];

1. **central character** -- the action by the [[center of a group|center]] is is controled by (...something...);

1. **growth** -- the functions are [[bounded functions]];

1. **cuspidality** -- (...)

(e.g. [Frenkel 05, section 1.6](#Frenkel05), [Loeffler 11, page 4](#Loeffler11), [Martin 13, definition 4](#Martin13), [Litt, def.4](#Litt)).

(These conditions are not entirely set in stone, they are being varied according to application (see e.g. [this MO comment](http://mathoverflow.net/a/66598/381))).

In particular one considers subspaces of "[[unramified]]" such functions, namely those which are in addition trivial on the subgroup of $GL_n$ of the [[integral adeles]] $\mathcal{O}_F$ ([Goldfeld-Hundley 11, def. 2.1.12](#GoldfeldHundley11)). This means that that unramified automorphic representations are spaces of functions on a [[double 

coset]] of the form

$$
  GL_n(F)\backslash GL_n(\mathbb{A}_F) / GL_n(\mathcal{O}_F)
  \,.
$$

See at _[[Langlands correspondence]]_ for more on this. Such double cosets are [[analogy|analogous]] to those appearing in the [[Weil uniformization theorem]] in [[complex analytic geometry]], an analogy which leads to the conjecture of the [[geometric Langlands correspondence]].


### Dirichlet characters

For the special case of $n = 1$ in the discussion of adelic automorphic forms [above](#InNumberTheory), the group 

$$
  GL_1(\mathbb{A}_F) = (\mathbb{A}_F)^\times = \mathbb{I}_F
$$ 

is the [[group of ideles]] and the quotient 

$$
  GL_1(F) \backslash GL_1(\mathbb{A}_F)
  = 
  F^\times \backslash (\mathbb{A}_F)^\times
$$

is the [[idele class group]]. Automorphic forms in this case are effectively [[Dirichlet characters]] in disguise... ([Goldfeld-Hundley 11, theorem 2.1.9](#GoldfeldHundley11)).




## Properties

### Function field analogy

[[!include function field analogy -- table]]

### Application in string theory

In [[string theory]] [[partition functions]] tend to be automorphic forms for [[U-duality]] groups. See the [references below](#ReferencesInStringTheory)

## Related entries

* [[modular form]], [[topological modular form]], [[topological automorphic form]]

* [[automorphic L-function]]

* [[Langlands duality]]



## References

### General

Introductions and surveys include

* {#Deligne} [[Pierre Deligne]], _Fromed Modulaires et representations de $GL(2)$_ ([](http://publications.ias.edu/sites/default/files/Number21.pdf))
 
* {#Gelbhart84} [[Stephen Gelbart]], starting on p. 20 (196) of _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219 ([web](http://www.ams.org/journals/bull/1984-10-02/S0273-0979-1984-15237-6/))

* Nolan Wallach, _Introductory lectures on automorphic forms_ ([pdf](http://math.ucsd.edu/~nwallach/luminy-port2.pdf))
[[!redirects automorphic forms]]

* E. Kowalski, section 3 of  _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))

* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))

* {#Bump} Daniel Bump, _Automorphic forms and representations_

* {#Loeffler11} David Loeffler, _Computing with algebraic automorphic forms_, 2011 ([[LoefflerAutomorphic.pdf:file]])

* {#Martin13} [[Kimball Martin]], _A brief overview of modular and automorphic forms_,2013 [pdf](http://www2.math.ou.edu/~kmartin/papers/mfs.pdf)

* {#Litt} [[Daniel Litt]], _Automorphic forms notes, part I_ ([pdf](http://math.stanford.edu/~dlitt/Talks/automorphicformspt1.pdf))


* Denis Trotabas, Modular Forms and Automorphic Representations (2010) ([pdf](http://math.stanford.edu/~conrad/modseminar/pdf/L10.pdf))

* Werner Muller, Spectral theory of automorphic forms (2010) ([pdf](http://www.math.uni-bonn.de/people/mueller/skripte/specauto.pdf))

* {#Miyake76} Toshitsune Miyake's _Modular Forms_ 1976 (English version 1989) ([review pdf](projecteuclid.org/euclid.bams/1183556263))


Review in the context of the [[geometric Langlands correspondence]] is in

* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))



The generalization of theta functions to [[automorphic forms]] is due to 

* [[André Weil]], _Sur certaines groups d'operateur unitaires_, Acta. Math.  111 (1964), 143-211

see [Gelbhart 84, page 35 (211)](Langlands+program#Gelbhart84) for review.

Further developments here include

* {#Kudla77} [[Stephen Kudla]], _Relations between automorphic forms produced by theta-functions_, in _Modular Functions of One Variable VI_, Lecture Notes in Math. 627, Springer, 1977, 277&#8211;285.

* {#Kudla78} [[Stephen Kudla]], _Theta functions and Hilbert modular forms_,Nagoya Math. J. 69 (1978) 97-106


* {#Stopple95} [[Jeffrey Stopple]], _Theta and $L$-function splittings_, Acta Arithmetica LXXII.2 (1995) ([pdf](http://matwbn.icm.edu.pl/ksiazki/aa/aa72/aa7221.pdf))



### In string theory
  {#ReferencesInStringTheory}

The relation between [[string theory]] on [[Riemann surfaces]] and automorphic forms was first highlighted in

* {#Witten88} [[Edward Witten]], _Quantum field theory, Grassmannians, and algebraic curves_, Comm. Math. Phys. Volume 113, Number 4 (1988), 529-700 ([Euclid](http://projecteuclid.org/euclid.cmp/1104160350))

See also

* {#GRV10} [[Michael Green]], Jorge G. Russo, Pierre Vanhove, _Automorphic properties of low energy string amplitudes in various dimensions_ ([arXiv:1001.2535](http://arxiv.org/abs/1001.2535))


[[!redirects automorphic forms]]

[[!redirects automorphic representation]]
[[!redirects automorphic representations]]

[[!redirects Fuchsian function]]
[[!redirects Fuchsian functions]]