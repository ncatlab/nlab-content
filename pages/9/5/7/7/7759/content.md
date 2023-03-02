
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Model theory
+-- {: .hide}
[[!include model theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

In [[model theory]] the notion of *abstract elementary classes* is a vast generalizations of that of [[elementary classes]] of [[structure in model theory|structures]] beyond [[first-order theory|first-order theories]] (e.g. for the infinitary logic $L_{\omega_1,\omega}$) as introduced by [[Saharon Shelah]]. Their theory is also more general than the homogeneous model theory. 

An __abstract elementary class__ is a __nonempty__ class $K$ of structures for a given signature with language $L(K)$, that is closed under [[isomorphisms]] and equipped with a strong substructure relation $\prec_K$ (strong substructure relation means that if $M\prec_K N$ and $M_0\subset M$ is a substructure, then $M_0 \prec_K N$) that is a [[partial order]] satisfying the axioms on union of chains (Tarski-Vaught), coherence and downward Loewenheim-Skolem properties. More precisely, $\prec_K$ is a partial order such that 

(A0) if $M,N\in K$, $M\prec_K N$ then $M\subset N$

(A1) (closure under isomorphisms) 

* (a) $M\in K$ and $N$ an $L(K)$ structure with $N\cong M$, then $N\in K$

* (b) if $N_1,N_2,M_1,M_2\in K$, $f_i : N_i\cong M_i$, $i = 1,2$, $f_1\subset f_2$, with $M_1\prec_K M_2$ then $N_1\prec_K N_2$

(A2) for $M,N,P\in K$, if $M\prec_K P$, $N\prec_K P$, and $M\subset N$, then $M\prec_K N$ 

(A3) downward Loewenheim-Skolem. There exist a cardinal $LS(K) = LS(K,\prec_K)\geq |L(K)|+\aleph_0$ such that $\forall M\in K$, $\forall A\subset |M|$, $\exists N\in K$ with $A\subset |N|$, $N\prec_K M$, $\|N\|\leq |A|+LS(K)$.  

(A4) (Tarski-Vaught chain condition) for every regular cardinal $\mu$

....

The usual elementary classes, i.e. the classes of the form $K = Mod(T)$ for a first-order theory $T$, are abstract elementary with respect to the relation $\prec_K$ of being an elementary submodel, with ${|LS(K)|} = {|L(T)|}+\aleph_0$ ($L(T)$ is the underlying language of the theory $T$). 



## Related entries

* [[amalgamation]]

## References

* wikipedia [abstract elementary class](http://en.wikipedia.org/wiki/Abstract_elementary_class)

* [[Saharon Shelah]], _Classification theory for elementary abstract classes I, II, Studies in Logic (London), __18__, __20__, College Publications, London 2009

* John Baldwin, _Categoricity_, Amer. Math. Soc. 2011, [pdf](http://www.math.uic.edu/~jbaldwin/pub/AEClec.pdf)

* D. W. Kueker, _Abstract elementary classes and infinitary logic_, Ann. Pure Appl. Logic __156__ (2008), 274-286.

AECs can also be essentially identified with [[accessible categories]] in which all morphisms are [[monomorphisms]].  Some recent papers which study them from this viewpoint include:

* [[Tibor Beke]], [[Jiří Rosický]] _Abstract elementary classes and accessible categories_, Annals of Pure and Applied Logic __163__ (2012) 2008-2017, [arxiv/1005.2910](http://arxiv.org/abs/1005.2910) 

* Michael Lieberman, [[Jiří Rosický]], Sebastien Vasey, *Internal sizes in μ-abstract elementary classes*, [arxiv/1708.06782](https://arxiv.org/abs/1708.06782); *Set-theoretic aspects of accessible categories*, [arxiv/1902.06777](https://arxiv.org/abs/1902.06777)

* M. J. Lieberman, _Topological and category-theoretic aspects of abstract elementary classes_, Thesis, The University of Michigan 2009, [pdf](http://deepblue.lib.umich.edu/bitstream/2027.42/63854/1/liebermm_1.pdf); defense slides [pdf](http://www.math.upenn.edu/~mlieb/defense.pdf); _Category theoretic aspects of abstract elementary classes_, Annals Pure Appl. Logic __162__ (2011), 903-915; _A topology for Galois types in AECs_, [arxiv/0906.3573](http://arxiv.org/abs/0906.3573)

On [[topos theory|topos theoretic]] methods in model theory of AECs:

* Christian Espíndola, _A topos-theoretic proof of Shelah's eventual categoricity conjecture for abstract elementary classes_, [arxiv/1906.09169](https://arxiv.org/abs/1906.09169); _A short proof of Shelah's eventual categoricity conjecture for AEC's with amalgamation, under GCH_, [arxiv/1909.13713](https://arxiv.org/abs/1909.13713)

On the [[homotopy types]] of [[classifying spaces]] of abstract elementary classes:

* [[Tim Campion]], Jinhe Ye, *Homotopy Types of Abstract Elementary Classes*, Journal of Pure and Applied Algebra
**225** 5 (2021) 106461 &lbrack;[arXiv:1909.07965](https://arxiv.org/abs/1909.07965), [doi:10.1016/j.jpaa.2020.106461](https://doi.org/10.1016/j.jpaa.2020.106461)&rbrack;





[[!redirects abstract elementary classes]]