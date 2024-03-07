# UNIFOR
Disciplina: Raciocinio Logico algoritimico
Orientador: Prof. Ricardo Carubbi

## Lista 1 de exercicios

### Exercicio 01
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular a média aritmética entre duas notas de um aluno e mostrar sua situação, que pode ser aprovado ou reprovado.
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um numero}}
B --> C[/N1, N2/]
C --> D["MEDIA = (N1 +N2)/2"]
D --> E{<=5}
E --F--> F{{APROVADO}}
E --V--> G{{REPROVADO}}
F --> H([FIM])
G --> H
```
```

ALGORITIMO verifica se foi aprovado ou reprovado
DECLARE N1,N2
ESCREVA "Digite um numero"
LEIA numero
DECLARE MEDIA
CALCULE MEDIA (N1 + N2)/2
LEIA MEDIA
SE MEDIA for <=5 ENTAO
		ESCREVA "REPROVADO"
SENAO
		ESCREVA"APROVADO"
FIM
```
