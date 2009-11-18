<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea  ##

A [[model category]] $C$ is _cofibrantly generated_ if there is a [[set]]
(meaning: small set, not a proper class) of cofibrations and one of
trivial cofibrations, such that all other (trivial) cofibrations are
_generated_ from these.

Ths property of being cofibrantly generated is particularly tractable
and useful in the case that the model category is a 
[[presentable category]]. In this case one speaks of a
[[combinatorial model category]].

## Definition ##

We first give the simple definition that applies in the case that the model category in question is [[presentable category|presentable]].

For $S \subset Mor(C)$ any collection of morphisms, write

* $rlp(S)$ for the collection of morphisms with the _right_ 
  [[weak factorization system|lifting property]] 
  with respect to $S$;
  
* $llp(S)$ for the collection of morphisms with the _left_ 
  [[weak factorization system|lifting property]] with respect to $S$;
  
+-- {: .un_defn}
###### Definition

A [[model category]] $C$ that is a [[presentable category]] is  **cofibrantly generated** if there is a small [[set]] $cof_0 \subset cof \subset Mor(C)$ of cofibrations such that the collection $cof$ of all cofibrations is

$$
  cof = llp(rlp(cof_0))
  \,.
$$
=--

Notice that necessarily

$$
  cof_0 \subset llp(rlp(cof_0))
  \,.
$$

There is another way to characterize $llp(rlp(cof_0))$.

+-- {: .un_prop}
###### Proposition

If $C$ is [[presentable category|presentable]], and $S \subset Mor(C)$ is any set of morphisms, then $llp(rlp(S))$ is  the smallest collection containing $S$ that is closed under  [[pushout]], [[retract]]s and [[transfinite composition]].
=--

+-- {: .proof}
###### Proof

Use the [[small object argument]].
=--


## References ##

See [[Higher Topos Theory|HTT section A.1.2]].


