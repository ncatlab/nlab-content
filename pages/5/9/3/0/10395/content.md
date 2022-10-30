
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Mapping space
+--{: .hide}
[[!include mapping space - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $G$ a [[topological group]] (or [[Lie group]]) and $P \to X$ a $G$-[[principal bundle]], then forming [[mapping spaces]] out of the [[circle]] yields a free [[loop group]]-[[principal bundle]] over the [[free loop space]] of $X$:

$$
  \array{
    \mathcal{L}G &\to& \mathcal{L} P
    \\
    && \downarrow
    \\
    && \mathcal{L} X
  }
  \,.
$$

In the special case that $X = Y \times S^1$ is a [[Cartesian product]] with the [[circle]], then one can consider the [[subspace]] of the [[free loop space]] of $X$ on those loops whose [[projection]] on the $S^1$-factor is the [[identity]]. This subspace is of course [[equivalence|equivalent]] to $Y$, giving a canonical inclusion

$$
  i \;\colon\; Y \hookrightarrow \mathcal{L} (Y \times S^1)
  \,.
$$

(Abstractly, this is the [[adjunct]] of the [[identity]] under the [[internal hom]]-[[adjunction]].)

Along this inclusion one can [[pullback|pull back]] the $\mathcal{L}G$-principal bundle over $\mathcal{L}X$. The **caloron correspondence** is the statement that if 

$$
  \Omega_{Y} P \hookrightarrow \mathcal{L} P
$$ 

in turn is the subspace on those loops in $P$ which map $0 \in S^1$ to a chosen [[section]] of $P$ over $Y \times \{0\}$, then forming the pullback $i^\ast \Omega_Y P$ in

$$
  \array{
    i^\ast \Omega_Y P &\to& \Omega_Y P
    \\
    \downarrow && \downarrow
    \\
    Y &\stackrel{i}{\longrightarrow}& \mathcal{L}(Y \times S^1)
  }
$$

constitutes an [[equivalence of groupoids]] between that of $G$-[[principal bundles]] over $Y \times S^1$ and [[loop group]]-principal bundles over $Y$.

## Related concepts

* [[double dimensional reduction]]

## References

The term "caloron correspondence" originates in 

* H. Garland, [[Michael Murray]], _Kac-Moody monopoles and periodic instantons_. Comm. Math. Phys., 120(2):335&#8211;351, 1988.

A review and further developments are in

* [[Michael Murray]], Raymond F. Vozzo, _The caloron correspondence and higher string classes for loop groups_, J. Geom. Phys., 60(9):1235-1250, 2010 ([arXiv:0911.3464](http://arxiv.org/abs/0911.3464))

See also

* Pedram Hekmati, [[Michael Murray]], Raymond Vozzo, _The general caloron correspondence_, J. Geom. Phys., 62(2):224-241, 2012 ([arXiv:1105.0805](http://arxiv.org/abs/1105.0805))

[[!redirects caloron correspondences]]
