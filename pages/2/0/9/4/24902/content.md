\tableofcontents

## Definition

Given a [[Tarski universe]] $(U, T)$, the **locally $U$-small inductive cover** for a notion of [[real numbers]] is an [[inductive]] [[type family]] defined by the following rules:

Formation rules for locally $U$-small inductive covers:

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash a:\sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad b:\sum_{I:U} T[I/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r}{\Gamma \vdash a \lhd b \; \mathrm{type}}$$

Introduction rules for locally $U$-small inductive covers:

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash a:\sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad b:\sum_{I:U} T[I/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r}{\Gamma \vdash \mathrm{proptrunc}(a, b):\mathrm{isProp}(a \lhd b)}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash I:U \quad \Gamma \vdash \mathcal{F}:T[I/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad i:T[I/A]}{\Gamma \vdash \mathrm{reflexivity}(I, \mathcal{F}, i):\mathcal{F}(i) \lhd (I, \mathcal{F})}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash q:\mathbb{Q} \quad \Gamma \vdash r:\mathbb{Q} \quad \Gamma \vdash a:q \lt r \quad \Gamma \vdash I:U \quad \Gamma \vdash \mathcal{F}:T[I/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad \Gamma \vdash J:U \quad \Gamma \vdash \mathcal{G}:T[J/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad \Gamma \vdash b:(q, r) \lhd (G, \mathcal{J}) \quad \Gamma \vdash j:[J/A] \quad \Gamma \vdash c:\mathcal{G}(j) \lhd (J, \mathcal{G})}{\Gamma \vdash \mathrm{transitivity}(q, r, a, I, \mathcal{F}, J, \mathcal{G}, b, j, c):\left((q, r) \lhd (I, \mathcal{F})\right)}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash q:\mathbb{Q} \quad \Gamma \vdash r:\mathbb{Q} \Gamma \vdash a:q \lt r \quad \quad \Gamma \vdash s:\mathbb{Q} \quad \Gamma \vdash t:\mathbb{Q} \quad \Gamma \vdash b:q \lt r \quad \Gamma \vdash I:U \quad \Gamma \vdash \mathcal{F}:T[I/A] \to \sum_{q:\mathbb{Q}} \sum_{r:\mathbb{Q}} q \lt r \quad \Gamma \vdash c:(q, r) \subseteq (s, t) \quad \Gamma \vdash d:(s, t) \lhd (I, \mathcal{F})}{\Gamma \vdash \mathrm{monotonicity}(q, r, a, s, t, b, I, \mathcal{F}, c, d):(q, r) \lhd (I, \mathcal{F})}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash q:\mathbb{Q} \quad \Gamma \vdash r:\mathbb{Q} \quad \Gamma \vdash a:q \lt r \quad \Gamma \vdash s:\mathbb{Q} \quad \Gamma \vdash t:\mathbb{Q} \quad \Gamma \vdash b:q \lt r \quad \Gamma \vdash I:U \quad \Gamma \vdash \mathcal{F}:T[I/A] \to (\mathbb{Q} \times \mathbb{Q}) \quad \Gamma \vdash c:(s, t) \lhd (I, \mathcal{F})}{\Gamma \vdash \mathrm{localization}(q, r, a, s, t, b, I, \mathcal{F}, c):(q, r) \cap (s, t) \lhd (I, \lambda i.(\mathcal{F}(i) \cap (s, t))}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash q:\mathbb{Q} \quad \Gamma \vdash r:\mathbb{Q} \quad \Gamma \vdash s:\mathbb{Q} \quad \Gamma \vdash t:\mathbb{Q} \quad \Gamma \vdash a:q \lt r \quad \Gamma \vdash b:r \lt s \quad \Gamma \vdash c:s \lt t}{\Gamma \vdash \mathrm{coveroverlap}(q, r, s, t, a, b, c):(q, r) \lhd \left[(q, t), (r, s)\right]}$$

$$\frac{\Gamma \vdash U \; \mathrm{type} \quad \Gamma, A:U \vdash T \; \mathrm{type} \quad \Gamma \vdash q:\mathbb{Q} \quad \Gamma \vdash r:\mathbb{Q} \quad \Gamma \vdash a:q \lt r \quad}{\Gamma \vdash \mathrm{coverwithin}(q, r, a):(q, r) \lhd \left(\sum_{s:\mathbb{Q}} \sum_{t:\mathbb{Q}} (q \lt r) \times (r \lt s) \times (s \lt t), \lambda u.u\right)}$$

Elimination rules for locally $U$-small inductive covers:

...

Computation rules for locally $U$-small inductive covers:

...

## Properties

Every locally $U$-small inductive cover on the [[real numbers]] is a locally $U$-small pointwise cover on the [[real numbers]]. Assuming excluded middle, every locally $U$-small pointwise cover is a locally $U$-small inductive cover. 

## See also

* [[cover]]

## References

* *Homotopy Type Theory: Univalent Foundations of Mathematics*, The [[Univalent Foundations Project]], Institute for Advanced Study, 2013. ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf))