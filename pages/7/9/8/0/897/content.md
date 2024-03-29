#Idea#

In a category with [[interval object]] one has for every object $X$ a notion of paths in $X$. (Indeed, the very definition of category with interval object is meant to guarantee that for every object there is its [[fundamental category]] in the [[Trimble n-category|Trimblean sense]]).

The idea is that if for all these paths in $X$ there is a _reverse_ path, then the object $X$ is _undirected_ or _groupoidal_. Otherwise it is _strictly directed_ (not to be confused with a [[directed object]]). 

#Definition (tentative)#

Let $V$ be a [[category]] with an [[interval object]] $I$. Recall that there is for every object $X$ of $V$ a canonical morphism $X_0 \to [I,X]$ which embeds the points of $X$, $X_0 := [pt,X]$, as the constant paths into the "object of directed paths" $[I,X]$.

An object $X$ in $V$ is called **undirected** or an **undirected object** with respect to $I$, &#8211; or **$I$-undirected** &#8211; if this morphism is a weak equivalence:
$$
  (X is undirected) \Leftrightarrow
  ([\pt,X] \stackrel{\simeq}{\to} [I,X])
  \,;
$$
otherwise it is called **strictly directed** or a **strictly directed object** with respect to $I$, or **strictly $I$-directed**.

#Examples#

* $V = $  [[Top]] with its standard [[model category]] structure, and $I = [0,1]$ the standard interval. Then all objects are undirected since the interval is contractible.

* $V = \omega Cat$, [[strict omega-category|strict omega-categories]], equipped with the [[folk model structure]] and $I = \{a \to b\}$ the 1-[[globe]], the first [[oriental]]. Then
  * strict $\omega$-[[omega-groupoid]]s are undirected;
  * in particular the interval $I$ itself is strictly directed, as there is no weak equivalence from $I_0 = I$ to $[I,I] = \{a \to b \to c\}$; 
  * in general, the undirected objects should be precisely those for which every $j$-morphism is an $\omega$-[[equivalence]].  These should consist of those $\infty$-[[infinity-groupoid]]s that are strict as $\infty$-categories, or those objects that are weakly equivalent to a strict $\omega$-groupoid.  For this purpose it is essential that the internal-hom for the [[Crans-Gray tensor product]] on strict $\omega$-categories contains _lax_ transformations, modifications, and so on; if it only contained _pseudo_ natural transformations, then the undirected objects would just be those for which every 1-morphism is an equivalence.

* Once we have a closed monoidal homotopical structure on the category $dTop$ of [[directed space|directed topological spaces]], it should be true that in $V = dTop$ with $I = I_d$ the standard directed interval, an object $(X, d X)$ is undirected precisely if it contains no nontrivial directed path.

#Remarks#

Whether or not an object is undirected depends on the choice of interval object. 

* For instance the terminal object $pt$ itself is always a an interval object, $I = pt$, but in a trivial way. Every object is $pt$-undirected. 

* A bit more generally, the interval object may be not equal to the terminal object, but still be _weakly equivalent_ to it.  For instance the standard (undirected) topological  interval $[0,1]$ is not equal to but is weakly equivalent to the point in the standard  [[model structure on topological spaces]]. This implies in particular that with  respect to the standard undirected topological interval even a [[directed space|directed topological space]] should undirected. (Well, we still need to specify the closed structure on $dTop$ to make this true...) It's only the standard _directed_ topological interval which can detect the directedness of a strictly directed topological space.

* Analogous statements are true in the example of [[strict  omega-category|strict omega-categories]], where the analogue of the standard directed topological interval is the 1-[[globe]] $I_{dir} = \{a \to b\}$, while the example of the standard undirected topological interval is the [[groupoid]] version of this, $I_{inv} = \{a \stackrel{\simeq}{\to} b\}$, where the morphism from $a$ to $b$ is an [[isomorphism]]. As opposed to $I_{dir}$ this $I_{inv}$ is weakly equivalent to the terminal category $pt = \{\bullet\}$ (the 0-[[globe]]) (with respect to the [[folk model structure]]). It should be true that every strict $\omega$-category is $I_{inv}$-undirected, even if it is strictly $I_{dir}$-directed.
