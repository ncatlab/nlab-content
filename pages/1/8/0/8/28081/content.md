
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functorial quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--



\tableofcontents


## Idea

When ([[classical field theory|classical]] or [[quantum field theory]]) [[field theory]] is expressed as [[extended field theory|extended]] [[functorial field theory]], hence as ([[(infinity,n)-functor|$(\infty,n)$-]])[[functors]] on some ([[(infinity,n)-category of cobordisms|$(\infty,n)$-]])[[category of cobordisms]], there is the notion of *[[natural transformation]]* between such functors/field theories. 

By the *[[holographic principle of higher category theory]]* the components of such [[natural transformations]] are themselves close to being higher functors on cobordisms themselves, but in one dimension lower, hence may be understood as a generalized form of (extended) functorial field theories themselves.
But the lack of exact functoriality of these transformation components means that there is (in general) a "twist" or "[[quantum anomaly|anomaly]]".

In the archetypal case one considers transformations 
$$
  twFFT_{d} \colon  \mathbf{1} \Rightarrow FFT_{d+1}
$$ 
out of the [[tensor unit]] $\mathbf{1}$ in the given ([[higher category|higher]]) [[category]] of field theories, in which case such *twisted functorial field theories* (twFFT) have also been called *relative* FFTs, relative to the given $FFT_{d+1}$.

This is closely analogous and related to how [[sections]] of a [[vector bundle]] --- hence *twisted functions*: twisted by the bundle --- are equivalently morphism of vector bundles from the tensor unit bundle (the [[trivial bundle|trivial]] [[line bundle]]).

These days, also the term *symmetry TFT* (for the $FFT_{d+1}$) is popular.

In the case $d = 2$, the components that [[natural transformations]] between [[TQFT]] [[3-functors]] assign to [[surfaces]] are [[3-morphisms]] between [[2-morphisms]] making "tin-can diagrams" (vividly so when using [[globular set|globular]] [[geometric shape for higher structures|shapes of higher morphisms]], whence the original slogan: "*[D-branes from tin cans](https://www.google.com/search?q=schreiber+D-branes+from+tin-cans)*") as shown in the last row of the following table (from [Schreiber 2006](#Schreiber2006)):

\begin{imagefromfile}
    "file_name": "TwistedQFTAndHolographicCats.png",
    "width": 600,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}

More informal but more popular these days is a corresponding schematic diagram of the following form (from [ABBGN24](#ABBGN2024)):

\begin{imagefromfile}
    "file_name": "SymmetryTFT-ABBGN2024.png",
    "width": 500,
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 30
    }
\end{imagefromfile}



## References

The notion of *[[twisted functorial field theory|twisted]]* or *[[relative functorial field theory|relative]]* functorial field theory as [[natural transformations]] between FQFTs was popularized in:

* [[Stephan Stolz]], [[Peter Teichner]]: *Twisted field theories*, §5 in: *Supersymmetric field theories and generalized cohomology*, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.): *[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]*, Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:1108.0189](https://arxiv.org/abs/1108.0189), [ams:pspum-83](https://bookstore.ams.org/pspum-83/)&rbrack;

* [[Daniel Freed]], [[Constantin Teleman]]: *Relative quantum field theory*, Commun. Math. Phys. **326** (2014) 459–476  &lbrack;[arXiv:1212.1692](https://arxiv.org/abs/1212.1692), [doi:10.1007/s00220-013-1880-1](https://doi.org/10.1007/s00220-013-1880-1)&rbrack;

but the observation of the phenomenon is already in

* {#Schreiber2006} [[Urs Schreiber]]: "A kind of Holography", section 4 of: *On 2D QFT -- from Arrows to Disks* (2006) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schreiber/ad.pdf), [pdf](/schreiber/files/Schreiber-ArrowsToDisks.pdf)&rbrack;

  presented as: 

  *Quantum 2-States: Sections of 2-vector bundles*, talk at *[Higher categories and their applications](https://www.fields.utoronto.ca/programs/scientific/06-07/homotopy/highercat/index.html)*, Fields Institute (Jan 2007) &lbrack;[pdf](https://www.math.uni-hamburg.de/home/schreiber/atd.pdf), [pdf](/schreiber/files/schreiber_2VectorSpaces_Jan2007.pdf)&rbrack;

  which [was communicated](https://golem.ph.utexas.edu/category/2007/06/extended_quantum_field_theory.html) to the above authors at:

  *[Workshop on Elliptic Cohomology](https://www.zmp.uni-hamburg.de/events/workshop-cohomology.html)*, Hamburg (June 2007) &lbrack;poster: [pdf](https://www.zmp.uni-hamburg.de/events/workshop-cohomology/files/workshop-ellcoh-cdr.pdf), [[WorkshopEllipticCohomologyPoster-Hamburg2007.pdf:file]]&rbrack;

and then in:

* {#SchommerPries} [[Chris Schommer-Pries]], pp. 65 in: _Topological defects and classifying local topological field theories in low dimension_, talk at *[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]* &lbrack;[[SchommerPriesDefects.pdf:file]]&rbrack;

Further mathematical development:

* [[Theo Johnson-Freyd]], [[Claudia Scheimbauer]]: *(Op)lax natural transformations, twisted quantum field theories, and "even higher" Morita categories*, Advances in Mathematics **307** (2017) 147-223 &lbrack;[arXiv:1502.06526](https://arxiv.org/abs/1502.06526), [doi:10.1016/j.aim.2016.11.014](https://doi.org/10.1016/j.aim.2016.11.014)&rbrack;

* [[Claudia Scheimbauer]], Thomas Stempfhuber: *Relative field theories via relative dualizability*, Lett. Math. Phys. **115** 65 (2025) &lbrack;[arXiv:2312.05051](https://arxiv.org/abs/2312.05051), [doi;10.1007/s11005-025-01948-7](https://doi.org/10.1007/s11005-025-01948-7)&rbrack;

Meanwhile the perspective has become popular in [[theoretical physics]] under various names such as "[[quantum anomaly|anomaly]] field theory", for instance:

* [[Samuel Monnier]]: *A Modern Point of View on Anomalies*, in: proceedings of *[[Higher Structures in M-Theory 2018]]*, Fortschritte der Physik **67** 8-9 (2019) 1910012 &lbrack;[arXiv:1903.02828](https://arxiv.org/abs/1903.02828), [doi:10.1002/prop.201910012](https://doi.org/10.1002/prop.201910012), video:[yt](https://youtu.be/PAKf_o5XCek)&rbrack;

and "symmetry TFT", for instance:

* Fabio Apruzzi, [[Federico Bonetti]], Iñaki García Etxebarria, Saghar S. Hosseini, [[Sakura Schäfer-Nameki]]: *Symmetry TFTs from String Theory*, Commun. Math. Phys. **402**  (2023) 895–949 &lbrack;[arXiv:2112.02092](https://arxiv.org/abs/2112.02092), [doi:10.1007/s00220-023-04737-2](https://doi.org/10.1007/s00220-023-04737-2)&rbrack;

* {#ABBGN2024} Riccardo Argurio, Francesco Benini, Matteo Bertolini, Giovanni Galati, Pierluigi Niro: *On the Symmetry TFT of Yang-Mills-Chern-Simons theory*,  J. High Energ. Phys. **2024** 130 (2024) &lbrack;<a href="https://doi.org/10.1007/JHEP07(2024)130">doi:10.1007/JHEP07(2024)130</a>, [arXiv:2404.06601](https://arxiv.org/abs/2404.06601)&rbrack;


[[!redirects twisted functorial field theories]]

[[!redirects relative functorial field theory]]
[[!redirects relative functorial field theories]]

[[!redirects relative field theory]]
[[!redirects relative field theories]]

[[!redirects anomaly field theory]]
[[!redirects anomaly field theories]]

[[!redirects symmetry TFT]]
[[!redirects symmetry TFTs]]

