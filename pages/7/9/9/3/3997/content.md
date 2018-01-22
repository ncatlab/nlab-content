

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



# Creation of limits
* table of contents
{: toc}

## Definition

Let $F\colon C\to D$ be a [[functor]] and $J\colon I\to C$ a [[diagram]].  We say that $F$ **creates** limits for $J$ if $J$ has a limit whenever the composite $F\circ J$ has a limit, and $F$ both [[preserved limit|preserves]] and [[reflected limit|reflects]] limits of $J$.  This means that, in addition to $J$ having a limit whenever $F \circ J$ does, a [[cone]] over $J$ in $C$ is a limiting cone if and only if its image in $D$ is a limiting cone over $F\circ J$.

Of course, a functor $F$ creates a [[colimit]] if $F^{op}$ creates the corresponding limit.

If $F$ creates all limits or colimits of a given type (i.e. over a given category $I$), we simply say that $F$ creates that sort of limit (e.g. $F$ creates products, $F$ creates equalizers, etc.).

## Examples

A [[monadic functor]] creates all limits that exist in its codomain, and all colimits that exist in its codomain and are preserved by the corresponding monad (or, equivalently, by the monadic functor itself).  Creation of a particular sort of [[split coequalizer]] figures prominently in Beck's [[monadicity theorem]].

## Terminological remarks

MacLane uses a different definition of creation of limits in [[Categories Work]], which reads  

* $F : C \to D$ creates limits for $J : I \to C$, if to every limiting cone $L$ over $F J$ in $D$ there exists a unique cone $L'$ over $J$ which is mapped to $L$, and this $L'$ is a limit of $J$.

 This definition is **non-equivalent** to the one given here in two ways:

1. MacLane's definition imposes strict equality conditions on objects, which violates the [[principle of equivalence]].

2. MacLane's definition implies the preservation of limits only if a limiting cone exists in $D$. For example, $1\to 2$ creates limits for $1\to 1$ in MacLane's sense, but not in the sense of the definition given here.

The additional strictness in MacLane's definition is useful to give a version of the [[monadicity theorem]] up to isomorphism - rather than equivalence - of categories.

* [Kissinger](http://permalink.gmane.org/gmane.science.mathematics.categories/6644) suggested a concise way to state creation/preservation/etc. of limits.  However, there is [some dispute](https://nforum.ncatlab.org/discussion/7024/lifted-limit/?Focus=56765#Comment_56765) about its correctness.

## Related pages

* [[preserved limit]]

* [[reflected limit]]

* **created limit**

* [[lifted limit]]

[[!redirects created limits]]
[[!redirects creation of limits]]
[[!redirects created colimit]]
[[!redirects created colimits]]
[[!redirects creation of colimits]]

[[!redirects creates limits]]
[[!redirects creates colimits]]