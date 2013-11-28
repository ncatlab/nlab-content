
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Introduction and motivation

Legend has it that there was a time when only three people understood general relativity. Whether true and in which sense, the point of the legend is: classical Einstein gravity was once considered enormously subtle and esoteric.

But one of the three was Hilbert, and he made the mists go away. He gave a clear mathematical axiomatization: classical Einstein gravity is the study of the critical points of the integral of the scalar curvature density functional on the space of pseudo-Riemannian manifolds.

Riemann made this a general principle: [[Riemann's 6th problem]] asks us to: mathematically axiomatize physics.

Due to this axiomatic formulation, today every beginning student understands general relativity. Mathematical axiomatization has made it easy. 

What has taken the place of the mysterious is instead now [[quantum field theory]]. According to Feynman, "nobody understand quantum mechanics". This is the next item in Hilbert's sixth problem to be solved. 

[[William Lawvere]] has worked his hole life on the problem of axiomatizin [[classical mechanics|classical]] [[continuum mechanics]].

We now follow his steps and then improve.


## Mapping spaces in gauge theory and General covariance 
 {#HigherMappingSpaces}

Lawvere's starting point was the observation that central to the formulation of physics is the existence of _[[mapping spaces]]_ which satisfy the [[exponential law]].

Indeed, generically a [[physical system]] is determined by 

* a [[space]] $\Sigma$ called [[spacetime]] or [[worldvolume]]

* a [[space]] $X$ called [[target space]] or [[field bundle]] etc.

Such that a [[trajectory]] or [[physical field|field configurations]] is a map

$$
  \Sigma \longrightarrow X
  \,.
$$

For instance $\Sigma = \mathbb{R}$ the abstract [[worldline]] and $X$ [[spacetime]], then $\Sigma \to X$ is the [[trajectory]] of a [[particle]] in [[spacetime]].

Hence the [[mapping space]] $[\Sigma,X]$ is the space of all trajectories, [[path space]] the domain of the infamous [[path integral]].

Lawvere observed that this not only needs to exist as a decent "space", it also needs to satisfy the axiom of an [[internal hom]]. Because if we split

$$
  \Sigma = \mathbb{R} \times \Sigma_{d-1}
$$

into [[space]] and [[time]], then we want that spacetime field configurations

$$
  \mathbb{R} \times \Sigma_{d-1} \longrightarrow X
$$

are the same as trajectories of fields on space

$$
  \mathbb{R}  \longrightarrow [\Sigma_{d-1}, X]
  \,.
$$

But acutally in physics one needs a bit more than this. Physics is fundamental governed by [[gauge equivalence]], which means that there is no sense in askking if field consigurations are equal, we must ask if they are [[equivalence|equivalent]].

A fundamental example of this is Einstein [[general covariance]].

This says that if 

$$
  s \;\colon\; U \hookrightarrow \Sigma
$$

is a region in spacetime, and $\phi \colon \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma$ is a [[diffeomorphism]], then

$$
  \phi^\ast s \;\colon\; U \hookrightarrow \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma
$$

is "the same" region. Stated this way in ordinary [[topos theory]] this is confusing, and historically it was confusing. This is essentially the famous "[[hole paradox]]".

But this is recolved in [[higher topos theory]]. Here a [[space]] $S$ is a [[groupoid]] or [[homotopy type]]. This means that it is not sensible to ask if two maps into it are equal, but between any two maps there is a space of equivalences between them.

For general covariance this means by the above that spacetime is not actually a manifold $\Sigma$, but is actually the [[action groupoid]]/[[quotient stack]]

$$
  \Sigma//Diff(\Sigma)
$$

This is [[general covariance]]. 


But now this means we also need to consider the [[mapping spaces]] in higher topos theory. A basic fact is

$$
  \left(
  \array{
    \Sigma &\longrightarrow& \Sigma//Diff(\Sigma)
    \\
    && \downarrow
    \\
    && \mathbf{B}Diff(\Sigma)
  }
  \right)
  \;\;
  \in
  \;\;
  \mathbf{H}_{/\mathbf{B}Diff(\Sigma)}
  \simeq Diff(\Sigma)Act(\mathbf{H})
  \,.
$$

Lawvere also introduced [[categorical logic]] and understood [[dependent product]] $\prod$ and [[dependent sum]] $\sum$ as [[base change]].

Using this we have the mapping space of fields


$$
  \mathbf{B}Diff(\Sigma)
  \;\;
   \vdash
  \;\;
   \left[
     \Sigma//Diff(\Sigma)
     \,,\;
      X
   \right]
$$

and 

Theorem: down in the absolute context 

$$
   \vdash
  \;\;
   \underset{\mathbf{B}Diff(\Sigma)}{\sum}
   \left[
     \Sigma//Diff(\Sigma)
     \,,\;
      X
   \right]
   \;\;
   \simeq
   \;\;
   [\Sigma, X]//Diff(\Sigma)
  \,.
$$

This is the famous insight of Einstein. Derived by lifting Lawvere's argument about mapping spaces from topos theory to higher topos theory.



## Toposes of laws of motion and Hamilton-Jacobi-Lagrange mechanics


In ([Lawvere 97](#Lawvere97)) it was observed that [[equations of motion]] in [[physics]] can (almost, see below) be formalized in [[synthetic differential geometry]] as follows.

Let $\mathbf{H}$ be an ambient [[smooth topos|synthetic differential]] [[topos]] (such as the [[Cahiers topos]] of [[smooth spaces]] and [[formal smooth manifolds]]).

The canonical [[line object]] $\mathbb{A}^1 = \mathbb{R}$ of this models the [[continuum]] line, the abstract [[worldline]]. Let

$$
  D \hookrightarrow \mathbb{R}
$$

be the inclusion of the first order [[infinitesimally thickened point|infinitesimal]] neighbourhood of the origin of $\mathbb{R}$ -- in the [[internal logic]] this is $D = \{x \in \mathbb{R}| x^2 = 0\}$, externally it is the [[spectrum of a commutative ring|spectrum]] of the [[ring of dual numbers]] over $\mathbb{R}$.

Then for $X \in \mathbf{H}$ any [[object]] which we are going to think of as a [[configuration space]] of a [[physical system]]. For instance if the system is a [[particle]] propagating on a [[spacetime]], then $X$ is that spacetime. Or $X$ may be the [[phase space]] of the system.

Accordingly the [[mapping space]] $[\mathbb{R}, X] \in \mathbf{H}$ is the [[smooth space|smooth]] [[path space]] of $X$. This is the space of potential [[trajectories]] of the [[physical system]].

If $X$ is thought of as [[phase space]], then every point in there determines a unique [[trajectory]] starting at that point. This means that time evolution is then an [[action]] of $\mathbb{R}$ on $X$. As $X$ here might be any space, we have the collection 

$$
  \mathbb{R}Act(\mathbf{H}) \in Topos
$$ 

of all $\mathbb{R}$-[[actions]] on objects in $\mathbf{H}$. This is again a [[topos]], and hence this is a first version of what one might call a _[[topos of laws of motion]]_.

On the other hand, if we think of $X$ as [[configuration space]], then it is (in the simplest but common case of [[physical systems]]) a [[tangent vector]] in $X$ that determines a [[trajectory]], hence a point in $[D,X]$. There is the canonical projection $[\mathbb{R},X] \longrightarrow [D,X]$ from the smooth [[path space]] to the [[tangent bundle]], which sends each path to its [[tangent vector]]/[[derivative]] at $0 \in \mathbb{R}$. A [[section]] of this map is hence an assignment that sends each tangent vector to a [[trajectory]] which starts out with this tangent. Specifying such a section is hence part of what it means to have [[equations of motion]] in [[physics]]. Accordingly in _[[Toposes of laws of motion]]_ [[Lawvere]] called the collection of such data a Galilian [[topos of laws of motion]].

Of course this is not quite yet what is actually used and needed in physics.  On p. 9 of ([Lawvere 97](#Lawvere97)) this problem is briefly mentioned:

> But what about actual dynamical systems in the spirit of [[Galileo]], for example, second-order ODE's? (Of course, the [[symplectic geometry|symplectic]] or [[Hamiltonian mechanics|Hamiltonian systems]] that are also much studied do address this question of states of [[becoming|Becoming]] versus locations of [[being|Being]], but in a special way which it may not be possible to construe as a topos;

It turns out that it does exist as a "[[higher topos theory|higher topos]]".

In _[[schreiber:Classical field theory via Cohesive homotopy types]]_ it is observed that if $\mathbf{H}$ to be not just a [[topos]] but an [[(infinity,1)-topos|infnity-topos]], then genuine [[classical mechanics]] governed by [[Hamilton's equations]] and [[Hamilton-Jacobi theory]] arises by actions of $\mathbb{R}$ on objects in the [[slice (infinity,1)-topos]] $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$, where $\mathbf{B}U(1)_{conn} \in \mathbf{H}$ is the [[moduli stack]] of [[circle group]]-[[principal connections]]. So

$$
  \mathbb{R}Act\left(
    \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
  \right)
$$

is actually a "topos of laws of motion" in the sense of Hamilton-Lagrange-Jacobi [[classical mechanics]]. For more on this see _[[Higher toposes of laws of motion]]_.






## Extensive/intensive duality and Cohomological quantization


...

[[intensive and extensive]] becomes [[motivic quantization]]

...


## Applications -- What is it all good for?

### Non-perturbative quantization of Poisson manifolds 

 [[higher geometric quantization of 2d Chern-Simons theory]]

[[symplectic groupoid]] of [[adjoint representation]] is 


universal [[orbit method]]


### Fine-structure of quantum anomaly cancellation in 2d QFT

The first thing to notice is that quantum field theory is
a subject richer than often realized. 

perturbation theory to nonperturbative

higher gauge fields in string theory

FDM: background RR+B field cocycle in twisted differential K-theory

was not available

BNV: realizable in stable cohesion.

Central for the discussion of 2d QFT. 
The infamous "[[landscape of string theory vacua]]" is essentially
the moduli space of certain 2d field theories satisfying consistency  conditions like this.



## References


* [[William Lawvere]] _[[Categorical dynamics]]_, 1967 Chicago lectures ([pdf](http://www.mat.uc.pt/~ct2011/abstracts/lawvere_w.pdf))

* [[William Lawvere]], _[[Toposes of laws of motion]]_, 1997
 {#Lawvere97}

* _[[schreiber:Classical field theory via Cohesive homotopy types]]_

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_

