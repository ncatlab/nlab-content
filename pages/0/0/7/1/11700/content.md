
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Analytification is the process of universally turning an [[algebraic space]] into an [[analytic space]].

## Definition

Let $X \to Spec(\mathbb{C})$ be a [[scheme]] of [[locally finite type]] over the [[complex numbers]]. Its set $X(\mathbb{C})$ of "complex points" is the set of [[maximal ideals]], since $\mathbb{C}$ is an [[algebraically closed field]], e.g. [Neeman 07, prop. 4.2.4](#Neeman07)). 

This set $X(\mathbb{C})$ canonically carries the [[complex analytic topology]]. As such it is a [[topological space]] written $X^{an}$. Equipped with the canonical [[structure sheaf]] $\mathcal{O}_{X^{an}}$ this is a [[complex analytic space]]. This $(X^{an}, \mathcal{O}_{X^{an}})$ is called the _analytification_ of $X$. 

This construction extends to a [[functor]] from the [[category]] of [[schemes]] over $\mathbb{C}$ to that of [[complex analytic spaces]].

See e.g. ([Neeman 07, section 4, p.71](#Neeman07), [Danilov 91, chapter 3, paragraph 1, section 1.1 (p.61)](#Danilov91)

Generalization to [[structured (infinity,1)-toposes]] is in ([Lurie 08, remark 4.4.13](#Lurie08)).

## Examples

The analytification of the [[projective space]] $\mathbb{P}^1$ is the [[complex projective space]] $(\mathbb{P}^1)^{an} \simeq \mathbb{C}\mathbb{P}^1$, hence the [[Riemann sphere]].

The analytification of an [[elliptic curve]] is the [[complex torus]].

see e.g. ([Danilov 91, example in chapter 3, paragraph 1, section 1.1. (p. 61)](#Danilov91))


## Properties

### Existence and fully faithfulness (GAGA)
 {#Existence}

The analytification of an [[algebraic space]] over the [[complex numbers]] which is

1. [[locally of finite type]]

1. [[locally separated]]

is a [[complex analytic space]].

Moreover, under suitable conditions analytification is a [[fully faithful functor]].

This is a classical result due to ([Artin 70, theorem 7.3](#Artin70)). A textbook account of the proof is in ([Neeman 07, section 10](#Neeman07)).  Discussion in more general [[analytic geometry]] is in ([Conrad-Temkin 09, section 2.2](#ConradTemkin09)). 

Generalization to [[algebraic stacks]]/[[Deligne-Mumford stacks]]/[[geometric stacks]] is in ([Lurie 04](#Lurie04), [Hall 11](#Hall11), [Geraschenko & Zureick-Brown 12](#GeraschenkoZureickBrown12)).

### As geometric realization in $\mathbb{A}^1$-homotopy theory
 {#GeometricRealizationInA1Homotopy}

For $k \hookrightarrow \mathbb{C}$ a field, then 
the functor that takes a smooth complex scheme to the the [[homotopy type]]
underlying its analytification induces [[geometric realization]]

$$
  Sh_\infty(Sch^{sm}_k)
  \to 
  Sh_\infty(Sch^{sm}_k)^{\mathbb{A}^1}
  \to 
  \infty Grpd
$$

([Isaksen 01](#Isaksen01), [Dugger-Isaksen 05, theorem 5.2](#DuggerIsaksen05))

## Related concepts

* [[GAGA]]

## References

### Complex analytification

Original articles include

* {#Artin70} [[Michael Artin]], _Algebraization of formal moduli: II. Existence of modifications_, Annals of Math., 91 no. 1 (1970), pp. 88&#8211;135.

* [[Alexander Grothendieck]], [[SGA]] I, Expos&#233; XII

A review of that is in 

* Yan Zhao, _G&#233;om&#233;trie alg&#233;brique et g&#233;om&#233;trie analytique_, 2013 ([pdf](http://pub.math.leidenuniv.nl/~jinj/2013/efg/gaga.pdf))

Textbook accounts include

* {#Neeman07} [[Amnon Neeman]], _Algebraic and analytic geometry_, London Math. Soc. Lec. Note Series __345__, 2007 ([publisher](http://www.cambridge.org/us/academic/subjects/mathematics/geometry-and-topology/algebraic-and-analytic-geometry))

* {#Danilov91} [[Vladimir Danilov]], chapter 3 of _Cohomology of algebraic varieties_, in I. Shafarevich (ed.), _Algebraic Geometry II_, volume 35 of _Encyclopedia of mathematical sciences_, Springer 1991 ([GoogleBooks](http://books.google.de/books?id=ZhzXJHUgcRUC&lpg=PA67&ots=aVQoeMkBwc&dq=analytification&pg=PA61&redir_esc=y#v=onepage&q=analytification&f=false)))

Discussion for [[real analytic spaces]] includes

* {#Huisman02} [[Johannes Huisman]], section 2 of _The exponential sequence in real algebraic geometry and Harnack's Inequality for proper reduced real schemes_, Communications in Algebra, Volume 30, Issue 10, 2002 ([pdf](http://pageperso.univ-brest.fr/~huisman/rech/publications/exphi.pdf))


Generalizations to [[higher geometry]] are in

* {#ConradTemkin09} [[Brian Conrad]], M. Temkin: *Non-Archimedean analytification of algebraic spaces*, J. Algebraic Geom. **18** 4 (2009) 731-788 &lbrack;[arXiv:0706.3441](http://arxiv.org/abs/0706.3441), [doi:10.1090/S1056-3911-09-00497-4](https://doi.org/10.1090/S1056-3911-09-00497-4)&rbrack;


* {#Lurie04} [[Jacob Lurie]], _[[Tannaka duality for geometric stacks]]_, ([arXiv:math.AG/0412266](http://arxiv.org/abs/math/0412266))

* {#Lurie08} [[Jacob Lurie]], _[[Structured Spaces]]_, 2008

* {#Hall11} [[Jack Hall]], _Generalizing the GAGA Principle_ ([arXiv:1101.5123](http://arxiv.org/abs/1101.5123))

* {#GeraschenkoZureickBrown12} [[Anton Geraschenko]], David Zureick-Brown, _Formal GAGA for good moduli spaces_ ([arXiv:1208.2882](http://arxiv.org/abs/1208.2882))

See also

* [[Walter Gubler]]. _Forms and currents on the analytification of an algebraic variety (after Chambert-Loir and Ducros)_ ([arXiv:1303.7364](http://arxiv.org/abs/1303.7364))

Discussion in the context of [[hypercovers]] and [[A1-homotopy theory]] is in 


* {#Isaksen01} [[Daniel Isaksen]], _&#201;tale realization of the $\mathbb{A}^1$-homotopy theory of schemes_, 2001 ([K-theory archive](http://www.math.uiuc.edu/K-theory/0495/))

* {#DuggerIsaksen05} [[Daniel Dugger]] and [[Daniel Isaksen]], _Hypercovers in topology_, 2005 ([pdf](http://www.math.uiuc.edu/K-theory/0528/hypercover.pdf), [K-Theory archive](http://www.math.uiuc.edu/K-theory/0528/))

### Non-archimedean analytification
 {#ReferencesNonArchimedeanAnalytification}

Discussion in more general [[rigid analytic geometry]] is in

* [[Brian Conrad]], Michael Temkin, _Non-archimedean analytification of algebraic spaces_ ([arXiv:0706.3441](http://arxiv.org/pdf/0706.3441))

[[!redirects analytifications]]