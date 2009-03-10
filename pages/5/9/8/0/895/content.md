
#Cofibration category: ($C$, _cof_, _w.e._)

A *cofibration category* is a category $C$ with two classes of morphisms, _cof_ of
_cofibrations_ and _w.e._ of _weak equivalences_.
These are to satisfy:

C 1) Isomorphisms are both cofibrations and weak equivalences.  If

$$A\stackrel{f}{\rightarrow} B \stackrel{g}{\rightarrow} C$$ 
are composable morphisms in $C$, then if two of $f$, $g$ $gf$ are in  _w.e._, so is the
third; if $f$, $g \in cof$ then $gf\in cof$.

C2) Pushout axiom:

Given $B\rightarrow A$ in _cof_ and any $f : B\rightarrow Y$, the pushout


$$
  \array{
    B &\stackrel{f}{\rightarrow}& Y
    \\
    \downarrow_i
    &&
    \downarrow^{\bar{i}}
    \\
   A &\stackrel{\bar{f}}{\to}&  A \cup_B Y   
  }
$$

exists and $\bar{i}$ is in _cof_; if $f$ is a w.e., so is $\bar{f}$; if $i$ is also a w.e., so is $\bar{i}$.

C3) Factorisation axiom:

Given $B\stackrel{f}{\rightarrow} Y$, there is a factorisation 

$$
  \array{
B&\stackrel{f}{\longrightarrow}&Y\\
\stackrel{i}{\searrow}&&\stackrel{g}{\nearrow}\\
&A&
}$$

with $i \in cof$, $g\in w.e.$

C4) Axiom on fibrant models:

Using the terminology: "$f$ is a _trivial cofibration_" to mean "$f\in
cof \cap w.e.$", and "$RX$ is _fibrant_" to mean "Given any trivial
cofibration $i: RX \stackrel{\simeq}{\rightarrow}Q$, there is a retraction $r :
Q \rightarrow RX$, $ri = Id_{RX}$", the axiom states:

Given $X\in C$, there is trivial cofibration $X\rightarrow RX$ with $RX$ fibrant.

##Examples:##

* If $C$ has a model category structure then the full subcategory of  cofibrant objects forms a cofibration category.

##References:##

H.J. Baues, _Algebraic homotopy_, Cambridge studies in advanced mathematics 15, 
Cambridge University Press, (1989). 
