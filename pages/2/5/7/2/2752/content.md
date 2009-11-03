(idea : table of examples for the adjunction homset isomorphisms or the triangle identities)


homset version:

$$
\array {

\arrayopts{\padding{150}\collines{solid}\rowlines{solid}}

& C & D & L & R & \sharp : C(X,RY) \to D(LX,Y) & \flat : D(LX,Y) \to C(X,RY) & (\flat) \circ (\sharp) = \id & (\sharp) \circ (\flat) = \id \\


binary products & C & C \times C & L X = (X,X) & R (X_1,X_2) = X_1 \times X_2 & 

f ^ \sharp = ( \pi_1 \circ f, \pi_2 \circ f ) &
(g_1,g_2)_\flat = \langle g_1 , g_2 \rangle &

\langle \pi_1 \circ f , \pi_2 \circ f \rangle = f &

(\pi_1 \circ \langle g_1 , g_2 \rangle 
, \pi_2 \circ \langle g_1 , g_2 \rangle ) =

(g_1 , g_2) \\

equalisers & C & (\cdot \doublerightarrow \cdot) \to C &
L X = (\id_X,\id_X) & R (g_1,g_2) = eq(g_1,g_2) &

&&&

}


$$



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




category: meta