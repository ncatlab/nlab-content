A periodic map is a self-map of a [[spectrum]] $X$ of the form
$$\Sigma^d X \xrightarrow{f} X$$
for some $d \geq 0$, the condition of periodicity is that, when we iterate $f$, no $\Sigma^{t d}X$ is null homotopic.  (note that it's increasing dimension by d):
$$ ... \to \Sigma^{2d} X \xrightarrow{\Sigma^d f} \Sigma^d X \xrightarrow{f} X$$ 

A related concept: If $\exists t$ s.t. $\Sigma^{t d} X$ is null homotopic, then $f$ is instead called a nilpotent map.

##A verbose introduction to periodic maps##

Let us take the mindset of a harmonic analyst as we are handed one period of an interesting function $S^d X \xrightarrow{v} X$. Our first inclination is to shift this map a step $d$ to the left and lay them next to each other, ad infinitum.

$$... \xrightarrow{S^{3d} v} S^{3d} X \xrightarrow{S^{2d}v} S^{2d} X \xrightarrow{S^d v} S^d X \xrightarrow{v} X$$

for notational simplicity:

$$... \xrightarrow{v^4} S^{3d} X \xrightarrow{v^3} S^{2d} X \xrightarrow{v^2} S^d X \xrightarrow{v} X$$

If, when we iterate $v$ enough times, we find ourselves looking at a sad contractible space, tired by our repetitive antics, shriveled to a point, we quite naturally call $v$ nilpotent. But we are harmonic analysts -- seekers of periodicity! We wish to look at $v$ which do not die when we suspend them over and over, those that are periodic with period $d$. So...in what case does $v$ not die?

With $v$ on our mind we look at an element $f$ in the homotopy classes of maps from $S^k X$ to $Y$, represented by the map:

$$S^k X\xrightarrow{f} Y$$

How do we fit this together with our self map $v$?
$$S^d X \xrightarrow{v} X$$
We shift $v$ 
$$S^d(S^k X) \xrightarrow{S^k v} (S^k X)$$
and lay it in place next to $f$.
$$... \xrightarrow{S^k v^3} S^{2d}(S^k X) \xrightarrow{S^k v^2} S^d(S^k X) \xrightarrow{S^k v}(S^k X) \xrightarrow{f} Y$$

We might look at this collection of maps,

$$S^{j d}(S^k X) \xrightarrow{f \circ S^k v^j} Y$$

In slightly more palatable notation, we're looking at the collection $v^j f \in [S^{j d+k} X, Y]$ as $j$ ranges over the natural numbers -- forbidding ourselves from looking at $v$ if $v^j$ is constant for any $j$.

Why limit ourselves to $S^{j d+k}$? Let us look at all $S^* := {S^n}_{n \in \mathbb{Z}}$, that is, we look at the set $v^j f \in [S^* X, Y]$ (still demanding that all $v^j f$ are nontrivial):

$$\{f, v f, v^2f, ...\}$$

We name this set of $v$-periodic elements in $[S^*X, Y]$ a "$v$-periodic family"

**Note**: The $v_n$-periodic families are not actually periodic in $\pi_*^S$, they are maps *induced* by periodic maps between CW-complexes. 

##Examples of periodic maps##

See [[toda-smith complex]].

An example motivating the study of periodic maps: the bott element in $ku$. (I'm not sure that this is entirely correct).


$$S^2 \xrightarrow{\beta} ku$$
$$S^2 \wedge ku \to  ku \wedge ku  \to ku$$
$$\Sigma^2 ku \xrightarrow{\times \beta} ku$$


