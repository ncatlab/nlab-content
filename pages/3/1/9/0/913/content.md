
# Sequences
* table of contents
{: toc}

## Definitions

A __sequence__ is [[function]] whose [[source|domain]] is a [[subset]] of the set $\mathbb{N}$ of [[natural numbers]] (or more generally a subset of the set $\mathbb{Z}$ of integers).  Often one means an __infinite sequence__, which is a sequence whose domain is infinite.  Sequences (especially finite ones) are often called __[[lists]]__ in computer science.  (In [[constructive mathematics]], the domain of a sequence must be a [[decidable subset]] of $\mathbb{Z}$.)

Up to [[bijection]], the only possible sources are those of the form
$$\{i: \mathbb{Z} \;|\; 0 \leq i \lt n\}$$
for $n = 0, 1, 2, \ldots, \infty$; other domains are used for notational convenience.

One normally writes the value of the sequence $a$ at the argument $i$ as $a_i$ rather than $a(i)$.  Similarly, given a term $a[i]$ with the free variable $i$, one often defines a sequence whose values equal those terms as $(a[i])_{i \lt n}$, $\{a[i]\}_i$, or the like.  In fact, one even often says literally 'Let $(a_i)$ be a sequence.' even though 'Let $a$ be a sequence.' would be less of an abuse of notation.  This is all because notation for sequences arose before [[functions]] were considered in their full generality, and one distinguished a 'sequence' (whose domain was a set of integers) from a 'function' (whose domain was an interval in the real line or a region in the complex plane).  Early mathematicians also often conflated the sequence (the function itself) with its range (a subset of the function\'s [[target]]); hence the use of curly braces.  All of this applies in greater generality to [[families]] with index sets other than $\mathbb{N}$.


## Generalisations

Infinite sequences are often used in topology, but for topology in general, one needs to generalise to [[nets]], also called _Moore--Smith sequences_.  Here one replaces the domain $\mathbb{N}$ by any arbitrary [[direction|directed set]].

Even for situations (such as metric spaces) where sequences classically suffice, the [[constructive mathematics|constructive]] definition of an infinite sequence in $X$ arguably should be a __sequential net__: a [[multi-valued function]] from $\mathbb{N}$ to $X$, that is a [[span]] $\mathbb{N} \leftarrow A \rightarrow X$ where the map $A \to \mathbb{N}$ is a [[surjection]].  (This is a special case of an alternative definition of [[net]] that uses only [[partially ordered]] directed sets.)  In some [[foundations]] of mathematics, you can get the same result by defining a sequential net to be a __presequence__: a [[prefunction]] (which is like a function but need not preserve [[equality]]) from $\mathbb{N}$.

For example, every [[real number]] (defined as a located Dedekind cut) may be represented as a sequential Cauchy net, even when they might not all be represented as Cauchy sequences.  Many usual properties of [[metric spaces]] and other [[sequential spaces]] also hold constructively using sequential nets.

Why are sequential nets not commonly seen?  Using either [[excluded middle]] or [[countable choice]], every sequential net is equivalent as a net (in the sense that it has the same [[eventuality filter]]) to a sequence.  So for the purposes of [[topology]], at least, there is no added generality.  Most mathematicians accept at least one of the needed logical principles ($EM$ or $CC$), and most mathematicians that doubt one still accept the other, so this better concept (if indeed it is better) is not widely appreciated.  But there are [[toposes]], even widely studied ones, in which neither principle is valid.  (To be precise, the principle needed is [[weak countable choice]].)

+--{: .query}
[[Mike Shulman|Mike]]: I think that redefining a "sequence" to be a certain sort of net creates too much confusion relative to the potential gain.  If you want to use nets, you can just say "net."  If you want to work with the restricted sort of net whose order is induced by a surjection to $N$, then I would suggest introducing a new term for those, like $\omega$-net (since there is an obvious generalization replacing $\omega$ by any other ordinal).  But sequences are used all over the place in mathematics, not just in topology, and the meaning of "sequence" as "function defined on $N$" is so universal that I don't think one should mess with it.

_Toby_:  Of course you're right that we can't just change the definition in mathematics as a whole, only in those contexts where (considering the intended applications) this is equivalent (given WCC) to the standard one.  That this was my intent was hardly clear above, so I rewrote that.  I certainly can't just say 'net'; '$\omega$-net' might work, although I have a vague feeling that that already means something.  I usually say 'presequence' to myself, but that is from a chain of related terms that is hard to motivate in isolation.  'sequential net' might work.

There is a bit of related stuff at [[net]] too, by the way.  I ought to get my own web here and use it to explain the foundations of mathematics from presets (type theory without identity types), where this comes naturally.
=--


[[!redirects sequence]]
[[!redirects sequences]]
[[!redirects infinite sequence]]
[[!redirects infinite sequences]]

[[!redirects sequential net]]
[[!redirects sequential nets]]
[[!redirects presequence]]
[[!redirects presequences]]
