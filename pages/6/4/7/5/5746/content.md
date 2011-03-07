
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\mathfrak{g}=\bigoplus_{i}\mathfrak{g}^i$ a [[differential graded Lie algebra]], let $MC(\mathfrak{g})$ be the set of [[Maurer-Cartan element]]s, i.e.,

$$
MC(\mathfrak{g})=\{x\in \mathfrak{g}^1 such that dx+\frac{1}{2}[x,x]=0\}
$$

One thinks element in this set as _flat $\mathfrak{g}$-[[connection on a bundle|connection]]s: indeed

$$
x\in MC(\mathfrak{g}) \Leftrightarrow (d+[x,-])^2=0.
$$

The subspace $\mathfrak{g}^0$ of $\mathfrak{g}$ is a [[Lie algebra]]; the group 

$$
  exp(\mathfrak{g}^0)
$$

acts on as a group of [[gauge transformation]]s on the set of $\mathfrak{g}$-connections (by conjugation), and this action preserves the subset of flat connections. Hence we have a _gauge action_ of  $exp(\mathfrak{g}^0)$ on $MC(\mathfrak{g})$:
$$
e^{a}(d+[x,-])e^{-a}=d+[e^a*x,-].
$$
Explicitely,
$$
e^a*x=x+\sum_{n=0}^\infty \frac{([a,-])^n}{(n+1)!}([a,x]-da)
$$

The _Deligne groupoid_ $Del(\mathfrak{g})$ of the dgla $\mathfrak{g}$ is the [[nLab:action groupoid|action groupoid]]
$$
Del(\mathfrak{g})=MC(\mathfrak{g})// exp(\mathfrak{g}^0)
$$


## Examples

For $\mathfrak{g}$ a [[nLab:Lie algebra|Lie algebra]] this is the [[delooping|delooping groupoid]] $\mathbf{B} exp(\mathfrak{g})=*//exp(\mathfrak{g})$.

## Related concepts

* [[Lie integration]]


## References

Parts of the above is taken from

* [[Domenico Fiorenza]], _[[domenicofiorenza:The periods map of a complex projective manifold. An oo-category perspective]]_