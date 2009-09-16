We should distinguish 

* Cuntz--Quillen formal smoothness in noncommutative setup (see [[quasi-free algebra]])

* the Grothendieck's notion of formal smoothness for [[commutative rings]], [[schemes]], morphisms (or even more general functors $Scheme^{op}\to Set$) which will be discussed here. 

In EGA IV, Grothendieck defines formal smoothness in the generality of relative setup: for morphisms. Formal smoothness is weaker than smoothness, and there are characterizations when formally smooth morphisms are smooth.


##Definition (EGAIV${}_4$ 17.1.1)##

A morphism $f :X\to Y$ is __formally smooth__ if   it satisfies the _infinitesimal lifting property_: for every ring $A$ and nilpotent ideal $I\subset A$ and morphism $Spec A\to Y$ the induced map

$$ Hom_Y(Spec A, X)\to Hom_Y(Spec(A/J),X)$$

is surjective. 


##Smoothness versus formal smoothness (EGAIV${}_4$ 17.5.2 and 17.15.15)##

For a morphism $f:X\to Y$ of schemes, and $x$ a point of $X$, the following are equivalent

(i) $f$ is smooth at $x$

(ii) $f$ is locally of finite presentation at $x$ and there is an open neighborhood $U\subset X$ of $x$ such that $f|_U: U\to Y$ is formally smooth

(iii) $f$ is flat at $x$, locally of finite presentation at $x$ and the sheaf of [[Kähler differential]]s $\Omega_{X/Y}$ is locally free in a neighborhood of $x$

The relative dimension of $f$ at $x$ will equal the rank of the module of K&#228;hler differentials. 

For EGAIV$_4$ (Publ. IH&#201;S, 32 (1967), p. 5-361) see [numdam](http://www.numdam.org/numdam-bin/fitem?id=PMIHES_1967__32__5_0).

## formally smooth scheme ##

A [[scheme]] $S$, i.e. a scheme over the ground ring $k$, is a [[formally smooth scheme]] if the corresponding morphism $S \to Spec(k)$ is a formally smooth morphism.

There is also an interpretation of formal smoothness via the formalism of [[Q-categories]].

[[!redirects formal smoothness]]
[[!redirects formally smooth]]