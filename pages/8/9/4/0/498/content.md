
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--

# Local rings
* table of contents
{: toc}

## Definitions

A **local ring** is a [[ring]] (with [[unit]], usually also assumed [[commutative ring|commutative]]) such that:

* $0 \ne 1$; and

* whenever $a + b = 1$, $a$ or $b$ is [[invertible]].

Here are a few equivalent ways to phrase the combined condition:

* Whenever a (finite) [[sum]] equals $1$, at least one of the summands is invertible.

* Whenever a sum is invertible, at least one of the summands is invertible.

* Whenever a sum of products is invertible, for at least one of the summands, all of its multiplicands are invertible.  (This is not entirely trivial in the noncommutative case, but it\'s still correct.)

* The invertible elements form an [[anti-ideal]]: 
  * $0$ is not invertible 
  * if $a + b$ is invertible, then either $a$ is invertible or $b$ is invertible
  * if $a \cdot b$ is invertible, then $a$ is invertible and $b$ is invertible

The anti-ideal of invertible elements is in fact a minimal anti-ideal, so the [[quotient object|quotient ring]] of a local ring by its anti-ideal of invertible elements is a [[Heyting field]], the __[[residue field]]__ of the local ring.

In the context of [[excluded middle]], every [[weak local ring]] is a [[local ring]]. Thus, the following is equivalent to the above definitions in classical mathematics:

* The sum of two non-invertible elements is non-invertible.
* The non-invertible elements form an [[ideal]]. 

\begin{remark}\label{TrivialRingAsALocalRing}
In [LombardiQuitté2010](#LombardiQuitté2010), the authors' definitions of local ring do not include the non-equational axiom $1 \neq 0$, which means that the [[trivial ring]] is a local ring and constitutes the [[terminal object]] in the [[category|categories]] of local rings.
\end{remark}

## Examples

* Every [[Heyting field]] is a local ring.

* Every [[Kock field]] is a local ring.

* For $R$ a local ring, then the [[power series ring]] $R[ [x] ]$ is also a local ring.

## Properties

### Jacobson radical

The set of non-invertible elements in a local ring is the [[Jacobson radical]]. 

### Kaplansky's theorem 
 {#KaplanskyTheorem}

+-- {: .num_theorem} 
###### Theorem 
**(Kaplansky)** 
A [[projective module]] over a commutative local ring is a [[free module]]. 
=-- 

An exposition of the proof may be found [here](http://blog.jpolak.org/?p=363). A [[constructive mathematics|constructive]] proof of a finitary weakening of Kaplansky's theorem proceeds as follows.

+-- {: .num_lemma}
###### Lemma
Let $A$ be a local ring. Let $\mathfrak{a}$ be a finitely generated idempotent ideal in $A$. Then $\mathfrak{a} = (0)$ or $\mathfrak{a} = (1)$.
=--
+-- {: .proof}
###### Proof
Consider $\mathfrak{a}$ as a finitely generated $A$-module. Then, by [[Nakayama's lemma]], there exists an element $x \in A$ such that $x \equiv 1$
modulo $\mathfrak{a}$ and $x \mathfrak{a} = 0$. Since $A$ is a local ring, $x$ is invertible or $1-x$ is invertible. In the first case it follows that $\mathfrak{a} = (0)$, in the second that $\mathfrak{a} = (1)$.
=--

+-- {: .num_lemma}
###### Lemma
Let $A$ be a local ring. Let $P$ be an idempotent matrix over $A$. Then $P$ is equivalent to a diagonal matrix with entries $1$ and $0$.
=--
+-- {: .proof}
###### Proof
Since $P$ is idempotent, so are its ideals $(\Lambda^i P)$
of $i$-minors:
$$ (\Lambda^i P) = (\Lambda^i (P \circ P)) =
(\Lambda^i P \circ \Lambda^i P) \subseteq (\Lambda^i P) \cdot (\Lambda^i P)
\subseteq (\Lambda^i P). $$
By the previous lemma, they are therefore each equal to $(0)$ or $(1)$. Since they form a descending chain, there exists a stage $r$ such that $(\Lambda^r P) = (1)$ and $(\Lambda^{r+1} P) = (0)$. Therefore all $(r+1)$-minors of $P$ are zero, and -- since $A$ is a local ring -- there exists at least one invertible $r$-minor. Thus $P$ can be made into a diagonal matrix of the desired form by applying row and column transformations.
=--

+-- {: .num_remark}
###### Remark
We can even show that $P$ is _similar_ to a diagonal matrix with entries $1$ and $0$: By the lemma, image and kernel of $P$ are finite free. Combining bases of these subspaces, we obtain a basis of the full space; expressing $P$ with respect to this basis, we obtain a diagonal matrix of the desired form.
=--

+-- {: .num_theorem}
###### Theorem
Let $M$ be a finitely generated module over a local ring $A$. Assume that $M$ is projective. Then $M$ is finite free.
=--
+-- {: .proof}
Fix a linear surjection $p : A^n \to M$ and a section $s : M \to
A^n$. The composition $P \coloneqq s \circ p$ is idempotent and $M$ is isomorphic to $A^n/\operatorname{ker}(P)$. Since $P$ is equivalent to a diagonal matrix with entries $1$ and $0$, this module is obviously finite free.
=--


## In geometry

In [[algebraic geometry]] or [[synthetic differential geometry]] and [[commutative algebra]], the most commonly used definition of a local commutative ring is a commutative ring $R$ with a unique maximal ideal. Hence the Spec of such an $R$ has a unique closed point. Intuitively it can be thought of as some kind of "infinitesimal neighborhood" of a closed point.

The spectrum of a ring $R$ is [[focal point|local]], i.e. in any covering of $Spec R$ by open subsets one of the subsets is already the whole of $Spec R$, if and only if $R$ is a local ring. This provides some justification for the name.

The [[topos theory]] formulation of this is a [[local topos]].

An important example of a local ring in algebraic geometry is $R = k[\epsilon]/\epsilon^2$. This ring is known as the ring of dual numbers. Intuitively, we can think of its spectrum as consisting of a closed point and a tangent vector. Indeed this is justified, as morphisms from $\operatorname{Spec} R$ to a scheme $X$ correspond exactly to pairs $(x,v)$, where $x \in X$ and $v$ is a (Zariski) tangent vector at $x$.

Local rings are also important in [[deformation theory]]. One might define an infinitesimal deformation of a scheme $X_0$ to be a deformation of $X_0$ over $\operatorname{Spec} R$ where $R$ is a local ring.


## In weak foundations

Local rings are often more useful than fields when doing mathematics [[internalization|internally]]. For one thing, the definition make sense in any [[coherent category]]. But unlike the definition of [[discrete field]] (which is also coherent), it is satisfied by a [[real-numbers object]]. Rather than mod out by the ideal of non-invertible elements, you take care to use only properties that are invariant under multiplication by an invertible element.

In [[constructive mathematics]], one could do the same thing, but it\'s more common to use the notion of [[Heyting field]]. This is closely related, however; the quotients of local rings are precisely the Heyting fields (which are themselves local rings). In fact, one can define an [[apartness relation]] (like that on a Heyting field) in any local ring: $x \# y$ iff $x - y$ is invertible. Then the local ring is a Heyting field if and only if this apartness relation is [[tight relation|tight]].

+-- {: .num_prop #internal} 
###### Proposition 
The addition and multiplication operations on a local ring $R$ are strongly extensional with respect to the canonical apartness relation $\#$ defined by $x \# y$ iff $x - y$ is invertible. In this way a local ring becomes an internal [[ring object]] in the category $Apart$, consisting of sets with apartness relations and maps (strongly extensional functions) between them. 
=-- 

+-- {: .proof} 
###### Proof 
Recall that products $X \times Y$ in the category of sets with apartness relations is the cartesian product of the underlying sets equipped with the apartness relation defined by $(x, y) \# (x', y')$ iff $x \# x'$ in $X$ *or* $y \# y'$ in $Y$. Recall also that a function $f: X \to Y$ between sets with apartness relations is *strongly extensional* if $f(x) \# f(y)$ implies $x \# y$. 

For addition, if $(x + y) \# (x' + y')$, then $x + y - (x' + y') = (x - x') + (y - y')$ is invertible, so $x - x'$ or $y - y'$ is invertible since $R$ is local, whence $(x, y) # (x', y')$. Thus addition is strongly extensional. 

For multiplication, if $x y # x' y'$, then $x y - x' y'$ is invertible. Write $x y - x' y' = (x - x')y + x'(y - y')$. Since $R$ is local, either $(x - x')y$ is a unit or $x'(y - y')$ is a unit. From this we easily conclude $x - x'$ is a unit or $y - y'$ is, whence $(x, y) # (x', y')$. So multiplication is also strongly extensional. 
=-- 

Constructively there are also possible variants of the definition of local ring.  For instance, in [Johnstone77](#Johnstone77) a **[[weak local ring]]** is defined to be a ring in which the sum of any two noninvertible elements is noninvertible. The quotients of weak local rings are the [[weak Heyting fields]], or what Johnstone called  *residue [[fields]]* (nontrivial rings in which every noninvertible element is zero); this is the origin of the name "residue field" by Johnstone.

There is also the notion of a **[[residually discrete local ring]]**, which is a local ring where every element is either invertible or noninvertible, or equivalently, where the [[apartness relation]] of the local ring is a [[decidable relation]]. The quotient of residually discrete local rings are precisely the [[discrete fields]]. 

## Local homomorphisms 

Classically, if $R$ and $S$ are local rings with maximal ideals $\mathfrak{m}$ and $\mathfrak{n}$ respectively, then a ring [[homomorphism]] $f: R \to S$ is said to be *local* if $f(\mathfrak{m}) = \exists_f (\mathfrak{m}) \subseteq \mathfrak{n}$. Equivalently, $\mathfrak{m} \subseteq f^{-1}(\mathfrak{n})$. Taking [[complements]] and using the fact that taking [[inverse images]] preserve complements, this is equivalent to $f^{-1}(S^\times) \subseteq R^\times$ where $R^\times$ is the [[group of units]]. Of course we also have $R^\times \subseteq f^{-1}(S^\times)$ (equivalently $f(R^\times) \subseteq S^\times$) just from the fact that $f$ is a ring homomorphism, so in brief $f$ is local if $R^\times = f^{-1}(S^\times)$: an element $f(r)$ is invertible (if and) only if $r$ is. 

In constructive settings it makes sense to take this last formulation as our notion of local homomorphism. In view of Proposition \ref{internal}, it makes sense to say it like this: 

+-- {: .num_defn} 
###### Definition 
A *local homomorphism* between local rings is an internal ring homomorphism between their associated internal rings in the category $Apart$. 
=-- 

Possible to-dos: say something about $\mathfrak{m}$-adic topology, completion, Zariski topos as classifying topos... 



## Related concepts

* [[localization of a commutative ring]]

* [[strict local ring]]

* [[Jacobson radical]]

* [[valuation ring]] 

* [[Zariski topos]] 

* [[Henselian ring]]

* [[ordered local ring]]

* [[weak local ring]]

* [[local ring setoid]]

* [[residually discrete local ring]]

* [[apartness ring]]

| [[commutative ring]] | [[reduced ring]] | [[integral domain]] |
---------------------|-----------------|-----------------|
| [[local ring]] | [[reduced local ring]] | [[local integral domain]] |
| [[Artinian ring]] | [[semisimple ring]] | [[field]] |
| [[Weil ring]] | [[field]] | [[field]] |

## References

* {#Johnstone77} [[Peter Johnstone]], *Rings, Fields, and Spectra*, Journal of Algebra **49** (1977) pp 238-260. doi:[10.1016/0021-8693(77)90284-8](https://doi.org/10.1016/0021-8693%2877%2990284-8)

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Richman20} [[Fred Richman]], *Laurent series over $\mathbb{R}$*. Communications in Algebra, Volume 48, Issue 5, 11 Jan 2020 Pages 1982-1984 &lbrack;[doi:10.1080/00927872.2019.1710166](https://doi.org/10.1080/00927872.2019.1710166)&rbrack;

[[!redirects local ring]]
[[!redirects local rings]]