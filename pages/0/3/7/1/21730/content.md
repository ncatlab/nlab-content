

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea ##

A cofunctor is a kind of morphism between [[category|categories]] (not to be confused with a [[contravariant functor]]). In contrast to a [[functor]], the assignment on objects of a cofunctor goes in the _opposite_ direction to the assignment on morphisms. 

Cofunctors generalise both [[bijective on objects functor|bijective-on-objects functors]] and [[discrete fibration|discrete opfibrations]]. 

Cofunctors arise naturally in the study [[internal category in a monoidal category|non-cartesian internal categories]]. 

## Definition ##

A **cofunctor** $\varphi : A \nrightarrow B$ from a [[category]] $A$ to a category $B$ consists of a 
map sending each [[object]] $a \in A$ to an object $\varphi_{0}a \in B$ 
and a map sending each pair $(a \in A, u : \varphi_{0}a \to b \in B)$ to a [[morphism]] $\varphi_{1}(a, u) : a \to a'$ in $A$, where $a' = cod(\varphi_{1}(a, u))$, such that 

* $\varphi_{1}$ respects codomains: $\varphi_{0}a' = cod(u)$ where $a' = cod(\varphi_{1}(a, u))$, 

* $\varphi_{1}$ preserves identity morphisms: $\varphi_{1}(a, 1_{\varphi_{0}a}) = 1_{a}$, 

* $\varphi_{1}$ preserves composition: $\varphi_{1}(a, v \circ u) = \varphi_{1}(a', v) \circ \varphi_{1}(a, u)$ where $a' = cod(\varphi_{1}(a, u))$. 

\begin{centre}
\begin{tikzcd}
A
\arrow[d, "\varphi"', "/"{anchor=center,sloped}]
& a
\arrow[d, phantom, "\vdots"]
\arrow[r, "{\varphi_{1}(a, u)}"]
& a'
\arrow[d, phantom, "\vdots"]
\\
B
& \varphi_{0} a
\arrow[r, "u"]
& b = \varphi_{0}a'
\end{tikzcd}
\end{centre}

Given a pair of cofunctors $\varphi : A \nrightarrow B$ and $\gamma : B \nrightarrow C$, their composite cofunctor $\gamma \circ \varphi \colon A \nrightarrow C$ sends each object $a \in A$ to an object $\gamma_{0}\varphi_{0}a \in C$ 
and each pair $(a \in A, u : \gamma_{0}\varphi_{0}a \to c \in C)$ to a 
morphism $\varphi_{1}(a, \gamma_{1}(\varphi_{0}a, u))$ in $A$. 
This defines a category $\mathbf{Cof}$ whose objects are [[small category|small categories]], and whose morphisms are cofunctors. 

## Examples ##

* Every [[monoid]] [[homomorphism]] $A \to B$ yields a cofunctor $B \nrightarrow A$. There is a fully faithful functor $\mathbf{Mon} \to \mathbf{Cof}^{op}$.

* Every [[bijective on objects functor]] $A \to B$ yields a cofunctor $B \nrightarrow A$. 

* Every [[discrete fibration|discrete opfibration]] $A \to B$ yields a cofunctor $A \nrightarrow B$. 

* Every split [[Grothendieck fibration|Grothendieck opfibration]] has an underlying cofunctor given by the [[cleavage|splitting]]. 

* More generally, every [[delta lens]] has an underlying cofunctor. 

* Let $\mathbb{N}$ denote the [[monoid]] of [[natural numbers]] under addition. A cofunctor $\tau : A \to \mathbb{N}$ is the same as a choice of morphism $\tau(a, 1)$ out of every object in $a \in A$. 

## References ##

* {#HigginsMackenzie93} [[Philip J. Higgins]], [[Kirill C. H. Mackenzie]], _Duality for base-changing morphisms of vector bundles, modules, Lie algebroids and Poisson structures_, Mathematical Proceedings of the Cambridge Philosophical Society, 114, 1993 ([doi:10.1017/S0305004100071760](http://dx.doi.org/10.1017/S0305004100071760))

* {#Aguiar97} [[Marcelo Aguiar]], _Internal categories and quantum groups_, PhD thesis, Cornell University, 1997 ([pdf](http://pi.math.cornell.edu/~maguiar/thesis2.pdf))

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))

* {#Clarke20a} Bryce Clarke, _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} Bryce Clarke, _Internal split opfibrations and cofunctors_, Theory and Applications of Categories, 35, 2020 ([link](http://www.tac.mta.ca/tac/volumes/35/44/35-44abs.html))

