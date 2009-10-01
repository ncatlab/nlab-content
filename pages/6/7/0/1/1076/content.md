#Idea#

A _triangulated category_ is a [[category]] that behaves like the [[homotopy category of an (infinity,1)-category|homotopy category]] of a [[stable (infinity,1)-category]]. Indeed, most examples of triangulated categories that arise in practice appear this way. 

Therefore, all the structure and properties of a triangulated category is best understood as a 1-categorical shadow of the corresponding properties of [[stable (infinity,1)-category|stable (infinity,1)-categories]], which are in fact simpler and more natural. 

#Definition#

A __triangulated category__ is 

* an [[additive category]];

* [[category with translation|with (additive) translation]];

* equipped with a collection of [[category with translation|triangles]] called __distinguished triangles__ (dts) 

* such that the following axioms hold

**TR0:** every triangle isomorphic to a dt is itself a dt;

**TR1:** the triangle 

$$
  X \stackrel{Id_X}{\to} X \to 0 \to T X
$$ 

is a dt;

**TR2:** for all $f : X \to Y$, there exists a dt 

$$
  X \stackrel{f}{\to} Y \to Z \to TX
  \,;
$$

**TR3:** a triangle 

$$
  X \stackrel{f}{\to} Y \stackrel{g}{\to} Z \stackrel{h}{\to} T X
$$ 

is a dt precisely if 

$$
  Y \stackrel{-g}{\to} Z \stackrel{-h}{\to} T X \stackrel{-F(f)}{\to} T Y
$$ 

is a dt;

**TR4:** given two dts 

$$
  X \stackrel{f}{\to} Y \stackrel{g}{\to} Z \stackrel{h}{\to} T X
$$ 

and 

$$X' \stackrel{f'}{\to} Y' \stackrel{g'}{\to} Z' \stackrel{h'}{\to} T X'$$ 

and given morphisms $\alpha$ and $\beta$ in

$$\array{
  X &\stackrel{f}{\to}& Y
  \\
  \downarrow^\alpha && \downarrow^\beta
  \\
  X' &\stackrel{f'}{\to}& Y'  
}$$

there exists a morphism $\gamma : Z \to Z'$ 
extending this to a morphism of dts in that
the diagram 

$$
  \array{
    X &\stackrel{f}{\to}& Y
    &\stackrel{g}{\to}& Z
    &\stackrel{h}{\to}& T X
    \\
    \downarrow^\alpha && \downarrow^\beta
    && \downarrow^{\exists \gamma}
    && \downarrow^{T(\alpha)}
    \\
    X' &\stackrel{f'}{\to}& Y'
    &\stackrel{g'}{\to}& Z'
    &\stackrel{h'}{\to}& T X'
}
$$

commutes;

**TR5:** given three distinguished triangles of the form

$$
\begin{aligned}
& X \stackrel{f}{\to} Y
    \stackrel{h}{\to} Y/X
    \stackrel{}{\to} T X
\\
& Y \stackrel{g}{\to} Z
    \stackrel{k}{\to} Z/Y
    \stackrel{}{\to} T Y
\\
& X \stackrel{g \circ f}{\to} Z
    \stackrel{l}{\to} Z/X
    \stackrel{}{\to} T X
\end{aligned}
$$ 

there exists a dt

$$
Y/X \stackrel{u}{\to} Z/X
    \stackrel{v}{\to} Z/Y
    \stackrel{w}{\to} T (Y/X)
$$

such that the following big diagram commutes

$$
  \array{
    X 
    &&\stackrel{g \circ f}{\to}&& 
    Z
    &&\stackrel{k}{\to}&& 
    Z/Y
    &&\stackrel{k}{\to}&& 
    T (Y/X)
    \\
    & 
    {}_{f}\searrow
    && 
    \nearrow_{g}
    &&
    \searrow^{l}
    &&
    \nearrow_{v} 
    &&
    \searrow^{}
    &&
    \nearrow_{T(h)}
    \\
    &&
    Y
    &&&&
    Z/X
    &&&&
    T Y
    \\
    &&&
    \searrow^{h}
    &&
    \nearrow_{u}
    &&
    \searrow^{}
    &&
    \nearrow_{T(f)}
    \\
    &&&&
    Y/X
    &&\stackrel{}{\to}&&
    T X
  }
$$

+--{: .query}
[[Mike Shulman|Mike]]: This classical definition is actually redundant; TR4 and one direction of TR3 follow from the remaining axioms.  See J.P. May, _The additivity of traces in triangulated categories_, [pdf](http://www.math.uchicago.edu/~may/PAPERS/AddJan01.pdf).
=--


#Remarks#

* In the context of triangulated categories the translation functor $T : C \to C$ is often called the **suspension functor** and usually denoted $(-)[1] : X \mapsto X[1]$. However unlike "translation functor", suspension functor is also the term used when the invertibility is not assumed, cf. [[suspended category]].

#Examples#

* The [[homotopy category]] of [[chain complexes]] in an [[abelian category]] (the category of chain complexes modulo [[chain homotopy]]) is a triangulated category: the translation functor is the shift functor on [[chain complexes]] and the distinguished triangles are those coming from the [[mapping cone]] construction $X \stackrel{f}{\to}Y \to Cone(f) \to T X$.

* The [[localization]] $C/N$ of any triangulated category $C$ at a [[null system]] $N \hookrightarrow C$, i.e. the localization using the [[calculus of fractions]] given by the morphisms $f : X \to Y$ such that there exists dts $X \to Y \to Z \to T X$ with $Z$ an object of a [[null system]], is still naturally a triangulated category, with the dts being the triangles isomorphic to an image of a dt under $Q : C \to C/N$.

  * In particular, therefore, the [[derived category]] of any [[abelian category]] is a triangulated category, since it is the localization of the homotopy category at the null system of acyclic complexes.

* As mentioned before, the [[homotopy category of an (infinity,1)-category|homotopy category]] of a [[stable (infinity,1)-category]] is a triangulated category.

  * Therefore in particular the [[stable homotopy category]] (the homotopy category of [[spectrum|spectra]]) is a triangulated category.

* Likewise, the homotopy category of a [[stable model category]] is also a triangulated category.

  * This is a more classical route to the triangulated category of [[spectrum|spectra]].

  * It also provides a direct construction of the homotopy category and derived category of many abelian categories.


#Discussion#

The original definition of triangulated categories is apparently due to Verdier who developed the theory upon guidelines by Grothendieck; Dold and Puppe developed independently a version without octahedron axiom with motivation in algebraic topology. Grothendieck in the manuscript [[Pursuing Stacks]] mentions that the usual definition of triangulated categories and the corresponding [[derived category|derived categories]]  seemed to be inadequate for some of the developments that he wished for.  He also says something to the effect that he had tried to interest various of his ex-students in doing a thorough treatment of the ideas, which he considered to be necessary for future development and which he then proceeds  to sketch out. That was the theory of [[derivateur|dérivateurs]].  

+--{+ .query}
[[Zoran Skoda]]: I am not quite sure if this is entirely correct. Grothendieck indeed wanted more flexibility in homotopical algebra and went to develop these things; but if one talks
only very specifically about the concept of triangulated category itself (not wider context) than the main complaint of everybody was about the crudeness of localization at quasiisomorphisms; the thing which for example Drinfel'd's "quotients of dg-categories" paper successfully rectifies (and then again Lyubashenko in quotients of $A_\infty$-categories).
=--

The idea of 'd&#233;rivateurs' is that in addition to looking at a basic category of 'things' such as chain complexes, you should also look at all categories of diagrams of such things, and the derived / homotopy Kan extensions between the corresponding derived categories that correspond to a change of the indexing category.

The basic idea behind this was explored slightly later by Alex Heller (1988). His memoir discusses the corresponding homotopy theory and links it to earlier work of Doug Anderson. 

#References#

Accounts can be found for instance in

* A. Neeman, 2001, Triangulated Categories , Princeton University Press Press,

or section 10 of

* Kashiwara-Schapira, [[Categories and Sheaves]];

or section 3 of 

* J. Lurie, [[Stable Infinity-Categories]]

or

* B. Noohi, _Lectures on derived and triangulated categories_ ([arXiv](http://arxiv.org/abs/0704.1009))

A link for discussion and a list of source material for  'd&#233;rivateurs' can be found at

* A. Grothendieck,  [Les D&#233;rivateurs](http://people.math.jussieu.fr/~maltsin/groth/Derivateurs.html)

This includes copies of the first thirteen chapters of a 2000 page manuscript of Grothendieck. 

[[Georges Maltsiniotis]] has written an introduction to the topic (in French) which is listed near the bottom of the webpage: (G. Maltsiniotis , "Introduction &#224; la th&#233;orie des d&#233;rivateurs, d'apr&#232;s Grothendieck", Preprint (2001).) 


Alex Heller's memoir is very readable

*  A. Heller, "Homotopy theories", Memoirs of the American Mathematical Society, Vol. 71, No 383 (1988).  

F. Muro's complementary slides surveying triangulated categories: [htag.pdf](http://personal.us.es/fmuro/htag.pdf).

[[!redirects triangulated categories]]