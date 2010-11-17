
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

##Idea#

A _2-crossed module_ encodes a semistrict 3-group -- a [[Gray group]] -- in generalization of how a [[crossed module]] encodes a [[strict 2-group]].

A [[simplicial group]] whose [[Moore complex]] has length $1$ (that is, at most stuff in dimensions $0$ and $1$) will be the internal [[nerve]] of a strict $2$-[[2-group|group]] and the Moore complex will be the corresponding [[crossed module]].  What if we have a simplicial group whose Moore complex has at most stuff in dimensions $0$, $1$, and $2$; can we describe its structure in some similar way?  Yes, and Conduch&#233; provided a neat description of the structure involved.  From the structure one can rebuild a simplicial group, a type of internal $2$-[[nerve]] construction.

In other words, a $2$-crossed module _is_ the Moore complex of a $2$-[[truncated]] simplicial group.

## Definition

A __$2$-crossed module__ is a [[normal complex of groups]]
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

## Remarks

*  In a $2$-crossed module as above the structure $\partial_2: L \to M$ is a [[crossed module]], but $\partial_1: M\to N$ may not be one, as the Peiffer identity need not hold.  The _[[Peiffer commutator]]_, which measures the failure of that identity, may not be trivial, but it will be a boundary element and the Peiffer lifting gives a structured way of getting an element in $L$ that maps down to it.

*  It is sometimes useful to consider a [[crossed module]] as being a [[crossed complex]] of length 1 (i.e. on possibly non-trivial morphism only).  Likewise one can consider a 2-crossed module as a special case of a [[2-crossed complex]]. Such a gadget is intuitively a 2-crossed module with a 'tail', which is a chain complex of modules over the $\pi_0$ of the base 2-crossed module, much as a crossed complex is a crossed module together with a 'tail'. The homotopy theory of these is little developed as yet, but, in part, is related to the theory of [[quadratic module]]s and [[quadratic complex]]es as introduced by Baues.

## Examples

Any [[crossed module]],
$
  G_2 \stackrel{\delta }{\to}{G_1}
$ gives a 2-crossed module, $L\stackrel{\partial_2}{\to} M \stackrel{\partial_1}{\to}N,$ by setting $L = 1$, the trivial group, and, of course, $M = G_2$, $N = G_1$. Conversely any 2-crossed module having  trivial top dimensional group ($L=1$) 'is' a crossed module. This gives an inclusion of the category of crossed modules into that of 2-crossed modules, as a [[reflective subcategory]]. 

The reflection is given by noting that, if 
$$L\stackrel{\partial_2}{\longrightarrow} M \stackrel{\partial_1}{\longrightarrow}N$$ 
is a 2-crossed module, then $Im\, \partial_2$ is a normal subgroup of $M$, and then there is an obvious induced crossed module structure on 
$$\partial_1 : \frac{M}{Im\, \partial_2} \to N.$$


But we can do better than this.  More generally, let 
$$\ldots \to 1 \to 1 \to C_3\stackrel{\partial_3}{\longrightarrow} C_2 \stackrel{\partial_2}{\longrightarrow}C_1,$$
be a truncated [[crossed complex]] (of groups) in which all higher dimensional terms are trivial, then taking $L = C_3$, $M = C_2$ and $N = C_1$, with trivial Peiffer lifting, gives one a 2-crossed complex. Conversely suppose we have a 2-crossed module with trivial Peiffer lifting: $\{m_1,m_2\} = 1$ for all $m_1$, $m_2 \in M$, axiom 3 then shows that $L$ is an Abelian group, and similarly the other axioms can be analysed to show that the result is a truncated crossed complex.

This gives:

+-- {: .un_prop}
###### Proposition

The category $Crs_{2]}$ of crossed complexes of length 2 is equivalent to the full subcategory of $2-CMod$ given by those 2-crossed modules with trivial Peiffer lifting.
=--

Of course, the resulting 'inclusion' has a left adjoint, which is quite fun to check out! (You kill off the subgroup of $L$ generated by the Peiffer lifting, .... is that all?)


### From simplicial groups to 2-crossed modules

If $G$ is a simplicial group then 

$$\frac{\mathcal{N}G_2}{d_0(\mathcal{N}G_3)} \to \mathcal{N}G_1\to \mathcal{N}G_0,$$

is a 2-crossed module. (You are invited to find the Peiffer lifting!)

### From crossed squares to 2-crossed modules

Both [[crossed square|crossed squares]] and 2-crossed modules model all connected homotopy 3-types so one naturally asks how to pass from one description to the other.  Going from crossed squares to 2-crossed modules is easy, so will be given here (going back is harder).

Let 
$$\array{& L & {\to}^\lambda & M & \\
         \lambda^\prime & \downarrow &&\downarrow & \mu\\
          &N & {\to}_{\nu}& P & \\
}$$
be a crossed square then $N$ acts on $M$ via $P$, so ${}^n m := {}^{\nu(n)}m$, and so we can form $M\rtimes N$ and the sequence
$$L\stackrel{((\lambda')^{-1},\lambda)}{\longrightarrow}M\rtimes N\stackrel{\mu\nu}{\longrightarrow}P$$ 
is then a 2-crossed complex.

(And, yes, these are actually group homomorphisms: $(\mu,\nu)(m,n) = \mu(m)\nu(n)$, the product of the two elements! Try it!)

The full result and an explanation of what is going on here is given in

* D. Conduch&#233;, _Simplicial Crossed Modules and Mapping Cones_, Georgian Math. J., 10, (2003), 
623--636

## Related concepts

* [[crossed module]], [[differential crossed module]]

* **2-crossed module** / [[crossed square]], [[differential 2-crossed module]]

* [[crossed complex]]

* [[hypercrossed complex]]




[[!redirects 2-crossed modules]]