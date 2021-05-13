


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
=--
=--


> under construction

#Contents#
* table of contents
{:toc}

## Idea

Quantum information refers to data that can be physically stored in a [[quantum mechanics|quantum system]]. 

Quantum information theory is the study of how such information can be encoded, measured, and manipulated. A notable sub-field is _quantum computation_, a term often used synonymously with quantum information theory, which studies protocols and algorithms that use quantum systems to perform computations.

Categorical quantum information refers to a program in which the cogent aspects of [[Hilbert space]]-based quantum information theory are abstracted to the level of [[symmetric monoidal categories]].

## Quantum protocols and algorithms

Brief synopsis of teleportation, [[entanglement]] swapping, BB84, E91, Deutsch-Jozsa, Shor should go here...

## Category-theoretic formulation

There is a formulation of (aspects of) [[quantum mechanics in terms of dagger-compact categories]]. This lends itself to (and is in fact motivated by) to a discussion of quantum information.

The linear adjoint $(-)^\dagger$ gives Hilbert spaces the structure of a [[†-category]]. The category of Hilb of Hilbert spaces forms a **&#8224;-symmetric monoidal category**, that is, a [[symmetric monoidal category]] equipped with a symmetric monoidal functor $(-)^\dagger$ from $Hilb^{op}$ to $Hilb$. Furthermore, the category FHilb of _finite dimensional_ Hilbert spaces forms a **[[dagger-compact category|†-compact closed category]]**, or a [[compact closed category]] such that $A_*$ := $(A^*)^\dagger = (A^\dagger)^*$ and $(\eta_A)^\dagger = \epsilon_{A^*}$.

### Graphical notation

Graphical notation via [[Penrose notation]]/[[string diagrams]]/[[tensor networks]]:


Morphisms in a [[monoidal category]] (and 2-categories in general) are inherently two dimensional, where $\circ$ is _vertical_ composition and $\otimes$ is _horizontal_ composition. These satisfy an [[interchange law]]:

\[ (f_1 \otimes f_2) \circ (g_1 \otimes g_2) = (f_1 \circ g_1) \otimes (f_2 \circ g_2) \]

So, if we think of these four morphisms as occupying a spot in 2 dimensional space:

+--{: .query}
[[Aleks Kissinger]]: TODO: figure
=--

we realize that the bracketing from above is essentially meaningless syntax. This notion is the guiding concept for the graphical notation of monoidal categories, or string diagrams. In this notation, we represent objects $A,B$ as directed strings and arrows $f : A \rightarrow B$ as boxes.

<div style="text-align:center">
<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="60px" height="109px" viewBox="-39 3 60 109" enable-background="new -39 3 60 109" xml:space="preserve">
<line fill="none" stroke="#000000" stroke-width="2" x1="-9.5" y1="12" x2="-9.5" y2="102"/>
<text transform="matrix(1 0 0 1 -0.5 30)" font-family="Helvetica" font-size="12">A</text>
<text transform="matrix(1 0 0 1 -0.5 93)" font-family="Helvetica" font-size="12">B</text>
<rect x="-27.5" y="39" fill="#CCCCEE" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-14,22.5 -9.5,27 -5,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-14,86 -9.5,90.5 -5,86 "/>
<text transform="matrix(1 0 0 1 -14.4805 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
</svg>
</div>

We represent the tensor product as juxtaposition:

<div style="text-align:center">
<svg version="1.1" id="Layer_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" x="0px" y="0px"
	 width="234px" height="108px" viewBox="-60 0 174 108" xml:space="preserve">
<line fill="none" stroke="#000000" stroke-width="2" x1="62.5" y1="12" x2="62.5" y2="102"/>
<text transform="matrix(1 0 0 1 71.5 30)" font-family="'Helvetica'" font-size="12">A</text>
<text transform="matrix(1 0 0 1 71.5 93)" font-family="'Helvetica'" font-size="12">B</text>
<rect x="44.5" y="39" fill="#CECBE6" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="58,22.5 62.5,27 67,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="58,86 62.5,90.5 67,86 "/>
<text transform="matrix(1 0 0 1 57.5195 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="116.5" y1="12" x2="116.5" y2="102"/>
<text transform="matrix(1 0 0 1 125.5 30)" font-family="'Helvetica'" font-size="12">C</text>
<text transform="matrix(1 0 0 1 125.5 93)" font-family="'Helvetica'" font-size="12">D</text>
<rect x="98.5" y="39" fill="#99CCCC" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="112,22.5 116.5,27 121,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="112,86 116.5,90.5 121,86 "/>
<text transform="matrix(1 0 0 1 108.5195 63.0322)" font-family="Helvetica" font-style="italic" font-size="24">g</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="-63.5" y1="12" x2="-63.5" y2="102"/>
<text transform="matrix(1 0 0 1 -54.5 30)" font-family="'Helvetica'" font-size="12">A</text>
<text transform="matrix(1 0 0 1 -54.5 93)" font-family="'Helvetica'" font-size="12">B</text>
<rect x="-81.5" y="39" fill="#CECBE6" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-68,22.5 -63.5,27 -59,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-68,86 -63.5,90.5 -59,86 "/>
<text transform="matrix(1 0 0 1 -68.4805 66.0322)" font-family="Helvetica" font-style="italic" font-size="24">f</text>
<line fill="none" stroke="#000000" stroke-width="2" x1="-0.5" y1="12" x2="-0.5" y2="102"/>
<text transform="matrix(1 0 0 1 8.5 30)" font-family="'Helvetica'" font-size="12">C</text>
<text transform="matrix(1 0 0 1 8.5 93)" font-family="'Helvetica'" font-size="12">D</text>
<rect x="-18.5" y="39" fill="#99CCCC" stroke="#000000" stroke-width="2" width="36" height="36"/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-5,22.5 -0.5,27 4,22.5 "/>
<polyline fill="none" stroke="#000000" stroke-width="2" points="-5,86 -0.5,90.5 4,86 "/>
<text transform="matrix(1 0 0 1 -8.4805 63.0322)" font-family="Helvetica" font-style="italic" font-size="24">g</text>
<text transform="matrix(1 0 0 1 25.1362 62.2832)" font-family="Helvetica" font-size="18">=</text>
<text transform="matrix(1 0 0 1 -39.5469 62.1729)" font-family="Helvetica" font-size="17.9327">&#8855;</text>
</svg>
</div>

and composition as graph composition:

<div style="text-align:center">
<svg xmlns:svg="http://www.w3.org/2000/svg" xmlns="http://www.w3.org/2000/svg" version="1.1" width="207" height="189" viewBox="-60 0 153.92308 189" id="Layer_1" xml:space="preserve"><defs id="defs3013"/>
<line x1="12.46154" y1="45" x2="12.46154" y2="135" id="line2979" style="fill:none;stroke:#000000;stroke-width:2"/>
<text x="21.46154" y="63" id="text2981" style="font-size:12px;font-family:Helvetica">A</text>
<text x="21.46154" y="126" id="text2983" style="font-size:12px;font-family:Helvetica">B</text>
<rect width="36" height="36" x="-5.5384598" y="72" id="rect2985" style="fill:#cecbe6;stroke:#000000;stroke-width:2"/>
<polyline points="-68,22.5 -63.5,27 -59,22.5 " id="polyline2987" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(75.96154,33)"/>
<polyline points="-68,86 -63.5,90.5 -59,86 " id="polyline2989" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(75.96154,33)"/>
<text x="7.481041" y="99.032204" id="text2991" style="font-size:24px;font-style:italic;font-family:Helvetica">f</text>
<line x1="-50.53846" y1="45" x2="-50.53846" y2="135" id="line2993" style="fill:none;stroke:#000000;stroke-width:2"/>
<text x="-41.53846" y="63" id="text2995" style="font-size:12px;font-family:Helvetica">B</text>
<text x="-41.53846" y="126" id="text2997" style="font-size:12px;font-family:Helvetica">C</text>
<rect width="36" height="36" x="-68.53846" y="72" id="rect2999" style="fill:#99cccc;stroke:#000000;stroke-width:2"/>
<polyline points="-5,22.5 -0.5,27 4,22.5 " id="polyline3001" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(-50.03846,33)"/>
<polyline points="-5,86 -0.5,90.5 4,86 " id="polyline3003" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(-50.03846,33)"/>
<text x="-58.518959" y="96.032204" id="text3005" style="font-size:24px;font-style:italic;font-family:Helvetica">g</text>
<text x="42" y="95.283203" id="text3007" style="font-size:18px;font-family:Helvetica">=</text>
<text x="-24.585361" y="103.1729" id="text3009" style="font-size:36px;font-family:Helvetica"><tspan id="tspan2874" style="font-size:36px">&#9702;</tspan></text>
<text x="93.46154" y="36" id="text2897" style="font-size:12px;font-family:Helvetica">A</text>
<text x="93.46154" y="99" id="text2899" style="font-size:12px;font-family:Helvetica">B</text>
<polyline transform="translate(147.96154,6)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2903" points="-68,22.5 -63.5,27 -59,22.5 "/><polyline transform="translate(147.96154,6)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2905" points="-68,86 -63.5,90.5 -59,86 "/><line style="fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:4;stroke-dasharray:none" id="line2909" y2="171" x2="84.46154" y1="18" x1="84.46154"/><text x="93.46154" y="162" id="text2913" style="font-size:12px;font-family:Helvetica">C</text>
<rect width="36" height="36" x="66.46154" y="108" id="rect2915" style="fill:#99cccc;stroke:#000000;stroke-width:2"/><polyline transform="translate(84.96154,69)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2919" points="-5,86 -0.5,90.5 4,86 "/><text x="76.481041" y="132.0322" id="text2921" style="font-size:24px;font-style:italic;font-family:Helvetica">g</text>
<rect width="36" height="36" x="66.46154" y="45" id="rect2901" style="fill:#cecbe6;stroke:#000000;stroke-width:2"/><text x="79.481041" y="72.032204" id="text2907" style="font-size:24px;font-style:italic;font-family:Helvetica">f</text>
</svg>
</div>

That is, we perform a pushout along the common edge in the category of typed graphs with boundaries. Consider the interchange law from above, but replacing some of the arrows with identities.

\[
(f \otimes 1_D) \circ (1_A \otimes g) = (f \circ 1_A) \otimes (1_D \circ g) =
(1_B \circ f) \otimes (g \circ 1_C) = (1_B \otimes g) \circ (f \otimes 1_C)
\]

Graphically, this means we can "slide boxes" past each other.

<div style="text-align:center">
<svg xmlns:svg="http://www.w3.org/2000/svg" xmlns="http://www.w3.org/2000/svg" version="1.1" width="243" height="189" viewBox="-60 0 180.69231 189" id="Layer_1" xml:space="preserve"><defs id="defs3013"/>
<line x1="-10.153852" y1="18" x2="-10.153852" y2="171" id="line2854" style="fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:4;stroke-dasharray:none"/><text x="-46.153854" y="36" id="text2897" style="font-size:12px;font-family:Helvetica">A</text>
<text x="-46.153854" y="99" id="text2899" style="font-size:12px;font-family:Helvetica">B</text>
<polyline transform="translate(8.3461471,6)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2903" points="-68,22.5 -63.5,27 -59,22.5 "/><polyline transform="translate(8.3461471,6)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2905" points="-68,86 -63.5,90.5 -59,86 "/><line style="fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:4;stroke-dasharray:none" id="line2909" y2="171" x2="-55.153854" y1="18" x1="-55.153854"/><text x="-1.1538526" y="162" id="text2913" style="font-size:12px;font-family:Helvetica">D</text>
<rect width="36" height="36" x="-28.153852" y="108" id="rect2915" style="fill:#99cccc;stroke:#000000;stroke-width:2"/><polyline transform="translate(-9.6538529,69)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2919" points="-5,86 -0.5,90.5 4,86 "/><text x="-18.134352" y="132.0322" id="text2921" style="font-size:24px;font-style:italic;font-family:Helvetica">g</text>
<rect width="36" height="36" x="-73.153854" y="45" id="rect2901" style="fill:#cecbe6;stroke:#000000;stroke-width:2"/><text x="-60.134354" y="72.032204" id="text2907" style="font-size:24px;font-style:italic;font-family:Helvetica">f</text>
<text x="-1.1538526" y="99" id="text2856" style="font-size:12px;font-family:Helvetica">C</text>
<polyline points="-68,86 -63.5,90.5 -59,86 " id="polyline2858" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(53.346147,6)"/><text x="23.846148" y="106" id="text2860" xml:space="preserve" style="font-size:32px;font-style:normal;font-weight:normal;fill:#000000;fill-opacity:1;stroke:none;font-family:Bitstream Vera Sans"><tspan x="23.846148" y="106" id="tspan2862" style="font-size:24px">=</tspan></text>
<line style="fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:4;stroke-dasharray:none" id="line2864" y2="171" x2="115.84615" y1="18" x1="115.84615"/><text x="79.846153" y="99" id="text2866" style="font-size:12px;font-family:Helvetica">A</text>
<text x="79.846153" y="162" id="text2868" style="font-size:12px;font-family:Helvetica">B</text>
<polyline points="-68,22.5 -63.5,27 -59,22.5 " id="polyline2870" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(134.34616,69)"/><polyline points="-68,86 -63.5,90.5 -59,86 " id="polyline2872" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(134.34616,69)"/><line x1="70.846146" y1="18" x2="70.846146" y2="171" id="line2874" style="fill:none;stroke:#000000;stroke-width:2;stroke-miterlimit:4;stroke-dasharray:none"/><text x="124.84615" y="99" id="text2876" style="font-size:12px;font-family:Helvetica">D</text>
<rect width="36" height="36" x="97.846153" y="45" id="rect2878" style="fill:#99cccc;stroke:#000000;stroke-width:2"/><polyline points="-5,86 -0.5,90.5 4,86 " id="polyline2880" style="fill:none;stroke:#000000;stroke-width:2" transform="translate(116.34616,6)"/><text x="107.86565" y="69.032196" id="text2882" style="font-size:24px;font-style:italic;font-family:Helvetica">g</text>
<rect width="36" height="36" x="52.846153" y="108" id="rect2884" style="fill:#cecbe6;stroke:#000000;stroke-width:2"/><text x="65.865654" y="135.0322" id="text2886" style="font-size:24px;font-style:italic;font-family:Helvetica">f</text>
<text x="124.84615" y="36" id="text2888" style="font-size:12px;font-family:Helvetica">C</text>
<polyline transform="translate(179.34616,-57)" style="fill:none;stroke:#000000;stroke-width:2" id="polyline2890" points="-68,86 -63.5,90.5 -59,86 "/></svg>
</div>

## Extensions

CPM, classical structures, ...

## Related entries

* [[quantum logic]], [[quantum theory]]

* [[Kochen-Specker theorem]]

* [[quantum computation]]

* [[qbit]], [[quantum circuit model]]

* [[quantum error correcting code]]

* [[information theory]], [[information geometry]]

* [[MIP-star=RE]]

* [[entanglement entropy]], [[holographic entanglement entropy]]

## References

Textbook accounts:

* Masahito Hayashi, _Quantum information theory - mathematical foundation_ Graduate Texts in Physics (2017)

* Nielsen, Chuang, _Quantum computation and quantum information_, Cambridge Univeristy Press, [ch1 pdf](https://ncatlab.org/nlab/files/NielsenChuangQuantumComputation.pdf)

* Sumeet Khatri, Mark M. Wilde, _Principles of Quantum Communication Theory: A Modern Approach_ ([arXiv:2011.04672](https://arxiv.org/abs/2011.04672))

* [[Giuliano Benenti]], [[Giulio Casati]], [[Davide Rossini]], *Principles of Quantum Computation and Information*, World Scientific 2018  ([doi:10.1142/10909](https://doi.org/10.1142/10909), [2004 pdf](http://mmrc.amss.cas.cn/tlb/201702/W020170224608149307696.pdf))

In a context of [[quantum optics]]:

* [[Tim Byrnes]], [[Ebubechukwu Ilo-Okeke]], Section 11 of: *Quantum Atom Optics: Theory and Applications to Quantum Technology*, Cambridge University Press 2021 ([arXiv:2007.14601](https://arxiv.org/abs/2007.14601), [CUP](https://www.cambridge.org/core/books/quantum-atom-optics/2D867888B5C666D3A936F1C942C99568))


Lecture notes:

* Reinhard Werner, _Mathematical methods of quantum information theory_, 18 lecture course (2017) video playlist [yt](https://www.youtube.com/playlist?list=PLDfPUNusx1EoBAn8vXYjcF95R7mI_eR6o)

See also:

* Wikipedia [quantum information](https://en.wikipedia.org/wiki/Quantum_information), [Bures metric](https://en.wikipedia.org/wiki/Bures_metric)


Further original articles:

* Carmen Maria Constantin, _Sheaf-theoretic methods in quantum mechanics and quantum information theory_, PhD thesis, Oxford 2015 [arxiv/1510.02561](https://arxiv.org/abs/1510.02561)

* [[Samson Abramsky]], Adam Brandenburger, _The sheaf-theoretic structure of nonlocality and contextuality_, [arxiv/1102.0264](https://arxiv.org/abs/1102.0264)

* Dominik Šafránek, _Simple expression for the quantum Fisher information matrix), Phys. Rev. A97 (2018) [doi](https://doi.org/10.1103/PhysRevA.97.042322)


* [[Roman Orus]], _Entanglement, quantum phase transitions and quantum algorithms_ ([arXiv:quant-ph/0608013](https://arxiv.org/abs/quant-ph/0608013))

> In Chapter 1 we consider the irreversibility of renormalization group flows from a quantum information perspective by using majorization theory and conformal field theory.

Quantum information in relation to the [[representation theory of the symmetric group]]:

* [[Alonso Botero]], *Quantum Information and the Representation Theory of the Symmetric Group*, Rev. colomb. mat. vol.50 no. 2 Bogotá July/Dec. 2016 ([doi:10.15446/recolma.v50n2.62210](https://doi.org/10.15446/recolma.v50n2.62210), [pdf](http://www.scielo.org.co/pdf/rcm/v50n2/v50n2a05.pdf))




[[!redirects quantum information theory]]
