
#Contents#
* automatic table of contents goes here
{:toc}

## Idea: use a string of spheres not just one!
Given a locally compact and $\sigma$-compact space $X$, and with a base ray $* : [0,\infty) \to X$, with end $\varepsilon(X)$, the &#268;ech homotopy groups of $\varepsilon(X)$ relative to $*$ are defined by $lim \pi_n(\varepsilon(X))$.  These 'make sense' but do not behave well, since the limit will destroy exactness in situations where we would hope for and expect long exact sequences. E.M. Brown (1974) suggested a different construction based on an infinite string of spheres:
##Strings of spheres
+--{: .un_defn}
######Definition######
Let $\underline{S}^n = ([0,\infity) \cup \bigcup_{k=0}^\infty(S^n \times \{k\})/(k\sim (\underline{1},k)$. This is called a **string of $n$-spheres.**
=--
This, of course, means that $\underline{S}^n $ is defined as a pushout
 
<img src="http://latex.codecogs.com/gif.latex?\xymatrix{\mathbb{N}\ar[r]\ar[d]%26[0,\infty)\ar[d]\\S^n\times\mathbb{N}\ar[r]%26\underline{S}^n}"/>

(Picture to go here)

###Properties###
1. $\varepsilon(\underline{S}^n)$ is a pro-space isomorphic to an $\mathbb{N}$-indexed one with $k^{th}$ level, $\bigvee_{j\geq k}S^n_j$, where each $S^n_j$ is a copy of $S^n$.  The structural/ bonding maps from the $(k+1)^{st}$ level to the $k^{th$ level are the obvious inclusions.

1. The space $\underline{S}^n$ is, of course, considered as being based at the ray (given by the right vertical map in the pushout square).

1. The space $\underline{S}^n$ is a [[spherical object]] and the family $\mathcal{A} = \{\underline{S}^n\}^\infty_{n=0}$ defines a theory.

##The Brown-Grossman homotopy groups##
+--{: .un_defn}
######Definition######
The $n^{th}$ Brown-Grossman homotopy group of $(X,*)$ is given by the  group of based proper homotopy classes of based proper maps from $\underline{S}^n$ to $(X,*)$;

$$\underline{\pi}_n(X,*) = Ho(Proper)(\underline{S}^n, (X,*)).$$
=--


###Properties###
1. As was pointed out above, the $\underline{S}^n$ are cogroups so the $\underline{\pi}_n(X,*)$ are groups, which are abelian for $n\geq 2$.

1. In fact the $\underline{\pi}_n(X,*)$ form a $\Pi_\mathcal{A}$-[[spherical object|algebra]] for $\mathcal{A}$ as above.  Not only are there the sort of morphisms in $\Pi_\mathcal{A}$ that will induce analogues of [[Whitehead products]], [[composition operations]] etc. but there are other interesting morphisms there, for instance: 

1. There is a proper **shift map** $S: \underline{S}^n\to \underline{S}^n$, which  shifts all the spheres one place to the right.   This induces, by composition, a morphism $S^*(X): \underline{\pi}_n(X,*)\to \underline{\pi}_n(X,*)$. This means that each individual $\underline{\pi}_n(X,*)$ has more structure than simply being a group.