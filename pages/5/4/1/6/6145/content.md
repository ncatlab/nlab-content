
#Contents#
* table of contents
{:toc}

## Definition. 

Given a [[locally compact topological group]] $G$, a system of imprimitivity on $G$ consists of a

* unitary representation $\rho: G\to U(H)$ on a Hilbert space $H$

* a locally compact Hausdorff space $X$ with continuous left $G$-action

* a regular [[projection-valued measure]] $P:B(X)\to End H$ where $B(X)$ is the Borel $\sigma$-algebra of $X$

such that 

$$
\rho(g)P(E)\rho(g)^{-1} = P(gE)
$$

for all $g\in G$ and $E\in B(X)$. 

#### An approach via $\ast$-representations

In the above definition, one can replace the projection-valued measure $P$ by a $\ast$-representation $M : C_0(X)\to H$ of the $C^\ast$-algebra $C_0(X)$ by defining $M(f) = \int f dP$, then 
$$
\rho(g)M(f)\rho(g^{-1}) = M(L_g f), \,\,\,\,L_g(f)(x) := f(g^{-1}x).
$$
On the other hand, any $M$ satisfying this property defines a regular projection-valued measure as above. 


#### Extensions

Remark: A possible extension is to replace $X$ by a measurable space with a measurable left action of $G$.

## Applications

This concept is important in Mackey machinery and in the applications to the study of coherent states and Berezin quantization.

## References

* [[Gerald B. Folland]], Sec. 6.4 in: *A course in abstract harmonic analysis*, Studies in Advanced Mathematics. CRC Press (1995) &lbrack;[pdf](https://sv.20file.org/up1/1415_0.pdf), [gBooks](http://books.google.com/books?hl=en&lr=&id=0VwYZI1DypUC)&rbrack;

[[!redirects systems of imprimitivity]]