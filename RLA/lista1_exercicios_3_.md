
# UNIFOR
**Disciplina:** Raciocinio Logico algoritimico<br>
**Orientador:** Prof. Ricardo Carubbi

## Lista 1 de exercicios

### Exercicio 03
Represente, em fluxograma e pseudocódigo, um algoritmo para determinar se um número inteiro e positivo é par ou impar.
#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um numero}}
B --> C[/numero/]
C --> D{numero > 0}
D --F--> E{{o numero nao pode ser negativo!}}
E --> J
D --V--> F[resto = numero %2]
F --> G{resto == 0}
G --NAO--> H{{O numero é impar}}
G --SIM--> I{{O novo numero é par}}
H --> J([FIM])
I --> J
```
```
ALGORITIMO verificar_par_impar
DECLARE numero, resto INTEIRO
ESCREVA "Digite um numero"
LEIA numero
SE numero > 0 ENTAO
      SE resto = 0 ENTAO
	    ESCREVA "O numero é par1"
	SENAO
		ESCREVA "O numero é impar!"
SENAO
	ESCREVA "O numero deve ser positivo!"
FIM
```
 



