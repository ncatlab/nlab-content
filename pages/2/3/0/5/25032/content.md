
\tableofcontents

## Definition

Given a set $V$ with an [[extensional relation]] $\prec$ on $V$, a **ordered pairing structure** on $V$ is a [[binary function]] $(-,-):V \times V \to V$ such that 

* for all $a \in V$ and $b \in V$, $a \prec (a, b)$ and $b \prec (a, b)$

* for all $a \in V$, $a' \in V$, $b \in V$, $b' \in V$, $a = a'$ and $b = b'$ if and only if $(a, b) = (a', b')$

## Foundational concerns

In any [[material set theory]] one could add a primitive binary operation $(-,-)$ which takes material sets $a$ and $b$ and returns a material set $(a, b)$ such that 

* for all $a$ and $b$, $a \prec (a, b)$ and $b \prec (a, b)$

* for all $a$, $a'$, $b$, $b'$, $a = a'$ and $b = b'$ if and only if $(a, b) = (a', b')$

## See also

* [[ordered pair]]

* [[axiom of pairing]] 

## References

* [[Håkon Robbestad Gylterud]], [[Elisabeth Bonnevier]], *Non-wellfounded sets in HoTT* ([arXiv:2001.06696](https://arxiv.org/abs/2001.06696))

[[!redirects ordered pairing structures]]