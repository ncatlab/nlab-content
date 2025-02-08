
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[representation theory]], *unitarization* refers to [[isomorphisms]] from a given [[linear representation]] on a [[Hermitian space|Hermitian]] [[inner product space]] ([[Hilbert space]]) to that [[underlying]] a [[unitary representation]].

## Properties

### Existence for compact groups

For $G$ a *[[compact topological group|compact]]* [[topological group]] then every [[linear representation]] $\rho \,\colon\,G \to Aut(\mathscr{H})$ on a ([[complex numbers|complex]] [[separable Hilbert space|separable]]) [[Hilbert space]] may be unitarized by re-defining the [[inner product]] of $\mathscr{H}$ to be the "[[group averaging]]" of the original one, given by the [[integration|integral]]

\[
  \label{GroupAveragedInnerProduct}
  \langle v, w \rangle_{new}
  \;\coloneqq\;
  \int_{g \in G} 
  \big\langle
    \rho(g)(v)
    ,\,
    \rho(g)(w)
  \big\rangle_{old}
  \,
  \mathrm{d}g
\]

against the [[Haar measure]] on $G$.

(cf. [Knapp 1996, Prop. 4.6](#Knapp96))

\begin{remark}
**(Terminology)**
Some authors refer to (eq:GroupAveragedInnerProduct) as Weyl's *unitarian trick* or similar, cf. [Gomez 2009 p 5](#Gomez09). But the original "unitarian trick" of [Weyl 1939 pp 137](#Weyl39) (cf. [Knapp96, Prop. 7.15](#Knapp96)) is really referring to a another construction which just uses the above unitarization as an intermediate step (cf. [Knapp96, p 445](#Knapp96)).
\end{remark}

\begin{example}
  In the case that $G$ is a [[finite group]], the formula (eq:GroupAveragedInnerProduct) reduces to the [[sum]]
\[
  \langle v, w \rangle_{new}
  \;\coloneqq\;
  \tfrac{1}{{\vert G \vert}}
  \sum_{g \in G}
  \big\langle
    \rho(g)(v)
    ,\,
    \rho(g)(w)
  \big\rangle_{old}
  \,,
\]

and it is elementary to see that this new inner product is indeed preserved:

$$
  \begin{array}{l}
    \big\langle
      \rho(h)(v)
      ,\,
      \rho(h)(w)
    \big\rangle_{new}
    \\
    \;=\;
    \tfrac{1}{{\vert G \vert}}
    \,
    \sum_{g \in G}
    \Big\langle
      \rho(h)\big(\rho(g)(v)\big)
      ,\,
      \rho(h)\big(\rho(g)(w)\big)
    \Big\rangle_{old}
    \\
    \;=\;
    \tfrac{1}{{\vert G \vert}}
    \,
    \sum_{g \in G}
    \big\langle
      \rho(h g)(v)
      ,\,
      \rho(h g)(w)
    \big\rangle_{old}
    \\
    \;=\;
    \tfrac{1}{{\vert G \vert}}
    \,
    \sum_{g' \in G}
    \big\langle
      \rho(g')(v)
      ,\,
      \rho(g')(w)
    \big\rangle_{old}
    \\
    \;=\;
    \tfrac{1}{{\vert G \vert}}
    \,
    \big\langle
      \rho(h)(v)
      ,\,
      \rho(h)(w)
    \big\rangle_{new}
    \mathrlap{\,.}
  \end{array}
$$

\end{example}



## Variations and generalizations

Provided that one assumes enough Choice to ensure weak-star compactness in the unit ball of B(H), for H a Hilbert space: every bounded strong-operator-continuous representation of a locally compact amenable group on a Hilbert space H is unitarizable. See the Wikipedia page for [Uniformly bounded representation](https://en.wikipedia.org/wiki/Uniformly_bounded_representation) \[version: 2025-12-08\] for some of the historical references.

## References

The terminology "unitarian trick" goes back to:

* {#Weyl39} [[Hermann Weyl]]: *The Classical Groups -- Their Invariants and Representations*, Princeton University Press (1939) &lbrack;[jstor:j.ctv3hh48t](https://www.jstor.org/stable/j.ctv3hh48t), [pdf](https://www-fourier.ujf-grenoble.fr/~panchish/ETE%20LAMA%202018-AP/Weyl_The%20Classical%20Groups.pdf), [Wikipedia entry](https://en.wikipedia.org/wiki/The_Classical_Groups)&rbrack;
  > "We therefore take refuge in what might be called the unitarian trick: each group is replaced by the subgroup of those elements that are unitary transformations."

Textbook account:

* {#Knapp96} [[Anthony W. Knapp]]: *Lie Groups Beyond an Introduction*, Progress in Mathematics **140** (1996, 2002) &lbrack;[ISBN:9780817642594](https://link.springer.com/book/9780817642594)&rbrack;

Lecture notes:

* {#Gomez09} Raul Gomez, p 5 of: *Introduction to Representation Theory of Lie groups* (2009) &lbrack;[pdf](https://pi.math.cornell.edu/~gomez/Files/PDF/Representations.pdf)&rbrack;

See also: 

* Wikipedia: *[Unitarian trick](https://en.wikipedia.org/wiki/Unitarian_trick)*


[[!redirects unitarizations]]
