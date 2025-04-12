
\tableofcontents

## Idea

In [[dependent type theory]], given types $A$ and $B$, an [[anafunction]] is a [[type family]] $x\colon A, y \colon B \vdash R(x, y) \; \mathrm{type}$ which comes with a family of witnesses 
$$x \colon A \vdash p(x) \colon \mathrm{isContr}\left(\sum_{y:B} R(x, y) \right)$$
that for each [[term|element]] $x\colon A$, the [[dependent sum type]] $\sum_{y\colon B} R(x, y)$ is a [[contractible type]]. 

A *dependent anafunction* is like such an anafunction but where we allow $B$ to also [[dependent type|depend]] on $x\colon A$. 

## Definition 

In [[dependent type theory]] ([[homotopy type theory]]), given a type $A$ and a [[type family]] $x\colon A \vdash B(x) \; \mathrm{type}$, a **dependent anafunction** is a type family $x\colon A, y\colon B(x) \vdash R(x, y) \; \mathrm{type}$ which comes with a family of witnesses 
$$x \colon A \vdash p(x) \colon \mathrm{isContr}\left(\sum_{y\colon B(x)} R(x, y) \right)$$
that for each element $x\colon A$, the [[dependent sum type]] $\sum_{y\colon B(x)} R(x, y)$ is a [[contractible type]]. 

## Properties

The [[principle of unique choice]] holds in dependent type theory, which means that given any dependent anafunction $x:A, y:B(x) \vdash R(x, y) \; \mathrm{type}$, there is a dependent function $x:A \vdash f(x):B(x)$. 

## Dependent function types as types of dependent anafunctions

In the same way that one could define [[equivalence types]] as types of [[one-to-one correspondences]] and [[function types]] as types of [[anafunctions]], one could define [[dependent function types]] as types of dependent anafunctions. This requires both [[identity types]] and [[indexed heterogeneous identity types]] being defined first, which we shall write as $a =_A b$ and $x =_{B}^{p} y$ respectively for $a:A$, $b:A$, $p:a =_A b$, $x:B(a)$, and $y:B(b)$. We use Agda notation $(x:A) \to B(x)$ for dependent function types rather than the dependent product type notation $\prod_{x:A} B(x)$ or $\Pi(x:A).B(x)$ in this section. 

Rules for dependent function types
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma \vdash (x:A) \to B(x) \; \mathrm{type}} \qquad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x) \vdash \mathcal{F}_{A, B}(f, x, y) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B(x)}{\Gamma \vdash \lambda x.f(x):(x:A) \to B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type} \quad \Gamma, x:A \vdash f(x):B(x)}{\Gamma, x:A \vdash \alpha(x):\mathcal{F}_{A, B}(\lambda x.f(x), x, f(x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A \vdash \mathrm{ev}(f, x):B(x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A \vdash \beta(f, x):\mathcal{F}_{A, B}(f, x, \mathrm{ev}(f, x))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x), u:\mathcal{F}_{A, B}(f, x, y) \vdash \kappa(f, x, y, u):\mathrm{ev}(f, x) =_{B(x)} y}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x), x:A, y:B(x), u:\mathcal{F}_{A, B}(f, x, y) \vdash \eta(f, x, y, u):\beta(f, x) =_{\mathcal{F}_{A, B}(f, x)}^{\kappa(f, x, y, u)} u}$$

By the rules for [[dependent pair types]] and [[dependent function types]], one could derive that 

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash B(x) \; \mathrm{type}}{\Gamma, f:(x:A) \to B(x) \vdash \eta(f):(x:A) \to \mathrm{isContr}\left((y:B) \times \mathcal{F}_{A, B}(f, x, y)\right)}$$

which is precisely the statement that $\mathcal{F}_{A, B}(f)$ is a dependent anafunction for all dependent functions $f:(x:A) \to B(x)$. 

## See also

* [[anafunction]]

* [[dependent function]]

* [[dependent function type]]

* [[dependent correspondence]]

[[!redirects dependent anafunction]]
[[!redirects dependent anafunctions]]