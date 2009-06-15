Talk notes for the session of 

* Friday June 12 

of 

* [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]].


## Corbett Redden: String structures and 3-forms ##


* notational conventions 

  * $M^n$ a smooth closed $n$-manifold
  
  * $g$ a Riem. metric 
  
  * $Spin \to P \to M$ a principal $Spin(n)$-bundle
  
  * $A$ a connection on $P$
  
  * $S$ a string class
  
### Outline ###

* I $\{String Structures\}/_{homotopy}$

* II harmonic 4-forms on $P$

* III geometry and tmf?

### I. String structures ###

**definition** 

* $B String$ is defined to be the homotopy fiber $B String(n) \to B Spin(n) \stackrel{p_1/2}{\to} K(\mathbb{Z},4)$

* a **[[string structure|String structure]]** on $\pi : P \to M$ is a lift of the classifying map to $B Spin$ through 
  $B String \to B Spin$
  $$
    \array{
        P && B String
        \\
        \downarrow &\nearrow& \downarrow
        \\
        M &\to& B Spin
    }
  $$
  
**Prop**

* String structure exists iff $\frac{1}{2}p_1(P) = 0 \in H^4(X,\mathbb{Z})$ (essentially by definition through homotopy fiber)

* let $i^*_P$ the pullback to the fiber of $P$, then we have
  $$\{String structures\}/_{homotopy} 
     \simeq_{canonical} \{String classes\} 
    := 
    \{\rho \in H^3(P,\mathbb{Z}) 
     s. t. i_P^* \rho = 1 
     \in H^3(Spin, \mathbb{Z})\}
  $$
  
* $\{string class\}$ is a torsor for $H^3(M, \mathbb{Z})$ under $\rho \mapsto \rho + \pi^ H^3(M)$

Proof. universal example

$$
  \array{
    K(\mathbb{Z},3) &\simeq& \pi^* E Spin &\to & E Spin
    \\
    && B String &\to& B Spin &\to& K(\mathbb{Z}, 4)
  }
$$

>hm, here is my ([[Urs Schreiber|Urs]]) description of the situation:

consider the following pasting diagram of 
[[homotopy limit|homtopy pullbacks]] 
($P$ is the given $Spin$-bundle, $\hat P$ its String-lift)

$$
  \array{
    String &\to& \hat P &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    Spin &\to& P &\to&  B^2 U(1) &\to& {*}
    \\
    \downarrow && \downarrow && \downarrow && \downarrow
    \\
    {*} &\to& X &\to& B String(n) &\to& B Spin(n)
  }
$$

**Why String structures? **

String structure on $P$ $\stackrel{transgresses}{\mapsto}$
Spin structure on loop space $L Spin \to L P \to L M$

but all the reps of this loop group are projective, so there is 
actually a central $S^1$ extension of $L Spin$ in the game

$$
  \hat {L Spin} \to L Spin
$$

Need: 

$$
  \array{
    \hat {L Spin} &\to & \hat {L P}
    \\
    \downarrow && \downarrow
    \\
    L Spin &\to& L P
  }
$$

$$
  \rho \in H^3(P, \mathbb{Z}) \mapsto 
$$

$$
  \array{
    (\pi_! ev^*) \rho &\in& H^2(L P, \mathbb{Z})
    \\
    \downarrow && \downarrow
    \\
    iniv. ext. && H^2(L G, \mathbb{Z})
  }
$$

(on the right: $S^1$-bundles)

** String orientation ** of tmf = topological modular forms

$$
  M O\langle 8\rangle^{-n} = M String &\stackrel{\sigma}{\to}& tmf^{-n}(pt)
$$

so give a String manifold with a String class on $Spin(T M)$

$$
  M , \rho \mapsto [M, \rho] \mapsto \sigma(M,\rho)
$$

$$
  \array{
    && tmf
    \\
    & {}^{\sigma}\nearrow & \downarrow
    \\
    M String &\stackrel{Witten genus}{\to}& Mod Forms
  }
$$


  $Witten genus(M) =$  "$index^{S^1} D_{L M}$"


(by the way, $\sigma$ is surjective on homotopy classes)


**warning**: I think above my $\rho$ should really be an $S$

### II Harmonic representative of $S$ ###

*reminder*

$(M,g) \mapsto \Delta = d d^* + d^* d$

$$
  H^k(M,\mathbb{R}) \simeq_{Hodge} \Delta^*_g \subset \Omega^k(M)
$$

**construction** 

start with $(\pi : P  \to M, g_m, A)$

choose a bininvariant metric 

$$
  g_\rho := \pi^* g_m \oplus g_{spin}
$$

where the direct sum comes from the splitting of tangent spaces $T_p P$ using
the connection that we have

Introduce scaling factor $\delta \gt 0$

$$
  g_\rho := \pi^* g_m \oplus \delta^2 g_{spin}
$$

take the "adiabatic limit" $\lim_{\delta \to 0}$

so now there is a 1-parameter family of metric on the bundle, and for each 
one can look at its Laplacian, so as $\delta$ tends to 0 something becomes
singular and one has to be careful, but fortunately others already did
that for us...


**theorem** (Mazzeo-Melrose, Dai, Forman)

the kernel
$
  Ker \Delta_{g_\rho} 
$ 

* extends smoothly to $\delta = 0$ 
  *(there is a smooth path in some Grassmannian space)

* and comes from a filtration isomorphic to Serre SS for $(Spin \to P \to M)$

this means that 

$$
  \Rightarrow H^k(P, \mathbb{Z})
  \stackrel{\simeq}{\to}
   \lim_{\delta \to 0}
   Ker \Delta_{g_\rho}
   =: H^k(P)
$$

**Theorem** (Redden)

Given $P \stackrel{\pi}{\to} g, A$ and $\frac{1}{2}p_1(P) = 0$

then
$$
  \array{
    H^3(P, \mathbb{Z}) &\to& H^3(P,\mathbb{R}) &\to& H^3(P)
    \\
    S &&\mapsto& CS_3(A)&& CS_3(A) - \pi^* H 
  } 
$$

here $CS_3(A)$ is the Chern-Simons 3-form of the spin-connection

and recall $H^3(P)$ here denotes _harmonic forms_ on $P$ (should really be
script font

**remark**

in genral 

$$
  [\rho]_{g_\delta} = 
  CS_3(A) - \pi^* H + O(\delta) \not\in \pi^* \Omega^3(M)
$$

if we have a product of two groups we accordingly would get
CS of one connection minus CS of the other.

**What is $H$? **

(first digression)

**theorem** (Chern-Simons,...)

given $(P \to M , A)  \mapsto \hat {frac{1}{2} p_1}(A) \hat H^4(M)$ 


$$
  \array{
    \Omega^3_{\mathbb{Z}} &\to& 
    (M)\Omega^3(M) &\stackrel{a}{to}& \hat H^4(M) &\to& H^4(M,\mathbb{Z}) &\to& 0
    \\
    && 
    H &\mapsto& \hat{\frac{1}{2}p_1(A)} 
    &\mapsto& 
    \frac{1}{2}p_1(P) = 0
    && 
  }
$$

in particular

$$
  \array{
    && \mathbb{R}
    \\
    & {}^{\int H} \nearrow & \downarrow
    \\
    \mathbb{Z}_3(M)
    &\stackrel{\hat {\frac{1}{2}p_1(A)}}{\to}&
    \mathbb{R}/\mathbb{Z}
  }
$$

and secondly  $d^* H = 0$

these two properties determine $H$ uniquely up to 
harmonic forms $\mathcal{H}^3_{\mathbb{Z}}(M) = ker \Delta_g$

**Equivariance**

$$
  H_{\rho + \pi^* \psi} = H_\rho + \pi^* H4
$$

where $\psi \in H^3(M, \mathbb{Z})$ $\mapsto H_4 \in \mathcal{H}^3(M)$

over all what this says is that if we go from

$$
 \array{
    Metr(M)\times A(P) \times \{String Class\} & (g,A,S)
    \\
    \downarrow & \downarrow
    \\
    \Omega^3(P) & CS_3(A) - \pi^* H_{q,A,S}
    \\
    \downarrow & \downarrow
    \\
    \Omega^3(M) & H_{g, A \rho}
 }
$$

$$
  \array{
     && tmf^{-n}
     \\
     & \nearrow & \downarrow
    \\
    M String &\stackrel{}{\to}&
    MF
  }
$$

**conjecture** (S. Stolz) if $M$ is String and admits a positive
Ricci curvature metric, then $Witten(M) = 0$

question: also $\sigma(M,\rho) = 0$? no, no way!

**hypothesis**

If $M$ is a Spin manifold that admits a metric and String structure
$(g, S)$ and $A$ is the Levi-Civita connection

such that

* $Ric(g) \gt 0$

* $H_{g,s} = 0 \in \Omega^3(M)$

$\Rightarrow \sigma(M,S) = 0 \in tmf^{-n}(pt)$

**example**  $M = S^3 = SU(2)$

$$
  p_1 \in H^4(S^3) = 0
$$

$$
  H^3(S^3, \mathbb{Z}) = \mathbb{Z} = number of string classes
$$

$$
  d H = d^* H = 0  \Rightarrow H \in H^3(S^3, \mathbb{R}) \simeq \mathbb{R}
$$

$$
  \array{
    String Classes
    \\
    \downarrow
    \\
    M String^{-3} = \pi_3^S = tmf^{-3} = \mathbb{Z}/{24}
  }
$$

>(can't type the full diagram...)

consider a 1-parameter family of "berger metrics" on $S^3$

rescaling the fiber in the Hopf fibration $S^1 \to S^3 \to S^2$


## Konrad Waldorf ##

>[[Urs Schreiber|Urs]]: I had to miss that and the following two talks, hopefully somebody else has notes. Konrad's talk is based on his new article 

* [[Konrad Waldorf]], _String connections and Chern-Simons theory_ ([arXiv](http://arxiv.org/abs/0906.0117))

## one more##

...

## Mike Hopkins : Kervaire invariant one ##

...

***

[[Oberwolfach Workshop, June 2009 -- Thursday, June 11|Previous day]] --- [[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology|Main workshop page]] --- No next day