
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

A [[ring]] $R$ is a **principal ideal domain** if

1. it is an [[integral domain]] (hence in particular a [[commutative ring]])

2. every [[ideal]] in $R$ is a [[principal ideal]]. 

Often _pid_ is used as an abbreviation of "principal ideal domain".

A _pid_ can also be characterized as an [[integral domain]] wich possesses a [[Dedekind-Hasse norm]], making very clear the fact that it is a generalization of an [[Euclidean domain]].

## Examples

* any [[field]]

* the ring $\mathbb{Z}$ of [[integers]]

* a [[polynomial ring]] with [[coefficients]] in a field (in fact, for any commutative ring $R$, the ring $R[x]$ is a pid if and _only if_ $R$ is a field) 

* a [[valuation ring|discrete valuation ring]] (for example, a ring of formal power series over a field) 

* any [[Euclidean domain]]

* in the ring of [[entire function|entire]] [[holomorphic functions]] on $\mathbb{C}$ every finitely generated ideal is principal  ([Helmer 40](#Helmer40)), but the ring is only a [[Bézout domain]].

That both the [[integers]] and the [[polynomial rings]] $\mathbb{F}_q[x]$ over [[finite fields]] are principal integral domains with [[finite group|finite]] [[group of units]] is one aspect of the close similarity between the two that is the topic of the [[function field analogy]]. That also the [[holomorphic functions]] on the [[complex plane]] form a [[Bézout domain]] may then be viewed as part of the further similarity that relates the previous two to topics such as [[geometric Langlands duality]]. See at _[[function field analogy -- table]]_ for more on this.

## Properties 


+-- {: .num_lemma} 
###### Lemma 
In a pid $R$, an element $x$ is irreducible iff $(x)$ is a [[maximal ideal]]. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose $x$ is irreducible and $a \notin (x)$. Then the ideal generated by $a, x$ is principal, say $(b)$. Then $x = b y$ and since $x$ is irreducible, one of $b, y$ is a unit; if $y$ is a unit then $(x) = (b) = (a, x)$ and thus $a \in (x)$, contradiction. So then $b$ must be a unit, i.e., $(b)$ is the improper ideal. Thus $(x)$ has no proper extension: $(x)$ is maximal. 

For any ring $R$, if $(x)$ is maximal and $x = a b$ for a non-unit $a$, then the inclusion $(x) \subseteq (a)$ is an equality by maximality, so $a = x v$ for some $v$. Then $x = x v b$. In an integral domain we conclude $1 = v b$; thus $b$ is a unit. 
=-- 

+-- {: .num_prop #noeth} 
###### Proposition 
A pid is a [[Noetherian ring]]. 
=-- 

+-- {: .proof} 
###### Proof 
The union of an ascending chain of ideals $I_1 \subseteq I_2 \subseteq \ldots$ is an ideal $I$; if $I = (x)$, then $x$ belongs to one of the $I_n$, whereupon $I = I_n$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
A PID is a [[unique factorization domain]]. 
=-- 

+-- {: .proof} 
###### Proof 
Working in classical logic, Proposition \ref{noeth} says that the reverse inclusion relation on the set of nonzero ideals is [[well-founded relation|well-founded]]. Let $A$ be the subset of ideals $(a)$ that are products of finitely many (maybe zero!) maximal principal ideals. For any proper ideal $(x) \neq (0)$, if every $(t)$ properly containing $(x)$ can be factored into maximals, then so can $(x)$. (Spelling this out: either $(x)$ is maximal/irreducible, or factors as $(s)(t)$ where both $s$ and $t$ are non-units; $(s)$ and $(t)$ factor into maximals by hypothesis, and therefore so does $(x)$.) Thus $A$ is an inductive set, so by well-foundedness it contains every ideal $(x) \neq (0)$, i.e., $x$ can be factored into irreducibles. 

For uniqueness of the factorization, we first remark that if $p$ is irreducible and $p|a b$, then $p|a$ or $p|b$. (For $R/(p)$ is a [[field]] and thus *a fortiori* an [[integral domain]], so that if $a b \equiv 0 \; mod p$, then $a \equiv 0 \; mod p$ or $b \equiv 0 \; mod p$.) Thus if $p_1 p_2 \ldots p_m = q_1 q_2 \ldots q_n$ are two factorizations into irreducibles of the same element, then $p_1$ divides one of the irreducibles $q_i$, in which case $(p_1) = (q_i)$ and each is a unit times the other, meaning we can cancel $p_1$ on both sides and argue by induction. 
=-- 




## Structure theory of modules 
 {#StructureTheoryOfModules}

### Free and projective modules 

+-- {: .num_theorem #free} 
###### Theorem 
If $R$ is a pid, then any [[submodule]] $M$ of a [[free module]] $F$ over $R$ is also free. (For the converse statement, see [here](http://ncatlab.org/nlab/show/free+module#submod).) 
=-- 

+-- {: .proof} 
###### Proof 
By freeness of $F$, there exists an isomorphism $F \cong \sum_{j \in J} R_j$, a [[coproduct]] of copies $R_j$ of $R$ (as a module over the ring $R$) indexed over a set $J$, which we assume [[well-ordering|well-ordered]] using the [[axiom of choice]]. Define submodules of $F$: 

$$F_{\leq j} \coloneqq \sum_{i \leq j} R_i, \qquad F_{\lt j} \coloneqq \sum_{i \lt j} R_i\,.$$ 

Any element of $M \cap F_{\leq j}$ can be written uniquely as $(x, r)$ where $x \in F_{\lt j}$ and $r \in R_j$. Define a [[homomorphism]]

$$p_j \colon M \cap F_{\leq j} \to R$$ 

by $p_j((x, r)) = r$. The [[kernel]] of $p_j$ is $M \cap F_{\lt j}$, and we have an [[exact sequence]]

$$0 \to M \cap F_{\lt j} \to M \cap F_{\leq j} \to \im p_j \to 0$$ 

where $\im p_j$ is a submodule (i.e., an [[ideal]]) of $R$, hence generated by a single element $r_j$. Let $K \subseteq J$ consist of those $j$ such that $r_j \neq 0$, and for $k \in K$, choose $m_k$ such that $p_k(m_k) = r_k$. We claim that $\{m_k: k \in K\}$ forms a [[basis]] for $M$. 

First we prove [[linear independence]] of $\{m_k\}$. Suppose $\sum_{i=1}^{n} a_i m_{k_i} = 0$, with $k_1 \lt k_2 \lt \ldots \lt k_n$. Applying $p_{k_n}$, we get $a_n p_{k_n}(m_{k_n}) = a_n r_{k_n} = 0$. Since $r_{k_n} \neq 0$, we have $a_n = 0$ (since we are working over a domain). The assertion now follows by [[induction]].  

Now we prove that the $m_k$ generate $M$. Assume otherwise, and let $j \in J$ be the least $j$ such that some $m \in M \cap F_{\leq j}$ cannot be written as a linear combination of the $m_k$, for $k \in K$. If $j \notin K$, then $m \in M \cap F_{\lt j}$, so that $m \in M \cap F_{\leq i}$ for some $i \lt j$, but this contradicts minimality of $j$. Therefore $j \in K$. Now, we have $p_j(m) = r \cdot r_j$ for some $r$; put $m' = m - r m_j$. Clearly 

$$p_j(m') = p_j(m) - r \cdot p_j(m_j) = 0$$ 

and so $m' \in M \cap F_{\lt j}$. Thus $m' \in M \cap F_{\leq i}$ for some $i \lt j$. At the same time, $m'$ cannot be written as a linear combination of the $m_k$; again, this contradicts minimality of $j$. Thus the $m_k$ generate $M$, as claimed. 
=-- 

Since the [[integers]] $\mathbb{Z}$ form a pid, and [[abelian groups]] are the same as $\mathbb{Z}$-[[modules]], we have 

+-- {: .num_cor} 
###### Corollary 
**(Dedekind)** 
A [[subgroup]] of a [[free abelian group]] is also free abelian. 
=-- 

+-- {: .num_remark} 
###### Remark

The analog of this statement for possibly non-abelian [[groups]] is the _[[Nielsen-Schreier theorem]]_.

=--

Also, since [[projective modules]] are [[retracts]] of free modules, we have 

+-- {: .num_cor} 
###### Corollary 
Projective modules over a pid are free. In particular, submodules of projective modules are projective. 
=-- 

### Normal forms
 {#SmithNormalForm}

+-- {: .num_prop #MatricesOverPrincipalIdealDomainsHaveSmithNormalForm}
###### Proposition
**([[matrices]] over [[principal ideal domains]] [[matrix equivalence|equivalent]] to [[Smith normal form]])**

For $R$ a [[commutative ring]] which is a [[principal ideal domain]], every [[matrix]] $A \in Mat_{n \times m}(R)$ with entries in $R$ is [[matrix equivalence|matrix equivalent]] to a [[diagonal matrix]] filled up with zeros:

There exist [[invertible matrices]] $P \in Mat_{n \times n}(R)$ and $Q \in Mat_{m \times m}(R)$ such that the [[matrix product|product matrix]] $P A Q$ is a [[diagonal matrix]] filled up with zeros:

$$
  P A Q
  \;=\;  
$$
<center>
<img src="https://ncatlab.org/nlab/files/SmithNormalForm.jpg" width="300">
</center>

such that, moreover, each $a_i$ [[divisor|divides]] $a_{i+1}$.

=--

For [[matrices]] with coefficients in the pid of [[integers]] see also

* _[[Hermite normal form]]_.


### Torsion-free modules 

+-- {: .num_prop #torsionfree}
###### Proposition 
A finitely generated [[torsion subgroup|torsionfree]] module $M$ over a pid $R$ is free. 
=-- 

+-- {: .proof} 
###### Proof 
Let $S$ be a finite set of generators of $M$, and let $T \subseteq S$ be a maximal subset of linearly independent elements. (Unless $M = 0$, then $T$ has at least one element, because $M$ is torsionfree.) We claim that $M$ can be embedded as a submodule of the free module $F$ generated by $T$ (which in turn is the span of $T$ as a submodule $F \subseteq M$). By Theorem \ref{free}, it follows that $M$ is free. 

Let $x_1, \ldots, x_n$ be the elements of $T$. It follows from maximality of $T$ that for any $m \in S - T$, there is a linear relation 

$$r_m m + r_1 x_1 + \ldots + r_n x_n = 0$$ 

with $r_m \neq 0$. For each $m$ in the complement $S - T$, pick such an $r_m$, and form $r = \prod_{m \in S - T} r_m$. Then the image of the scalar multiplication $\lambda_r \colon M \to M$ factors through $F \subseteq M$, and $M \to \lambda_r(M)$ is monic because $M$ is torsionfree. This completes the proof. 
=-- 

+-- {: .num_prop #flat} 
###### Proposition 
Let $R$ be a pid. Then an $R$-module $M$ is torsionfree if and only if it is [[flat module|flat]]. 
=-- 

+-- {: .proof} 
###### Proof 
Suppose $M$ is flat. Let $K$ be the field of fractions of $R$; since $R$ is a domain, we have a monic $R$-module map $R \to K$. By flatness, we have an induced monomorphism $M \cong R \otimes_R M \to K \otimes_R M$. For any nonzero $r \in R$, the naturality square 

$$\array{
M & \to & K \otimes_R M \\
 \mathllap{\lambda_r} \downarrow & & \downarrow \mathrlap{1 \otimes \lambda_r} \\ 
M & \to & K \otimes_R M
}$$ 

commutes, and since the map $1 \otimes \lambda_r$ is multiplication by a non-zero scalar on a vector space, it follows that this map and therefore also $\lambda_r$ is monic, i.e., $M$ is torsionfree. 

In the other direction, suppose $M$ is torsionfree. Any module is the filtered colimit over the system of finitely generated submodules and inclusions between them; in this case all the finitely generated submodules of $M$ are torsion-free and hence free, by Proposition \ref{torsionfree}. Thus $M$ is a filtered colimit of free modules; it is therefore flat by a standard result proved [here](http://ncatlab.org/nlab/show/flat+module#filtfree). 
=-- 


### Structure theory of finitely generated modules 

_[[structure theorem for finitely generated modules over a principal ideal domain]]_


## In constructive mathematics

In [[constructive mathematics]], many important rings may fail to be principal ideal domains in the na&#239;ve sense; the notion of _[[Bézout domain]]_, in which only the finitely generated ideals are required to be principal, is better behaved.

For instance, the ring of integers is a principal ideal domain if and only if the [[excluded middle|law of excluded middle]] holds: In one direction, the usual proofs rely on being able to [[decidable proposition|decide]] whether any particular integer belongs to the ideal or not. For the converse, let $\varphi$ be an arbitrary proposition. Consider the ideal $\{ x \in \mathbb{Z} | (x = 0) \vee \varphi \}$. By assumption, it is generated by some number $n$. Since the integers are [[decidable equality|discrete]], it holds that $n = 0$ or $n \neq 0$. In the first case $\neg\varphi$ holds, in the second $\varphi$.

However, this ideal cannot be proved to be finitely generated either.  If an ideal is generated by $n_1, \ldots, n_k$, then we may form their [[gcd]] one step at a time, which we can do algorithmically.  Therefore, $\mathbb{Z}$ remains a B&#233;zout domain.

On the other hand, we could try to modify the concept of principal ideal domain to recover a concept that is identical to the usual one in [[classical mathematics]] but also includes $\mathbb{Z}$.  For instance, we could demand that every [[decidable subset|decidable]] ideal is principal, or (potentially more strongly) that any ideal generated by a decidable subset is principal.  While these seem to work at first, they are too weak to prove that every PID is a B&#233;zout domain, so we should try to think of something better.

Some authors have tried to define a principal ideal domain as a [[Noetherian ring|Noetherian]] [[Bézout ring|Bézout]] [[integral domain|domain]], but it is unknown if this still coincides in constructive mathematics with the definition of principal ideal domain above. 

## See also

* [[unique factorization domain]]

* [[principal ideal domain]]

## References

* {#Helmer40} O. Helmer, _Divisibility properties of integral functions_, Duke Math. J.
6 (1940), 345-356.

* Wikipedia, _[Principal ideal domain](http://en.wikipedia.org/wiki/Principal_ideal_domain)_

* Eric Wofsey, _Principal Ideal Domains_, (written for Mathcamp 2009) [pdf](https://web.archive.org/web/20161213182507/http://www.math.harvard.edu/~waffle/pids.pdf)

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))


[[!redirects principal ideal domain]]
[[!redirects principal ideal domains]]
[[!redirects pid]]
[[!redirects pids]]
[[!redirects PID]]
[[!redirects PIDs]]
