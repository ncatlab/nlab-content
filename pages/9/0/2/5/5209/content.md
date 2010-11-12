##Idea##
A **temporal algebra** will be a [[modal algebra]] with two operation that reflect the future and past modal operators of a [[temporal logic]].

##Temporal algebras##
+--{: .un_defn}
######Definition######
A **temporal algebra** is a Boolean algebra, $(\mathbb{B}, m_0,m_1)$, with operators, of type 2,
with the condition that the operators are _conjugate_:

$m_0 x\cdot y=0$ if, and only if, $m_1 y\cdot x = 0$.

Equivalently (and equationally) this can be written as 

$x\leq l_0m_1x\cdot l_1m_0x$

where $l_i$ is the dual of $m_1$.
=--