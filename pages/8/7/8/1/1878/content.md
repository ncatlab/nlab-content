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

### Special case: presentable/combinatorial model category ###

In the special case that the [[model category]] $C$ is a [[presentable category]] the condition for it to be cofibrantly generated has a more elegant description. In that case it is called a [[combinatorial model category]]. See there for more on this.

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

## Properties ##

The following theorem allows to recognize cofibrantly generated model categories by checking fewer conditions.

+-- {: .un_theorem}
###### Theorem
**(recognition theorem for cofibrantly generated model categories)**

Let $C$ be a [[category]] with all small [[limit]]s and [[colimit]]s and  $W$ a class of maps satisfying [[category with weak equivalences|2-out-of-3]] 
and closed under [[retract]]s (in the [[arrow category]]).

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


+-- {: .proof}
###### Proof

This is originally due to [[Dan Kan]], reproduced for instance as theorem 11.3.1 in _ModLoc_ .

We have to show that with weak equivalences $W$
setting $cof_C := cof(I)$ and $fib_C := inj(J)$ defines a model category
structure.

The existence of [[limit]]s, [[colimit]]s and the [[category with weak equivalences|2-out-of-3 property]] holds by assumption, as does closure under [[retract]]s of $W$.

Closure under retracts of $fib$ and $cof$ follows by the general statement that
classes of morphisms defined by a left or right lifting property are closed under
retracts (e.g. 7.2.8 in _ModLoc_ ).

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
    \downarrow^f && \downarrow^{\mathrlap{\in W}} && \downarrow^f
    \\
    Y &\stackrel{=}{\to}& Y 
    & \stackrel{=}{\to} & Y
  }
$$

that exhibits $f$ as a weak equivalence.

=--



## References ##

A standard textbook reference is section 11 of

* **ModLoc**, Hirschhorn, _Model categories and their localization_ .

For the general case a useful reference is for instance the first section of 

* [[Tibor Beke]], _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0102087))

For the case of a [[presentable category]] a useful reference is [[Higher Topos Theory|HTT section A.1.2]].
