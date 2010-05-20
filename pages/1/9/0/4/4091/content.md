This is the graphviz source for an expanded version of the diagram at [[TVS relationships]].  The intention is to see if it is possible to make this into a lattice, so that the arrows are not just one-way implications, but also theorems such as "Quasi-Barrelled and Quasi-Complete implies Barrelled" can be read off the diagram.

For instructions on how to generate the SVG from this source, see [[lctvs dot source]].  The current SVG can be seen at [[lattice of TVS properties]].

~~~~
digraph LCTVS {
mode=KK;
splines=true;
overlap=orthoyx;
// style for locally convex topological space properties
node [shape=box, style=filled, fillcolor="#ffffbb"];
LCTVS [tooltip="Locally Convex Topological Vector Space", href="http://ncatlabe.org/nlab/show/LCTVS"];
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
Re [tooltip="Reflexive", href="http://ncatlab.org/nlab/show/reflexive topological vector space"];
Cn [tooltip="Convenient", href="http://ncatlab.org/nlab/show/convenient space"];
SR [tooltip="Semi-Reflexive", href="http://ncatlab.org/nlab/show/semi-reflexive topological vector space"];
Bo [tooltip="Bornological", href="http://ncatlab.org/nlab/show/bornological topological vector space"];
LC [tooltip="Locally Complete", href="http://ncatlab.org/nlab/show/locally complete topological vector space"];
QC [tooltip="Quasi-Complete", href="http://ncatlab.org/nlab/show/quasi-complete topological vector space"];
QB [tooltip="Quasi-Barrelled", href="http://ncatlab.org/nlab/show/quasi-barrelled topological vector space"];
Mk [tooltip="Mackey", href="http://ncatlab.org/nlab/show/Mackey topological vector space"];
LF [tooltip="strict inductive sequence of Fr&#233;chet spaces", href="http://ncatlab.org/nlab/show/LF space"];
LB [tooltip="strict inductive sequence of Banach spaces", href="http://ncatlab.org/nlab/show/LB space"];
AP [tooltip="Approximation Property", href="http://ncatlab.org/nlab/show/approximation property"];
Pt [tooltip="Ptak Space", href="http://ncatlab.org/nlab/show/Ptak space"];
BC [tooltip="Br Space", href="http://ncatlab.org/nlab/show/Ptak space"];
// Style for topological vector space properties
node [fillcolor="#ffbbff"];
TVS [tooltip="Topological Vector Space", href="http://ncatlabe.org/nlab/show/TVS"];
Bl [tooltip="Barrelled", href="http://ncatlab.org/nlab/show/barrelled topological vector space"];
// Style for topological properties
node [fillcolor="#bbffff"];
TS [tooltip="Topological Space", href="http://ncatlab.org/nlab/show/topological space"];
Pc [tooltip="Paracompact", href="http://ncatlab.org/nlab/show/paracompact space"];
CP [tooltip="Countably Paracompact", href="http://ncatlab.org/nlab/show/countably paracompact space"];
Sq [tooltip="Sequentially Complete", href="http://ncatlab.org/nlab/show/sequentially complete topological vector space"];
Nm [tooltip="Normal", href="http://ncatlab.org/nlab/show/normal topological space"];
Cp [tooltip="Complete", href="http://ncatlab.org/nlab/show/complete topological vector space"];
Br [tooltip="Baire", href="http://ncatlab.org/nlab/show/Baire topological vector space"];
Me [tooltip="Metrisable", href="http://ncatlab.org/nlab/show/metrisable topological vector space"];
Se [tooltip="Separable", href="http://ncatlab.org/nlab/show/separable space"];
SC [tooltip="Second-Countable", href="http://ncatlab.org/nlab/show/Second-Countable topological vector space"];
// Style for nodes with no label
node [shape=circle, width=.2, fillcolor="#ffffbb"];
QCBo [label="", tooltip="Quasi-Complete and Bornological", href="http://ncatlab.org/nlab/show/bornological topological vector space"];
QCQB [label="", tooltip="Quasi-Complete and Quasi-Barrelled", href="http://ncatlab.org/nlab/show/barreled topological vector space"];
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
LCTVS -> TVS -> TS;
}
~~~~