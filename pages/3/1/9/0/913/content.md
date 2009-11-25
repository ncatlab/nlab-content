A __sequence__ is [[function]] whose [[source|domain]] is a [[subset]] of the set $\mathbf{N}$ of [[natural numbers]] (or more generally a subset of the set $\mathbf{Z}$ of integers).  Often one means an __infinite sequence__, which is a sequence whose domain is infinite.  Sequences (especially finite ones) are often called __[[lists]]__ in computer science.  (In [[constructive mathematics]], the domain of a sequence must be a [[decidable subset]] of $\mathbf{Z}$.)

Up to [[bijection]], the only possible sources are those of the form
$$\{i: \mathbf{Z} \;|\; 0 \leq i \lt n\}$$
for $n = 0, 1, 2, \ldots, \infty$; other domains are used for notational convenience.

One normally writes the value of the sequence $a$ at the argument $i$ as $a_i$ rather than $a(i)$.  Similarly, given a term $a[i]$ with the free variable $i$, one often defines a sequence whose values equal those terms as $(a[i])_{i \lt n}$, $\{a[i]\}_i$, or the like.  In fact, one even often says literally 'Let $(a_i)$ be a sequence.' even though 'Let $a$ be a sequence.' would work be less of an abuse of notation.  This is all because notation for sequences arose before [[functions]] were considered in their full generality, and one distinguished a 'sequence' (whose domain was a set of integers) from a 'function' (whose domain was an interval in the real line or a region in the complex plane).  Early mathematicians also often conflated the sequence (the function itself) with its range (a subset of the function\'s [[target]]); hence the use of curly braces.

# Generalisations #

Infinite sequences are often used in topology, but for topology in general, one needs to generalise to [[nets]], also called _Moore--Smith sequences_.  Here one replaces the domain $\mathbf{N}$ by any arbitrary [[direction|directed set]].

Even for situations (such as metric spaces) where sequences classically suffice, the [[constructive mathematics|constructive]] definition of an infinite sequence in $X$ arguably should be a [[multi-valued function]] from $\mathbf{N}$ to $X$, that is a [[span]] $\mathbf{N} \leftarrow A \rightarrow X$ where the map $A \to \mathbf{N}$ is a [[surjection]].  (This is a special case of an alternative definition of [[net]] that uses only [[partially ordered]] directed sets.)  In some type-theoretic [[foundations]] of mathematics, you can get the same result by allowing the sequence to be an 'operation' (which is like a function but need not preserve [[equality]]).

For example, using this definition of generalised sequence, every [[real number]] (defined as a located Dedekind cut) may be represented as a generlised Cauchy sequence, even when this fails with the strict definition of sequence.  Many usual properties of [[metric spaces]] and other [[sequential spaces]] also depend on this.

Why is this not done?  Using either [[excluded middle]] or [[countable choice]], any such map $A \to X$ is equivalent as a [[net]] (in the sense that it has the same eventuality filter) to an actual sequence.  So for the purposes of topology, at least, there is no added generality.  Most mathematicians accept at least one of the needed logical principles (EM or CC), and most mathematicians that doubt one still accept the other, so this better definition (if indeed it is better) is not widely appreciated.  But there are [[topos]]es, even widely studied ones, in which neither principle is valid.  (To be precise, the principle needed is a form of choice weaker than either EM or CC; see \[Richman et al, 1999\] for the precise statement as WCC, although this paper does not consider the definition of sequence.)

+--{: .query}
[[Mike Shulman|Mike]]: I think that redefining a "sequence" to be a certain sort of net creates too much confusion relative to the potential gain.  If you want to use nets, you can just say "net."  If you want to work with the restricted sort of net whose order is induced by a surjection to $N$, then I would suggest introducing a new term for those, like $\omega$-net (since there is an obvious generalization replacing $\omega$ by any other ordinal).  But sequences are used all over the place in mathematics, not just in topology, and the meaning of "sequence" as "function defined on $N$" is so universal that I don't think one should mess with it.

_Toby_:  Of course you're right that we can't just change the definition in mathematics as a whole, only in those contexts where (considering the intended applications) this is equivalent (given WCC) to the standard one.  That this was my intent was hardly clear above, so I rewrote that.  I certainly can't just say 'net'; '$\omega$-net' might work, although I have a vague feeling that that already means something.  I usually say 'presequence' to myself, but that is from a chain of related terms that is hard to motivate in isolation.  'sequential net' might work.

There is a bit of related stuff at [[net]] too, by the way.  I ought to get my own web here and use it to explain the foundations of mathematics from presets (type theory without identity types), where this comes naturally.
=--


# References #
* Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://www.math.fau.edu/Richman/HTML/DOCS.HTM).

[[!redirects sequences]]