
# Uniform covers
* table of contents
{: toc}

## Idea

A uniform cover is an [[open cover]] in which enough of the [[subsets]] have a uniform minimal size.  This doesn\'t make sense in (say) an arbitrary [[topological space]], but it does make sense in a [[uniform space]] (or a [[uniform locale]]).  In fact, it\'s possible to *define* a uniform space by specifying which covers are uniform.


## Definitions

The most general definition (that we have here so far) is in a [[uniform space]] or [[uniform locale|locale]], but we can write down the definition in other familiar situations as well.


### In a metric space

Let $X$ be a (pseudo)[[metric space]].  A collection $\mathcal{C}$ of subsets of $X$ is a __uniform cover__ if:

*  For some [[positive number]] $\epsilon$, every [[open ball]] of radius $\epsilon$ is contained in some element of $\mathcal{C}$.


### In a topological group or vector space

Let $X$ be a [[topological vector space]] or even a [[topological abelian group]].  A collection $\mathcal{C}$ of subsets of $X$ is a __uniform cover__ if:

*  For some [[neighbourhood]] $N$ of $0$ (the [[identity element]] of the group), every set of the form $a + N$ is contained in some element of $\mathcal{C}$.

If $X$ is a [[topological group]], then we have both left-uniform and right-uniform covers, depending on whether we use $a N$ or $N a$ in the definition above.  (I\'m not sure what the convention is, if any, on which is left and which is right.)


### In a uniform space

Sometimes the notion of uniform cover is taken as axiomatic in the definition of [[uniform space]].  But if we define a uniform space in terms of entourages, then we have:

Let $X$ be a [[uniform space]].  A collection $\mathcal{C}$ of subsets of $X$ is a __uniform cover__ if:

*  For some [[entourage]] $U$, every set of the form $U[a] \coloneqq \{ b\colon X \;|\; a \approx_U b \}$ is contained in some element of $\mathcal{C}$.

This definition subsumes both (pseudo)metric spaces and topological groups (although a nonabelian topological group has two uniform structures, corresponding to the two notions of uniform cover).


[[!redirects uniform cover]]
[[!redirects uniform covers]]
