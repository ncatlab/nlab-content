/*

[[!redirects lctvs lattice dot source]]

This is the graphviz source for an alternative version of the diagram at [[TVS relationships]].  The original intention was to see if it is possible to make this into a lattice.  However, that would have made the diagram too unwieldy.  Instead, the attempt is simply to expand and improve on the original diagram.

The current SVG can be seen at [[diagram of LCTVS properties]].

To recreate the SVG, the **whole** source of this page (or just the code below) should be run through `dot` (note that this part of the page is actually a comment in the dot source so doesn't get seen).  For example, assuming that the source has been saved as `lctvs.dot`, run:

    dot -Tsvg -o lctvs.svg lctvs.dot

~~~~
*/
digraph LCTVS {
splines=true;
overlap=orthoyx;
// style for properties relating to size
subgraph size {
style=none;
node [shape=box, style=filled, fillcolor="#ffffbb"];
FD [tooltip="Finite-Dimensional", href="http://ncatlab.org/nlab/show/Finite-Dimensional topological vector space"];
Hi [tooltip="Hilbert (technically, admits a Hilbertian structure)", href="http://ncatlab.org/nlab/show/Hilbert space"];
Nu [tooltip="Nuclear", href="http://ncatlab.org/nlab/show/Nuclear space"];
Ba [tooltip="Banach (technically, complete and normable)", href="http://ncatlab.org/nlab/show/Banach space"];
IP [tooltip="Topology from an inner-product", href="http://ncatlab.org/nlab/show/inner-product space"];
Mo [tooltip="Montel", href="http://ncatlab.org/nlab/show/Montel space"];
Sc [tooltip="Schwartz", href="http://ncatlab.org/nlab/show/Schwartz space"];
UB [tooltip="Ultrabornological", href="http://ncatlab.org/nlab/show/ultrabornological topological vector space"];
Fr [tooltip="Fr&#233;chet", href="http://ncatlab.org/nlab/show/Fr&#233;chet space"];
DF [tooltip="DF", href="http://ncatlab.org/nlab/show/DF topological vector space"];
No [tooltip="Normable space", href="http://ncatlab.org/nlab/show/normed vector space"];
Bo [tooltip="Bornological", href="http://ncatlab.org/nlab/show/bornological topological vector space"];
LF [tooltip="strict inductive sequence of Fr&#233;chet spaces", href="http://ncatlab.org/nlab/show/LF space"];
LB [tooltip="strict inductive sequence of Banach spaces", href="http://ncatlab.org/nlab/show/LB space"];
Me [tooltip="Metrisable", href="http://ncatlab.org/nlab/show/metrisable topological vector space"];
// no label
node [shape=circle, width=.2];
NuFr [label="", tooltip="Nuclear Fr&#233;chet space", href="http://ncatlab.org/nlab/show/nuclear topological vector space"];
}
// style for properties relating to completeness
subgraph complete {
node [shape=box, style=filled, fillcolor="#bbffff"];
LC [tooltip="Locally Complete", href="http://ncatlab.org/nlab/show/locally complete topological vector space"];
QC [tooltip="Quasi-Complete", href="http://ncatlab.org/nlab/show/quasi-complete topological vector space"];
Pt [tooltip="Ptak Space", href="http://ncatlab.org/nlab/show/Ptak space"];
BC [tooltip="Br Space", href="http://ncatlab.org/nlab/show/Ptak space"];
Sq [tooltip="Sequentially Complete", href="http://ncatlab.org/nlab/show/sequentially complete topological vector space"];
Cp [tooltip="Complete", href="http://ncatlab.org/nlab/show/complete topological vector space"];
}
// style for properties relating to duality
subgraph dual {
node [shape=box, style=filled, fillcolor="#ffbbff"];
Re [tooltip="Reflexive", href="http://ncatlab.org/nlab/show/reflexive topological vector space"];
SR [tooltip="Semi-Reflexive", href="http://ncatlab.org/nlab/show/semi-reflexive topological vector space"];
QB [tooltip="Quasi-Barrelled", href="http://ncatlab.org/nlab/show/quasi-barrelled topological vector space"];
Mk [tooltip="Mackey", href="http://ncatlab.org/nlab/show/Mackey topological vector space"];
Bl [tooltip="Barrelled", href="http://ncatlab.org/nlab/show/barrelled topological vector space"];
// no label
node [shape=circle, width=.2];
MkSR [label="", tooltip="Mackey and Semi-Reflexive", href="http://ncatlab.org/nlab/show/Mackey topological vector space"];
}
// Style for nodes with no label
node [shape=circle, width=.2, style=filled, fillcolor="#ffffbb"];
QCQB [label="", tooltip="Quasi-Complete and Quasi-Barrelled", href="http://ncatlab.org/nlab/show/barreled topological vector space"];
ReBa [label="", tooltip="Reflexive Banach space", href="http://ncatlab.org/nlab/show/reflexive topological vector space"];
ReFr [label="", tooltip="Reflexive Fr&#233;chet space", href="http://ncatlab.org/nlab/show/reflexive topological vector space"];


FD -> Hi;
Hi -> IP;
IP -> No;
No -> Me;
Hi -> ReBa;
ReBa -> Ba;
Ba -> LB;
Ba -> Fr;
Fr -> Me;
Fr -> LF;
LB -> LF;
Ba -> No;
FD -> NuFr;
Nu -> Sc;
NuFr -> Nu;
NuFr -> ReFr;
NuFr -> Mo;
No -> DF;
LB -> DF;

UB -> Bo;
Bo -> QB;
Bl -> QB;
QB -> Mk;
Re -> Bl;
Re -> MkSR;
QCQB -> Bl;
MkSR -> Mk;
MkSR -> SR;

Pt -> BC;
BC -> Cp;
Cp -> QC;
QC -> Sq;
Sq -> LC;

QCQB -> QC;
ReBa -> ReFr;
ReFr -> Re;
ReFr -> Fr;

SR -> QC;

Fr -> Pt;

Mo -> Re;

Me -> Bo;

LF -> UB;
UB -> QCQB;

/*
All the rest generates the key
*/

subgraph keys {
rank=same;
yFD  [label="",width=0,style=invis];
yDF [shape=box, style=solid, label="Key to symbols"];
yPt  [label="",width=0,style=invis];
}

subgraph cluster_key_col1 {
color=white;
node [label="",width=0,style=invis];
yHi;
yNu;
yBa;
yIP;
yMo;
ySc;
yUB;
yFr;
yZ1;
}

subgraph key1 {
node [shape=box, style=filled, fillcolor="#ffffbb"];
xFD [label="FD: Finite-Dimensional", href="http://ncatlab.org/nlab/show/Finite-Dimensional topological vector space"];
xHi [label="Hi: Hilbert (technically, admits a Hilbertian structure)", href="http://ncatlab.org/nlab/show/Hilbert space"];
xNu [label="Nu: Nuclear", href="http://ncatlab.org/nlab/show/Nuclear space"];
xBa [label="Ba: Banach (technically, complete and normable)", href="http://ncatlab.org/nlab/show/Banach space"];
xIP [label="IP: Topology from an inner-product", href="http://ncatlab.org/nlab/show/inner-product space"];
xMo [label="Mo: Montel", href="http://ncatlab.org/nlab/show/Montel space"];
xSc [label="Sc: Schwartz", href="http://ncatlab.org/nlab/show/Schwartz space"];
xUB [label="UB: Ultrabornological", href="http://ncatlab.org/nlab/show/ultrabornological topological vector space"];
xFr [label="Fr: Fr&#233;chet", href="http://ncatlab.org/nlab/show/Fr&#233;chet space"];
}

subgraph cluster_key_col2 {
color=white;
node [label="",width=0,style=invis];
yNo;
yBo;
yLF;
yLB;
yMe;
yLC;
yQC;
yZ2;
}

subgraph key2 {
node [shape=box, style=filled, fillcolor="#ffffbb"];
xDF [label="DF: DF", href="http://ncatlab.org/nlab/show/DF topological vector space"];
xNo [label="No: Normable space", href="http://ncatlab.org/nlab/show/normed vector space"];
xBo [label="Bo: Bornological", href="http://ncatlab.org/nlab/show/bornological topological vector space"];
xLF [label="LF: strict inductive sequence of Fr&#233;chet spaces", href="http://ncatlab.org/nlab/show/LF space"];
xLB [label="LB: strict inductive sequence of Banach spaces", href="http://ncatlab.org/nlab/show/LB space"];
xMe [label="Me: Metrisable", href="http://ncatlab.org/nlab/show/metrisable topological vector space"];
node [shape=box, style=filled, fillcolor="#bbffff"];
xLC [label="LC: Locally Complete", href="http://ncatlab.org/nlab/show/locally complete topological vector space"];
xQC [label="QC: Quasi-Complete", href="http://ncatlab.org/nlab/show/quasi-complete topological vector space"];
}

subgraph cluster_key_col3 {
color=white;
node [label="",width=0,style=invis];
yPt;
yBC;
ySq;
yCp;
yRe;
ySR;
yQB;
yMk;
yBl;
yZ3;
}


subgraph key2 {
node [shape=box, style=filled, fillcolor="#bbffff"];
xPt [label="Pt: Ptak Space", href="http://ncatlab.org/nlab/show/Ptak space"];
xBC [label="BC: Br Space", href="http://ncatlab.org/nlab/show/Ptak space"];
xSq [label="Sq: Sequentially Complete", href="http://ncatlab.org/nlab/show/sequentially complete topological vector space"];
xCp [label="Cp: Complete", href="http://ncatlab.org/nlab/show/complete topological vector space"];
node [shape=box, style=filled, fillcolor="#ffbbff"];
xRe [label="Re: Reflexive", href="http://ncatlab.org/nlab/show/reflexive topological vector space"];
xSR [label="SR: Semi-Reflexive", href="http://ncatlab.org/nlab/show/semi-reflexive topological vector space"];
xQB [label="QB: Quasi-Barrelled", href="http://ncatlab.org/nlab/show/quasi-barrelled topological vector space"];
xMk [label="Mk: Mackey", href="http://ncatlab.org/nlab/show/Mackey topological vector space"];
xBl [label="Bl: Barrelled", href="http://ncatlab.org/nlab/show/barrelled topological vector space"];
}

edge [style=invis];
yFD -> yHi;
yHi -> yNu;
yNu -> yBa;
yBa -> yIP;
yIP -> yMo;
yMo -> ySc;
ySc -> yUB;
yUB -> yFr;
yFr -> yZ1;

yDF -> yNo;
yNo -> yBo;
yBo -> yLF;
yLF -> yLB;
yLB -> yMe;
yMe -> yLC;
yLC -> yQC;
yQC -> yZ2;

yPt -> yBC;
yBC -> ySq;
ySq -> yCp;
yCp -> yRe;
yRe -> ySR;
ySR -> yQB;
yQB -> yMk;
yMk -> yBl;
yBl -> yZ3;


yFD -> xFD;
yHi -> xHi;
yNu -> xNu;
yBa -> xBa;
yIP -> xIP;
yMo -> xMo;
ySc -> xSc;
yUB -> xUB;
yFr -> xFr;
yDF -> xDF;
yNo -> xNo;
yBo -> xBo;
yLF -> xLF;
yLB -> xLB;
yMe -> xMe;
yLC -> xLC;
yQC -> xQC;
yPt -> xPt;
yBC -> xBC;
ySq -> xSq;
yCp -> xCp;
yRe -> xRe;
ySR -> xSR;
yQB -> xQB;
yMk -> xMk;
yBl -> xBl;




/*
FD -> Hi;
FD -> SC;
FD -> Nu;
FD -> Mo;
Hi -> Ba;
Hi -> IP;
Hi -> Re;
SC -> Me;
SC -> Se;
Mo -> Re;
Mo -> Pc;
Nu -> Sc;
Ba -> UB;
Ba -> Fr;
Ba -> DF;
Ba -> No;
IP -> No;
Re -> Bl;
Re -> SR;
UB -> Bo;
Fr -> Cn;
Fr -> Cp;
Fr -> Br;
Fr -> Me;
Cn -> Bo;
Cn -> LC;
Cp -> QC;
Br -> Bl;
Me -> Bo;
Me -> Pc;
SR -> QC;
Bo -> QB;
Bl -> QB;
QC -> Sq;
Pc -> Nm;
QB -> Mk;
Nm -> CP;
Sq -> LC;
LB -> LF;
LF -> Cp;
QCBo -> QC;
QCBo -> Bo;
QCBo -> Bl;
Hi -> AP;
Nu -> AP;
QCQB -> Bl;
QCQB -> QC;
Pt -> BC;
BC -> Cp;
Fr -> Pt;
Fr -> LF;
Ba -> LB;
*/
}

/*
~~~~
*/
