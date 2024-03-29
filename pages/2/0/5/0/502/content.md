
# Choice objects
* table of contents
{: toc}

## Definitions and terminology

As it is used here, and by (at least some) [[topos]] theorists, a **choice object** is an object $B$ such that the [[axiom of choice]] holds when making choices _from_ $B$.

By contrast, a [[projective object]] is an object $A$ such that AC holds when making choices _indexed by_ $A$.

Confusingly, some constructivists use "choice set" to mean what we call a "[[projective set]]".


## Properties

One way to state the axiom of choice is that every [[entire relation]] from $A$ to $B$ (so that every element of $A$ is related to some element of $B$) contains (the graph of) a [[function]] $A\to B$.  With this terminology, we may say that

* $A$ is _projective_ iff every entire relation from $A$ to $B$, for any $B$, contains a function $A\to B$, while
* $B$ is _choice_ iff every entire relation from $A$ to $B$, for any $A$, contains a function $A\to B$.

Equivalently (at least, in a topos) $B$ is choice iff it has a _[[choice function]]_: a function $c\colon P^+B \to B$ such that $c(x)\in x$ for all $x\in P^+B$.  Here $P^+B$ is the object of all [[inhabited set|inhabited]] subsets of $B$.  We can also say that an object is choice if and only if it is [[well-order|classically well-orderable]] (that is, it admits a [[total order]] where every inhabited subset has a least element); see D4.5.13 in the [[Elephant]].

In [[constructive mathematics]], the principle of [[excluded middle]] is equivalent to the statement that the set $2 = \{a \ne b\}$ is a choice set.

## Related entries

* [[projective object]]

* [[axiom of choice]]

* [[well-ordering theorem]]

## References

* [[Peter Freyd]], _Choice and Well-ordering_ , APAL **35** (1987) pp.149-166.

* M.-M. Mawanda, _Well-ordering and Choice in Toposes_ , JPAA **50** (1988) pp.171-184.

* {#Johnstone} [[Peter Johnstone]], _[[Sketches of an Elephant]] vol. II_, Oxford UP 2002. (D4.5, pp.987-998)

[[!redirects choice object]]
[[!redirects choice objects]]
[[!redirects choice set]]
[[!redirects choice sets]]
[[!redirects well-orderable set]]
[[!redirects well-orderable sets]]
