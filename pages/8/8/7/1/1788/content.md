

The MC-forms at a point $X = x^i T_i$ are (by [Helgason 2001, Thm. 7.4](#Helgason01))
$$
    e^i
    \;=\;
    \mathrm{d}x^i
    \left(
      \frac
        {1 - exp(- ad X)}
        {ad X}
      (\partial_k)
    \right)
    \mathrm{d}x^k
$$
where (by [ibid, p. 36](#Helgason01))
$$
  \frac{1 - exp(-A)}{ A }
  \;\;
  \coloneqq
  \;\;
  \sum_{n=0}^\infty
  \tfrac{1}{(n+1)}
  (-A)^n
  \,.
$$
(for $A \colon \mathfrak{g} \to \mathfrak{g}$ any [[linear map|linear]] [[endomorphism]]) so that:
$$
  e^i
  \;=\;
  \mathrm{d}x^i
  \left(
    \textstyle{
      \sum_{n = 0}^\infty
    }
    \tfrac{1}{(n+1)!}
    (
      - ad X
    )^n
    (\partial_k)
  \right)
  \mathrm{d}x^k
  \,.
$$

Unwinding this with 

$$
  (ad X)
  \;=\;
  \big(
    x^j
    f^\bullet_{j \bullet}
  \big)
$$

we get

$$
  e^i
    \;=\;
  \tfrac{1}{1!}
  \mathrm{d}x^i
  -
  \tfrac{1}{2!}
  f^i_{jk}x^j \mathrm{d}x^k
  +
  \tfrac{1}{3!}
  f^i_{j k'}
  f^{k'}_{k l}
  x^j x^k \mathrm{d}x^l
  + 
  \cdots
$$




## References

* {#Helgason01} [[Sigurdur Helgason]], §I.8 in: *Differential geometry, Lie groups and symmetric spaces*, Graduate Studies in Mathematics **34** (2001) \[<a href="https://bookstore.ams.org/gsm-34">ams:gsm-34</a>\]
