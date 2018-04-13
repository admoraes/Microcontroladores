Para todas as questões, considere que as variáveis `f`, `g`, `h`, `i` e `j` são do tipo inteiro (16 bits na arquitetura do MSP430), e que o vetor `A[]` é do tipo inteiro. Estas variáveis estão armazenadas nos seguintes registradores:

- f: R4
- g: R5
- h: R6
- i: R7
- j: R8
- A: R9

Utilize os registradores R11, R12, R13, R14 e R15 para armazenar valores temporários.

1. Traduza as seguintes linhas em C para a linguagem assembly do MSP430. Utilize somente as seguintes instruções: mov.w, add.w, sub.w, clr.w, dec.w, decd.w, inc.w e incd.w.

int mult_unsigned (unsigned int a, unsigned int b){

int soma = 0;

  if (a == 0 || b == 0) return 0;
  else{
    while(b != 0){
      soma += a;
      b--;
    }
  }
}

mult_unsigned:

tst.w R15             ;a == 0?
jeq resultado_nulo

tst.w R14             ;b == 0?
jeq resultado_nulo

mult_unsigned_else:
R15

resultado_nulo:
clr.w R15             ;a*b = 0
RET

(a) `f *= 5;`

(b) `g *= 6;`

(d) `A[2] = 6*A[1] + 5*A[0];`

(e) `A[3] = 3*f - 5*h;`

(f) `A[5] = 6*(f - 2*h);`
