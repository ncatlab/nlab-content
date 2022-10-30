#Idea#

A _causet_ or _causal_ set is essentially the same thing as a [[partial order|poset]].  

The difference in terminology indicates the restriction to certain applications: regarding a poset as a _causal set_ means to regard it as a model for something like a space with time evolution: a morphism $a \to b$ in the poset is read as encoding the information: "there is a time evolution process which takes $a$ to $b$". Equipped with this interpretation as causal sets, posets find applications in



* **computer science**, where causal sets model concurrent computations: there exists a morphism $a \to b$ in the poset if $a$ and $b$ are states of some machine and if operating the machine can take it from state $a$ to state $b$. A simple example would be type of computation which can be done in a single step $in \to out$, but which needs to be done on _two_ inputs of the same kind. The causal set modelling this situation is

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

* **relativistic physics**, where every globally hyperbolic Lorentian metric on a manifold equips that manifold naturally with the structure of a causal set: there is a morphism from the point $x$ to the point $y$ in the manifold precisely if $y$ is in the _future_ of $x$, i.e. precisely if there exists a smooth path from $x$ to $y$ whose tangent vector is everywhere non-spacelike with respect to the Lorentyian metric. 
Moreover, the Lorentyian metric on a manifold can essentially  (need to dig out the details here, see discussion at [[smooth Lorentzian space]]) be reconstructed from this poset structure and from a _measure_. This has led to some attempts to use posets as a foundational concept for relativistic physics. 


The only technical distinction between the notion of posets and that of causal sets is that for a causal set the [[under category|under-over categories]]
$x\darr X\darr y$ for all objects $x$ and $y$ in the poset 
(the category of "two-step time evolution paths" from $y$ to $x$)
are required to be _finite_. This means these are required to have a finite set of objects (and hence necessarily, being a poset, a finit set of morphisms).



#Definition#

A causal set, or **causet** is a [[partial order|poset]] $X$ such that for all objects $x,y$ [[under category|under-over categories]] $x \downarrow X \downarrow y$ is finite.


#References#

* Timothy Porter, [[PorterDipath.pdf:file]]

[[!redirects causets]]