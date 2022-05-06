
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


[[!redirects  geometric theory of categories]]
[[!redirects essentially algebraic theory of categories]]
[[!redirects cartesian theory of categories]]

#Contents#
* table of contents
{:toc}

##Idea
The [[geometric theory|geometric]] **theory of categories** $\mathbb{K}$ is a [[first-order logic|first-order]] axiomatisation of the concept of a  [[category]]. $\mathbb{K}$ is (morally) an [[essentially algebraic theory]], and literally a cartesian theory i.e. _grosso modo_ a [[regular theory]] where existential quantification is provably unique.

Historically, the first axiomatisation was given by [[William Lawvere| F. William Lawvere]] in his [[Functorial Semantics of Algebraic Theories|dissertation]] in 1963 as part of a formalisation of the [[category of categories]] (cf. Lawvere ([1963](#Law63},[1966](#Law66)) or [[ETCC]] for further information).

## Definition

The [[signature]] $\Sigma_\mathbb{K}$ has two sorts $O$ and $A$ for objects and arrows, respectively, three function symbols $d_0:A\to O$ , $d_1:A\to O$ and $id:O\to A$, assiging to morphisms their domain, respectively, codomain and to the objects their [[identity|identity morphisms]], as well as a relation symbol $C\rightarrowtail A\times A\times A$ expressing composition of morphisms.

The **theory of categories** is the theory $\mathbb{K}$ over the signature $\Sigma_\mathbb{K}$ with the following sequents:[^var]

[^var]: Here and in the following $x,y$ are variables ranging over O, whereas the $f_1,f_2,\dots$ range over A; the contexts are assumed to be canonical i.e. consisting of all free distinct variables occurring in a sequent listed in order of first appearance.

* $\top\vdash d_0(id(x))=x\wedge d_1(id(x))=x\quad$ ,

* $C(f_1,f_2,f_3)\vdash d_0(f_1)=d_0(f_3)\wedge d_1(f_1)=d_0(f_2)\wedge d_1(f_2)=d_1(f_3)\quad $ ,

* $C(f_1,f_2,f_3)\wedge C(f_1,f_2,f_4)\vdash f_3=f_4\quad $ ,

* $d_1(f_1)=d_0(f_2)\vdash\exists f_3 C(f_1,f_2,f_3)\quad$ ,

* $\top \vdash C(f,id(d_1(f)),f)\wedge C(id(d_0(f)),f,f)\quad $ ,

* $C(f_1,f_2,f_4)\wedge C(f_2,f_3,f_5)\wedge C(f_4,f_3,f_6)\wedge C(f_1,f_5,f_7)\vdash f_6=f_7\quad $.

### Remark

The third axiom implies that the existential quantification occurring in the fourth axioms is unique thus $\mathbb{K}$ is indeed _cartesian_. Since the chosen signature uses a composition relation instead of a partial composition operation the theory as given here is not literally [[essentially algebraic theory|essentially algebraic]] in the syntactic sense, though, of course, it is [[Morita equivalence|Morita equivalent]] to an essentially algebraic axiomatisation. Other signatures, like a single sorted "arrows only" one, are also possible, the one used here (taken from Johnstone [1977](#J77)) leans on the so called **elementary theory of abstract categories** as presented in Lawvere ([1966](#Law66)).

## Properties

Foremost, we have

+-- {: .num_prop}
###### Proposition

Let $\mathcal{E}$ be a [[Grothendieck topos]]. Then $Mod_{\mathbb{K}}(\mathcal{E})=cat(\mathcal{E})$ with $cat(\mathcal{E})$ the category of (small) [[internal category|internal categories]] in $\mathcal{E}$ with internal functors as morphisms.$\qed$
=--

+-- {: .num_prop}
###### Proposition
The [[classifying topos]] $Set[\mathbb{K}]$ is the presheaf topos on the opposite of the category of finitely presentable categories in $Set$.
=--

This follows from the fact that the classifying toposes of [[cartesian theory|cartesian theories]] are generally given as the presheaf toposes on the opposite of the category of finitely presentable models in $Set$ (cf. Johnstone [2002](#J02), p.891).[^diss] The proposition holds more generally with $Set$ replaced by an arbitrary topos $\mathcal{E}$ with a [[natural numbers object]] (cf. Johnstone-Wraith [1978](#JW78), p.226).$\qed$

[^diss]: Apparently $Set[\mathbb{K}]$ made its first appearance in Johnstone's 1974 Cambridge dissertation on "Internal category Theory" (cf. Tierney [1976](#Tierney76)). 

## Some related theories

* The [[theory of model homomorphisms|theory $\mathbb{K}^2$ of $\mathbb{K}$-model homomorphisms]] is the **theory of functors**.

* Recall that a _discrete opfibration_ is an internal functor $F\,:\,\mathbf{F}\to \mathbf{C}$ with the property that the following diagram
$$
\array{ 
   & & \\
F_1 &\overset{d_0}{\longrightarrow}& F_0
    \\
    {}^{\mathllap{\gamma_1}}
    \downarrow 
    & & 
    \downarrow^{\mathrlap{\gamma_0}}
    \\
    C_1 
      &\underset{d_0}{\longrightarrow}& 
    C_0
    \\  & &
  }
$$
  is pullback. Whence by adding the appropriate geometric axiom to the theory $\mathbb{K}^2$ of functors one obtains as a quotient the **theory of discrete opfibrations** $\mathbb{K}^2_\downarrow$.

  Let $\mathbf{C}\in cat(\mathcal{E})$ be an internal category. By pulling back its classifying morphism $\overline{\mathbf{C}}\,:\,\mathcal{E}\to \mathcal{E}[\mathbb{K}]$ along the geometric morphism $d_1\,:\,\mathcal{E}[\mathbb{K}^2_\downarrow]\to \mathcal{E}[\mathbb{K}]$ that classifies the codomain of the generic discrete opfibration as an internal category
$$
\array{ \mathcal{E}[\mathbb{K}^\downarrow_\mathbf{C}] &\longrightarrow &\mathcal{E}[\mathbb{K}^2_{\downarrow}]
    \\
    \downarrow 
    & & 
    \downarrow^{d_1}
    \\
    \mathcal{E} 
      &\underset{\overline{\mathbf{C}}}{\longrightarrow}& 
    \mathcal{E}[\mathbb{K}]
    \\ & &
  }
$$
  one obtains the classifying topos $\mathcal{E}[\mathbb{K}^{\downarrow}_\mathbf{C}]$ for discrete opfibrations on $\mathbf{C}$, or, equivalently, internal diagrams (=copresheaves) on $\mathbf{C}$. Since an internal [[profunctor]] $\mathbf{C} &#8696; \mathbf{D}$ is by definition an internal diagram on $\mathbf{C}^{op}\times\mathbf{D}\,$, one can use this construction to obtain the _classifying topos for internal profunctors_ from $\mathbf{C}$ to $\mathbf{D}$ by pulling back along the classifying morphism for $\mathbf{C}^{op}\times\mathbf{D}$ (cf. Johnstone [1977](#J77), p.209).

* By adding the following sequents to the theory $\mathbb{K}$ of categories one obtains the **theory of filtered categories** $\mathbb{K}^\gt$ with models the internal [[filtered category|filtered categories]] (cf. Johnstone [1977](#J77), p.203):

  $\array{\\
\top\vdash \exists x (x=x)
\\
\\ 
\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\top\vdash \exists f_1\exists f_2 (d_0(f_1)=x\wedge d_0(f_2)=y\wedge d_1(f_1)=d_1(f_2))
\\
d_0(f_1)=d_0(f_2)\wedge d_1(f_1)=d_1(f_2)\vdash \exists f_3\exists f_4\big (C(f_1,f_3,f_4)\wedge C(f_2,f_3,f_4)\big )\quad}$



## Related entries

* [[category]]

* [[category theory]]

* [[geometric theory]]

* [[theory of objects]]

* [[theory of model homomorphisms]]

* [[theory of flat functors]]

* [[ETCC]]


## References

* [[Peter Freyd|P. J. Freyd]], A. Scedrov, _[[Categories, Allegories]]_ , North-Holland Amsterdam 1990.

* {#J77}[[Peter Johnstone]], _Topos Theory_ , Academic Press New York (1977). (Also available as Dover Reprint, Mineola 2014, p.202f)

* {#J02}[[Peter Johnstone]], _Sketches of an Elephant vol.2_ , Oxford UP 2002. (D1.1.7(e), p.813, D1.3.4, p.833)

* {#JW78}[[Peter Johnstone]], [[Gavin Wraith]], _Algebraic Theories in Toposes_ , pp.141-242 in Johnstone, Paré (eds.), _Indexed Categories and Their Applications_ , Springer LNM **661** Heidelberg 1978.

* {#Law63}F. W. Lawvere, _[[Functorial Semantics of Algebraic Theories]]_ , Ph.D. thesis, Columbia University New York 1963. (With an author's comment and a supplement in: Reprints in Theory and Applications of Categories, no.5 (2004) pp.1-121 ([pdf](http://www.tac.mta.ca/tac/reprints/articles/5/tr5.pdf)))

* {#Law66}F. W. Lawvere, _The Category of Categories as a Foundation for Mathematics_ , pp.1-20 in Eilenberg, Harrison, MacLane, R&#246;hrl (eds.), _Proceedings of the Conference on Categorical Algebra - La Jolla 1965_, Springer Heidelberg 1966.

* {#Tierney76}[[Myles Tierney]], _Forcing Topologies and Classifying Toposes_ , pp.211-219 in Heller, Tierney (eds.), _Algebra, Topology and Category Theory_  , Academic Press New York 1976.


