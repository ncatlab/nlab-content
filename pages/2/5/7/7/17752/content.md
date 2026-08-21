

## Idea

The _Jordan-H&#246;lder theorem_ says that every _[[composition series]]_ of a given [[group]], and every _[[Jordan-Hölder sequence]]_ on a given object in an [[abelian category]], has the same length, and the same [[simple object|simple]] factors, up to [[permutation]]. In particular says that the [[length of an object]] in an abelian category is well defined.

More generally, a form of the theorem holds in any [[homological category]].

## Proof

This is a proof of the classical version of the theorem.

\begin{theorem}
  \label{JHT}
  Every [[composition series]] of a given [[finite object|finite]] [[group]] has the same length and the same [[simple object|simple]] factors up to [[permutation]].
\end{theorem}

\begin{proof}
  \label{JHT}
  Let $G$ be a [[finite object|finite]] [[group]] with two [[composition series]] $G = G_0 \rhd ... \rhd G_n$ (a) and $G = G_0\prime \rhd ... \rhd G_m\prime$ (b) where $G_n = G_m\prime = 1$ (the [[trivial group]]) and $n$, $m$ are nonzero [[natural numbers]]. Proceed by [[induction]] on $|G|$. The base case is trivial. In the inductive case:

  If $G_1 = G_1\prime$ (case A), then we have two composition series for the same group of order less than $|G|$. By induction, $n = m$ and we have a permutation relating the [[quotient group|factor groups]], which can be easily extended (as $G_0/G_1 = G_0\prime/G_1\prime$), so this case is done.

  If $G_1 \neq G_1\prime$ (case B), then we have $G_1 \lhd G$ and $G_1\prime \lhd G$, so $G_1 G_1\prime = \{ g g\prime | g \in G_1, g\prime \in G_1\prime \} \lhd G$. As both $G_1$ and $G_1\prime$ are both maximal [[normal subgroup|normal]] in $G$ and $G_1 G_1\prime$ contains both, $G_1 G_1\prime = G$. Thus, by the [[second isomorphism theorem]] for groups, $G/G_1 \cong G_1\prime/(G_1 \cap G_1\prime)$ and $G/G_1\prime \cong G_1/(G_1 \cap G_1\prime)$. Let $H \coloneq G_1 \cap G_1\prime$; due to the previous [[isomorphisms]] $H$ is maximal normal in both $G_1$ and $G_1\prime$.

  Now, let $H = H_2 \rhd ... \rhd H_l$ be a composition series for $H$. Thus we have two new composition series $G = G_0 \rhd G_1 \rhd H_2 \rhd ... \rhd H_l = 1$ (c) and $G = G_0\prime \rhd G_1\prime \rhd H_2 \rhd ... \rhd H_l = 1$ (d). By case A we see that $n = l$ and that there are isomorphisms relating (a) and (c). Similarly, by case A we also see that $m = l$ and that there are isomorphisms relating  (b) and (d). These, as well as the isomorphisms $G_0/G_1 \cong G_1\prime/H_2$ and $G_0\prime/G_1\prime \cong G_1/H_2$, allow us to connect (a) and (b) through (c) and (d).
\end{proof}

## Relation to FTA

The theorem can be seen as a generalization of the [[fundamental theorem of arithmetic]]. Using [[cyclic groups]] to represent positive [[natural numbers]], [[simple object|simple]] cyclic groups correspond to [[prime numbers]] and [[composition series]] correspond to [[prime factorizations]].

## References

* [[David Speyer]], _The Jordan-H&#246;lder theorem_ ([pdf](https://web.archive.org/web/20210926062254/http://www.math.lsa.umich.edu/~speyer/594_2013/JordanHolder.pdf))

[[!redirects Jordan-Holder theorem]]
[[!redirects Jordan–Hölder theorem]]
[[!redirects Jordan–Holder theorem]]
