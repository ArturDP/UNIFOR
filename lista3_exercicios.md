# UNIFOR
Disciplina: Raciocinio Logico algoritimico
Orientador: Prof. Ricardo Carubbi

## Lista 3 de exercicios

### Exercicio 01
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um numero: }}
B --> C[/num/]
C --> D{num >= 0}
D --N--> E{{O número deve ser positivo!}}
E --> F([FIM])
D --S--> G[ resto = num % 2]
G --> H{resto == 0}
H --S--> I{{O número é par}}
H --N--> J{{O número é ímpar}}
I & J --> F
```
#### Pseudocódigo
```
ALGORITMO verfica_par_impar
DECLARE num: int, resto
INICIO
ESCREVA "Digite um número: "
LEIA num
ENQUANTO num < 0 FAÇA


	ESCREVA “Digite um número positivo: "
	LEIA num
FIM_ENQUANTO
resto = num % 2
SE resto == 0 ENTÃO
	ESCREVA "O número é par"
SENÃO
	ESCREVA "O número é ímpar"
FIM
 
```	
#### TESTE
| num | resto | num >= 0 | resto == 0 | Saída |
| --| --| --| --| -- |
| -1 | False |  |  | "O número deve ser positivo"
| 0 | True | 0 | True | "O número é par!"|
| 10 | True | 0 | True | "O número é par!"|
| 11 | True | 1 | False | "O número é ímpar!"|

### Exercicio 02
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.
```mermaid
flowchart TD

A([INICIO]) --> B["i = 0"]
B --> C{i <= 30}
C -- sim --> D{i%3 == 0}
C -- não --> E([FIM])
D -- não --> F["i=+1"]
F --> C
D -- sim --> G{{"exibir i"}}
G --> F
```
#### Pseudocódigo
```
