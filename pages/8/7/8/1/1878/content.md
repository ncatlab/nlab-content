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

We need the following general terminology

+-- {: .un_defn}
###### Definition

Let $C$ be a category with all [[colimit]]s and let $I \subset Mor(C)$ a class of morphisms. We write

* $cell(I)$ for the class of morphisms obtained by [[transfinite composition]] of [[pushout]]s of elements in $I$;

* $cof(I)$ for the class of [[retract]]s (in the [[arrow category]] $Arr(C)$) of elements in $cell(I)$

* $inj(I) := rlp(I)$ for the class of morphisms with the right [[lifting property]] with respect to $I$.

=--

A [[model category]] with all [[colimit]]s is **cofibrantly generated** if there is a small [[set]] $I$ and a small set $J$ such that

* $cof(I)$ is precisely the collection cofibrations of $C$;

* $coj(J)$ is precisely the collection of acyclic cofibrations in $C$; and

* $I$ and $J$ permit the [[small object argument]].

In this case we have necessarily that

* $inj(J)$ is precisely the collection of fibrations on $C$;

* $inj(I)$ is pecisely the collection of acyclic cofibrations of $C$.

## Special case: presentable/combinatorial model category ##

In the special case that the [[model category]] $C$ is a [[presentable category]] the condition or it to be cofibrantly generated has a more elegant description. In that case it is called a [[combinatorial model category]]. See there for more on this.

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

For the general case a useful reference is for instance the first section of 

* [[Tibor Beke]], _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0102087))

For the case of a [[presentable category]] a useful reference is [[Higher Topos Theory|HTT section A.1.2]].
