# Contents
* table of contents
{:toc}



## Models in Modal Logics ## 
To give the standard (geometric) semantics of modal logics one needs models and these will be discussed here and in the companion [[algebraic models for  modal logics]].

###Models in Monomodal Logics###

Again we look at the basic model language.

+--{: .un_defn}
######Definition ######
A _model_ for $\mathcal{L}_\omega(1)$ is a pair $\mathfrak{M} = (\mathfrak{F},V)$, where $\mathfrak{F}$ is a frame (for $\mathcal{L}_\omega(1)$) and $V: Prop \to \mathcal{P}(W)$, is a function, called a _valuation_, assigning to each atomic proposition $p$ a subset of the set, $W$, of worlds.
=--

###Gloss###
1. Informally we think of $V(p)$ as the set of 'worlds' in our model where $p$ is true.

1. Frames are 'mathematical pictures' of ontologies that are found interesting (for the context), whilst a model 'puts some flesh on' the frame by adding contingent information.

1. Frames give a **combinatorial**, **relational** or **geometric** basis for the semantics of these logics.  There is also an **algebraic** semantics that will be examined in another entry. (To be done)

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

###What is a valuation?###
In the definition of a Kripke model the valuation is all important.  It is what puts meaning onto the frame. It is very useful to push this idea around through a couple of adjunctions and reinterpretations. The process is fairly intuitive, but it pays to do things reasonably formally:

1. Note that the power set $\mathcal{P}(W)$ can also be written as $\mathbf{2}^W$ the set of functions from $W$ to $\mathbf{2}$, where we write $\mathbf{2}$ for the 'set' of classical [[truth values]], $\{\bot \to \top\}$, or $\{true,false\}$, or $\{0,1\}$ or ... .   We wrote 'set' in inverted commas for several reasons:

   * Firstly an important role here is played by the multiple structures that $\mathbf{2}$ has. It is a [[Heyting algebra]]; it has a natural [[poset]] structure; it is the [[subobject classifier]] in the [[topos]] of sets, and so on. In fact it is the source of most of the logic semantic structure within this context.  Its structure induces similar structures on the powerset, $\mathcal{P}(W)$, given by union etc, that made the semantics work above.  (See also the discussion on [[dualizing object|ambimorphic objects]] in the entry on the [[Chu construction]].)

   * Next note that although we said 'set' we could do a lot of this in other settings.  For instance we could work within a more general topos with an object of possible worlds and an object of propositions. We would need the extra [[Heyting algebra]] structure on what would there probably be written as $\Omega$, and our negation interpretation would be more subtle.

   * Finally we could categorify things.  For the moment we will leave this aside, but note the discussion at [[truth value]].


1.  For convenience we will write $P$ for $Prop$, then a valuation is $V: P\to \mathbf{2}^W$, and using  co[[currying]] this corresponds to $V: P\times W\to \mathbf{2}$.  That, of course, corresponds to a subset of $P\times W$.  That subset consists of all pairs, $(p,w)$, for which $w\in V(p)$ so  interprets as the set of pairs in which the proposition $p$ is 'true' in world $w$.

1.  We could re[[currying|curry]] after transposing $P$ and $W$, to get $V$ to correspond to $\tilde{V}: W \to \mathcal{P}(P)$, so that $\tilde{V}(w)$ is the set of propositions true about the world $w$.

1.  Another useful direction is to see this as giving a binary [[Chu construction|Chu space]]. (To be investigated later.) 


## References## 

Generally this entry is based on

* P. [[Blackburn]], M. de Rijke and Y. [[Venema]], _Modal Logic_, Cambridge Tracts in Theoretical Computer Science, vol. 53, 2001, 

(any mistakes or errors of interpretation are due to ....!)