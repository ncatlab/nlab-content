A __sequence__ is [[function]] whose [[source|domain]] is a [[subset]] of the set $\mathbf{N}$ of [[natural number]]s (or more generally a subset of the set $\mathbf{Z}$ of integers).  Often one means an __infinite sequence__, which is a sequence whose domain is infinite.  Sequences (especially finite ones) are often called __lists__ in computer science.  (In [[constructivism|constructive mathematics]], the domain of a sequence must be a [[decidable subset]] of $\mathbf{Z}$.)

Up to [[bijection]], the only possible sources are those of the form
$$\{i: \mathbf{Z} \;|\; 0 \leq i \lt n\}$$
for $n = 0, 1, 2, \ldots, \infty$; other domains are used for notational convenience.

One normally writes the value of the sequence $a$ at the argument $i$ as $a_i$ rather than $a(i)$.  Similarly, given a term $a[i]$ with the free variable $i$, one often defines a sequence whose values equal those terms as $(a[i])_{i \lt n}$, $\{a[i]\}_i$, or the like.  In fact, one even often says literally 'Let $(a_i)$ be a sequence.' even though 'Let $a$ be a sequence.' would work be less of an abuse of notation.  This is all because notation for sequences arose before [[function]]s were considered in their full generality, and one distinguished a 'sequence' (whose domain was a set of integers) from a 'function' (whose domain was an interval in the real line or a region in the complex plane).  Early mathematicians also often conflated the sequence (the function itself) with its range (a subset of the function\'s [[target]]); hence the use of curly braces.

# Remarks #

Arguably the definition of an infinite sequence should be as a [[span]] $\mathbf{N} \leftarrow A \rightarrow X$ (where $X$ is the target) and the map $A \to \mathbf{N}$ is a [[surjection]].  This is a special case of a definition of [[net]] that uses only [[partial order|partially ordered]] [[directed set]]s.  In some type-theoretic [[foundations]] of mathematics, you can instead allow the sequence to be an 'operation' (like a function but need not preserve equality).

For example, using this definition of sequence, every [[real number]] (defined as a located Dedekind cut) may be represented as a Cauchy sequence, even when this fails with the strict definition of sequence.  The usual properties of [[sequential space]]s also depend on this.

Why is this not done?  Using either [[excluded middle]] or [[countable choice]], any such map $A \to X$ is equivalent as a [[net]] (in the sense that it has the same eventuality filter) as an actual sequence.  So for the purposes of topology, at least, there is no added generality.  Most mathematicians accept at least one of the needed logical principles (EM or CC), and most mathematicians that doubt one still accept the other, so this better definition (if indeed it is better) is not widely appreciated.  But there are [[topos]]es, even widely studied ones, in which neither principle is valid.  (To be precise, the principle needed is a form of choice weaker than either EM or CC; see \[Richman et al, 1999\] for the precise statement as WCC, although this paper does not consider the definition of sequence.)

# References #
* Douglas Bridges, Fred Richman, and Peter Schuster (1998). A weak countable choice principle. Available from [Fred Richman's Documents](http://www.math.fau.edu/Richman/HTML/DOCS.HTM).