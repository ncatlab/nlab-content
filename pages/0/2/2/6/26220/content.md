
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition
Let $\mathcal{H}=\mathcal{H}_o\oplus\mathcal{H}_c$ be a $\mathbb{Z}$-[[graded vector space]], and $\mathfrak{l}$ a collection of $n$-ary maps that make $(\mathcal{H}_c,\mathfrak{l})$ an [[L-infinity-algebra|$L_\infty$-algebra]]. If there is a collection of maps 

$$
\mathfrak{n}
  \;=\;
\big\{
n_{k,l} \colon (\mathcal{H}_c ^{\otimes k})\otimes (\mathcal{H}_o )^{\otimes l} \to \mathcal{H}_o
\big\}_{k,l\geq 0}
$$

each graded-symmetric for $(\mathcal{H}_c ^{\otimes k})$ satisfying the identities

$$
\begin{array}{l}
\sum_{p+r=n} \sum_{\sigma\in S_n} \frac{(-1)^{\epsilon(\sigma)}}{p! r!} n_{1+r,m}(l_p (c_{\sigma (1)} , \cdots , c_{\sigma (p)}),c_{\sigma (p+1)}, \cdots, c_{\sigma (n)}; o_1, \cdots, o_m) 
\\
\;+\;
\sum_{p+r=n} \sum_{i+s+j=m} \sum_{\sigma\in S_n} \frac{(-1)^{\mu_{p,i}(\sigma)}}{p! r!} n_{p,i+1+j} (c_{\sigma (1)}, \cdots , c_{\sigma (p)}; o_1, \cdots, o_i, n_{r,s}(c_{\sigma (p+1)}, \cdots, c_{\sigma(n)};o_{i+1}, \cdots, o_{i+s}), o_{i+s+1}, \cdots, o_m)
\\
\;=\;
0
\,,
\end{array}
$$

where the sign exponent $\mu_{p,i}(\sigma)$ is defined as

$$
\mu_{p,i}(\sigma) = \epsilon(\sigma)+ (c_{\sigma (1)}+ \cdots + c_{\sigma(p)}) + (o_1+ \cdots + o_i) + (o_1+ \cdots + o_i)(c_{\sigma (p+1}+ \cdots + c_{\sigma (n)})
$$

then $(\mathcal{H},\mathfrak{l},\mathfrak{n})$ is called a **weak open-closed homotopy algebra** (weak OCHA).

If furthermore one has that $l_0=n_{0,0} =0$ then this is an **open-closed homotopy algebra** (OCHA).

## Properties

By definition, $(\mathcal{H}_c,\mathfrak{l})$ is a Lie-infinity-algebra. Furthermore, given a (weak) OCHA one can show that $(\mathcal{H}_o,\{n_{0,k}\})$ is an (weak) [[A-infinity algebra]]. These are interpreted as the closed, and open sectors, respectively (see [[string field theory]] for more on this).

## References

General:

* [[Hiroshige Kajiura]], [[Jim Stasheff]]. *Open-closed homotopy algebra in mathematical physics*. J. Math. Phys. 47, 023506 (2006). ([doi](https://doi.org/10.1063/1.2171524)).
