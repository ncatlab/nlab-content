<div class="rightHandSide toc">
[[!include differential graded objects - contents]]
</div>


##Differential graded Lie algebras

A _pre-graded Lie algebra_ (pre-gla) is a [[graded vector space|pre-gvs]], $L$, together with a bilinear map of degree zero

$$[\quad,\quad ] : L\otimes L \to L,$$

such that

$$[x,y] = (-1)^{|x||y|+1}[y,x]$$

and 

$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$

for every triple $(x,y,z)$ of homogeneous elements in $L$.

(The first property is call _antisymmetry_, the second _the Jacobi identity_.)

A _morphism_ $f: L \to L'$ of pre-glas is a linear map of degree zero, that is compatible with the brackets,

$$f[x,y] = [f(x),f(y)].$$

####Examples

a) To any augmented pre-ga $A$, one can associate a pre-gla, denoted $\bar{A}_L$, with underlying gvs $\bar{A}$ and with bracket, the commutator, $[x,y] = xy -(-1)^{|x||y|}yx$ for each pair $(x,y)$ of homogeneous elements.  $\bar{A}_L$ is abelian (i.e. with trivial bracket) if and only if $A$ is graded commutative.

b) If $A$ is a pre-cga and $L$ is a pre-gla, the tensor product $A\otimes L$ has a pre-gla structure with bracket

$$[a\otimes l,a'\otimes l'] = (-1)^{|a||l|}aa' \otimes [l,l']$$

for $a,a', l, l'$ homogeneous.


####Derivations of graded Lie algebras

Let $L$ be a pre-gla.  A _derivation_ of glas, of degree $p\in \mathbb{Z}$, is a linear mapping $\theta \in Hom_p(L,L)$ such that

$$\theta[x,y] = [\theta{x},y] + (-1)^{p|x|}[x,\theta(y)]$$

for any pair $x,y$ of homogeneous elements of $L$.  We denote by $Der_p(L)$, the vector space of degree $p$ derivations of the gla, $L$.

###Differential graded Lie algebras

A differential $\partial$ of a pre-gla is a Lie algebra derivation of degree -1 such that $\partial\circ \partial = 0$.  The pair $(L,\partial)$ is then called a _differential pre-graded Lie algebra_ (pre-dgla); its homology $H(L,\partial)$, is a pre-gla.  

A morphism of pre-dglas is a morphism for both the underlying pre-gla and the pre-dgvs. We denote the corresponding category  by $pre DGLA$.


This means that a  differential graded Lie algebra is an internal Lie algebra in the symmetric monoidal category of chain complexes with tensor product given as in [[differential graded vector space|differential graded vector spaces]]. 

+--{:  .query}
[[Tim Porter|Tim]]:  I have changed the wording that Zoran suggested slightly. Of course, a dgla is an internal Lie algebra, a term that needs making precise in an entry, but  then we must make precise the tensor product, and the symmetry.  All that abstract baggage is, of course, in other entries, but I think it best to avoid the term 'simply'.  I have heard it expressed that category theorists tend to use the term 'simply' aand other similar terms too much from the point of view others working in neighbouring disciplines.  

For instance, if someone knows de Rham theory from a geometric viewpoint, we know that  in the long run it will be useful for them to understand the differential graded algebra from a categorical viewpoint  as that is one of the most fruitful  approaches for geometrically significant generalisations and applications BUT the debutant can get very put off by thinking that they have to understand lots of category theory before they can start understanding the de Rham complex. In fact coming from that direction they can understand the category theory via the de Rham theory.  So I suggest that we simply avoid 'simply'!!  

I know some researchers in other subject areas are looking with interest to the nLab as a quick means of entry into some interesting mathematics and a handy reference for definitions and background. That is great but it perhaps means that  we have to be a bit careful about our natural feeling that the categorical approach is nearly always the 'best'.  'Simply' is one problem, another is, I think, use of diagrams rather than formulae.  My feeling is that both should be given (though the diagrams are more difficult to get looking nice). 

[[Urs Schreiber|Urs]]: these are all good points. In general I believe it will be good to offer different perspectives in an $n$Lab entry, and explain what they are useful for, each. I take the point that the word "simply" for the categorical perspective may raise unintended feelings, so maybe it should be avoided or at least not left uncommented. 

But we should also not hide the important point here, which is hinted at by the word simply: I think that the important point is that the abstract  category-theoretic formulation which packages a long list of detailed definitions in a single statement such as "internal Lie algebra" allows us to recognize that that list of definitions is _right_.

There are many definitions that one can dream up. But some are better than others and category theory can explain why.

For instance I have seen experts who calucalted with differential graded algebra all day long be mystified by why exactly all the sign rules are as they are. The best explanation they had was: it works and yields interesting results. They were positively interested to learn that _all_ these signs follow automatically and consistently by realizting that differential graded algebra is algebra internal to the category of chain complexes.

This doesn't mean that it is best to introduce DGCA in this internal language. But it does mean that it is worthwhile pointting out that lots of nitty-gritty details of definitions can "simply" be derived by starting with an abstract internal definition and then turning the crank.


[[Tim Porter|Tim]]: I could not have put it better myself. I was wondering if there might not be some  way in which this viewpoint might not be expressed explicitly.  Perhaps David C has some thoughts.. sort of 'the unreasonable effectiveness of categorical language'?

My intention for my own contribution (with help hopefully) is to gradually add glosses in the lexicon entries so as to help interpret in both directions, categorically,and geometrically. 

For instance, in the construction of the cobar one take the tensor algebra of the suspension of the cokernel (is it?) of the augmentation.  WHY?!!!!!!! How can one understand this? Magic? It works? In fact it is still a bit of a mystery to me and saying that it comes from such and such a categorical property still needs spelling out for me. I have asked rational homotopy theorists and have partially understood things from their point of view but there are still gaps in my understanding of it and some of them worry me!

_Toby_:  One should be able to say something like, 'From a category-theoretic perpsective, a differential graded Lie algebra is simply an internal Lie algebra in an appropriate category of chain complexes.'.  This advertises what Urs says, that definitions come automatically from the category-theoretic perspective, without pretending that this will be simple to anyone coming from outside that perpsective.

[[Zoran Škoda]]: Tim, your question about the intricacies of cobar construction in the category of chain complexes is an interesting one, which I can not fully answer, specially in a short answer. However, still the categorical picture simplifies the viewpoint and the definition at least,and gives a direction how to proceed there as well. Given a dgca
C one looks at the functor Tw(C,A) assigning to an algebra A the set of solution of the [[Maurer-Cartan equation]] $d t + t*t = 0$ where $*$ is the convolution product. Cobar construction is the (co)representative of this covariant functor. If you take Tw(C,A) as a contravariant functor on the coalgebras, for fixed A, then its representative is the bar construction (this is said in different words in entry [[twisting cochain]]). So bar and cobar construction are simply representatives of very natural functors; accidents of the realization of these functors by formulas in Ch are a bit unfortunate as you pointed out.
=--

####Examples

a) If $(A,\partial)$ is an augmented pre-dga, $(\bar{A}_L,\partial)$ is a pre-dgla.

b) If $(A,\partial)$ is a pre-cdga and $(L,\partial')$, a pre-dgla, $A \otimes L$, together with the tensor product differential, is a pre-dgla.

c)  Let $(V,\partial)$ be a pre-dgvs, then the pre-dgvs, $(Hom(V,V),D)$, constructed earlier is a pre-dga  for the multiplication law given by composition of mappings.  Its associated pre-dgla has

$$[f,g] = f\circ g - (-1)^{|f||g|}g\circ f$$

and 

$$Df = [\partial,f].$$

In particular, if $(V,\partial) = (A,d)$ is a cdga (resp. $(V,\partial) = (L,\partial)$ is dgla), then $Der(A,d) = (\bigoplus_p Der_p(A),D)$, (resp. $Der(L,\partial) = (Der_p(L),D)$) is a sub-pre-dgl of $(Hom(V,V),D)$.


####DGLA

A dgla is a pre-dgla with a lower grading; explicitly:


###Definition

A **differential graded Lie algebra**, $(L,\partial)$, is a graded vector space $L = \bigoplus_{p\geq 0}L_p$, together with a bilinear map of degree 0
$$[\quad ,\quad] : L\otimes L \to L,$$
and a differential $\partial$ satisfying 
$$\partial L_p \subseteq L_{p-1},  \quad [x,y] = (-1)^{|x||y|+1}[y,x],$$
$$(-1)^{|x||z|}[x,[y,z]] +(-1)^{|y||x|}[y,[z,x]] +(-1)^{|z||y|}[z,[x,y]] = 0$$
and
$$\partial[x,y] = [\partial x,y] + (-1){|x|}[x,\partial y]$$
for every triple $(x,y,z)$ of homogeneous elements in $L$.

Let $DGLA$ be the corresponding category.



A dgla is $n$-_reduced_ (resp. _homologically $n$-reduced_) if $L_p = 0$ (resp. $H_p(L,\partial) = 0$) for all $p\lt n$.  Denote by $DGLA_n$ (resp.  $DGLA_{hn}$), the corresponding categories.

####Filtrations

If $(L,\partial)$ is a pre-dgla, a _gla-filtration_ of $L$ (resp. a _dgla-filtration_ of $( L,\partial)$ ) is a family of subgraded vector spaces $F_p L$, $p\in \mathbb{Z}$, such that $F_p L\subseteq F_{p+1}L$, $[F_p L,F_n L]\subseteq F_{p+n} L$, (resp. and $\partial F_p L\subseteq F_p L$).

####Bracket length filtration

Let $L$ be a pre-gla.  Its _bracket length filtration_ is obtained from the descending central series:

$$F^1 L = L; \quad F^p L = [L,F^{p-1} L] \quad  if \quad p\geq 2.$$

It is a gla-filtration.

$Q(L) = L/F^2L$ is called the _space of indecomposables_ of $L$.

If $(L,\partial)$ is a pre-dgla, $F^p L$ is stable by $\partial$.  Letting $Q(\partial)$ be the induced differential on $Q(L)$, $Q$ then defines a functor
$$Q : pre DGLA \to pre DGVS.$$

####Free Lie algebra, $\mathbb{L}(V)$.

Let $V$ be a pre-gvs, $T(V)$, the tensor algebra on $V$ with augmentation ideal $\overline{T(V)}$ (recall $T(V) = \bigoplus_{n\geq 0} V^{\otimes n}$ and the augmentation sends $V (= V^{\otimes 1}$ to 0). 

 Let $\overline{T(V)}_L$ be $\overline{T(V)}$ with the pre-gla structure given by the commutators.  We denote by $\mathbb{L}(V)$, the Lie subalgebra of $\overline{T(V)}_L$ generated by $V$. 
+--{:query}
[[Tim Porter|Tim]]: A more explicit description may help here, cf. Quillen, Rational Homotopy theory (p.281) or MacLane, Homology.
=--
If $L$ is a pre-gla, any morphism of pre-gvs $f: V\to L$ has a unique extension to a pre-gla morphism $\hat{f} :\mathbb{L}(V)\to L$.  If $(e_\alpha)_{\alpha\in I}$ is a homogeneous basis for $V$, $\mathbb{L}(V)$ may be denoted $\mathbb{L}((e_\alpha)_{\alpha\in I})$.

On the free Lie algebra $\mathbb{L}(V)$, the bracket length filtration comes from a gradation $\mathbb{L}(V) = \bigoplus_j\mathbb{L}^j(V) $, where $\mathbb{L}^j(V) $ is the subspace generated by the brackets of elements of $V$ of length $j$.  The inclusion $\mathbb{L}(V)\hookrightarrow T(V)$ identifies $\mathbb{L}^j(V)$ with $\mathbb{L}(V)\cap T^j(V)$.

If $\mathbb{L}(V), \partial)$ is a dgla, free as a gla, with $V$ fixed, $\partial$ is the sum of derivations $\partial_k$ defined by : $\partial_k \subset \mathbb{L}^k(V)$.  The isomorphism between $V$ and $Q\mathbb{L}(V)$ identifies $\partial_1V$ with $Q(\partial)$.  $\partial_1$ (resp. $\partial_2$) is called the _linear part_ (resp, the _quadratic part_) of $\partial$.




####Products and Coproducts (sums)

Let $(L,\partial)$ and $(L',\partial')$ be two dglas.  Their _product_ $(L,\partial)\times(L',\partial')$ in $DGLA$ is defined by:

*  the underlying vector space is the direct sum $L\oplus L'$;

*  $(L,\partial)$ and $(L',\partial')$ are two sub differential graded Lie algebras of $(L,\partial)\times(L',\partial')$;

*  if $x\in L$ and $x' \in L'$, then $[x,x'] = 0$.

Their _coproduct_ or _sum_ $(L,\partial)\star(L',\partial')$ is often called their _free product_. 

 For example.

$$\mathbb{L}(V)\star \mathbb{L}(V') \cong   \mathbb{L}(V\oplus V').$$

More generally if $L$ and $L'$ are given by generators and relations

$$L = \mathbb{L}(V)/I , \quad L' = \mathbb{L}(V')/I' ,$$

$$L\star L' = \mathbb{L}(V\oplus V')/{I,I'}.$$

The differential on $L\star L'$ is the unique Lie algebra derivation extending $\partial$ and $\partial'$.