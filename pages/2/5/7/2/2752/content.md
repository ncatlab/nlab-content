(idea : table of examples for the triangle identities)

though right now this seems to be more confusing than instructive ;)

## Examples

$$


\array {

\arrayopts{\padding{100}\collines{solid}\rowlines{solid}}


C & D & L & R & \eta : \id \implies R L & \epsilon : L R \implies \id & R \epsilon \circ \eta R : R \to R & L \eta \circ \epsilon L : L \to L\\

C & C \times C & L X = (X,X) & R (X_1,X_2) = X_1 \times X_2 & 

\array {
\eta_X : X \to X \times X\\
\eta_X = \langle \id_X,\id_X \rangle 


}
&

\array { 

\epsilon_{(X_1,X_2)} : (X_1 \times X_2, X_1 \times X_2) \to (X_1, X_2)\\
\epsilon_{(X_1,X_2)} = ( \pi_1 , \pi_2 )

}
& 

\array {
(R \epsilon \circ \eta R)_{X_1,X_2} =\\ 
R( \pi_1 , \pi_2 ) \circ \eta_{X_1 \times X_2} =\\
(\pi_1 \times \pi_2) \circ \langle \id_{X_1 \times X_2}, \id_{X_1 \times X_2} \rangle
}
&

\array {
(L \eta \circ \epsilon L)_X =\\ 
L (\langle \id_X , \id_X \rangle) \circ \epsilon_{X \times X} =\\
( \langle \id_X , \id_X \rangle
, \langle \id_X , \id_X \rangle )
\circ
( \pi_1 , \pi_2 )
}


}
$$ 