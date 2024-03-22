# UNIFOR
*Disciplina:* Raciocinio Logico algoritimico
*Orientador:* Prof. Ricardo Carubbi

## Lista 2 de exercicios

### Exercicio 01
Calcule a média de quatro números inteiros dados.
#### Fluxograma
```mermaid
flowchart TD
A([INICIO]) --> B{{Digite quatro numeros}}
B --> C[/N1, N2, N3, N4/]
C --> D["MEDIA = (N1 +N2 +N3 + N4)/2"]
D --> E{{CALCULAR MEDIA}}
E --> F([FIM])
```
```
ALGORITIMO “Cálculo da média de quatro valores”
DECLARE N1,N2,N3,N4
ESCREVA "Digite quatro numeros"
LEIA numero
DECLARE MEDIA
CALCULE MEDIA (N1 + N2 + N3 + N4)/2
LEIA MEDIA
FIM
```
#### Teste de mesa (0.5 ponto)

| Entrada1 | Entrada2 | Entrada3 | Entrada4 |  Saída   | 
|    --    |    --    |    --    |    --    |    --    | 
|    13    |    24    |    30    |   120    |  46.75   |
|    10    |    20    |    30    |    40    |   25.0   |

### Exercício 02 (2.5 pontos)
Leia uma temperatura dada em Celsius (C) e imprima o equivalente em Fahrenheit (F). (Fórmula de conversão: F = (9/5) * C + 32)

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
A([Início]) --> B{{Digite a temperatura em Celsius: }}
B --> b[/C/]
b --> C["calcula_F = (9/5) * C + 32"]
C --> D{{calcula_F}}
D --> E([Fim])
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ConverteCelsiusFarenheit
DECLARE C, calculo_F: REAL
INICIAR
ESCREVA DigitCIOus: 
LEIA C
calcula_F = (9/5) * C + 32
ESCREVA calcula_F
FIM
```

#### Teste de mesa (0.5 ponto)

| Entrada | Saída |
|    -    |   -   |
|   10    | 50.0  |
|   36    | 96.8  |

### Exercício 03 (2.5 pontos)
Receba dois números reais e um operador e efetue a operação correspondente com os valores recebidos (operandos). 
O algoritmo deve retornar o resultado da operação selecionada simulando todas as operações de uma calculadora simples.

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
a([INICIO]) --> b{{digite um numero:}}
b --> B[/n1/]
B --> c{{digite outro numero:}}
c --> C[/n2/]
C --> d{{"selecione a operação desejada:\n 1 para: Somar(+)\n 2 para: Subtrair(-)\n 3 para: Multiplicar(x)\n 4 para: Dividir(/)\n"}}
d --> e[/opcao/]
e --> f{opcao == 1}
f --false--> g{opcao == 2}
g --false--> h{opcao == 3}
h --false--> i[resultado = n1 / n2]
i --> J{{resultado}}
J --> K([FIM])
f --true--> F[resultado = n1 + n2]
F --> J
g --true--> G[resultado = n1 - n2]
G --> J
h --true--> H[resultado = n1 * n2]
H --> J
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo Calculadora
DECLARAR n1, n2, opcao, resultado: REAL
INICIAR
ESCREVER "digite um numero:"
LEIA n1
ESCREVER "digite outro numero:"
LEIA n2
ESCREVER "selecione a operação desejada:\n 1 para: Somar(+)\n 2 para: Subtrair(-)\n 3 para: Multiplicar(x)\n 4 para: Dividir(/)"
LEIA opcao
SE opcao == 1 ENTAO
	resultado = n1 + n2
SENAO SE opcao == 2 ENTAO
	resultado = n1 - n2
SENAO SE opcao == 3 ENTAO
	resultado = n1 * n2
SENAO
	resultado = n1 / n2

ESCREVER resultado
FIM
```

#### Teste de mesa (0.5 ponto)

| Entrada1 | Entrada2 | Entrada3 | Saída |
|    --    |    --    |    --    |   -   | 
|    5     |    5     |    1     |  10   |
|    5     |    5     |    2     |   0   |
|    5     |    5     |    3     |  25   |
|    5     |    5     |    4     |   1   |

### Exercício 04 (2.5 pontos)
Elaborar um algoritmo que, dada a idade, classifique nas categorias: infantil A (5 - 7 anos), infantil B (8 -10 anos), juvenil A (11 - 13 anos), juvenil B (14 -17 anos) e adulto (maiores que 18 anos).

#### Fluxograma (1.0 ponto)

```mermaid
flowchart TD
a([INICIO]) --> b{{Digite sua idade: }}
b --> B[/idade/]
B --> c{ 5 <= idade <=7}
c --false--> d{8 <= idade <=10}
d --false--> e{11 <= idade <=13}
e --false--> f{14 <= idade <= 17}
f --false--> G{{categoria: adulto}}
c --true--> C{{categoria: infantil A}}
d --true--> D{{categoria: infantil B}}
e --true--> E{{categoria: juvenil A}}
f --true--> F{{categoria: juvenil B}}
C --> H([FIM])
D --> H
E --> H
F --> H
G --> H
```

#### Pseudocódigo (1.0 ponto)

```
Algoritmo ClassificaCategoria
DECLARAR idade: INTEIRO
INICIAR
ESCREVER "Digite sua idade:"
LEIA idade
SE 5 <= idade <=7 ENTAO
	ESCREVER "categoria: infantil A"
SENAO SE 8 <= idade <=10 ENTAO
	ESCREVER "categoria: infantil B"
SENAO SE 11 <= idade <=13 ENTAO
	ESCREVER "categoria: infantil B"
SENAO SE 14 <= idade <=17 ENTAO
	ESCREVER "categoria: juvenil B"
SENÃO
	ESCREVER "categoria: adulto"
FIM
```

#### Teste de mesa (0.5 ponto)

|Entrada| Saída |
|  --   |  --   |
| 15    | categoria: juvenil B|
| 20    |  categoria: adulto  |
