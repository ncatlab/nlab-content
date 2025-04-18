
#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

The concept of _causal set_ -- or *causet*, for short -- is a [[concept with an attitude]]: In itself it is just a [[partially ordered set]] (or *poset*, for short), but meant to be understood as a set of [[spacetime]] [[events]] subject to the [[relation]] of [[causality]].

As such, causal sets play a role in:

* **computer science**, where causal sets model [[concurrency|concurrent]] [[computations]]: there exists a morphism $a \to b$ in the poset if $a$ and $b$ are states of some machine and if operating the machine can take it from state $a$ to state $b$. A simple example would be type of computation which can be done in a single step $in \to out$, but which needs to be done on _two_ inputs of the same kind. The causal set modelling this situation is

  $$
    \left\lbrace
    \array{
       (in_1, in_2) &\to& (out_1, in_2)
       \\
       \downarrow && \downarrow
       \\
       (in_1, out_2) &\to& (out_1,out_2) 
    }
    \right\rbrace
  $$

* **[[relativistic field theory]]**, where every [[globally hyperbolic Lorentzian manifold|globally hyperbolic Lorentzian]] [[structure]] equips the [[underlying]] [[set]] of points in a [[manifold]] naturally with the structure of a causal set: there is a morphism from the point $x$ to the point $y$ in the manifold precisely if $y$ is in the _future_ of $x$, i.e. precisely if there exists a smooth path from $x$ to $y$ whose tangent vector is everywhere non-spacelike with respect to the Lorentzian metric. 
Moreover, the Lorentzian metric on a manifold can essentially  (need to dig out the details here, see discussion at [[smooth Lorentzian space]]) be reconstructed from this poset structure and from a _measure_. This has led to some attempts to use posets as a foundational concept for relativistic physics. 

  For more see [[smooth Lorentzian space]]

The only technical distinction between the notion of posets and that of causal sets is that for a causal set the [[interval|under-over category]]
$x\darr X\darr y$ for all objects $x$ and $y$ in the poset 
(the category of "two-step time evolution paths" from $y$ to $x$)
is required to be _finite_. This means these are required to have a [[finite set]] of objects (and hence necessarily, being a poset, a finite set of morphisms).



## Definition

A causal set, or **causet** is a [[partial order|poset]] $X$ such that for all objects $x,y$ the [[interval]] $[x,y] = \{z \mid x \le z \le y\}$ is finite.

## Related concepts

* [[causal structure]]

* [[causal order]]

* [[causal complement]], [[causal closure]]

* [[causal locality]], [[causal additivity]]

* [[causal perturbation theory]]

* [[time-ordered product]]

* [[S-matrix]]


## References

Discussion in [[relativistic field theory]] and [[quantum gravity]]:

* Nomaan X, *Quantum Field Theory On Causal Sets*, in *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2306.04800](https://arxiv.org/abs/2306.04800)&rbrack;

* Stav Zalel, *Covariant Growth Dynamics*, in *[[Handbook of Quantum Gravity]]*, Springer (2023) &lbrack;[arXiv:2302.10582](https://arxiv.org/abs/2302.10582)&rbrack;

* [[Steven Carlip]], *Causal Sets and an Emerging Continuum* &lbrack;[arXiv:2405.14059](https://arxiv.org/abs/2405.14059)&rbrack;

* Heidar Moradi, Yasaman K. Yazdi, Miguel Zilhão: *Fluctuations and Correlations in Causal Set Theory* &lbrack;[arXiv:2407.03395](https://arxiv.org/abs/2407.03395)&rbrack;



See also:

* Wikipedia, *[Causal set](http://en.wikipedia.org/wiki/Causal_sets)*


* [[Tim Porter]], _[[PorterDipath.pdf:file]]_



[[!redirects causets]]
[[!redirects causal set]]
[[!redirects causal sets]]
[[!redirects locally finite poset]]
[[!redirects locally finite posets]]