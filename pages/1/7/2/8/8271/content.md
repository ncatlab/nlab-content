
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #tStruc}
###### Definition

Let $C$ be a [[triangulated category]]. A _t-structure_ on $C$ is a [[pair]] $\mathfrak{t}=(C_{\ge 0}, C_{\le 0})$ of [[strictly full subcategories]]

$$
   C_{\geq 0}, C_{\leq 0} \hookrightarrow C
$$

such that

1. for all $X \in C_{\geq 0}$ and $Y \in C_{\leq 0}$ the [[hom object]] is the [[zero object]]: $Hom_{C}(X, Y[-1]) = 0$;

1. the subcategories are closed under [[suspension]]/desuspension: $C_{\geq 0}[1] \subset C_{\geq 0}$ and $C_{\leq 0}[-1] \subset C_{\leq 0}$.

1. For all [[objects]] $X \in C$ there is a [[fiber sequence]] $Y \to X \to Z$ with $Y \in C_{\geq 0}$ and $Z \in C_{\leq 0}[-1]$.

 
=--

+-- {: .num_defn }
###### Definition

Given a t-structure, its _heart_ is the intersection

$$
  C_{\geq 0} \cap C_{\leq 0}
  \hookrightarrow
  C
  \,.
$$

=--

### In stable $\infty$-categories

In the [[infinity-category|infinity-categorical]] setting $t$-structures arise as [[torsion theory|torsion/torsionfree]] classes associated to suitable [[orthogonal factorization system|factorization systems]] on a [[stable infinity-category]] $C$.

* In a stable setting, the subcategories are closed under de/suspension simply because they are co/reflective and reflective and these operations are co/limits. Co/reflective subcategories of $C$ arise from co/[[reflective factorization systems]] on $C$;

* A _bireflective_ factorization system on a $\infty$-category $C$ consists of a [[orthogonal factorization system|factorization system]] $\mathbb{F}=(E,M)$ where both classes satisfy the [[two-out-of-three]] property.

* A bireflective factorization system $(E,M)$ on a stable $\infty$-category $C$ is called _normal_ if the diagram $S x\to x\to R x$ obtained from the reflection $R\colon C\to M/0$ and the coreflection $S\colon C\to *\!/E$ (where the category $M/\!* =\{A\mid (0\to A)\in M\}$ is obtained as $\Psi(E,M)$ under the adjunction $\Phi\dashv \Psi$ described at [[reflective factorization system]] and in [CHK](#CHK); see also [FL0, &#167;1.1](#FL0)) is _exact_, meaning that the square in
$$
\begin{array}{cccccc} 
0 &\to& S X &\to& X\\
&& \downarrow&&\downarrow\\
&& 0 &\to& R X\\
&& && \downarrow\\
&& && 0
\end{array}
$$
is a fiber sequence for any object $X$; see [FL0, Def 3.5 and Prop. 3.10](#FL0) for equivalent conditions for normality.

**Remark.** [CHK](#CHK) established a hierarchy between the three notions of simple, semi-exact and normal factorization system: in the setting of stable $\infty$-category the three notions turn out to be equivalent: see [FL0, Thm 3.11](#FL0).

**Theorem.** There is a bijective correspondence between the class $TS( C )$ of $t$-structures and the class of normal torsion theories on a stable $\infty$-category $C$, induced by the following correspondence:

* On the one side, given a normal, bireflective factorization system $(E,M)$ on $C$ we define the two classes $(C_{\ge0}(\mathbb{F}), C_{\lt 0}(\mathbb{F}))$ of a $t$-structure $\mathfrak{t}(\mathbb{F})$ to be the torsion and torsionfree classes $(*\!/E, M/\!*)$  associated to the factorization $(E,M)$.
* On the other side, given a $t$-structure on $C$ we set
$$E(t)=\{f\in C^{\Delta[1]} \mid \tau_{\lt 0}(f) \;\text{ is an equivalence}\};$$
$$M(t)=\{f\in C^{\Delta[1]} \mid \tau_{\geq0}(f) \;\text{ is an equivalence}\}.$$

_Proof._ This is [FL0, Theorem 3.13](#FL0)

**Theorem.** There is a natural monotone action of the group $\mathbb{Z}$ of integers on the class $TS( C )$ (now confused with the class $FS_\nu( C )$ of normal torsion theories on $C$) given by the suspension functor: $\mathbb{F}=(E,M)$ goes to $\mathbb{F}[1] = (E[1], M[1])$. 

This correspondence leads to study _families_ of $t$-structures $\{\mathbb{F}_i\}_{i\in I}$; more precisely, we are led to study _$\mathbb{Z}$-equivariant_ [[k-ary factorization system|multiple factorization systems]] $J\to TS( C )$.

**Theorem.** Let $\mathfrak{t} \in TS(C)$ and $\mathbb{F}=(E,M)$ correspond each other under the above bijection; then the following conditions are equivalent:

1. $\mathfrak{t}[1]=\mathfrak{t}$, i.e. $C_{\geq 1}= C_{\geq 0}$;
2. $C_{\geq 0}=*\!/E$ is a stable $\infty$-category;
3. the class $E$ is closed under pullback.

In each of these cases, we say that $\mathfrak{t}$ or $(E,M)$ is _stable_.

_Proof._ This is [FL1, Theorem 2.16](#FL1)

This results allows us to recognize _$t$-structures with stable classes_ precisely as those which are fixed in the natural $\mathbb{Z}$-action on $TS( C )$.

Two "extremal" choices of $\mathbb{Z}$-chains of $t$-structures draw a connection between two apparently separated constructions in the theory of derived categories: _Harder-Narashiman filtrations_ and _semiorthogonal decompositions_ on triangulated categories: we adopt the shorthand $\mathfrak{t}_{1,\dots, n}$ to denote the tuple $\mathfrak{t}_1\preceq \mathfrak{t}_2\preceq\cdots\preceq \mathfrak{t}_n$, each of the $\mathfrak{t}_i$ being a $t$-structure $((C_i)_{\ge 0}, (C_i)_{\lt 0})$ on $C$, and we denote similarly $\mathfrak{t}_\omega$. Then

* In the _stable case_ the tuple $t_{1,\dots, n}$ is endowed with a (monotone) $\mathbb{Z}$-action, and the map $\{0\lt 1\cdots\lt n\}\to TS( C )$ is equivariant with respect to this action; the absence of nontrivial $\mathbb{Z}$-actions on $\{0\lt 1\cdots\lt n\}$ forces each $t_i$ to be stable.
* In the _orbit case_ we consider an _infinite_ family $t_\omega$ of $t$-structures on $C$, obtained as the orbit of a fixed $(E_0, M_0)\in TS( C )$ with respect to the natural $\mathbb{Z}$-action.


### Towers

The HN-filtration induced by a $t$-structure and the factorization induced by a [[semiorthogonal decomposition]] on $C$ both are the byproduct of the _tower_ associated to a tuple $\mathfrak{t}_{1,\dots, n}$:

(...)


## Properties

### General

+-- {: .num_prop }
###### Proposition

The heart of a stable $(\infty,1)$-category is an [[abelian category]]. 

=--

([BBD 82](#BBD82), [[Higher Algebra|Higher Algebra, remark 1.2.1.12]], [FL0, Ex. 4.1](#FL0) and [FL1, &#167;3.1](#FL1))


### Application to spectral sequence

If the heart of a t-structure on a [[stable (∞,1)-category]] with [[sequential limits]] is an [[abelian category]], then the [[spectral sequence of a filtered stable homotopy type]] converges (see there).

## Related concepts

* [[Bridgeland stability]]

## References

For [[triangulated categories]]:

* [[Sergei Gelfand]], [[Yuri Manin]], *[[Methods of homological algebra]]*,  transl. from the 1988 Russian (Nauka Publ.) original, Springer (1996, 2002) &lbrack;[doi:10.1007/978-3-662-12492-5](https://doi.org/10.1007/978-3-662-12492-5)&rbrack;

* [[Donu Arapura]], _Triangulated categories and $t$-structures_ ([pdf](http://www.math.purdue.edu/~dvb/preprints/perv2.pdf))

* [[Alexander Beilinson]], [[Joseph Bernstein]], [[Pierre Deligne]], _Faisceaux pervers_, Asterisque __100__, Volume 1, 1982
 {#BBD82}

* D. Abramovich, A. Polishchuk, _Sheaves of t-structures and valuative criteria for stable complexes_, J. reine angew. Math. __590__ (2006), 89&#8211;130

* A. L. Gorodentsev, S. A. Kuleshov, A. N. Rudakov, _t-stabilities and t-structures on triangulated categories_, Izv. Ross. Akad. Nauk Ser. Mat. __68__ (2004), no. 4, 117&#8211;150

* A. Polishchuk, _Constant families of t-structures on derived categories of coherent sheaves_, Moscow Math. J. __7__ (2007), 109&#8211;134

* John Collins, [[Alexander Polishchuk]], _Gluing stability conditions_, [arxiv/0902.0323](http://arxiv.org/abs/0902.0323)


For [[stable (∞,1)-categories]]

* [[Jacob Lurie]], _[[Higher Algebra]]_


For [[reflective factorization systems]] and normal torsion theories in stable $\infty$-categories:

* Cassidy and H&#233;bert and [[Max Kelly|Kelly]], "Reflective subcategories, localizations, and factorization systems".  *J. Austral. Math Soc. (Series A)* 38 (1985), 287--329 ([pdf](http://journals.cambridge.org/download.php?file=%2FJAZ%2FJAZ1_38_03%2FS1446788700023624a.pdf&code=5796045be8904c5183c2e95bce65491e))
 

* {#RosickyTholen08} [[Jiri Rosicky]], [[Walter Tholen]], _Factorization, Fibration and Torsion_, Journal of Homotopy and Related Structures, Vol. 2(2007), No. 2, pp. 295-314  ([arXiv:0801.0063](http://arxiv.org/abs/0801.0063), [publisher](http://www.emis.de/journals/JHRS/volumes/2007/n2a14/))


* {#FL0} [[Domenico Fiorenza]], [[Fosco Loregian]], *$t$-Structures are normal torsion theories*, Appl Categor Struct **24** (2016) 181–208 &lbrack;[arxiv:1408.7003](http://arxiv.org/abs/1408.7003), [doi:10.1007/s10485-015-9393-z](https://doi.org/10.1007/s10485-015-9393-z)&rbrack; 

* {#FL1} [[Domenico Fiorenza]], [[Fosco Loregian]], [[Giovanni Marchetti]], *Hearts and towers in stable $\infty$-categories*,  J. Homotopy Relat. Struct. **14**  (2019) 993–1042 &lbrack;[arXiv:1501.04658](https://arxiv.org/abs/1501.04658), [doi:10.1007/s40062-019-00237-0](https://doi.org/10.1007/s40062-019-00237-0)&rbrack;


[[!redirects t-structures]]

[[!redirects t-structure on a stable (∞,1)-category]]
[[!redirects t-structures on a stable (∞,1)-category]]

[[!redirects t-structure on a stable (infinity,1)-category]]
[[!redirects t-structures on a stable (infinity,1)-category]]


[[!redirects heart]]
[[!redirects hearts]]


[[!redirects heart of a t-structure]]
[[!redirects hearts of t-structures]]

[[!redirects heart of a stable (∞,1)-category]]
[[!redirects hearts of stable (∞,1)-categories]]

[[!redirects heart of a stable (infinity,1)-category]]
[[!redirects hearts of stable (infinity,1)-categories]]
