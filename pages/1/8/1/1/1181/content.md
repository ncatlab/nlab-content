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


# Natural numbers object
* table of contents
{: toc}

## Idea

Recall that a [[topos]] is a [[category]] that behaves likes the category [[Set]] of [[set|sets]].  

A **natural numbers object** (NNO) in a topos is an [[object]] that behaves in that topos like the set $\mathbb{N}$ of [[natural number|natural numbers]] does in [[Set]]; thus it provides a formulation of the "axiom of infinity" in structural [[set theory]] (such as [[ETCS]]).  The definition is due to [[William Lawvere]] ([1963](#Law63)).


## Definition

### In a topos or cartesian closed category {#CCC}

A **natural numbers object** in a [[topos]] (or any [[cartesian closed category]]) $E$ with [[terminal object]] $1$ is 

* an [[object]] $\mathbb{N}$ in $E$ 

* equipped with 
  
  * a [[morphism]] $z :1 \to \mathbb{N}$ from the [[terminal object]] $1$;

  * a [[morphism]] $s : \mathbb{N} \to \mathbb{N}$ (successor);

* such that for every other [[diagram]] $1 \stackrel{q}{\to}A \stackrel{f}{\to} A$ there is a unique morphism $u : \mathbb{N} \to A$ such that

\begin{center}
  \begin{tikzcd}
    1 \ar[r, "z"] \ar[rd, "q"']        &
    \mathbb{N} \ar[r, "s"] \ar[d, "u"] &
    \mathbb{N} \ar[d, "u"]             \\
    & A \ar[r, "f"'] & A
  \end{tikzcd}
\end{center}

All this may be summed up by saying that a natural numbers object is an [[initial algebra|initial]] [[algebra for an endofunctor|algebra for the endofunctor]] $X \mapsto 1 + X$ (the functor underlying the "[[maybe monad]]").
Equivalently, it is an initial [[algebra for an endo-profunctor|algebra for the endo-profunctor]]  $Hom_E(1,=) \times Hom_E(-,=)$.

By the universal property, the natural numbers object is unique up to [[isomorphism]]. 

+-- {: .num_prop} 
###### Proposition 
Let $C, D$ be cartesian closed categories, and suppose $D$ has a natural numbers object $(\mathbb{N}, z: 1 \to \mathbb{N}, s: \mathbb{N} \to \mathbb{N})$. If $L: D \to C$ is a [[left adjoint]] that preserves the terminal object, then $(L \mathbb{N}, L z, L s)$ is a natural numbers object in $C$. 
=-- 

The proof is straightforward. It follows for example that the left adjoint part $f^\ast$ of a geometric morphism $f^\ast \dashv f_\ast: E \to F$ between toposes with natural numbers objects preserves the natural numbers object, and also that a [[Grothendieck quasitopos]] $Q$ presented by a [[site]] $(C, J)$ has a natural numbers object, since the [[reflective subcategory|reflection functor]] $L: Set^{C^{op}} \to Q$ preserves finite products and the terminal object in particular. 

### In a general category with finite products
{#withparams}

Note that this definition actually makes sense in any category $E$ having finite [[product]]s, such as a [[pretopos]].  However, if $E$ is not [[cartesian closed category|cartesian closed]], then it is better to explicitly assume a stronger version of this definition "with parameters" (which follows automatically when $E$ is cartesian closed, such as when $E$ is a topos). What this amounts to is demanding that $(\mathbb{N}, z, s)$ not only be a natural numbers object (in the above, unparametrized sense) in $E$, but that also, for each object $A$, this is preserved by the cofree coalgebra functor into the [[Kleisli category]] of the [[comonad]] $X \mapsto A \times X$ (which may be thought of as the category of maps parametrized by $A$). (Put another way, the finite product structure of $E$ gives rise to a canonical [[self-indexing]], and we are demanding the existence of an (unparametrized) NNO within this [[indexed category]], rather than just within the base $E$).

To be explicit: 

+-- {: .num_defn} 
###### Definition 
In a category with finite products, a _parametrized natural numbers object_ is an object $N$ together with maps $z: 1 \to N$, $s: N \to N$ such that given any objects $A$, $X$ and maps $f: A \to X$, $g: X \to X$, there is a unique map $\phi_{f, g}: A \times N \to X$ making the following diagram commute: 

$$\array{
A & \stackrel{\langle 1_A, z \circ !\rangle}{\to} & A \times N & \stackrel{1_A \times s}{\leftarrow} & A \times N \\
 & \mathllap{f} \searrow & \downarrow \mathrlap{\phi_{f, g}} & & \downarrow \mathrlap{\phi_{f, g}} \\
 & & X & \underset{g}{\leftarrow} & X
}$$ 
=--

In the [[internal language]], commutativity of this diagram says that $\phi_{f,g}(a,z) = f(a)$ and $\phi_{f,g}(a,s(n)) = g(\phi_{f,g}(a,n))$.

It may seem odd that $A$ only appears in the domain of $f$ and not $g$.  However, this simplification is inessential, and indeed we are free to add $N$ to the domain of $g$ as well:

+-- {: .num_prop}
###### Proposition
If $(N,z,s)$ is a parametrized natural numbers object in a category with finite products, then for any objects $A$, $X$ with maps $f:A\to X$, $g:A\times N\times X \to X$, there is a unique map $\phi_{f,g} : A\times N \to X$ such that, in the [[internal language]], $\phi_{f,g}(a,z) = f(a)$ and $\phi_{f,g}(a,s(n)) = g(a,n,\phi_{f,g}(a,n))$ for all $n:N$.
=--
+-- {: .proof}
###### Proof
Let $X' = A\times N\times X$, and define $f':A\to X'$ by $f'(a) = (a,z,f(a))$ and $g':X'\to X'$ by 

$$g'(a,n,x) = (a,n,g(a,n,x)).$$  

Then the assumption gives $\phi': A\times N \to X'$ such that 

$$\phi'(a,z) = f'(a) = (a,z,f(a)), \qquad \phi'(a,s(n)) = g'(\phi'(a,n)).$$

The composite $A \times N \xrightarrow{\phi'} X' \xrightarrow{\pi_1} A$ satisfies 

$$\pi_1 \phi'(a,z) = \pi_1(a,z,f(a)) = a, \qquad \pi_1\phi'(a,s(n)) = \pi_1 g'(\phi'(a,n)) = \pi_1 \phi'(a,n).$$  

Thus, by the uniqueness assumption, we have $\pi_1 \phi'(a,n) = a$ for all $a,n$.  By a similar argument, we have $\pi_2 \phi'(a,n) = n$ for all $a,n$.  Therefore, $\phi'(a,s(n)) = (a,n,g(a,n,\phi'(a,n)))$, and hence the composite $A\times N  \xrightarrow{\phi'} X' \xrightarrow{\pi_3} X$ is the desired $\phi_{f,g}$.
=--

The functions which are constructible out of the structure of a category with finite products and such a "parametrized NNO" are precisely the [[partial recursive function|primitive recursive]] ones. Specifically, the unique structure-preserving functor from the free such category $F$ into [[Set]] yields a bijection between $Hom_F(1, \mathbb{N})$ and the actual natural numbers, as well as surjections from $Hom_F(\mathbb{N}^m, \mathbb{N})$ onto the primitive recursive functions of arity $m$ for each finite $m$. With cartesian closure, however, this identification no longer holds, since non-primitive recursive functions (such as the [[partial recursive function|Ackermann function]]) become definable as well.

In this context an important class is the class of [[pretopos|pretoposes]] with a parametrized NNO - the so called [[arithmetic pretopos|arithmetic pretoposes]].

### In type theory

For the moment see at _[[inductive type]]_ the section _[Examples - Natural numbers](inductive+type#NaturalNumbers)_


## Finite colimit characterization

In a topos, the natural numbers object $\mathbb{N}$ is uniquely characterized by the following [[colimit]] conditions due to [[Peter Freyd]]: 

+-- {: .num_theorem #Freyd} 
###### Theorem 
In a topos, a triple $(\mathbb{N}, 0: 1 \to \mathbb{N}, s: \mathbb{N} \to \mathbb{N})$ is a natural numbers object if and only if 

1. The morphism $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ is an [[isomorphism]]; 

2. The diagram 
$$\mathbb{N} \stackrel{\overset{s}{\to}}{\underset{1}{\to}} \mathbb{N} \to 1$$ 
is a [[coequalizer]]. 
=-- 

The necessity of the first condition holds in any category with binary coproducts and a terminal object, and the necessity of the second holds in any category whatsoever. 

+-- {: .proof}
###### Proof of theorem \ref{Freyd}: necessity
For a category $C$ with binary coproducts and 1, the natural numbers object can be equivalently described as an [[initial algebra]] structure $(0, s): 1 + \mathbb{N} \to \mathbb{N}$ for the endofunctor $F(c) = 1 + c$ defined on $C$. Then condition 1 is a special case of [[initial algebra of an endofunctor|Lambek's theorem]], that the algebra structure map of an initial algebra is an isomorphism. 

As for condition 2, given $f: \mathbb{N} \to X$ such that $f = f \circ s$, the claim is that $f$ factors as 

$$\mathbb{N} \overset{!}{\to} 1 \overset{x}{\to} X$$

for some unique $x$, in fact for $x = f(0)$. Uniqueness is clear since $!: \mathbb{N} \to 1$, being a retraction for $0: 1 \to \mathbb{N}$, is epic. On the other hand, substituting either $f$ or $f(0) \circ !$ for $g$ in the diagram 

$$\array{ 
1 & \overset{0}{\to} & \mathbb{N} & \overset{s}{\to} & \mathbb{N} \\ 
 & ^\mathllap{f(0)} \searrow & \downarrow ^g & & \downarrow ^g \\ 
 & & X & \underset{1_X}{\to} & X
}$$ 

this diagram commutes, so that $f = f(0) \circ !$ by the uniqueness clause in the universal property for $\mathbb{N}$.
=--

+-- {: .proof}
###### Proof of theorem \ref{Freyd}: sufficiency
Here we just give an outline, referring to [(Johnstone)](#Johnstone), section D.5.1, for full details. Let $N$ be an object satisfying the two colimit conditions of Freyd. First one shows (see the lemma \ref{Peano} below) that $N$ has no nontrivial $F$-subalgebras. Next, let $A$ be any $F$-algebra, and let $i: B \to N \times A$ be the intersection of all $F$-subalgebras of $N \times A$. One shows that $\pi_1 \circ i: B \to N$ is an ($F$-algebra) isomorphism. Thus we have an $F$-algebra map $f: N \to A$. If $g: N \to A$ is any $F$-algebra map, then the equalizer of $f$ and $g$ is an $F$-subalgebra of $N$, and therefore $N$ itself, which means $f = g$. 
=-- 

+-- {: .num_lemma #Peano} 
###### Lemma 
Let $F$ be the endofunctor $F(X) = 1+X$. If $N$ satisfies Freyd's colimit conditions, then any $F$-subalgebra of $N$ is the entirety of $N$. 
=-- 

+-- {: .proof} 
###### Proof 
Following [(Johnstone)](#Johnstone), we may as well show that the smallest $F$-subalgebra $N'$ of $N$ (the internal intersection of all $F$-subalgebras) is all of $N$. Let $S \hookrightarrow N \times N$ be the union of the relation $R = \langle 1, s \rangle: N \to N \times N$ and its opposite, so that $S$ is a symmetric relation. Working in the Mitchell-B&#233;nabou language, one may check directly that the following formula is satisfied: 

$$\forall x, y: N (\langle x, y \rangle \in S) \Rightarrow ((x \in N') \Leftrightarrow (y \in N'))$$ 

Let us say a term $w$ of type $P N$ is $S$-**closed** if the formula 

$$\forall x, y: N (\langle x, y \rangle \in S) \Rightarrow ((x \in [w]) \Leftrightarrow (y \in [w]))$$ 

is satisfied. Now define a relation $T$ on $N$ by the subobject

$$\{\langle x, y \rangle \in N \times N: \forall w: P N (w \; is \; S closed) \Rightarrow ((x \in [w]) \Leftrightarrow (y \in [w])).$$ 

Observe that $T$ is an equivalence relation that contains $S$ and therefore $R$. It therefore contains the kernel pair of the coequalizer of $1$ and $s$; since this coequalizer is by assumption $N \to 1$, the kernel pair is all of $N \times N$. Also observe that since $N'$ is $S$-closed by definition, it is $T$-closed as well, and we now conclude 

$$\forall x, y \in N: (x \in N') \Leftrightarrow (y \in N')$$ 

so that, putting $y = 0: 1 \to N'$, we conclude that $x \in N \Rightarrow x \in N'$, i.e., that $N'$ is all of $N$. 
=-- 


+-- {: .un_remark} 
###### Remark 
A slightly alternative proof of sufficiency uses the theory of well-founded coalgebras, as given [here](http://ncatlab.org/toddtrimble/published/Initial+algebras+and+terminal+coalgebras). If $N$ is a fixpoint of the functor $F(X) = 1+X$, regarded as an $F$-[[coalgebra for an endofunctor|coalgebra]], then the internal union of well-founded subcoalgebras of $N$ is a natural numbers object $\mathbb{N}$. Then the subobject $\mathbb{N} \hookrightarrow N$ can also be regarded as a subalgebra; by the lemma, it is all of $N$. Thus $N$ is a natural numbers object. 
=--   

## Free constructions in a topos

In [[topos theory]] the existence of a natural numbers object (NNO) has a couple of far-reaching consequences. 

Firstly, the existence of a NNO in a topos $\mathcal{S}$ is equivalent to the existence of [[free object|free]] unary systems in $\mathcal{S}$, unary systems being objects with an [[endomorphism]] in $\mathcal{S}$. 

+-- {: .num_prop #free_object_with_endomorphism_in_topos}
###### Proposition
Let $\mathcal{S}$ be a topos and $\mathbf{unsys}(\mathcal{S})$ its category of internal unary systems. Then $\mathcal{S}$ has a NNO precisely if the forgetful functor $U:\mathbf{unsys}(\mathcal{S})\to \mathcal{S}$ has a left adjoint.
=--

Let $F:\mathcal{S}\to\mathbf{unsys}(\mathcal{S})$ be a left adjoint to the forgetful functor $U$, and let $1$ be a terminal object in $\mathcal{S}$.  Then $F(1)$ is a NNO in $\mathcal{S}$, by definition of an NNO. 

Secondly, it is a theorem due to C. J. Mikkelsen that the existence of a NNO in a topos $\mathcal{S}$ is equivalent to the existence of [[free monoid|free monoids]] in $\mathcal{S}$:

+-- {: .num_prop #free_monoids_in_topos}
###### Proposition
Let $\mathcal{S}$ be a topos and $\mathbf{mon}(\mathcal{S})$ its category of internal monoids. Then $\mathcal{S}$ has a NNO precisely if the forgetful functor $U:\mathbf{mon}(\mathcal{S})\to \mathcal{S}$ has a left adjoint.
=--

For a proof see Johnstone ([1977](#JT77),p.190).

It then is a theorem due to [[Andreas Blass]] ([1989](#Blass)) that $\mathcal{S}$ has a NNO precisely if $\mathcal{S}$ has an [[classifying topos for the theory of objects|object classifier]] $\mathcal{S}[\mathbb{O}]$.

A consequence of this, discussed in sec. B4.2 of (Johnstone 2002,I p.431), is that [[classifying topos|classifying toposes]] for [[geometric theories]] over $\mathcal{S}$ exist precisely if $\mathcal{S}$ has a NNO.

So from a different perspective, in a topos the existence of free objects over various gadgets like e.g. [[algebraic theory|algebraic theories]] or [[geometric theory|geometric theories]] (often) hinge on the existence of free unary systems or monoids, the intuition being that the free unary systems and free monoids permit to construct a free model _syntactically_ by providing for the (syntactic) building blocks needed for this process.

Notice that algebraic theories can nevertheless have free algebras even if the ambient topos lacks a NNO. This may happen for algebraic theories that have the property that the free algebra on a finite set of generators has a finite carrier e.g. in the topos $FinSet$ of finite sets [[graphic category|free graphic monoids]] exist.

## Examples

### In a sheaf topos
 {#ExamplesInASheafTopos}

In any [[Grothendieck topos]] $E = Sh(C)$ the natural numbers object is given by the [[constant sheaf]] on the [[set]] of ordinary natural numbers, i.e. by the [[sheafification]] of the [[presheaf]] $C^{op} \to Set$ that is constant on the set $\mathbb{N}$.

There are interesting cases in which such sheaf toposes contain objects that look like they ought to be natural numbers objects but do not satisfy the above axioms: for instance some of the models described at [[Models for Smooth Infinitesimal Analysis]] are sheaf toposes that contain besides the standard natural number object a larger object of **[[smooth natural numbers]]** that has [[generalized element]]s which are "infinite natural numbers" in the sense of [[nonstandard analysis]].


## Properties

### Transfer along inverse images
 {#Transfer}

+-- {: .num_prop}
###### Proposition

Natural number objects are preserved by [[inverse images]]:

let $f = (f^* \dashv f_*) : \mathcal{E} \underoverset{f_*}{f^*}{\leftrightarrows} \mathcal{F}$ be a [[geometric morphism]] of toposes. If $\mathbb{N} \in \mathcal{F}$ is a natural numbers object, then its [[inverse image]] $f^* \mathbb{N}$ is a natural numbers object in $\mathcal{E}$. 

=--

([Johnstone, lemma A.4.1.14](#Johnstone)). Of course, by the [finite colimit characterization](http://ncatlab.org/nlab/show/natural+numbers+object#finite_colimit_characterization_24), we need only the fact that inverse images preserve finite colimits and the terminal object. 

+-- {: .num_example}
###### Example

If $\mathcal{E}$ is a [[sheaf topos]], then there is a unique [[geometric morphism]] $(\Delta \dashv \Gamma): \mathcal{E} \underoverset{\Gamma}{\Delta}{\leftrightarrows} Set$, the [[global section]] geometric morphism, with the [[inverse image]] being the [[locally constant sheaf]] functor, it follows that 

$$
  \Delta(\mathbb{N}) \cong \Delta\left(\sum_{n: \mathbb{N}} 1\right) \cong \sum_{n: N} \Delta 1 \cong \sum_{n: \mathbb{N}} 1,
$$ 

with the evident successor and constant $0$, is the natural nunbers object in $\mathcal{E}$.  

=--

+-- {: .num_example}
###### Example

If $\mathcal{E}$ is a topos and $X \in \mathcal{E}$ an object, then the [[slice topos]] sits by an [[etale geometric morphism]] over $\mathcal{E}$

$$
  \mathcal{E}_{/X}
  \stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}

  \mathcal{E}
  \,,
$$

where the [[inverse image]] form the [[product]] with $X$. Hence for $\mathbb{N} \in \mathcal{E}$ a natural numbers object, the projection $(X \times \mathbb{N} \to X)$ is a natural numbers object in $\mathcal{E}_{/X}$.

=--

### Relation to rig objects

The initial [[rig]] object in a category with finite products, ($\mathbb{N},0:1\rightarrow\mathbb{N},1:1\rightarrow\mathbb{N},+:\mathbb{N}\times\mathbb{N}\rightarrow\mathbb{N},\times:\mathbb{N}\times\mathbb{N}\rightarrow\mathbb{N})$ with suitable commutative diagrams expressing the rig axioms and [[initial object|initiality]], has the structure of a natural numbers object given by the triple $(\mathbb{N}, 0:1\rightarrow\mathbb{N}, x+1:\mathbb{N}\rightarrow\mathbb{N})$. 

### Relation to object of integers

Given a natural numbers object $\mathbb{N}$ in a [[pretopos]], we can construct an [[integers]] [[integers object|object]] as follows.  Let $a, b\colon E \to \mathbb{N} \times \mathbb{N}$ be the [[kernel pair]] of the addition map ${+}\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$, and let $\pi_1, \pi_2\colon \mathbb{N} \times \mathbb{N} \to \mathbb{N}$ be the [[product]] projections. We define $\mathbb{Z}$ to be the [[coequalizer]] of the [[congruence]] $(\pi_1 \circ a, \pi_2 \circ b), (\pi_1 \circ b, \pi_2 \circ a)\colon E \to \mathbb{N} \times \mathbb{N}$.  A similar construction yields a [[rational numbers]] object $\mathbb{Q}$. 

For a [[real numbers]] object, rather more care is needed; see [[real numbers object]].


## Related concepts

* [[natural numbers]]

* [[natural numbers type]]

* [[Peano arithmetic]]

* [[free monoid]]

* [[arithmetic pretopos]]

* [[integers object]]

## References

* {#Law63}[[F. William Lawvere]], _[[Functorial Semantics of Algebraic Theories]]_, Ph.D. thesis Columbia University 1963. (Published with an author's comment as: TAC Reprint no.5 (2004) pp 1-121. ([abstract](http://www.tac.mta.ca/tac/reprints/articles/5/tr5abs.html))

* {#Ben91}[[Jean Bénabou]], _Some Remarks on Free Monoids in a Topos_, pp.20-29 in LNM **1488** Springer Heidelberg 1991.

* {#Blass} [[Andreas Blass]], _Classifying topoi and the axiom of infinity_, Algebra Universalis **26** (1989) pp.341-345.

* {#JT77}[[Peter Johnstone]], _Topos Theory_, Academic Press New York 1977. (Dover reprint Minneola 2014, chap. 6)

* {#Johnstone}[[Peter Johnstone]], _[[Sketches of an Elephant]]_, Oxford UP 2002.

In [[elementary (infinity,1)-toposes]]:

* [[Nima Rasekh]], _Every Elementary Higher Topos has a Natural Number Object_, ([arXiv:1809.01734](https://arxiv.org/abs/1809.01734))
 


[[!redirects natural numbers object]]
[[!redirects natural numbers objects]]
[[!redirects natural number object]]
[[!redirects natural number objects]]
[[!redirects natural-numbers object]]
[[!redirects natural-numbers objects]]
[[!redirects natural-number object]]
[[!redirects natural-number objects]]
[[!redirects NNO]]
[[!redirects NNOs]]