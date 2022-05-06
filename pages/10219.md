
# Split supports
* table of contents
{: toc}

## Definition

Recall that the **[[support]]** of an object $X$ of a [[regular category]] (or [[n-category]]) is its [[(-1)-truncation]], i.e. the [[image]] of the map $X\to 1$ to the [[terminal object]].  Let $\Vert X \Vert$ denote its support.

We say that $X$ has a **split support** if the canonical map $X\to {\Vert X \Vert}$ has a [[section]].  Since $\Vert X \Vert$ is a [[subterminal object]], it is equivalent to say that there exists any morphism ${\Vert X \Vert} \to X$.

If all objects has split supports, we say that **supports split** in the ambient category.


## Relation to axiom of choice

Supports splitting in a category is a weak form of the external [[axiom of choice]] (all regular epis split).  In fact, the splitting of supports is exactly the "difference" between the external axiom of choice and the *internal* axiom of choice, i.e.

$$ EAC \Leftrightarrow (IAC \;\text{ and }\; SS).$$


## In foundations

### In set theory

If we assume [[excluded middle]], then supports split in the category [[Set]].  This has little to do with the foundational [[axiom of choice]]; it is more like [[well-pointed category|well-pointedness]].  Note, however, that to say there is a *function* assigning to every $X$ a section of $X\to {\Vert X \Vert}$ is much stronger: such a function is a global [[choice operator]].

In [[constructive mathematics]], however, it may not be true that all supports split in Set; this can fail in the [[internal logic]] of some [[toposes]].  (Note that the "internal" version of "supports split in Set" in a topos may not be the same as the statement that supports split as an external statement about the topos itself.)  See [(Fourman-Scedrov)](#FourmanScedrov) and [(KECA)](#KECA).  Thus, splitting of supports can be regarded as a weaker form of [[excluded middle]].


### In (homotopy) type theory

In [[type theory]] under [[propositions as types]]), where assertions of existence are always witnessed, to say that "all supports split" would by default mean that there is a *function* as above, assigning to every $X$ a section of $X\to {\Vert X \Vert}$, and imply the global axiom of choice.  To recover the statement which depends only on excluded middle, we need an additional truncation:

$$ \prod_{(X:Type)} \Vert ( \Vert X \Vert \to X ) \Vert. $$

We might pronounce this version as "all supports [[mere proposition|merely]] split".

In [[homotopy type theory]], the pure constructive version of "all supports split" ($\prod_{(X:Type)} \Vert X \Vert \to X$) is in fact inconsistent: it contradicts the [[univalence axiom]].  As before, the truncated version is true under LEM but may fail otherwise.


#### Objects with split support

Since not all supports split in homotopy type theory, it is interesting to consider whether the support of some particular type is split.  For instance, for any $f:A\to B$, the type $qinv(f) \coloneqq \sum_{g:B\to A} (f g = id_B) \times (g f = id_A)$ has split support, since its support can be proven to be equal to the type of coherent equivalence data on $f$.

It is shown in [(KECA)](#KECA) that a type in homotopy type theory has split support if and only if it admits a [[steady function|steady]] endomap.  Thus, it has merely split support if and only if it merely admits a steady endomap.

Some general classes of types can be shown *not* to have split support, at least not uniformly, by arguments similar to the one which shows that not all types have split support.  For instance, the identity type $x=_A y$ has split support for all $x,y:A$ if and only if $A$ is an [[h-set]]; this is proven in [(KECA)](#KECA), and the "only if" direction is also a special case of Theorem 7.2.2 of [[the HoTT book]].

Similarly, we have:

+-- {: .un_theorem}
###### Theorem
If the type $steady(f)\coloneqq \prod_{(x,y:A+A)} (f x = f y)$ has split support for every [[endomap]] $f:A+A\to A+A$, then $A$ is an [[h-set]].
=--
+-- {: .proof}
###### Proof
Given $a,b:A$ with $\Vert a=b\Vert$, we show $a=b$; this suffices to show that $A$ is a set.  Define $g,h : A \to A+A$ to be constant at $inl(a)$ and $inl(b)$ respectively, and $f = [g,h] : A+A \to A+A$.  Then

$$steady(f) =  ( (A\times A) \to ((a=a) \times (a=b) \times (b=a) \times (b=b)) ) $$

Since $\Vert a=b\Vert$, we have $\Vert steady(f)\Vert$.  Thus, by assumption, $steady(f)$; hence $a=b$.
=--

In particular, not all types of the form $steady(f)$ have split support.  Thus, "steadiness" is not as well-behaved a notion as being quasi-invertible.


## References

* {#FourmanScedrov} M. P. Fourman and A. Scedrov. The "world's simplest axiom of choice" fails. 
*Manuscripta Math.*, 38(3):325{332, 1982.
 

* {#KECA} [[Nicolai Kraus]], [[Martin Escardo]], [[Thierry Coquand]], [[Thorsten Altenkirch]], _Generalizations of Hedberg's theorem_, in M. Hasegawa (Ed.): TLCA 2013, LNCS 7941, pp. 173-188. Springer, Heidelberg 2013. [PDF](http://www.cs.bham.ac.uk/~mhe/papers/hedberg.pdf).  

  (In this paper, types with split support are called "h-stable")
 


[[!redirects split support]]
[[!redirects split supports]]
[[!redirects supports split]]

[[!redirects h-stable type]]
[[!redirects h-stable types]]
