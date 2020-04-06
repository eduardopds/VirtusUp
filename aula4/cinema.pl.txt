pessoa(ana).
pessoa(bia).
pessoa(cris).
pessoa(duda).
pessoa(eva).

anabia(ana,_,bia,_,_).
anabia(ana,_,_,bia,_).
anabia(ana,_,_,_,bia).
anabia(_,ana,_,bia,_).
anabia(_,ana,_,_,bia).
anabia(_,_,ana,_,bia).

anabia(bia,_,ana,_,_).
anabia(bia,_,_,ana,_).
anabia(bia,_,_,_,ana).
anabia(_,bia,_,ana,_).
anabia(_,bia,_,_,ana).
anabia(_,_,bia,_,ana).

criseva(cris,eva,_,_,_).
criseva(_,_,_,eva,cris).

verifica(A,B,C,D,E) :- A \= B, A\=C, A\=D, A\=E, B\=C, B\=D,B\=E,C\=D,C\=E,D\=E.
cinema(A,B,C,D,E):- pessoa(A),pessoa(B),pessoa(C),pessoa(D),pessoa(E),verifica(A,B,C,D,E),criseva(A,B,C,D,E),anabia(A,B,C,D,E).


