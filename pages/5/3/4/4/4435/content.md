
For $X$ a [[smooth manifold]], consider the [[de Rham complex]] $(\Omega^\bullet(X), d_{dR})$ of [[differential form]]s on $X$, a [[cochain complex]] with the structure of a [[dg-algebra]].

Every [[vector field]] $v \in \Gamma(T X)$ of $X$ induces a [[derivation]] on this [[dg-algebra]] of degree $-1$ 

$$
  \iota_v : \Omega^\bullet(X) \to \Omega^{\bullet-1}(X)
$$

given by evaluation of forms on $v$.

As every degree -1-map, this induces a [[chain homotopy]] 

$$
  0 \stackrel{\iota_v}{\to} [d_{dR},\iota_v]
  : 
  \Omega^\bullet(X) \to \Omega^\bullet(X)
  \,.
$$

One finds that

* $[d_{dR},\iota_v,] = \mathcal{L}_v$ is the [[Lie derivative]] on forms along $v$;

* $[\mathcal{L}_v, \mathcal{L}_w] = \mathcal{L}_{[v,w]}$

* $[\mathcal{L}_v, \iota_w] = \iota_{[v,w]}$

* $[\iota_v, \iota_w] = 0$.

These relations are sometimes called **Cartan calculus**. The first one is sometimes calledd **Cartan's magic formula**.

[[!redirects Cartan's magic formula]]
