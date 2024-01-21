

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea


In [[mathematics]] it happens at times that one and the same concept is given two different names to indicate a specific perspective, a certain attitude as to what to do with such objects. 

## Examples

### Series

A _[[series]]_ is just a [[sequence]].

But one says _series_ instead of _sequence_ when one is interested in studying its partial [[sums]]. In particular it means something different to say that a series _converges_ than to say that a sequence converges. The series $n\mapsto a_n$ converges if and only if the sequence $n\mapsto \sum_{i\lt n}a_i$ converges. 

### Lists
 {#Lists}

A *[[list]]* is just a [[tuple]], but calling it a list indicates that one is interested in the operation of [[concatenation]] of lists. 

### Presheaves and copresheaves

A _[[presheaf]]_ is just a [[contravariant functor|contravariant]] [[functor]], analogous to how a [[copresheaf]] is just a [[covariant functor|covariant]] [[functor]].  

(More specifically, an "$S$-valued presheaf" is a contravariant functor with [[codomain]] a given [[category]] $S$; in modern [[category theory]] the "default" value of $S$ here is usually [[Set]].) 

But one says _presheaf_ instead of (set-valued) _contravariant functor_ when one is interested in studying its [[sheafification]], or even if one is just interested in regarding the [[category of functors]] with its structure of a [[topos]]: the [[presheaf topos]].

### Sieves
 {#Sieve}

A *[[sieve]]* is just a [[subfunctor]] of a [[representable functor]], but calling them "sieves" serves to indicate that (mostly) one is interested in regarding these as *[[covers]]* of a [[Grothendieck topology]] or [[coverage]], making the ambient [[category]] into a [[site]].
 
### Young diagrams

A *[[Young diagram]]* is a [[partition]] that wants to become a [[Young tableau]].

### Quivers

A _[[quiver]]_ is just a [[directed graph]] ([[pseudograph]], to be explicit). 

But one says _quiver_ instead of _directed graph_ when one is interested in studying _[[quiver representations]]_: [[functors]] from the [[free category]] on that graph to the [[category]] of [[finite-dimensional vector spaces]].


### Causal set
 {#CausalSet}

A *[[causal set]]* is just a [[partially ordered set]].

But one says *causal set* in order to indicate that one means to think of the [[elements]] of the [[poset]] as [[spacetime]] [[events]] and of the order-[[relation]] as given by [[causality]].
 
### Persistence modules
 {#PersistenceModule}

A *[[persistence module]]* is just a [[sequence]] of [[linear maps]] (or a [[zigzag]] of these, for [[zigzag persistence modules]]), but one says *persistence module* to indicate that one is interested in the [[persistence diagrams]] encoding this sequence.


### Fields (physics)
 {#FieldsInPhysics}

A _[[field (in physics)]]_ is just a [[section]] of a [[fiber bundle]]. 

But in [[mathematical physics]] one says _field_ instead of _section of a fiber bundle_ to indicate that one is going to consider a [[Lagrangian density]] on the corresponding [[jet bundle]] of the given [[fiber bundle]] (then called the _[[field bundle]]_ ) and study the induced [[classical field theory|classical]] or [[quantum field theory]]. 


### Random variables and estimators

Both [[random variable|random variables]] and estimators are almost always just [[real number|real valued]] [[measurable function| measurable maps]]. Though sometimes the former takes more general values in some [[Polish space]] instead.

But in [[probability theory]] a random variable is interpreted as a map from a _sample space_ to a _space of [[state|states]]_ which represents the observed outcomes or outcomes predicted by some model.
In contrast in [[statistics]] an estimator guesses or estimates a certain parameter associated to some random model.

### Tensor networks
  {#TensorNetworks}

A _[[tensor network]]_ is just a [[string diagram]] (i.e. [[Penrose notation]]).

But in discussion of the [[AdS/CFT correspondence in solid state physics]] one says _[[tensor network]]_ when regarding [[string diagrams]] as encoding [[quantum states]] in the [[Hilbert space]] which is the [[tensor product]] of all the external [[vertices]].

### Dynamical systems

A _[[dynamical system]]_ is just a set $S$ with a [[group]] [[action]] $f \colon G \times S \to S$. 

However, in dynamical systems theory, one takes the group $G$ to represent _time_, the set $S$ to represent the _space_ of the dynamical system, and the group action $f$ to represent the _laws of motion_ of this dynamical system. 


### Abstract rewriting systems
 {#AbstractRewritingSystems}

An *[[abstract re-writing system]]* is just a [[relation]] on some [[set]] $X$.

However, calling this relation an abstract rewriting system indicates that one is interested in studying the behaviour of chains of related elements $x \to x_1 \to x_2 \to \cdots$ (thought of as successive stages of [[rewriting]] $x$), for instance to see if they are [[confluent category|confluent]].


### Curves 

A _[[curve]]_ in $n$-dimensional [[Cartesian space]] is just a [[smooth function]] $r:\mathbb{R} \to \mathbb{R}^n$. 

However, in [[differential geometry]], one takes the function $r$ as defining a parameterization of a smooth curve.

### Flows of time

A _flow of time_ is just a set endowed with a [[strict partial order]].

However, in [[temporal logic]], a (point-based) [[model]] is a pair consisting of a flow of time and a valuation.

## Further examples
 {#FurtherExamples}

### Module objects
 {#ModuleObjects}

A [[module object]] in a [[monoidal category]] $C$ is just an [[action object]] over a [[monoid object]] in $C$. 

Typically one says "module object" to amplify a [[linear algebra|linear algebraic]] nature or intended meaning of such actions (which, for instance, would be lacking for a [[group action]] in [[Set]], but be present for an action of the corresponding [[group algebra]] in [[Vect]]).


### Subsets and predicates

In some [[foundations of mathematics]], a _[[subset]]_ of a set $S$ is just a _[[predicate]]_, a function with domain $S$ and codomain the class of [[truth values]] $\Omega$. 



\linebreak
\linebreak


[[!redirects concepts with an attitude]]