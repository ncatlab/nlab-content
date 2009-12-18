Given an $A$-[[coring]] or even a more general additive [[comonad]] with a [[grouplike element]] there are several related (but in general nonequivalent) notions of connections.

As explained in [[grouplike element]], to an $A$-coring $C$ with a grouplike elements one associates a [[semi-free differential graded algebra]] $\Omega A = \Omega(A,C)$, sometimes called its (generalized) Amitsur complex. The simplest notion of a connection for the coring $C$ is a [[connection for a differential graded algebra|connection]] for the corresponding Amitsur complex. 

Let now $A$ be a $k$-algebra and $(C,\Delta,\epsilon)$ be an $A$-coring with grouplike element $g$ and $(\Omega A,d)$ its [[Amitsur complex]]. 

A __connection__ $\nabla:M\otimes_A\Omega^\bullet\to M\otimes_A\Omega^{\bullet+1}$ on a module $M$ over a [[semifree dga]] (in the sense of the entry [[connection for a differential graded algebra]]) is determined by its value $\nabla_M|_M$ on $M\cong M\otimes_A A$. If $\rho^M:M\to M\otimes_A C$ is a right $C$-[[coaction]] then the formula 

$$\nabla|_M:m\mapsto \rho^M(m)-m\otimes g$$ 

determines a [[flat connection]] on $M$. Conversely, any flat connection determines a right $C$-coaction by 

$$\rho^M(m)=\nabla(m)+m\otimes g.$$ 

This amounts to a *bijection between $C$-coactions and flat connections* on $M$. Regarding that coactions correspond to descent data in the context of comonadic descent, this gives the flat connection interpretation of such descent data. A first instance is probably Grothendieck's identification of flat connections and the first order costratifications in Grothendieck's theory of differential calculus on schemes (foundations of [[crystalline cohomology]], see book by Berthelot and Ogus; cf. also [[Grothendieck connection]]).


## Connections on comodules directly

One the other hand, one can consider more generally additive comonads, and define connections on comodules over them rather directly. Or dually one can work with connection on modules over [[additive monad]]s. 

Menini and &#350;tefan first define an intermediate notion of a quasi-connection for monads. Let $A$ be an [[additive category]] $(T,\mu,\eta)$ an additive monad in $A$ and $\nu:TM\to M$ an action on some object $M$ in $A$. 
Then a __quasi-connection__ on $M$ is a map $\nabla:M\to TM$ such that 

$$
\nabla \circ \nu - \mu\circ T(\nabla) = id_{TM} -  \eta\circ\nu: TM\to TM.
$$

A quasi-connection is a __connection__ if, in addition,

$$
\nu\circ\nabla = 0.
$$

For every connection in Menini--&#350;tefan sense, one defines its **curvature** $F_\nabla : M\to T^2 M$ by the formula

$$
F_\nabla := (id_{T^2 M} - \eta_{TM}\circ\mu_M)\circ T(\nabla)\circ\nabla.
$$

As usually, we define a **flat connection** as a connection whose curvature vanishes. 

In this setting one again has a bijection between flat connections and descent data. 

* P. Nuss, Noncommutative descent and non-abelian cohomology,  $K$-Theory  12  (1997),  no. 1, 23--74. 

* T. Brzezi&#324;ski, R. Wisbauer, Corings and comodules, London Math. Soc. Lec. Note Series 309, Cambridge 2003.

* C. Menini, Talk at MSRI: Connections, symmetry operators and descent data for triples, 1999, [link](http://www.msri.org/communications/ln/msri/1999/hopfalg/menini/1/index.html)

* C. Menini, D. &#350;tefan, Descent theory and Amitsur cohomology of triples, J. Algebra 266 (2003), no. 1, 261--304. 


[[!redirects connection for coring]]