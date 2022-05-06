\begin{tikzcd}[column sep=normal, row sep=large]
	& 
	& 
	& \scriptsize \text{metrisable}
	& 
	& 
	\\
	& \text{second countable}
	& 
	& \sigma\text{-locally finite base} 
	& \sigma\text{-locally discrete base} 
	& \text{first countable}
	\\[.9em]
	  \text{separable}
	& 
	& \text{Lindel\"of}
	& \substack{\text{weakly Lindel\"of }\wedge \\ \sigma\text{-locally finite base}}
	& 
	& \text{Fr\'echet-Urysohn}
	\\
	& 
	& 
	& 
	& 
	& \text{sequential}
	\\
	  \text{countable chain condition}  
	& 
	& \text{weakly Lindel\"of}
	& 
	& 
	& \text{countably tight}
	\arrow[Rightarrow, from=3-4, to=2-2]
	\arrow[Rightarrow, from=3-4, to=5-3]
	\arrow[Rightarrow, from=3-4, to=2-5]
	\arrow[Rightarrow, from=2-2, to=3-1, 
		"\substack{\text{countable}\\ \text{choice}}" description] 
	\arrow[Rightarrow, from=2-2, to=3-3,
		"\substack{\text{countable}\\ \text{choice}}" description] 
	\arrow[Rightarrow, from=3-1, to=3-3, "\text{if $X$ metacompact}"] 
	\arrow[Rightarrow, from=3-3, to=5-3]
	\arrow[Rightarrow, from=3-1, to=5-3, "\text{AC}" {description, near end}]
	\arrow[Rightarrow, from=2-2, to=2-4]
	\arrow[Rightarrow, from=3-1, to=5-1]
	\arrow[Rightarrow, from=2-4, to=2-5]
	\arrow[Rightarrow, from=2-5, to=2-6]
	\arrow[Rightarrow, from=2-6, to=3-6]
	\arrow[Rightarrow, from=3-6, to=4-6]
	\arrow[Rightarrow, from=4-6, to=5-6]
	\arrow[Rightarrow, from=1-4, to=2-4]
	\arrow[Rightarrow, from=2-5, to=1-4, bend right, "\substack{\text{Nagata-Smirnov metrization theorem:}\\ \text{if $X$ regular and } \mathrm{T}_2}" right]
	\arrow[Rightarrow, from=5-1, to=3-3, "\text{AC}" {description, near end}, "\text{if $X$ paracompact}" {near start, below right}]
\end{tikzcd}
\begin{tikz}[remember picture, overlay]
        \node[rectangle, draw, blue,
                fit={(tikz@f@1-1-1) (tikz@f@1-1-3)  (tikz@f@1-2-2)}
            ] 
        {};
\end{tikz}

