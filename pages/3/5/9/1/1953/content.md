
#Contents#
* table of contents
{:toc}

## Idea

A [[space]] $X$ is called **formally smooth** if every [[morphism]]s $Y \to X$ into it has all possible [[infinitesimal object|infinitesimal]] extensions.

Traditionally this has considered in the context of [[geometry]] over formal duals of [[ring]]s and [[associative algebra]]s. This we discuss in the section ([Concrete notion](#ConcreteNotion)). But generally the notion makes sense in any context of <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a>. This we discuss in the section 
[General abstract notion](#GeneralAbstractNotion).

## General abstract notion
 {#GeneralAbstractNotion}

 [KontsevichRosenbergSpaces](#KontsevichRosenbergSpaces)


## Concrete notion
 {#ConcreteNotion}

In the context of geometry over formal duals of [[ring]]s and [[associative algebra]]s there are two definitions




* Grothendieck's notion of formal smoothness for [[commutative rings]], [[schemes]], morphisms (or even more general functors $Scheme^{op}\to Set$) which will be discussed here. 



In EGA IV, Grothendieck defines formal smoothness in the generality of relative setup: for morphisms. Formal smoothness is weaker than smoothness, and there are characterizations when formally smooth morphisms are smooth.


### Over commutative rings 
 {#OverCommutativeRings}

A morphism $f :X\to Y$ is __formally smooth__ if   it satisfies the _infinitesimal lifting property_: for every ring $A$ and nilpotent [[ideal]] $I\subset A$ and morphism $Spec(A)\to Y$ the induced map

$$ Hom_Y(Spec(A), X)\to Hom_Y(Spec(A/I),X)$$

is surjective. 

This is due to ([[EGAIV]]${}_4$ 17.1.1)

#### Smoothness versus formal smoothness 

For a morphism $f:X\to Y$ of schemes, and $x$ a point of $X$, the following are equivalent

(i) $f$ is smooth at $x$

(ii) $f$ is locally of finite presentation at $x$ and there is an open neighborhood $U\subset X$ of $x$ such that $f|_U: U\to Y$ is formally smooth

(iii) $f$ is flat at $x$, locally of finite presentation at $x$ and the sheaf of [[Kähler differential]]s $\Omega_{X/Y}$ is locally free in a neighborhood of $x$

The relative dimension of $f$ at $x$ will equal the rank of the module of K&#228;hler differentials. 

This is ([[EGAIV]]${}_4$ 17.5.2 and 17.15.15)


#### Formally smooth scheme 

A [[scheme]] $S$, i.e. a scheme over the ground ring $k$, is a [[formally smooth scheme]] if the corresponding morphism $S \to Spec(k)$ is a formally smooth morphism.

There is also an interpretation of formal smoothness via the formalism of [[Q-categories]].

### Over noncommutative algebras

see 

  ([CuntzQuillen](#CuntzQuillen)), [[quasi-free algebra]]

## References

The definition over commutative rings is in 

* [[EGAIV]]${}_4$ Publ. IH&#201;S, 32 (1967), p. 5-361) see [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1967__32__5_0.


The definition over noncommutative algebras is in

* [[J. Cuntz]], [[D. Quillen]], _Algebra extensions and nonsingularity_, J. Amer. Math. Soc. __8__ (1995), 251&#8211;289.
 {#CuntzQuillen}

The general abstract definition and its relation to the standard definitions is in

* [[Maxim Kontsevich]], [[Alexander Rosenberg]], _Noncommutative spaces_, preprint MPI-2004-35 ([ps](http://www.mpim-bonn.mpg.de/preprints/send?bid=2331), [dvi](http://www.mpim-bonn.mpg.de/preprints/send?bid=2303))
 {#KontsevichRosenbergSpaces}


See also 

* [MO:is-formal-smoothness-a-local-property](http://mathoverflow.net/questions/22393/is-formal-smoothness-a-local-property)

* A. Ardizzoni, _Separable functors and [[formal smoothness]]_,  J. K-Theory  1  (2008),  no. 3, 535--582, [math.QA/0407095](http://arxiv.org/abs/math.QA/0407095), [doi](http://dx.doi.org/10.1017/is007011015jkt012), [MR2009k:16069](http://www.ams.org/mathscinet-getitem?mr=2009k:16069)

* T. Brzezi&#324;ski, _Notes on formal smoothness_, *in*: Modules and Comodules (series _Trends in Mathematics_). T Brzezi&#324;ski, JL Gomez Pardo, I Shestakov, PF Smith (eds), Birkh&#228;user, Basel, 2008, pp. 113-124 ([doi](http://dx.doi.org/10.1007/978-3-7643-8742-6), [arXiv:0710.5527](http://arxiv.org/abs/0710.5527))


[[!redirects formal smoothness]]
[[!redirects formally smooth]]