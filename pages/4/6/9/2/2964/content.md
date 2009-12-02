<div class="rightHandSide toc">
[[!include categorification - contents]]
</div>

 * automatic table of contents goes here
 {:toc}

#General case
On this page, we explain a connection between decategorification and degroupoidification, which appears when one considers [[groupoid]] [[internalization|internal to]] [[scheme]]s.  One can construct a category of sheaves attached to such a groupoid, and a sequence of finite groups, given by points over a finite field.  This connection has been exploited quite widely within arithmetic geometry, but has not really been stated in the conntext of categorification.
##Basic data
Let $X\rightrightarrows Y$ be a groupoid internal to schemes ($Y$ is the scheme of [[object]]s and $X$ the scheme of [[morphism]]s) where both schemes are of finite type.

Then we can make two constructions from this scheme:

* The $\mathbb{F}_p$-points $X(\mathbb{F}_p)
\rightrightarrows Y(\mathbb{F}_p)$ form a finite groupoid (with no additional structure).
* There is a [[simplicial object|simplicial]] scheme $N(X\rightrightarrows Y)$ given by the [[nerve]] of $X\rightrightarrows Y$ (this sends $\Delta^n$ to $X\times_Y X\times_Y\cdots  \times_Y X$, with the obvious face and degeneracy maps).

  * One special case is when this is an [[action groupoid]].  The resulting simplicial scheme should be thought of as the Borel space for the action on $Y$.

+--{: .query}
[[David Roberts]]: One could write $Y//X$ for this nerve, as you are considering it as the weak or homotopy quotient. This would help when trying to draw diagrams of simpilicial schemes.

[[Ben Webster]]: Sorry, that is way too confusing for me.  Double-slashes are for [[GIT quotients]] in my world. Also, for whatever reason they look awful on this site.  Even adding negative spaces doesn't make them look less unpleasant.

[[David Roberts]]: Sure. There should be a double slash command in LaTeX - it\'s probably in some obscure package not usable here.

[[Ben Webster]]: In normal LaTeX, two negative spaces (\!) is about right, but here they don't seem to work.  I don't consider negative spaces obscure.

[[David Roberts]]:I mean a single command, like that for double vertical lines (\backslash |)

[[Urs Schreiber]]: possibly the command for double shash is \sslash. It produces "$\sslash$". But I don't have the required font installed, so I can't be sure.

[[Ben Webster]]: Well, it works on one of my computers, so it's the right command...
=--

##Linearization, and the function sheaf correspondence

The latter construction can be "linearized" in an analogous way to [[geometric function theory]], except using the [[constructible derived category|derived category of sheaves with finite rank constructible cohomology]] with coefficients in the [[p-adic number|p-adics]] $\mathbb{Q}_\ell$ for some prime $\ell$ of $N(X\rightrightarrows Y)$.  Let $D(N(X\rightrightarrows Y))$ denote this category.  In fact, we will require the graded version of this category, provided by [[mixed sheaves]].  We denote this graded category $D_{mix}(N(X\rightrightarrows Y))$  


There is a map $\alpha_{q,\ell}$ from $K^0(D_{mix}(N(X\rightrightarrows Y))$ to the set $\mathbb{Q}_\ell[N(X \rightrightarrows Y)(\mathbb{F}_q)]$ of $\mathbb{Q}_\ell$ valued functions on any $\mathbb{F}_q$ point of $N(X\rightrightarrows Y)$ where $\ell$ and $q$ where $\ell$ is a prime and $\ell\nmid q$, given by the supertrace of automorphism of the stalk of the sheaf at that point induced by the action of the Frobenius $q^n$ on $X\times_{\mathrm{Spec}\mathbb{Z}}  \mathrm{Spec}\overline{\mathbb{F}_q}$.

This map has the property that multiplying by the [[motivic integral]] of $\mathbb{A}^1$ (i.e., $m_!m^*$ for the map $m:X\times \mathbb{A}^1\to X$) multiplies the corresponding function by $q$.

Furthermore, no non-zero element of $K^0(D_{mix}(N(X\rightrightarrows Y))$ is killed by this map for all  $q$.

If $N(X_1\rightrightarrows Y_1)\overset{f}\leftarrow N(Z\rightrightarrows W) \overset{g}\rightarrow N(X_2 \rightrightarrows Y_2)$ is a [[span]] of groupoids of schemes, then we have a functor $g_!f^*:D_{mix}(N(X_1\rightrightarrows Y_1))\to D_{mix}(N(X_2 \rightrightarrows Y_2))$, given by pull-back followed by compactly supported pushforward.

Furthermore, there is an induced span of groupoids on this set of $\mathbb{F}_q$-points, which in turn induces a map $(gf)^\dagger$ from $\mathbb{Q}_\ell[N(X_1\rightrightarrows Y_1)(\mathbb{F}_q)]\to \mathbb{Q}_\ell[N(X_2 \rightrightarrows Y_2)(\mathbb{F}_q)]$.

The content of the [[Grothendieck trace formula]] connects these two constructions. 

+--{: .un_theorem}
###### Theorem

The functor  $g_!f^*:D_{mix}(N(X_1\rightrightarrows Y_1))\to D_{mix}(N(X_1\rightrightarrows Y_1))$ induces a map $(gf)_\dagger:K^0(D_{mix}(N(X_1\rightrightarrows Y_1)))\to K^0(D_{mix}(N(X_2 \rightrightarrows Y_2)))$ such that the diagram
$$
  \array{
      K^0(D_{mix}(N(X_1\rightrightarrows Y_1))&\overset{(gf)_\dagger}\to& K^0(D_{mix}(N(X_2 \rightrightarrows Y_2)))   \\
     \downarrow^{\alpha_{q,\ell}} && \downarrow^{\alpha_{q,\ell}} 
     \\
    \mathbb{Q}_\ell[(N(X_1\rightrightarrows Y_1)\mathbb{F}_q)] &\overset{(gf)^\dagger}\to& \mathbb{Q}_\ell[N(X_2 \rightrightarrows Y_2)(\mathbb{F}_q)]
  }
$$
=--

That is, modulo a few details:

+--{: .standout}
The [[decategorification]] of the mixed derived category and [[degroupoidification]] of the $\mathbb{F}_q$ points coincide. 
=--

We note that in many examples of geometric [[categorification]], the fact that the decategorification is correct is checked by   understanding the degroupoidification  and using this theorem, though it is typically not stated this explicitly.

#Examples
Since all groupoids appearing below are action groupoids, I'll denote them $X/G$ in place of $G\times X\Rightarrow X$.

##The Hecke algebra

If one takes the span of groupoids 
$$\array{B\backslash G/B &&&&\\
&\nwarrow&&&\\
&& B\backslash G\times_B G/B &\to &B\backslash G/B\\
&\swarrow&&&\\
B\backslash G/B &&&&\\}$$
over the action groupoid for $B\times B$ acting on the left and right on $G$ for a simple algebraic group, then the resulting monoidal category is the [[Hecke category]] of G.  Its decategorification is the [[Hecke algebra]] of G, which is checked by showing the Hecke algebra is groupoidified 
by the F_q points of this, a result which was proved [Iwahori in 1964](http://www.ams.org/mathscinet-getitem?mr=165016).

##Geometric Satake

Considers the groupoid given by the action of $G(\mathbb{Z}[t])\times G(\mathbb{Z}[t])$ on the left and right on $G(\mathbb{Z}(t))$ considered as as pro-ind-schemes over $\mathbb{Z}$.  The derived category of this groupoid scheme is monoidal by the analogous diagram to that above.

The groupoidification of the $\mathbb{F}_q$ points was shown by Satake to be the representation ring
of ${^L G}$, the Langlands dual group.  Thus, $D_{mix}(G(\mathbb{Z}[t])\backslash G(\mathbb{Z}(t)/ G(\mathbb{Z}[t])$ also contains a categorification of the representation ring of ${^L G}$.  

In fact, Mirkovi&#263; and Vilonen showed that the subcategory of $D_{mix}(G(\mathbb{Z}[t])\backslash G(\mathbb{Z}(t))/ G(\mathbb{Z}[t])$ consisting of perverse sheaves is equivalent to the category of representations of ${^L G}\times_{\mathrm{Spec}\mathbb{Z}} \mathrm{Spec}\overline{\mathbb{Q}_\ell}$ as an algebraic group.  In fact, if one replaces $\mathbb{Q}_\ell$ by any other ring both in the coefficient of the sheaves, and the base of the algebraic group, the result still holds.

##The Hall algebra and Lusztig's categorification

If one takes the groupoid of representations of a Dynkin quiver with fixed dimension vector and basis $E_d$ (with each vector only having components over one dot), with the morphisms given by isomorphisms of representations (note, this is the action groupoid for a product of general linear groups $GL_d$ acting on a finite dimensional vector space), the resulting simplicial scheme is the fine moduli space of representations of that quiver.

There is a span of groupoids 
$$
\array{E_{d''}/GL_{d''} &&&&\\
&\nwarrow&&&\\
&& \mathrm{SES}(d,d',d'')&\to &E_d/GL_d\\
&\swarrow&&&\\
E_{d'}/GL_{d'} &&&&\\}
$$
where the span in the middle is the set of short exact sequences of representations with basis of dimension vector $d',d''$ mapping into and out of one of dimension vector $d$, preserving all bases, and the morphism are the obvious possible basis changes in this situation (this the action of groupoid for the parabolic in $GL_d$ preserving this filtration).

It was proved by Ringel that the $\mathbb{F}_q$ points of this variety groupoidify the upper half of the quantum group (of course, not in that language).  The natural resulting categorification was described by Lusztig and used to construct the canonical basis of $U_q(\mathfrak{g})$ where $ \mathfrak{g}$ is the simple Lie algebra associated to this quiver.

This categorification was described indpendently by Rouquier and Khovanov-Lauda combinatorially.
