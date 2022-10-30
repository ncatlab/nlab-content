
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

This entry is about &#233;tale morphisms between [[schemes]]. The term _[[étale map]]_ is preferred in the context of [[topology]] and [[differential geometry]], see [[étalé space]] for the topological version. 

#Contents#
* table of contents
{:toc}



## Definition

+-- {: .un_defn}
###### Definition

A [[morphism]] of [[schemes]] is an **&#233;tale morphism** if the following equivalent conditions hold

1. it is

   1. [[smooth morphism of schemes|smooth]] 

   1. of [[relative dimension]] $0$. 

1. it is 

   1. [[flat morphism|flat]] 

   1. [[unramified]];

1. it is

   1. [[formally étale morphism|formally étale]];

   1. [[locally of finite presentation]]

=---

(A number of other equivalent definitions are listed at [wikipedia](http://en.wikipedia.org/wiki/Etale_morphism).)  


+-- {: .un_defn}
###### Definition

Jointly surjective collection of &#233;tale morphisms $\{U_i \to X\}$ is called an [[étale cover]].

=--

There is a weaker notion of a [[formally étale morphism]]. 

+-- {: .un_defn}
###### Definition

A morphism is **[[formally étale morphism]]** if it is 

* [[formally smooth]] (satisfying an infinitesimal lifting property) 

* and [[formally unramified]]. 

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





## Related concepts

* [[étale morphism]]

* **&#233;tale morphism of schemes**

  * [[étale site]], [[étale cohomology]]

  * [[étale (∞,1)-site]]

## References

The classical references are

* [[Pierre Deligne]] et al., _Cohomologie &#233;tale_ , Lecture Notes in Mathematics, no. 569, Springer-Verlag, 1977.
{#Deligne}

* [[James Milne]], _Etale cohomology_, Princeton Mathematical Series __33__, 1980. xiii+323 pp.

Lecture notes are

* [[James Milne]], _Lectures on etale cohomology_ ([pdf](http://www.jmilne.org/math/CourseNotes/LEC.pdf))

* [[Aise Johan de Jong]], _&#201;tale cohomology_ ([pdf](http://math.columbia.edu/~pugin/Teaching/Etale_files/EtaleCohomology.pdf))
{#deJong}

[[!redirects étale morphism of schemes]]

[[!redirects etale morphisms of schemes]]
[[!redirects étale morphisms of schemes]]
