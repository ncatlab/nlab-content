
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Nonstandard analysis is a rich formalization of [[analysis]] that uses a certain explicit notions of [[infinitesimal objects]]. In fact, not only infinitesimal but also infinitely large can be accomodated (and must be).  Moreover, not only the field of [[real numbers]], but more general algebraic structures can be extended, essentially via a construction of [[ultraproducts]]; also general sets can be extended to contain nonstandard elements (see [[internal set]]).

In fact the nonstandard method is not limited to analysis, but is rather a method of producing a models in the sense of [[model theory]], as pioneered by Robinson or using a syntactic extension of set theory, like the theory of [[internal sets]] by Nelson.

See also [[nonstandard analysis in topology]], [[internal set]].


## Motivation

At its beginning, infinitesimal calculus was developed nonrigorously, though many interesting arguments and formal manipulations were found. Cauchy and Weierstra&#223; introduced the $\epsilon$-$\delta$ approach, which enabled modern rigorous [[analysis]], but sometimes this method is cumbersome. For example, sometimes one needs to work with several infinitesimal levels or kinds of continuity in the same problem, and finding estimates may be very cumbersome. One would like to introduce infinitesimal quantities as additional elements of the sets of usual ('standard') quantities. Several related rigorous frameworks appeared under the name of __nonstandard analysis__, since the first such discovered by [[Abraham Robinson]]. Most often, approaches using [[ultrafilters]], certain classes called [[internal sets]] and using [[topos theory]] enable the foundation of nonstandard analysis. Many properties and theorems from classical analysis imply new statements of nonstandard analysis; the mechanism is the so-called __transfer principle__, which can be required axiomatically without respect to a particular model of nonstandard analysis. 


## Models

### An approach via ultrafilters

Assuming the [[axiom of choice]] (whose full strength is not necessary), there exists a free (= not containing finite subsets) [[ultrafilter]] $F$ on the set of [[natural numbers]] $\mathbb{N}=\{1,2,3,\ldots\}$, and such ultrafilters are in $1$--$1$ correspondence with finitely additive [[measures]] on $\mathbb{N}$ (using the [[power set|algebra of all subsets]]) taking values in the two element set $\{0,1\}$.


Fix a free ultrafilter $F$ on $\mathbb{N}$, and consider the set of all [[sequences]] of real numbers, $\mathbb{R}^{\mathbb{N}}$. So an element in here is a sequence

$$
  a = (a_0, a_1, a_2, \cdots)
$$

of real numbers.

We write $f\sim_F g$ if the set $\{i\in\mathbb{N}|f(i)=g(i)\}$ belongs to $F$; these are precisely the sequences which are equal almost everywhere with respect to the associated measure. The relation $\sim_F$ is an [[equivalence relation]] and ${}^*\mathbb{R} := \mathbb{R}^{\mathbb{N}}/{\sim_F}$ is a __nonstandard extension__ of $\mathbb{R}$, whose elements are sometimes called **hyperreal numbers**. 

(This is a special case of the [[ultraproduct]] construction in [[model theory]].  In fact, we could have started with an ultrafilter on any set, not just $\mathbb{N}$.  Such more general ultraproducts are necessary in order to obtain more refined models of nonstandard analysis satisfying stronger "saturation" principles.)

Given $f\in \mathbb{R}^{\mathbb{N}}$, we write $f_F$ for its equivalence class in ${}^*\mathbb{R}$. In particular, given any real number $r\in \mathbb{R}$ the image $^* r :=(i\mapsto r)_F$ of the constant sequence 

$$
  r = (r,r,r, \cdots )
  \,.
$$

is an element in $^*\mathbb{R}$ and this gives an [[injection]] $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$. 


$^*\mathbb{R}$ is equipped with a strict total ordering given by

$$
f_F\lt g_F \;\Leftrightarrow\; \{i\in\mathbb{N}|f(i)\lt g(i)\}\in F,
$$

which makes $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$ a [[monotone function]]. 

* An element $\delta\in{}^*\mathbb{R}$ such that $^* 0\lt\delta$ is called a __positive number__ .  

* An element $\delta$ such that for all positive $r\in \mathbb{R}$ we have  $ -{}^* r \lt  \delta\lt{}^* r$ is called an __infinitesimal number__. 

Unlike in the real numbers, positive infinitesimal numbers exist: for example the class $f_F$ where $f:n\mapsto 1/n$ is such and $g_F$ for $g:n\mapsto 1/n^2$ is a different one. 


Let $n$ be a nonnegative integer and $u:\mathbb{R}^n\to\mathbb{R}$ a function. Then there is a nonstandard extension $^* u:({}^*\mathbb{R})^n\to{}^*\mathbb{R}$ of $u$; it is defined by

$$
^*u(f^1_F,\ldots, f^n_F) = g \;\Leftrightarrow\; \{i\in\mathbb{N}| u(f^1(i),\ldots,f^n(i))=g(i) \}\in F.
$$

This is indeed an extension of $u$ in the sense that $^* u({}^*r_1,\ldots,{}^*r_n)={}^* r$ iff $u(r_1,\ldots,r_n)=r$.
This way, the usual operations $+,\cdot$ and the absolute value $|\cdot|$ extend to $^*\mathbb{R}$; usually one denotes these and other standard operations on ${}*\mathbb{R}$ without putting $^*$ in front, writing simply e.g. $f_F+g_F$.


To extend division appropriately, we need a little bit more care as it is originally just partially defined, so we need an extension of the formalism to subsets of the real line. In particular there is a following definition of an extension $^* E\subset{}^*\mathbb{R}$ of a subset $E\subset\mathbb{R}$:

$$
f_F\in{}^* E \;\Leftrightarrow\; \{i\in\mathbb{N}|f(i)\in E\}\in F.
$$

(For example, a number is positive, as defined earlier, if an only if it belongs to $^*\{r|r \gt 0\}$.)  Then division is extended to a function $^*\mathbb{R} \times ^*\{r|r \ne 0\} \to ^*\mathbb{R}$.  If $1/x$ is infinitesimal, then $x$ itself is __infinite__.


Conversely, an element $x\in{}^*\mathbb{R}$ is __finite__ if $|x|\lt {}^* r$ for some $r\in\mathbb{R}$. Every finite element $x\in{}^*\mathbb{R}$ is infinitely close to a unique real number $q\in\mathbb{R}$ in the sense that $x-{}^*q$ is infinitesimal. We say that $q$ is the __standard part__ of $x$ and is denoted by $q= st(x)$. Given a real number $r\in\mathbb{R}$, the subset $\mu(r)$ of all elements $x\in{}^*\mathbb{R}$ such that $st(x)=r$ is said to be the __monad__ of the real number $r\in\mathbb{R}$. Monads should be thought of as infinitesimal neighborhoods. An elementary fact:
a subset $E\subset\mathbb{R}$ is open iff $\mu(r)\subset{}^*E$ for all $r\in E$; $E$ is closed iff $st(x)\in E$ for all finite $x\in{}^* E$; and $E$ is [[compact space|compact]] iff, for all $x\in{}^* E$, $x$ is finite and $st(x)\in E$. 


In this model of nonstandard analysis, the [[transfer principle]] is a corollary of a general theorem on ultraproducts due Jerzy &#321;o&#347;.  It can be stated in terms of a certain formal language $L(\mathbb{R})$ of the real numbers.  We can also extend this model to ultrapowers of larger sets, not just $\mathbb{R}$ itself, with a corresponding extension of the language.  In the limit where we reach an entire "universe" of mathematics, this leads to the topos-theoretic filterquotient and sheaf models below.


### Filterquotients of topoi

The ultrapower construction above can be performed in the general context of [[topos]] theory.  From any topos $\mathcal{E}$ and any filter $\Phi$ of [[subterminal objects]] in $\mathcal{E}$, one can construct a topos $\mathcal{E}/\Phi$, the [[filterquotient]] of $\mathcal{E}$ by $\Phi$.  There is a [[logical functor]] $\mathcal{E} \to \mathcal{E}/\Phi$.

If $\mathcal{E} = Set / \mathbb{N}$, then any filter on $\mathbb{N}$ gives a filter of subterminals in $\mathcal{E}$,  whose corresponding filterquotient corresponds to the above construction.  The composite functor
$$ Set \to Set/\mathbb{N} \to (Set/\mathbb{N})/\Phi $$
might be written $^*(-)$.  If $\Phi$ is an ultrafilter, then $(Set/\mathbb{N})/\Phi$ is a two-valued topos, whose [[internal logic]] is essentially that of the ultrafilter model described above.  In particular, the global elements of $^*\mathbb{R}$, as an object of this topos, are precisely the "hyperreal numbers" described above.

In this context, the [[transfer principle]] is the fact that the functor $^*(-)$ is both [[logical functor|logical]] and [[conservative functor|conservative]], and hence it both preserves and reflects the truth of formulas in the internal languages.


### Sheaves on the topos of filters

A different topos-theoretic construction is to consider the topos of sheaves on a category of filters.  This topos models the [[internal set]] theory of Nelson, a more axiomatic approach to nonstandard analysis.  References:

* I. Moerdijk, _A model for intuitionistic non-standard arithmetic_
* Erik Palmgren, _[A sheaf-theoretic foundation for nonstandard analysis](http://www.sciencedirect.com/science/article/pii/S0168007296000413)_
* E. Palmgren, _A constructive approach to nonstandard analysis_
* E. Palmgern, _Remarks on a constructive sheaf model of nonstandard analysis_, [doi](http://dx.doi.org/10.1.1.30.4785)
* Jonas Eliasson, _Ultrapowers as sheaves on a category of ultrafilters_

## Measure and generalized functions

The Lebesgue measure on $\mathbf{R}^n$ extends to [[Loeb measure]] on ${}^\ast\mathbf{R}^n$. This may be used for probability theory and also for generalized functions. 

The theory of generalized functions of Schwarz can be reproduced by nonstandard analysis:

__Theorem.__ ([[Abraham Robinson]]) Every generalized function $f:\mathbf{R}\to\mathbf{R}$ can be represented as the integration of the product of test function with a nonstandard smooth function $\tilde{f}: {}^\ast\mathbf{R}\to{}^\ast \mathbf{R}$ 

$$
(f,\phi) = \int \tilde{f} \phi d x
$$

There is also inutionistic version of nonstandard analysis approach to generalized functions as well as nonstandard approaches to Sato [[hyperfunction]]s (Sousa pinto), to Coulombeu distributions etc. 


## Relationship to other types of infinitesimal {#ToposModels}

There are other ways of realizing the notion of [[infinitesimal number]] precisely, such as [[synthetic differential geometry]] and the [[surreal number]]s.  Neither seem to be very closely related to NSA---the techniques and flavor of each subject are quite different.  However, some things can be said.

* While the most common infinitesimals appearing in SDG are [[nilpotent]], in contrast to those of NSA which are invertible, some models of SDG do contain invertible infinitesimals; see [here](http://ncatlab.org/nlab/show/infinitesimal+number#NSAvsSDG).

* Since the surreal numbers are the universally embedding ordered field, any field of hyperreals can be embedded in the surreals.  However, such embeddings don't seem very useful, since they don't preserve any of the important structure of the hyperreals (such as the transfer principle).

## Related concepts

* [[monad in nonstandard analysis]] ([[infinitesimal neighbourhood]])

## References 
 {#References}

Original references:

* {#Robinson66} [[Abraham Robinson]], *Non-standard analysis*, Studies in Logic and the Foundations of Mathematics **42**, North-Holland (1966), Princeton University Press (1996) &lbrack;[ISBN:9780691044903](https://press.princeton.edu/books/paperback/9780691044903/non-standard-analysis)&rbrack;

* {#Keisler76} [[Jerome Keisler]], *Foundations of Infinitesimal Calculus*, Prindle Weber & Schmidt (1976, 2022) &lbrack;[pdf](https://people.math.wisc.edu/~hkeisler/foundations.pdf)&rbrack;

* [[Jerome Keisler]], _Elementary calculus: an infinitesimal approach_, [online](http://www.math.wisc.edu/~keisler/calc.html) undergraduate textbook.

Textbook accounts:

* E. I. Gordon, A. G. Kusraev, [[Semën S. Kutateladze]], *Infinitesimal Analysis*, Mathematics and its Applications **544**, Springer (2002) &lbrack;[doi:10.1007/978-94-017-0063-4](https://doi.org/10.1007/978-94-017-0063-4)&rbrack;


See also:

* Wikipedia: [nonstandard analysis](http://en.wikipedia.org/wiki/Non-standard_analysis), [ultraproduct](http://en.wikipedia.org/wiki/Ultraproduct), [hyperreal numbers](http://en.wikipedia.org/wiki/Hyperreal_numbers), [Abraham Robinson](http://en.wikipedia.org/wiki/Abraham_Robinson), [constructive non-standard analysis](http://en.wikipedia.org/wiki/Constructive_non-standard_analysis), [criticism of nonstandard analysis](http://en.wikipedia.org/wiki/Criticism_of_non-standard_analysis)

* [[Sergio Albeverio]], Jens Erik Fenstad, Raphael Hoegh-Krohn, _Nonstandard methods in stochastic analysis and mathematical physics_, Academic Press 1986 (there is also a Dover 2009 edition and a 1990 Russian translation)


* Sergio Salbany, Todor Todorov, _Nonstandard analysis in topology_, [arxiv/1107.3323](http://arxiv.org/abs/1107.3323)  



* {#Moerdijk95} [[Ieke Moerdijk]], _A model for intuitionistic nonstandard arithmetic_, Annals of Pure and Applied Logic __73__ (1995), pp. 37&#8211;51.

* [[Jaap van Oosten]], _Synthetic Nonstandard Arithmetic_, 2011 ([pdf](https://www.staff.science.uu.nl/~ooste110/talks/darmstadt2.pdf))

* Juha Ruokolainen, _Constructive nonstandard analysis without actual infinity_, 2004, [pdf](https://oa.doria.fi/bitstream/handle/10024/2865/construc.pdf)
* E. Palmgren, _Developments in Constructive Nonstandard Analysis_, Bull. Symbolic Logic __4__, n. 3 (1998), 233&#8211;272.

* E. Palmgren, _Constructive nonstandard representations of generalized functions_, <a href="http://dx.doi.org/10.1016/S0019-3577(00)88579-1">doi</a> 
* Robert A. Herrmann, _Nonstandard analysis and generalized functions_, [math.FA/0403303](http://arxiv.org/abs/math/0403303)

* Robert A. Hermann, _Nonstandard analysis applied to advanced undergraduate mathematics_, [math.GM/0312432](http://www.arXiv.org/abs/math.GM/0312432)

* A. E. Hurd, P. A. Loeb, _Introduction to nonstandard real analysis_, Acad. Press 1985. 

* Hans Vernaeve, _Nonstandard principles for generalized functions_, [arxiv/1101.6075](http://arxiv.org/abs/1101.6075)

* Imme van den Bergh, V&#237;tor Manuel Carvalho das Neves (eds.), _The strength of nonstandard analysis_, [gBooks](http://books.google.com/books?id=nWyPEAW16U8C)

* R. F. Hoskins, J. Sousa Pinto, _Theories of generalized functions_, Horwood Publ. 2005

* Imme van den Berg, _Nonstandard asymptotic analysis_, Lec. Notes Math. __1249__, Springer 1987

* Edward Nelson, _Radically elementary probability theory_

* Diener-Diener (eds.), _Nonstandard analysis in practice_

* Loeb-Wolff (eds.), _Nonstandard analysis for the working mathematician_

* [[Terry Tao]], _Ultraproducts as a bridge between discrete and continuous analysis_ ([web](http://terrytao.wordpress.com/2013/12/07/ultraproducts-as-a-bridge-between-discrete-and-continuous-analysis/))

* V. A. Lyubetski&#301;, _&#1054;&#1094;&#1077;&#1085;&#1082;&#1080; &#1080; &#1087;&#1091;&#1095;&#1082;&#1080;. &#1054; &#1085;&#1077;&#1082;&#1086;&#1090;&#1086;&#1088;&#1099;&#1093; &#1074;&#1086;&#1087;&#1088;&#1086;&#1089;&#1072;&#1093; &#1085;&#1077;&#1089;&#1090;&#1072;&#1085;&#1076;&#1072;&#1088;&#1090;&#1085;&#1086;&#1075;&#1086; &#1072;&#1085;&#1072;&#1083;&#1080;&#1079;&#1072; _, Uspekhi Mat. Nauk __44__ (1989), no. 4(268), 99--153, 256; translation _Valuations and sheaves. On some questions of non-standard analysis_, in Russian Math. Surveys __44__ (1989), no. 4, 37&#8211;112 [MR1023104](http://www.ams.org/mathscinet-getitem?mr=1023104) [doi](http://dx.doi.org/10.1070/RM1989v044n04ABEH002140) [IOP pdf](http://iopscience.iop.org/0036-0279/44/4/R03/pdf/0036-0279_44_4_R03.pdf) [rus pdf](http://www.mathnet.ru/php/getFT.phtml?jrnid=rm&paperid=1849&what=fullt&option_lang=rus)

* Bruno Dinis, _Nonstandard intuitionistic interpretations_, [arxiv/1512.07113](http://arxiv.org/abs/1512.07113)
* Sam Sanders, _The unreasonable effectiveness of nonstandard analysis_, [arxiv/1508.07434](http://arxiv.org/abs/1508.07434)
* V. Kanovei, _A course on foundations of nonstandard analysis_, (With a
preface by M. Reeken.), IPM, Tehran, Iran, 1994.
* V. Kanovei, M. Reeken, Internal approach to external sets and uni-
verses, Part 1, Bounded set theory, Studia Logica, 1995.

On the relation of the techniques of the pioneers of infinitesimal calculus and Robinson's nonstandard analysis:

* Piotr Blaszczyk, Vladimir Kanovei, Karin U. Katz, [[Mikhail Katz]], [[Semen S. Kutateladze]], David Sherry, *Toward a history of mathematics focused on procedures*, Foundations of Science **22** (2017) 763–783 &lbrack;[arxiv/1609.04531](http://arxiv.org/abs/1609.04531), [doi:10.1007/s10699-016-9498-3](https://doi.org/10.1007/s10699-016-9498-3)&rbrack;


[[!redirects hyperreal]]
[[!redirects hyperreal number]]
[[!redirects hyperreals]]
[[!redirects hyperreal numbers]]

[[!redirects non-standard analysis]]
[[!redirects NSA]]
