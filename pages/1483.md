##Motivation##

Given two [[topological space]]s $X,Y$ and a continuous map $f:X\to Y$, or equivalently the [[functor]] $f^{-1}:\mathrm{Open}(X)\to\mathrm{Open}(Y)$, forming the morphism of sites $\mathrm{Open}(Y)\to\mathrm{Open}(X)$ one can introduce two kinds of "morphisms" between [[sheaf|sheaves]] on $X$ and on $Y$: morphisms and comorphisms of sheaves over different base spaces. Depending on a motivation one or another is more natural. 

1. MORPHISMS. Recall that for a fixed base space, say $X$, the category of [[etale space]]s over $X$ is equivalent to the category of sheaves over $X$. Etale spaces make a subcategory of the slice category $\mathrm{Bun}_X=\mathrm{Top}/X$ of spaces ("bundles") over $X$. Denote by $p_F:E(F)\to X$ the etale map corresponding to a sheaf $F$. Thus for different bases we can simply define morphisms of sheaves $F\to G$ in etale space language, as continuous maps between the etale spaces $\xi: E(F)\to E(G)$ over $f$, i.e. $p_G\circ\xi=f\circ p_F$. These maps restrict to set theoretic maps on the level of [[stalk]]s. 

2. COMORPHISMS. The idea of comorphism is the idea of cospaces, rather than spaces; namely we like to replace a space, like in noncommutative geometry, by an object in a dually behaved category (say commutative rings; however it does not need to be strictly the dual category). For example, consider the ring of smooth functions on a manifold. A smooth morphism of manifolds $M\to N$ amounts to a set theoretic map ($f$ above) of underlying sets 
together with a compatible family of maps of algebras $k_V :C^\infty(V)\to C^\infty(f^{-1} V)$ where $V\subset N$ runs through all open subsets of $N$. Here of course $k_V : g\mapsto g\circ f|_{f^{-1}V}$. 

##Definition##

Let $F$ be a $R$-valued presheaf over a category $C$ and $G$ a $R$-valued presheaf over a category $D$. A __comorphism__ of $G$-valued presheaves $F\to G$ of $G$-valued  over a functor $f^{-1}:D\to C$ (thought of as a morphism of sites $f$ in opposite direction) is a morphism $k$ of $R$-valued presheaves over $C$: $k : G\to f_* F = F\circ f^{-1}$. Instead of saying that $k$ is a co(homo)morphism over $f$ (or $f$-comorphism), one often says that comorphism of presheaves is a pair $(f,k)$. If the presheaf is the structure sheaf of a [[ringed site]] one calls the comorphism, the morphism of ringed sites; the usual notation is then $(f,f^\sharp)$.  

In the case of a topological space, and sheaves of sets (or algebras of some kind), there is another description in terms of stalks, namely comorphisms be described as certain multi-valued maps between stalks. More precisely, given a continuous map $f:X\to Y$ and sheaves $F$ over $X$ and $G$ over $Y$, a comorphism $(f,f^\sharp)$ is a collection of maps $f^\sharp_x : G_{f(x)}\to F_{x}$ for all $x\in X$ such that for any section $s\in G(V)$ where $V^{\mathrm{open}}\subset Y$ the map $x\mapsto f^\sharp_x(s(f(x)))$ is a section of $F$ over $f^{-1}(V)$. We can view all $f^{\sharp}_x$ where $x\in f^{-1}(y)$ for a fixed $y$ as a single multi-valued map of stalks $G_y\to \coprod_{x\in f^{-1}(y)} F_x$ satisfying the continuity constraint mentioned. 

##Remarks##

1. Notice that by adjunction morphism $G\to f_* F$ of sheaves of sets over $Y$ corresponds to a unique morphism $f^* G\to F$ of sheaves of sets over $X$. However, in the case of ringed sites, morphism $G\to f_* F$ is required to be morphism of sheaves of rings, whereas the adjunction does *not* guarantee that the corresponding morphism $f^* G\to F$ of sheaves of sets over $X$ is a morphism of sheaves of rings over $X$. 

2. In the case of sheaves of sets, the $G$-component of the unit of adjunction $\eta_G :G\to f_* f^* G$ is clearly a comorphism $G\to f^* G$ over $f$. Given any comorphism $(f,k):G\to F$ (i.e. $k:G\to f_* F$) we can decompose it as
a composition 
$$
G\stackrel{\eta_G}\to f^* G\stackrel{k\circ\eta_G^{-1}}\to F 
$$
where the first map is a (canonical) comorphism over $f$ and the second map is a morphism of sheaves over $X$. Both maps may be viewed as multi-valued maps of etale spaces with the corresponding continuity conditions. In fact this is the unique decomposition of a given $f$-comorphism $k$ of sheaves of sets $G\to F$ into a compositon of $f$-comorphism of sheaves of sets $G\to f^*G$ and a morphism of sheaves of sets over $X$. There is also a unique decomposition of $k$ as
$
G\to f_* F\to F, 
$
where $G\to f_*F$ is a morphism and $f_* F\to F$ is a comorphism over $f$, namely
$$
G\stackrel{i^{-1}\circ k}\to f_* F\stackrel{i}\to F 
$$
where $i$ is the $f$-comorphism which is given by the identity $f_*F\to f_* F$. In fact, this can be seen as an intermediate step in the adjunction $f^*\dashv f_*$:
$$
\mathrm{Hom}_X(f^*G,F)\cong \mathrm{cohom}_f(G,F)\cong\mathrm{Hom}_Y(G,f_* F).
$$

 