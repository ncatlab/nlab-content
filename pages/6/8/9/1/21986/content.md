+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

# Integers object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

An **integers object** [[internalization|internal to]] a topos is an [[object]] that behaves in that topos like the set $\mathbb{Z}$ of [[integers]] does in [[Set]].

## Definition

### In a topos or cartesian closed category {#CCC}

An **integers object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbb{Z}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $z:1 \to \mathbb{Z}$ from the [[terminal object]] $1$;

  * an [[isomorphism]] $s : \mathbb{Z} \cong \mathbb{Z}$ ([[successor]]),

such that for all objects $A$ with morphism $z_A:1 \to A$ and isomorphism $s_A:A \cong A$, there is a unique morphism $u_A:\mathbb{Z} \to A$ such that $u_A \circ z = z_A$ and $u_A \circ s = s_A \circ u_A$. 

By the [[universal property]], the integers object is unique up to [[isomorphism]]. 

### In a closed symmetric monoidal category

One could generalize the above definition of an integers object to any [[closed monoidal category|closed]] [[symmetric monoidal category]]: [[pointed objects in a monoidal category|pointed objects in a symmetric monoidal category]] are represented by morphisms out of the [[tensor unit]]. Thus, an integers object in a closed symmetric monoidal category $C$ with [[tensor unit]] $1$ is

* an [[object]] $\mathbb{Z}$ in $C$ 

* equipped with 
  
  * a [[morphism]] $z :1 \to \mathbb{Z}$ from the [[tensor unit]] $1$;

  * an [[isomorphism]] $s : \mathbb{Z} \cong \mathbb{Z}$ (successor);

such that for all objects $A$ with morphism $z_A:1 \to A$ and isomorphism $s_A:A \cong A$, there is a unique morphism $u_A:\mathbb{Z} \to A$ such that $u_A \circ z = z_A$ and $u_A \circ s = s_A \circ u_A$. 

## Free construction in a topos

The existence of an integers object in a topos $\mathcal{S}$ is equivalent to the existence of [[free group|free groups]] in $\mathcal{S}$:

+-- {: .num_prop #free_groups_in_topos}
###### Proposition
Let $\mathcal{S}$ be a topos and $\mathbf{Grp}(\mathcal{S})$ its category of internal [[group objects]]. Then $\mathcal{S}$ has an integers object precisely if the forgetful functor $U:\mathbf{Grp}(\mathcal{S})\to \mathcal{S}$ has a left adjoint.
=--

## Construction from natural numbers objects
Suppose the topos $E$ has a [[natural numbers object]] $\mathbb{N}$. Then an integers object $\mathbb{Z}$ is a [[filtered colimit]] of objects 

$$\mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \mathbb{N} \stackrel{1 + (-)}{\to} \ldots$$ 

whereby $-n:1\rightarrow\mathbb{Z}$ is represented by the morphism $z:1\rightarrow\mathbb{N}$ in the $n^{th}$ copy of $\mathbb{N}$ appearing in this diagram (starting the count at the $0^{th}$ copy). The resulting induced map to the colimit 

$$\mathbb{N} \times \mathbb{N} \cong \sum_{m \in \mathbb{N}} \mathbb{N} \to \mathbb{Z}: (m, n) \mapsto n-m$$ 

imparts a monoid structure (in fact a group structure) on $\mathbb{Z}$ descended from the monoid structure on $\mathbb{N} \times \mathbb{N}$. 

## Examples

There are many examples of natural numbers objects. 

### In closed symmetric monoidal categories

\begin{example}
The [[integers]] are the integers object in the [[closed monoidal category|closed]] [[symmetric monoidal category]] [[Set]]. 
\end{example}

\begin{example}
The [[disjoint union]] $\mathbb{Z} + \{\infty\}$ is the [[integers object]] in the closed symmetric monoidal category of [[pointed sets]] $Set_*$, with $z:\mathbb{2} \to \mathbb{Z} + \{\infty\}$ taking the [[boolean]] [[true]] to $\infty$ and [[false]] to $0$ and $s:\mathbb{Z} + \{\infty\} \cong \mathbb{Z} + \{\infty\}$ taking integers to its successor and $\infty$ to $\infty$.
\end{example}

\begin{example}
The underlying abelian group of the [[ring of Laurent polynomials]] $\mathbb{Z}[X, X^{-1}]$ is the integers object in the closed symmetric monoidal category [[Ab]], with $z:\mathbb{Z} \to \mathbb{Z}[X, X^{-1}]$ taking [[integers]] to constant [[Laurent polynomials]] and the [[abelian group]] [[isomorphism]] $s:\mathbb{Z}[X, X^{-1}] \cong \mathbb{Z}[X, X^{-1}]$ multiplying Laurent polynomials by the indeterminant $X$. 
\end{example}

\begin{example}
More generally, given a [[commutative ring]] $R$, the underlying $R$-module of the [[ring of Laurent polynomials]] $R[X, X^{-1}]$ is the integers object in the closed symmetric monoidal category [[RMod]], with $z:R \to R[X, X^{-1}]$ taking [[scalars]] to constant [[Laurent polynomials]] and the [[linear isomorphism]] $s:R[X, X^{-1}] \cong R[X, X^{-1}]$ multiplying Laurent polynomials by the indeterminant $X$. 
\end{example}

### In a sheaf topos
 {#ExamplesInASheafTopos}

In any [[Grothendieck topos]] $E = Sh(C)$ the integers object is given by the [[constant sheaf]] on the [[set]] of ordinary integers, i.e. by the [[sheafification]] of the [[presheaf]] $C^{op} \to Set$ that is constant on the set $\mathbb{Z}$.

Similar to the case for [[natural numbers objects]], there are interesting cases in which such sheaf toposes contain objects that look like they ought to be integers objects but do not satisfy the above axioms: for instance some of the models described at [[Models for Smooth Infinitesimal Analysis]] are sheaf toposes that contain besides the standard integers object a larger object of **[[smooth natural numbers|smooth integers]]** that has [[generalized element]]s which are "infinite integers" in the sense of [[nonstandard analysis]].

## Properties

### Inverse

By definition of [[isomorphism]], there is an [[inverse]] [[isomorphism]] $p:\mathbb{Z} \cong \mathbb{Z}$, where $p \circ s = \mathrm{id}_\mathbb{Z}$ and $s \circ p = \mathrm{id}_\mathbb{Z}$. 

### Initial ring object

In a category with finite products, the initial [[ring object]], an object $\mathbb{Z}$ with global elements $0:1\rightarrow\mathbb{Z}$ and $1:1\rightarrow\mathbb{Z}$, a morphism $-:\mathbb{Z}\rightarrow\mathbb{Z}$, morphsims $+:\mathbb{Z}\times\mathbb{Z}\rightarrow\mathbb{Z}$ and $\times:\mathbb{Z}\times\mathbb{Z}\rightarrow\mathbb{Z}$, and suitable commutative diagrams expressing the ring axioms and [[initial object|initiality]], has the structure of an integers object given by $z = 0$ and $s = x + 1$. 

## Related concepts

* [[integers]]

* [[integers type]]

* [[natural numbers object]]

* [[free group]]

* [[ring object]]

* [[circle object]]


[[!redirects integers object]]
[[!redirects integers objects]]
[[!redirects integer object]]
[[!redirects integer objects]]