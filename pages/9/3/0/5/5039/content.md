
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Models in Modal Logics

The [[semantics]] of [[modal logics]] based on [[Kripke frames]] ("geometric" in contrast to [[algebraic models for modal logics]]), often called **Kripke semantics** &lbrack;[Kripke (1959)](#Kripke59), [(1963)](#Kripke63)&rbrack;. 

In the following we say *frame* for *[[Kripke frame]]*. 


### Models in Monomodal Logics

Again we look at the basic model language.

+-- {: .un_defn}
###### Definition

A _model_ for $\mathcal{L}_\omega(1)$ is a pair $\mathfrak{M} = (\mathfrak{F},V)$, where $\mathfrak{F}$ is a [[frame (modal logic)
  |frame]] (for $\mathcal{L}_\omega(1)$), that is, a non-empty set, $W$, equipped with a binary relation, $R$, and $V: Prop \to \mathcal{P}(W)$, is a function, called a _valuation_, assigning to each atomic proposition $p$ a subset of the set, $W$, of worlds.
=--


### Gloss

1. Informally we think of $V(p)$ as the set of 'worlds' in our model where $p$ is true.

1. The binary relation of the frame allows for the modelling of the truth of a modal proposition, $\Diamond \phi$ or $\Box \phi$, at some world in terms of the truth of $\phi$ at related worlds.

## Satisfaction

+-- {: .un_defn}
###### Definition

Suppose that $w$ is a state in a model $\mathfrak{M} = (W,R,V)$.  We inductively define the notion of a formula $\phi$ being satisfied in the model at state $w$, as follows:

* for $p\in Prop$, $\mathfrak{M},w \models p$ if and only if $w\in V(p)$;

* $\mathfrak{M},w \models \bot$ never;
 
* $\mathfrak{M},w \models \neg \phi$ if and only if it is not true that $\mathfrak{M},w \models \phi$;

* $\mathfrak{M},w \models \phi \vee \psi$ if and only if $\mathfrak{M},w \models\phi$ or $\mathfrak{M},w \models\psi$;

* $\mathfrak{M},w \models \Diamond \phi$ if and only if, for some $v \in W$ such that $ R w v$, $\mathfrak{M},v \models \phi$.
=--


### Notes

1. The terminology used in talking about 'satisfaction' tends to interpret $\mathfrak{M},v \models \phi$ as saying the formula $\phi$ is **true** in $\mathfrak{M}$ at state $v$. 
 

2. $\mathfrak{M},w \models \square \phi$ if and only if $\forall v\in W$ $ R w n$ implies $\mathfrak{M},v \models  \phi$. (The proof is fairly routine manipulation of negations.)


3. We say a set $\Sigma$ of formulae is true at state $w\in W$ of a model $\mathfrak{M}$, written $\mathfrak{M},w \models \Sigma$, if all members of $\Sigma$ are satisfied as $w$.


4. It is convenient to extend the valuation $V$ to arbitrary formulae by setting $V(\phi) := \{w \mid \mathfrak{M},w \models \phi\}$. We then get useful interpretations such as: if for all worlds $v$, $\mathfrak{M},v \models  (\phi\to \psi)$ and _modus ponens_ holds, (i.e. we have a logic as such in which we are working,  then $V(\phi)\subseteq V(\psi)$. (This comment is deliberately slightly vague, but indicates a common type of argument that will be behind many results, where more precision is available, so think of it as a template for a result rather than a result as such.)


### What is a valuation?

In the definition of a Kripke model the valuation is all important.  It is what puts meaning onto the frame. It is very useful to push this idea around through a couple of adjunctions and reinterpretations. The process is fairly intuitive, but it pays to do things reasonably formally:

1. Note that the power set $\mathcal{P}(W)$ can also be written as $\mathbf{2}^W$ the set of functions from $W$ to $\mathbf{2}$, where we write $\mathbf{2}$ for the 'set' of classical [[truth values]], $\{\bot \to \top\}$, or $\{true,false\}$, or $\{0,1\}$ or ... .   We wrote 'set' in inverted commas for several reasons:

   * Firstly an important role here is played by the multiple structures that $\mathbf{2}$ has. It is a [[Heyting algebra]]; it has a natural [[poset]] structure; it is the [[subobject classifier]] in the [[topos]] of sets, and so on. In fact it is the source of most of the logic semantic structure within this context.  Its structure induces similar structures on the powerset, $\mathcal{P}(W)$, given by union etc, that made the semantics work above.  (See also the discussion on [[dualizing object|ambimorphic objects]] in the entry on the [[Chu construction]].)

   * Next note that although we said 'set' we could do a lot of this in other settings.  For instance we could work within a more general topos with an object of possible worlds and an object of propositions. We would need the extra [[Heyting algebra]] structure on what would there probably be written as $\Omega$, and our negation interpretation would be more subtle.

   * Finally we could categorify things.  For the moment we will leave this aside, but note the discussion at [[truth value]].


2.  For convenience we will write $P$ for $Prop$, then a valuation is $V: P\to \mathbf{2}^W$, and using  co[[currying]] this corresponds to $V: P\times W\to \mathbf{2}$.  That, of course, corresponds to a subset of $P\times W$.  That subset consists of all pairs, $(p,w)$, for which $w\in V(p)$ so  interprets as the set of pairs in which the proposition $p$ is 'true' in world $w$.


3.  We could re[[currying|curry]] after transposing $P$ and $W$, to get $V$ to correspond to $\tilde{V}: W \to \mathcal{P}(P)$, so that $\tilde{V}(w)$ is the set of propositions true about the world $w$.


4.  Another useful direction is to see this as giving a binary [[Chu construction|Chu space]]. (To be investigated later.) 


## Models in Multimodal Logics

Again we look at the basic model language this time with $n$ unary modal operators.

+-- {: .un_defn}
###### Definition

A _model_ for $\mathcal{L}_\omega(n)$ is a pair $\mathfrak{M} = (\mathfrak{F},V)$, where $\mathfrak{F}$ is a frame (for $\mathcal{L}_\omega(n)$) and $V: Prop \to \mathcal{P}(W)$, is a function, called a _valuation_, assigning to each atomic proposition $p$ a subset of the set, $W$, of worlds.
=--


## Satisfaction in the multimodal case

This is virtually the same as in the monomodal case, except for the last case which involves the $n$ modal operators. (We give it in full repeating the earlier cases for convenience.)

+-- {: .un_defn}
###### Definition

Suppose that $w$ is a state in a model $\mathfrak{M} = (W,R,V)$.  We inductively define the notion of a formula $\phi$ being satisfied in the model at state $w$, as follows:

* for $p\in Prop$, $\mathfrak{M},w \models p$ if and only if $w\in V(p)$;

* $\mathfrak{M},w \models \bot$ never;
 
* $\mathfrak{M},w \models \neg \phi$ if and only if it is not true that $\mathfrak{M},w \models \phi$;

* $\mathfrak{M},w \models \phi \vee \psi$ if and only if $\mathfrak{M},w \models\phi$ or $\mathfrak{M},w \models\psi$;

* for each $i = 1, \ldots, n$, $\mathfrak{M},w \models \Diamond_i \phi$ if and only if, for some $v \in W$ such that $ R_i w v$, $\mathfrak{M},v \models \phi$.
=--

Satisfaction on a class of models  is related to [[validity]] of modal formulae. In this way a class of frames can determine a logic and then the logic determines a class of frames.  The axiomatisation of that class/logic is then an interesting challenge.

## Related concepts

* [[modal type theory]]

* [[Kripke frame]], [[Kripke semantics]]

* [[algebraic model for modal logic]]

## References

The concept originates with:

* {#Kripke59} [[Saul A. Kripke]], *A Completeness Theorem in Modal Logic*, The Journal of Symbolic Logic **24** 1 (1959) 1-14 &lbrack;[doi:10.2307/2964568](https://doi.org/10.2307/2964568), [jstor:2964568](https://www.jstor.org/stable/2964568), [pdf](https://www.filosoficas.unam.mx/~morado/Cursos/17Modal/Kripke1959.pdf)&rbrack;

* {#Kripke63} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic I. Normal Modal Propositional Calculi*, Mathematical Logic Quaterly **9** 5-6 (1963) 67-96 &lbrack;[doi:10.1002/malq.19630090502](https://doi.org/10.1002/malq.19630090502)&rbrack;

* [[Saul A. Kripke]], *Semantical Considerations on Modal Logic*, Acta Philosophical Fennica **16** (1963) 83-94 &lbrack;[pdf](http://saulkripkecenter.org/wp-content/uploads/2019/03/Semantical-Considerations-on-Modal-Logic-PUBLIC.pdf)&rbrack;

* {#Kripke65} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic II. Non-Normal Modal Propositional Calculi*, in *The Theory of Models* (Proceedings of the 1963 International Symposium at Berkeley) Studies in Logic and the Foundations of Mathematics (1965) 206-220 &lbrack;[doi:10.1016/B978-0-7204-2233-7.50026-5](https://doi.org/10.1016/B978-0-7204-2233-7.50026-5)&rbrack;


Textbook accounts:

* {#BlackburnDeRijkeVenema01} [[Patrick Blackburn]], [[Maarten de Rijke]], [[Yde Venema]], *Modal Logic*, Cambridge Tracts in Theoretical Computer Science **53**, Cambridge University Press  (2001) &lbrack;[doi:10.1017/CBO9781107050884](https://doi.org/10.1017/CBO9781107050884)&rbrack;

* [[Valentin Goranko]], [[Martin Otto]], §1 in: *Model Theory of Modal Logic*, in Section 5 in: *Handbook of Modal Logic*, Studies in Logic and Practical Reasoning **3** (2007) 249-329 &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~otto/papers/mlhb.pdf),  [book webpage](https://cgi.csc.liv.ac.uk/~frank/MLHandbook/), [publisher page](https://www.sciencedirect.com/bookseries/studies-in-logic-and-practical-reasoning/vol/3/suppl/C)&rbrack;

Generalization beyond [[Kripke frames]]:

* [[Dov Samet]], §6 in: *S5 knowledge without partitions*, Synthese **172** (2010) 145–155 &lbrack;[doi:10.1007/s11229-009-9469-0](https://doi.org/10.1007/s11229-009-9469-0)&rbrack;



[[!redirects geometric model for modal logic]]
[[!redirects geometric model for modal logics]]
[[!redirects geometric models for modal logic]]
[[!redirects geometric models for modal logics]]

[[!redirects Kripke semantics]]

[[!redirects geometric model of modal logic]]
[[!redirects geometric models of modal logic]]



