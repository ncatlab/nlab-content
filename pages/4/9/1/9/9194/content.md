__Foliated categories__ (cat&#233;gories feuillet&#233;es), or simply __foliations__ (not to be confused with [[foliations]] in differential geometry), were introduced by [[Jean Bénabou]] in unpublished work dating back to 1984.
They are a weaker structure than a [[fibered category]], but still allow one to test for various standard properties of functors fibrewise.


The definition goes as follows: a functor $P\colon \mathbf{X} \to \mathbf{B}$ makes $\mathbf{X}$ a foliated category (over $\mathbf{B}$) if every morphism $f$ in $\mathbf{X}$ factors as a $P$-vertical morphism $v$ (i.e. $P(v)$ is an identity morphism in $\mathbf{B}$), followed by a $P$-[[cartesian morphism]] $k$, i.e. $f = k\circ v$, and, further, $P$-cartesian morphisms are closed under composition. (Note that this is the weaker notion of cartesian morphism.) If closure under composition is not required, we obtain the notion of **prefoliated category**.

A morphism between foliated categories $\mathbf{X}'\to \mathbf{X}$ (over $\mathbf{B}$) is a functor over $\mathbf{B}$ that sends cartesian morphisms to cartesian morphisms, and such that for every object $X'$ of $\mathbf{X}'$, and morphism $f\colon Y\to F(X')$ in $\mathbf{X}$, there is a factorisation $f = F(k)\circ v$, where $v$ is vertical in $\mathbf{X}$ and $k$ is cartesian in $\mathbf{X}'$. Bénabou calls such functors _cartesian_.


## References

* Jean B&#233;nabou, _Cartesian functors and foliated categories_ (1 May 2012), [YouTube](https://www.youtube.com/watch?v=Y1CeHmjNcuk)

* Jean B&#233;nabou, _Foncteurs cart&#233;siens et cat&#233;gories feuillet&#233;es_ (9 November 2012, journ&#233;e Guitart, Paris) [YouTube](https://www.youtube.com/watch?v=p3vcZDyZ4Yo) [slides](https://docs.google.com/presentation/d/17E0epsZWcDTYlwAMZ4PFCLIf4dyigS-WUA0siUtU-wY/edit?hl=fr#slide=id.gce595186_059)

* Jean Bénabou, _Du vieux et du neuf sur la construction de Grothendieck_, March 2019, [YouTube](https://youtu.be/NC0I18B45kE) (the material on foliated categories—called simply foliations—starts after timestamp 1:01:00).

A short summary is in [a message](https://github.com/punkdit/categories/blob/master/gmane/science/mathematics/categories/8243) at Category List.

[[!redirects foliated categories]]
[[!redirects prefoliated category]]
[[!redirects prefoliated categories]]