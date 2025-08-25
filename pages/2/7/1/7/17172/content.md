


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


# Contents 
* table of contents 
{:toc}

## Idea 

Dehn surgery is a method for constructing one [[manifold]] from another, especially one [[3-manifold]] from another, by a kind of cut-and-paste procedure. 

## Method 

A standard application of Dehn surgery is [[surgery]] along a [[link]] $L$ in a [[3-sphere]] $S^3$. This works in two steps (whose description makes it sound like *Zahn* surgery[^1]): 

[^1]: Yes, that's supposed to be a little joke. 'Zahn' here is the German word. 

* Form the [[complement]] in the [[3-sphere]] of a [[tubular neighborhood]] of the [[embedding of topological spaces|embedded]] [[link]] $L \hookrightarrow S^3$, of the form $L \times int(D^2)$. This is called *Dehn drilling*. The result is a 3-[[manifold with boundary]] $M$, whose [[boundary]] $\partial M \cong L \times S^1$ can be viewed as the boundary of a [[disjoint union]] of [[solid tori]] $L \times D^2$. 

* To each of the [[connected components]] $C_1, \ldots, C_n$ of $\partial M$, apply an (orientation-preserving) [[homeomorphism]], say $\phi_1, \ldots, \phi_n$. The [[union]] $\phi_1 \cup \ldots \cup \phi_n$ is a homeomorphism $\phi: \partial M \to \partial M$. Then perform a *Dehn filling* by constructing the [[pushout]] of an evident [[span]]: 
$$
  \array{
    \partial M
    &
    \overset{\phi}{\longrightarrow}
    & \partial M 
    \\ 
    \mathllap{incl} 
    \downarrow 
    & & 
    \downarrow 
    \mathrlap{incl}
    \\
    M 
    &
    & 
    L \times D^2,
  }
$$ 
thus refilling the drilled portion, but in a new way (along $\phi$). This gives a new [[3-manifold]] $N$. 

Some further notes: the surgery can be done one [[solid torus]] at a time. A homeomorphism on a boundary torus $S^1 \times S^1$ sends a meridian $S_1 \times \{1\}$ to some simple closed curve that is homotopic to a curve of rational slope $p/q$ (the curve which is the image of the line $y = (p/q)x$ in $\mathbb{R}^2$ under the quotient map $\mathbb{R}^2 \to \mathbb{R}^2/\mathbb{Z}^2 \cong S^1 \times S^1$). It turns out that the result of the surgery depends, up to homeomorphism, only on the quantity $p/q$, called a *surgery coefficient*. If all the surgery coefficients are [[integers]], we speak of an *integral surgery*. 

Put a bit different: given a [[framed link]] in an [[orientation|oriented]] 3-manifold like $S^3$, an integral surgery drills out a solid torus, [[Dehn twist|twists]] it an integral number of times according to the framing, and then reattaches it. 

## Results 

+-- {: .num_theorem} 
###### Theorem 
**(Lickorish-Wallace)** 
Every [[connected space|connected]] [[orientation|oriented]] [[closed manifold|closed]] [[3-manifold]] $N$ arises by performing an integral Dehn surgery along a [[link]] $L \hookrightarrow S^3$ (i.e., surgery along a framed link). 
=-- 


## Related concepts

* [[Kirby calculus]]

* [[surgery theory]]



## References 

### General

Named after [[Max Dehn]].

See also:

* Wikipedia, _[Dehn surgery](https://en.wikipedia.org/wiki/Dehn_surgery)_

### In Chern-Simons theory

Relation between [[Dehn surgery]] and [[Wilson loop observables]] in [[Chern-Simons theory]]:

* E. Guadagnini, _Surgery rules in quantum Chern-Simons field theory_, Nuclear Physics B
Volume 375, Issue 2, 18 May 1992, Pages 381-398 (<a href="https://doi.org/10.1016/0550-3213(92)90037-C">doi:10.1016/0550-3213(92)90037-C</a>)

* Boguslaw Broda, _Chern-Simons theory on an arbitrary manifold via surgery_ ([arXiv:hep-th/9305051](https://arxiv.org/abs/hep-th/9305051))




 

[[!redirects Dehn surgeries]]
