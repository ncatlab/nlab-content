
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Mathematics
+-- {: .hide}
[[!include mathematicscontents]]
=--
=--
=--

# Contents
* table of contents 
{: toc}


## Idea 

In [[classical mathematics]], a _countable_ [[ordinal]] is the [[order type]] of a [[well ordering|well-ordered]] [[set]] whose [[cardinality]] is countable (i.e., either [[finite set|finite]] or [[natural numbers|denumerable]]). 

Countable ordinals play an important role in [[recursion]] theory, [[computability theory]], and in [[proof theory]], where they are used for example to measure the [[consistency]] strength of formal [[theories]] via [[ordinal analysis]]. They also play a role in [[philosophy of mathematics]], for example to discuss what it means for a notion to be "[[predicativity|predicative]]". 

## Definitions 

As indicated above, countable ordinals can be defined structurally as countable well-ordered sets (or "[[wosets]]"). As is the case with any ordered set, a woset $W$ can be regarded as a [[coalgebra over an endofunctor|coalgebra]] over the covariant [[power-set]] functor, 

$$\theta: W \to P(W)$$ 

$$\,$$ 

$$x \mapsto \{y: y \lt x\}.$$ 

A coalgebra map $f: W \to W'$ between wosets, aka a [[simulation]], amounts to an inclusion of the domain as an initial segment of the codomain. 

The [[category]] of countable wosets and simulations, thus ordered by inclusion, is a [[preorder]] and in fact equivalent to a woset. In [[material set theory]], this woset is often identified with the [[first uncountable ordinal]] (well-ordered set under the membership relation), often denoted $\omega_1$. [[structural set theory|Structurally]], we can define $\omega_1$ up to [[isomorphism]] as a [[skeleton]] of the category of countable ordinals, and so the study of countable ordinals becomes a study of the order structure of $\omega_1$. 

This $\omega_1$ has no top element (of course not: otherwise $\omega_1$ would be a countable ordinal), and much of the interest and fun of the subject lies in playing the childhood game of seeing who can name the bigger number, or in this case the bigger countable ordinal. A key fact is that $\omega_1$ is countably cocomplete, and therefore behaves like a self-contained [[universe]] with respect to countably cocontinuous operations. There is quite a lot of scope in what one can build up to using such operations. After playing the larger ordinal game for a while, and becoming impressed by the sizes of ordinals one can define -- while recognizing at the same time that one is "never getting anywhere" relative to $\omega_1$ itself -- it is hard not to become awestruck by the staggering immensity of $\omega_1$. 

Anyone who is unimpressed by the size of large countable ordinals has almost surely never seriously played with them. For that matter, people who are unimpressed by large _finite_ numbers have probably never played around with them either, or at least not all that imaginatively! (And interestingly, one can use large countable ordinals reflectively to construct enormous integers, or one can use large [[uncountable ordinals]] reflectively to construct enormous countable ordinals.) 


## Fixed points and the Veblen hierarchy 


Here we discuss the use of [[fixed point]] theory in describing the lower stages of the Veblen hierarchies of countable ordinals, which will lead up to the Feferman-Sch&#252;tte ordinal. We freely allow ourselves to reason classically and use the [[principle of excluded middle]]. 

The ordinal $\omega_1$ is countably [[cocomplete category|cocomplete]], and we are primarily interested in functors or order-preserving maps $f: \omega_1 \to \omega_1$ that preserve [[colimits]] of countable (finite or denumerable) diagrams -- or countable chains, without loss of generality. We'll call such maps _continuous_, for short. If $x \leq f(x)$ for all $x \in \omega_1$, then we say that $f$ is _inflationary_. 

Preservation of colimits of finite nonempty chains comes for free, so we can ignore that. The colimit of the empty chain is the bottom element $0$, and we will make a point of including preservation of that. 

The first result is a baby form of a general theorem due to [[Adamek|Adámek]] on [[initial algebras of endofunctors]]. 

+-- {: .num_prop #fix} 
###### Proposition 
Suppose $f: \omega_1 \to \omega_1$ is inflationary and continuous. Then every $x \in \omega_1$ has an upper bound that is a fixed point under $f$. 
=-- 

+-- {: .proof} 
###### Proof 
For any $x$, the colimit $x'$ of $x \leq f(x) \leq f^2(x) \leq \ldots$ exists, and since $f$ preserves countable colimits, $x'$ is a fixed point of $f$. 
=-- 

+-- {: .num_lemma} 
###### Lemma 
If $f: \omega_1 \to \omega_1$ is order-preserving and satisfies $f(\beta) = \sup \{f(\alpha): \alpha \lt \beta\}$ for all limit (i.e., non-successor) ordinals $\beta$, then $f$ is continuous. 
=-- 

The converse of this result is trivially true. 

+-- {: .proof} 
###### Proof 
For the case $\beta = 0$, the set $\{f(\alpha): \alpha \lt \beta\}$ is empty and thus has $0$ as its supremum, so $f(0) = 0$. 

Suppose that $\beta$ is the colimit of a chain $x_1 \leq x_2 \leq \ldots$ with countably infinite image. Then this chain is [[cofinal functor|cofinal]] in the set $\{\alpha: \alpha \lt \beta\}$, and similarly $f(x_1) \leq f(x_2) \leq \ldots$ is cofinal in $\{f(\alpha): \alpha \lt \beta\}$. Therefore the colimit of this chain is the same as the [[supremum]] of $\{f(\alpha): \alpha \lt \beta\}$, which is $f(\beta)$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Suppose $f: \omega_1 \to \omega_1$ is inflationary and continuous. Define $f': \omega_1 \to \omega_1$ to be the function that takes each $x \in \omega_1$ to the least fixed point of $f$ that is greater than $f'(y)$ for all $y \lt x$. Then $f'$ is also inflationary and continuous. 
=-- 

+-- {: .proof} 
###### Proof 
By definition, $f'(y) \lt f'(x)$ whenever $y \lt x$, so $f'$ is order-preserving. That $f'$ is inflationary is proved by [[induction]]: given that $\alpha \leq f'(\alpha)$ for all $\alpha \lt \beta$, we have $\alpha \leq f'(\alpha) \lt f'(\beta)$ i.e. $\alpha \lt f'(\beta)$ for all $\alpha \lt \beta$, whence $\beta \leq f'(\beta)$. To prove $f'$ is continuous, let $\beta$ be a non-successor; by continuity of $f$ we have 

$$f(\sup \{f'(\alpha): \alpha \lt \beta\}) = \sup \{f(f'(\alpha)): \alpha \lt \beta\} = \sup \{f'(\alpha): \alpha \lt \beta\}$$ 

so that this supremum is in fact a fixed point of $f$, and thus the least fixed point of $f$ greater than every $f'(\alpha)$ for $\alpha \lt \beta$. It therefore follows by definition of $f'$ that 

$$f'(\beta) = \sup \{f'(\alpha): \alpha \lt \beta\}$$ 

and so, by the preceding lemma, $f'$ is continuous. 
=-- 

+-- {: .num_defn} 
###### Definition 
The _Veblen hierarchy_ is a family of functions $f_\alpha: \omega_1 \to \omega_1$, one for each $\alpha \in \omega_1$, defined as follows. 

* Define $f_0: \omega_1 \to \omega_1$ by $f_0(x) = \sup \{y+2: y \lt x\}$. 

This is inflationary, and continuous by the lemma. 

* Then define $f_\alpha: \omega_1 \to \omega_1$ by $f_{\alpha + 1} = f_\alpha^'$ and $f_\beta = \sup_{\alpha \lt \beta} f_\alpha$ at limit ordinals $\beta \gt 0$. 

By induction and the preceding proposition, $f_\alpha$ is inflationary and continuous at successor cardinals $\alpha$, and also at limit cardinals $\alpha \gt 0$ since countable colimits of inflationary and continuous maps are also inflationary and continuous.  
=-- 

It is worth contemplating the growth of the first few $f_\alpha$. For $f_0$, we have $f_0(\alpha) = \alpha + 1$ if $\alpha$ is a successor, and $f_0(\alpha) = \alpha$ if $\alpha$ is a limit ordinal. 

This means that next we have $f_1(0) = 0$, $f_1(1) = \omega$, $f_1(2) = 2 \omega$, ..., $f_1(\omega) = \omega^2$, and so on. The first fixed point past $0$ is at $x = \omega^\omega$. 

Next, we have $f_2(0) = 0$, $f_2(1) = \omega^\omega$, $f_2(2) = \omega^{2\omega}$, ..., $f_2(\omega) = \omega^{\omega^2}$, and so on. The first fixed point past $0$ is the same as the first fixed point of $x \mapsto \omega^x$ (a countably iterated exponential stack), typically denoted as $\epsilon_0$. 

We pause to note that $\epsilon_0$ is sometimes considered the first reasonable thing to call a "large countable ordinal". An [[ordinal analysis]] first carried by by Gerhard Gentzen asserts, roughly speaking, that the consistency of [[Peano arithmetic]] is provable from [[primitive recursive arithmetic]] (which is weaker than PA) augmented by the principle of induction up to $\epsilon_0$. 

Pressing on, we have $f_3(0)= 0$, $f_3(1) = \epsilon_0$, $f_3(2) = \epsilon_1$ (the first fixed point of $x \mapsto \omega^x$ past $\epsilon_0$), and so on. The first fixed point past $0$ of $f_3$ is the limit of $\epsilon_0, \epsilon_{\epsilon_0}, \epsilon_{\epsilon_{\epsilon_0}}, \ldots$, sometimes indicated by an infinite descending stack of subscripts $\epsilon$. This ordinal is of size that far, far surpasses any human powers of visualization. 

And clearly we are only just getting started. Each successive $f_n(1)$ dwarfs its predecessor $f_{n-1}(1)$ to an indescribable degree. To speak nothing of $f_\omega(1)$, and so on. 

## Ordinal notations and the Feferman-Sch&#252;tte ordinal 

Despite such colossal sizes, it is possible to effectively notate such ordinals using nothing more than finite binary trees, all the way up to the Feferman-Sch&#252;tte ordinal, which seems to be the first of the "large countable ordinals" that the experts consider big enough to honor with human names. (There are others much further down the pike, such as the Bachmann-Howard ordinal or the considerably larger, almost godlike Church-Kleene ordinal.) 

Before introducing this, we prove the following lemmas. 

+-- {: .num_lemma} 
###### Lemma 
If $\alpha \lt \beta$, then every value $f_\beta(x)$ is a fixed point of $f_\alpha$. 
=-- 

+-- {: .proof} 
###### Proof 
This is clear if $\alpha + 1 = \beta$. Suppose $f_\gamma(x)$ is a fixed point of $f_\alpha$ whenever $\alpha \lt \gamma \lt \beta$. If $\beta$ is a successor $\gamma + 1$, then we have 

$$f_\beta(x) = f_\gamma(f_\beta(x)) = f_\alpha(f_\gamma(f_\beta(x))) = f_\alpha(f_\beta(x)),$$ 

and if $\beta$ is a limit, then 

$$f_\alpha(f_\beta(x)) = f_\alpha(\sup_{\alpha \lt \gamma \lt \beta} f_\gamma(x)) = \sup_{\alpha \lt \gamma \lt \beta} f_\alpha(f_\gamma(x)) = \sup_{\alpha \lt \gamma \lt \beta} f_\gamma(x) = f_\beta(x)$$ 

which completes the proof. 
=-- 

+-- {: .num_lemma #inflat} 
###### Lemma 
For all $y \in \omega_1$, we have $y \leq f_y(1)$. 
=-- 

+-- {: .proof} 
###### Proof 
By induction. Suppose $\alpha \leq f_\alpha(1)$ for all $\alpha \lt \beta$. Since $1 \leq f_\beta(1)$, we have 

$$\alpha \leq f_\alpha(1) \leq f_\alpha(f_\beta(1)) = f_\beta(1)$$ 

since $f_\beta(1)$ is by the preceding lemma a fixed point of $f_\alpha$. Since $f_\beta(1)$ is both a limit ordinal and an upper bound for every $\alpha \lt \beta$, it follows that $\beta \leq f_\beta(1)$. 
=-- 

Notice that by definition, $f_\beta(\gamma)$ is continuous in the argument $\beta$, since we defined $f_\beta = \sup_{\alpha \lt \beta} f_\alpha$ at limit ordinals $\beta$. Therefore the function $x \mapsto f_x(1)$ is inflationary (by lemma \ref{inflat}) and continuous. Applying proposition \ref{fix}, it has a least fixed point. This fixed point is called the **Feferman-Sch&#252;tte ordinal**, denoted by $\Gamma_0$. 

+-- {: .num_theorem} 
###### Theorem 
If $\alpha \gt 0$ is less than $\Gamma_0$, then there exist $\beta, \gamma$, both less than $\alpha$, such that $\alpha = f_\beta(\gamma)$. 
=-- 

+-- {: .proof} 
###### Proof 
If $\alpha$ is not a limit ordinal, then $\alpha = \gamma + 1$ and hence $\alpha = f_0(\gamma)$. Obviously $\alpha$ cannot be a value of $f_\beta$ for $\beta \gt 0$, since all such values are limit ordinals. 

If $\alpha$ is a limit ordinal and $\alpha \lt \Gamma_0$, then there is some $\beta \lt \alpha$ for which $\alpha$ is _not_ a fixed point of $f_\beta$. Otherwise we would have $f_\beta(\alpha) = \alpha$ for all $\beta \lt \alpha$, and this would force $f_\alpha(\alpha) = \alpha$ (by definition of $f_\alpha$). And in that case 

$$\alpha \leq f_\alpha(1) \leq f_\alpha(\alpha) = \alpha$$ 

so that $\alpha$ is a fixed point of $x \mapsto f_x(1)$, contradicting $\alpha \lt \Gamma_0$. 

Thus, for $\alpha$ a limit ordinal, take $\beta$ to be the least ordinal such that $\alpha \lt f_\beta(\alpha)$. Note that $\beta$ is a successor, $\beta = \beta' + 1$, because we have $\alpha = f_\gamma(\alpha)$ for any $\gamma \lt \beta$, and this would imply $\alpha = f_\beta(\alpha)$ if $\beta$ were a limit. 

We have $\alpha \leq f_\beta(\gamma)$ for some $\gamma \lt \alpha$ (for if $f_\beta(\gamma) \lt \alpha$ for all $\gamma \lt \alpha$, we could infer $\alpha$ is a fixed point of $f_\beta$). Let $\gamma$ be the least ordinal (less than $\alpha$) such that $\alpha \leq f_\beta(\gamma)$. Then in fact this last inequality is an equality. For suppose $\gamma = \delta + 1$; then by definition of $\gamma$, we have 

$$f_\beta(\delta) = f_{\beta' + 1}(\delta) \lt \alpha$$ 

and we also have that $\alpha = f_{\beta'}(\alpha)$ by definition of $\beta$. Since $f_\beta(\gamma) = f_{\beta' + 1}(\gamma) = f_{\beta' + 1}(\delta + 1)$ is by definition the least $f_{\beta'}$-fixpoint greater than $f_{\beta' + 1}(\delta)$, we immediately infer $f_\beta(\gamma) \leq \alpha$, as required. If on the other hand $\gamma$ is a limit, we have 

$$f_\beta(\delta) \lt \alpha$$ 

for all $\delta \lt \gamma$, and we again infer $f_{\beta}(\gamma) \leq \alpha$, as required. 
=-- 

This theorem gives a canonical finite binary tree representation of any $\alpha \lt \Gamma_0$, by recursion. The binary tree $\tau(0)$ of $0$ consists of just $0$ as root, with no child-pair. Given that every $\beta$ less than $\alpha$ has been assigned a binary tree $\tau(\beta)$, we define $\tau(\alpha)$ to have the child-pair $(\tau(\beta), \tau(\gamma))$ where 

* $\beta$ is the least ordinal less than $\alpha$ such that $\alpha \lt f_\beta(\alpha)$, and 

* $\gamma$ is the least ordinal less than $\alpha$ such that $\alpha \leq f_\beta(\gamma)$. 

The resulting binary tree $\tau$ is finite for every $\alpha \lt \Gamma_0$, since it has binary branching and there are no infinite branches or paths up the tree (since that would yield an infinite descent $\alpha \gt \alpha_1 \gt \alpha_2 \gt \ldots$ with no least element, contradicting well-orderedness). 

This finite binary tree notation is one of many possible ordinal notations for naming countable ordinals. It is more expressive the Cantor normal form that provides a notation for ordinals $\alpha$ less than $\epsilon_0$, where one writes $\alpha$ uniquely in the form 

$$\alpha = \omega^\beta + \gamma$$ 

with $\beta, \gamma \lt \alpha$ and $\gamma \lt \gamma + \omega^\beta$, and continues recursively. 

+-- {: .num_remark} 
###### Remark 
However, Cantor normal form has the virtue of uniqueness. For the binary operation $(\beta, \gamma) \mapsto f_\beta(\gamma)$, it is possible to have two distinct pairs $(\beta, \gamma)$, $(\beta', \gamma')$ which are equivalent in the sense that 

$$f_\beta(\gamma) = f_{\beta'}(\gamma');$$ 

we counteracted this by using the pair $(\beta, \gamma)$ which was least in its equivalence class with respect to [[lexicographic order]]. 
=-- 

## Fundamental sequences and the Bachmann-Howard ordinal 

### Fast-growing functions on $\mathbb{N}$ 

## Recursive ordinals 

Of course, having reached $\Gamma_0$ as the least fixed point of $x \mapsto f_x(1)$, there is nothing stopping one from starting all over again with a new Veblen hierarchy, defining $g_0(x) = f_x(1)$ and defining $g_\alpha$ analogously to how we defined $f_\alpha$. 

In one or another way we can continue extending ordinal notation schemes, but all such schemes are recursive by definition, and at some point we cannot go any further: 

+-- {: .num_defn} 
###### Definition 
A countable ordinal $\alpha$ is **recursive** if there is a computable relation on $\mathbb{N}$ (or a [[recursive subset]] of $\mathbb{N} \times \mathbb{N}$) that well-orders $\mathbb{N}$, so that the resulting woset is isomorphic to $\alpha$. 
=-- 

There are countably many computable relations on $\mathbb{N}$, and so the supremum of the recursive ordinals in $\omega_1$ exists. It is called the **Church-Kleene ordinal**. It is the first non-recursive ordinal. 

## Related concepts

* [[uncountable ordinal]]
* [[countable set]]
* [[ordinal analysis]]

## References 

For a light-hearted introduction with many useful references, see 

* [[John Baez]], Week 236, This Week's Finds in Mathematical Physics, July 26, 2006. ([web](http://math.ucr.edu/home/baez/week236.html)) 

A very readable account of countable ordinals up to the Feferman-Sch&#252;tte ordinal is 

* Jean Gallier, *What's so Special about Kruskal's Theorem and the Ordinal $\Gamma_0$?, A Survey of Some Results in Proof Theory*, Annals of Pure and Applied Logic, Vol. 53, 199-260 (1991). ([Part II](ftp://ftp.cis.upenn.edu/pub/papers/gallier/kruskal2.pdf)) 

An application of coalgebra theory to ordinal notation systems is described here: 

* Peter Hancock, Ordinal notation systems. ([web](http://homepages.inf.ed.ac.uk/v1phanc1/ordinal-notations.html)) 

[[ordinal analysis|Ordinal analysis]] as measuring consistency strengths of theories is well-described in this paper: 

* [[Michael Rathjen]], The art of ordinal analysis, International Congress of Mathematicians, II, Eur. Math. Soc., Zurich, pp. 45&#8211;69. ([pdf](http://www.icm2006.org/proceedings/Vol_II/contents/ICM_Vol_2_03.pdf)) 

[[!redirects countable ordinals]]

