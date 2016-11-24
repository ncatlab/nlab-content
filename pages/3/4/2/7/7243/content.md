
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
 {#Idea}

For each [[prime number]] $p$ the [[ring]] of _$p$-adic integers_ $\mathbb{Z}_p$ is the [[formal completion]] of the ring $\mathbb{Z}$ at the [[prime ideal]] $(p)$. Geometrically this means that $\mathbb{Z}_p$ is the [[ring of functions]] on a [[formal neighbourhood]] of $p$ inside [[Spec(Z)]] (this is discussed in more detail [below](#AsFormalNeighbourhoodOfPrime)). Algebraically it means that the elements in $\mathbb{Z}_p$ look like [[formal power series]] where the formal variable is the prime number $p$.

## Definition 

For any [[prime number]] $p$, the [[ring]] of $p$-**adic integers** $\mathbb{Z}_p$ (which, to avoid possible confusion with the ring $\mathbb{Z}/(p)$ used in [[modular arithmetic]], is also written as $\widehat{\mathbb{Z}}_p$) may be described in one of several ways: 

1. To the person on the street, it may be described as (the ring of) numbers written in base $p$, but allowing infinite expansions to the left. Thus, numbers of the form 
$$\sum_{n \geq 0} a_n p^n$$ 
where $0 \leq a_n \lt p$, added and multiplied with the usual method of carrying familiar from adding and multiplying ordinary integers. 

2. More abstractly, it is the [[limit]] $\underset{\leftarrow}{\lim} \mathbb{Z}/(p^n)$, in the [[category]] of (unital) [[ring|rings]], of the [[diagram]] 
$$ \ldots \to \mathbb{Z}/(p^{n+1}) \to \mathbb{Z}/(p^n) \to \ldots \to \mathbb{Z}/(p) .$$ 
This is also a limit in the category of [[topological rings]], taking the rings in the diagram to have [[discrete topologies]].

3. Alternatively, it is the [[metric completion]] of the ring of [[integers]] $\mathbb{Z}$ with respect to the $p$-adic [[absolute value]]. Since addition and multiplication of integers are [[uniform space|uniformly continuous]] with respect to the $p$-adic [[absolute value]], they extend uniquely to a uniformly continuous addition and multiplication on $\mathbb{Z}_p$. Thus $\mathbb{Z}_p$ is a [[topological ring]]. 

4. Also $\mathbb{Z}[ [ x ] ]/(x-q)\mathbb{Z}[ [ x ] ]$, see at _[[analytic completion]]_. 

Hence one also speaks of the _$p$-[[adic completion]]_ of the integers.  See [[completion of a ring]] (which generalizes 2&3).

There is also this characterization:

+-- {: .num_lemma #pAdicIntegersAspExtensionofFpByThemselves}
###### Lemma

There is a [[short exact sequence]]

$$
  0 
    \to
  \mathbb{Z}_{p}
    \overset{p \cdot (-)}{\longrightarrow}
  \mathbb{Z}_{p}
    \longrightarrow
  \mathbb{Z}/p\mathbb{Z}
    \to
  0
  \,.
$$

=--

+-- {: .proof}
###### Proof

Consider the following [[commuting diagram]]

$$
  \array{
     \vdots && \vdots && \vdots
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p^3\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^4 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p^2\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^3 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     \mathbb{Z}/p\mathbb{Z}
       &\overset{p\cdot (-)}{\longrightarrow}&
     \mathbb{Z}/p^2 \mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
     \\
     \downarrow
       &&
     \downarrow
       &&
     \downarrow
     \\
     0
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}
       &\longrightarrow&
     \mathbb{Z}/p\mathbb{Z}     
  }
  \,.
$$

Each horizontal sequence is exact. Taking the [[limit]] over the vertical sequences yields the sequence in question. Since limits commute over limits, the result follows.

=--




## Properties

### Topology

The ring of $p$-adic integers has the following properties: 

* As a [[topological space]], it is [[compact space|compact]], [[Hausdorff space|Hausdorff]], and [[totally disconnected space|totally disconnected]] (i.e., is a [[Stone space]]). Moreover, every point is an [[accumulation point]], and there is a countable basis of [[clopen set|clopen sets]] -- a Stone space with these properties must be [[homeomorphism|homeomorphic]] to [[Cantor space]]. 

* As a [[topological group]] under addition, it is therefore an [[almost connected group]]. As an [[abelian group|abelian]]  [[compact group]], it is [[Pontryagin duality|Pontryagin dual]] to the [[Prüfer group|Prüfer]] $p$-group as [[discrete group]]. 

### Relation to profinite completion of the integers

+-- {: .num_example #ProfCompletionOfIntegers}
###### Example

The [[profinite completion of the integers]] is

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

### Pontrajgin duality to Pr&#252;fer $p$-group

Under [[Pontryagin duality]], the [[abelian group]] underlying $\mathbb{Z}_p$ maps to the [[Prüfer p-group]] $\mathbb{Z}[p^{-1}]/\mathbb{Z}$, see at _[[Pontryagin duality for torsion abelian groups]]_.

$$
  \array{
     &\mathbb{Z}[p^{-1}]/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{Q}/\mathbb{Z}
     &\hookrightarrow&
     \mathbb{R}/\mathbb{Z}
     \\
     {}^{\mathllap{hom(-,\mathbb{R}/\mathbb{Z})}}\downarrow
     \\
     &\mathbb{Z}_p
     &\leftarrow&
     \hat \mathbb{Z}
     &\leftarrow&
     \mathbb{Z}
  }
$$


### As the formal neighbourhood of a prime
 {#AsFormalNeighbourhoodOfPrime}

The [[formal spectrum]] $Spf(\mathbb{Z}_p)$ of $\mathbb{Z}_p$ may be understood as the [[formal neighbourhood]] of the point corresponding to the [[prime]] $p$ in the [[prime spectrum]] $Spec(\mathbb{Z})$ of the [[integers]]. The inclusion

$$
  \{p\}
  \hookrightarrow
  Spf(\mathbb{Z}_p)
  \hookrightarrow
  Spec(\mathbb{Z})
$$

is the [[Isbell duality|formal dual]] of the canonical [[projection]] maps $\mathbb{Z}\to \mathbb{Z}_p\to \mathbb{Z}/(p)$.

This plays a central role for instance in the [[function field analogy]].
It is highlighted for instance in ([Hartl 06, 1.1](Hartl06), [Buium 13, section 1.1.3](#Buium13)). See also at _[[arithmetic jet space]]_ and at _[[ring of Witt vectors]]_.

[[!include infinitesimal and local - table]]

## Related notions 

* $p$-[[p-adic number|adic number]], [[adele]].

* [[p-adic complex number]]

* [[Z-infinity-module]] 

* [[p-completion]]

* [[local-global principle]]

* [[p-adic homotopy]]

* [[ℓ-adic cohomology]]

* [[p-adic geometry]]

* [[p-adic physics]]


## References

Introductions and surveys include

* {#Sullivan70} [[Dennis Sullivan]], pp. 9 of _Localization, Periodicity and Galois Symmetry_ (The 1970 MIT notes) edited by [[Andrew Ranicki]], K-Monographs in Mathematics, Dordrecht: Springer ([pdf](http://www.maths.ed.ac.uk/~aar/surgery/gtop.pdf)) 



* Bernard Le Stum, _One century of $p$-adic geometry -- From Hensel to Berkovich and beyond_ talk notes, June 2012 ([pdf](http://www-irma.u-strasbg.fr/IMG/pdf/NotesCoursLeStum.pdf))


* {#Lenstra} [[Hendrik Lenstra]], _Profinite groups_ ([pdf](http://websites.math.leidenuniv.nl/algebra/Lenstra-Profinite.pdf))
 
The [[synthetic differential geometry]]-aspect of the $p$-adic numbers is highlighted for instance in 

* {#Hartl06} [[Urs Hartl]], _A Dictionary between Fontaine-Theory and its Analogue in Equal Characteristic_ ([arXiv:math/0607182](http://arxiv.org/abs/math/0607182))

* {#Buium13} [[Alexandru Buium]], _Differential calculus with integers_ ([arXiv:1308.5194](http://arxiv.org/abs/1308.5194))

[[!redirects p-adic integer]]
[[!redirects p-adic integers]]

[[!redirects adic integer]]
[[!redirects adic integers]]

[[!redirects ring of p-adic integers]]
[[!redirects rings of p-adic integers]]
