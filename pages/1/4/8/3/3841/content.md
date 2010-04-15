
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A transfinite [[cardinal]] $\pi$ is a **regular cardinal** if it satisfies the following equivalent definitions:

* no [[set]] of cardinality $\pi$ is the union of fewer than $\pi$ sets of cardinality less than $\pi$.  

* given a function $P \to X$ (regarded as a family $\{P_x\}_{x\in X}$) such that $|X| \lt \pi$ and $|P_x| \lt \pi$ for all $x \in X$, then $|P| \lt \pi$.  

* the [[category]] $\Set_{\lt\pi}$ of sets of cardinality $\lt\pi$ has all [[colimits]] of size $\lt\pi$.  

A cardinal that is not regular is called **singular**.

## Examples

### Regular cardinals


* The first regular cardinal is $\aleph_0 = |\mathbb{N}|$: 

  because a set with cardinality less than $\aleph_1$ is a [[finite set]] and a finite union of finite sets is still a finite set. 


* The [[successor]] of any infinite cardinal, such as $\aleph_1$, is a regular cardinal.


### Singular cardinals

* $\aleph_\omega = \bigcup_{n\in \mathbb{N}} \aleph_n$ is singular, more or less by definition, since $\aleph_n\lt\aleph_\omega$ and $|\mathbb{N}| = \aleph_0 \lt\aleph_\omega$.
