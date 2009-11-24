<div class="rightHandSide toc">
[[!include model category theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea  ##

A [[model category]] $C$ is _cofibrantly generated_ if there is a [[set]]
(meaning: small set, not a proper class) of cofibrations and one of trivial cofibrations, such that all other (trivial) cofibrations are _generated_ from these.

## Definition ##

We need the following general terminology

+-- {: .un_defn}
###### Definition
**(cells and injectives)**

Let $C$ be a category with all [[colimit]]s and let $S \subset Mor(C)$ a class of morphisms. We write

* $rlp(S)$ for the collection of morphisms with the _right_ 
  [[weak factorization system|lifting property]] 
  with respect to $S$;
  
* $llp(S)$ for the collection of morphisms with the _left_ 
  [[weak factorization system|lifting property]] with respect to $S$.

Moreover, we also write, now for $I \subset Mor(C)$: 

* $cell(I)$ for the class of morphisms obtained by [[transfinite composition]] of [[pushout]]s of elements in $I$;

* $cof(I)$ for the class of [[retract]]s (in the [[arrow category]] $Arr(C)$) of elements in $cell(I)$

* $inj(I) := rlp(I)$ for the class of morphisms with the right [[lifting property]] with respect to $I$.

=--

+-- {: .un_defn}
###### Definition
**(cofibrantly generated model category)**


A [[model category]] with all [[colimit]]s is **cofibrantly generated** if there is a small [[set]] $I$ and a small set $J$ such that

* $cof(I)$ is precisely the collection cofibrations of $C$;

* $cof(J)$ is precisely the collection of acyclic cofibrations in $C$; and

* $I$ and $J$ permit the [[small object argument]].

=--

Since $I$ and $J$ are assumed to admit the [[small object argument]] the collection of cofibrations and acyclic cofibrations has the following simpler characterization:

+-- {: .un_proposition}
###### Proposition

In a cofibrantly generated model category we have

* $cof(I) = llp(rlp(I))$

* $cof(J) = llp(rlp(J))$.

=--

And therefore the fibrations are precisely $rlp(J)$ and the acyclic fibrations precisely $rlp(I)$.

+-- {: .proof}
###### Proof

The argument is the same for $I$ and $J$. So take $I$. 

By definition we have $I \subset llp(rlp(I))$ and it is checked that collections of morphisms given by a left lifting property are stable under pushouts, transfinite composition and pushouts. So $cof(I) \subset llp(rlp(I))$.

For the converse inclusion we use the [[small object argument]]: let $f : X \to Z$ be in $llp(rlp(I))$. The small object argument produces a factorization
$f : X \stackrel{f' \in cof(I)}{\to} Y \stackrel{f''\in rlp(I)}{\to} Z$. 

It follows that $f$ has the left [[lifting property]] with respect to $f''$ which yields a morphism $\sigma$ in

$$
  \array{
    X &\stackrel{f'}{\to}& Y
    \\
    \downarrow^{\mathrlap{f}} 
    &{}^\sigma\nearrow& \downarrow^{\mathrlap{f''}}
    \\
    X &\stackrel{=}{\to}& X
  }
$$

which exhibits $f$ as a retract of $f'$

$$
  \array{
     X &\stackrel{=}{\to}& X &\stackrel{=}{\to}& X
     \\
     \downarrow^{\mathrlap{f}} && 
     \downarrow^{\mathrlap{f''}} && 
     \downarrow^{\mathrlap{f}}
     \\
     Z &\stackrel{\sigma}{\to}& Y
     &\stackrel{f''}{\to}&
     Z
  }
  \,.
$$

Therefore $f \in cof(I)$.

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


## Examples ##

...

## Related concepts ##

* A cofibrantly generated model category that is also a [[locally presentable category]] is called a [[combinatorial model category]].

* A cofibrantly generated model category for which the doamins of the morphisms in $I$ and $J$ are [[compact object]]s or [[small object]]s is a [[cellular model category]].

## References ##

A standard textbook reference is section 11 of

* **ModLoc**, Hirschhorn, _Model categories and their localization_ .

For the general case a useful reference is for instance the first section of 

* [[Tibor Beke]], _Sheafifiable homotopy model categories_ ([arXiv](http://arxiv1.library.cornell.edu/abs/math/0102087))

For the case of a [[presentable category]] a useful reference is [[Higher Topos Theory|HTT section A.1.2]].
