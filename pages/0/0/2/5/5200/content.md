
# The logic $S4_{(m)}$
* table of contents
{:toc}

## The epistemic logics $S4$ and $S4_{(m)}$## 
(Note that $S4 = S4_{(1)}$.)

Although better than $K$ (resp. $K(m)$), the [[the logic T(m)|epistemic logics ]], $T$ and $T_{(m)}$, still do not reflect that much of our intuition of 'knowledge'. One of the usual richer logics considered is the logic $S4$ (or in its 'multi-agent' form $S4_{(m)}$).  These involve the axiom scheme know as $(4)$, that is also present in many [[temporal logics]].

## The axioms $(4)_i$## 
This is found in two equivalent forms (for agent $i$):

* $M_i M_i p\to M_i p$

and 

* $K_i p\to K_i K_i p$.

In this second form, it clearly corresponds to ''Agent $i$ knows that (s)he knows what (s)he knows''! That 'positive introspection' seems reasonable.  The dual version interprets as ''If the agent considers that it is possible that it is possible that $p$ holds, then the agent considers it possible that $p$ holds'' and again that is 'common sense'.

## The logics $S4$ and $S4_{(m)}$
* $S4$ - this logic is obtained from $T$ by adding the axiom $(4)$.

* $S4_{(m)}$ starting from $T_{(m)}$, add, for each $i = 1,\ldots, m$ the axiom $(4)_i$.

##Reflexive transitive Kripke frames##
With $T_{(m)}$, the models corresponded to frames where each relation $R_i$ was reflexive.  Here we consider the class $\mathcal{S}4(m)$ of models with frames, where each $R_i$ is both reflexive _and_ transitive.

+--{: .un_defn}
######Theorem (Soundness of $S4_{(m)}$)
$S4_{(m)}\vdash \phi \Rightarrow \mathcal{S}4(m)\models \phi.$
=--
+--{: .un_proof}
######Proof######
(We show this for $m = 1$.)

Suppose that $\mathfrak{M}= ((W,R),V)$ where $R$ is a reflexive transitive relation on $W$.  We have to check that $\mathfrak{M}\models (4)$.

Suppose $\mathfrak{M},w\models K p$, then, for every  $t$ with $R w t$, we have $\mathfrak{M},t\models p$.  Now suppose we seek to check that $\mathfrak{M},w\models K K p$ so we have $t$ with $R w t$ and want $\mathfrak{M},t\models K p$, so we look at all $u$ with $R t u$ and have to see if $\mathfrak{M},u\models p$, but as $R w t$ and $R t u$ hold then $R w u$ holds, since $R$ is transitive, and we then _know_ that $\mathfrak{M},u\models p$.
=--