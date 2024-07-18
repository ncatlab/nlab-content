
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Mapping space
+-- {: .hide}
[[!include mapping space - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In the strict sense of the word a _loop space_ in [[topology]] for a given [[pointed topological space]] $X$ is the [[mapping space]] (with its [[compact-open topology]], see the example [there](compact-open+topology#LoopSpace)) $Maps_\ast(S^1, X)$ of [[continuous functions]] from the [[circle]] to $X$, such that they take the given basepoint of the circle to the prescribed basepoint in $X$ (or if one drops this condition, then one speaks of the _[[free loop space]]_). One such continuous function may be thought of as a continuous loop in $X$, and hence the mapping space is the space of all these loops.

If here $X$ is equipped with further structure, such as [[smooth structure]] (e.g. a [[smooth manifold]]), then one may in good cases find such extra structure also on the loop space, for instance to form a _[[smooth loop space]]_, etc. See at _[[manifolds of mapping spaces]]_ for more on this.

If one regards this construction not in [[point-set topology]] but in [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] ([[homotopy hypothesis|equivalently]] [[∞Grpd]]), then, up to [[weak homotopy equivalence]], the loop space is equivalent to the [[homotopy fiber product]] of the basepoint inclusion $\ast \to X$ along itself.




## Definition

Let [[Top]] be a [[nice category of spaces|nice category of topological spaces]], in particular one which is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[cartesian closed category|cartesian closed]]. Let $(S^1, pt)$ be the [[circle]], i.e., 1-dimensional [[sphere]], with chosen basepoint, and let $(X, *)$ be a space with a chosen [[pointed set|basepoint]]. Then the **loop space** of $X$ (at $*$) is an [[internal hom]] 

$$\Omega X = hom((S^1, pt), (X, *))$$

in the category $Top_*$ of based spaces. Explicitly, it is given by the [[pullback]] in $Top$ 

$$\array{
\Omega X & \to & 1\\ 
 \downarrow & & \downarrow *\\
X^{S^1} & \underset{X^{pt}}{\to} & X^1
}$$

(using [[exponential object|exponentials]] to denote internal homs in $Top$), in other words the [[function set|function space]] of basepoint-preserving maps $S^1 \to X$, whose basepoint is the constant map $S^1 \to X$ at the basepoint of $X$.  

The category $Top_*$ is [[symmetric monoidal category|symmetric]] monoidal [[monoidal closed category|closed]]; its monoidal product is called the **[[smash product]]**, often denoted $\wedge$. In particular, the loop space functor 

$$\Omega = hom((S^1, pt), -): Top_* \to Top_*$$ 

has a [[left adjoint]] obtained by taking smash product with $(S^1, pt)$. This left adjoint $S: Top_* \to Top_*$ is called the **[[suspension]] functor**. Explicitly, the suspension $S X$ is formed as the [[pushout]] 

$$\array{
 & 1 \times X + S^1 \times 1& \to & 1\\
(pt \times X, S^1 \times *) & \downarrow & & \downarrow \\
 & S^1 \times X & \to & S X
}$$ 

with basepoint provided by the right vertical arrow. 


## Properties

### Homotopy-associative structure
 {#AInfinityStructure}

A loop space is an example of a [[A-∞ space]], in particular it is an [[H-space]]. Loop spaces admit this rich algebraic structure which arises from the fact that the based space $S^1$ carries a correspondingly rich co-algebraic structure, starting from the fact that the based space $S^1$ is an H-[[cogroup]]. 

The description of this structure on loop spaces has been the very motivation for the introduction of the notion of [[operad]] and [[algebra over an operad]] in ([May](#May)).


An important theoretical consideration is when an H-space, and particularly one having the type of a [[CW-complex]], has the homotopy type of a loop space of another CW-complex: $X \simeq \Omega Y$. In this circumstance, one calls $Y$ a **[[delooping]]** of $X$; an important example is where $X$ carries a [[topological group]] structure $G$, and $Y$ is the [[classifying space]] of $G$. 

The most basic fact about deloopings is the shift in [[homotopy group]]s: 

* $\pi_n(\Omega Y) \cong \pi_{n+1}(Y)$ 

which follows straight from the [[adjunction]] $S \dashv \Omega$ plus the fact that the suspension of $S^n$ is $S^{n+1}$. (This isomorphism needs to be developed at greater length.) 

The modern study of the question "when can an H-space be [[delooping|delooped]]?" was inaugurated by [[Jim Stasheff]]. The basic theorem is as follows (all spaces assumed to be CW-complexes): 

+-- {: .num_theorem}
###### Theorem

An [[H-space]] $X$ admits a delooping if and only if the [[monoid]] $\pi_0(X)$ induced from the H-space structure is a [[group]], and the H-space $X$ structure can be extended to a structure of [[algebra over an operad]] over [[Jim Stasheff|Stasheff]]'s [[A-∞ operad]] $K$.
=--

This is due to ([Stasheff](#Stasheff)). The analogous statement holds true in every [[(∞,1)-topos]] other than [[Top]]. Details on this more general statement are at [[loop space object]] and at [[groupoid object in an (∞,1)-category]].


### Local homotopy properties ###

Let the space $X$ be [[locally connected space|locally 0-connected]] and [[semi-locally simply connected space|semi-locally 1-connected]] (i.e. it admits a [[universal covering space]]). The loop space $\Omega X$ for any basepoint is locally path connected, as is the free loop space $X^{S^1}$. If $X$ is locally 1-connected and admits a basis of open sets $U$ such that $\pi_2(U) \to \pi_2(X)$ is the zero map, then $\Omega X$ is locally 0-connected and semi-locally 1-connected, and so admits a universal covering space. 

In general, if $X$ is locally $n$-[[n-connected space|connected]], $\Omega X$ is locally $(n-1)$-connected. This process can obviously be iterated up to $n$ times, so that $\Omega^n X$ is locally 0-connected. This can be weakened to locally $(n-1)$-connected and semi-locally $n$-connected: this is just like the $n=1$ case but replacing $\pi_1$ with $\pi_n$ (as was done in the previous paragraph with $\pi_2$). We will actually define a space to be semi-locally $n$-connected to include the condition that it is locally $(n-1)$-connected. This result was proved for more general mapping spaces $X^P$ and various subspaces when $X$ is Hausdorff and $P$ a finite [[polyhedron]] in ([Wada](#Wada)) but a much simpler and direct proof for general $X$ and $P = I$ or $P= S^1$ is possible.

+-- {: .un_theorem}
###### Conjecture

The fundamental $n$-groupoid of a space $X$ ([[Trimble n-category|Trimblean]] for choice) can be topologised to be an internal $n$-groupoid in $\Top$ when $X$ is semi-locally $n$-connected. Furthermore, the homotopy groups of the $n$-groupoid, _a priori_ topological groups, are discrete.
=--

For $n=2$, this is in [[David Roberts]]\'s [[Fundamental Bigroupoids and 2-Covering Spaces|thesis]].  For $n=1$, it has been known for ages and is in [[Ronnie Brown]]\'s topology textbook.

### Homology of loop spaces

See at _[[homology of loop spaces]]_.

## Models

There is a [[Quillen equivalence]]

$$
  (G \dashv \bar W) 
   \;\colon\; 
  sGrp
   \stackrel{\overset{\Omega}{\leftarrow}}{\underset{\bar W}{\to}}
  sSet_0
$$

between the [[model structure on simplicial groups]] and the [[model structure on reduced simplicial sets]], thus exhibiting both of these as models for [[infinity-groups]] ([Kan 58](#Kan58)). Its [[left adjoint]] $G$, the _[[simplicial loop space]] construction_, is a concrete model for the loop space construction with values in [[simplicial groups]].

See also [[simplicial group]] and [[groupoid object in an (∞,1)-category]] for more details.


## Related concepts

* [[path space]]

* [[loop space object]], [[free loop space object]]

  [[loop space type]]
  
  * [[Sullivan model of loop space]]

  * [[delooping]], [[looping and delooping]]

  * **loop space**, [[free loop space]], 

  * [[relative loop space]]

  * [[iterated loop space]]

  * [[infinite loop space]]

  * [[formal loop space]]

  * [[derived loop space]]

  * [[smooth loop space]]

  * [[loop space of a wedge of circles]]


* [[caloron correspondence]]

* [[suspension object]]

  * [[suspension]]

[[!include k-monoidal table]]

* [[A-infinity space]], [[model structure for dendroidal Cartesian fibrations]]

## References

### General

* {#Kan58} [[Daniel Kan]], _On homotopy theory and c.s.s. groups_, Ann. of Math. 68 (1958), 38-53

* {#Stasheff} [[Jim Stasheff]], _Homotopy associative $H$-spaces I, II_, Trans. Amer. Math. Soc. 108, 1963, 275-312 

* {#May} [[Peter May]], _The geometry of iterated loop spaces_ Lecture Notes in Mathematics 271 (1970) ([pdf](http://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf))
 

* H. Wada, _Local connectivity of mapping spaces_, Duke Mathematical Journal, vol ? (1955) pp 419-425

The simplicial loop group functor is discussed in chapter V, section 5 of

* [[Paul Goerss]], [[Rick Jardine]], _Simplicial homotopy theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

See also the references at [[looping and delooping]].

### Examples
 {#ReferencesExamples}

On loop spaces of [[configuration spaces of points]]:


* [[Edward Fadell]], [[Sufian Husseini]], _The space of loops on configuration spaces and the Majer-Terracini index_, Topol. Methods Nonlinear Anal. Volume 11, Number 2 (1998), 249-271 ([euclid:tmna/1476842829](https://projecteuclid.org/euclid.tmna/1476842829))

* [[Fred Cohen]], [[Samuel Gitler]], _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Aguadé J., Broto C., [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))

* [[Fred Cohen]], [[Samuel Gitler]], _On loop spaces of configuration spaces_, Trans. Amer. Math. Soc. __354__ (2002), no. 5, 1705&#8211;1748, ([jstor:2693715](https://www.jstor.org/stable/2693715), [MR2002m:55020](http://www.ams.org/mathscinet-getitem?mr=1881013))

  (on [[ordinary homology]] of [[loop spaces]] of configuration spaces)



[[!redirects loop space]]
[[!redirects loop spaces]]

[[!redirects based loop space]]
[[!redirects based loop spaces]]

[[!redirects based loop]]
[[!redirects based loops]]

