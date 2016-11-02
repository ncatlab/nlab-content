+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
The **topos of recursive sets**, or, for short, the _recursive topos_ , is a [[Grothendieck topos]] $\mathcal{R}$ that provides a [[cartesian closed category|cartesian closed]] context to do higher order recursion theory in. It can be viewed as a discrete analogue to the [[Johnstone's topological topos|topological topos]].

## Definition
Let $\mathbf{R}$ be the monoid of all total [[recursive function|recursive functions]] $\mathbb{N}\to\mathbb{N}$ under concatenation viewed as a category with one object $\mathbb{N}$. Consider the [[coverage]] $J(\mathbb{N})$ whose covers consist of finite families of maps $(f_i:\mathbb{N}\to\mathbb{N} {}|{} 1\leq i \leq n)$ such that $\cup_i Im(f_i)=\mathbb{N}$.

The _recursive topos_ is defined as $\mathcal{R}=Sh(\mathbf{R}, J)$.

## Properties

+-- {: .num_prop}
###### Proposition
$\mathcal{R}$ is a [[local topos]] i.e. the [[global section functor]] $\Gamma:\mathcal{R}\to Set$ has a right adjoint: $\Gamma\dashv B: Set\to \mathcal{R}$.
=--

This appears as prop.1.5 in [Mulry (1982)](#Mulry82). $B$ maps a set $X$ to the sheaf $X^{\mathbb{N}}$ of sequences of elements in $X$.

+-- {: .num_prop #RNO}
###### Proposition
The object $\mathbb{R}_D$ of [[real numbers object|Dedekind real numbers]] corresponds to the sheaf of sequences of real numbers $\langle r_n\rangle$ satisfying:

For all $n\in \mathbb{N}^+$ there exists a finite recursive cover $A_1,\dots A_k$ such that for all $m_1, m_2$ in $A_i$ $(i=1,\dots,k)$, $|r_{m_2}-r_{m_1}|\lt 1/n$.
=-- 

This is prop.4.1 in [Mulry (1982)](#Mulry82).

## Related entries

* [[Johnstone's topological topos]]

* [[bornological topos]]

* [[effective topos]]

* [[recursive function]]

## References

The recursive topos was introduced in

* {#Mulry82}[[Philip Mulry|P. S. Mulry]], _Generalized Banach-Mazur functionals in the topos of recursive sets_ , JPAA **26** (1982) pp.71-83.

A comparison with the [[effective topos]] is in chapter 6 of

* [[Giuseppe Rosolini]], _Continuity and Effectiveness in Topoi_ , PhD thesis University of Oxford 1986. ([ps](ftp://ftp.disi.unige.it/pub/person/RosoliniG/papers/coneit.ps.gz))

See also

* [[Peter Johnstone]], _Sketches of an Elephant vol. I_, Oxford UP 2002. (example A2.1.11(k), p.81)

* [[William Lawvere|F. William Lawvere]], _Diagonal arguments and cartesian closed categories_ , pp.134-145 in LNM **92** Springer Heidelberg 1969. (Reprinted with author's commentary as [TAC Reprint **15** (2006)](http://tac.mta.ca/tac/reprints/articles/15/tr15abs.html))

* [[Philip Mulry|P. S. Mulry]], _Adjointness in recursion_ ,
APAL **32** (1986), pp.281&#8211;289.

* [[Philip Mulry|P. S. Mulry]], _A categorical approach to the theory of computation_ ,
APAL **43** (1989), pp.293&#8211;305.

* [[Philip Mulry|P. S. Mulry]], _Partial map classifiers and partial cartesian closed categories_ , Theor. Comp. Sci. **136** (1994) pp.109&#8211;123.

[[!redirects Mulry topos]]
[[!redirects Mulry-Lawvere topos]]
[[!redirects Lawvere-Mulry topos]]
[[!redirects recursive topos]]