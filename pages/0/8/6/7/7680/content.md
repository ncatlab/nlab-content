[[!redirects II.2, constant and étale k-groups]]

This entry is about a section of the text

* Michel [[Demazure, lectures on p-divisible groups]], [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)

Let $k$ be a field.


+-- {: .num_defn}
###### Definition

If $E$ is a group then the [[constant scheme]] $E_k$ on $E$ carries a [[group scheme|group structure]]. Such an $E_k$ is called constant $k$-group.

=--

+-- {: .num_defn}
###### Definition and Remark

Let $k_s$ denote the field extension of $k$ consisting of separable elements. Let $\Pi:=Gal(k_s/k)$ denote the [[Galois group]] of this extension. Then the functor

$$(-)(k_s):\begin{cases}
et Sch_k
&\to&
Gal(k_s/k)-Set
\\
X
&\to&
X(k_s)
\end{cases}$$

is an equivalence between the category of &#233;tale $k$-schemes and that of sets equipped with a group action of$Gal(k_s/k)$.

Moreover this gives a functor


$$(-)(k_s):\begin{cases}
et Gr_k
&\to&
Gal(k_s/k)-Mod
\\
X
&\to&
X(k_s)
\end{cases}$$

which is an equivalence between the category of &#233;tale $k$[[group scheme|-groups]] and that of groups equipped with a group action of $Gal(k_s/k)$. Note that commutative $Gal(k_s/k)$-groups are called Galois modules, too.

A $k$-group scheme is &#233;tale iff its coefficient extension $X\otimes_k k_s$ along $k\hookrightarrow k_s$ is a constant k-scheme.

=--


* Michel Demazure, lectures on p-divisible groups [web](http://sites.google.com/site/mtnpdivisblegroupsworkshop/lecture-notes-on-p-divisible-groups)
