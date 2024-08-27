
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A _super-group_ is the analog in [[supergeometry]] of [[Lie groups]] in [[differential geometry]].

## Definition

### Algebraic super groups

An [[affine scheme|affine]] algebraic super group is the [[formal dual]]  of a [[superalgebra|super]]-[[commutative Hopf algebra]].


### Super Lie groups

A _super Lie group_ is a [[group object]] in the [[category]] [[SDiff]] of [[supermanifolds]], that is a super [[Lie group]].


One useful way to characterize [[group objects]] $G$ in the
[[category]] $SDiff$ of [[supermanifold]] is by first sending 
$G$ with the [[Yoneda embedding]] to a [[presheaf]] on $SDiff$
and then imposing a lift of $Y(G) : SDiff^{op} \to Set$
through the [[forgetful functor]] [[Grp]] $\to$ [[Set]]
that sends a (ordinary) [[group]] to its underlying [[set]].

So a group object structure on $G$ is a diagram

$$
  \array{
    && Grp
    \\
    & {}^{(G,\cdot)}\nearrow & \downarrow
    \\
    SDiff^{op} &\stackrel{Y(G)}{\to}& Set
  }
  \,.
$$

This gives for each [[supermanifold]] $S$ an ordinary group 
$(G(S), \cdot)$, so in particular a product operation

$$
  \cdot_S : G(S) \times G(S) \to G(S)
  \,.
$$

Moreover, since morphisms in $Grp$ are group homomorphisms, it follows
that for every morphism $f : S \to T$ of [[supermanifold]]s we get a 
commuting diagram

$$
  \array{
    G(S) \times G(S) &\stackrel{\cdot_S}{\to}& G(S)
    \\
    \uparrow^{G(f)\times G(f)}  && \uparrow^{G(f)}
    \\
    G(T) \times G(T) &\stackrel{\cdot_T}{\to}& G(T)     
  } 
$$

Taken together this means that there is a morphism

$$
  Y(G \times G)  \to Y(G)
$$

of representable presheaves. By the [[Yoneda lemma]], this uniquely
comes from a morphism $\cdot : G \times G \to G$, which is the 
product of the group structure on the object $G$ that we are after.

etc.  


This way of thinking about supergroups is often explicit in 
some parts of the literature on supergeometry: some authors
define a supergroup or [[super Lie algebra]] as a
rule that assigns to every [[Grassmann algebra]] $A$ 
over an ordinary [[vector space]] an ordinary [[group]]
$G(A)$
or [[Lie algebra]] and to a morphism of [[Grassmann algebra]]s
$A \to B$
_covariantly_ a morphism of groups $G(A) \to G(B)$. 
But the [[Grassmann algebra]] on an $n$-dimensional [[vector space]]
is naturally isomorphic to the function ring on the [[supermanifold]]
$\mathbb{R}^{0|n }$. So the definition of supergroups in terms of 
Grassmann algebras is secretly the same as the above definition
in terms of the [[Yoneda embedding]].




## Examples


### The super-translation group
  {#SuperTranslationGroup}

also called the **[[super-Heisenberg group]]**

The additive group structure on $\mathbb{R}^{1|1}$ is given on [[generalized element]]s in (i.e. in the logic internal to) the [[topos]] of [[sheaf|sheaves]] on the category [[SCartSp]] of [[cartesian space|cartesian]] superspaces by

$$
  \mathbb{R}^{1|1} \times \mathbb{R}^{1|1} \to 
  \mathbb{R}^{1|1}
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

Recall how the notation works here: by the [[Yoneda embedding]] we have a [[full and faithful functor]]

> [[SDiff]] $\hookrightarrow$ $Fun(SDiff^{op}, Set)$

and we also have the theorem, discussed at [[supermanifold]]s, that maps from some $S \in SDiff$ into $\mathbb{R}^{p|q}$ is given by a tuple of $p$ even section $t_i$ and $q$ odd sections $\theta_j$. The above notation specifies the map of supermanifolds by displaying what map of sets of maps from some test object $S$ it corresponds to under the [[Yoneda embedding]].

Now, for each $S \in $ [[SDiff]] there is a [[group]] structure on the [[hom-set]] $SDiff(S, \mathbb{R}^{1|1}) \simeq C^\infty(S)^{ev} \times C^\infty(S)^{odd}$ given by precisely the above formula for this given $S$

$$
  \mathbb{R}^{1|1}(S) \times \mathbb{R}^{1|1}(S) \to 
  \mathbb{R}^{1|1}(S)
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

where $(t_i, \theta_i) \in C^\infty(S)^{ev} \times C^\infty(S)^{odd}$ etc and where the addition and product on the right takes place in the function [[super algebra]] $C^\infty(S)$.

Since the formula looks the same for all $S$, one often just writes it without mentioning $S$ as above.


### The super Euclidean group 

The super-translation group is the $(1|1)$-dimensional case of the [[super Euclidean group]].



[[!include super-Minkowski Lie group -- example]]




### General linear supergroup

[[general linear supergroup]]

...


### Orthosymplectic supergroup

[[orthosymplectic supergroup]]

...

## Finite super-groups

There is a finite analog for super-groups that does not quite fit in the framework presented here:

+-- {: .num_defn}
###### Definition

A finite super-group is a tuple $(G, z \in G)$, where $G$ is a finite group and $z$ is central and squares to $1$.

The representations of a finite super-group are $\mathbb{Z}_2$-graded:
An irreducible representation has odd degree if $z$ acts by negation, and even degree if it acts as the identity.

This definition is found e.g. in:

* Paul Bruillard, Cesar Galindo, Tobias Hagge, Siu-Hung Ng, Julia Yael Plavnik, Eric C. Rowell, Zhenghan Wang, _Fermionic Modular Categories and the 16-fold Way_ ([pdf] (https://arxiv.org/pdf/1603.09294v2))

=--

## Properties

### Representations, Tannaka duality and Deligne's theorem

[[Deligne's theorem on tensor categories]] (see there for details) says that every suitably well-behave linear [[tensor category]] is the [[category of representations]] of an algebraic supergroup. In particular the [[Hopf algebra]] of functions on an affine algebraic supergroup is a [[triangular Hopf algebra]].

[[!include structure on algebras and their module categories - table]]


## References

References mentioning the definition of super Lie groups as [[internal groups]] in  [[supermanifolds]] and mostly also the perspective of [[functorial geometry]]:

* Katsumi Yagi, *Super Lie Groups*, Adv. Stud. Pure Math. Progress in Differential Geometry (1993) 407-412 &lbrack;[euclid:1534359537](https://projecteuclid.org/euclid.aspm/1534359537)&rbrack;

* {#DeligneMorgan99} [[Pierre Deligne]], [[John Morgan]], §2.10 in: _Notes on Supersymmetry (following [[Joseph Bernstein]])_, in: *[[Quantum Fields and Strings]], A course for mathematicians*, **1**, Amer. Math. Soc. Providence (1999) 41-97 &lbrack;[ISBN:978-0-8218-2014-8](https://bookstore.ams.org/qft-1-2-s), [web version](http://www.math.ias.edu/qft), [[DeligneMorgan-NotesOnSusy.pdf:file]]&rbrack;


* {#Varadarajan04} [[Veeravalli Varadarajan]], section 7.1 of: _[[Supersymmetry for mathematicians]]: An introduction_,  Courant Lecture Notes in Mathematics **11**, American Mathematical Society (2004) &lbrack;[doi:10.1090/cln/011](http://dx.doi.org/10.1090/cln/011), <a href="http://dec1.sinp.msu.ru/~panov/LibBooks/SUSY/(Courant_Lecture_Notes_11)V._S._Varadarajan-Supersymmetry_for_Mathematicians__An_Introduction_(Courant_Lecture_Notes)-American_Mathematical_Society(2004).pdf">pdf</a>&rbrack;

* [[Dennis Westra]], _Superrings and supergroups_, PhD thesis (2009) &lbrack;[doi10.25365/thesis.6869](https://doi.org/10.25365/thesis.6869), [pdf](http://www.mat.univie.ac.at/~michor/westra_diss.pdf), [[Westra-Superrings.pdf:file]]&rbrack;

* [[Claudio Carmeli]], Lauren Caston, [[Rita Fioresi]], Section 3.4 in: _Mathematical Foundations of Supersymmetry_, EMS Series of Lectures in Mathematics **15** (2011) &lbrack;[ISBN:978-3-03719-097-5](https://bookstore.ams.org/emsserlec-15/), [arXiv:0710.5742](https://arxiv.org/abs/0710.5742)&rbrack;


Discussion in a context of [[supergravity]]:

* {#CastellaniDAuriaFre} [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fré]], section II.2 of: _[[Supergravity and Superstrings - A Geometric Perspective]]_, World Scientific (1991) &lbrack;[doi:10.1142/0224](https://doi.org/10.1142/0224), toc: [[CDF91-TOC.pdf:file]], chII.2: [[CastellaniDAuriaFre-ChII2.pdf:file]], ch II.3: [[CastellaniDAuriaFre-ChII3.pdf:file]]&rbrack;



Discussion of [[group extensions]] for supergroups:

* {#Drupieski14} [[Christopher Drupieski]], _Strict polynomial superfunctors and universal extension classes for algebraic supergroups_ ([arXiv:1408.5764](http://arxiv.org/abs/1408.5764))

Discussion as Hopf-superalgebras includes

* Nicol&#225;s Andruskiewitsch, Iv&#225;n Angiono, Hiroyuki Yamane, _On pointed Hopf superalgebras_, Contemp. Math. vol. 544, pp. 123--140, 2011 ([arXiv:1009.5148](https://arxiv.org/abs/1009.5148))


[[!redirects supergroups]]

[[!redirects super Lie group]]
[[!redirects super Lie groups]]

[[!redirects super group]]
[[!redirects super groups]]

[[!redirects Lie supergroup]]
[[!redirects Lie supergroups]]

[[!redirects super-group]]
[[!redirects super-groups]]