
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[space]] $X$ is called **formally smooth** if every [[morphism]]s $Y \to X$ into it has all possible [[infinitesimal object|infinitesimal]] extensions.

(If there is at most one extension per infinitesimal extension of $Y$ with no guarantee of existence it is called a [[formally unramified morphism]]. If the thickenings exist uniquely, it is called a [[formally etale morphism]]).


Traditionally this has considered in the context of [[geometry]] over formal duals of [[ring]]s and [[associative algebra]]s. This we discuss in the section ([Concrete notion](#ConcreteNotion)). But generally the notion makes sense in any context of <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a>. This we discuss in the section 
[General abstract notion](#GeneralAbstractNotion).

## General abstract notion
 {#GeneralAbstractNotion}

### Definition

Let 

$$
  \mathbf{H}
   \stackrel{\overset{u^*}{\hookrightarrow}}{\stackrel{\overset{u_*}{\leftarrow}}{\underset{u^!}{\to}}}
  \mathbf{H}_{th}   
$$

be a triple of [[adjoint functor]]s with $u^*$ a [[full and faithful functor]] that preserves the [[terminal object]]. 

We may think of this as exhibiting <a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#InfinitesimalCohesion">infinitesimal cohesion</a> (see there for details, but notice that in the notation used there we have $u^* = i_!$, $u_* = i^*$ and $u^! = i_*$). 

We think of the objects of $\mathbf{H}$ as [[cohesive topos|cohesive space]]s and of the objects of $\mathbf{H}_{th}$ as such cohesive spaces possibly equipped with [[infinitesimal object|infinitesimal extension]]. 

As a class of examples that is useful to keep in mind consider a [[Q-category]] $(cod \dashv \epsilon \dashv dom) : \bar A \to A$  of <a href="http://nlab.mathforge.org/nlab/show/Q-category#InfinitesimalThickening">infinitesimal thickening of rings</a> and let

$$
  ((u^* \dashv u_* \dashv u^!) : \mathbf{H}_{th} \to \mathbf{H}) := 
  ([dom,Set] \dashv [\epsilon, Set] \dashv [codom,Set] : [\bar A, Set] \to [A,Set])
$$ 

be the corresponding <a href="http://nlab.mathforge.org/nlab/show/Q-category#PresheafQCategory">Q-category of copresheaves</a>.

For any such setup there is a canonical [[natural transformation]]

$$
  u^* \to u^!
  \,.
$$

Details of this are in the section <a href="http://ncatlab.org/nlab/show/cohesive%20topos#AdjointQuadruples">Adjoint quadruples</a> at [[cohesive topos]].

From this we get for every morphism $f : X \to Y$ in $\mathbf{H}$ a canonical morphism

\[
  \label{MorphismIntoPullback}
  u^* X \to u^* Y \prod_{u^! Y} u^! X
  \,.
\]

+-- {: .num_defn #AbstractFormallySmoothMorphism}
###### Definition

A morphism $f : X \to Y$ in $\mathbf{H}$ is called **formally smooth** if (eq:MorphismIntoPullback) is an [[effective epimorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.1, prop. 5.3.1.1](#KontsevichRosenbergSpaces)).

The dual notion, where the above morphism is a [[monomorphism]] is that of [[formally unramified morphism]]. If both conditions hold, hence if the above morphism is an [[isomorphism]], one speaks of a [[formally  étale morphism]].

+-- {: .num_defn #AbstractFormallySmoothObject}
###### Definition

An object $X \in \mathbf{H}$ is called **formally smooth** if the morphism $X \to *$ to the [[terminal object]] is formally smooth.

=--

+-- {: .num_prop #AbstractFormallySmoothObjectDirect}
###### Proposition

The object $X$ is formally smooth precisely if 

$$
  u^* X \to u^! X
$$

is an [[effective epimorphism]].

=--

This appears as ([KontsevichRosenberg, def. 5.3.2](#KontsevichRosenbergSpaces)).

### Properties

+-- {: .num_prop}
###### Proposition

Formally smooth morphisms are closed under composition.

=--

This appears as ([KontsevichRosenberg, prop. 5.4](#KontsevichRosenbergSpaces)).


## Concrete notion
 {#ConcreteNotion}




### Over commutative rings 
 {#OverCommutativeRings}

Let $k$ be a [[field]] and let $CAlk_k$ be the [[category]] of commutative 
[[associative algebra]]s over $k$. Write

$$
  \mathbf{H} = [CAlg_k, Set]
$$

for the [[presheaf topos]] over the [[opposite category]] $CAlg_k^{op}$. This is the context in which [[scheme]]s and [[algebraic space]]s over $k$ live.

+-- {: .num_defn #CFormalSmoothness}
###### Definition


A morphism $f :X\to Y$ in $\mathbf{H} = [CAlg_k, Set]$ is __formally smooth__ if   it satisfies the _infinitesimal lifting property_: for every algebra $A$ and nilpotent [[ideal]] $I\subset A$ and morphism $Spec(A)\to Y$ the induced map

$$ Hom_Y(Spec(A), X)\to Hom_Y(Spec(A/I),X)$$

is surjective. 

=--

This is due to ([[EGAIV]]${}_4$ 17.1.1)

+-- {: .num_prop #AbstractAndConcreteCommutativeFormallySmoothCoincidesOnObjects}
###### Proposition

An object $X \in [CAlg_k, Set]$ is formally smooth in the concrete sense of def. \ref{CFormalSmoothness} precisely if it is so in the abstract sense of def. \ref{AbstractFormallySmoothObjectDirect}.

=--

This appears as ([KontsevichRosenbergSpaces, 4.1](#KontsevichRosenbergSpaces)).

#### Smoothness versus formal smoothness 

For a morphism $f:X\to Y$ of schemes, and $x$ a point of $X$, the following are equivalent

(i) $f$ is a [[smooth morphism]] at $x$

(ii) $f$ is locally of finite presentation at $x$ and there is an open neighborhood $U\subset X$ of $x$ such that $f|_U: U\to Y$ is formally smooth

(iii) $f$ is flat at $x$, locally of finite presentation at $x$ and the sheaf of [[Kähler differential]]s $\Omega_{X/Y}$ is locally free in a neighborhood of $x$

The relative dimension of $f$ at $x$ will equal the rank of the module of K&#228;hler differentials. 

This is ([[EGAIV]]${}_4$ 17.5.2 and 17.15.15)


#### Formally smooth scheme 

A [[scheme]] $S$, i.e. a scheme over the ground ring $k$, is a [[formally smooth scheme]] if the corresponding morphism $S \to Spec(k)$ is a formally smooth morphism.

There is also an interpretation of formal smoothness via the formalism of [[Q-categories]].


### Over noncommutative algebras


Let $k$ be a [[field]] and let $Alg_k$ be the category of [[associative algebra]]s over $k$ (not necessarily commutative). Let

$$
  Alg_k^{inf} : \bar A \to Alg_k
$$

be the [[Q-category]] of <a href="http://ncatlab.org/nlab/show/Q-category#InfinitesimalThickening">infinitesimal thickenings</a> of $k$-algebras (whose objects are surjective $k$-algebra morphisms with nilpotent kernel).
Notice that the [[presheaf topos]] 

$$
  \mathbf{H} := [Alg_k, Set]
$$ 

is the context in which [[noncommutative scheme]]s live. Let $\mathbf{H}_{th} \to \mathbf{Q}$ be the <a href="http://ncatlab.org/nlab/show/Q-category#PresheafQCategory">copresheaf Q-category</a> over $Alg_k^{inf}$.


+-- {: .num_prop #NCFormalSmoothness}
###### Proposition

Let $f : R \to S$ be a morphism in $Alg_k$ such that $R$ is a [[separable algebra]]. Write $Spec f : Spec S \to Spec R$ for the corresponding morphism in $\mathbf{H} = [Alg_k, Set]$.

This $Spec f$ is formally smooth in the sense of def. \ref{AbstractFormallySmoothMorphism} precisely if the $S \otimes_k S^{op}$-[[module]]

$$
  \Omega^1_{S|R} := ker ( R \otimes_k R \stackrel{mult}{\to} R \stackrel{f}{\to} S)
$$

is a [[projective object]] in $S \otimes_k S^{op}$[[Mod]].


=--


In particular, setting $R = k$ we have that an object of the form $Spec S$ is formally smooth according to def. \ref{AbstractFormallySmoothObject} precisely if $\Omega^1(S|k)$ is projective. This is what in ([CuntzQuillen](#CuntzQuillen)) is called the condition for a [[quasi-free algebra]].

## Related concepts

**formally smooth morphism** and [[formally unramified morphism]] $\Rightarrow$ [[formally étale morphism]].


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