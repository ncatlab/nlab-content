
#Contents#
* automatic table of contents goes here
{:toc}


## Definition 

The **d&#233;calage** $Dec\, Y$ of a [[simplicial set]] $Y$, is the simplicial set obtained by shifting every dimension down by one, 'forgetting' the last face and degeneracy  of $Y$ in each dimension:

* $(Dec \, Y)_n = Y_{n+1}$;
* $d_k^{n,Dec \,Y}  = d^{n+1,Y}_{k}$;
* $s_k^{n,Dec \,Y}  = s^{n+1,Y}_{k}$.


This simplicial set comes with a natural projection, $d_{last} : Dec\, Y \to Y$, given by the 'left over' face map.     Moreover this map gives a [[homotopy equivalence]]

$$Dec\,Y \simeq const(Y_0),$$

between $Dec\, Y$ and the constant simplicial set on $Y_0$. 

The same construction works in other contexts, as is easily seen. The case of $Dec G$ for $G$ a [[simplicial group]] is important in the simplicial theory of algebraic models for [[homotopy n-type]]s.

The map $d_{last} : Dec\, Y \to Y$, is a [[Kan fibration]], and in particular, in the simplicial group case, $d_{last} : Dec\, G \to G$, is an epimorphism.  Taking the kernel of this and then applying $\pi_0$, yields a [[crossed module]] constructed from the [[Moore complex]] of $G$

$$NG_1/d_2(NG_2)\to NG_0,$$

which has kernel $\pi_1(G)$ and cokernel $\pi_0(G)$.

+-- {: .query}

[[Urs Schreiber]]: It should be possible to write $Dec Y$ as the [[pullback]] $Q$ 

$$
  \array{
    Q &\to& const(Y_0)
    \\
    \downarrow && \downarrow
    \\
    Y^{\Delta[1]} &\stackrel{d_1}{\to}& Y
  }
$$

in [[sSet]]. Shouldn't it? 

Let me check this. First I check that this pullback has the property that $Q_n = Y_{n+1}$.

For this I use expression of the $(n+1)$-simplex as the cone over the $n$-simplex, which is exhibted by the pushout diagram

$$
  \array{
    \Delta[n] \times \{1\} &\to& \Delta[n] \times \Delta[1]
    \\
    \downarrow && \downarrow
    \\
    \Delta[0] &\to& \Delta[n+1]
  }
  \,.
$$

This identifies the nondegenerate $(n+1)$-cell of $\Delta[n+1]$ as the map 

$$
  (0,0,1,2, \cdots,n-1,n), (0,1,1, \cdots,1,1) : [n+1] \to [n] \times [1]
  \,.
$$

(See for instance page 25 [here](http://arxiv.org/PS_cache/arxiv/pdf/0809/0809.4221v1.pdf#page=25)).

Applying $Hom_{\Delta}(-,Y)$ to this pushout diagram yields the pullback diagram

$$
  \array{
    Y_{n+1} &\to& Y_0
    \\
    \downarrow && \downarrow
    \\
    (Y^{\Delta[1]})_n &\to& Y
  }
$$

in [[Set]]. Since pushouts of simplicial sets are computed degreewise in sets we have that $Q_n = Y_{n+1}$ for all $n$. 

Now check that the face and degeneracy maps act as given by the formula for the decalage. Under the above identification with $\Delta[n+1]$ by a pushout, the face map $\delta_i :\Delta[n+1] \to \Delta[n+2]$ is that induced by the morphism of pushout diagrams

$$
  \array{
     \Delta[n] \times \Delta[1] &\stackrel{(\delta_i,Id_{\Delta[1])}}{\to}&
      \Delta[n+1] \times \Delta[1]
     \\
     \uparrow && \uparrow
     \\
     \Delta[n] \times \{1\} &\stackrel{(\delta_i,Id_{\Delta[0])}}{\to}& 
      \Delta[n+1] \times \{1\}
     \\
     \downarrow && \downarrow
     \\
     \Delta[0] &\to& \Delta[0]
  }
  \,.
$$

The induced morphism on the pushouts takes the nondegenerate cell $(0,0,1,2, \cdot,n-1,n), (0,1,1, \cdots, 1,1) : [n+1] \to [n] \times [1]$ of $\Delta[n+1]$ to the cell

$$
  \delta_i(0,0,1,2, \cdot,n-1,n), (0,1,1, \cdots, 1,1) : [n] \to [n+1] \times [1].
$$

That produces all the faces except that of the form $(0,1,2, \cdots, n-1,n),(0,0, \cdots, 0,0) : [n] \to [n+1] \times [1]$, hence except for the 0-face. So this is indeed as in the decalage.

An entirely analogous argument applies for the degeneracy maps.

Finally, check that if $Y$ is a Kan complex, we have a Kan fibration $Q \to Y$ induced from the other inclusion $\Delta[n] \times \{0\} \to \Delta[n] \times \Delta[1]$ not used above. This is then the vertical morphism in the diagram

$$
  \array{
    Q &\to& const(Y_0)
    \\
    \downarrow && \downarrow
    \\
    Y^{\Delta[1]} &\stackrel{d_1}{\to}& Y
    \\
    {}^{\mathllap{d_0}}\downarrow
    \\
    Y
  }
$$

This is recognized as the construction appearing in the factorization lemma in the [[category of fibrant objects]] of Kan complexes (described also at [[homotopy pullback]] and [[generalized universal bundle]]), hence is a [[Kan fibration]], as described there.


=--
 

## Decalage comonad 

Decalage also has an abstract nonsense description as follows. The simplicial category, as a monoidal category $(\Delta, +, 0)$ equipped with the monoid $1$, is the "walking monoid", i.e., is initial among monoidal categories equipped with a monoid. Therefore $\Delta^{op}$ is the walking comonoid; as a result, there is a comonad 

$$- + 1: \Delta^{op} \to \Delta^{op}$$ 

which induces a comonad on simplicial sets whose underlying functor is precisely decalage: 

$$Dec: Set^{\Delta^{op}} \to Set^{\Delta^{op}}$$

The map $d_{last}: Dec \to Id$ is the counit of this comonad. The comonad itself is analogous to a kind of unbiased path space comonad $P$ on $Top$ whose value at a space $X$ is a pullback 

$$\array{
P X & \to & X^I \\
\downarrow & & \downarrow eval_0 \\
|X| & \stackrel{i}{\to} & X
}$$

where $i$ is the set-theoretic identity inclusion of $X$ equipped with the discrete topology. Thus we have 

$$P X = \sum_{x_0 \in X} P(X, x_0),$$ 

the sum over all possible basepoints $x_0$ of path spaces based at $x_0$. The analogy is made precise by a canonical isomorphism 

$$Dec \circ S \cong S \circ P$$ 

where $S: Top \to Set^{\Delta^{op}}$ is simplicial singularization. 

A $P$-coalgebra partitions $X$ into path components and exhibits contractibility of each component. Similarly, a coalgebra of the decelage comonad exhibits the acyclicity of the underlying simplicial set. 

####Total D&#233;calage####

 Using either the simplicial [[comonadic resolution]] generated by the above comonad or directly using ordinal sum, we get a [[bisimplicial set]] known as the [[total decalage|total décalage]] of $Y$. This will be explored more fully in a separate entry.

## Literature

A reasonably full discussion of the d&#233;calage can be found in Luc Illusie's thesis, 

* L. Illusie, 1971, _Complexe cotangent et deformations I_, volume 239 of Lecture Notes in Maths ,  Springer-Verlag. and  1972, _Complexe cotangent et deformations II_, volume 283 of Lecture Notes in 
Maths , Springer-Verlag. 

It is used in Duskin's Memoir, 

* [[John Duskin]], 1975, _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc.


The notion of decalage is widely appearing since the paper introducing the method of [[cohomological descent]] in [[Hodge theory]]:

* [[Pierre Deligne]], _Th&#233;orie de Hodge. III_, Inst. Hautes &#201;tudes Sci. Publ. Math. __44__ (1974), 5--77. 

An application in theory of stacks is in

* [[Anders Kock]], _The stack quotient of a groupoid_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, __44__ no. 2 (2003), p. 85--104 [numdam](http://www.numdam.org/item?id=CTGDC_2003__44_2_85_0)


See also 

* Ehlers, _Algebraic Homotopy in Simplicially Enriched Groupoids_, 1993, 
University of Wales Bangor, available [[Ehlers-thesis.pdf|here:file]], (see also the reference below and the Tim Porter's [[Menagerie]] notes 


[[!redirects decalage]]
[[!redirects décalage]]
