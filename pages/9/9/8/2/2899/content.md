This entry is about &#233;tale morphisms between [[scheme]]s. The word [[etale map|étale map]] is preffered in context of [[topology]] and [[differential geometry]], see [[étalé space]] for the topological version. 

#Contents#
* table of contents
{:toc}



## Definition

+-- {: .un_defn}
###### Definition

A [[morphism]] of [[schemes]] is an **&#233;tale morphism** if the following equivalent conditions hold

* it is

  * a [[smooth morphism of schemes|smooth morphism]] 

  * and it is of [[relative dimension]] $0$. 

1. it is 

   * [[flat morphism|flat]] 

   * and [[unramified]].  

=---

(A number of other equivalent definitions are listed at [wikipedia](http://en.wikipedia.org/wiki/Etale_morphism).)  


+-- {: .un_defn}
###### Definition

A collection of &#233;tale morphisms $\{U_i \to X\}$ that [[cover]] $X$ is called an [[étale cover]].

=--

There is a weaker notion of a formally &#233;tale morphism. 

+-- {: .un_defn}
###### Definition

A morphism is **formally &#233;tale** if it is 

* [[formally smooth]] (satisfying an infinitesimal lifting property) 

* and formally unramified. 

=--

+-- {: .un_defn}
###### Definition

These are sheaf-like properties, which can be formalized in the language of [[Q-categories]] ([[monopresheaf]] and [[epipresheaf]] properties on the $Q$-category of nilpotent thickenings). 

=--

## Properties


### Closure properties

* A [[composite]] of &#233;tale morphism is &#233;tale.

* The property of being &#233;tale is [[base change|preserved under pullbacks]] along any morphism of schemes. 

* A smooth map of schemes is &#233;tale iff there is an [[étale cover]] of the base  scheme by [[open subschemes]] such that the pullback of the projection to each of them is an open local isomorphism of [[locally ringed spaces]] (and in particular, the pullback of the projection morphism is an [[étalé space|étale map]] of the corresponding underlying topological spaces). 

  This disjointness picture of &#233;tale covers make them suitable for having nontrivial [[cohomology]] in situations where Zariski covers give vanishing cohomology.

### Classes of examples

+-- {: .un_prop}
###### Proposition

Let $k$ be a [[field]]. A morphism of [[scheme]]s $Y \to Spec k$ is &#233;tale precisely if $Y$ is a [[coproduct]] $Y \simeq \coprod_i Spec k_i$ for each $k_i$ a finite and separable [[field extension]] of $k$.

=--

This appears for instance as [de Jong, prop. 3.1 i)](#deJong). 

+-- {: .un_remark}
###### Remark

Such &#233;tale morphisms are classified by the classical [[Galois theory]] of field extensions.

=--


+-- {: .un_prop}
###### Proposition

A [[ring]] homomorphism $A \to B$ is &#233;tale precisely if  $B \simeq R[x_1, \cdots, x_n]/(f_1, \cdots, f_n)$ where 

* all the $f_i$ are [[polynomial]]s;

* the [[Jacobian]] $det(\frac{\partial f_i}{\partial x_j})$ is a unit in $S$.

=--

This appears for instance as [de Jong, prop. 3.1 ii)](#deJong).



### As locally constant sheaves {#AsLocallyConstantSheaves}

+-- {: .un_prop}
###### Proposition

A [[sheaf]] $F$ on a scheme $X$ corresponds to an &#233;tale morphism $Y \to X$ precisely if there is an [[étale cover]] $\{U_i \to X\}$ such that each restriction

$$
  F|_{U_i} \simeq LConst K_i
$$

is [[isomorphic]] to a [[constant sheaf]] on a [[set]] $K_i$.

=--

A proof is in ([Deligne](#Deligne)).



## Examples

* A finite separable [[field extension]] $K \hookrightarrow L$ corresponds dually to an &#233;tale morphism $Spec L \to Spec K$. These are the morphisms classified by classical [[Galois theory]].





## The &#233;tale sites

&#201;tale morphisms are used to define small and big [[etale site|étale sites]] and [[étale cohomology]]. 

## References

A classical reference is

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics, no. 569, Springer-Verlag, 1977.
{#Deligne}

Lecture notes are

* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}

[[!redirects etale morphism]]
[[!redirects étale morphism]]
[[!redirects etale morphism of schemes]]
[[!redirects étale morphism of schemes]]
[[!redirects formally etale morphism]]
[[!redirects formally étale morphism]]
