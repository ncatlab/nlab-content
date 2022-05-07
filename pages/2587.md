> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



#Contents#
* autoamtic table of contents goes here
{:toc}

## Definition

The **string group** $String(n)$  is defined to be, as a [[topological group]], the [[Whitehead tower|3-connected cover]] of the [[Spin group]] $Spin(n)$, for any $n \in \mathbb{N}$.

Notice that for $n\ge3$, $Spin(n)$ itself is the [[Whitehead tower|simply connected cover]] of the [[special orthogonal group]] $SO(n)$, which in turn is the connected component (of the identity)  of the [[orthogonal group]] $O(n)$. Hence $String(n)$ is one element in the [[Whitehead tower]] of $\mathrm{O}(n)$:

$$
  \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to \mathrm{O}(n)
  \,.
$$


The next higher connected group is called the [[Fivebrane group]].

The [[homotopy group]]s of $O(n)$ are for $k \in \mathbb{N}$ and for sufficiently large $n$

$$
  \array{
     \pi_{8k+0}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+1}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+2}(O) & = 0
     \\
     \pi_{8k+3}(O) & = \mathbb{Z}
     \\
     \pi_{8k+4}(O) & = 0
     \\
     \pi_{8k+5}(O) & = 0
     \\
     \pi_{8k+6}(O) & = 0
     \\
     \pi_{8k+7}(O) & = \mathbb{Z}
  }
  \,.
$$

By [[Whitehead tower|co-killing]] these groups step by step one gets

$$
  \array{
     cokill~this &&&& to~get
     \\
     \\
     \pi_{0}(O) & = \mathbb{Z}_2 &&& SO
     \\
     \pi_{1}(O) & = \mathbb{Z}_2 &&& Spin
     \\
     \pi_{2}(O) & = 0
     \\
     \pi_{3}(O) & = \mathbb{Z} &&& String
     \\
     \pi_{4}(O) & = 0
     \\
     \pi_{5}(O) & = 0
     \\
     \pi_{6}(O) & = 0
     \\
     \pi_{7}(O) & = \mathbb{Z} &&& Fivebrane
  }
  \,.
$$


## Definition by co-killing of $\pi_3$ 

More in detail this means the following.

First notice that since by construction $\pi_i(\mathcal{B}Spin(n)) = 0 $ for $0 \leq i \leq 3$, by the [[Hurewicz theorem]] we have for the degree 4 [[integral cohomology]] group of the [[classifying space]] $B Spin(n)$ that

$$
  H^4(B Spin(n)) \simeq \pi_4(B Spin(n))
  \simeq
  \mathbb{Z}
  \,.
$$

The generator of this group is called the **fractional first Pontryagin class** and denoted 

$$
  \frac{1}{2}p_1 : B Spin(n) \to B^4 \mathbb{Z} \simeq K(\mathbb{Z},4)
$$ 

because the ordinary first [[Pontryagin class]] $p_1 : \mathcal{B} SO(n) \to K(\mathbb{Z},4)$ fits into a diagram

$$
  \array{
    B Spin(n) &\stackrel{\frac{1}{2} p_1}{\to}&
    B^4 \mathbb{Z}
    \\
    \downarrow && \downarrow^{\cdot 2}
    \\
    B SO(n) &\stackrel{p_1}{\to}&
    B^4 \mathbb{Z}
  }
  \,,
$$

where the right vertical morphism comes from multiplication by 2 in $\mathbb{Z}$.

This says that _after being pulled back_ to $\mathcal{B} Spin(n)$ the first [[Pontryagin class]] is 2 times the generator of the degree 4 [[integral cohomology]] group of $\mathcal{B}Spin(n)$ and hence that generator is called one half of $p_1$, denoted $\frac{1}{2}p_1$ (by slight abuse of notation). 

The [[delooping]] of the String-group as a [[topological group]] is the [[homotopy fiber]] of this fractional Pontyagin class, i.e. the [[homotopy pullback]]

$$
  \array{
    B String(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    B Spin(n) &\to& \mathcal{B}^4 \mathbb{Z}
  }
$$

in [[Top]].


In other words: $B String(n)$ is the $U(1)$- 2-[[gerbe]] or $B^2 U(1)$ [[principal ∞-bundle]] on $B Spin(n)$ whose class is $\frac{1}{2}p_1 \in H^4(B Spin(n), 4)$.


## Models 

### As a topological group 

There is a model due to Stolz and Teichner in 'What is an elliptic object?'...



### As a smooth 2-group 

While $Spin(n)$ is not just a [[topological group]] but a (finite dimensional) [[Lie group]], $String(n)$ cannot have the structure of a finite dimensional [[Lie group]], due to the fact that the third [[homotopy group]] is nontrivial for every (finite dimensional) Lie group, while for $\pi_3(String(n)) = 0$ by the very definition of $String(n)$.

However, one can define an _infinite-dimensional_ Lie group with the correct properties to be a model of $String(n)$ ([Nikolaus-Sachse-Wockel 2013](#NikolausSachseWockel)).

There are also smooth models of $String(n)$ in the form of [[2-group]]s. See [[string 2-group]].

## Role in string theory


The reason for the name is that in [[string theory]], for (blah) to be well-defined, it is necessary for the 
structure group of (blah) to lift to (blah). 

See [[String structure]].

If one considers passing to the (free) [[loop space]] of spacetime and then doing [[quantum mechanics]], the requirement of the previous paragraph is that the structure group lifts to ... (cite Killingback, Mickelsson, Schreiber, Witten,...) 

## Generalization to other groups

One may consider the universal 3-connected cover of any general [[compact space|compact]], [[simple Lie group|simple]] and [[simply connected space|simply connected]] [[Lie group]] $G$, in complete analogy to the case $G = Spin(n)$. Accordingly one speaks of string-groups $String_G$.

Of these the case $G = $ [[E8]] is the other one relevant in [[string theory]]: see [[Green-Schwarz mechanism]].

## Related concepts

$\cdots \to$ [[Fivebrane group]] $\to$ **string group** $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]].

[[!include image of J -- table]]


* [[string orientation of tmf]]

[[!include table of orthogonal groups and related]]

## References 


Originally the String-group was just known by its generic name: with $\mathcal{B} O \langle 8 \rangle$ being the topologist's notation for the [[n-connected|7-connected]] cover of the [[delooping]]/[[classifying space]] $\mathcal{B}O$ of the group $O$.

When it was realized that lifts of the structure maps $X \to \mathcal{B}O$ of the [[tangent bundle]] of a [[manifold]] $X$ through the projection $\mathcal{B}O\langle 8 \rangle \to \mathcal{B}O$ -- now called a [[String structure]] -- play the same role in [[string theory]] as a [[Spin structure]] does in ordinary [[quantum mechanics]], the term _String group_ for $\Omega (\mathcal{B}O\langle 8 \rangle)$ was suggested.

Following some inquiries by [[Jim Stasheff]] and confirmed in private email by [[Haynes Miller]] it seems that the first one to propose the term _$String$ group_ for the group known to topologists as $\Omega (\mathcal{B}O\langle 8\rangle)$ was [[Haynes Miller]].

A model of the string group by [[local nets]] of fermions is discussed in

* [[Stefan Stolz]], [[Peter Teichner]], _The spinor bundle on loop space_ (2005) ([pdf](http://web.me.com/teichner/Math/Surveys_files/MPI.pdf))

Many more models exist by now in terms of [[geometric realization]] of a model for the [[string 2-group]]. See there for more references.

A good review is in the introduction of

* [[Chris Schommer-Pries]], _Central Extensions of Smooth 2-Groups and a Finite-Dimensional String 2-Group_ ([arXiv:0911.2483](http://arxiv.org/abs/0911.2483))
{#Schommer-Pries}

In 

* {#NikolausSachseWockel} [[Thomas Nikolaus]], [[Christoph Sachse]], [[Christoph Wockel]], _A Smooth Model for the String Group_, Int. Math. Res. Not. IMRN 16 (2013) 3678-3721, doi:[10.1093/imrn/rns154](https://dx.doi.org/10.1093/imrn/rns154), ([arXiv:1104.4288](http://arxiv.org/abs/1104.4288))

it is shown that the topological string group does admit a [[Frechet manifold]] [[Lie group]] structure. 

For relation to [[conformal nets]] see

* Bas Janssens, _Notes on Defects & String Group_ ([pdf](http://www.bjadres.nl/WorkInProgress/Defect&String.pdf))

[[!redirects String group]]