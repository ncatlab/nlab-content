

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition 

A [[connection on a bundle|connection]] on a [[fibre bundle]] is **flat** if its [[curvature]] is zero. 

The same definition of flatness holds for connections in various algebraic setups and for connections on [[quasicoherent sheaves]]. 

The condition of flatness is usually expressed via the [[Maurer-Cartan equation]]. Flat connections on bundles are also referred to as [[local systems]] (by the _Riemann-Hilbert correspondence_ discussed [below](#RiemannHilbertCorrespondence)).

## Properties

### Riemann-Hilbert correspondence
 {#RiemannHilbertCorrespondence}

That flat connections are equivalently [[representations]] of the [[fundamental groupoid]] of the base space/[[local systems]] is known as the _[[Riemann-Hilbert correspondence]]_.

### Flatness as integrability

In geometry one says instead of flat connection, **integrable connection**. The reason is roughly the following: in the theory of systems of differential equations the flatness of the corresponding connection is the condition of the integrability of the system. 

(...elaborate on this with equations)

The condition of flatness is usually expressed via the [[Maurer-Cartan equation]], which is in integrable systems theory often called *zero curvature equation*. For example, the Lax equations can always be written in the form of the zero curvature equation. 

### Over a complex manifold

Over a [[complex manifold]]/[[complex variety]] the [[Koszul-Malgrange theorem]] identifies holomorphic flat connections on [[complex vector bundles]] with [[holomorphic vector bundles]]. See there for more

### Over a Riemann surface

#### Existence

In ([Milnor](#Milnor)) it is shown that a [[vector bundle]] over a [[surface]] of [[genus]] $g$ admits flat connections iff its [[Euler class]] is less than $g$ by an [[absolute value]] (see also Wood, Bundles with totally disconnected structure group). [Sullivan](#Sullivan) gives a refinement.

#### Narasimhan&#8211;Seshadri theorem

The _[[Narasimhan-Seshadri theorem]]_ identifies [[moduli spaces of flat connections]] over a [[Riemann surface]] with that of certain [[stable vector bundles]]. 

### Isometric embeddings

Maurer-Cartan equation is called also structure equation when used to treat the conditions for isometric embeddings of Riemannian submanifolds in an Euclidean space. 

...

## Related concepts

* [[local system]], [[inner local system]]

* [[projectively flat connection]]

* [[moduli space of flat connections]], [[Narasimhan-Seshadri theorem]]

* [[flat ∞-connection]]

* [[flat section]]

## References

On the equivalence between flat connections ([[local systems]]) with [[group homomorphisms]] out of the [[fundamental group]] (over each [[connected component]]):

* [[Pierre Deligne]], §I.1 of: *Equations différentielles à points singuliers réguliers*, Lecture Notes  Math. **163**, Springer (1970) $[$[publications.ias:355](https://publications.ias.edu/node/355)$]$

and generally with [[functors]] out of the [[fundamental groupoid]]:

* [[Alexandru Dimca]], Prop. 2.5.1 of: *Sheaves in Topology*, Universitext, Springer (2004) &lbrack;[doi:10.1007/978-3-642-18868-8](https://doi.org/10.1007/978-3-642-18868-8)&rbrack;

* [[Urs Schreiber]], [[Konrad Waldorf]], p. 194 of: *Parallel Transport and Functors*, J. Homotopy Relat. Struct. **4** (2009) 187-244 &lbrack;[arXiv:0705.0452](https://arxiv.org/abs/0705.0452), [pdf](https://tcms.org.ge/Journals/JHRS/xvolumes/2009/n1a10/v4n1a10hl.pdf)&rbrack;

* [[Florin Dumitrescu]], Cor. 3 of: *Connections and Parallel Transport*, Journal of Homotopy and Related Structures **5** 1 (2010) 171–175 &lbrack;[arXiv:0903.0121](https://arxiv.org/abs/0903.0121), [pdf](https://tcms.org.ge/Journals/JHRS/xvolumes/2010/n1a10/v5n1a10hl.pdf)&rbrack;


The latter articles also discuss the generalization of this statement to non-flat connections ,for more see the references at *[[parallel transport]]* [here](parallel+transport#ReferencesInTermsOfParallelTransport).

See also

* {#Milnor} [[John Milnor]], *On the existence of a connection with curvature zero*, Comm. Math. Helv. **32** (1957/58) 215-223 &lbrack;[dml:139154](http://eudml.org/doc/139154)&rbrack;
  

* {#Sullivan} [[Dennis Sullivan]], _A generalization of Milnor's inequality_ Comm. Math. Helv. v. 51
  

* [[Hélène Esnault]], _Algebraic Differential Characters of Flat Connections with Nilpotent Residues_, in [[Nils Baas]] et al., The Abel Symposium 2007 ([pdf](bib.tiera.ru/b/91797))

[[!redirects integrable connection]]

[[!redirects flat connections]]

[[!redirects projectively flat connection]]
[[!redirects projectively flat connections]]