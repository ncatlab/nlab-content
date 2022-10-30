# Idea #

A [[triangulated category]], or at least an [[enhanced triangulated category]], is a model for a [[stable (infinity,1)-category]]. The archetypical example of these is the [[stable (infinity,1)-category of spectra]] of [[topological space]]s. For topological spaces there is the classical notion of [[Postnikov system]].

A Postnikov system in a general triangulated category is an abstraction of that topological construction to the general case.

# Definition #

Given a triangulated category $D$ a finite complex over $D$ is any sequence of objects and morphisms in $D$

$$
X^\bullet = \{ X^0 \stackrel{d^0}\to X^1 \stackrel{d^1}\to X^2 \stackrel{d^2}\to\ldots \stackrel{d^n}\to X^n\}
$$

in which $d_k\circ d_{k-1} = 0$. 

A __right Postnikov system subordinated to__ $X^\bullet$ is given by the following data

* a sequence of objects and morphisms

$$Y^0\stackrel{f_1}\leftarrow Y^1\stackrel{f_2}\leftarrow Y^2 \stackrel{f_3}\leftarrow\ldots\stackrel{f_{n-1}}\leftarrow Y^{n-1}\stackrel{f_n}\leftarrow Y^n= X^n[1]$$

* morphisms $j_{k-1}: Y^k\to X^k[n-k+1]$, $k = 0,\ldots,n-1$ with $j_{n-1} = id : Y^n = X^n[1]\to X^n[1]$

* morphisms $i_k : X^k[n-k]\to Y^{k+1}$, $k = 0,\ldots,n-1$

such that 

$$ j_k\circ i_k = d^k[n-k]: X^k[n-k]\to X^{k-1}[n-k], \,\,\,\,\,\,\,for\,\,\,all\,\,\,\,\,\,\,\,  0\lt k \lt n-1 $$

(in particular, $i_{n-1} = d^{n-1}$) and for all $0\leq k\leq n$ the triangles

$$
 X^k[n-k]\stackrel{i_k}\to Y^{k+1}\stackrel{f_k}\to Y^k
\stackrel{j_{k-1}}\to X^k[n-k+1]
$$

are distinguished.

A __right convolution__ of complex $X^\bullet$ is any object in $D$ of the form $Y^0[n-1]$ where $Y^0$ is the 
target end of the sequence as above in some right Postnikov system subordinated to $X^\bullet$.

There is also a left-hand version of Postnikov systems and convolutons; however the classes of left and right convolutions of complex $X^\bullet$ coincide. If $D = K^b(A)$ is the triangulated category of bounded complexes in an additive category $A$ then many examples can be obtained via [[twisted complex]]es in that setup, as introduced by Kapranov. 

The standard reference (beware typoi!) is chapter 4 (exercise section after 4.2) of

* S. I. Gel'fand, Yu. I. Manin, _Methods of homological algebra_, Russian &#1053;&#1072;&#1091;&#1082;&#1072; 1988, English Springer (2 editions).