
# Algebras for modal logics
* table of contents
{:toc}

## Idea

Classical [[propositional calculus]] has an algebraic model, namely a Boolean algebra. With a bit of imagination, one can give it a combinatorial model on the line of Kripke semantics. As this ordinary propositional logic has no modal operators, then the corresponding [[frame (modal logic)|frames]] have no relations, so are just sets.  If $W$ is such a set, (of worlds), a valuation $V: Prop \to 2^W$ just assigns to each $p \in Prop$ and $w\in W$ a truth value, $\top$ or $\bot$, (true or false).  We know however that there is a Boolean algebra structure around in that power set $2^W$ and the semantics extends the assignment given by $V$ to a map of algebras, from the term algebra based on the basic propositional language to the Boolean algebra of subsets of $W$. That is just to say that it builds up that extension of $V$ bit-by-bit on the terms. This gives an algebraic interpretation or representation of the terms of the logic in terms of the algebra of subsets of $W$, in other words an algebraic semantics.

Modal logics also have an algebraic semantics based on a Boolean algebra, but with additional operators that model the modal operators. This is as well as the [[geometric models for modal logics|geometric semantics]] using [[frames (modal logic)|frames]].


## Boolean algebras with operators (BAOs)

### Boolean algebras

We will, here, consider a [[Boolean algebra]], $\mathbb{B }$, as an algebra, and in the notation,

$$\mathbb{B} = (B, +, \cdot, \overline{},0,1)$$

so, for example, for a set $S$, the [[power set]] Boolean algebra will be

$$\mathbb{P}(S) = (\mathcal{P}(S), \cup, \cap,-,\emptyset, S),$$

where $-A$ is shorthand for the complement, $S- A$, of $A$.


### Operators

The __operators__ that we need to add into the Boolean algebras do not always preserve all the structure:

+-- {: .un_defn}
###### Definition

A function, $m : B\to B$ is called an __operator__ on the Boolean algebra, $\mathbb{B}$, if it is _additive_

$$m(x+y) = m x + m y.$$

The operator, $m$, is called __normal__ if $m0=0$.
=--

Any operator, $m$, in this sense has a dual $l : B\to B$ given by

$$l(x) = (m(x^-)^-.$$

As $m$ is additive, $l$ is __multiplicative__

$$l(x\cdot y) = l(x)\cdot l(y),$$

and has $l(1) = 1$ if $m$ is normal.


#### Remark

One of the myriad notations used for the generic modal operators $\lozenge$ and $\Box$, are $M$ and $L$, whence $M$ is 'possibility, and $L$ is 'necessity", and these gave the names to the operators above.

+-- {: .un_defn}
###### Definition

A **Boolean algebra with operators,** or BAO, of type $n$ consists of a Boolean algebra $\mathbb{B}$, and a set, $m_i$, $i = 1,\ldots, n$ of operators on $B$.
=--

BAOs are sometimes called **modal algebras**, especially in the case that $n = 1$.  The term **polymodal algebra** is then used for the general case. 

There is no need in the definition of BAOs to restrict to finitely many operators nor to have all the operators being unary. The general theory is discussed in the Survey by Goldblatt (see the references).


## Natural examples

+-- {: .num_example}
###### Example
**BAOs from frames.**

Let $\mathfrak{F} = (W ,R)$ be a frame. We define on the power set Boolean algebra, $\mathbb{P}(W)$, the operator $m$ by, if $T\subseteq W$, 
    
$$m(T) = \{w \in W : \exists t\in T, R w t \}$$
  
It perhaps pays to interpret this in the case where $R$ is a [[preorder]] and when it is an equivalence relation. In the first case, this will be the set of states less than or equal to something in $T$, in the second it is the union of all equivalence classes that contain an element of $T$.

+-- {: .un_lemma}
###### Lemma

The function $m$ is a normal operator.  
=--

The proof is a simple manipulation of the definitions.

The dual operator $l$ is given by $l(T) = \{w\in W\mid \forall t\in T \neg R w t\}$. (Again look at this for the preorder and equivalence frame cases.)

It is easy to extend this example to $\mathfrak{F} = (W ,R_1,\ldots, R_n)$ with the result being a BAO of type $n$.
=--

+-- {: .num_example}
###### Example
**The Lindenbaum-Tarski algebra of a modal logic.**

Suppose $\Lambda \subseteq \mathcal{L}_\omega(n)$ is a [[normal modal logic]], then its [[Lindenbaum-Tarski algebra]] has a natural BAO structure, for which see the above page.
=--


##Varieties of modal and polymodal algebras

The following is a list of some of the main equationally defined classes of (poly)modal algebras. (For convenience each has been given a separate entry.)

* [[temporal algebras]];

* [[closure algebras]];

* [[monadic algebras]].


## References

General books on modal logics that include information on algebraic models include:

* [[Patrick Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001.

* [[Marcus Kracht]], _Tools and Techniques in Modal Logic,_ Studies in Logic and the Foundation of Mathematics, 142, Elsevier, 1999.

There is an excellent short survey article (versions of which are available on the web):

*  [[Robert Goldblatt]], _Algebraic Polymodal Logic: A Survey_, the Logic Journal of the 
IGPL, 8, (2000) pages 393&#8211;450, Special Issue on Algebraic Logic, edited by Istvan Nemeti and 
Ildiko Sain. 


[[!redirects modal algebra]]
[[!redirects modal algebras]]
[[!redirects polymodal algebra]]
[[!redirects polymodal algebras]]
[[!redirects algebraic model for modal logics]]
[[!redirects algebraic models for modal logics]]
