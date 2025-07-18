
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea  ##

A [[model category]] $C$ is _cofibrantly generated_ if there is a [[set]]
(meaning: [[small set]], not a [[proper class]]) of [[cofibrations]] as well as one of [[acyclic cofibrations]], such that all other cofibrations 
and acyclic cofibrations, respectively,
are _generated_ from these, in some sense.

## Definition ##

We need the following general terminology:

\begin{definition}\label{CellsAndInjectives}
**(cells and injectives)**
\linebreak
Let $C$ be a [[category]] with all [[colimits]] and let $S \subset Mor(C)$ a [[class]] of [[morphisms]]. We write:

* $rlp(S)$  for the collection of morphisms with the _right_ 
  [[lifting property]];
  
* $llp(S)$ for the collection of morphisms with the _left_  [[lifting property]] with respect to $S$.

Moreover, we also write, now for $I \subset Mor(C)$: 

* $cell(I)$ for the [[relative cell complexes]], the class of morphisms obtained by [[transfinite composition]] of [[pushouts]] of [[coproducts]] of elements in $I$;

* $cof(I)$ for the class of [[retracts]] (in the [[arrow category]] $Arr(C)$) of elements in $cell(I)$;

* $inj(I) \coloneqq rlp(I)$ for the class of morphisms with the [[right lifting property]] with respect to $I$, the _$I$-[[injective morphisms]]_.

\end{definition}

+-- {: .num_defn #CofibrantlyGeneratedModelCategory}
###### Definition 

A [[model category]] $\mathcal{C}$ is **cofibrantly generated** if there are [[small set|small]] [[sets]] of morphisms $I, J \subset Mor(\mathcal{C})$ such that

* $cof(I)$ is precisely the collection of cofibrations of $C$;

* $cof(J)$ is precisely the collection of acyclic cofibrations in $C$; and

* $I$ and $J$ permit the [[small object argument]].

=--


Since $I$ and $J$ are assumed to admit the [[small object argument]] the collection of cofibrations and acyclic cofibrations has the following simpler characterization:

+-- {: .num_prop #RetractsOfCellComplexesExchaustLLPOfRLP}
###### Proposition

In a cofibrantly generated model category (Def. \ref{CofibrantlyGeneratedModelCategory}) we have

* $cof(I) = llp\big(rlp(I)\big)$,

* $cof(J) = llp\big(rlp(J)\big)$.

=--

And therefore the fibrations form precisely $rlp(J)$ and the acyclic fibrations precisely $rlp(I)$.

+-- {: .proof}
###### Proof

The argument is the same for $I$ and $J$. So take $I$. 

By definition we have $I \subset llp\big(rlp(I)\big)$ and it is readily checked that collections of morphisms given by a [[left lifting property]] are stable under [[pushouts]], [[transfinite composition]] and [[retracts]] (see [here](injective+or+projective+morphism#ClosurePropertiesOfInjectiveAndProjectiveMorphisms) for details). So $cof(I) \subset llp\big(rlp(I)\big)$.

For the converse inclusion we use the [[small object argument]]: let $f \colon X \to Z$ be in $llp\big(rlp(I)\big)$. The small object argument produces a factorization
$f : X \stackrel{f' \in cof(I)}{\to} Y \stackrel{f''\in rlp(I)}{\to} Z$. 

Finally we apply the "[[retract argument]]": It follows that $f$ has the left [[lifting property]] with respect to $f''$ which yields a morphism $\sigma$ in

$$
  \array{
    X 
    &\overset{f'}{\longrightarrow}& Y
    \\
    \mathllap{{}^{f}}
    \big\downarrow 
    &{}^\sigma\nearrow&
    \big\downarrow
    \mathrlap{{}^{f''}}
    \\
    Z 
    &\underset{=}{\longrightarrow}& 
    Z
  }
$$

which exhibits $f$ as a [[retract]] of $f'$

$$
  \array{
    X 
    &\overset{=}{\longrightarrow}& 
    X 
    &\overset{=}{\longrightarrow}& 
    X
    \\ 
    \big\downarrow
    {\mathrlap{{}^f}} 
    && 
    \big\downarrow
    {\mathrlap{{}^{f'}}} 
    && 
    \big\downarrow
     {\mathrlap{{}^f}}
     \\
     Z 
     &\underset{\sigma}{\longrightarrow}&
     Y
     &\underset{f''}{\longrightarrow}&
     Z
     \,.
  }
$$

Therefore $f \in cof(I)$.

=--



## Properties 

### Recognition theorem
 {#RecognitionTheorems}

The following theorem allows one to recognize cofibrantly generated model categories by checking fewer conditions.

+-- {: .num_theorem}
###### Theorem 

Let $C$ be a [[category]] with all small [[limit]]s and [[colimit]]s and  $W$ a class of maps satisfying [[category with weak equivalences|2-out-of-3]].

If $I$ and $J$ are sets of maps in $C$ such that

1. both $I$ and $J$ permit the [[small object argument]];

1. $cof(J) \subset cof(I) \cap W$;

1. $inj(I) \subset inj(J) \cap W$;

1. one of the following holds

   1. $cof(I) \cap W \subset cof(J)$ 
   
   1. $inj(J) \cap W \subset inj(I)$
   
then there is the stucture of a cofibrantly generated model category
on $C$ with 

* weak equivalences $W_C := W$

* generating cofibrations $I$ (i.e. $cof_C := llp(rlp(I))$) 

* generating acyclic cofibrations $J$.

=--

This is originally due to [[Daniel Kan]], reproduced for instance as ([Hirschhorn 03, theorem 11.3.1](#Hirschhorn03)). 


+-- {: .proof}
###### Proof

We have to show that with weak equivalences $W$
setting $cof_C := cof(I)$ and $fib_C := inj(J)$ defines a model category
structure.

The existence of [[limit]]s, [[colimit]]s and the [[category with weak equivalences|2-out-of-3 property]] holds by assumption. Closure under retracts of the weak equivalences will hold automatically if we check the rest of the axioms without using it, by an argument of A. Joyal.
Closure under retracts of $fib$ and $cof$ follows by the general statement that
classes of morphisms defined by a left or right lifting property are closed under retracts (e.g. [Hirschhorn 03, 7.2.8, ](#Hirschhorn03)).

The factorization property follows by applying the [[small object argument]]
to the set $I$, showing that every morphism may be factored as 
$$
  \stackrel{\in cof(I)}{\to} \stackrel{\in inj(I) \subset fib_C}{\to}
$$
and assumption 3 says that $inj(I) \subset W$. Similarly applying
the small object argument to $J$ gives factorizations
$$
  \stackrel{\in cof(J)}{\to} \stackrel{\in inj(J) = fib_C}{\to}
$$
and assumption 2 guarantees that $cof(J) \subset W$.

It remains to verify the lifting axiom. This verification depends on which
of the two parts of item 4 is satisfied. Assume the first one is, the argument
for the second one is analogous.

Then using the assumption $cof(I) \cap W \subset cof(J)$ and remembering that
we have set $inj(J) = fib_C$ we immediately have the lifting of trivial cofibrations
on the left against fibrations on the right.

To get the lifting of cofibrations on the left with acyclic fibrations on the right,
we show finally that $inj(J) \cap W \subset inj(I)$. To see this, apply the
factorization established before to an acyclic fibration $f : X \to Y$ to get

$$
  \array{
    X &\stackrel{=}{\to}& X
    \\
    \downarrow^{\mathrlap{\in cof(I) \cap W}} && \downarrow^{\mathrlap{f \in inj(J) \cap W}}
    \\
    Z &\stackrel{inj(I)}{\to}& Y
  }
  \,.
$$

With assumption 4 a this is

$$
  \array{
    X &\stackrel{=}{\to}& X
    \\
    \downarrow^{\mathrlap{\in cof(J) }} && 
    \downarrow^{\mathrlap{f \in inj(J) \cap W}}
    \\
    Z &\stackrel{inj(I)}{\to}& Y
  }
$$

so that we have a lift

$$
  \array{
    X &\stackrel{=}{\to}& X
    \\
    {}^{\mathllap{\in cof(J) }}
    \downarrow &{}^\sigma\nearrow& 
    \downarrow^{\mathrlap{f \in inj(J) \cap W}}
    \\
    Z &\stackrel{inj(I)}{\to}& Y
  }
$$

which establishes a retract

$$
  \array{
    X &\to& Z &\stackrel{\sigma}{\to}& X
    \\
    \downarrow^f && \downarrow^{\mathrlap{\in inj(I)}} && \downarrow^f
    \\
    Y &\stackrel{=}{\to}& Y 
    & \stackrel{=}{\to} & Y
  }
$$

that exhibits $f$ as an element of $inj(I)$ as this is closed under retracts.

=--

### Transfer along adjunctions

+-- {: .num_theorem #TransferOfCofibrantlyGeneratedModelStructure}
###### Theorem 

Let $\mathcal{C}$ be a cofibrantly generated model category, def. \ref{CofibrantlyGeneratedModelCategory}, with generating (acyclic) cofibrations $I$ (and $J$). Let $\mathcal{D}$ be any [[category]] with all small [[limits]] and [[colimits]] and consider a pair of  [[adjoint functors]]

$$
  (F \dashv U)
   \;\colon\;
  \array{
    \mathcal{D}
      \stackrel{\overset{F}{\longleftarrow}}{\underset{U}{\longrightarrow}}
    \mathcal{C}
  }
  \,.
$$

Write $F I \coloneqq \{F(i) | i \in I\}$ and $F J \coloneqq \{F(j) | j \in J\}$. If

1. both $F I$ and $F J$ admit the [[small object argument]];

1. $U$ takes $F J$-[[relative cell complexes]] to weak equivalences

then $F I$, $F J$ induce a cofibrantly generated model structure, def. \ref{CofibrantlyGeneratedModelCategory}, on $\mathcal{D}$. Its weak equivalences are the morphisms that are taken to weak equivalences by $U$. Moreover, the above [[adjunction]] is a [[Quillen adjunction]] for these model structures.

=--

This is due to [[Daniel Kan]], reproduced in ([Hirschhorn 03, theorem 11.3.2](#Hirschhorn03)). See also at _[[transferred model structure]]_.
 


### Presentation and generation
 {#PresentationAndGeneration}

+-- {: .num_prop }
###### Proposition

Let $C$ be a cofibrantly generated model category which is also [[proper model category|left proper]]. Then there exists a [[small set]] $S \subset Obj(C)$ of cofibrant objects which detect weak equivalences:

a morphism $f : A \to B$ in $C$ is a weak equivalence, precisely if for all $s \in S$ the induced morphism of [[derived hom-spaces]] 

$$
  \mathbb{R}Hom(s,f) : \mathbb{R}Hom(s,A) \to \mathbb{R}Hom(s,B)
$$

is a weak equivalence.

=--

This appears as ([Dugger, prop. A.5](#Dugger)).

## Examples ##

### On simplicial sets

The [classical model category structure on simplicial sets](https://ncatlab.org/nlab/show/model+structure+on+simplicial+sets) is cofibrantly generated:

+-- {: .num_prop}
###### Proposition

$sSet_{Quillen}$ is a cofibrantly generated model category with

* generating cofibrations the [[boundary]] inclusions $\partial \Delta[n] \to \Delta[n]$;

* generating acyclic cofibrations the [[horn]] inclusions $\Lambda^i[n] \to \Delta[n]$.

=--


### On topological spaces

The category of (based, compactly generated) topological spaces has a cofibrantly generated model structure (the [[classical model structure on pointed topological spaces]]) in which the set of cells is 

$$
   I = \{S^{n-1}_+ \rightarrow D^n_+\}_{n\geq 0}
$$ 

and the set of acyclic cells is 

$$
  J = \{D^n_+ \rightarrow (D^n \times I)_+\}_{n\geq 0}
  \,.
$$ 

(Here $+$ means disjoint basepoint, not northern hemisphere.) 

The category of unbased spaces has a similar cofibrantly generated model structure. (The [[classical model structure on topological spaces]].)

### On sequential spectra

The category of [[sequential prespectra]] has two cofibrantly generated model structures (the [[Bousfield-Friedlander model structures]]). 

Let $F_d A$ denote a prespectrum whose $n$th space is $\Sigma^{n-d} A$ when $n \geq d$, and $*$ otherwise. Then the _level model structure_ is generated by cells 

$$
  I = \{F_d S^{n-1}_+ \rightarrow F_d D^n_+\}_{d,n\geq 0}
$$ 

([[free spectra]] formed on the standard cells of the [[classical model structure on pointed topological spaces]])

and the set of acyclic cells is 

$$
  J = \{F_d D^n_+ \rightarrow F_d (D^n \times I)_+\}_{d,n\geq 0}
$$ 

The _stable model structure_ has the same cells, but more acyclic cells, which in turn guarantees that the fibrant spectra are the $\Omega$-spectra.

### On structured spectra

The categories of [[symmetric spectra]] and [[orthogonal spectra]] have similar cofibrantly generated level and stable model structures ([[model structure on symmetric spectra]], [[model structure on orthogonal spectra]]).

(see Mandell, May, Schwede, Shipley: _[[Model categories of diagram spectra]]_.)

### On diagrams

The category of diagrams indexed by a fixed small category $D$, taking values in another cofibrantly generated model category $C$.

(The [[model structure on functors]].)



## Related concepts ##

* A cofibrantly generated model category that is also a [[locally presentable category]] is called a *[[combinatorial model category]]*.

* A cofibrantly generated model category for which the [[domains]] of the morphisms in $I$ and $J$ are [[compact objects]] or [[small objects]] is a *[[cellular model category]]*.

* [[cellular category]]

* [[transferred model structure]]


## References ##

The original reference is:

* [[William G. Dwyer]], [[Philip S. Hirschhorn]], [[Daniel M. Kan]], Chapter II of: *[[Model Categories and More General Abstract Homotopy Theory]]*, &lbrack;[pdf](https://web.math.rochester.edu/people/faculty/doug/otherpapers/dhk.pdf), [[DwyerHirschhornKan-ModelCategories.pdf:file]]&rbrack;

In particular, the Kan recognition theorem is in §II.8 and the [[Kan transfer theorem]] is in §II.9.
This manuscript draft later transformed in 
[[Homotopy Limit Functors on Model Categories and Homotopical Categories]], losing the content on cofibrantly generated model categories in the process.

Textbook accounts:

* {#Hovey99} [[Mark Hovey]], Section 2.1 in: *[[Model Categories]]*, Mathematical Surveys and Monographs, **63** AMS (1999) &lbrack;[ISBN:978-0-8218-4361-1](https://bookstore.ams.org/surv-63-s), [doi:10.1090/surv/063](https://doi.org/http://dx.doi.org/10.1090/surv/063), [Google books](http://books.google.co.uk/books?id=Kfs4uuiTXN0C&printsec=frontcover)&rbrack;


* {#Hirschhorn03} [[Philip Hirschhorn]], Sec. 11 in: _Model Categories and Their Localizations_, AMS Math. Survey and Monographs Vol 99 (2002) ([ISBN:978-0-8218-4917-0](https://bookstore.ams.org/surv-99-s/), [pdf toc](http://www.gbv.de/dms/goettingen/360115845.pdf), [pdf](http://www.maths.ed.ac.uk/~aar/papers/hirschhornloc.pdf))

Further review:

* {#GoerssSchemmerhorn06} [[Paul Goerss]], [[Kirsten Schemmerhorn]], Section 3.1 of: _Model categories and simplicial methods_, Notes from lectures given at the University of Chicago in August 2004, published as: _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics **436** AMS (2007) &lbrack;[arXiv:math.AT/0609537](http://arxiv.org/abs/math.AT/0609537), [doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436)&rbrack;
 



For the general case a useful reference is for instance the first section of 

* [[Tibor Beke]], _Sheafifiable homotopy model categories_,  Math. Proc. Cambridge Philos. Soc.  __129__  (2000),  no. 3, 447--475.([math.CT/0102087](http://arxiv.org/abs/math/0102087)), _Sheafifiable homotopy model categories. II_, J. Pure Appl. Algebra  __164__  (2001),  no. 3, 307--324.

For the case of a [[presentable category]]:

* [[Jacob Lurie]], section A.1.2 in: *[[Higher Topos Theory]]*

See also: 

* {#Dugger} [[Dan Dugger]], Appendix of: _Replacing model categories with simplicial ones_ ([pdf](http://hopf.math.purdue.edu/Dugger/smod.pdf))
 

[[!redirects cofibrantly generated model categories]]

[[!redirects cofibrantly generated model structure]]
[[!redirects cofibrantly generated model structures]]

[[!redirects generating cofibration]]
[[!redirects generating cofibrations]]

[[!redirects generating acyclic cofibration]]
[[!redirects generating acyclic cofibrations]]

[[!redirects cofibrantly generated]]

[[!redirects Kan recognition theorem]]

