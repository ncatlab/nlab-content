

## Idea

Given a [[function]] $f$ of $n$ [[variables]], and given $n$ functions $\{g_i\}$ of one variable, then the _total derivative_ of the composite function $t \mapsto f(g_1(t),\cdots, g_n(t))$ is (if it exists) simply its [[derivative]] with respect to $t$, but understood as a [[linear combination]]of the [[partial derivatives]] of $f$, via the [[chain rule]]:

$$
  \frac{d f}{d t}
    =
  \sum_i
  \frac{\partial f}{\partial g_i}
  \,
  \frac{d g_i}{d t}
  \,.
$$

This has various evident generalizations. One is the [[horizontal derivative]] in [[variational calculus]], see at _[[variational bicomplex]]_.

[[!redirects total derivatives]]