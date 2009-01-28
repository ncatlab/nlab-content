##Idea##
A simplicial group whose [[Moore complex]] has length one (that is, at most stuff in dimensions 0 and 1) will be the internal nerve of a [[2-group]] and the Moore complex will be the correspondiong crossed module.  What if we have a simplicial group whose Moore complex has at most stuff in 
dimensions 0,1, and 2, can we describe its structure in some similar way? Yes, and Conduch&#233; provided a neat description of the structure involved. From the structure one can rebuild a simplicial group, a type of internal 2-nerve construction.

In other words, a 2-crossed module _is_ the Moore complex of a 2-truncated simplicial group.


##Definition##

A _2-crossed module_ is a normal complex   of  groups

$$L\stackrel{\partial_2}{\to} M \stackrel{\partial_1}{\to}N,$$ 

together with an action of $N$ on all three groups and a   mapping 

$$\{ - ,- \} : M\times M \to L$$

such that 

1.  the action of $N$ on itself is by conjugation, and $\partial_2$ and $\partial_1$ are $N$-equivariant;

1.  for all $m_0,m_1 \in M$,

    $$\partial_2\{m_0,m_1\} = \,^{\partial_1 m_0}m_1 . m_0m_1^{-1}m_0^{-1};$$
1.  if $\ell_0,\ell_0 \in L$, then
    $$\{\partial_2\ell_0,\partial_2\ell\} = [\ell_1,\ell_0];$$

1.  if $\ell \in L$ and $m\in M$, then

    $$\{m,\partial \ell\}\{\partial \ell,m\} = \,^{\partial m}\ell.\ell^{-1};$$
1.  for all $m_0,m_1,m_2 \in M$,
    
    * $\{m_0,m_1m_2\} = \{m_0,m_1\}\{ \partial \{m_0,m_2\},(m_0m_1m_0^{-1})\}\{m_0,m_2\}$;

    * $\{m_0m_1,m_2\} = \,^{\partial m_0}\{m_1,m_2\}\{m_0,m_1m_2m_1^{-1}\}$;

1. if $n\in N$ and $m_0,m_1 \in M$, then 

    $$ \,^{n} \{m_0,m_1\} = \{ \,^{n}m_0, \,^{n}m_1\}.$$


The pairing $\{ - ,- \} : M\times M \to L$ is often called the _Peiffer lifting_  of the 2-crossed module.

##Discussion##

*  In a 2-crossed module as above the structure $\partial_2: L \to M$ is a [[crossed module]], but that $\partial_1 : M\to N$ is not as the Peiffer identity does not hold.  The _Peiffer commutator_, which measures the failure of that identity, may not be trivial, but it will be an boundary element and the Peiffer lifting gives a structured way of getting an element in $L$ that maps down to it. 