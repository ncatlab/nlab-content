Given a category $C$ and an object $I\in Ob(C)$, the __category of points over $I$__ is the category $Pt_I(C)$ of [[pointed objects]] of the [[slice category]] $C/I$; or alternatively the [[under category|coslice]]-slice category

$$
Pt_I(C) = (I,id_I)\backslash(C/I)
$$

This can be unpacked the following way:

* An object of $Pt_I(C)$ is a pair $(p:X\leftrightarrow I:s)$ of morphisms of $C$ such that $s$ is a [[section]] of $p$; in other words it is a [[split epimorphism]] $p$ to $I$ with a fixed choice of splitting $s$.

* A morphism $f:(q:Y\leftrightarrow I:t)\to(p:X\leftrightarrow I:s)$ is any morphism $f:Y\to X$ such that $p\circ f= q$ and $f\circ t=s$. 

By the construction, the category $Pt_I(C)$ of points over $I$ is [[pointed category|pointed]] and [[finitely complete category|finitely complete]]; moreover the __[[inverse image]] functor__ $v^*:Pt_I(C)\to Pt_J(C)$ induced by $v:J\to I$ is a [[left exact functor]].

The __category $Pt(C)$ of points of $C$__ has objects $Ob(Pt(C))=\coprod_I Ob(Pt_I(C))$. In other words, the objects are the split epimorphisms $p:X\to I$ of $C$ with a choice of a splitting, or equivalently the [[retracts]] in $C$. At the level of morphisms it is just a bit more complex than the morphisms in each $Pt_I(C)$, namely the slice and coslice triangles become squares. More precisely, a morphism $(u,v): (q:Y\leftrightarrow J:t)\to (p:X\leftrightarrow I:s)$ is a pair of morphisms $u:Y\to X$, $v:J\to I$ in $C$ such that $u\circ t = s\circ v$ and $v\circ q =p\circ u$.

$$\array{
Y &\stackrel{u}\to & X \\
q\downarrow\uparrow t & & p\downarrow\uparrow s\\
J&\stackrel{v}\to & I
}$$
 
The __fibration of points__ is the codomain-assigning functor $\pi:Pt(C)\to C$, $\pi:(p:X\leftrightarrow I:s)\to I$, $(u,v)\mapsto u$. It is a [[fibered category]] in the sense of Grothendieck. Its fibers are $Pt_I(C)$ which are (as mentioned above) pointed and finitely complete. 
A morphism $(u,v)$ (in notation as above) is [[cartesian morphism|cartesian]]] iff $q,u,p,v$ are the sides of a [[pullback square]] in $C$ (i.e. $q$ is a pullback of $p$ along $v$ and $u$ a pullback of $v$ along $p$). The inverse image functor for this fibration is exactly described by the rule $v\mapsto v^*$ above. 


#References#

* [[Borceux-Bourn]]


[[!redirects category of points]]