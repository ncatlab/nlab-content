
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}


## Definition 

For any [[prime number]] $p$, the [[ring]] of $p$-**adic integers** $\mathbb{Z}_p$ (which, to avoid possible confusion with the ring $\mathbb{Z}/(p)$, is also written as $\widehat{\mathbb{Z}}_p$) may be described in one of several ways: 

1. To the person on the street, it may be described as (the ring of) numbers written in base $p$, but allowing infinite expansions to the left. Thus, numbers of the form 
$$\sum_{n \geq 0} a_n p^n$$ 
where $0 \leq a_n \leq p-1$, added and multiplied with the usual method of carrying familiar from adding and multiplying ordinary integers. 

2. More precisely, it is the [[metric space]] [[completion]] of the ring of [[integers]] $\mathbb{Z}$ with respect to the $p$-adic [[absolute value]]. Since addition and multiplication of integers are [[uniform space|uniformly continuous]] with respect to the $p$-adic [[absolute value]], they extend uniquely to a uniformly continuous addition and multiplication on $\mathbb{Z}_p$. Thus $\mathbb{Z}_p$ is a [[topological ring]]. 

3. Alternatively, it is the [[limit]], in the [[category]] of (unital) [[ring|rings]], of the [[diagram]] 
$$\ldots \to \mathbb{Z}/(p^{n+1}) \to \mathbb{Z}/(p^n) \to \ldots \to \mathbb{Z}/(p)$$ 
also considered as a topological ring if the limit is taken in the category of topological rings, and taking the rings in the diagram to have [[discrete space|discrete]] topologies. 


## Properties

### Topology

The $p$-adic integers have the following properties: 

* As a [[topological space]], it is [[compact space|compact]], [[Hausdorff space|Hausdorff]], and [[totally disconnected space|totally disconnected]] (i.e., is a [[Stone space]]). Moreover, every point is an [[accumulation point]], and there is a countable basis of [[clopen set|clopen sets]] -- a Stone space with these properties must be [[homeomorphism|homeomorphic]] to [[Cantor space]]. 

* As a [[topological group]] under addition, it is therefore an [[almost connected group]]. As an [[abelian group|abelian]]  [[compact group]], it is [[Pontryagin duality|Pontryagin dual]] to the [[Prüfer group|Prüfer]] $p$-group as [[discrete group]]. 

### Relation to profinite completion of the integers

+-- {: .num_example #ProfCompletionOfIntegers}
###### Example

The [[profinite completion of a group|profinite completion]] of the [[integers]] is

$$
  \widehat {\mathbb{Z}} 
    \coloneqq 
  \underset{\leftarrow}{\lim}_{n \in \mathbb{N}} (\mathbb{Z}/n\mathbb{Z})
  \,.
$$

This is [[isomorphism|isomorphic]] to the [[product]] of the $p$-adic integers for all $p$

$$
  \widehat{\mathbb{Z}} \simeq \underset{p\; prime}{\prod} \mathbb{Z}_p
  \,.
$$

=--

([e.g. Lenstra, example 2.2](#Lenstra))

+-- {: .num_defn }
###### Definition

The ring of integral [[adeles]] $\mathbb{A}_{\mathbb{Z}}$ is the [[product]]
of the profinite completion $\widehat{\mathbb{Z}}$ of the integers,
example \ref{ProfCompletionOfIntegers},
with the [[real numbers]]

$$
  \mathbb{A}_{\mathbb{Z}}
  \coloneqq
  \mathbb{R} \times \widehat{\mathbb{Z}}
  \,.
$$

The [[group of units]] of the ring of adeles is called the group of [[ideles]].

=--


## Related notions 

* $p$-[[p-adic number|adic number]], [[adele]].

* [[Z-infinity-module]] 

* [[p-adic homotopy]]

* [[ℓ-adic cohomology]]

* [[p-adic geometry]]

* [[p-adic physics]]

## References

Introductions and surveys include

* Bernard Le Stum, _One century of $p$-adic geometry -- From Hensel to Berkovich and beyond_ talk notes, June 2012 ([pdf](http://www-irma.u-strasbg.fr/IMG/pdf/NotesCoursLeStum.pdf))


* [[Hendrik Lenstra]], _Profinite groups_ ([pdf](http://websites.math.leidenuniv.nl/algebra/Lenstra-Profinite.pdf))
 {#Lenstra}
 

[[!redirects p-adic integer]]
[[!redirects p-adic integers]]

[[!redirects adic integer]]
[[!redirects adic integers]]

[[!redirects profinite completion of the integers]]