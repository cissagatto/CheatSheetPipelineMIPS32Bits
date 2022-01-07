# Cheat Sheet Pipeline MIPS 32 Bits


https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-1.pdf

https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-3.pdf

https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-4.pdf

https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-5.pdf

https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-6.pdf

https://github.com/cissagatto/CheatSheetPipelineMIPS32Bits/blob/main/pipeline-resumo-7.pdf

## PRATIQUE

Questão sobre Hazards no pipeline de 32 bits do MIPS:

a) Existem conflitos nas sequências de instruções abaixo? Responda apenas SIM ou NÃO para cada sequência.

b) Quais tipos estão presentes? Responda estruturais, dados, e/ou controle para cada sequência.

c) É possível reordenar o código? Se sim, faça-o.

d) Desenhe o diagrama de pipeline usando a representação 4 para identificar e indicar onde estão os conflitos para cada uma das sequências.

e) Desenhe o diagrama de pipeline usando a representação 1 com a solução para os conflitos para cada uma das sequências.


1) 

add $s0, $t0, $t1

sub $t2, $s0, $t3

2)

lw $s0, 20($t1)

sub $t2, $s0, $t3

3)

lw $1, -70($2)

lw $2, 100($0)

4)

add $s4, $s5, $s6

beq $s1, $s2, 40

or $s7, $s8, $s9

5)

add $s4, $s5, $s6

beq $s1, $s2, 40

lw $s3, 300($s0)

6)

lw $t0, 0($s1)

lw $t2, 4($t1)

sw $t2, 0($t1)

sw $t0, 4($t1)

7)

lw $t1, 0($t0)

lw $t2, 4($t0)

add $t3, $t1, $t2

sw $t3, 12($t0)

lw $t4, 8($t0)

add $t5, $t1, $t4

sw $t5, 16($t0)

8)

lw $10, 20(1)

sub $11, $2, $3

add $12, $3, $4

lw $13, 24($1) 

add $14, $5, $6

9)

lw $s1, 100($t0)

lw $s2, 200($t0)

lw $s3, 300($t0)

lw $s4, 400($t0)

lw $s5, 500($t0)


10)

lw $s1, 100($t0)

add $t7, $t2, $t3

sub $t4, $t5, $t6

lw $s5, 500($t0)

11)

sub $s2, $1, $4

and $12, $2, $5

or $13, $6, $2

add $14, $2, $2

sw $15, 100($2)

12)

lw $2, 20($1)

and $4, $2, $5

or $8, $2, $6

add $9, $4, $2

slt $1, $6, $7

13)

beq $1, $3, 28

and $12, $2, $5

or $13, $6, $2

add $14, $2, $2

lw $4, 50($7)

14)

lw $t0, 10($t1)

sw $13, 20($t4)

add $t5, $t6, $t7

sub $t8, $t9, $s5

15)

beq $s0, $s1, else

add $t0, $s2, $s3

add $t1, $s4, $s5

beq $zero, $zero, end

else: sub $t0, $s2, $s3

sub $t1, $s4, $s5

end: sw $t0, 0($t7)

sw $t1, 4($t7)

16)

lw $2, 20($1)

and $4, $2, $5

or $8, $2, $6

add $9, $4, $2

slt $1, $6, $7

17)

sub $t2, $t1, $t3

and $t4, $t2, $t5

or $t7, $t6, $t2

add $t8, $t2, $t2

sw $t9, 100($t2)

18)

sub $2, $1, $3

and $4, $2, $5

or $4, $4, $2

add $9, $4, $2

19)

add $t1, $t0, $t0

addi $t2, $t0, 5

addi $t4, $t1, 5

20)

addi $t1, $t0, 1

addi $t4, $t0, 2

addi $t3, $t0, 2

addi $t3, t0, 4

addi $t5, $t0, 5

21)

sub $10, $4, $8

beq $1, $3, 7

and $12, $2, $5

or $13, $2, $6

add $14, $4, $2

slt $15, $6, $7

lw $4, 50($7)


22)

sub $11, $2, $4

and $12, $2, $5

or $13, $2, $5

add $1, $2, $1

slt $15, $6, 7

lw $16, 50($7)

23)

lw $t0, 0($s1)

addu $t0, $t0, $s2

sw $t0, 0($s1)

addi $s1, $s1, -4

bne $s1, $zero, LOOP
