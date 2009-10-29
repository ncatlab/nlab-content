#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

A _loop space_ is a [[loop space object]] in [[Top]].


#Definition#

Let $Top$ be a [[nice category of spaces|nice category of topological spaces]], in particular one which is [[complete category|complete]], [[cocomplete category|cocomplete]], and [[cartesian closed category|cartesian closed]]. Let $(S^1, pt)$ be the [[circle]], i.e., 1-dimensional [[sphere]], with chosen basepoint, and let $(X, *)$ be a space with a chosen [[pointed set|basepoint]]. Then the **loop space** of $X$ (at $*$) is an [[internal hom]] 

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

# Structure on loop spaces #

A loop space is an example of a [[homotopy-associative space]], or H-space. In fact, loop spaces admit a rich algebraic structure which arises from the fact that the based space $S^1$ carries a correspondingly rich co-algebraic structure, starting from the fact that the based space $S^1$ is an H-[[cogroup]]. 

An important theoretical consideration is when an H-space, and particularly one having the type of a [[CW-complex]], has the homotopy type of a loop space of another CW-complex: $X \simeq \Omega Y$. In this circumstance, one calls $Y$ a **[[delooping]]** of $X$; an important example is where $X$ carries a topological group structure $G$, and $Y$ is the [[classifying space]] of $G$. 

The most basic fact about deloopings is the shift in homotopy groups: 

* $\pi_n(\Omega Y) \cong \pi_{n+1}(Y)$ 

which follows straight from the adjunction $S \dashv \Omega$ plus the fact that the suspension of $S^n$ is $S^{n+1}$. (This isomorphism needs to be developed at greater length.) 

The modern study of the question "when can an H-space be [[delooping|delooped]]?" was inaugurated by [[Jim Stasheff]]. The basic theorem is as follows (all spaces assumed to be CW-complexes): 

+-- {: .un_theorem}
###### Theorem

An H-space $X$ admits a delooping if and only if the monoid $\pi_0(X)$ induced from the H-space structure is a group, and the H-space $X$ structure can be extended to a structure of algebra over the [[Stasheff operad]] $K$. 
=--

Very stubby article; much work remains. 

### Local homotopy properties of loop spaces ###

Let the space $X$ be [[locally connected space|locally 0-connected]] and [[semi-locally simply connected space|semi-locally 1-connected]] (i.e. it admits a [[universal covering space]]). The loop space $\Omega X$ for any basepoint is locally path connected, as is the free loop space $X^{S^1}$. If $X$ is locally 1-connected and admits a basis of open sets $U$ such that $\pi_2(U) \to \pi_2(X)$ is the zero map, then $\Omega X$ is locally 0-connected and semi-locally 1-connected, and so admits a universal covering space. 

In general, if $X$ is locally $n$-[[n-connected space|connected]], $\Omega X$ is locally $(n-1)$-connected. This process can obviously be iterated up to $n$ times, so that $\Omega^n X$ is locally 0-connected. This can be weakened to locally $(n-1)$-connected and semi-locally $n$-connected: this is just like the $n=1$ case but replacing $\pi_1$ with $\pi_n$ (as was done in the previous paragraph with $\pi_2$). We will actually define a space to be semi-locally $n$-connected to include the condition that it is locally $(n-1)$-connected

+--{: .standout}
[[David Roberts]]: The following claim is conjectural, but for $n=2$ it is in my thesis. $n=1$ has been known for ages - I don't know where it was first, but it is in Ronnie Brown's topology textbook.
=--

+-- {: .un_theorem}
###### Theorem

The fundamental $n$-groupoid of a space $X$ ([[Trimble n-category|Trimblean]] for choice) can be topologised to be an internal $n$-groupoid in $\Top$ when $X$ is semi-locally $n$-connected.
=--

[[!redirects loop spaces]]
