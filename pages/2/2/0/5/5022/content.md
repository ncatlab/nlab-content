
# Contents
* table of contents
{:toc}

## Frames in Modal Logics ## 
(The term **frame** is used in a different sense in [[modal logic]] than in [[geometric logic]] where it stands for an abstraction of the algebraic structure corresponding to the [[lattice]] of [[open sets]] of a [[topological space]]; see [[frame]].)

We will start with the simplest case, namely a frame for the basic [modal language](/nlab/show/modal+logic#modal+language), $\mathcal{L}_\omega(1)$, (so with _one_ _binary_ modal operator, denoted $\Diamond$).

+--{: .un_defn}
######Definition ######
A _frame_ for $\mathcal{L}_\omega(1)$ is a pair $\mathfrak{F} = (W,R)$ with $W$ a non-empty set and $R$ a binary relation on $W$.
=--
(This is also called a _Kripke frame_.)

The terminology often used refers to $W$ as the set of possible worlds.  Its elements are sometimes called _worlds_, sometimes _states_, sometimes _points_, depending on the context and the whim of the writer.

## Models in Modal Logics ## 
To give the standard (geometric) semantics of modal logics one needs the models.  Again we look at the basic model language.

+--{: .un_defn}
######Definition ######
A _model_ for $\mathcal{L}_\omega(1)$ is a pair $\mathfrak{M} = (\mathfrak{F},V)$, where $\mathfrak{F}$ is a frame (for $\mathcal{L}_\omega(1)$) and $V: Prop \to \mathcal{P}(W)$, is a function, called a _valuation_, assigning to each atomic proposition $p$ a subset of the set, $W$, of worlds.
=--

###Gloss###
1. Informally we think of $V(p)$ as the set of 'worlds' in our model where $p$ is true.

1. Frames are 'mathematical pictures' of ontologies that are found interesting (for the context), whilst a model 'puts some flesh on' the frame by adding contingent information.

1. Frames give a **combinatorial** or **geometric** basis for the semantics of these logics.  There is also an algebraic semantics that will be examined in another entry. (To be done)

##Satisfaction##
+--{: .un_defn}
######Definition ######
Suppose that $w$ is a state in a model $\mathfrak{M} = (W,R,V)$.  We inductively define the notion of a formula $\phi$ being satisfied in the model at state $w$, as follows:

* for $p\in Prop$, $\mathfrak{M},w \models p$ if and only if $w\in V(p)$;

* $\mathfrak{M},w \models \bot$ never;
 
* $\mathfrak{M},w \models \neg \phi$ if and only if it is not true that $\mathfrak{M},w \models \phi$;

* $\mathfrak{M},w \models \phi \vee \psi$ if and only if $\mathfrak{M},w \models\phi$ or $\mathfrak{M},w \models\psi$;

* $\mathfrak{M},w \models \Diamond \phi$ if and only if, for some $v \in W$ such that $ R w v$, $\mathfrak{M},v \models \phi$.
=--

###Notes###
1. $\mathfrak{M},w \models \square \phi$ if and only if $\forall v\in W$ $ R w n$ implies $\mathfrak{M},v \models  \phi$. (The proof is fairly routine manipulation of negations.)


1. We say a set $\Sigma$ of formulae is true at state $w\in W$ of a model $\mathfrak{M}$, written $\mathfrak{M},w \models \Sigma$, if all members of $\Sigma$ are satisfied as $w$.

1. It is convenient to extend the valuation $V$ to arbitrary formulae by setting $V(\phi) := \{w \mid \mathfrak{M},w \models \phi\}$.
## References## 

Generally this entry is based on

* P. Blackburn, M. de Rijke and Y. Vedema, _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

(any mistakes or errors of interpretation are due to ....!)







[[!redirects Kripke frame]]
[[!redirects Kripke frames]]

[[!redirects frame (modal logic)]]
[[!redirects frames (modal logic)]]
[[!redirects frame (Kripke)]]
[[!redirects frames (Kripke)]]
