
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


# Little sites
* table of contents
{: toc}

## Idea

Let $C$ be a category with a [[pretopology]] $J$ (i.e. a [[site]]) and $a$ an object of $C$. As an analogy with sheaves on a topological space $X$, which are defined on the site $Op(X)$ of open sets of $X$, we can try to define sheaves on $a$, using the elements of covering families of $a$ from $J$. This is called the **little site** of $a$, in contrast to the [[big site]] of $a$ which is the slice category $C/a$ with its induced topology.

The [[topos]] of [[sheaves]] on the little site is the [[petit topos]] of $a$.

A little site may sometimes be called a _small site_, but it\'s probably best to save that name for a site which is a [[small category]].


## Definition

>[[David Roberts]]: The following is experimental, use at own risk, although I'm sure it has been thought about before.

Consider the subcategory $J/a$ of $C/a$ with objects $u_0 \to a$ such that $u_0$ is a member of some covering family $U = \{u_i \to a\}$. Given two such objects $u_0 \to a$, $v_0 \to a$, and  covering families $U$, $V$ that contain them, there is a covering family $W = UV$ which is the pullback (or at least a weak pullback) of $U$ and $V$ in $C$. There is then some element $w$ of $W$ such that there is a square 
$$\array{
w & \to & v_0 \\
\downarrow & & \downarrow \\
u_0  &\to  & a 
}
$$
so $J/a$ is 'a bit like' the category of opens of a space (it's probably [[filtered category|cofiltered]], but I haven't checked that there are weak equalisers).

Now the morphisms of $J/a$ are those triangles
$$\array{
v_0 & \to & u_0 \\
& \searrow& \downarrow \\
  &  & a 
}\, .
$$
such that $v_0 \to u_0$ is an element of a covering family of $u_0$, so the arrows $w \to u_0$ and $w \to v_0$ really are morphisms of $J/a$. Then we say a covering family of $u_0\to a$ is a collection of triangles that, when we forget the maps to $a$, form a covering family of $u_0$ in $C$. This is at the very least a [[coverage]], and so we have a site.

>To be continued...

## Related concept

* **little site**

* [[big site]]


[[!redirects little site]]
[[!redirects little sites]]

[[!redirects small site]]
[[!redirects small sites]]

[[!redirects petit site]]
[[!redirects petit sites]]
