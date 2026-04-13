
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
=--
=--


\tableofcontents

## Idea

In [[linear algebra]], what is known as the *rank-nullity theorem* (e.g. 3.22 of [Axler 2015](#Axler15), who calls it the *fundamental theorem of linear maps*) is the statement that for any [[linear map]] $f \colon V \to W$ out of a [[finite-dimensional vector space]], the [[sum]] of 

* the [[rank of a linear map|rank]] $rk(f) \coloneqq dim\big(im(f)\big)$, i.e. the [[dimension of a vector space|dimension]] of the [[image]];

with

* the *nullity* $nl(f) \coloneqq dim\big( ker(f) \big)$, i.e. the [[dimension of a vector space|dimension]] of the [[kernel]]

equals 

* the [[dimension]] $d_V \coloneqq dim(V)$ of the [[domain]] space $V$:

$$
  d_V \;=\; rk(f) + nl(f)
  \,.
$$

This rank-nullity theorem is the [[decategorification]] (under the [[dimension of a vector space|dimension]] [[functor]] $dim \colon FinDimVect \to \mathbb{Z}$) of the stronger statement that $V$ itself is the [[direct sum]] of its [[kernel]] and [[image]] [[vector spaces]]:

$$
  V \;\simeq\; im(f) \oplus ker(f)
  \,.
$$

This may be understood as an instance of the [[splitting lemma]] for [[vector spaces]], or more precisely of the statement ([here](split+exact+sequence#OfVectorSpaces)) that every [[short exact sequence]] of [[vector spaces]], such as

$$
  0 \to ker(f) \longrightarrow V \longrightarrow im(f) \to 0
$$

is a [[split exact sequence]], hence of the form

$$
  0 \to ker(f) \longrightarrow ker(f) \oplus im(f)  \longrightarrow im(f) \to 0
  \,.
$$


## Partial generalization to modules
  {#PartialGeneralizationToModules}


While the rank-nullity theorem does not fully generalize from [[vector spaces]] over [[fields]] to [[modules]] over [[rings]], some aspects do carry over. For instance:

\begin{proposition}\label{OrzechTheorem}
  Let $M$ be a [[finitely generated module]] over a [[unital ring|unital]] [[commutative ring]], and $N \subset M$ a [[submodule]]. Then [[surjective]] module [[homomorphisms]] $f \colon N \twoheadrightarrow M$ are already [[isomorphisms]].
\end{proposition}

This was claimed in [Orzech 1971](#Orzech1971), though with a gap in the proof (cf. [Grinberg 2014](#Grinberg2014)). A full proof was given by [Grinberg 2016](#Grinberg2016). For the special case $N = M$ see also [SP 05G8](#StacksProject05G8).

\begin{proof}\label{ProofOfOrzechTheorem}
The following proof essentially reproduces a [proof by Thomas Browning](https://math.stackexchange.com/a/5120133/58526) using the [[Cayley-Hamilton theorem]].

Let $(m_i \in M)_{i = 1}^k$ be the assumed [[finite set|finite]] [[tuple]] of generators of the module $M$, so that  
$$
  M 
    = 
  \langle m_1,\ldots,m_k\rangle
  \mathrlap{\,.}
$$ 
By the assumption that $f$ is [[surjective]], there must be [[preimages]] $(n_i \in N)_{i =1}^k$, 
hence with 
$$
  m_i 
    = 
  f(n_i)
  \mathrlap{\,.}
$$ 
Moreover, by the assumption that $N$ is a [[submodule]] of $M$, these preimages must be [[linear combinations]] of the generators, 
$$
  n_i 
   = 
  \textstyle{\sum_j} 
    a_{i j} m_j
$$
with [[coefficient]] [[matrix]]
$$
  A = (a_{i j})
  \mathrlap{\,,}
$$ 
so that 
$$
  \vec{n}=A\vec{m}
  \mathrlap{\,.} 
$$

Now, by [[Cayley-Hamilton theorem]], the [[matrix]] $A$ satisfies its own [[characteristic polynomial]] [[equation]]:
$$
  A^k 
    + 
  c_{k-1} A^{k-1}
    +
  \cdots
    +
  c_2 A^2
    +
  c_1 A
    +
  c_0 I
   \;=\;
  0
  \mathrlap{\,.}
$$

Applying this equation to $\vec{m}$ gives
$$
  A^k\vec{m}
    +
  c_{k-1} A^{k-1}\vec{m}
    +
  \cdots
    +
  c_2 A^2 \vec{m}
    +
  c_1 A\vec{m}
    +
  c_0\vec{m}
   \;=\;
  0
  \mathrlap{\,.}
$$

Now consider the step of first substituting $A\vec{m}=\vec{n}$
$$
  A^{k-1}\vec{n}
    +
  c_{k-1} A^{k-2}\vec{n}
    +
  \cdots
    +
  c_2A\vec{n}
    +
  c_1\vec{n}
    +
  c_0\vec{m}
   \;=\;
  0
  \mathrlap{\,.}
$$
and then applying $f$ component-wise, to obtain:
$$
  A^{k-1}\vec{m}
    +
  c_{k-1}A^{k-2}\vec{m}
    +
  \cdots
    +
  c_2A\vec{m}
    +
  c_1\vec{m}
    +
  f(c_0\vec{m})
    \;=\;
  0
  \mathrlap{\,.}
$$

Observe that this has had the effect of reducing the order of the powers of $A$. So, applying the same kind of step again, 
by first substituting $A\vec{m}=\vec{n}$ 
$$
  A^{k-2}\vec{n}
    +
  c_{k-1}A^{k-3}\vec{n}
    +
  \cdots
    + 
  c_2\vec{n}
    + 
  c_1\vec{m}
    +
  f(c_0\vec{m})
  \;=\;
  0
$$
and then applying $f$ component-wise, reduces the order by another unit, to yield:
$$
  A^{k-2}\vec{m}
    +
  c_{k-1}A^{k-3}\vec{m}
    +
  \cdots
    +
  c_2\vec{m}
    +
  f\big(
    c_1\vec{m}
    +
    f(c_0\vec{m})
  \big)
    \;=\;
  0
  \mathrlap{\,.}
$$

Hence by [[recursion|iteration]] of this step we eventually deduce an identity of the form
$$
  \vec{m}
    +
  f\Big(
    c_{k-1}\vec{m}
    +
   f\big(
     c_{k-2}\vec{m}
     +
     f(\cdots)
   \big)
  \Big)
  \;=\;
  0
  \mathrlap{\,.}
$$

But since the $\vec m = (m_i)$ are generators, this same identity thus holds for arbitrary $x \in M$, by forming  [[linear combinations]]:

$$
  x
  +
  f\Big(
    c_{k-1}x
    +
    f\big(
      c_{k-2}x
      +
      f(\cdots)
    \big)
  \Big)
  \;=\;
  0
  \mathrlap{\,.}
$$

Evaluating this for any element $x \in \ker(f)$ in the [[kernel]] of $f$ clearly causes the nested terms to vanish iteratively and hence implies $x = 0$, whence the kernel is trivial. This means that the surjective map $f$ is also [[injective]] and  [therefore](balanced+category#AbelianCategoriesAreBalanced) a  module [[isomorphism]], as claimed.
\end{proof}

## References

### Ordinary

Textbook accounts:

* {#Axler15} Sheldon Axler, 3.22 in: *Linear Algebra Done Right*, Springer (2015) &lbrack;[doi:10.1007/978-3-319-11080-6](https://doi.org/10.1007/978-3-319-11080-6)&rbrack;

A [[formal proof]] of the rank-nullity theorem in the [[Isabelle]] [[proof assistant]]:

* [Archive of Formal Proof](https://www.isa-afp.org/), *[Rank-Nullity Theorem in Linear Algebra](https://www.isa-afp.org/entries/Rank_Nullity_Theorem.html)*

See also:

* Wikipedia, *[Rank-nullity theorem](https://en.wikipedia.org/wiki/Rank%E2%80%93nullity_theorem)*


### Partial generalization to modules
 {#ReferencesPartialGenealizationToModules}

* {#Orzech1971} Morris Orzech: *Onto Endomorphisms are Isomorphisms*, The American Mathematical Monthly **78** 4 (1971) 357-362 \[<a href="https://doi.org/10.2307/2316897">doi:10.2307/2316897</a>, [jstor:2316897](https://www.jstor.org/stable/2316897)\]

* {#Grinberg2014} [[Darij Grinberg]]: *Is Orzech's generalization of the surjective-endomorphism-is-injective theorem correct?* (2014) &lbrack;[MO:q/1065786](https://math.stackexchange.com/q/1065786/58526)&rbrack;

* {#Grinberg2016} [[Darij Grinberg]]: *A constructive proof of Orzech’s theorem* (2016) &lbrack;[pdf](https://www.cip.ifi.lmu.de/~grinberg/algebra/orzech.pdf), [[Grinberg-OrzechTheorem.pdf:file]]&rbrack;

* {#StacksProject05G8} [[The Stacks Project]]: [Tag 05G8](https://stacks.math.columbia.edu/tag/05G8)


[[!redirects fundamental theorem of linear maps]]

[[!redirects Orzech's theorem]]
[[!redirects Orzech theorem]]

