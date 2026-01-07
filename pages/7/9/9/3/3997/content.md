

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


* table of contents
{: toc}

## Definition

Let $F\colon C\to D$ be a [[functor]] and $J\colon I\to C$ a [[diagram]], and suppose that the composite $F \circ J$ has a [[limit]].  We say that $F$ **creates** this limit if $J$ has a limit, and $F$ both [[preserved limit|preserves]] and [[reflected limit|reflects]] limits of $J$.  The latter two conditions together mean that a [[cone]] over $J$ in $C$ is a limiting cone if and only if its image in $D$ is a limiting cone over $F\circ J$.

Of course, a functor $F$ creates a [[colimit]] if $F^{op}$ creates the corresponding limit.

If $F$ creates all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ creates that sort of limit (e.g. $F$ creates products, $F$ creates equalizers, etc.).

## Examples

\begin{proposition}\label{MonadicFunctorsCreateLimits}
**([[monadic functors]] [[created limit|create limits]])**
A [[monadic functor]] 

1. creates all limits that exist in its [[codomain]];

1. creates all colimits that exist in its codomain and are preserved by the corresponding monad (or, equivalently, by the monadic functor itself).  

\end{proposition}
(e.g. [MacLane 71, Exercise IV.2.2 (p. 138)](#MacLane71))



Creation of a particular sort of [[split coequalizer]] figures prominently in Beck's [[monadicity theorem]].



## Terminological remarks

### Creation of non-existing limits

It seems that the notion of "creating a limit" is used most frequently when the limits exist in the codomain.  One may want to extend the terminology to cases when such limits don't exist, which would require making a choice about whether a non-existing limit should be regarded as "created".

In [[Categories Work]] the convention is that a functor creates *all* limits that do not exist in its codomain.  In this case, the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ has a limit whenever $F\circ J$ has a limit, and *in that case* limits of $J$ are preserved and reflected by $F$."  (But see below for an additional difference with [[Categories Work]].)

On the other hand, one might argue that it doesn't make sense to regard a limit that exists in the domain as being "created by the functor" if the limit in the codomain doesn't even exist.  In this case the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ has a limit whenever $F\circ J$ has a limit, and *furthermore in all cases* limits of $J$ are preserved and reflected by $F$."

Finally, one might even argue that based on the meaning of the English word "created", only something that exists can be created at all.  In this case the more generally applicable definition could be stated as "$F$ creates limits for $J$ if $J$ and $F\circ J$ both have limits, and furthermore limits of $J$ are preserved and reflected by $F$."

#### Relation to lifting limits

If $F$ creates limits for $J$, then it necessarily [[lifted limit|lifts]] limits for $J$ as well. Conversely, so long as $F \circ J$ has a limit, creation of limits for $J$ is equivalent to lifting and reflection of limits for $J$. Thus, one could give an alternative definition for limit creation by saying "$F$ creates limits for $J$ iff it lifts and reflects limits for $J$", which also applies to the case of non-existing limits.

### Strictness

The definitions given above are all "up to isomorphism", i.e. they satisfy the [[principle of equivalence]].  The definition in [[Categories Work]] is additionally *strict*: it requires that for every limiting cone $L$ over $F J$ in $D$ there exists a *unique* cone $L'$ over $J$ which is mapped *exactly* to $L$, and this $L'$ is a limit of $J$.  This is used in stating the version of the [[monadicity theorem]] that characterizes the [[category of algebras for a monad]] up to [[isomorphism]] rather than [[equivalence of categories]]. For [[amnestic functor|amnestic]] [[isofibrations]] the strict and the non-strict notion are equivalent.

## Remarks

[Kissinger](https://raw.githubusercontent.com/punkdit/categories/26b751bbcbe6765fe447e805629ff6416f4c38b1/gmane/science/mathematics/categories/6644) suggested a concise way to state creation/preservation/etc. of limits.  However, there is [some dispute](https://nforum.ncatlab.org/discussion/7024/lifted-limit/?Focus=56765#Comment_56765) about its correctness.


## Related pages

* [[preserved limit]]

* [[reflected limit]]

* **created limit**

* [[lifted limit]]


## References

* {#MacLane71} [[Saunders Mac Lane]], Definition V.1 in: _[[Categories for the Working Mathematician]]_ (1971)


* [[Jiří Adámek]], [[Horst Herrlich]], [[George E. Strecker]], Definition 13.17(2) in: _[[Abstract and Concrete Categories]]_.


* [[Emily Riehl]], §3.3 in: *[[Category Theory in Context]]*, Dover Publications (2017) &lbrack;[pdf](https://emilyriehl.github.io/files/context.pdf), [book website](https://math.jhu.edu/~eriehl/context/)&rbrack;
  


[[!redirects created limits]]
[[!redirects creation of limits]]
[[!redirects created colimit]]
[[!redirects created colimits]]
[[!redirects creation of colimits]]

[[!redirects creates limits]]
[[!redirects creates colimits]]

[[!redirects closure under limits]]
[[!redirects closure under colimits]]