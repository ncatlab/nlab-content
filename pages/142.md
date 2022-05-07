
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The term _stack_, is a traditional synonym for _[[2-sheaf]]_ or often, more restrictively, as a synonym for _[[(2,1)-sheaf]]_ (see there for more details).

This is part of a whole hierarchy of [[higher category theory|higher categorical]] generalizations of the notion of _[[sheaf]]_. A [[(2,1)-sheaf]] / stack is equivalently a [[1-truncated]] [[(∞,1)-sheaf]]/[[∞-stack]].

Generally, then, _[[n-stack]]_ is a synonym for _[[n-sheaf|(n+1)-sheaf]]_, or more restrictively for _[[(n,1)-sheaf|(n+1,1)-sheaf]]_.

More concretely this means that a 1-stack on a [[site]] $S$ (or more generally [[(2,1)-site]] or even [[(2,2)-site]] $S$) is 

* a ([[pseudofunctor|pseudo]]-)[[functor]] from  $S^{op}$ to the 2-category [[Cat]] of categories,

* that satisfies [[descent]] for all covers.

If the pseudofunctor takes values in the 2-subcategory [[Grpd]]$\subset Cat$ of groupoids, the stack is sometimes referred to as a stack of groupoids. This is the more commonly occurring case so the term 'stack' has come to mean 'stack of groupoids' in much of the literature. 

In some circles the notion of a stack as a generalized [[groupoid]] is almost more familiar than the notion of sheaf as a [[space and quantity|generalized space]]. For instance [[differentiable stacks]] have attracted much attention in the study of [[Lie groupoids]] and [[orbifolds]], while [[diffeological space]]s are only beginning to be investigated more in [[Lie theory]]. Groupoid stacks are closely related to internal groupoids [MO](https://mathoverflow.net/questions/93948/link-between-internal-groupoids-and-stacks-on-a-topos).

An [[algebraic stack]], [[differentiable stack]] etc. is a stack over a site of schemes or differentiable manifolds with additional representability conditions. 


## Provisional discussion

The following is "provisional" material on stacks that [[Todd Trimble]] wrote in the course of a discussion with [[Urs Schreiber|Urs]]. Somebody should turn this here into a coherent entry on stacks.

***

(Todd speaking.) I don't really speak "stacks", but in an effort to build a bridge between sheaves and stacks, I'll write down what I thought I understood, and ask someone such as Urs to come in and check. (Warning: I'm treating this edit box almost as a sandbox, in that what I say below is all a bit provisional until we get some discussion going.) 

+--{.query}
 Hi Todd, thanks for this. I started making some remarks on the relation between descent $\infty$-categories and pseudofunctors from [[covers]] regarded as [[sieves]] (hence as presheaves) at [[descent and codescent]] in the section titled _Descent in terms of pseudo-functors_.
=--

At the simplest level, let $C$ be a category. As we know, a presheaf on $C$ is just a functor $X: C^{op} \to Set$. 

Now let's categorify just once: regard a category $C$ as a bicategory whose local hom-categories are discrete. What I'll call a "pre-stack" is then a homomorphism of bicategories $X: C^{op} \to Cat$. Here I'm following Street's terminology: a homomorphism of bicategories is the "pseudo" version of a weak map of bicategories, as opposed to the "lax" version. So, we have given coherent isomorphisms $X(f)X(g) \to X(f g)$, and so on.  

Now suppose that $C$ also comes equipped with a topology $J$, and let $F$ be a $J$-covering sieve for $c$, so that in particular it's a subfunctor $i: F \hookrightarrow \hom(-, c)$. We want to build a (truncated) simplicial object out of this, and to this end I'll use some yoga which was basically developed in my Cafe post [on the bar construction](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html) [perhaps this may go partway to addressing your most recent [query](http://golem.ph.utexas.edu/category/2007/05/on_the_bar_construction.html#c021027) there, Urs]. 

Namely, there is a canonical way of presenting $F$ as a colimit of representables. Officially, it's given by a coend formula, but it's probably more illuminating to think of it in terms of tensor products over $C$: 

$$\hom_C(-, -) \otimes_C F(-) \cong F(-)$$ 

In the long-winded version, this says that $F$ is the coequalizer of a diagram having the form 

$$\sum_{c, d} \hom_C(-, c) \times \hom_C(c, d) \times F(d) \stackrel{\to}{\to} \sum_c \hom_C(-, c) \times F(c) \to F(-)$$ 

where the more visible one of the two parallel arrows involves the contravariant action of $C$ on $F$: 

$$\hom(c, d) \times F(d) \to F(c)$$ 

and the less visible one uses $C$ acting on itself: 

$$\hom(-, c) \times \hom(c, d) \times F(d) \to hom(-, d) \times F(d)$$ 

The point now is that this coequalizer diagram represents the tail end of a simplicial object (with $F(-)$ appearing in dimension -1), which in the notation of the bar construction one could call $B(C, C, F)$. Let me explain this last bit. 

The point is that any category $C$ can be regarded as a monad in the bicategory of spans. The underlying span is of course 

$$C_0 \stackrel{dom}{\leftarrow} C_1 \stackrel{cod}{\to} C_0$$ 

and a presheaf $F$ on $C$, as a discrete op-fibration, has an underlying span 

$$C_0 \leftarrow F \to 1$$ 

and is precisely an algebra over the monad $C$. Then, given the data of a monad and an algebra over that monad, one proceeds to build the bar construction as a simplicial object, and I think this is probably the simplicial thingy we want to base the category of descent data on (given a pre-stack $X$). 

In fact, if memory serves the category of descent data can be efficiently expressed in bicategorical language as follows. The covering sieve $F$ becomes a homomorphism of bicategories by changing base from $Set$ to $Cat$: 

$$C^{op} \stackrel{F}{\to} Set \stackrel{discrete}{\to} Cat$$ 

and, abbreviating $discrete$ to $d$, it turns out that 

$$Desc_F(X) \simeq Nat(d F, X)$$ 

where the thing on the right side is the category of strong (i.e., pseudo) natural transformations between the indicated bicategory homomorphisms. 

In that case, the stack condition on $X$ becomes the statement that the canonical functor 

$$X(c) \stackrel{Yoneda}{\cong} Nat(d \hom(-, c), X) \to Nat(d F, X)$$ 

(where the first equivalence comes from the bicategorical Yoneda lemma, and the second functor is induced from the subfunctor $i: F \to \hom(-, c)$) is an equivalence for all $J$-covering sieves $F$. This formulation connects up nicely, that is, is a straight categorification of what was put down in the entry [[sheaf]]. 

###Examples

* The stack of $BG$ is a functor $Mfd^{op} \to Gpd$, sending $U\in Mfd$ to the groupoid of $G$-principal bundles over $U$ with $G$-equivariant morphisms; sending $U\xrightarrow{f} V$ to the functor induced by pullbacks of principal bundles via $f$.  Then $BG$ comes from the prestack $BG^p: Mfd^{op} \to Gpd$ sending $U\in Mfd$ to the groupoid of trivial principal bundles over $U$ with $G$-equivariant morphisms (then it is just a $G$-valued function $U\xrightarrow{g} G$; sending $U\xrightarrow{f}V$ to the functor induced by pullbacks of principal bundles via $f$. Then sheafification or stackification will give us $BG$ back. 



## Related concepts

* [[sheaf]]

* [[presheaf of groupoids]]

* [[group stack]]

* [[2-sheaf]] / [[(2,1)-sheaf]] /  **stack** / [[model structure for (2,1)-sheaves]]

  * [[representable morphism of stacks]]

  * [[mapping stack]], [[quotient stack]]

  * [[geometric stack]]

    * [[differentiable stack]], [[Deligne-Mumford stack]]

  * [[rigidification of a stack]]

  * [[moduli stack]]

  * [[Picard stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]]

* [[axiom of stack completion]]

Special kinds of stacks include

* [[geometric stacks]];

* [[gerbes]].

[[!include homotopy n-types - table]]



## References

The concept originates, under the French term _champ_, in 

* {#Giraud66} [[Jean Giraud]], _Cohomologie non ab&#233;lienne_, Columbia University  (1966) ([GoogleBooks](https://books.google.de/books/about/Cohomologie_non_ab%C3%A9lienne.html?id=EQ1CAAAAIAAJ&redir_esc=y))

  published as: Grundlehren 179, Springer Verlag (1971) ([doi:10.1007/978-3-662-62103-5](https://www.springer.com/gp/book/9783540053071))

and under the English term _stack_ in

* {#DeligneMumford69} [[Pierre Deligne]], [[David Mumford]], _The irreducibility of the space of curves of given genus_, Publications Math&#233;matiques de l'IH&#201;S (Paris) 36: 75&#8211;109 (1969) ([numdam:PMIHES_1969__36__75_0](http://www.numdam.org/item?id=PMIHES_1969__36__75_0))


* [[Jean Giraud]], _Classifying topos_, in: [[William Lawvere]] (ed.) _Toposes, Algebraic Geometry and Logic_, Lecture Notes in Mathematics, vol 274. Springer (1972) ([doi:10.1007/BFb0073964](https://doi.org/10.1007/BFb0073964))

Further early discussion includes

* [[Marta Bunge]], [[Robert Pare]], _Stacks and equivalence of indexed categories_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 20 no.4 (1979) ([numdam](http://www.numdam.org/item?id=CTGDC_1979__20_4_373_0))
 
* [[Marta Bunge]], _Stack completions and Morita equivalence for categories in a topos_, Cahiers de topologie et g&#233;om&#233;trie diff&#233;rentielle xx-4, (1979)
401-436, ([MR558106](http://www.ams.org/mathscinet-getitem?mr=558106), [numdam](http://www.numdam.org/item?id=CTGDC_1979__20_4_401_0))

See also the references at _[[2-sheaf]]_.
 
Review:

* [[Ieke Moerdijk]], _Introduction to the language of stacks and gerbes_ ([arXiv](http://arxiv.org/abs/math/0212266))

* [[Jochen Heinloth]], _Some notes on differentiable stacks_ ([pdf](http://www.uni-due.de/~hm0002/stacks.pdf))

Discussion of stacks in their incarnation (under the [[Grothendieck construction]]) as [[Grothendieck fibrations]].

*  [[Angelo Vistoli]], _Grothendieck topologies, fibered categories and descent theory_ [MR2223406](http://www.ams.org/mathscinet-getitem?mr=2223406); [math.AG/0412512](http://arxiv.org/abs/math/0412512) pp. 1--104 in Barbara Fantechi, Lothar G&#246;ttsche, Luc Illusie, Steven L. Kleiman, Nitin Nitsure, Angelo Vistoli, _Fundamental algebraic geometry. Grothendieck's [[FGA explained]]_, Mathematical Surveys and Monographs __123__, Amer. Math. Soc. 2005. x+339 pp. [MR2007f:14001](http://www.ams.org/mathscinet-getitem?mr=2007f:14001)  


A [[model category]] structure on [[presheaves of groupoids]], presenting stacks, by a [[Bousfield localization of model categories|localization]] of a [[model structure on simplicial presheaves]] (modeling [[∞-stacks]] before localization) is discussed in

* [[John F. Jardine]], _Stacks and the homotopy theory of simplicial sheaves_, Homology, Homotopy and Applications, vol. 3 (2), 2001, pp.361--384 ([euclid:hha/1139840259](https://projecteuclid.org/euclid.hha/1139840259))

* {#Hollander01} [[Sharon Hollander]], _A homotopy theory for stacks_, Israel Journal of Mathematics, 163(1), 93-124  (2008) ([arXiv:math.AT/0110247](http://arxiv.org/abs/math.AT/0110247), [doi:10.1007/s11856-008-0006-5](https://doi.org/10.1007/s11856-008-0006-5))

[[!redirects stack*]]
[[!redirects stacks]]