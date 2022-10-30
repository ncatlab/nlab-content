
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
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

* whose underlying [[real vector space]] is is the [[direct sum]] $A \oplus A$, 

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
  \cdots
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
    DK(A) 
      &\overset{\simeq}{\longrightarrow}&
    \widetilde{DK}(A)
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

It is clear from Def. \ref{CayleyDicksonDoubleByAdjoiningFurtherGenerator} that for every element $x \in \widetilde{DK}(A)$ there is a _unique_ [[pair]] of elements $a,b \in A$ such that 

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

See also

* Wikipedia, _[Cayley&#8211;Dickson construction](https://en.wikipedia.org/wiki/Cayley%E2%80%93Dickson_construction)_


More:

* Daniel K. Biss, [[Daniel Dugger]], [[Daniel Isaksen]], _Large annihilators in Cayley-Dickson algebras_, 
 Communications in Algebra 36 (2), 632-664, 2008 ([arxiv:math/0511691](https://arxiv.org/abs/math/0511691))

* Daniel K. Biss, [[Daniel Christensen]], [[Daniel Dugger]], [[Daniel Isaksen]], _Large annihilators in Cayley-Dickson algebras II_, 	Boletin de la Sociedad Matematica Mexicana (3) 13(2) (2007), 269-292 ([arxiv:math/0702075](https://arxiv.org/abs/math/0702075))


* Daniel K. Biss, [[Daniel Christensen]], [[Daniel Dugger]], [[Daniel Isaksen]], _Eigentheory of Cayley-Dickson algebras_, 
Forum Mathematicum 21(5) (2009), 833-851 ([arxiv:0905.2987](https://arxiv.org/abs/0905.2987))






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


