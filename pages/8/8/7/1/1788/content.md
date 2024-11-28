
### Mix, isomix and compact linearly distributive categories

There are a series of structural steps by which linearly distributive categories collapses to a monoidal categories as shown in the picture below. 

\begin{center}
\begin{imagefromfile}
        "file_name": "LDC_schematic.jpg",
        "width": 600,
        "unit": "px"
\end{imagefromfile}
\end{center}
 
A **mix category** is an LDC with a **mix map** ${ m}:\bot\to\top$, and a  such that:

1) The following diagram commutes

\begin{tikzcd}
	{A \otimes B} & {A \otimes(\bot \oplus B)} & {(A \otimes \bot) \oplus B} \\
	{(A \oplus \bot) \otimes B} && {(A  \otimes \top) \oplus B} \\
	{A \oplus ( \bot \otimes B)} & {A \oplus ( \top \otimes B)} & {A \oplus B}
	\arrow["\simeq", from=1-1, to=1-2]
	\arrow["\simeq"', from=1-1, to=2-1]
	\arrow["{{mx} := }"{description}, dashed, from=1-1, to=3-3]
	\arrow["{\delta^L}", from=1-2, to=1-3]
	\arrow["{A \otimes {m} \oplus B}", from=1-3, to=2-3]
	\arrow["{\delta^R}"', from=2-1, to=3-1]
	\arrow["\simeq", from=2-3, to=3-3]
	\arrow["{A \oplus {m} \otimes B}"', from=3-1, to=3-2]
	\arrow["\simeq"', from=3-2, to=3-3]
\end{tikzcd}


2) The map, $\mx_{A,B}: A \otimes B \to A \oplus B$, called the mixor is natural in both the arguments.

An **isomix category** is a mix category in which the mix map is a natural isomorphism, $m: \bot \simeq \top$.

In an isomix category, the mixor is automatically a natural transformation. The mix map being an isomorphism does not imply that the mixor is a natural isomorphism.

An isomix category in which the mixor is a natural isomorphism is a compact LDC. The term "compact" here refers to the fact that both the monoidal structures are isomorphic. All compact LDCs are linearly equivalent to the underlying monoidal categories on the tensor $\otimes$ and the par $\oplus$.
