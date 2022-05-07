
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A _coherent sheaf of modules_ is a geometric globalization of the notion of [[coherent module]].


## Definition

### Over a ringed topos

Let $(X,\mathcal{O})$ be a [[ringed space]] or, more generally, a [[ringed site]]. 

A [[sheaf]] $\mathcal{E}$ on $X$ of $\mathcal{O}$-[[module]]s is

*  __finitely generated__, or __[[of finite type]]__ , if every point $x \in X$ has an open neighbourhood such that there is a surjective morphism 

   $$\mathcal{O}^n|_U \to \mathcal{E}|_U$$ 

   from a [[free module]] to $\mathcal{E}|_{U}$,  where $n$ is finite. 

* __coherent__ if it is 

  1. finitely generated 

  1. for every open $U$ in the base space (resp. every object $U$ in the base site), every finite $p \in \mathbb{N}$ and every morphism 

     $$\mathcal{O}^p|_U\to \mathcal{E}|_U$$ 

     of $\mathcal{O}|_U$-modules has a finitely generated [[kernel]]. 

* __finitely presented__ if there is an exact sequence of the form 

  $$\mathcal{O}^p\to\mathcal{O}^n\to\mathcal{E}\to 0$$ 

  with $p$ and $n$ finite. 

  Every finitely presented $\mathcal{O}$-module is finitely generated. 

* __[[quasicoherent sheaf|quasi coherent]]__ if it is _locally_   -- on a cover $\{U_i\}$ -- _presentable_, i.e. for each $i$ there is an [[exact sequence]]s

  $$
    \mathcal{O}^{I_i}|_{U_i} \to \mathcal{O}^{J_i}|_{U_i}
    \to \mathcal{E}|_{U_i}
    \to 0\,,
  $$

  where $I_i$ and $J_i$ may be infinite, i.e. $\mathcal{E}$ is locally the [[cokernel]] of [[free module]]s. For more see [[quasicoherent sheaf]].

### Over a structured $(\infty,1)$-topos

Over a [[spectral Deligne-Mumford stack]]:

([[Quasi-Coherent Sheaves and Tannaka Duality Theorems|Lurie QCoh, def. 2.6.20]])

## Properties

For a coherent sheaf $\mathcal{E}$ over a [[ringed space]], for every  point $y$ in the base space $X$ there is a neighborhood $V$ such that the $\mathcal{O}_X(V)$-module $\mathcal{E}(V)$ of sections of $\mathcal{E}$ over $V$ is finitely presented. 
On a [[noetherian scheme]] the notions of finitely presented and coherent sheaves of $\mathcal{O}$-modules agree, but this is not true on a general scheme or general analytic space; sometimes even the structure sheaf $\mathcal{O}$ itself is a counterexample (not coherent while finitely presented).

The notion of coherent sheaf behaves well on the category of noetherian schemes. On a general topological space, by a basic result of Serre, if two of the sheaves of $\mathcal{O}$-modules in a [[short exact sequence]]
$$
0\to \mathcal{E}\to\mathcal{E}'\to \mathcal{E}''\to 0
$$
are coherent then so is the third. All this holds even if $\mathcal{O}$ is a sheaf of noncommutative [[rings]]. For commutative $\mathcal{O}$, the inner hom $Hom_{\mathcal{O}}(\mathcal{E},\mathcal{F})$ in the category of sheaves of $\mathcal{O}$-modules is coherent if $\mathcal{E},\mathcal{F}$ are coherent. 

A theorem of Serre says that the category of coherent sheaves over a projective variety of the form $Proj R$ where $R$ is a graded commutative Noetherian ring is equivalent to the localization of the category of finitely generated graded $R$-modules modulo its ("torsion") subcategory of (finitely generated graded) $R$-modules of finite length. 

## Historical note and definition variants

First works on coherent sheaves in complex analytic geometry. Serre adapted their work to algebraic framework in his famous article [[FAC]]. Hartshorne's definitions are changed/adapted to the special setup of Noetherian schemes with the excuse that the coherence does not behave that well otherwise; thus they differ from the definitions in [[EGA]] and [[FAC]].  

[[A. Vistoli]] commented at MathOverflow [here](http://mathoverflow.net/questions/68150) that for some categorical purposes

> one should interpret "coherent" as meaning "quasi-coherent of finite presentation". The notion of coherent sheaf, as defined in EGA, is not functorial, that is, pullbacks of coherent sheaves are not necessarily coherent. Hartshorne's book defines "coherent" as "quasi-coherent and finitely generated", but this is a useless notion when working with non-noetherian schemes.

## Related concepts

* [[degree of a coherent sheaf]], [[rank of a coherent sheaf]] [[slope of a coherent sheaf]], 

* [[stable coherent sheaf]]

* [[quasicoherent sheaf]]
* [[triangulated categories of sheaves]]
* [[Bondal-Orlov reconstruction theorem]]

* [[coherent cohomology]]

##References

* [[J-P. Serre]], _[[Faisceaux algébriques cohérents]]_, Ann. of Math. (2) __61__,  (1955) 197--278, [doi](http://dx.doi.org/10.2307/1969915).

* H. Grauert, R. Remmert, _Coherent analytic sheaves_, Grundlehren der Math. Wissenschaften __265__, Springer 1984. xviii+249 pp.

* M. M. [[Kapranov]], _On the derived categories of coherent sheaves on some homogeneous spaces_,  Invent. Math.  92  (1988),  no. 3, 479--508, [doi](http://dx.doi.org/10.1007/BF01393744). 

* [[D. O. Orlov]], _&#1055;&#1088;&#1086;&#1080;&#1079;&#1074;&#1086;&#1076;&#1085;&#1099;&#1077; &#1082;&#1072;&#1090;&#1077;&#1075;&#1086;&#1088;&#1080;&#1080; &#1082;&#1086;&#1075;&#1077;&#1088;&#1077;&#1085;&#1090;&#1085;&#1099;&#1093; &#1087;&#1091;&#1095;&#1082;&#1086;&#1074; &#1080; &#1101;&#1082;&#1074;&#1080;&#1074;&#1072;&#1083;&#1077;&#1085;&#1090;&#1085;&#1086;&#1089;&#1090;&#1080; &#1084;&#1077;&#1078;&#1076;&#1091; &#1085;&#1080;&#1084;&#1080;_ ([pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=629&what=fullt&option_lang=rus), Russian)  Uspekhi Mat. Nauk __58__  (2003),  no. 3(351), 89--172;  Engl. transl. _Derived categories of coherent sheaves and equivalences between them_, Russian Math. Surveys __58__ (2003),  no. 3, 511--591.

* V. D. Golovin, _Homology of analytic sheaves and duality theorems_, Contemporary Soviet Mathematics (1989) viii+210 pp. transl. from Russian original &#1043;&#1086;&#1084;&#1086;&#1083;&#1086;&#1075;&#1080;&#1080; &#1072;&#1085;&#1072;&#1083;&#1080;&#1090;&#1080;&#1095;&#1077;&#1089;&#1082;&#1080;&#1093; &#1087;&#1091;&#1095;&#1082;&#1086;&#1074; &#1080; &#1090;&#1077;&#1086;&#1088;&#1077;&#1084;&#1099; &#1076;&#1074;&#1086;&#1081;&#1089;&#1090;&#1074;&#1077;&#1085;&#1085;&#1086;&#1089;&#1090;&#1080;, Moskva, Nauka 1986. (192 pp.)

* [[EGA]] 0.5.3.1
* Qing Liu, _Algebraic geometry and arithmetic curves_, 5.1.3

Categories of ind-coherent sheaves on schemes and stacks are studied  in [[Dennis Gaitsgory]], _Notes on Geometric Langlands: ind-coherent sheaves_, [arxiv/1105.4857](http://arxiv.org/abs/1105.4857)

Discussion in [[(∞,1)-topos theory]]

* [[Jacob Lurie]], _[[Quasi-Coherent Sheaves and Tannaka Duality Theorems]]_

category: sheaf theory, algebraic geometry

[[!redirects coherent sheaves]]