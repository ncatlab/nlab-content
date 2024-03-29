
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea
 {#Idea}

The notion of *$E L_\infty$-algebras* is meant to be the fully [[homotopy theory|homotopy theoretic]] (i.e. [[(infinity,1)-category|$(\infty,0)$-]][[categorification|categorified]]) [[higher structure]] enhancing the [[mathematical structure]] of *[[Lie algebras]]*: For $E L_\infty$-algebras both the [[Jacobi identity]] *and* the *[[exterior algebra|skew symmetry]]* of the [[Lie bracket]] are relaxed up to potentially infinite [[coherence law|coherent]] [[higher homotopy]].

This is in contrast to the more widely considered notion of [[L-infinity algebras|$L_\infty$-algebras]], which relax the [[Jacobi identity]] but retain strict [[exterior algebra|skew symmetry]]. (Whence the terminology "$E L_\infty$": the "$E$" is for "everything homotopy", a whimsical but time-honored terminology, enshrined in the now classical terminology of [[E-infinity algebras|$E_\infty$-algebras]]).

The [[homotopy theory]] of $E L_\infty$-algebra is in fact [[equivalence of (infinity,1)-categories|equivalent]] to [[model structure for L-infinity algebras|that of $L_\infty$-algebras]] (and thus both [[relation between L-infinity algebras and dg-Lie algebras|are equivalent even to]] [[model structure on dg-Lie algebras|that of dg-Lie algebras]], which are further [[rectification|rectified]] $L_\infty$-algebras): $L_\infty$-algebras are a special case of $E L_\infty$-algebras and every $E L_\infty$-algebra is [[weak equivalence|weakly equivalent]] to one that is an $L_\infty$-algebra (i.e. the homotopy-skew-symmetry may always be [[rectification|rectified]] to strict skew symmetry).

Nevertheless, in some circumstances it is practically useful to work with instances of $E L_\infty$-algebras up to [[isomorphism]] without passing to a [[weak equivalence|weakly equivalent]] [[L-infinity algebra|$L_\infty$-algebra]]. In particular, [Borsten, Kim & Saemann 2021](#BKS21) argue that the notion of $E L_\infty$-algebra serves to give a transparent way to understand [[adjusted Weil algebras]] for [[L-infinity algebras|$L_\infty$-algebras]], and then to understand [[tensor hierarchies]] (in [[gauged supergravity]]-theory) in terms of the resulting [[connection on a smooth principal infinity-bundle|$\infty$-connections]]/[[higher gauge theory]].


## $h\mathcal{L}ie$- and $\mathcal{E}ilh$-algebras

The following notions have been introduced by ([BKS21](#BKS21)).

### $h\mathcal{L}ie$-algebras

\begin{definition}
An $h\mathcal{L}ie$-algebra $(\mathfrak{E},\varepsilon_1,\varepsilon_2^i)$ is a graded vector space $\mathfrak{E}$ together with a differential and a collection of binary products,
\[
        \begin{aligned}
            \varepsilon_1&: \mathfrak{E}\rightarrow \mathfrak{E}, &|\varepsilon_1|=1,
            \\
            \varepsilon^i_2&: \mathfrak{E}\otimes \mathfrak{E}\rightarrow \mathfrak{E}, &|\varepsilon^i_2|=-i,
        \end{aligned}
\]
such that
\[
            \begin{aligned}
                \varepsilon_1(\varepsilon_1(x_1))&=0,
                \\
                \varepsilon_1(\varepsilon^i_2(x_1,x_2))&=(-1)^i\big(\varepsilon^i_2(\varepsilon_1(x_1),x_2)+(-1)^{|x_1|}\varepsilon^i_2(x_1,\varepsilon_1(x_2))\big)
                \\
                &+\varepsilon^{i-1}_2(x_1,x_2)-(-1)^{i+|x_1|\,|x_2|}\varepsilon^{i-1}_2(x_2,x_1),
                \\
                \varepsilon^i_2(\varepsilon_2^i(x_1,x_2),x_3)&=(-1)^{i(|x_1|+1)}\varepsilon^i_2(x_1,\varepsilon^i_2(x_2,x_3))-(-1)^{(|x_1|+i)|x_2|}\varepsilon^i_2(x_2,\varepsilon_2^i(x_1,x_3))
                \\
                &-(-1)^{(|x_2|+|x_3|)|x_1|+(i-1)|x_2|}\varepsilon^{i+1}_2(x_2,\varepsilon^{i-1}_2(x_3,x_1)),
                \\
                \varepsilon^{j}_2(\varepsilon^{i}_2(x_1,x_2),x_3)&=
                (-1)^{1+j(i+1)+|x_1|(|x_2|+|x_3|)+(j-1)|x_2|}\varepsilon_2^{i+1}(x_2,\varepsilon_2^{j-1}(x_3,x_1)),
                \\
                \varepsilon^{i}_2(\varepsilon^{j}_2(x_1,x_2),x_3)&=
                (-1)^{i(j+|x_1|)}\varepsilon_2^{j}(x_1,\varepsilon_2^{i}(x_2,x_3))-(-1)^{(|x_1|+j)|x_2|}\varepsilon_2^i(x_2,\varepsilon_2^j(x_1,x_3))
                \\
                &-(-1)^{j+|x_3|(j+|x_2|-1)+|x_1|(|x_2|+|x_3|)}\varepsilon_2^{i+1}(x_3,\varepsilon_2^{j-1}(x_2,x_1))
            \end{aligned}
\]
are satisfied for all $i,j\in \mathbb{N}$ s.t. $j$<$i$ and for all $x_1,x_2,x_3\in \mathfrak{E}$, where we regard $\varepsilon_2^{-1}=0$.
\end{definition}

### $\mathcal{E}ilh$-algebras

\begin{definition}
        An $\mathcal{E}ilh$-algebra $(\mathfrak{E},Q,\oslash_i)$ is a differential graded vector space $(\mathfrak{E},Q)$ equipped with binary operations $\oslash_i$ of degree $i\in \mathbb{N}$ which satisfy the quadratic identities
\[
\begin{aligned}
                a\oslash_i(b\oslash_i c)&=(-1)^{i(|a|+1)}((a\oslash_i b)\oslash_i c+(-1)^{|a|\,|b|}(b\oslash_i a)\oslash_i c),
                \\
                a\oslash_i(b\oslash_j c)&=(-1)^{ij+j|a|}(a \oslash_i b)\oslash_j c,
                \\
                a\oslash_j(b\oslash_i c)&=\begin{cases}
                    (-1)^{i|a|+|a|\,|b|}(b \oslash_i a)\oslash_j c
                    &\text{if } j-i=1,
                    \\
                    (-1)^{i|a|+|a|\,|b|}(b \oslash_i a)\oslash_j c
                    &\text{if } j-i=2,
                    \\
                    +(-1)^{i(|a|+j+1)+(|a|+|b|)|c|}((c\oslash_{j-1} a)\oslash_{i+1}b)
                    \\
                    (-1)^{i|a|+|a|\,|b|}(b \oslash_i a)\oslash_j c
                    &\text{if } j-i>2
                    \\
                    +(-1)^{i(|a|+j+1)+(|a|+|b|)|c|}((c\oslash_{j-1} a)\oslash_{i+1}b)
                    \\        
                    
                    +(-1)^{j+|a|(|b|+i)+(|a|+|b|)|c|}((c\oslash_{i+1} b)\oslash_{j-1}a)
                \end{cases}
            \end{aligned}
\]
for $j$>$i$, and such that differential $Q$ satisfies the property
\[
            \begin{aligned}
                Q(a\oslash_i b)&=(-1)^i\big((Qa)\oslash_i b+(-1)^{|a|}a\oslash_i Qb\big)\\
                &+(-1)^i (a \oslash_{i+1}b)-(-1)^{|a|\,|b|} (b\oslash_{i+1} a),
            \end{aligned}
\]
which is a deformed Leibniz rule.
\end{definition}
    
\begin{proposition}
    $\mathcal{E}ilh$-algebras are Koszul dual to $h\mathcal{L}ie$-algebras.
\end{proposition}

\begin{definition}
The Chevalley--Eilenberg algebra $\mathrm{CE}(\mathfrak{E})$ of an $h\mathcal{L}ie$-algebra $\mathfrak{E}$ whose differential and binary products are given by 
\[
            \begin{aligned}
                \varepsilon_1&: \mathfrak{E}\rightarrow \mathfrak{E},&\tau_\alpha&\mapsto m^\beta_\alpha \tau_\beta,&&|\varepsilon_1|=1,
                \\
                \varepsilon^i_2&: \mathfrak{E}\otimes \mathfrak{E}\rightarrow \mathfrak{E},&\tau_\alpha\otimes \tau_\beta&\mapsto m^{i,\gamma}_{\alpha\beta}\tau_\gamma,&&|\varepsilon^i_2|=i
            \end{aligned}
\]
for some $m^\beta_\alpha$ and $m^{i,\gamma}_{\alpha\beta}$ taking values in the underlying ground field is the $\mathcal{E}ilh$-algebra $(\oslash_\bullet^\bullet V,Q,\oslash_i)$ with $V=\mathfrak{E}[1]^*$ and the differential
\[
            Q t^\alpha=-(-1)^{|\beta|}m^\alpha_\beta t^\beta-(-1)^{i(|\beta|+|\gamma|)+|\gamma|(|\beta|-1)}\,m^{i,\alpha}_{\beta\gamma}\,t^\beta \oslash_i t^\gamma,
\]
where $|\beta|\coloneqq|t^\beta|$.
\end{definition}

Consider
\[
            \oslash^\bullet_\bullet V \,\coloneqq\, \underbrace{\mathbb{R}}_{\text{deg }0}\oplus\underbrace{V}_{\text{deg }1}\oplus\underbrace{\bigoplus_{i\in \mathbb{N}}V\oslash_i V}_{\text{deg }2}\oplus\underbrace{\bigoplus_{i,j\in \mathbb{N}}(V\oslash_i V)\oslash_j V}_{\text{deg }3}\oplus\dots
\]
    
\begin{definition}
The Chevalley--Eilenberg algebra $\mathrm{CE}(\mathfrak{E})$ of an $h\mathcal{L}ie$-algebra $\mathfrak{E}$ whose differential and binary products are given by 
\[
            \begin{aligned}
                \varepsilon_1&: \mathfrak{E}\rightarrow \mathfrak{E},&\tau_\alpha&\mapsto m^\beta_\alpha \tau_\beta,&&|\varepsilon_1|=1,
                \\
                \varepsilon^i_2&: \mathfrak{E}\otimes \mathfrak{E}\rightarrow \mathfrak{E},&\tau_\alpha\otimes \tau_\beta&\mapsto m^{i,\gamma}_{\alpha\beta}\tau_\gamma,&&|\varepsilon^i_2|=i
            \end{aligned}
\]
for some $m^\beta_\alpha$ and $m^{i,\gamma}_{\alpha\beta}$ is the $\mathcal{E}ilh$-algebra $(\oslash_\bullet^\bullet V,Q,\oslash_i)$ with $V=\mathfrak{E}[1]^*$ and the differential
\[
            Q t^\alpha=-(-1)^{|\beta|}m^\alpha_\beta t^\beta-(-1)^{i(|\beta|+|\gamma|)+|\gamma|(|\beta|-1)}\,m^{i,\alpha}_{\beta\gamma}\,t^\beta \oslash_i t^\gamma,
\]
where $|\beta|\coloneqq|t^\beta|$.
\end{definition}

## $E L_\infty$-algebras

$E L_\infty$-algebras are the homotopy version of $h\mathcal{L}ie$-algebras, defined by ([BKS21](#BKS21)).

    
Analogously to an $L_\infty$-algebra, an $EL_\infty$-algebra structure on a graded vector space $\mathfrak{E}$ is encoded by a differential $Q$ on the $\mathcal{E}ilh$-algebra $\mathrm{CE}(\mathfrak{E})\coloneqq (\oslash_\bullet^\bullet \mathfrak{E}[1]^\ast, Q, \oslash_i)$. The differential $Q$ is given by its action on $\mathfrak{E}[1]^\ast$, which will be encoded by structure constants $m$ as follows:
\[
        Q t^\alpha=\pm m^\alpha\pm m^\alpha_\beta t^\beta\pm m^{i_1,\alpha}_{\beta_1\beta_2} t^{\beta_1}\oslash_{i_1} t^{\beta_2}\pm m^{i_1i_2,\alpha}_{\beta_1\beta_2\beta_3}(t^{\beta_1}\oslash_{i_1} t^\gamma)\oslash_{i_2} t^\delta+\ldots,
\]
where $\{t^\alpha\}$ is a basis on $\mathfrak{E}[1]^\ast$.

These structure constants $m$ define higher products $\varepsilon^I_n:\mathfrak{E}^{\otimes n}\rightarrow \mathfrak{E}$ with degree$-|I|$ by
\[
\begin{aligned}
            \varepsilon_0=m^\alpha \tau_\alpha, \;
            \varepsilon_1(\tau_\alpha)=m^\beta_\alpha \tau_\beta, \; \varepsilon_2^i(\tau_\alpha,\tau_\beta)=m^{i,\gamma}_{\alpha\beta}\tau_\gamma,\ldots
            \\
            \varepsilon^I_n(\tau_{\alpha_1},\ldots,\tau_{\alpha_n})=m_{\alpha_1\ldots\alpha_n}^{I,\beta} \tau_\beta,
        \end{aligned}
\]
where $I$ is a multi-index consisting of $n-1$ indices $i_1,i_2,\ldots,\in \mathbb{N}$ and $|I|\coloneqq i_1+i_2+\ldots$.

## Related concepts


* [[A-∞ algebra]]

* [[E-∞ algebra]]

* [[L-∞ algebra]]

  * [[homomorphism of L-∞ algebras]]

  * [[infinity-Lie algebra cohomology]]

  * [[universal enveloping E-n algebra]]

  * [[nilpotent L-∞ algebra]]

  * [[L-∞ algebroid]]

  * [[derived L-∞ algebroid]]

  * [[sheaf of L-∞ algebras]]

* [[relation between L-∞ algebras and dg-Lie algebras]]

* [[adjusted Weil algebra]]

* [[tensor hierarchy]]

* [[Leibniz algebra]]

## References 
 {#References}

The general notion is discussed in:

* {#BKS21} [[Leron Borsten]], [[Hyungrok Kim]], [[Christian Saemann]]: _$EL_\infty$-algebras, Generalized Geometry, and Tensor Hierarchies_ ([arXiv:2106.00108](https://arxiv.org/abs/2106.00108))

The special case of weak Lie 2-algebras was originally considered in:

* {#Roytenberg07} [[Dmitry Roytenberg]]: *On weak Lie 2-algebras*, in: *XXVI Workshop on Geometrical Methods in Physics*, AIP Conference Proceedings **956**, American Institute of Physics, (2007) &lbrack;[arXiv:0712.3461](https://arxiv.org/abs/0712.3461), [hdl:10993/10465](http://hdl.handle.net/10993/10465)&rbrack;

and the more general special case of weak Lie 3-algebras in:

* [[Malte Dehling]], *On weak Lie 3-algebras* &lbrack;[arXiv:1710.11104](https://arxiv.org/abs/1710.11104)&rbrack;



[[!redirects EL-infinity-algebras]]
[[!redirects EL-infinity algebra]]
[[!redirects EL-infinity algebras]]
[[!redirects EL-∞ algebra]]
[[!redirects EL-∞ algebras]]
[[!redirects EL-∞-algebra]]
[[!redirects EL-∞-algebras]]

[[!redirects hemistrict Lie 2-algebra]]
[[!redirects hemistrict Lie 2-algebras]]

[[!redirects weak Lie 2-algebra]]
[[!redirects weak Lie 2-algebras]]

[[!redirects weak Lie 3-algebra]]
[[!redirects weak Lie 3-algebras]]


