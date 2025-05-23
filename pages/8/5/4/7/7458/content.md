
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

In general, the idea is that an $k$-congruence in an [[n-category]] $K$, where $k\le n$, is an "[[internal category|internal]] $(k-1)$-category" in $K$.  

Here we consider the case $m\le 2$, although we allow $n$ and $m$ to be of the form $(r,s)$; see _[[(n,r)-category]]_.

## Definition

+--{: .num_defn}
###### Definition
Let $D$ be a [[2-congruence]] in a [[2-category]] $K$.

* $D$ is a **(2,1)-congruence** if it is an internal groupoid, i.e. there is a map $D_1\to D_1$ providing "inverses".
* It is a **(1,2)-congruence** if $D_1\to D_0\times D_0$ is ff.
* It is a **1-congruence** if it is both a (2,1)-congruence and a (1,2)-congruence.
* it is a **(0,1)-congruence** if $D_1\to D_0\times D_0$ is an equivalence.
=--

Note that in a 1-category,

* a 2-congruence is just an internal category (a 1-category),
* a (2,1)-congruence is an internal groupoid (a (1,0)-category),
* a (1,2)-congruence is an internal poset (a (0,1)-category), and
* a 1-congruence is an internal equivalence relation (a 0-category).

Of course, a (0,1)-congruence in any 2-category is completely determined by any object $D_0$.

+--{: .num_theorem}
###### Theorem
Let $q:X\to Y$ be a morphism in $K$.  If $Y$ is $n$-truncated for $n\ge -1$, then $ker(q)$ is an $(n+1)$-congruence.  This means that:

1. If $Y$ is [[groupoidal object|groupoidal]], then $ker(q)$ is a (2,1)-congruence.
1. If $Y$ is [[posetal object|posetal]], then $ker(q)$ is a (1,2)-congruence.
1. If $Y$ is [[discrete object|discrete]], then $ker(q)$ is a 1-congruence.
1. If $Y$ is [[nLab:subterminal object|subterminal]], then $ker(q)$ is a (0,1)-congruence.

In all these cases the converse is true if $K$ is [[regular 2-category|regular]] and $q$ is [[nLab:eso morphism|eso]].
=--

+--{: .proof}
###### Proof
The forward directions are fairly obvious; it is the converses which take work.  Suppose first that $ker(q)$ is a (2,1)-congruence, and let $\alpha: f \to g: X \rightrightarrows Y$ be any 2-cell.  Pulling back the eso $q$ along $f$ and $g$ gives $P_1\to T$ and $P_2\to T$; let $r:P \to T$ be the pullback $P_1\times_X P_2$.  Since $K$ is regular, $r$ is eso.  By definition of kernels, the 2-cell $\alpha r$ corresponds to a map $P\to (q/q)$.  But $(q/q)\rightrightarrows C$ is a (2,1)-congruence, so composing this map with the "inverse" map $(q/q)\to(q/q)$ gives another map $P\to (q/q)$, and thereby another 2-cell $f r \to g r$ which is inverse to $\alpha r$.  Finally, since $r$ is eso, precomposing with it reflects invertibility, so $\alpha$ must also be invertible.  Thus $Y$ is groupoidal.

Now suppose that $ker(q)$ is a (1,2)-congruence, and let $\alpha,\beta: f\to g: T\to Y$ be two parallel 2-cells.  With notation as in the previous paragraph, the 2-cells $\alpha r$ and $\beta r$ correspond to morphisms $P\rightrightarrows (q/q)$ which become isomorphic in $X$.  But since $(q/q)\rightrightarrows X$ is a (1,2)-congruence, this implies that the two maps $P\rightrightarrows (q/q)$ are isomorphic, and hence $\alpha r = \beta r$.  And since $r$ is eso, precomposing with it is faithful, so $\alpha=\beta$; thus $Y$ is posetal.

The discrete case follows by combining the posetal and groupoidal cases, so it remains to show that if $ker(q)$ is a (0,1)-congruence then $Y$ is subterminal.  We know it is discrete, so it suffices to show that given two $f,g:T \rightrightarrows Y$ we have a 2-cell $f\to g$.  Continuing with the same notation, and letting $h,k:P\to X$ be the induced maps with $q h \cong f r$ and $q k \cong g r$, we have $(h,k):P\to X\times X = (q/q)$, and therefore the 2-cell defining the fork $(q/q) \;\rightrightarrows\;X \overset{q}{\to} Y$ gives us a 2-cell $q h \to q k$ and therefore $f r \to g r$.  Now $r$ is the quotient of its kernel, so for this 2-cell to induce a 2-cell $f\to g$ it suffices for it to be an action 2-cell for the actions of $ker(r)$ on $f r$ and $g r$; but this is automatic since we know $Y$ to be posetal.  Thus we have a 2-cell $f\to g$ as desired, so $Y$ is subterminal.
=--

## Related concepts

* [[congruence]], [[2-congruence]]

* [[internal category]], [[internal category in an (infinity,1)-category]]

## References

* [[Mike Shulman]], _[[michaelshulman:n-congruence]]_

[[!redirects (n,r)-congruences]]
