+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Philosophy
+-- {: .hide}
[[!include philosophy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

**Kinship** is the relation that obtains between persons related by real or fictive consanguinity. The organisation of these in systems of marriage and kinship play an important and prominent role for society as whole. In particular, in pre-industrial societies these tend to be cast into rigid and intricate patterns that are a preferred playground for applications of mathematics to anthropology ever since [[André Weil]] contributed an algebraic appendix to [[Claude Lévi-Strauss|Claude Lévi-Strauss']] groundbreaking [_Les structures &#233;l&#233;mentaires de la parent&#233;_](#LS67) in 1949.

### Topos-theoretic perspectives

Lawvere and Schanuel ([1997](#LawSchan97), [1999](#Law99)) proposed to study the concept of kinship starting from the notion of a (filiation structured) **society** modelled mathematically as a set $X$ (of _individuals_) together with two endofunctions $m,f$ that assign to an individual $x\in X$ his mother $m(x)\in X$ resp. his father $f(x)\in X$.

If one organizes these sets with filiation structure into a category the result is a [[topos]] namely the topos $Set^{M_2^{op}}$ of right actions of the free monoid $M_2$ on two symbols $\{m,f\}$.

Since the parental endofunctions $m,f$ are completely unconstrained[^Cour], the resulting 'kinship relations' are equally unconstrained, e.g. nothing prevents an individual's mother from coinciding with the same individual's father etc.  It therefore becomes necessary to equip the 'societies' with further structure. Lawvere and Schanuel propose to achieve this by introducing appropriate labeling objects $L$ and passage to the [[slice topos]] $Set^{M_2^{op}}/L$.

[^Cour]: so unconstrained indeed, that it might be better to think of the societies as being composed of 'sections' or 'marriage classes' instead of individuals and to think of $m,f$ as the assignment of the marriage classes  $m(x),f(x)$ of the respective parents of the individuals in the class $x$ in the spirit of [Courr&#232;ge (1965)](#Cour65). This has the drawback that it admits (hardly plausible) societies composed of infinitely many classes, whereas societies composed of (countably) infinitely-many individuals can be conceived of as an ideal self-image of a sucessful society projecting itself to eternity.

A minimal model of a society that at least keeps the **gender** of the parents apart is the set $G=\{female, male\}$ consisting of a 'female' and a distinct 'male' individual[^group] together with parental functions $m,f$ complying with the usual gender rules e.g. $m(female)=female$, $f(female)=male$ etc. Then a consistent gender distinction on the parental structure of an arbitrary society corresponds to a structure preserving map to $G$ i.e. an object of the slice topos $Set^{M_2^{op}}/G$.

[^group]: Again it makes more sense to consider $G$ to consist of two gender groups instead of two individuals.

Similarly, **exogamy** can be modeled by a _clans object_ $C$ e.g. consisting of two clans $C=\{bear, wolf\}$ obeying matrilinearity in the sense that the mother-of function $m$ is constant but the father-of function $f$ switches the clans expressing thereby that the father of an individual comes from another clan than the individual and his mother. By labeling with the product $G\times C$ one can achieve gender distinction and exogamy at the same time.

## Related entries

* [[Claude Lévi-Strauss]]

* [[canonical formula of myth]]

* [[structuralism]]

## Link

* Mathematical Anthropology and Cultural Theory ([online journal](http://mathematicalanthropology.org))

## References

Classical anthropological texts are 

* Robin Fox, _Kinship and Marriage_ , 2nd ed. Cambridge UP 1983.

* Maurice Godelier, _M&#233;tamorphoses de la parent&#233;_ , Fayard Paris 2004.

* {#LS67}[[Claude Lévi-Strauss]], _Les structures &#233;l&#233;mentaires de la parent&#233;_ , 2nd ed. Mouton The Hague 1967.

* [[Claude Lévi-Strauss]], _Reflexions sur l'atome de parent&#233;_ , L'Homme **13** no.3 (1973) pp.5-30. ([link](http://www.persee.fr/doc/hom_0439-4216_1973_num_13_3_367355))

An overview of structuralist kinship theory and a criticism of permutation models is

* {#Sperber68} Dan Sperber, _Le structuralisme en anthropologie_ , pp.167-238 in Ducrot et al. , _Qu'est-ce que le structuralisme?_ , Seuil Paris 1968.

Kinship systems are studied from a mathematical perspective in

* John P. Boyd, _The Algebra of Group Kinship_ , J. Math. Psych. **6** (1969) pp.139-167.

* {#Cour65}Philippe Courr&#232;ge, _Un mod&#232;le math&#233;matique des structures &#233;l&#233;mentaires de parent&#233;_ , L'Homme **5** no.3-4 (1965) pp.248-290. ([link](http://www.persee.fr/doc/hom_0439-4216_1965_num_5_3_366751))

* Aim&#233; Fuchs, _Les structures de parent&#233;: traitement math&#233;matique_ , Revue Europ&#233;enne des Sciences Sociales et Cahiers Vilfredo Pareto **19** (1981) pp.161-182.

* Alain Gottcheiner, _On some Classes of Kinship Systems I: Abelian Systems_ , Math. Anthr. **2** no. 4 (2008). ([pdf](http://mathematicalanthropology.org/Pdf/GottscheinerI_0908.pdf))

* Alain Gottcheiner, _On some Classes of Kinship Systems II: Nonabelian Systems_ , Math. Anthr. **2** no. 5 (2008). ([pdf](http://mathematicalanthropology.org/Pdf/GottscheinerII_0908.pdf))

* Labib Haddad, Yves Sureau, _Les groupes, les hypergroupes et l'&#233;nigme des Murngin_ , JPAA **87** (1993) pp.221-235.

* Per Hage, Frank Harary, _The Logical Structure of Asymmetric Marriage_ , L'Homme **36** no.139 (1996) pp.109-124. ([link](http://www.persee.fr/doc/hom_0439-4216_1996_num_36_139_370120))

* Paul Jorion, Gis&#232;le De Meur, Trudeke Vuyk, _Le mariage Pende_  , L'Homme **22** no.1 (1982) pp.53-73. ([link](http://www.persee.fr/doc/hom_0439-4216_1982_num_22_1_368256))

* Pin-Hsiung Liu, _Foundations of Kinship Mathematics_ , Academica Sinica Nankang 1986.

* [[Claude Lévi-Strauss]], Georges Guilbaud, _Syst&#232;me parental et matrimonial au Nord Ambrym_ , J. Soci&#233;t&#233; des oc&#233;anistes **26** no. 26 (1970) pp.9-32. ([link](http://www.persee.fr/doc/jso_0300-953x_1970_num_26_26_2281))

* Gis&#232;le De Meur (ed.), _New Trends in Mathematical Anthropology_ , Routledge London 1986.

* Gis&#232;le De Meur, Alain Gottcheiner, _Prescriptive Kinship Systems, Permutations, Groups, and Graphs_ , Math. Anthr. **1** no. 1 (2000). ([pdf](http://mathematicalanthropology.org/Pdf/MACTdeMEUR1100.pdf))

* Franklin E. Tjon Sie Fat, _Representing Kinship: Simple Models of Elementary Structures_ , PhD. Leiden University 1990.

* [[André Weil]], _Sur l'&#233;tude alg&#233;brique de certains types de lois de mariage (Syst&#232;me Murngin)_ , pp.257-263 in [L&#233;vi-Strauss (1949/1967)](#LS67).

* Harrison C. White, _An Anatomy of Kinship_ , Prentice-Hall Englewood Cliffs 1963.

A category-theoretic perspective is sketched in

* {#Law99}[[William Lawvere|F. William Lawvere]], _Kinship and Mathematical Categories_ , pp.411-425 in Jackendoff, Bloom, Wynn (eds.), _Language, Logic, and Concepts_ , MIT Press Cambridge 1999.

* {#LawSchan97}[[William Lawvere|F. William Lawvere]], [[Stephen Schanuel|Stephen H. Schanuel]], _Conceptual Mathematics_ , Cambridge UP 1997. (pp.162-163)

For related ideas see also

* Fran&#231;ois Lorrain, Harrison C. White, _Structural Equivalence of Individuals in Social Networks_ , Math. Sociology **1** (1971) pp.49-80.


[[!redirects kinship system]]
[[!redirects mathematical anthropology]]