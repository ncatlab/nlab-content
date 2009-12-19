
# Idea #

The notion of _Ehresmann connection_ describes a [[connection on a bundle|connection on]] a $G$-[[principal bundle]] $p : P \to X$ (for $G$ some [[Lie group]]) in terms of a [[Lie algebra]]-valued $1$-[[differential form|form]] $A \in \Omega^1(P,Lie(G))$ on $P$ that satisfies two conditions.

(Or rather, in the original formulation, it describes it equivalently in terms of the horizontal subbundle $H := ker A \subset T P$ of the [[tangent bundle]] of $P$ of vectors on which $A$ vanishes, see below.) 

This can be understood as the special case of [[schreiber:Differential Nonabelian Cohomology|nonabelian differential G-cocycle]] -- namely a cocycle with values in the [[groupoid of Lie-algebra valued forms]] $\bar \mathbf{B} G $ -- in [[Čech cohomology]] using the "canonical" [[Čech cover]] 

$$\cdots \to P \times_X P \simeq P \times G \stackrel{\to}{\to} P
$$ 

that comes from the total space surjection $p : P \to X$ of the [[bundle]] itself.

By the general mechanism of nonabelian [[Čech cohomology]] this means that a $\bar \mathbf{B}G$-valued cocycle with respect to this cover is

* a morphism $A : P \to \bar \mathbf{B}G$ : this is precisely given by the 1-form $A \in \Omega^1(P,Lie(G))$;

* a tranformation $g : p_1^*A \to p_2^*A$ that restricts to the $\mathbf{B}G$-cocycle of the underlying $G$-bundle.

Since $P \times_X P \simeq P \times G$ one may differentiate this transformation $g$ at the identity element of $G$. It is an exercise to check that this differential version of the &#268;ech cocycle condition yields the following two conditions on $A$

1. **first Ehresmann condition** -- restricted to the fibers, i.e. pulled back along $\array{G &\stackrel{i_x}{\to}& P \\ \downarrow && \downarrow \\ {*} &\stackrel{x}{\to}& X}$ it becomes the canonical left-invariant $Lie(G)$-valued 1-form $\theta \in \Omega^1(G,Lie(G))$ on $G$

  $$
    i_x^* A = \theta
  $$

2. **second Ehresmann condition** -- The form $A$ is _equivariant_ with respect to the $G$-[[action]] on $P$ in some sense. 

The crucial implication of the second property is that all [[characteristic form]]s of $A$ in $\Omega^\bullet(P)$ are pullbacks of forms on $X$: for $I$ any degree $k$ [[invariant polynomial]] on $Lie(G)$ and for $F_A \in \Omega^2(P,Lie(G))$ the curvature 2-form, we have

$$
  \exists c_I \in  \Omega^{2k}(X) : 
  I(F_A) = p^* c_I
  \,.
$$

# Note on terminology #

The terminology for the various incarnations of the single notion of [[connection on a bundle]] varies throughout the literature. What we here call an Ehresmann connection is sometimes, but not always, called **principal connection** (as it is defined for [[principal bundle]]s).



# References #


The original definition is due to

* [[Charles Ehresmann]], _Les connexions infinit&#233;simale dans une espace fibr&#233; diff&#233;rentiable_, Colloque
de Toplogie, Bruxelles (1950) 29-55.
[[!redirects Ehresmann-connection]]

A fair idea of what exactly that original article defined can be gained from its [MathScinet review](http://www.ams.org/mathscinet-getitem?mr=0042768)


A useful statement of the defintion in terms of a 1-form on the total space is for instance on [p. 13](http://arxiv.org/PS_cache/gr-qc/pdf/0611/0611154v2.pdf#page13) of

* Derek Wise, _MacDowell-Mansouri gravity and Cartan geometry_ ([arXiv](http://arxiv.org/abs/gr-qc/0611154))

A formulation and discussion of Ehresmann connections using language and tools from [[synthetic differential geometry]] is in section 6 of

* Moerdijk-Reyes, [[Models for Smooth Infinitesimal Analysis]]
