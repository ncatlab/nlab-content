
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

$\cdots \to$ **Fivebrane group** $\to$ [[string group]] $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]].

***

#Contents#
* autoamtic table of contents goes here
{:toc}

## Definition 

The **Fivebrane group** $Fivebrane(n)$  is defined to be, as a [[topological group]], the [[Whitehead tower|7-connected cover]] of the [[String group]] $String(n)$, for any $n \in \mathbb{N}$.

Notice that $String(n)$ itself if the 3-connected cover of $Spin(n)$,  which is itself is the [[Whitehead tower|simply connected cover]] of the [[special orthogonal group]] $SO(n)$, which in turn is the connected component (of the identity)  of the [[orthogonal group]] $O(n)$. Hence $Fivebrane(n)$ is one element in the [[Whitehead tower]] of $\mathrm{O}(n)$:

$$
  \cdots \to Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to \mathrm{O}(n)
  \,.
$$


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
     cokill this &&&& to get
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


## Further information... 


...should eventually go here. For the time being have a look at [[Fivebrane structure]].

## References

The term _fivebrane group_ and the role of this topological group in [[quantum anomaly]] cancellaton conditions in [[dual heterotic string theory]] was found by [[Hisham Sati]] and appeared in 


* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _Fivebrane structures_ , Reviews in Math. Phys. ([arXiv:0805.0564](http://arxiv.org/abs/0805.0564))

The term shortly after was picked up in

* [[Christopher Douglas]], [[André Henriques]], [[Michael Hill]], _Homological obstructions to string orientations_ ([arXiv:0810.2131](http://arxiv.org/abs/0810.2131))

[[!redirects fivebrane group]]