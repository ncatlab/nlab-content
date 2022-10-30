Let $o$ be a Dedekind domain, let $K:=Quot(o)$ denote its quotient field,  let $L/K$ be a finite separable field extension of degree $n$, let $O\supset o$ be the integral closure of $o$ in $L$. Then $O$ is in particular a Dedekind domain 

Let for

$$o\stackrel{i}{\to} O\to L$$

$f:=Spec(i):Spec(O)\to Spec(o)$ be the induced map between the [[nLab:spectrum|ring spectra]] called *ramified covering*

Let $p\in Spec(o)$ be a maximal prime ideal. Then the ideal $pO$ in $O$ has a unique product decomposition

$$pO=P_1^{e_1}\dots P_r^{e_r}$$

with different $P_i\in Spec(O)$. It is custom to introduce some classifying vocabulary depending on the kind of this decomposition and the degree of the field extension $f_i:=[O/P_i:o/p]$: the $e_i$ are called *ramification indices* and the $f_i$ are called *inertia degrees* (see e.g. the [German wikipedia](http://de.wikipedia.org/wiki/Verzweigung_(Algebra) for more details). These satisfy the *fundamental identity* $\Sigma_i e_i f_i =n$ and every point $p\in Spec(O)$ has $\le n$ preimages. If $p$ has $\lt n$ preimages then $p$ is called *ramified*.

Let now $L/K$ be [[nLab:Galois theory|galois]] then the [[nLab:Galois group|Galois automorphisms]] $\sigma\in Gal(L/K):=Aut_K(L)$ (i.e. the automorphisms of $L$ which restrict to the identity on $K$) induce automorphisms of [[nLab:scheme|schemes]] $Spec(\sigma)$ and (since $\sigma$ fixes $o$) the diagram

$$\array{
Spec(O)&\stackrel{\Spec(\sigma)}{\to}&\Spec(O)
\\
\downarrow^f &\swarrow
\\
Spec(o)
}$$

commutes. $\tau:=\Spec(\sigma)$ is an example of a *cover automorphism* (also called *cover transformation* or *Deck transformation*). Since $Spec:Rings\to Schemes$ is an equivalence of categories we have an isomorphism

$$Gal(L/K)\simeq Aut_{Spec(o)}(Spec(O))$$

where the object to the right we have the group of cover automorphism.

One can show that there is a *maximal unramified extension* ($e_i=1$ and the extensions $O/P_i:o/p$ being separable) $\tilde K$ of $K$ and the scheme $\tilde Y:=Spec(\tilde o)$ where $\tilde o$ denotes the integral closure of $o$ in $\tilde K$. Then $f:\tilde Y\to Y:=Spec(O)$ satisfies the axioms of a *[[nLab:universal cover|universal covering]]* and consequently we define on the side of schemes the *[[nLab:fundamental group]]*

$$\pi_1(Y):=Aut_Y(\tilde Y)\simeq Gal(\tilde K/ K)$$

## References

* J&#252;rgen Neukirch, algebraic number theory, I.&#167;13.6{#NeuNum}