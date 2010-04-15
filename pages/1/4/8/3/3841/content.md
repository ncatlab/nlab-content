#Contents#
* automatic table of contents goes here
{:toc}

## Definition

An infinite [[cardinal]] $\pi$ is a **regular cardinal** if it satisfies the following equivalent definitions:

* no [[set]] of cardinality $\pi$ is the union of fewer than $\pi$ sets of cardinality less than $\pi$.  

* given a function $P \to X$ (regarded as a family $\{P_x\}_{x\in X}$) such that $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$, then $|P| \lt \pi$.  

* the [[category]] $\Set_{\lt\pi}$ of sets of cardinality $\lt\pi$ has all [[colimits]] of size $\lt\pi$.  

A cardinal that is not regular is called **singular**.

## Examples

### Regular cardinals


* The first (infinite) regular cardinal is $\aleph_0 = |\mathbb{N}|$, because a set with cardinality less than $\aleph_0$ is a [[finite set]], and a finite union of finite sets is still a finite set.

* The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.  (This requires the [[axiom of choice]].)  In the case of $\aleph_1$, this means that a countable union of countable sets is countable.  Note that this implies that there exist arbitarily large regular cardinals: for any cardinal $\lambda$ there is a greater regular cardinal, namely $\lambda^+$.

* Sometimes it is convenient to allow finite cardinals to be considered regular.  In this case, the finite regular cardinals are precisely $0$, $1$, and $2$.  For $0$ this is vacuous; for $1$ it is because the union of an empty set of empty sets is empty; and for $2$ it is because the union of a [[subsingleton]] set of subsingleton sets is again a subsingleton.


### Singular cardinals

* $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and $|\mathbb{N}| = \aleph_0 \lt\aleph_\omega$.

[[!redirects regular cardinals]]
[[!redirects singular cardinal]]
[[!redirects singular cardinals]]
