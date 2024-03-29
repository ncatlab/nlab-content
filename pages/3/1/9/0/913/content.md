
# Sequences
* table of contents
{: toc}

## Definitions

A __sequence__ is a [[function]] whose [[source|domain]] is a [[subset]] of the set $\mathbb{N}$ of [[natural numbers]] (or more generally a subset of the set $\mathbb{Z}$ of [[integers]]; cf. *[[bi-infinite sequence]]* and the further generalizations [below](#Generalizations)).  Often one means an __infinite sequence__, which is a sequence whose domain is infinite.  Sequences (especially finite ones) are often called __[[lists]]__ in computer science.  (In [[constructive mathematics]], the domain of a sequence must be a [[decidable subset]] of $\mathbb{Z}$.) 

Sequences may also be indicated by functions $\omega \to X$ where $\omega$ is the first countably infinite [[ordinal]]: the key piece of structure on $\mathbb{N}$ relevant for the study of sequences, particularly in analysis, is the order structure. 

Up to [[bijection]], the only possible [[domains]] are those of the form
$$ \{i\colon \mathbb{Z} \;|\; 0 \leq i \lt n\} $$
for $n = 0, 1, 2, \ldots, \infty$; other domains are used for notational convenience.

An alternative generalisation takes the domain to be a set of [[ordinal numbers]], without loss of generality the set
$$ \{i\colon \Ord \;|\; i \lt \alpha\} $$
for $\alpha$ some specific ordinal number (or the [[proper class]] $\Ord$ of all ordinal numbers, if one wishes to allow for a proper class). 

A _subsequence_ of a sequence $a = a_n: \mathbb{N} \to X$ is a composition 

$$\mathbb{N} \stackrel{i}{\to} \mathbb{N} \stackrel{a}{\to} X$$ 

where $i$ is an order-preserving monomorphism. The salient point is that $i$ be [[cofinal diagram|cofinal]] as an embedding. 


## Notation

One normally writes the value of the sequence $a$ at the argument $i$ as $a_i$ rather than $a(i)$.  Similarly, given a term $a[i]$ with the free variable $i$, one often defines a sequence whose values equal those terms as $(a[i])_{i \lt n}$, $\{a[i]\}_i$, or the like.  In fact, one even often says literally 'Let $(a_i)$ be a sequence.' even though 'Let $a$ be a sequence.' would be less of an abuse of notation.  This is all because notation for sequences arose before [[functions]] were considered in their full generality, and one distinguished a 'sequence' (whose domain was a set of integers) from a 'function' (whose domain was an interval in the real line or a region in the complex plane).  Early mathematicians also often conflated the sequence (the function itself) with its range (a subset of the function\'s [[target]]); hence the use of curly braces.  All of this applies in greater generality to [[families]] with index sets other than $\mathbb{N}$.


## Generalisations
 {#Generalization}

### Nets

Infinite sequences are often used in [[topology]], but for topology in general, one needs to generalise to [[nets]], also called _Moore--Smith sequences_.  Here one replaces the domain $\mathbb{N}$ by any arbitrary [[direction|directed set]].

### Sequential nets

Recall that [[weak countable choice]] is a rather weak version of the [[axiom of choice]] that is accepted even in most schools of [[constructive mathematics]]; it follows separately from both [[excluded middle]] and [[countable choice]].  However, when it fails (as it does in the [[internal language]] of some widely studied [[toposes]], such as the [[topos of sheaves]] over the [[real line]]), then some important results about sequences fail, including many standard results in [[topology]].  In this case, we may want a slight generalisation that we call _sequential nets_.

A __[[sequential net]]__ is a [[multi-valued function]] from $\mathbb{N}$ (or a [[decidable subset|decidable]] [[subset]] thereof) to $X$, that is a [[span]] $\mathbb{N} \leftarrow A \rightarrow X$ where the map $A \to \mathbb{N}$ is a [[surjection]] (or has a decidable range).  Note that $A$ inherits the structure of a directed set via $A \to \mathbb{N}$, so that $A \to X$ is a net.  As a net, every sequential net is equivalent (in the sense of corresponding to the same [[filter]]) to some sequence, if you assume WCC.  Without WCC, however, this equivalence fails.

(Using a multi-valued function here is a special case of an alternative definition of [[net]] that uses only [[partially ordered]] directed sets; see [[net]].  In some [[foundations of mathematics]], we can get the same result by defining a sequential net to be a __presequence__: a [[prefunction]], which is like a function but need not preserve [[equality]], from $\mathbb{N}$ or a decidable subset thereof.)

Without WCC, many of the usual properties of [[metric spaces]] and other [[sequential spaces]] fail, but they continue to hold using sequential nets in the place of sequences.  For example, every (located Dedekind) [[real number]] may be represented as a sequential Cauchy net, even when they might not all be represented as Cauchy sequences; see [[Cauchy real number]].

## Sequence types

In [[dependent type theory]], a sequence type is simply the [[function type]] $\mathbb{N} \to A$, and thus comes with the following rules:

Formation rules for sequence types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathbb{N} \to A \; \mathrm{type}}$$

Introduction rules for sequence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, n:\mathbb{N} \vdash a(n):A}{\Gamma \vdash \lambda(n:\mathbb{N}).a(n):\mathbb{N} \to A}$$

Elimination rules for sequence types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:\mathbb{N} \to A, n:\mathbb{N} \vdash \mathrm{ev}(a, n):A}$$

Computation rules for sequence types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, n:\mathbb{N} \vdash a(n):A}{\Gamma, m:\mathbb{N} \vdash \beta_\Pi(m):\mathrm{ev}(\lambda(n:\mathbb{N}).a(n), m) =_{A} a(m)}$$

Uniqueness rules for sequence types:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:\mathbb{N} \to A \vdash \eta_\Pi(a):a =_{\mathbb{N} \to A} \lambda(n:\mathbb{N}).a(n)}$$

Sequence types also have their own extensionality principle, called [[sequence extensionality]]. This states that given two sequences $a:\mathbb{N} \to A$ and $b:\mathbb{N} \to A$ there is an [[equivalence of types]] between the [[identity type]] $a =_{\mathbb{N} \to A} b$ and the [[dependent sequence type]] $(n:\mathbb{N}) \to (a(n) =_{A} b(n))$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:\mathbb{N} \to A, b:\mathbb{N} \to A \vdash \mathrm{seqext}(a, b):(a =_{\mathbb{N} \to A} b) \simeq (n:\mathbb{N}) \to (a(n) =_{A} b(n))}$$

Sequence types are used in [[strongly predicative mathematics]], where one does not have [[function types]], to construct the [[real numbers]]. 

## Sequence spaces

In [[functional analysis]], one considers [[topological vector spaces]] of infinite sequences; these are the [[sequence spaces]].  (Actually, these generalise quite nicely to [[net]] spaces.)

## Related concepts

* [[limit of a sequence]]

* [[sequentially compact space]]

* [[sequence algebra]]

* [[sequential net]]

* [[tuple]], **sequence**, [[function]]

* [[dependent tuple]], [[dependent sequence]], [[dependent function]]

Not all that related, but similar sounding:

* [[sequential limit]]

[[!redirects sequence]]
[[!redirects sequences]]
[[!redirects infinite sequence]]
[[!redirects infinite sequences]]

[[!redirects sequence type]]
[[!redirects sequence types]]

[[!redirects presequence]]
[[!redirects presequences]]

[[!redirects pre-sequence]]
[[!redirects pre-sequences]]

[[!redirects subsequence]]
[[!redirects subsequences]]

[[!redirects sub-sequence]]
[[!redirects sub-sequences]]
