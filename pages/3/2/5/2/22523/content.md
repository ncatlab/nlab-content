

#Contents#
* table of contents
{:toc}

## Idea

The *HaPPY code* is a [[quantum error correction code]] (a class of such codes really, indexed by a "cutoff" [[natural number]]) which is thought to exhibit characteristic properties akin to the encoding of [[bulk]]-[[quantum states]] by [[boundary field theory|boundary]]-states expected in the [[AdS/CFT correspondence]]. In particular, the HaPPY code (or rather the [[tensor network]] that defines it) exhibits a discretized form of the [[Ryu-Takayanagi formula]] for [[holographic entanglement entropy]].

Concretely, the the HaPPY [[code subspace]] is the [[image]] of the [[linear map]] formed by:


\begin{imagefromfile}
    "file_name": "HaPPYCodeTesselation.jpg",
    "float": "right",
    "width": 440,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [Harlow 18](#Harlow18)"
\end{imagefromfile}


1. picking a [[perfect tensor]] $T$ of [[rank]] 6;

1. picking a finite cutoff of the [[pentagon|pentagonal]] [[tesselation]] of the [[hyperbolic plane]];

1. regarding its [[Poincaré duality|Poincaré dual]] [[graph]] as a [[tensor network]] ([[string diagram]] in [[finite-dimensional vector spaces]]) by 

   1. assigning $T$ to each [[vertex]] at the center of the [[pentagons]] (show in blue), with 5 of its indices contracted with its neighbours in the hyperbolic plane,

   1. and its 6th uncontracted index remaining as an input (shown in red);

   1. regading the uncontrated edges at the cutoff boundary as output (shown in white)

and thus as a [[linear map]] form the [[tensor product]] over the [[bulk]]-[[vertices]] to the [[tensor product]] over the edges sticking out over the boundary.

## Related concepts

* [[Majorana dimer code]]

## References

Tha HaPPY code is due to 

* {#PYHP15} [[Fernando Pastawski]], [[Beni Yoshida]], [[Daniel Harlow]], [[John Preskill]], _Holographic quantum error-correcting codes: Toy models for the bulk/boundary correspondence_, JHEP 06 (2015) 149 ([arXiv:1503.06237](https://arxiv.org/abs/1503.06237))

following a precursor observation in

* {#ADH14} [[Ahmed Almheiri]], [[Xi Dong]], [[Daniel Harlow]], _Bulk Locality and Quantum Error Correction in AdS/CFT_, JHEP 1504:163,2015 ([arXiv:1411.7041](https://arxiv.org/abs/1411.7041))


Review in:

* {#Harlow18} [[Daniel Harlow]], _TASI Lectures on the Emergence of Bulk Physics in AdS/CFT_ ([arXiv:1802.01040](https://arxiv.org/abs/1802.01040))

See also:

* Elliott Gesteau, Monica Jinwoo Kang, *The infinite-dimensional HaPPY code: entanglement wedge reconstruction and dynamics* ([arXiv:2005.05971](https://arxiv.org/abs/2005.05971))


[[!redirects HaPPY codes]]


