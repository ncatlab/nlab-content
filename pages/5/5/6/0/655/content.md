#Idea#

A [[simplicial group]] whose [[Moore complex]] has length $1$ (that is, at most stuff in dimensions $0$ and $1$) will be the internal [[nerve]] of a strict $2$-[[2-group|group]] and the Moore complex will be the corresponding [[crossed module]].  What if we have a simplicial group whose Moore complex has at most stuff in dimensions $0$, $1$, and $2$; can we describe its structure in some similar way?  Yes, and Conduch&#233; provided a neat description of the structure involved.  From the structure one can rebuild a simplicial group, a type of internal $2$-[[2-nerve|nerve]] construction.

In other words, a $2$-crossed module _is_ the Moore complex of a $2$-truncated simplicial group.

#Definition#

A __$2$-crossed module__ is a normal complex of groups
$$L\stackrel{\partial_2}{\to} M \stackrel{\partial_1}{\to}N,$$ 
together with an [[action]] of $N$ on all three groups and a mapping 
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

The pairing $\{ - ,- \} : M\times M \to L$ is often called the **Peiffer lifting**  of the $2$-crossed module.

#Remarks#

*  In a $2$-crossed module as above the structure $\partial_2: L \to M$ is a [[crossed module]], but $\partial_1: M\to N$ may not be one, as the Peiffer identity need not hold.  The _[[Peiffer commutator]]_, which measures the failure of that identity, may not be trivial, but it will be a boundary element and the Peiffer lifting gives a structured way of getting an element in $L$ that maps down to it.

*  It is sometimes useful to consider a [[crossed module]] as being a [[crossed complex]] of length 1 (i.e. on possibly non-trivial morphism only).  Likewise one can consider a 2-crossed module as a special case of a [[2-crossed complex]]. Such a gadget is intuitively a 2-crossed module with a 'tail', which is a chain complex of modules over the $\pi_0$ of the base 2-crossed module, much as a crossed complex is a crossed module together with a 'tail'. The homotopy theory of these is little developed as yet, but, in part, is related to the theory of [[quadratic module]]s and [[quadratic complex]]es as introduced by Baues.

#Examples#

*  Any [[crossed module]],
  $
    G_2 \stackrel{\delta }{\to}{G_1}
  $ gives a 2-crossed module, $L\stackrel{\partial_2}{\to} M \stackrel{\partial_1}{\to}N,$ by setting $L = 1$, the trivial group, and, of course, $M = G_2$, $N = G_1$. Conversely any 2-crossed module having  trivial top dimensional group ($L=1$) 'is' a crossed module. This gives an inclusion of the category of crossed modules into that of 2-crossed modules, as a [[reflective subcategory]]. 

   The reflection is given by noting that, if 

$$L\stackrel{\partial_2}{\longrightarrow} M \stackrel{\partial_1}{\longrightarrow}N$$ 

   is a 2-crossed module, then $Im\, \partial_2$ is a normal subgroup of $M$, and then there is an obvious induced crossed module structure on 

$$\partial_1 : \frac{M}{Im\, \partial_2} \to N.$$



*  More generally, let 

$$\ldots \to 1 \to 1 \to C_3\stackrel{\partial_3}{\longrightarrow} C_2 \stackrel{\partial_2}{\longrightarrow}C_1,$$

   be a [[crossed complex]] (of groups) in which all higher dimensional terms are trivial, then taking $L = C_3$, $M = C_2$ and $N = C_1$, with trivial Peiffer lifting, gives one a 2-crossed complex.