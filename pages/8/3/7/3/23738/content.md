
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition ##

\begin{definition}
Let $R$ be an integral domain and let $a,b \in R$. We call **gcd** of $a$ and $b$ an element $gcd(a,b) \in R$ such that:

1. $gcd(a,b)$ divides both $a$ and $b$,

1. for every element $r \in R$, if $r$ divides both $a$ and $b$, then $r$ divides $gcd(a,b)$.

\end{definition}

In other words, a gcd of $a$ and $b$ is a [[meet]] in the [[preordered set]] $(R,\mid)$ i.e. a [[cartesian product]] of $a$ and $b$ in $(R,\mid)$ seen as [[thin category]].

It follows from the properties of cartesian products that a gcd is unique up to isomorphism in the category $(R,\mid)$ and that every element isomorphic to a gcd of $a$ and $b$ is also a gcd of $a$ and $b$. 

That is, if a gcd of $a$ and $b$ exists, then the gcd's of $a$ and $b$ are exactly the products of this first gcd by any invertible element.

\begin{definition}
A **GCD domain** is an [[integral domain]] $R$ such that every pair $a,b \in R$ of elements admits a gcd. 
\end{definition}

## Properties

### Equivalence between GCD domain and LCM domain

\begin{definition}
Let $R$ be an integral domain and let $a,b \in R$. We call **lcm** of $a$ and $b$ an element $lcm(a,b) \in R$ such that:

1. both $a$ and $b$ divides $lcm(a,b)$,

1. for every element $r \in R$, if both $a$ and $b$ divide $r$, then $lcm(a,b)$ divides $r$.

\end{definition}
As for the gcd, an lcm of $a$ and $b$ is just a [[join]] in the preordered set $(R,\mid)$. Therefore, if an lcm of $a$ and $b$ exists, then the lcm's of $a$ and $b$ are exactly the products of this first lcm by any invertible element.

The following proposition treats the interactions of gcd, lcm and $0$.
\begin{proposition}
Let $R$ be an integral domain.

* Let $r \in R$. Then $gcd(r,0)=r$ and $lcm(r,0)=0$.

* Let $a,b \in R$. Then, $gcd(a,b)$ exists and is equal to $0$ iff both $a$ and $b$ are zero.

* Let $a,b \in R$. Then $lcm(a,b)$ exists and is equal to $0$ iff one of $a$ or $b$ is zero.

\end{proposition}
\begin{proof}

* We have that $r$ divides both $r$ and $0$. If $s$ divides both $r$ and $0$, then in particular $s$ divides $r$. Therefore $gcd(r,0)=r$. We have that both $r$ and $0$ divides $0$. If both $r$ and $0$ divides $s$, then in particular $0$ divides $s$. Therefore $lcm(r,0)=0$.

* If $gcd(a,b)=0$, then both $a$ and $b$ are zero since $gcd(a,b)$ divides both of them. If both $a$ and $b$ are zero, we already know from the previous point that $gcd(a,b)=0$.

* If $lcm(a,b)=0$, then $ab=0$ since $lcm(a,b)$ divides $ab$. It follows that either $a$ or $b$ is zero. Now, suppose that one of $a$ or $b$ is zero. We already know that both $a$ and $b$ divide $0$. Suppose that $c \in R$ is such that both $a$ and $b$ divides $c$. One of $a,b$ being zero, it follows that $0$ divides $c$. We conclude that $lcm(a,b)=0$.

\end{proof}

We will now proceed to prove that a GCD domain can equivalently be defined as an integral domain such that every pair of elements admits an lcm. First, we need a lemma about the compatibility of gcd's with multiplication.

\begin{lemma}
Let $R$ be an integral domain. Let $a,b\in R$ and let $m \in R$. Suppose that $gcd(a,b)$ and $gcd(ma,mb)$ exist. Then $gcd(ma,mb)=m\cdot gcd(a,b)$ (up to multiplication by an invertible element).
\end{lemma}
\begin{proof}
If $m=0$ then, we have $gcd(ma,mb)=0=m\cdot gcd(a,b)$. We can therefore suppose that $m$ is nonzero.

1. Since $gcd(a,b)$ divides both $a$ and $b$, we obtain that $m\cdot gcd(a,b)$ divides both $ma$ and $mb$. Hence, $m\cdot gcd(a,b) \mid gcd(ma,mb)$. 

1. We know that $m$ divides both $ma$ and $mb$. Therefore, $m \mid gcd(ma,mb)$. It follows that $gcd(ma,mb)=mu$ for some $u \in R$. It follows that $mu$ divides both $ma$ and $mb$ i.e. there exists $s,t \in R$ such that $ma=msu$ and $mb=mtu$. Since $m$ is nonzero, we deduce that $a=su$ and $b=tu$. Thus $u$ divides both $a$ and $b$. Hence, $u \mid gcd(a,b)$. By multiplying by $m$, we obtain that $gcd(ma,mb) \mid m\cdot gcd(a,b)$. 

From the two previous points, we deduce that $gcd(ma,mb)$ and $m \cdot  gcd(a,b)$ are associated.
\end{proof}

We can now prove that:
\begin{theorem}
Let $R$ be an integral domain and let $a,b \in R \backslash \{0\}$. Then $lcm(a,b)$ exists iff $gcd(ma,mb)$ exists for every $m \in R \backslash \{0\}$. 
\end{theorem}
\begin{proof}
$\Leftarrow$: Suppose that $a,b \in R \backslash \{0\}$ are such that $gcd(ma,mb)$ exists for every $m \in R \backslash \{0\}$. Then, in particular $gcd(a,b)$ exists. We can thus write:
$$
a=gcd(a,b)s
$$
and
$$
b=gcd(a,b)t
$$
where $s,t \in R$.

We claim that $gcd(a,b)st$ is a lcm of $a$ and $b$.

Indeed, both $a$ and $b$ divide $gcd(a,b)st$. Moreover, suppose that $q \in R$ is such that $a \mid q$ and $b \mid q$. Then $ab \mid qb$ and $ab \mid qa$. It follows that $ab \mid gcd(qa,qb)=q\cdot gcd(a,b)$. Thus $gcd(a,b)gcd(a,b)st \mid q\cdot gcd(a,b)$. Since $a,b$ are not both zero, we have $gcd(a,b) \neq 0$. We deduce that $gcd(a,b)st \mid q$. We have verified the two conditions for $gcd(a,b)st$ to be a lcm of $a$ and $b$.

$\Rightarrow$: Suppose that $a,b \in R \backslash \{0\}$ are such that $lcm(a,b)$ exists. We can then write:
$$
ab=lcm(a,b)s
$$ 
and
$$
lcm(a,b)=at
$$
and
$$
lcm(a,b)=bu
$$
where $s,t,u \in R$. 

We claim that $s$ is a gcd of $a$ and $b$.

We can thus write:
$$
ab=ats
$$
and
$$
ab=bus
$$
from which it follows that $b=ts$ and $a=us$. Therefore, $s$ divides both $a$ and $b$. 

Suppose now that $v \in R$ is such that $v$ divides both $a$ and $b$. Then $v$ is nonzero. Moreover, $v \mid ab$. Write $ab=kv$ where $k \in R$. We have that $a \mid k$ (since $v \mid b$) and $b \mid k$ (since $v \mid a$). Therefore, $lcm(a,b) \mid k$. Write $k=lcm(a,b)l$ where $l \in R$. We obtain $ab=lcm(a,b)lv$. Hence, $lcm(a,b)s=lcm(a,b)lv$. Since both $a$ and $b$ are nonzero, we have that $lcm(a,b)$ is nonzero. It follows that $s=lv$. Therefore $v \mid s$. 

We have verified the two conditions for $s$ to be a gcd of $a$ and $b$. We can thus write $s=gcd(a,b)$. 

Let $m \in R \backslash \{0\}$. We want to show that $m\cdot gcd(a,b)$ is a gcd of $ma$ and $mb$. 

We know that $gcd(a,b)$ divides both $a$ and $b$. It follows that $m \cdot gcd(a,b)$ divides both $ma$ and $mb$.

Let $v \in R$ be such that $v$ divides both $ma$ and $mb$. Then $v$ is nonzero. Write $ma=v\alpha$ from which we have $mab=v\alpha b$. We obtain that $a \mid \alpha b$ (since $v \mid mb$). Moreover, $b \mid \alpha b$. It follows that $lcm(a,b) \mid \alpha b$. By multiplying by $v$, we get that $lcm(a,b)v \mid \alpha bv=mab$. Since $ab=lcm(a,b)gcd(a,b)$, we obtain that $v \mid m\cdot gcd(a,b)$.

We have verified the two conditions for $m\cdot gcd(a,b)$ to be a gcd of $ma$ and $mb$.
\end{proof}
We can therefore state:
\begin{corollary}
Let $R$ be an integral domain. Then $R$ is a GCD domain iff every pair of elements of $R$ admits an lcm.
\end{corollary}

### Properties of gcd's and lcm's

Let $R$ be a GCD domain. We already know that $gcd(ma,mb)=m \cdot gcd(a,b)$ for every $a,b,m \in R$. The same is true for lcm's.

\begin{proposition}
Let $R$ be a GCD domain. Let $a,b \in R$ and let $m \in R$. Then $lcm(ma,mb)=m\cdot lcm(a,b)$ (up to multiplication by a unit).
\end{proposition}
\begin{proof}
If $m=0$ then the two sides of the equation are zero. We can thus suppose that $m$ is nonzero.

1. We know that $a \mid lcm(a,b)$, that $b \mid lcm(a,b)$. Therefore, $ma \mid m\cdot lcm(a,b)$ and $mb \mid m\cdot lcm(a,b)$. Hence $\lcm(ma,mb) \mid m\cdot lcm(a,b)$.

1. We know that $m \mid ma$, therefore $m \mid lcm(ma,mb)$. It follows that we can write:
$$
lcm(ma,mb)=mu
$$
where $u \in R$. Hence both $ma$ and $mb$ divides $mu$. Since $m$ is nonzero, we obtain that both $a$ and $b$ divides $u$. Hence, $lcm(a,b) \mid u$. By multiplying by $m$, we obtain that $m \cdot lcm(a,b) \mid lcm(ma,mb)$.

From the two previous points, we conclude that $lcm(ma,mb)$ and $m \cdot lcm(a,b)$ are associated. 
\end{proof}

The compatibility of the product with gcd's and lcm's implies that the multiplicative monoid of an integral domain is a [[prelattice-ordered commutative monoid]].

### Other properties

Every GCD domain of [[Krull dimension|dimension]] at most 1 is a [[Bézout domain]].

## Examples

* The ring of integers $\mathbb{Z}$

* For any [[GCD domain]] $R$, the [[polynomial ring]] $R[x]$ on one generator 

* The ring of [[entire function|entire]] [[holomorphic functions]] on the [[complex plane]]

## See also ##

* [[GCD ring]]

* [[integral domain]]

* [[Bézout domain]]

* [[unique factorization domain]]

* [[Euclidean domain]]

* [[field]]

## References ##

* [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* [MS1449521](https://math.stackexchange.com/questions/1449521/gcd-domain-is-lcm-domain)

* [PlanetMath: an integral domain is lcm iff it is gcd](https://planetmath.org/anintegraldomainislcmiffitisgcd)

[[!redirects GCD domains]]
