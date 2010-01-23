<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


> under construction

#Contents#
* automatic table of contents goes here
{:toc}
 
## Idea

Hochschild homology and cohomology are characteristic objects associated to  a [[bimodule]] $N$ over a [[monoid]] $A$, in a context where $A$ is really to be thought of as a [[algebra in an (infinity,1)-category|monoid in an monoidal (∞,1)-category]].

If the [[monoid]] in  question plays the role of an _algebra of functions_ on a [[space]] $X$, $A = C(X)$,
then this has geometric interpretations. Notably
  
* the _Hochschild homology_ of $A$ regarded as a bimodule over itself 
  tends to be like the algebra of 
  [[Kähler differential]]s $\Omega^\bullet_K(A)$ on $A$, and hence is something like the algebra of [[differential form]]s on $X$;
    
* the _Hochschild cohomology_ of $A$ regarded as a bimodule over itself
  tends to be like the algebra of [[derivation]]s $Der(A)$ of $A$, 
  and hence something like the [[vector field]]s on $X$.

The seminal [[Hochschild-Kostant-Rosenberg theorem]] states that under suitable conditions on $A$, these statements become exactly true.    
 
Notice that differential forms are objects in [[de Rham cohomology]] but 
are still computed by the Hochschild _homology_ of $A$. 
The terminology reflects the dualization in passing from the [[space]] $X$ to the algebra of functions $A = C(X)$ on it:
it is the Hochschild _homology_ of algebra objects that relates to the
_[[cohomology]]_ of [[space]]s.

Below in section 

* [The nPOV on Hochschild cohomology](#nPOV)

we discuss a conceptual interpretation of Hochschild homology,
that will explain _why_ this is true, and what Hochschild
homology is conceptually, from the [[nPOV]] on [[cohomology]], as 
described there.

Complementary to that, in the section 

* [More traditional description of Hochschild cohomology](#TraditionalIdeas)

we describe the original definition of Hochschild cohomology and 
the evolution of its understanding approaching the [[nPOV]].

Finally in the section titled [Details](#Details) the technical details
are spelled out.
 
 
### More traditional descriptions of Hochschild cohomology {#TraditionalIdeas}
 
Originally the notion of Hochschild cohomology was introduced as the 
[[cochain cohomology]] of a certain [[cochain complex]] associated to any [[bimodule]] $N$ over some [[algebra]] $A$: its [[bar complex]], written 
 
$$
  C_\bullet(N,A) := N \otimes_{A \otimes A^{op}} \mathrm{B}_\bullet A
  \,,
$$
  
where $N$ and $A$ are regarded as $A \otimes A^{op}$-bimodules in the obvious way.

Then it was understood that this complex is the result of tensoring the $A$-bimodules $N$ with $A$ over $A \otimes A^{op}$ but using the [[derived functor]] of the [[tensor product]] functor --  the [[Tor functor]] -- in the ambient [[model structure on chain complexes]]:
 
$$
   C_\bullet(N,A) = N \otimes^D_{A\otimes A^{op}} A = Tor^\bullet_{A\otimes A^{op}}(N,A)
   \,.
$$  
 
Then still a little later, it was understood that this is just the ordinary tensor product in the [[symmetric monoidal (infinity,1)-category]] of chain complexes. If this
is understood, we can just write again simply 
$$
  C_\bullet(M,A) := N \otimes_{A \otimes A^{op}} A
  \,.
$$

This, generally, is the definition of the Hochschild cohomology object
of any bimodule over an [[monoid in a monoidal (∞,1)-category]]. Of special interest is the case where $N = A$. In this case this object is also called the ("$(\infty,1)$-" or "derived-")**center** of $A$:
  
$$
  Z(A) := A \otimes_{A \otimes A^{op}} A
$$
 
In parallel to this formal understanding of Hochschild cohomology, its
conceptual meaning has been better understood: from staring at the explicit description of $C_\bullet(N,A)$ one sees that it has something to do with [[loop space object]]s: a chain in $C_n(N,A)$ is usefully thought of as  a circle with $n$ marked points. One of these points is labeled $N$, the  other are labeled $A$. The [[differential]] on $C_\bullet(N,A)$ acts by taking tensor products over $A$ separately of all neighbour pairs of
bimodules sitting on this circle, and taking the alternating sum of this
as a collection of such circles with $(n-1)$ marked points.
 
A fully geometric understanding of these was given by Ben-Zvi/Nadler/Francis in their work on [[geometric ∞-function theory]]. This we unify now with our [[nPOV]]-perspective on [[cohomology]] in order to give the following [[nPOV]]-perspective on Hochschild cohomology, proper. 
 
### The $n$POV on Hochschild cohomology {#nPOV}

Let $\mathbf{H}$ be an [[(infinity,1)-topos]] of [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathbf{K}$ the $(\infty,2)$-topos of $(\infty,2)$-sheaves on a [[site]] $C$, such that the [[quasicoherent ∞-stack]]

$$
  C : C^{op} \to (\infty,1)Cat
$$

$$
  U \maptso Stab(C_{/U})
$$ 

as described at [[schreiber:∞-vector bundle]]
does indeed satisfy [[descent]] in that it is indeed an object 
in $\mathbf{K}$.

Recall that for $X \in \mathbf{H} \subset \mathbf{K}$ any object, its [[free loop space object]] $\mathcal{L} X$ is the $(\infty,1)$-[[pullback]]

$$
  \array{
     && \mathcal{L} X
     \\
     & \swarrow && \searrow
     \\
     X &&&& X
     \\
     & {}_{\mathllap{(Id,Id)}}\searrow && \swarrow_{\mathrlap{(Id,Id)}}
     \\
     && X \times X
  }
  \,.
$$

Notice that this is usefully thought of as the [[span trace]] of the 
[[identity]] [[span]]

$$
  \mathcal{L} X 
  = 
  Tr
  \left(
    \array{
      && X
      \\
      & {}^{\mathllap{Id}}\swarrow && \searrow^{\mathrlap{Id}}
      \\
      X &&&& X
    }
  \right)
  \,.
$$

Assume that $X$ is such that on it $C$ satisfies the axioms
of [[geometric function theory]] (see [[geometric ∞-function theory]] for more details).

Then:

The **Hochschild cohomology of $X$** is the [[cohomology]] of 
the [[free loop space object]] $\mathcal{L}X$
with coefficients in $C$:

$$
  HH(X) = \mathbf{K}(\mathcal{L}X, C) =: C(\mathcal{L}X)
  \,.
$$

$$
  HH^n(X) := HH_n(C(X)) := \pi_0\Omega^n\mathbf{H}(\mathcal{L}X, C)
  \,.
$$

By the assumption that $C(-)$ is a 
[[geometric function theory|geometric function object]] on $X$ we can rewrite 

$$
  HH(X) = \mathbf{H}(\mathcal{L}X,C) =: C(\mathcal{K}X)
$$

as 

$$
  \cdots \simeq C(X) \otimes_{C(X)\otimes C(X)^{op}}
   \infty Mod(X)
  \,.
$$

This is hence indeed the Hochschild homology object $HH_\bullet(A) = A \otimes_{A \otimes A^{op}}$ 
of the algebra object $A = \infty Mod(X)$, regarded  as a bimodule over itself.

More generally, let $f : Y \to X$ be a morphism in $\mathbf{H}$ and 
consider the [[span trace]] 

$$
  \mathcal{L}_X Y :=
  Tr
  \left(
    \array{
      && Y
      \\
      & {}^{\mathllap{f}}\swarrow && \searrow^{\mathrlap{f}}
      \\
      X &&&& X
    }
  \right)
$$

which is the $(\infty,1)$-[[pullback]]

$$
  \array{
    && \mathcal{L}_X Y
    \\
    & \swarrow && \searrow
    \\
    Y &&&& X
    \\
    & {}_{\mathllap{f,f}}\searrow && \swarrow_{\mathrlap{Id,Id}}
    \\
    && X \times X
  }
  \,.
$$

Then we take the Hochschild cohomology of $Y$ relative to $f : Y \to X$
to be 

$$
  HH(Y,X) := \mathbf{K}(\mathcal{L}_X Y, C) =: \infty Mod(\mathcal{L}_X Y)
  \,.
$$

In the case that $f$ is such that $C(-) = \mathbf{K}(-,C)$ satisfies 
[[geometric function theory]]
on it, this is

$$
  \cdots = C( Y \times_{X \times X} Y)
  \simeq
  C(Y) \otimes_{C(X) \otimes C(X)^{op}} C(X)
  \,.
$$

This is indeed the Hochschild homology object of the $C(X)$-bimodule
object structure on $C(Y)$ induced from $f^*$:

$$
  \cdots =: HH_\bullet(C(Y), C(X))
  \,.
$$


## Details {#Details}

...

### The bar complex


> The bar complex is called the bar complex because its inventors wrote it down using lots of bars. If you don't believe this it shows that you have no idea how careless mathematicians can be about finding good terminology for the objects they hold in high esteem.





 
## References
 
The traditional story of Hochschild (co)homology is discussed for instance
in chapter 4 of
 
* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603))
 
The $(\infty,1)$-categorical picture with its relation to 
[[geometric infinity-function theory]] is discussed in
 
* [[David Ben-Zvi]], [[John Francis]], [[David Nadler]], 
  _[[geometric infinity-function theory|Integral transforms and Drinfeld centers in derived algebraic geometry]]_ ([arXiv:0805.0157])
 
 
---
## Hochschild cohomology

[MathSciNet](http://www.ams.org/mathscinet/search/publications.html?pg4=AUCN&s4=&co4=AND&pg5=TI&s5=&co5=AND&pg6=PC&s6=&co6=AND&pg7=ALLF&s7=%22Hochschild+cohomology%22&co7=AND&Submit=Search&dr=all&yrop=eq&arg3=&yearRangeFirst=&yearRangeSecond=&pg8=ET&s8=All)

[Google Scholar](http://scholar.google.co.uk/scholar?q=%22Hochschild+cohomology%22&hl=en&lr=&btnG=Search)

[Google](http://www.google.com/search?hl=en&q=%22Hochschild+cohomology%22&btnG=Search)

[arXiv: Experimental full text search](http://search.arxiv.org:8081/?query=%22Hochschild+cohomology%22&in=)

[arXiv: Abstract search](http://front.math.ucdavis.edu/search?a=&t=&q=%22Hochschild+cohomology%22&c=&n=25&s=Abstracts)

category: Search results
---
## Hochschild cohomology

NCG (Algebra and noncommutative geometry)

category: World [private]
---
## Hochschild cohomology

This can be regarded as an instance of [[Monad cohomology]].

For Hochschild cohomology of Segal cats and model cats, see Toen: Homotopical and higher categorical structures in algebraic geometry. File Toen web unpubl hab.pdf. Idea: Hochschild cohom should be the space of endomorphisms of an identity functor.

For Hochschild cohom of DG-categories, see Toen: Lecture on DG-categories. File Toen web unpubl swisk.pdf. Treats basic theory, localization, relation to model cats, functorial cones, K-theory and Hochschild cohomology, and descent problems.

category: Definition
---
## Hochschild cohomology

Short exposition of Hochschild cohomology (for associative algebras) in Ch 11 of Pierce (el), under Algebras.

For cohomology of algebras, see Cartan-Eilenberg, and maybe MacLane: Homology.

Course notes from Grojnowski's lectures in Cambridge.

category: Paper References
---
## Hochschild cohomology

Brief intro in Caldararu's notes on Derived categories of sheaves, in Homol alg folder or on arXiv.

Schuhmacher: Hochschild cohomology of complex spaces and noetherian schemes, HHA vol 6

Yekutieli: The continuous Hochschild cochain complex of a scheme, Can J Math Vol 54 (6).

category: Online References
---
## Hochschild cohomology

<http://www.math.uiuc.edu/K-theory/0190>

[arXiv:1102.5756](http://front.math.ucdavis.edu/1102.5756) Cohomology of exact categories and (non-)additive sheaves
from arXiv Front: math.KT by Dmitry Kaledin, Wendy Lowen
We use (non-)additive sheaves to introduce an (absolute) notion of Hochschild
cohomology for exact categories as Ext's in a suitable bisheaf category. We
compare our approach to various definitions present in the literature.

Various things by Toen on Hochschild stuff in abstract settings.

[arXiv:1001.5379](http://front.math.ucdavis.edu/1001.5379) The homology of digraphs as a generalisation of Hochschild homology
from arXiv Front: math.KT by Paul Turner, Emmanuel Wagner
J. Przytycki has established a connection between the Hochschild homology of
an algebra $A$ and the chromatic graph homology of a polygon graph with
coefficients in $A$. In general the chromatic graph homology is not defined in
the case where the coefficient ring is a non-commutative algebra. In this paper
we define a new homology theory for directed graphs which takes coefficients in
an arbitrary $A-A$ bimodule, for $A$ possibly non-commutative, which on
polygons agrees with Hochschild homology through a range of dimensions.

Toen: Algebres simplicicales etc, file Toen web prepr rhamloop.pdf. Comparison between functions on derived loop spaces and de Rham theory. Take a smooth k-algebra, k aof char zero. Then (roughly) the de Rham algebra of A and the simplical algebra $S^1 \otimes A$ determine each other (functorial equivalence). Consequence: For a smooth k-scheme $X$, the algebraic de Rham cohomology is identified with $S^1$-equivariant functions on the derived loop space of $X$. Conjecturally this should follow from a more general comparison between functions on the derived loop space and cyclic homology. Also functorial and multiplicative versions of HKR type thms on decompositions of Hochschild cohomology, for any separated k-scheme.

Title: Operads of natural operations I: Lattice paths, braces and Hochschild
 cochains.
Authors: Michael Batanin, Clemens Berger and Martin Markl.
In this first paper of a series we study various operads of natural
operations on Hochschild cochains and relationships between them.
<http://arxiv.org/abs/0906.4097>

category: Some Research Articles
---
## Hochschild cohomology

<http://mathoverflow.net/questions/28472/book-on-hochschild-cohomology>

<http://mathoverflow.net/questions/33877/hochschild-cohomology-of-a-and-of-mod-a>

<http://mathoverflow.net/questions/11081/hochschild-cohomology-of-fukaya-categories-and-quantum-cohomology>

<http://mathoverflow.net/questions/108463/when-do-hochschild-homology-and-cohomology-agree-ambidexterity>

category: Other Information

nLab page on [[nlab:Hochschild cohomology]]
