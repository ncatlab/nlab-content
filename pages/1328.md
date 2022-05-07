#Idea#

[[simplicial presheaf|Simplicial presheaves]] equipped with the [[model structure on simplicial presheaves]] are one model/presentation for the [[(∞,1)-category of (∞,1)-sheaves]] on a given [[site]].

The fibrant object $\bar X$ that a [[simplicial presheaf]] $X : S^{op} \to SSet$ is weakly equivalent to with respect to this model structure is the [[∞-stackification]] of $X$. One expects that [[∞-stacks]]/[[(∞,1)-sheaves]] are precisely those [[(∞,1)-presheaves]] which satisfy a kind of [[descent]] condition.

Precsisely what this condition is like for the particular model constituted by simplicial presheaves with the given Jardine [[model structure on simplicial presheaves]] was worked out in 

* Daniel Dugger, Sharon Hollander, Daniel C. Isaksen, _Hypercovers and simplicial presheaves_ ([web](http://www.math.uiuc.edu/K-theory/0563/)) 

and

* Toën-Vezzosi, _Segal topoi and stacks over Segal categories_ ([pdf](http://poincare.dma.unifi.it/~vezzosi/papers/msri.pdf))

recalled as corollary 6.5.3.13 in 

* [[Jacob Lurie]], [[Higher Topos Theory]].

The following is a summary of these results.

The main point is that the fibrant objects are essentially those simplicial presheaves, which satisfy [[descent]] with respect not just to [[covers]], but to [[hypercovers]].

Localizations of [[(∞,1)-presheaves]] at [[hypercovers]] are called [[hypercompletions]] in [section 6.5.3](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=534) of [[Higher Topos Theory]]. Notice that in [section 6.5.4](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=539) of [[Higher Topos Theory]] it is argued that it may be more natural _not_ to localize at [[hypercovers]], but just at [[covers]] after all.

#Details#

A well-studied class of models/presentations for an [[(∞,1)-category of (∞,1)-sheaves]] is obtained using the [[model structure on simplicial presheaves]] on an  ordinary (1-categorical) [[site]] $S$, as follows.

Let $[S^{op}, SSet]$ be the [[SimpSet|SSet]]-[[enriched category]] of [[simplicial presheaf|simplicial presheaves]] on $S$. 

Recall from [[model structure on simplicial presheaves]] that there is the _global_ and the _local_ injective simplicial model structure on $[S^{op}, SSet]$, and that the local model structure is a (Bousfield-)localization of the global model structure.

According to [section 6.5.2](http://www.math.harvard.edu/~lurie/papers/highertopoi.pdf#page=528)  of [[Higher Topos Theory|HTT]] we have:

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _global_ injective model structure is (the [[SimpSet|SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $PSh_{(\infty,1)}(S)$ of [[(∞,1)-presheaves]] on $S$.

* the full simplicial subcategory on fibrant-cofibrant objects of $[S^{op}, SSet]$ with respect to the _local_ injective model structure is (the [[SimpSet|SSet]]-[[enriched category]] realization of) the $(\infty,1)$-category  $\bar{Sh}_{(\infty,1)}(S)$ which is the [[hypercompletion]] of the $(\infty,1)$-category $Sh_{(\infty,1)}(S)$ of [[(∞,1)-sheaves]] on $S$.

Since with respect to the local or global injective model structure all objects are automatically cofibrant, this means that $\bar Sh_{(\infty,1)}(S)$ is the full sub-$(\infty,1)$-category of $PSh_{(\infty,1)}(S)$ on simplicial presheaves which are fibrant with respect to the local injective model structure: these are the [[∞-stacks]] in this model.

By the general properties of [[localization of an (∞,1)-category]] there should be a class of morphisms $f : Y \to X$ in $PSh_{(\infty,1)}(S)$ -- hence between injective-fibrant objects in $[S^{op}, PSh(S)]$ -- such that the simplicial presheaves representing $\infty$-stacks are precisely the [[local objects]] with respect to these morphisms.

This was worked out in 

* D. Dugger, S. Hollander, D. Isaksen, _Hypercovers and simplicial presheaves_ ([pdf](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf))

We now describe central results of that article.
 
+-- {: .un_defn}
###### Definition

For $X \in S$ an object in the [[site]] regarded as a simplicial presheaf and $Y \in [S^{op}, SSet]$ a simplicial presheaf on $S$, a morphism $Y \to X$ is a **[[hypercover]]** if it is a _local acyclic fibration_, i.e. of for all $V \in S$ and all diagrams
$$
  \array{
    \Lambda^k[n]\otimes V &\to & Y
    \\
    \downarrow && \downarrow
    \\
    \Delta^n\otimes V &\to& 
    X
  }
  \;\; respectively \;\,
  \array{
    \partial \Delta^n\otimes V &\to & Y
    \\
    \downarrow && \downarrow
    \\
    \Delta^n\otimes V &\to& 
    X
  }
$$
there exists a covering  [[sieve]] $\{U_i \to V\}$ of $V$ with respect to the given [[Grothendieck topology]] on $S$ such that for every $U_i \to V$ in that [[sieve]] the pullback of the abve diagram to $U$ has a lift
$$
  \array{
    \Lambda^k[n]\otimes U_i &\to & Y
    \\
    \downarrow &\nearrow & \downarrow
    \\
    \Delta^n\otimes U_i &\to& 
    X
  }
  \;\; respectively \;\,
  \array{
    \partial \Delta^n\otimes U_i &\to & Y
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta^n\otimes U_i &\to& 
    X
  } 
  \,.
$$
=--

If $S$ is a [[Verdier site]] then every such hypercover $Y \to X$ has a refinement by a hypercover which is cofibrant with respect to the projective global [[model structure on simplicial presheaves]]. We shall from now on make the assumption that the hypercovers $Y \to X$ we discuss are cofibrant in this sense. These are called _split hypercovers_. (This works in many cases that arise in practice, see the discussion after [DHI, def. 9.1](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=29).)

+-- {: .un_prop}
###### Proposition

The objects of $Sh_{(\infty,1)}(S)$ -- i.e. the fibrant objects with respect to the projective model structure on $[S^{op}, SSet]$ -- are precisely those objects $A$ of $PSh_{(\infty,1)}(S)$ -- i.e. [[Kan complex]]-valued simplicial presheaves -- which
**satisfy descent for all split hypercovers**, i.e. those for which for all split hypercover $f : Y \to X$ in $[S^{op}, SSet]$ we have that
$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](Y,A)
$$
is a [[model structure on simplicial sets|weak equivalence of simplicial sets]].
=--

+-- {: .proof}
###### Proof

This is [DHI, thm 1.3](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=3) formulated in the light of [DHI, lemma 4.4 ii)](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf#page=9).
=--

Notice that by the [[co-Yoneda lemma]] every simplicial presheaf $F : S^{op} \to SSet$, which we may regard as a presheaf $F : \Delta^{op}\times S^{op} \to Set$, is isomorphic to the [[weighted limit|weighted colimit]] 
$$
    F \simeq colim^\Delta F_\bullet
$$
which is equivalently the [[end|coend]]
$$
  F \simeq \int^{[n] \in \Delta} \Delta^n \cdot F_n
  \,,
$$ 
where $F_n$ is the Set-valued presheaf of $n$-cells of $F$ regarded as an $SSet$-valued presheaf under the inclusion $Set \hookrightarrow SSet$, and
where the [[SimpSet|SSet]]-weight is the canonical cosimplicial simplicial set $\Delta$, i.e. for all $X \in S$
$$
  F : X \mapsto \int^{[n] \in \Delta} \Delta^n \times F(X)_n
  \,.
$$
In particular therefore for $A$ a [[Kan complex]]-valued presheaf the descent condition reads
$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](colim^\Delta Y_\bullet,A)
  \simeq
  lim^\Delta [S^{op}, SSet](Y_\bullet,A)
  \,.
$$

With the shorthand notation introduced above the **descent condition** finally reads, for all global-injective fibrant simplicial presheaves $A$ and hypercovers $U \to X$:
$$
  A(X) \stackrel{\simeq}{\to} lim^\Delta A(Y_\bullet)
  \,.
$$
The right hand here is often denoted $Desc(Y_\bullet \to X, A)$, in which case this reads
$$
  A(X) \stackrel{\simeq}{\to} Desc(Y_\bullet \to X, A)
  \,.
$$












## formulation in terms of homotopy limit ##

(expanded version of remark 2.1 in [DHI](http://hopf.math.purdue.edu//Dugger-Hollander-Isaksen/hypspre.pdf))


Using the [[Bousfield-Kan map]] every simplicial presheaf $F$ is also weakly equivalent to the weighted limit over $F_\bullet$ with weight given by $N(\Delta/(-)) : \Delta \to SSet$.

$$
  lim^{N(\Delta/(-))} F_\bullet \stackrel{\simeq}{\to}
  lim^\Delta F_\bullet
  \,.
$$

But by the discussion at [[weighted limit]], the left hand computes the [[homotopy limit]] of $F_\bullet$ (since $F_\bullet$ is objectwise fibrant, since $F_n$ factors through $Set \hookrightarrow SSet$), hence we have a weak equivalence

$$
  holim F_\bullet \stackrel{\simeq}{\to}
  F
  \,.
$$

Often the descent condition is therefore formulated with the cover $U$ replaced by its homotopy limit, whence it reads

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  [S^{op}, SSet](hocolim U_\bullet,A)
  \,.
$$

With $A$ global-injective fibrant this is equivalent to

$$
  [S^{op}, SSet](X,A) \stackrel{\simeq}{\to}
  holim [S^{op}, SSet](U_\bullet,A)
  \,.
$$

Using the notation introduced above this becomes finally

$$
  A(X) \stackrel{\simeq}{\to} holim A(U_\bullet)
  \,.
$$

[[!redirects homotopy descent]]