> under construction

#Contents#
* autoamtic table of contents goes here
{:toc}

# Definition #

The **string group** $String(n)$  is defined to be, as a [[topological group]], the [[Whitehead tower|3-connected cover]] of the [[Spin group]] $Spin(n)$, for any $n \in \mathbb{N}$.

More in detail this means the following.

First notice that since by construction $\pi_i(\mathcal{B}Spin(n)) = 0 $ for $0 \leq i \leq 3$, by the [[Hurewicz theorem]] we have for the degree 4 [[integral cohomology]] group of the [[delooping]]/[[classifying space]] $\mathcal{B}Spin(n)$ that

$$
  H^4(\mathcal{B} Spin(n)) \simeq \pi_4(\mathcal{B}Spin(n))
  \simeq
  \mathbb{Z}
  \,.
$$

The generator of this group is called the **fractional first Pontryagin class** and denoted $\frac{1}{2}p_1 : \mathcal{B} Spin(n) \to \mathcal{B}^4 \mathbb{Z} \simeq K(\mathb{Z},4)$ because for $p_1 : \mathcal{B} SO(n) \to K(\mathbb{Z},4)$ the ordinary first [[Pontryagin class]] it fits into a diagram

$$
  \array{
    \mathcal{B} Spin(n) &\stackrel{\frac{1}{2} p_1}{\to}&
    \mathcal{B}^4 \mathbb{Z}
    \\
    \downarrow && \downarrow^{\cdot 2}
    \\
    \mathcal{B} SO(n) &\stackrel{p_1}{\to}&
    \mathcal{B}^4 \mathbb{Z}
  }
  \,,
$$

where the right vertical morphism comes from multiplication by 2 in $\mathbb{Z}$.

This says that _after being pulled back_ to $\mathcal{B} Spin(n)$ the first Pontryagin class becomes is 2 times the generator of the degree 4 [[intgeral cohomology]] group of $\mathcal{B}Spin(n)$ and hence that generator is called one half of $p_1$, denoted $\frac{1}{2}p_1$ (by slight abuse of notation). 

The [[delooping]] of the String-group as a [[topological group]] is the [[homotopy fiber]] of this fractional Pontyagin class, i.e. the [[homotopy pullback]]

$$
  \array{
    \mathcal{B} String(n) &\to& {*}
    \\
    \downarrow && \downarrow
    \\
    \mathcal{B} Spin(n) &\to& \mathcal{B}^4 \mathbb{Z}
  }
$$

in [[Top]].


In other words: $\mathcal{B}String(n)$ is the $U(1)$- 2-[[gerbe]] or $\mathcal{B}^2 U(1)$ [[principal ∞-bundle]] on $\mathcal{B} Spin(n)$ whose class is $\frac{1}{2}p_1 \in H^4(\mathcal{B}Spin(n), 4)$.



# Models #

## as a topological group ##

There is a model due to Stolz and Teichner in 'What is an elliptic object?'...



## as a smooth 2-group ##

While $Spin(n)$ in not just a [[topological group]] but a (finite dimensional) [Lie group]], $String(n)$ cannot have the structure of a finite dimensional [[Lie group]], due to the fact that the third [[homotopy group]] is nontrivial for every (finite dimensional) Lie group, while for $\pi_3(String(n)) = 0$ by the very definition of $String(n)$.

+--{: .query}
[[David Roberts]]: This raises an interesting question: is there an infinite dimensional Lie group which is a 3-connected cover? This seems very hard to do.
=--

But there are smooth models of $String(n)$ in the form of [[2-group]]s. See [[string 2-group]].

# role in string theory #


The reason for the name is that in [[string theory]], for (blah) to be well-defined, it is necessary for the 
structure group of (blah) to lift to (blah). 

See [[String structure]].

If one considers passing to the (free) [[loop space]] of spacetime and then doing [[quantum mechanics]], the requirement of the previous paragraph is that the structure group lifts to ... (cite Killingback, Mickelsson, Schreiber, Witten,...) 

# generalization to other groups#

One may consider the universal 3-connected cover of any general [[compact space|compact]], [[simple Lie group|simple]] and [[simply connected]]  [[Lie group]] $G$, in complete analogy to the case $G = Spin(n)$. Accordingly one speaks of string-groups $String_G$.

Of these the case $G = $ [[E8]] is the other one relevant in [[string theory]]: see [[Green-Schwarz mechanism]].

#Origin of the term#

Following some inquiries by [[Jim Stasheff]] and confirmed in private email by [[Haynes Miller]] it seems that the first one to propose the term _$String$ group_ for the group known to topologists as $\Omega (\mathcal{B}O\langle 8\rangle)$ was [[Haynes Miller]].

[[!redirects String group]]