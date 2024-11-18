
\tableofcontents

## Idea

The notion of clustering generalizes convergence.

## Definition

A __cluster space__ is a [[set]] $S$ together with a [[relation]] $\rightsquigarrow$ from $\mathcal{F}S$ to $S$; if $F \rightsquigarrow x$, we say that $F$ __clusters__ at $x$ or that $x$ is a __cluster point__ of $F$.  The axioms are as follows:

1. Centred: The [[principal ultrafilter]] $F_x \rightsquigarrow x$;
2. Antitone: If $F \supseteq G$ and $F \rightsquigarrow x$, then $G \rightsquigarrow x$;
3. Codirected: If $F \cap G \rightsquigarrow x$ then $F \rightsquigarrow x$ or $G \rightsquigarrow x$.
4. Nontrivial: If $F \rightsquigarrow x$, then $F$ is proper.

Note that the direction of isotony and directedness for clustering is the reverse of that for convergence (hence 'antitone' and 'codirected').  Nontriviality is the nullary version of directedness (equivalent to the statement that the improper filter never clusters at any point), which we explicitly need this time.  Alternatively, we can take $\rightsquigarrow$ as a relation only on the *proper* filters; then nontriviality may be omitted from the axioms (as was done in the original reference, [Muscat 2015](#Muscat2015)).

Every convergence space is a cluster space (using the usual definition of $\rightsquigarrow$ from $\to$), and many of the notions of convergence generalize to cluster spaces, including continuous functions, open/closed sets, neighborhood filters, pre-closure, compactness, etc.

This definition of a cluster space does not seem to work in [[constructive mathematics]].  In particular, Muscat\'s proof that every convergence space satisfies the directedness axiom relies on [[excluded middle]], and the [[lesser limited principle of omniscience]] follows if it holds in the [[real line]], for example.  It\'s not clear yet what if any alternative will work better.

## Related concepts

* [[convergence space]]

## References

* Joseph Muscat (2015). An axiomatization of filter clustering. Conference: 2015 12th International Conference on Fuzzy Systems and Knowledge Discovery (FSKD). [DOI:10.1109/FSKD.2015.7381908](https://doi.org/10.1109/FSKD.2015.7381908).
  {#Muscat2015}

[[!redirects cluster space]]
[[!redirects cluster spaces]]
[[!redirects clustering space]]
[[!redirects clustering spaces]]
[[!redirects cluster structure]]
[[!redirects cluster structures]]
[[!redirects clustering structure]]
[[!redirects clustering structures]]
[[!redirects cluster relation]]
[[!redirects cluster relations]]
[[!redirects clustering relation]]
[[!redirects clustering relations]]