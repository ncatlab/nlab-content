

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Diagram chasing lemmas
+-- {: .hide}
[[!include diagram chasing lemmas - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _four lemma_ is one of the basic [[diagram chasing]] lemmas in [[homological algebra]].
It follows directly from the [[salamander lemma]]. It directly implies the [[five lemma]].

## Statement

Let $\mathcal{A}$ be an [[abelian category]]. 

+-- {: .num_prop}
###### Proposition

Consider a [[commuting diagram]] in $\mathcal{A}$ of the form

$$
  \array{
    &\to& &\stackrel{\xi}{\to}& &\to&
    \\
    \downarrow^{\mathrlap{\tau}}
    &&
    \downarrow^{\mathrlap{f}}
    &&
    \downarrow^{\mathrlap{g}}
    &&
    \downarrow^{\mathrlap{\nu}}
    \\
    &\to& &\stackrel{\eta}{\to}& &\to&
  }
$$

where 

1. the rows are [[exact sequences]],

1. $\tau$ is an [[epimorphism]],

1. $\nu$ is a [[monomorphism]].

Then

1. $\xi(ker(f)) = ker(g)$ (the [[image]] under $\xi$ of the [[kernel]] of $f$ is the [[kernel]] of $g$)

1. $im(f) = \eta^{-1}(im(g))$ (the [[preimage]] under $\eta$ of the [[image]] of $g$ is the [[image]] of $f$)

(the "strong four lemma") and hence in particular

1. if $g$ is an [[epimorphism]] then so is $f$;

1. if $f$ is a [[monomorphism]] then so is $g$

(the "weak four lemma").

=--

A direct proof from the [[salamander lemma]] is spelled out at _[salamander lemma -- implications -- four lemma](salamander+lemma#FourLemma)_.

## References

The strong/weak four lemma appears as lemma 3.2, 3.3 in chapter I and then with proof in lemma 3.1 of chapter XII of

* [[Saunders MacLane]], _Homology_ (1967) reprinted as Classics in Mathematics, Springer (1995)
 {#MacLane}


[[!redirects 4 lemma]]
