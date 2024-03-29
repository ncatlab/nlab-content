
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


# The Mean Value Theorem
* table of contents
{: toc}

## Idea {#idea}

The motivating idea of the [[derivative]] in [[differential calculus]] is that it is approximated by a [[ratio]] of differences.  We may also say that an instantaneous rate of change is approximated by an average rate of change.  The Mean Value Theorem (MVT) reverses this, and says that any average rate of change is equal to some instantaneous rate of change, if certain differentiability conditions are met.

The name comes from the fact that, due to the [[fundamental theorem of calculus]], an average rate of change over an [[interval]] may be viewed as an average (or [[mean]]) of the instantaneous rates of change along the interval.  Thus, the theorem states that the mean value of the derivative on an interval is attained somewhere in that interval.


## Statements {#statement}

There are traditionally three versions of increasing generality, although even the most general version is implicit in the most specific version (requiring only a linear coordinate transformation).

+-- {: .num_theorem #rolle}
###### Rolle\'s Theorem

Suppose that $a \lt b$ are [[real numbers]] and $f$ is a [[continuous map|continuous]] [[real number|real]]-valued [[function]] on $[a,b]$.  If $f$ is [[differentiable function|differentiable]] on the [[interior]] $]{a,b}[$, and if $f(a) = f(b)$, then for some $c \in {]{a,b}[}$,
$$ f'(c) = 0 .$$
=--

+-- {: .num_theorem #lagrange}
###### Lagrange\'s Theorem

Suppose that $a \lt b$ are [[real numbers]] and $f$ is a [[continuous map|continuous]] [[real number|real]]-valued [[function]] on $[a,b]$.  If $f$ is [[differentiable function|differentiable]] on the [[interior]] $]{a,b}[$, then for some $c \in {]{a,b}[}$,
$$ f'(c) = \frac {f(b) - f(a)} {b - a} ,$$
or equivalently
$$ f'(c) (b - a) = f(b) - f(a) .$$
=--

+-- {: .num_theorem #cauchy}
###### Cauchy\'s Theorem

Suppose that $a \lt b$ are [[real numbers]] and $f$ and $g$ are [[continuous map|continuous]] real-valued [[functions]] on $[a,b]$.  If $f$ and $g$ are [[differentiable function|differentiable]] on the interior $]{a,b}[$, then for some $c \in {]{a,b}[}$,
$$ f'(c) (g(b) - g(a)) = g'(c) (f(b) - f(a)) ;$$
assuming that $f'$ and $g'$ are never simultaneously zero in $]{a,b}[$ and that $(f(a),g(a)) \neq (f(b),g(b))$, then for some $c \in {]{a,b}[}$,
$$ \frac {f'(c)} {g'(c)} = \frac {f(b) - f(a)} {g(b) - g(a)} ,$$
where either side of this equation is allowed to be interpreted as $\infty$ in case it is division by zero (necessarily with a nonzero dividend under these conditions); or perhaps better, an equality of [[ratio]]s:
$$ f'(c) : g'(c) :: f(b) - f(a) : g(b) - g(a) .$$
=--

If we write $u$ for $f(x)$ and $v$ for $g(x)$, then this last version states that
$$ \left.{\frac{\mathrm{d}u}{\mathrm{d}v}}\right|_{x=c} = \left.{\frac{\Delta{u}}{\Delta{v}}}\right|_{x=a}^b .$$
Compare this to the definition
$$ \left.{\frac{\mathrm{d}u}{\mathrm{d}v}}\right|_{x=a} \coloneqq \lim_{b\to{a}} \left.{\frac{\Delta{u}}{\Delta{v}}}\right|_{x=a}^b $$
(although this is really only a *definition* when $v$ is $x$, which reduces Cauchy\'s theorem to Lagrange\'s).


## Naming

Rolle\'s theorem is usually called just 'Rolle\'s' theorem, being the only result attributed today to [[Michel Rolle]]; but Lagrange\'s and Cauchy\'s theorems must be called 'mean value' theorems, as [[Joseph-Louis Lagrange]] and [[Augustin-Louis Cauchy]] did far more.  By default, the term 'Mean Value Theorem' usually refers to Lagrange\'s theorem.  (But neither Rolle nor Lagrange proved their theorem in the general case; the first proofs of all of them are due to Cauchy in 1823, a decade after Lagrange\'s death and more than a century after Rolle\'s death.)


## Mean-value inequalities

One consequence of these mean-value theorems if that if the relevant derivatives (or ratios of derivatives) are bounded, then the corresponding differences (or ratios of differences) will also be bounded.  We state this for Lagrange\'s theorem, although there are versions that correspond more to Rolle\'s or Cauchy\'s.

+-- {: .num_theorem #inequality}
###### The Mean-Value Inequality aka the Law of Bounded Change

Suppose that $a \lt b$ are [[real numbers]] and $f$ is a [[continuous map|continuous]] [[real number|real]]-valued [[function]] on $[a,b]$.  If $f$ is [[differentiable function|differentiable]] on the [[interior]] $]{a,b}[$, and we have $m \leq f' \leq M$ on $]{a,b}[$ for some constants $m$ and $M$, then
$$ m \leq \frac {f(b) - f(a)} {b - a} \leq M .$$
A slightly weaker statement is
$$ {|{f(b) - f(a)}|} \leq {|{b - a}|} \, \sup_{]{a,b}[} {|{f'}|} ,$$
which is true even if the derivative is unbounded (in which case the right-hand side is [[infinity|infinite]]).
=--

In [[constructive mathematics]], the mean-value theorems generally cannot be proved, since it may be impossible to find the value $c$ (although some variations with stronger hypotheses or weaker conclusions can often be proved, similarly to the [[Intermediate-Value Theorem]]).  However, the mean-value inequality is true in constructive mathematics, as long as $f$ is [[uniformly differentiable map|uniformly differentiable]] on every closed subinterval of $]{a,b}[$ (as is typical).

The second form of the mean-value inequality shows the relationship of differentiability to [[Lipschitz continuity]]: a continuous function on an interval with bounded derivative on the interior of the interval is Lipschitz continuous on that interval (and the [[supremum]] of the [[absolute value]] of the [[derivative]] is the [[Lipschitz constant]]).


## References {#refs}

* Wikipedia, _[Mean value theorem](http://en.wikipedia.org/wiki/Mean_value_theorem)_

* nForum discussion of [constructive versions](https://nforum.ncatlab.org/discussion/5574/constructive-mean-value-theorem/)


[[!redirects mean value theorem]]
[[!redirects mean value theorems]]
[[!redirects Mean Value Theorem]]
[[!redirects Mean Value Theorems]]
[[!redirects mean-value theorem]]
[[!redirects mean-value theorems]]
[[!redirects Mean-value Theorem]]
[[!redirects Mean-value Theorems]]
[[!redirects Mean-Value Theorem]]
[[!redirects Mean-Value Theorems]]
[[!redirects MVT]]

[[!redirects Rolle's theorem]]
[[!redirects Rolle theorem]]
[[!redirects Rolle's Theorem]]
[[!redirects Rolle Theorem]]

[[!redirects mean value inequality]]
[[!redirects mean value inequalities]]
[[!redirects Mean Value Inequality]]
[[!redirects Mean Value Inequalities]]
[[!redirects mean-value inequality]]
[[!redirects mean-value inequalities]]
[[!redirects Mean-value Inequality]]
[[!redirects Mean-value Inequalities]]
[[!redirects Mean-Value Inequality]]
[[!redirects Mean-Value Inequalities]]
