# Exercícios de Descrição Estrutural

##questão 1

%%file exercicio.sv

Módulo exercicio

module exercicio(a,b,c,z);

// Declaração de portas input a, b, c; ouput z; // Variáveis (fios) intermediárias wire nc, nb, na, p0, p1, p2;

// Estrutura not not0 (nc, c);

not not1 (nb, b);

not not2 (na, a);

and and0 (p0, c, nb);

or or0 (p1, nc, a);

and and1 (p2, na, b);

or orf (z, p0, p1, p2);

endmodule

##questão 2

module exercicio2(i0,i1,a,q);

input i0,i1,a; output q;

wire p1,p2,p3;

nand nand0 (p1,a,a);
nand nand1 (p2,i0,a);
nand nand2 (p3,i1,p1);
nand nand3 (q,p2,p3);

endmodule

##questão 3

module exercicio3(a,b,c,d,e);

input a,b; output c,d,e;

wire n1,n2,p1,p2;

not not1 (n1,a);
not not2 (n2,b);
and and1 (p1,b,n1);
and and2 (p2,a,n2);
and andc (c,a,n2);
and and3 (e,b,n1);
or or1 (d,p1,p2);

endmodule
