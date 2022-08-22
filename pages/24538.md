
A __radical ring__ is a ring $R$ whose [[Jacobson ideal]] equals the ring, $J(R) = R$. 

Regarding that one characterization of the Jacobson ideal is that it is the intersection of all left annihilators of simple $R$-modules, that means that there are no simple modules.

For every ring $(R,+,\cdot,0,1)$ there is a Jacobson circle operation $\circle$ defined by
$$
a\circ b = a\cdot b + a + b
$$
Now, $(R,\circ,0)$ is a semigroup. Jacobson has proven that the circle semigroup is a group iff $(R,+,\cdot,0,1)$ is a radical ring. In that case one calls this group the adjoint group $R^\circ$ of the radical ring $R$. Every radical ring $R$ is a right $R^\circ$-module via $r^a = r\cdot a + r$ for $r\in R$, $a\in R^\circ$. Indeed, 
$$(r^a)^b = (r\cdot a + r)\cdot b + r\cdot a + r = r\cdot (a\cdot b + b + a)+r = r\cdot (a\circ b) + r$$

category: algebra