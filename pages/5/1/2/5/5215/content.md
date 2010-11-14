
# The logic $S5_{(m)}$
* table of contents
{:toc}

## The epistemic logics $S5$ and $S5_{(m)}$## 
(Note that $S5 = S5_{(1)}$.)

Although better than $K$ (resp. $K(m)$), and $T$ (resp. $T(m)$), $S4$ (resp. $S4(m)$) is still not considered adequate for knowledge representation.  Because of this further axioms have been put forward, too many to be mentioned here.  We will limit ourselves, (at this stage in the development of these entries, at least) to introducing one more axiom, that is a bit more contentious, (but is nice from the nPOV.) 


## The axioms $B_i$## 

The axiom denoted $B_i$, (and again refer to Kracht for some indication of possible reasons) is 

* $p \to K_i M_i p$.

The interpretation is the 'if $p$ is true then agent $i$ knows that it is possible that $p$ is true.'

Another axiom that is relevant here is:

## The axioms $(5)_i$## 

* $\neg K_i p \to K_i \neg K_i p$

Axiom (5) interprets as saying 'If agent $i$ does not know that $p$ holds, then (s)he knows that (s)he does not know'. This is termed 'negative introspection'.

## The logics $S5$ and $S5_{(m)}$##
* $S5$ - this logic is obtained from $S4$ by adding the axiom $B$.

* $S5_{(m)}$ starting from $S4_{(m)}$, add, for each $i = 1,\ldots, m$ the axiom $B_i$.


In either case the same result can be obtained by adding in $5$ or $(5)_i$ in place of the corresponding $B$.

####Critique####
This is highly doubtful as a property of knowledge when applied to human beings. If an agent is ignorant of the truth of an assertion, it is very often unlikely that (s)he knows this ignorance.

+--{: .query}
[[Tim Porter]] It would be good to have some discussion on this axiom.  (Donald Rumsfeld's known unknowns has been worked to death, (although sometimes quite well done as [here](http://wn.com/modal_logic)), so please... something worth saying :-)).  This might stray over to a new entry as I would hope to see what there is to say especially looking to models of 'why' an agent 'knows' something.  My query is whether that aspect has been explored and if so where. My feeling is that in S5 (and elsewhere) the reasons may give a groupoid-like structure (see below about the Kripke semantics) for the geometric semantics.
=--
##Equivalence frames##
With $T_{(m)}$, the models corresponded to frames where each relation $R_i$ was reflexive. With $S4_{(m)}$, the frames needed to be transitive as well.  Here we consider the class $\mathcal{S}5(m)$ of models with frames, where each $R_i$ is an equivalence relation.  These are sometimes called _equivalence frames_.

+--{: .un_defn}
######Theorem (Soundness of $S5_{(m)}$)
$S5_{(m)}\vdash \phi \Rightarrow \mathcal{S}5(m)\models \phi.$
=--
+--{: .un_proof}
######Proof######
(We show this for $m = 1$.)
We have already shown (here in [[the logic S4(m)]]) that the older axioms $T$ and $(4)$ hold so it remains to show if we have a frame, $\mathfrak{M}= ((W,R),V)$, where $R$ is an equivalence relation on $W$ then $\mathfrak{M}\models B$.


=--