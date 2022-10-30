

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

A bisimplicial set is a bisimplicial object in [[Set]].


## Properties

### Diagonal

+-- {: .un_def }
###### Definition
**(diagonal)**

For $X_{\bulet,\bullet}$ a bisimplicial set, its **diagonal** is the simplicial set that this the precomposition with $(Id, Id) : \Delta^{op} \to \Delta^{op} \times \Delta^{op}$, i.e. the simplicial set with components.

$$
  d(X)_n = X_{n,n}
  \,.
$$

=--


+-- {: .un_def }
###### Definition
**(realization)**

The **realization** $|X|$ of a bisimplicial set $X_{\bullet,\bullet}$ is the [[simplicial set]] that is given by the [[coend]]

$$
  |X| =  \int^{[n] \in \Delta} X_{n,\bullet} \times \Delta[n]_\bullet
$$

in [[sSet]].

=--

+-- {: .un_prop }
###### Proposition
**(diagonal is realization)**

For $X$ a bisimplicial set, its diagonal $d(X)$ is (isomorphic to) its realization $|X|$:

$$
  |X| \simeq d(X)
  \,.
$$


=--

+-- {: .proof}
###### Proof

This is exercise 1.6 in  in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 


=--

+-- {: .un_prop }
###### Proposition
**(diagonal is homotopy colimit)**

The diagonal of a bisimplicial set $X_{\bullet,\bullet}$ is also (up to weak equivalence) the [[homotopy colimit]] of $X$ regarded as a simpliciall diagram in the [[model structure on simplicial sets]]

$$  
  diag X \simeq hocolim (X : \Delta^{op} \to sSet_{Quillen})
  \,.
$$

=--

This appears for instance as theorem 3.6 in ([Isaacson](#Isaacson)).

+-- {: .proof}
###### Proof

This follows with the above equivalence to the [[coend]] $diag X \simeq \int^{[k] \in \Delta} \Delta[k] \cdot X_k$ and general expression of  [[homotopy colimit]]s by coends (as discussed there) in terms of the [[Quillen bifunctor]]

$$
  \int^\Delta (-) \cdot (-)
    :
   [\Delta, sSet_{Quillen}]_{Reedy} \times
   [\Delta, sSet_{Quillen}]_{Reedy}  
  \to 
    sSet_{Quillen}
$$

in [[Reedy model structure]]s (as discussed there) by using that $\Delta[-] : \Delta \to sSet_{Quillen}$ is a Reedy cofibrant resultion of the point in $[\Delta, sSet_{Quillen}]$ and that every object in $[\Delta^{op}, sSet_{Quillen}]_{Reedy}$ is cofibrant.
=--

+-- {: .un_prop }
###### Proposition
**(degreewise weak equivalences)**

Let $X,Y : \Delta^{op} \times \Delta^{op} \to Set$ be bisimplicial sets.
A morphism $f : X \to Y$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : X(n,\bullet) \to Y(n,\bullet)$ induces a weak equivalence 
$d(f) : d(X) \to d(Y)$ of the associated diagonal simplicial sets
(with respect to the standard [[model structure on simplicial sets]]).

=--


+-- {: .proof}
###### Proof

This is prop 1.9 in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of 

* Goerss-Jardine, _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 

=--

### Total d&#233;calage and total simplicial sets

There is a [[functor]] called _[[ordinal sum]]_

$$
  + : \Delta^\op \times \Delta^{op} \to \Delta^{op}
  \,.
$$

This induces an [[adjoint triple]]

$$
  ssSet
   \stackrel{\overline{+_!}{\to}}{\stackrel{\overline{+^*}{\leftarrow}}{\underline{+_*}}}
  sSet
  \,.
$$

Here 

* $T := +_*$ is called the **total simplicial set** functor or [[codiagonal]];

* $Dec := +^*$ is called the [[total decalage]] functor;

* 

$T$ preserves degreewise [[weak equivalences]] of [[simplicial sets]].

For $X$ any bisimplicial set 

* the canonical morphism
 
  $$
    diag X \to T X
  $$

  from the [[diagonal]] to the total simplcial set is a weak equivalence in the [[model structure on simplicial sets]];

* the [[unit of an adjunction|adjunction unit]]

  $$
    X \to T Dec X
  $$

  is a weak equivalence.

The standard [[delooping]] functor for [[simplicial group]]s

$$
  \bar W : sGrp \to sSet_*
$$

is the composite

$$
  \bar W 
   : 
  sGrpd
   \stackrel{B}{\to}
  sGrpd
   \stackrel{N}{\to}
  ssSet
   \stackrel{T}{\to}
  sSet
  \,.
$$

The [[transferred model structure]] on $ssSet$ along $T$ exists. And for it $(Dec \dashv T) : ssSet \leftrightarrow sSet$ is a [[Quillen equivalence]].

Moreover, every fibration in the [[Reedy model structure]] on $sSet \simeq sSet^\Delta$ is also a $T$-fibration.


## Bisimplicial abelian groups 


+-- {: .un_prop }
###### Proposition

Let $A,B : \Delta^{op} \times \Delta^{op} \to Ab$ be bisimplicial abelian groups.
A morphism $f : A \to B$ which is degreewise in one argument a weak equivalence
$f_{n,\bullet} : A(n,\bullet) \to B(n,\bullet)$ induces a weak equivalence 
$d(f) : d(A) \to d(B)$ of the associated diagonal complexes.

=--


+-- {: .proof}
###### Proof

This is Lemma 2.7 in [chapter 4](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-4.dvi) of ([GoerssJardine](#GoerssJardine))


=--

## References

* [[Paul Goerss]] [[Rick Jardine]], _Simplicial Homotopy Theory_ ([dvi](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html)) 
{#GoerssJardine}

* [[Rick Jardine]], Lecture 008 (2010) ([pdf](http://www.math.uwo.ca/~jardine/papers/HomTh/lecture008.pdf))

* [[Samuel Issacson]], _Excercises in homotopy colimits_ ([pdf](http://www-math.mit.edu/~mbehrens/TAGS/Isaacson_exer.pdf))
{#Isaacson}

* A. Cegarra, Josu&#233; Remedios, _The relationship between the diagonal and the bar constructions on a bisimplicial set_ ([pdf](http://www.ugr.es/~acegarra/Paperspdfs/TRBDWC.pdf))

[[!redirects bisimplicial sets]]

[[!redirects total decalage]]
[[!redirects total décalage]]