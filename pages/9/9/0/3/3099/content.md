
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **(combinatorial) species** is a [[presheaf]] or [[higher category theory|higher categorical]] presheaf on the [[groupoid]] [[core]]([[FinSet]]).


## Definition


### 1-categorical

The [[category]] of **species**, $Species := PSh(core(FinSet))$, is the [[category of presheaves]] on the [[groupoid]] $\mathbb{P} := core(FinSet)$ of [[finite sets]] and [[bijections]], the [[core]] of [[FinSet]]: 

$$
  \hat \mathbb{P} := PSh(core(FinSet))
  \,.
$$

For more, see [[structure type]].

### 2-categorical

A **2-species** (also called a [[stuff type]]) is a [[2-presheaf]] on [[core]]([[FinSet]]), i.e. a [[pseudofunctor]]

$$
  core(FinSet) \to Grpd
$$

to the [[2-category]] [[Grpd]].

### $(\infty,1)$-categorical

Generally, an **$\infty$-species** or **homotopical species** is an [[(∞,1)-presheaf]] of $core(FinSet)$, i.e. an [[(∞,1)-functor]]

$$
  core(FinSet)^{op} \to \infty Grpd
$$

to the [[(∞,1)-category]] [[∞Grpd]].

The [[(∞,1)-category]] of $\infty$-species is the [[(∞,1)-category of (∞,1)-presheaves]]

$$
  \infty Species := PSh_{(\infty,1)}(core(FinSet))
  \,,
$$


## Cardinality

Under [[groupoid cardinality]] 

$$
  |-| : \infty Grpd_{tame} \to \mathbb{R}
$$

every (tame) [[∞-groupoid]] is mapped to a [[real number]]

$$
  X \mapsto |X| := \sum_{[x] \in \pi_0(X)}\prod_{i = 1}^{\infty} (\pi_i(X,x)^{(-1)^{i}})
  \,.
$$

A species $\mathbf{X}$ assigns an [[∞-groupoid]] $\mathbf{X}_n$ to each [[natural number]] $n \in \mathbb{Z}$. Therefore under [[groupoid cardinality]] we may naturally think of a tame species as mapping to a [[power series]]

$$
  \mathbf{X} \mapsto |\mathbf{X}|
  :=
  \sum_{n = 0}^{\infty} \frac{1}{n!} |\mathbf{X}_n| z^n
  \in 
  \mathbb{R}[ [ z ] ]
  \,.
$$

## References

...

[[!redirects homotopical species]]
[[!redirects (infinity,1) species]]
[[!redirects ∞-species]]
