#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Nonstandard analysis is a richer formalization of [[analysis]] that uses a certain explicit notions of [[infinitesimal object]]s. In fact, not only infinitesimal but also infinitely large can be accomodated; moreover not only the field of [[real number]]s, but more general algebraic structures can be extended, essentially via a construction of [[ultraproducts]]; also general sets can be extended to contain nonstandard elements (see [[internal set]]). 

See also [[nonstandard analysis in topology]].


##Motivation##

At its beginning, infinitesimal calculus was developed nonrigorously, though many interesting arguments and formal manipulations were found. Cauchy and Weierstra&#223; introduced the $\epsilon$-$\delta$ approach, which enabled modern rigorous [[analysis]], but sometimes this method is cumbersome. For example, sometimes one needs to work with several infinitesimal levels or kinds of continuity in the same problem, and finding estimates may be very cumbersome. One would like to introduce infinitesimal quantities as additional elements of the sets of usual ('standard') quantities. Several related rigorous frameworks appeared under the name of __nonstandard analysis__, since the first such discovered by Abraham Robinson. Most often, approaches using [[ultrafilters]], certain classes called [[internal set]]s and using [[topos theory]] enable the foundation of nonstandard analysis. Many properties and theorems from ordinary mathematics imply new statements of nonstandard analysis; the mechanism is the so-called __transfer principle__, which can be required axiomatically without respect to a particular model of nonstandard analysis. 


##An approach via ultrafilters##

Assuming the [[axiom of choice]] (whose full strength is not necessary), there exists a free (= not containing finite subsets) [[ultrafilter]] $F$ on the set of [[natural numbers]] $\mathbb{N}=\{1,2,3,\ldots\}$, and such ultrafilters are in $1$--$1$ correspondence with finitely additive [[measure]]s on $\mathbb{N}$ (using the [[power set|algebra of all subsets]]) taking values in the two element set $\{0,1\}$.


Fix a free ultrafilter on $\mathbb{N}$, and consider the set of all [[sequences]] of real numbers, $\mathbb{R}^{\mathbb{N}}$. We write $f\sim_F g$ if the set $\{i\in\mathbb{N}|f(i)=g(i)\}$ belongs to $F$; these are precisely the sequences which are equal almost everywhere with respect to the associated measure. The relation $\sim_F$ is an [[equivalence relation] and ${}^*\mathbb{R} := \mathbb{R}^{\mathbb{N}}/{\sim_F}$ is a __nonstandard extension__ of $\mathbb{R}$, whose elements are sometimes called **hyperreal numbers**. This is a special case of the [[ultraproduct]] construction in [[model theory]]. Given $f\in \mathbb{R}^{\mathbb{N}}$, we write $f_F$ for its equivalence class in ${}^*\mathbb{R}$. In particular, given any real number $r\in \mathbb{R}$ the image $^* r :=(i\mapsto r)_F$ of the constant sequence $(r,r,r,\ldots)$ is an element in $^*\mathbb{R}$ and this gives an [[injection]] $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$. 


$^*\mathbb{R}$ is equipped with a linear ordering given by

$$
f_F\lt g_F \;\Leftrightarrow\; \{i\in\mathbb{N}|f(i)\lt g(i)\}\in F,
$$

which makes $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$ a [[monotone function]]. An element $\delta\in{}^*\mathbb{R}$ such that $^* 0\lt\delta$ is called a __positive number__; an element $\delta$ such that $^* r\lt\delta\lt{}^* r$ for all $r\in \mathbb{R}$ such that $r\gt 0$ is called an __infinitesimal number__. Unlike in the real numbers, positive infinitesimal numbers exist: for example the class $f_F$ where $f:n\mapsto 1/n$ is such and $g_F$ for $g:n\mapsto 1/n^2$ is a different one. 


Let $n$ be a nonnegative integer and $u:\mathbb{R}^n\to\mathbb{R}$ a function. Then there is nonstandard extension $^* u:({}^*\mathbb{R})^n\to{}^*\mathbb{R}$ of $f$; it is defined by

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


Conversely, an element $x\in{}^*\mathbb{R}$ is __finite__ if $|x|\lt {}^* r$ for some $r\in\mathbb{R}$. Every finite element $x\in{}^*\mathbb{R}$ is infinitely close to a unique real number $q\in\mathbb{R}$ in the sense that $x-{}^*q$ is infinitesimal. We say that $q$ is the __standard part__ of $x$ and is denoted by $q= st(x)$. Given a real number $r\in\mathbb{R}$, the subset $\mu(r)$ of all elements $x\in{}^*\mathbb{R}$ such that $st(x)=r$ is said to be the __monad__ of the real number $r\in\mathbb{R}$. Monads should be thaught of as infinitesimal neighborhoods. An elementary fact:
a subset $E\subset\mathbb{R}$ is open iff $\mu(r)\subset{}^*E$ for all $r\in E$; $E$ is closed iff $st(x)\in E$ for all finite $x\in{}^* E$; and $E$ is [[compact space|compact]] iff, for all $x\in{}^* E$, $x$ is finite and $st(x)\in E$. 


In this model of nonstandard analysis a version of the transfer principle (in terms of certain formal language $L(\mathbb{R})$) is established as a corollary of a general theorem on ultraproducts due Jerzy &#321;o&#347;.  

#References#

* Sergio Albeverio, Jens Erik Fenstad, Raphael Hoegh-Krohn, _Nonstandard methods in stochastic analysis and mathematical physics_, Academic Press 1986 (there is also a Dover 2009 edition and a 1990 Russian translation)

* Jerome Keisler, _Elementary calculus: an infinitesimal approach_, [online](http://www.math.wisc.edu/~keisler/calc.html) undergraduate textbook.

* Wikipedia: [nonstandard analysis](http://en.wikipedia.org/wiki/Non-standard_analy), [ultraproduct](http://en.wikipedia.org/wiki/Ultraproduc), [hyperreal numbers](http://en.wikipedia.org/wiki/Hyperreal_numbers), [Abraham Robinson](http://en.wikipedia.org/wiki/Abraham_Robinson)

There is a realizatiion of aspects of nonstandard analysis in some models of [[synthetic differential geometry]]. See chapter 6 of

* [[Ieke Moerdijk]] and [[Gonzalo Reyes]], [[Models for Smooth Infinitesimal Analysis]]