##Motivation##

At the beginning infinitesimal calculus was developed nonrigorously though many interesting arguments in formal manipulations were found. Cauchy introduced $\epsilon$-$\delta$ approach which enabled modern analysis, but sometimes this method is cumbersome. For example, sometimes one needs to work with several infinitesimal levels, or kinds of continuity in the same problem and finding estimates is very cumbersome. One would like to introduce infinitesimal quantities as additional elements in the sets of usual quantities. Several related rigorous frameworks appeared under the name __nonstandard analysis__, since the first such discovered by Robinson. Most often approaches using ultrafilters, certain classes called [[internal set]]s and using topos theory enable the foundation of nonstandard analysis. Many properties and theorems from usual mathematics imply new statements of nonstandard analysis, and the mechanism is so-called __transfer principle__ which can be required axiomatically without respect to a particular model of nonstandard analysis. 

##An approach via ultrafilters##

Assuming [[axiom of choice]] there exist a free (= not containing finite subsets) [[ultrafilter]] $F$ on the set of natural numbers $\mathbb{N}=\{1,2,3,\ldots\}$. Such ultrafilters are in 1-1 correspondence with finitely additive [[measure]] on $\mathbb{N}$ taking values in the two element set $\{0,1\}$. Consider the set of all [[sequences]] of real numbers $\mathbb{R}^{\mathbb{N}}$. We write $f\sim_F g$ if the set $\{i\in\mathbb{N}|f(i)=g(i)\}\in F$. These are precisely the sequences which are equal almost everywhere with respect to the associated measure. Relation $\sim_F$ is a relation of equivalence and ${}^*\mathbb{R} := \mathbb{R}^{\mathbb{N}}/\sim_F$ is a nonstandard extension of $\mathbb{R}$ and its elements are sometimes called **hyperreal numbers**. Given $f\in \mathbb{R}^{\mathbb{N}}$, we write $f_F$ for its equivalence class in ${}^*\mathbb{R}$. In particular given any real number $r\in \mathbb{R}$ the image $^* r :=(i\mapsto r)_F$ of the constant sequence $(r,r,r,\ldots)$ is an element in $^*\mathbb{R}$ and this gives an injection $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$. 

$^*\mathbb{R}$ is equipped with a linear ordering given by

$$
f_F\lt g_F \Leftrightarrow \{i\in\mathbb{N}|f(i)\lt g(i)\}\in F,
$$

which makes $*:\mathbb{R}\hookrightarrow {}^*\mathbb{R}$ a [[monotone function]]. An element $\delta\in{}^*\mathbb{R}$ such that $^* 0\lt\delta\lt{}^* r$ for all $r\in \mathbb{R}$ such that $r\gt 0$ is called a positive __infinitesimally small number__. Infinitesimally small numbers exist: for example the class $f_F$ where $f:n\mapsto 1/n$ is such and $g_F$ for $g:n\mapsto 1/n^2$ is a different such class. 

Let $n$ be a nonnegative integer and $u:\mathbb{R}^n\to\mathbb{R}$ a function. Then there is nonstandard extension $^* u:({}^*\mathbb{R})^n\to{}^*\mathbb{R}$ of $f$ 
is defined by

$$
*u(f^1_F,\ldots, f^n_F) = g \Leftrightarrow \{i\in\mathbb{N}| u(f^1(i),\ldots,f^n(i))=g(i) \}\in F.
$$

This is indeed an extension of $u$ in the sense that $^* u({}^r_1,\ldots,{}^*r_n)={}^* r$ iff $u(r_1,\ldots,r_n)=r$.
This way, the usual operations $+,\cdot$ and the absolute value $|\cdot|$ extend to $^*\mathbb{R}$; usually one denotes these standard three operations on ${}*\mathbb{R}$ without putting $^*$ in front, writing simply e.g. $f_F+g_F$. (To extend appropriately the division we need a little bit more care as it is originally just partially defined, so we need an extension of the formalism to subsets of real line.) 

An element $x\in{}^*\mathbb{R}$ is *finite* if $|x|\lt {}^* r$ for some $r\in\mathbb{R}$. Every finite element $x\in{}^*\mathbb{R}$ is infinitesimally close to a unique real number $q\in\mathbb{R}$ in the sense that $|x-{}^*r|$ is either $0$ or a positive infinitesimally small number. We say that $q$ is the __standard part__ of $x$ and is denoted by $q= st(x)$. Given a real number $r\in\mathbb{R}$, the subset $\mu(r)$ of all elements $x\in{}^*\mathbb{R}$ such that $st(x)=r$ is said to be the __monad__ of the real number $r\in\mathbb{R}$.

* Sergio Albeverio, Jens Erik Fenstad, Raphael Hoegh-Krohn, _Nonstandard methods in stochastic analysis and mathematical physics_, Academic Press 1986 (there is also a Dover 2009 edition and a 1990 Russian translation)