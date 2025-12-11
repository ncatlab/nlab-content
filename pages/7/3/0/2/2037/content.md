
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include algebra - contents]]
=--
=--
=--


# Cayley--Dickson construction
* table of contents
{: toc}

## Idea

The _Cayley-Dickson construction_ or _Cayley-Dickson double_ ([Dickson 1919, (6)](#Dickson1919)) takes a [[real numbers|real]] [[star-algebra]] $A$ to a new real [[star-algebra]] whose elements are [[pairs]] of elements of $A$, in generalization of how the [[complex numbers]] arise as a doubling of the [[real numbers]].

When iteratively applied to the [[real numbers]], regarded as a [[star-algebra]] with [[identity morphism|trivial]] [[involution]], the Cayley-Dickson construction yields, consecutively, the [[complex numbers]], then the [[quaternions]], then the [[octonions]] (thus all four [[real normed division algebras]]), then the [[sedenions]], ...


## Definition


Let $A$ be an [[nonassociative algebra|possibly nonassociative]] [[star-algebra]] over the [[field]] $\mathbb{R}$ of [[real numbers]]: an algebra equipped with an [[involution]] $\overline(-) \colon x \mapsto \overline{x}$ which is an [[antiautomorphism]].  (Actually, $\mathbb{R}$ could be replaced by any [[commutative ring]] in the definitions, although some properties may depend on this ring.)

### Definition in components

+-- {: .num_defn #CayleyDicksonDoubleInComponents}
###### Definition
**(Cayley-Dickson construction in components)**

The  _Cayley--Dickson double_ of the [[real numbers|real]] [[star-algebra]] $A$ is the [[real numbers|real]] [[star-algebra]] $CD(A)$

* whose underlying [[real vector space]] is the [[direct sum]] $A \oplus A$, 

* whose multiplication is given by

  \[
    \label{ProductInComponents}
    (a,b)      
    (c, d) 
     \;\coloneqq\; 
    (a c - d \overline{b}, \overline{a} d + c b)
  \]

* whose star-[[involution]] is given by

  \[
    \label{InvolutionInComponents}
    \widebar{(a,b)} 
    \;\coloneqq\;
    (\overline{a},-b)
   \,.
  \]


=--

([Dickson 1919, (6)](#Dickson1919))

### Definition by generators and relations
 {#DefinitionByGeneratorsAndRelations}

+-- {: .num_defn #CayleyDicksonDoubleByAdjoiningFurtherGenerator}
###### Definition
**(Cayley-Dickson double by [[generators and relations]])

The _Cayley-Dickson double_ of a [[real numbers|real]] [[star-algebra]] $A$ is the [[real numbers|real]] [[star-algebra]] $\widetilde{CD}(A)$ obtained by adjoining one generator $\ell$ to $A$ subject to the following [[generators and relations|relations]]:

\[
  \label{TheNewGenerator}
  \ell^2 \;=\; -1
  \,,
  \phantom{AAA}
  \overline{\ell}
  \;=\;
  - \ell
\]

and

\[
  \label{DicksonRelations}
  a (\ell b) 
  = 
  \ell (\overline{a} b)
  \,,
  \phantom{AA}
  (a \ell) b 
  = 
  (a \overline{b}) \ell
  \,,
  \phantom{AA}
  (\ell a) (b \ell)
  = 
  - \overline{a b}
\]

for all $a, b \in A$.

=--

([Baez 02, second half of 2.2](#Baez02))

+-- {: .num_lemma #InducedRelations}
###### Lemma
(**induced relations**)

The relation in Def. \ref{CayleyDicksonDoubleByAdjoiningFurtherGenerator} imply the following further relations:

\[
  \label{al}
  a \ell \;=\; \ell \overline{a}
  \,,
  \phantom{AA}
  \ell a \;=\; \overline{a} \ell
\]

\linebreak

\[
  (\ell a) b 
  \;=\;
  \ell (b a)
  \,,
  \phantom{AA}
  a (b \ell)   
  \;=\;
  (b a) \ell
\]

\linebreak

\[
  \label{laTimeslb}
  (\ell a) (\ell b) 
  \;=\;
  - b \overline{a}
  \,,
  \phantom{AA}
  (a \ell) (b \ell)
  \;=\;
  - \overline{b} a
\]

for all $a, b \in A$.

=--

+-- {: .proof}
###### Proof

Using (eq:DicksonRelations) we have:

\[
  \begin{aligned}
  a \ell 
  & =
  a (\ell 1)
  \\
  & =
  \ell (\overline{a} 1)
  \\
  & =
  \ell \overline{a}
  \end{aligned}
  \phantom{AAA}
  ,
  \phantom{AAA}
  \begin{aligned}
  \ell a
  & =
  (1 \ell) a
  \\
  & =
  (1 \overline{a}) \ell
  \\
  & =
  \overline{a} \ell
  \end{aligned}
\]

Using this and (eq:DicksonRelations) we have:

\[
  \label{lab}
  \begin{aligned}
    (\ell a) b
    & =
    (\overline{a} \ell ) b
    \\
    & =
    (\overline{a} \overline{b}) \ell
    \\
    & =
    \ell \overline{  
      \overline{a} \overline{b}
    }
    \\ 
    & =
    \ell (b a)
  \end{aligned}
  \phantom{AAA}
  ,
  \phantom{AAA}
  \begin{aligned}  
    a (b \ell)
    & =
    a (\ell \overline{b})
    \\
    & = \ell( \overline{a} \overline{b} )
    \\
    & =

    \overline{
      \overline{a} \overline{b}
    }
    \ell
    \\
    & =
    (b a) \ell
  \end{aligned}
\]

and

\[
  \label{lalb}
  \begin{aligned}
  (\ell a) (\ell b)
  & =
  (\ell a) (\overline{b} \ell)
  \\
  & =
  - \overline{ a \overline{b} }
  \\
  & =
  - b \overline{a}
  \end{aligned}
  \phantom{AAA}
  ,
  \phantom{AAA}
  \begin{aligned}
    (a \ell) (b \ell)
    & =
    (\ell \overline{a}) (b \ell)
    \\
    & =
    - \overline{ \overline{a} b }
    \\
    & =
    - \overline{b} a
  \end{aligned}
\]

=--


### Equivalence of the definitions



+-- {: .num_prop}
###### Proposition

Definition \ref{CayleyDicksonDoubleInComponents} and Definition \ref{CayleyDicksonDoubleByAdjoiningFurtherGenerator} are equivalent, in that we have an [[isomorphism]] of [[real numbers|real]] [[star-algebras]]:

$$
  \array{ 
    \phi
    & 
    CD(A) 
      &\overset{\simeq}{\longrightarrow}&
    \widetilde{CD}(A)
    \\
    &
    (a,b)
    &\mapsto&
    a + \ell b
  }
$$

=--

+-- {: .proof}
###### Proof

It is clear from Def. \ref{CayleyDicksonDoubleByAdjoiningFurtherGenerator} that for every element $x \in \widetilde{CD}(A)$ there is a _unique_ [[pair]] of elements $a,b \in A$ such that 

$$
  x = a + \ell b \;=\; \phi(a,b)
  \,.
$$

This means that $\phi$ is a [[linear isomorphism]] of the underlying [[real vector spaces]]. Hence it only remains to check that $\phi$ is indeed an [[algebra homomorphism]] and that it respects the [[involution]].

To see that $\phi$ is an [[algebra homomorphism]], we multiply out and then use the relations (eq:lab) and (eq:lalb) from Lemma \ref{InducedRelations}:

$$
  \begin{aligned}
    \phi(a,b) \phi(c,d)
    & =
    (a + \ell b)
    (c + \ell d)
    \\
    & =
    a c + (\ell b)(\ell d)
    +
    a (\ell d) + (\ell b) c
    \\
    & =
    a c - d \overline{b}
    +
    \ell ( 
      \overline{a} d  
      + 
      c b
    )
    \\
    & 
    = 
    \phi(a c - d \overline{b}, \overline{a} d + c b)
  \end{aligned}
$$

Here in the last line we indeed find the component formula (eq:ProductInComponents).

To see that $\phi$ respects the involution we use (eq:TheNewGenerator) from Def. \ref{CayleyDicksonDoubleByAdjoiningFurtherGenerator} and (eq:al) from Lemma \ref{InducedRelations}:

$$
  \begin{aligned}
    \overline{\phi(a,b)}
    & =
    \overline{ a + \ell b }
    \\
    & =
    \overline{a} + \overline{\ell b}
    \\
    & =
    \overline{a} - \overline{b} \ell
    \\
    & = 
    \overline{a} - \ell b
    \\
    & = \phi( \overline{a}, -b )
    \,.
  \end{aligned}
$$

Here in the last line we indeed find the component formula (eq:InvolutionInComponents).

=--

\linebreak


## Properties


The map $a\mapsto (a,0)$ is a [[monomorphism]] $A\to A^2$. If $A$ is [[unital algebra|unital]] with unit $1$ then $A^2$ is unital with unit $(1,0)$. In the unital case, the element $\mathrm{i} \coloneqq (0,1)$ has the property $\mathrm{i}^2 = -1 \coloneqq (-1,0)$, and we may write $(a,b)$ as $a + b \mathrm{i}$ (while $a + \mathrm{i} b = (a,\overline{b})$).  For this reason, we may write $A[\mathrm{i}]$ in place of $A^2$, at least when $A$ is unital.


Generally speaking, the double $A^2$ of an algebra $A$ has a nice property iff $A$ is one level nicer.  For simplicity, assume that $A$ is unital (so that $\mathbb{R}$ is a subalgebra).  Since $\overline{\mathrm{i}} = -\mathrm{i}$, we see that the involution on $A^2$ is trivial iff the involution on $A$ is trivial and $A$ further has $2 = 0$.  Since $\mathrm{i} a = \overline{a} \mathrm{i}$, $A^2$ is [[commutative algebra|commutative]] iff $A$ is commutative and the involution in $A$ is trivial.  Since $a (b \mathrm{i}) = (b a) \mathrm{i}$, $A^2$ is [[associative algebra|associative]] iff $A$ is associative and commutative. Finally, $A^2$ is [[alternative algebra|alternative]] iff $A$ is associative (and hence also alternative).


## Examples

\begin{imagefromfile}
    "file_name": "QuaternionOctonionMultiplicationTable.jpg",
    "float": "right",
    "width": 400,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": ""
\end{imagefromfile}


The standard example is the sequence of consecutive doubles starting with $\mathbb{R}$ itself (with the [[identity map]] as involution); these are the __Cayley--Dickson algebras__: the [[real numbers]] $\mathbb{R}$, the [[complex numbers]] $\mathbb{C}$, the [[quaternions]] $\mathbb{H}$, the [[octonions]] (or Cayley numbers) $\mathbb{O}$, 

These are the [[real normed division algebras]]


The diagram on the right shows a basis of [[imaginary number|imaginary]] [[octonions]] obtained via Cayley-Dickson doubling from a standard basis $\{i,j,k\}$ of [[imaginary number|imaginary]] [[quaternions]].


\linebreak

\linebreak

\linebreak


Next, the CD-double of the [[octonions]] is the [[sedenions]] $\mathbb{S}$, etc. , followed by further algebras which are not [[division algebras]].  
All of these algebras are [[power-associative algebra|power-associative]], [[flexible algebra|flexible]], and unital, and have all [[inverse elements]]; the subalgebra with $\overline{x} = x$ is always just $\mathbb{R}$.

## Cayley-Dickson-Albert construction

The Cayley-Dickson construction described above was slightly generalized in [Section 5 of Albert (1942)](#Alb42CDA), where the multiplication is further modified by a parameter $\gamma$ in the [[ground field]]. This process constructs an algebra $A^{\gamma}$ starting from a unital algebra $A$ of order $n$ over a field $F$ endowed with an [[involution]] $J:A\to A$ over $F$ such that for all $x\in A$:

* $x+ J(x) \in F$,

* $x J(x) = J(x) x \in F$.

To construct $A^{\gamma}$, one chooses a parameter $\gamma\in F$, and on the vector space $A\oplus A$ one defines a product

$$
(g_1 ,g_2 )\cdot (h_1, h_2 ) = (g_1 h_1 + \gamma J(h_2) g_2 , h_2 g_1 +g_2 J(h_1 ))
$$

and an involution $K$ on $A^{\gamma}$ as

$$
K((g_1, g_2 ))= (J(g_1) , -g_2)
$$

In particular, for $F=\mathbb{R}$ this process allows to get the [*split-*](composition+algebra#split_composition_algebras) variants of the real division algebra, cf.:

* [[split-complex numbers]]

* [[split quaternions]]

* [[split octonions]]

## Higher algebra

[Albuquerque & Majid (1999)](#AM99quasi) describe the Cayley-Dickson process from a different point of view. The quaternions, and octonions are realized as $\mathbb{Z}_2^n$ [[group algebra|group algebras]] over the reals *twisted* by a group $n$-cocycle $\omega\in Z^n(\mathbb{Z}_2^n,\mathbb{R}^{\times})$, for $n=2,3$, respectively.

In more detail, the quaternions are described as the group algebra $\mathbb{R}[\mathbb{Z}_2\times\mathbb{Z}_2]$ where the group multiplication is twisted by a cocycle $\omega(g,h)$. The 2-cocycle condition of such a function implies that the quaternions are associative. On the other hand, the octonions are realized as a group algebra $\mathbb{R}[\mathbb{Z}_2\times\mathbb{Z}_2\times\mathbb{Z}_2 ]$ where the function $\omega(g,h)$ twisting the multiplication is no longer a 2-cocycle. One of the effects of this is that the octonions are no longer associative or, rather, that they satisfy a nontrivial associativity condition, in the sense of a [[quasi-Hopf algebra]]. This nontrivial associativity condition is witnessed by a group $3$-cocycle in $Z^3(\mathbb{Z}_2\times \mathbb{Z}_2\times \mathbb{Z}_2, \mathbb{R}^{\times})$. Notably, this $3$-cocycle turns out to be a $3$-coboundary, so that its cohomology class is trivial.

This point of view also clarifies the common claim that algebras in the Cayley-Dickson process lose "nice" properties after more iterations. Rather, a more precise claim is that these nice properties are weakened. In the case of the octonions, these are better regarded as associative *up to* a nontrivial cocycle.

This highlights that a more suitable point of view to study the algebras arising in the Cayley-Dickson process is [[higher algebra]]. As noted in e.g. ([p.8 of Baez (2002)](#Baez02)), the octonions are indeed associative, when viewed as a [[monoid object]] [[internalization|internal]] to the [[tensor category]] which is the [[fusion category]] of $\mathbb{Z}_2^3$-graded real vector spaces with nontrivial [[associator]] defined by the twisting $3$-cocycle.

This seems to suggest a pattern regarding the rest of the $2^n$-gons, as of now unproven(?). For instance, the sedenions could be realized as a twist of the group algebra $\mathbb{R}[\mathbb{Z}_2^4]$ by a 4-cocycle $Z^4(\mathbb{Z}_2^4,\mathbb{R}^{\times})$, and as such would have fewer nice properties *as a 1-algebra*. Yet as a higher algebra it would retain its nice properties: it would correspond to the [[fusion 2-category]] of $\mathbb{Z}_2^4$-graded [[2-vector space|2-vector spaces]] twisted by a group 4-cocycle.


## Related concepts 

* [[composition algebra]]


## References

Named after [[Arthur Cayley]] and [[Leonard Dickson]].

The original article:


* {#Dickson1919} [[Leonard Dickson]], _On Quaternions and Their Generalization and the History of the Eight Square Theorem_, 
Annals of Mathematics, Second Series, Vol. 20, No. 3 (Mar., 1919), pp. 155-171 ([jstor:1967865](https://www.jstor.org/stable/1967865))


Review and introduction:

*  [[M M Postnikov]], _Lectures on geometry, Semester V: Lie groups and Lie algebras_, Lec. 14 (russian and english editions)

* {#Baez02} [[John Baez]], _[The Cayley--Dickson construction](http://math.ucr.edu/home/baez/octonions/node5.html)_, in _[The octonions](http://math.ucr.edu/home/baez/octonions/)_, Bull. Amer. Math. Soc. 39 (2002), 145-205, [doi](http://dx.doi.org/10.1090/S0273-0979-01-00934-X)

* [[John Baez]], _[This Week's Finds --- Week 59](http://math.ucr.edu/home/baez/week59.html)_

* [[Tevian Dray]], [[Corinne Manogue]], Section 5.1 of: _The Geomety of Octonions_, World Scientific 2015 ([doi:10.1142/8456](https://doi.org/10.1142/8456))


See also

* Wikipedia, _[Cayley&#8211;Dickson construction](https://en.wikipedia.org/wiki/Cayley%E2%80%93Dickson_construction)_


More:

* Daniel K. Biss, [[Daniel Dugger]], [[Daniel Isaksen]], _Large annihilators in Cayley-Dickson algebras_, 
 Communications in Algebra 36 (2), 632-664, 2008 ([arxiv:math/0511691](https://arxiv.org/abs/math/0511691))

* Daniel K. Biss, [[Daniel Christensen]], [[Daniel Dugger]], [[Daniel Isaksen]], _Large annihilators in Cayley-Dickson algebras II_, 	Boletin de la Sociedad Matematica Mexicana (3) 13(2) (2007), 269-292 ([arxiv:math/0702075](https://arxiv.org/abs/math/0702075))


* Daniel K. Biss, [[Daniel Christensen]], [[Daniel Dugger]], [[Daniel Isaksen]], _Eigentheory of Cayley-Dickson algebras_, 
Forum Mathematicum 21(5) (2009), 833-851 ([arxiv:0905.2987](https://arxiv.org/abs/0905.2987))

On the generalization of the Cayley-Dickson construction:

* [[Abraham Adrian Albert]], *Quadratic forms permitting composition,* Ann. of Math. (2) **43** (1942), 161–177. ([doi](https://doi.org/10.2307/1968887))

On the Cayley-Dickson construction in terms of [[quasi-Hopf algebra|quasi-Hopf algebras]]:

* {#AM99quasi} Helena Albuquerque, [[Shahn Majid]]. *Quasialgebra Structure of the Octonions*. Journal of Algebra
Volume 220, Issue 1, 1 October 1999, Pages 188-224. ([doi](https://doi.org/10.1006/jabr.1998.7850))



[[!redirects Cayley-Dickson construction]]
[[!redirects Cayley–Dickson construction]]
[[!redirects Cayley--Dickson construction]]

[[!redirects Cayley-Dickson constructions]]
[[!redirects Cayley–Dickson constructions]]
[[!redirects Cayley--Dickson constructions]]

[[!redirects Cayley-Dickson double]]
[[!redirects Cayley–Dickson double]]
[[!redirects Cayley--Dickson double]]

[[!redirects Cayley-Dickson doubles]]
[[!redirects Cayley–Dickson doubles]]
[[!redirects Cayley--Dickson doubles]]

[[!redirects Cayley-Dickson double algebra]]
[[!redirects Cayley–Dickson double algebra]]
[[!redirects Cayley--Dickson double algebra]]

[[!redirects Cayley-Dickson double algebras]]
[[!redirects Cayley–Dickson double algebras]]
[[!redirects Cayley--Dickson double algebras]]

[[!redirects double of an algebra with involution]]
[[!redirects double of algebra with involution]]
[[!redirects doubles of algebras with involution]]

[[!redirects double of a star-algebra]]
[[!redirects doubles of star-algebras]]
[[!redirects double of a *-algebra]]
[[!redirects doubles of *-algebras]]

[[!redirects Cayley-Dickson algebra]]
[[!redirects Cayley-Dickson algebras]]
[[!redirects Cayley–Dickson algebra]]
[[!redirects Cayley–Dickson algebras]]
[[!redirects Cayley--Dickson algebra]]
[[!redirects Cayley--Dickson algebras]]

[[!redirects Dickson double]]
[[!redirects Dickson doubles]]
[[!redirects Dickson double construction]]
[[!redirects Dickson double constructions]]


