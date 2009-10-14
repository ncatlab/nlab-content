
#Contents#
* autoamtic table of contents goes here
{:toc}

# Definition #

The **string group** $String(n)$  is defined to be, as a [[topological group]], the [[Whitehead tower|3-connected cover]] of the [[Spin group]] $Spin(n)$, for any $n \in \mathbb{N}$.

Notice that $Spin(n)$ itself is the [[Whitehead tower|simply connected cover]] of the [[special orthodonal group]] $SO(n)$, which in turn is the connected component (of the identity)  of the [[orthogonal group]] $O(n)$. Hence $String(n)$ is one element in the [[Whitehead tower]] 

$$
  \cdots Fivebrane(n) \to String(n) \to Spin(n) \to SO(n) \to O(n)
  \,.
$$

of $O(n)$. The next higher connected group is called the [[Fivebrane group]].

The [[homotopy group]]s of $O(n)$ are for $k \in \mathbb{N}$ and for sufficiently large $n$

$$
  \array{
     \pi_{8k+0}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+1}(O) & = \mathbb{Z}_2
     \\
     \pi_{8k+2}(O) & = 0
     \\
     \pi_{8k+3}(O) & = \mathbb{Z}
     \\
     \pi_{8k+4}(O) & = 0
     \\
     \pi_{8k+5}(O) & = 0
     \\
     \pi_{8k+6}(O) & = 0
     \\
     \pi_{8k+7}(O) & = \mathbb{Z}
  }
  \,.
$$

By [[Whitehead tower|co-killing]] these groups step by step one gets

$$
  \array{
     cokill this &&&& to get
     \\
     \\
     \pi_{0}(O) & = \mathbb{Z}_2 &&& SO
     \\
     \pi_{1}(O) & = \mathbb{Z}_2 &&& Spin
     \\
     \pi_{2}(O) & = 0
     \\
     \pi_{3}(O) & = \mathbb{Z} &&& String
     \\
     \pi_{4}(O) & = 0
     \\
     \pi_{5}(O) & = 0
     \\
     \pi_{6}(O) & = 0
     \\
     \pi_{7}(O) & = \mathbb{Z} &&& Fivebrane
  }
  \,.
$$


## defining by co-killing of $\pi_3$ ##

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

# generalization to other groups #

One may consider the universal 3-connected cover of any general [[compact space|compact]], [[simple Lie group|simple]] and [[simply connected]]  [[Lie group]] $G$, in complete analogy to the case $G = Spin(n)$. Accordingly one speaks of string-groups $String_G$.

Of these the case $G = $ [[E8]] is the other one relevant in [[string theory]]: see [[Green-Schwarz mechanism]].

# References #


Originally the String-group was just known by its generic name: with $\mathcal{B} O \langle 8 \rangle$ being the topologist's notation for the [[connected cover|7-connected]] of the [[delooping]] $\mathcal{B}O$ of the group $O$.

When it was realized that lifts of the structure maps $X \to \mathcal{B}O$ of the [[tangent bundle]] of a [[manifold]] $X$ through the projection $\mathcal{B}O\langle 8 \rangle \to \mathcal{B}O$ -- now called a [[String structure]] -- play the same role in [[string theory]] as a [[Spin structure]] does in ordinary [[quantum mechanics]], the term _String group_ for $\Omega (\Mathcal{B}O\langle 8 \rangle)$ was suggested.

Following some inquiries by [[Jim Stasheff]] and confirmed in private email by [[Haynes Miller]] it seems that the first one to propose the term _$String$ group_ for the group known to topologists as $\Omega (\mathcal{B}O\langle 8\rangle)$ was [[Haynes Miller]].


Until somebody invests more energy into this entry here, there is this

* blog entry on [String(n)](http://golem.ph.utexas.edu/string/archives/000572.html)


[[!redirects String group]]