
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The __free group__ on a given [[set]] $S$ is the [[free object]] on $S$ in [[Grp|the category of groups]].  The elements of $S$ are called the __generators__ of this group.

## Definition

### In type theory

In [[dependent type theory]], the free group on a type $A$ is the [[0-truncation]] of the [[underlying type of free infinity-group]] of $A$, $\mathrm{FreeGroup}(A) \coloneqq [\mathrm{UTFIG}(A)]_0$. This is because in any dependent type theory with [[uniqueness of identity proofs]], where every type is 0-truncated, the underlying type of the free infinity-group of $A$ is the free group of $A$. 

In addition, one could construct the free group directly from the traditional axioms of a [[group]], as detailed below:

The [[inference rules]] for free group types:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mathrm{FreeGroup}(A) \; \mathrm{type}}$$

Introduction rules for free groups:

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \eta:A \to \mathrm{FreeGroup}(A) \; \mathrm{type}} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \mu:\mathrm{FreeGroup}(A) \times \mathrm{FreeGroup}(A) \to \mathrm{FreeGroup}(A)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \epsilon:\mathrm{FreeGroup}(A)} \quad \frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \iota:\mathrm{FreeGroup}(A) \to \mathrm{FreeGroup}(A)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:\mathrm{FreeGroup}(A) \quad \Gamma \vdash y:\mathrm{FreeGroup}(A) \quad \Gamma \vdash z:\mathrm{FreeGroup}(A)}{\Gamma \vdash \alpha(x, y, z):\mathrm{Id}_{\mathrm{FreeGroup}(A)}(\mu(x, \mu(y, z)),\mu(\mu(x, y), z))}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:\mathrm{FreeGroup}(A)}{\Gamma \vdash \lambda_\epsilon(x):\mathrm{Id}_{\mathrm{FreeGroup}(A)}(\mu(\epsilon, x), x)} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:\mathrm{FreeGroup}(A)}{\Gamma \vdash \rho_\epsilon(x):\mathrm{Id}_{\mathrm{FreeGroup}(A)}(\mu(x, \epsilon), x)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:\mathrm{FreeGroup}(A)}{\Gamma \vdash \lambda_\iota(x):\mathrm{Id}_{\mathrm{FreeGroup}(A)}\mu(\iota(x), x),  \epsilon)} \quad \frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:\mathrm{FreeGroup}(A)}{\Gamma\vdash \rho_\iota(x):\mathrm{Id}_{\mathrm{FreeGroup}(A)}(\mu(x, \iota(x)), \epsilon)}$$

$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma \vdash \tau:\mathrm{isSet}(\mathrm{FreeGroup}(A))}$$

## Properties

* Every [[subgroup]] of a free group is itself a free group. This is the _[[Nielsen-Schreier theorem]]_.

## Related concepts

* [[free monoid]]

* [[free product of groups]]

* [[free abelian group]], [[free groupoid]]

* [[underlying type of free infinity-group]]

* [[Fox derivative]]

## References

Early discussion of ([[subgroups]] of) [[free groups]] (proof of the [[Nielsen-Schreier theorem]]) and generalization to the [[amalgamated free product of groups]]:

* [[Otto Schreier]], *Die Untergruppen der freien Gruppen*, Abh. Math. Semin. Univ. Hambg. **5** (1927) 161–183 &lbrack;[doi:10.1007/BF02952517](https://doi.org/10.1007/BF02952517)&rbrack;

Textbook account:

* [[Mark A. Armstrong]], chapter 27 of: *Groups and Symmetry*, Undergraduate Texts in Mathematics, Springer (1988) &lbrack;[doi:10.1007/978-1-4757-4034-9](https://doi.org/10.1007/978-1-4757-4034-9), [pdf](https://superoles.wordpress.com/wp-content/uploads/2014/10/lluvia.pdf)&rbrack;


Expository review:

* Abhay Chandel, *Free groups and amalgamated product*, BSc thesis (2013) &lbrack;[pdf](http://home.iiserb.ac.in/~kashyap/Group/thesis_abhay.pdf), [[Chandel-AmalgamatedProducts.pdf:file]]&rbrack;




Discussion of free groups in [[homotopy type theory]]:

* [[Univalent Foundations Project]], §6.11 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]*, Institute for Advanced Study (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Marc Bezem]], [[Ulrik Buchholtz]], [[Pierre Cagne]], [[Bjørn Ian Dundas]], [[Daniel R. Grayson]]: §6.2 in: *[[Symmetry]]* (2021) &lbrack;[pdf](https://unimath.github.io/SymmetryBook/book.pdf)&rbrack;

* [[Nicolai Kraus]], [[Thorsten Altenkirch]], *Free Higher Groups in Homotopy Type Theory*, LICS '18: Proceedings of the 33rd Annual ACM/IEEE Symposium on Logic in Computer Science, (2018) &lbrack;[arXiv;1805.02069](https://arxiv.org/abs/1805.02069), [doi:10.1145/3209108.3209183](https://doi.org/10.1145/3209108.3209183)&rbrack;





[[!redirects free groups]]


