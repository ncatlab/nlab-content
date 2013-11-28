
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

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

## References

The notion originates around

* [[William Lawvere]] _[[Categorical dynamics]]_, 1967 Chicago lectures ([pdf](http://www.mat.uc.pt/~ct2011/abstracts/lawvere_w.pdf))

and was made more explicit in 

* [[William Lawvere]], _[[Toposes of laws of motion]]_, 1997
 {#Lawvere97}



[[!redirects toposes of laws of motion]]

