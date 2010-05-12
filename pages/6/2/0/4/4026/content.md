The graph on [[topological vector spaces]] was created using [Graphviz](http://www.graphviz.org/).  The source is laid out below, the command to generate the diagram is:

~~~
dot -Tsvg lctvs.dot -o lctvs.svg
~~~

The XHTML comments need to be stripped from the resulting SVG, a simple script to do this is

~~~
perl -i.orig -ne '/&lt;!--/ || print' -f lctvs.svg
~~~

These can, of course, be combined into:

~~~
dot -Tsvg lctvs.dot | perl -ne '&lt;!--/ || print' > lctvs.svg
~~~

The top lines also need to be deleted (everything up to the opening `svg` tag) but this is simple to do upon cut-and-pasting into the nLab.

The source for the diagram follows.  Apart from a few options at the start, it consists of a list of **nodes** followed by a list of connections between the nodes.  The initial word `digraph` indicates that this is a _directed_ graph and so the edges are written as `->`.  For more on the syntax and options see the Graphviz documentation.

~~~
digraph LCTVS {
mode=KK;
splines=true;
overlap=orthoyx;
FD [label="Finite-Dimensional", href="http://ncatlab.org/nlab/show/Finite-Dimensional topological vector space", shape=box];
Hi [label="Hilbert", href="http://ncatlab.org/nlab/show/Hilbert topological vector space", shape=box];
SC [label="Second-Countable", href="http://ncatlab.org/nlab/show/Second-Countable topological vector space", shape=box];
Nu [label="Nuclear", href="http://ncatlab.org/nlab/show/Nuclear topological vector space", shape=box];
Ba [label="Banach", href="http://ncatlab.org/nlab/show/Banach topological vector space", shape=box];
IP [label="Inner-Product", href="http://ncatlab.org/nlab/show/Inner-Product topological vector space", shape=box];
Se [label="Separable", href="http://ncatlab.org/nlab/show/Separable topological vector space", shape=box];
Mo [label="Montel", href="http://ncatlab.org/nlab/show/Montel topological vector space", shape=box];
Sc [label="Schwartz", href="http://ncatlab.org/nlab/show/Schwartz topological vector space", shape=box];
UB [label="Ultrabornological", href="http://ncatlab.org/nlab/show/Ultrabornological topological vector space", shape=box];
Fr [label="Fr&#233;chet", href="http://ncatlab.org/nlab/show/Fr&#233;chet topological vector space", shape=box];
DF [label="Dual-Fr&#233;chet", href="http://ncatlab.org/nlab/show/Dual-Fr&#233;chet topological vector space", shape=box];
No [label="Normed", href="http://ncatlab.org/nlab/show/Normed topological vector space", shape=box];
Re [label="Reflexive", href="http://ncatlab.org/nlab/show/Reflexive topological vector space", shape=box];
Cn [label="Convenient", href="http://ncatlab.org/nlab/show/Convenient topological vector space", shape=box];
Cp [label="Complete", href="http://ncatlab.org/nlab/show/Complete topological vector space", shape=box];
Br [label="Baire", href="http://ncatlab.org/nlab/show/Baire topological vector space", shape=box];
Me [label="Metrisable", href="http://ncatlab.org/nlab/show/Metrisable topological vector space", shape=box];
SR [label="Semi-Reflexive", href="http://ncatlab.org/nlab/show/Semi-Reflexive topological vector space", shape=box];
Bo [label="Bornological", href="http://ncatlab.org/nlab/show/Bornological topological vector space", shape=box];
LC [label="Locally Complete", href="http://ncatlab.org/nlab/show/Locally Complete topological vector space", shape=box];
Bl [label="Barrelled", href="http://ncatlab.org/nlab/show/Barrelled topological vector space", shape=box];
QC [label="Quasi-Complete", href="http://ncatlab.org/nlab/show/Quasi-Complete topological vector space", shape=box];
Pc [label="Paracompact", href="http://ncatlab.org/nlab/show/Paracompact topological vector space", shape=box];
QB [label="Quasi-Barralled", href="http://ncatlab.org/nlab/show/Quasi-Barralled topological vector space", shape=box];
Sp [label="Sequentially Complete", href="http://ncatlab.org/nlab/show/Sequentially Complete topological vector space", shape=box];
Nm [label="Normal", href="http://ncatlab.org/nlab/show/Normal topological vector space", shape=box];
Mk [label="Mackey", href="http://ncatlab.org/nlab/show/Mackey topological vector space", shape=box];
CP [label="Countably Paracompact", href="http://ncatlab.org/nlab/show/Countably Paracompact topological vector space", shape=box];
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
Cp -> LC;
Cp -> QC;
Br -> Bl;
Me -> Bo;
Me -> Pc;
SR -> QC;
Bo -> QB;
Bl -> QB;
QC -> Sp;
Pc -> Nm;
QB -> Mk;
Nm -> CP;
}
~~~