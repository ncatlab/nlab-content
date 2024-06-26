
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Second-order arithmetic is a [[theory]] of [[arithmetic]] dealing with [[natural numbers]] and, what makes it "second-order", [[sets]] of natural numbers[^fine]. SOA, or $Z_2$ as it is often denoted, is [[proof theory|proof-theoretically]] weak in comparison with [[ZFC]], but still strong enough to derive "almost all of undergraduate mathematics" (Friedman). 

[^fine]: The logic that governs the language and theory of $Z_2$ is ordinary (first-order) predicate logic. The "second-order" aspect is really in the _models_, where one interprets the symbol $\in$ as membership in a background set theory, i.e., terms of type $P N$ are interpreted as subsets of the set that interprets the type $N$, and an extensionality axiom is in force. A _full model_ is where $P N$ is interpreted as the full power set of $N$. When one sees absoluteness assertions such as "there is only one (full) model of SOA up to isomorphism," it should be clear that this is meant with regard to a given background set theory. Cf. the fact that while there is, up to isomorphism, at most one [[natural numbers object]] $\mathbb{N}$ in a given [[topos]], the set of global elements $\Gamma(\mathbb{N})$ might contain "non-standard elements" as viewed against the background $Set$. 


## Definition

The [[theory|language]] of SOA consists of two sorts, here denoted $N$ and $P N$, together with 

* A constant $0$ of type $N$, 

* An unary function symbol $s \colon N \to N$, 

* Binary function symbols $+, \cdot \colon N \times N \to N$, 

* A binary relation symbol $\lt$ of type $N \times N$. 

* A binary relation symbol $\in$ of type $N \times P N$. 

The axioms of SOA may be divided into two parts: the first part comprises the "first-order axioms" that deal only with the sort $N$, and defines which is known as _Robinson arithmetic_. The second part comprises [[induction]] and [[comprehension schemes]] that involve the symbol $\in$. 


### "First-order" axioms

Omitting the sort $P N$ and the symbol $\in$ from the language, the [[theory|axioms]] in this section give [[Robinson arithmetic]]. The logic throughout is [[classical logic|classical]] [[first-order logic|first-order]] (predicate) logic with [[equality predicate|equality]]. 

For all the formulas in this section, it is tacitly understood that there are universal quantifiers at the heads of formulas, binding all variables which appear freely. 

1. $s(m) = 0 \rightarrow \bot$. 

2. $s(m) = s(n) \rightarrow m = n$. 

3. $(0 = n) \vee (\exists_m s(m) = n)$. 

4. $m + 0 = m$.

5. $m + s(n) = s(m+n)$. 

6. $m \cdot 0 = 0$.

7. $m \cdot s(n) = (m\cdot n)+m]$. 

8. $m \lt 0 \rightarrow \bot$. 

9. $m \lt s(n) \leftrightarrow ((m \lt n) \vee (m=n))$.

10. $(0 = n) \vee (0 \lt n)$. 

11. $((s(m) \lt n) \vee (s(m) = n)) \leftrightarrow m \lt n$. 


### "Second-order" axioms

Note: according to convention, lower-case letters refer to terms of type $N$, and upper-case letters to terms of type $P N$. 

1. [[comprehension scheme|Comprehension scheme]]: for any [[formula]] $\varphi$ in the language of SOA with [[free variables]] $\vec{m} = m_1, \ldots, m_j$ and $\vec{X} = X_1, \ldots, X_k$, 
$$\forall \vec{m} \forall \vec{X} \exists Z \forall n (n\in Z \leftrightarrow \varphi(n))$$ 
provided that the variable $Z$ does not appear in $\varphi$. (Using [[alpha-equivalence]] to rename variables, it\'s enough that $Z$ does not appear free in $\varphi$.)

2. Full [[induction]] scheme: for $\varphi$ any formula with a free variable $n$ and possible remaining free variables $\vec{m} = m_1, \ldots, m_j$ and $\vec{X} = X_1, \ldots, X_k$, 

$$
  \forall \vec{m} \forall \vec{X} ((\varphi(0) \wedge \forall n (\varphi(n) \rightarrow \varphi(s(n))) \rightarrow \forall n \varphi(n))
$$

The instance in the full induction scheme where $\varphi$ is the formula $n \in X$ is called simply the _induction axiom_. The induction axiom together with the comprehension scheme implies the full induction scheme. 


## Subsystems of SOA

The theory described above gives full second-order arithmetic. However, in [[reverse mathematics]], one often studies subsystems of weaker proof-theoretic strength than SOA, by limiting in some way the comprehension scheme (often also beefing up the single induction axiom with more instances of the induction scheme, to offset the weakening). The main examples are given in [Wikipedia](http://en.wikipedia.org/wiki/Reverse_mathematics); a standard reference is [Simpson](#Sim). 

Many important subsystems for SOA have been the subject of an [[ordinal analysis]].

Another important subsystem is _intuitionistic_ second-order arithmetic, or second-order [[Heyting arithmetic]].  Here, we use [[intuitionistic logic]] rather than classical logic as the underlying first-order logic.  In a subsystem without the induction axiom, we must add axioms stating that equality and order are [[decidable predicate|decidable]]:

* $(m = n) \vee ((m = n) \rightarrow \bot)$;

* $(m \lt n) \vee ((m \lt n) \rightarrow \bot)$.

Full (classical) SOA may be recovered from intuitionistic SOA by adding a similar axiom that set membership is decidable; in a subsystem without the comprehension scheme, this needs to be strengthened to an axiom scheme that every proposition (with any free variables) is true or false (effectively making the logic classical again).


## Related concepts

* [[foundations]] 

* [[elementary function arithmetic]] 

* [[descriptive set theory]]


## References

* Wikipedia _[Second order arithmetic](http://en.wikipedia.org/wiki/Second-order_arithmetic)_

* Harvey Friedman's [Home Page](http://www.math.osu.edu/~friedman.8/)

* {#Sim} Stephen G. Simpson, _Subsystems of second order arithmetic_, Perspectives in Logic (2nd ed.), Cambridge University Press (2009) ([pdf](http://www.personal.psu.edu/t20/sosoa/chapter1.pdf))



[[!redirects SOA]]
[[!redirects second order arithmetic]]
[[!redirects second-order arithmetic]]
[[!redirects higher-order arithmetic]]