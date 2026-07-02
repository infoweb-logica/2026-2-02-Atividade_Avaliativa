# 2026 - ILP - Atividade avaliativa no. 02 do 2o bimestre

## Informações gerais
- **Objetivo**:
  - avaliar conhecimento dos alunos.
  - almpliar a "caixa de ferramentas" do aluno na construção de lógica.
- **Público alvo**: alunos da disciplina de [Introdução a lógica e programação](https://github.com/infoweb-logica/) do curso de [Infoweb](https://diatinf.ifrn.edu.br/cursos/tecnico-em-informatica-para-internet/) na [DIATINF](https://diatinf.ifrn.edu.br/) no [CNAT-IFRN](https://portal.ifrn.edu.br/campus/natalcentral/).
- **Professor**: [L A Minora](https://github.com/leonardo-minora/)

---

São 3 as avaliações:
- **avaliação a**
- [avaliação b](../tipo_b/)
- [avaliação c](../tipo_c/)

---
## Avaliação 2.a - 2º bimestre

**Observação**: foi individualizado os valores de entrada(s) das questões.
Contudo caso deseje testar, aconeslho executar como _python debugger_, e use as entrada(s) abaixo e confira com a(s) respectiva(s) saída(s).

1. Execute o programa abaixo e registre as saídas na tabela abaixo.

```python
print(2026, 7, 2)
print('desejo boa avaliação a todos')
```

| Entradas | Saídas |
| -------- | ------ |
|          | 2026 7 2<br/>desejo boa avaliação a todos |

---
2. Execute o programa abaixo e registre as saídas na tabela abaixo.

```python
ano = 2026
mes = 6
dia = 30
print(f'hoje é {dia} de {mes} de {ano}.')
```

| Entradas | Saídas |
| -------- | ------ |
|          | hoje é 30 de 6 de 2026. |

---
3. Execute o programa abaixo e registre as saídas na tabela abaixo.

```python
for contador in range(3):
  print(f'contando {contador+1} de 3.')
```

| Entradas | Saídas |
| -------- | ------ |
|          | contando 1 de 3.<br />contando 2 de 3.<br />contando 3 de 3. |

---
4. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero = input()
print(f'# {numero}')
```

| Entradas | Saídas |
| -------- | ------ |
| 3        | # 3    |
| 4        | # 4    |

---
5. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero = int(input())
for contador in range(numero):
  print(f'contando {contador+1} de {numero}.')
```

| Entradas | Saídas |
| -------- | ------ |
| 3        | contando 1 de 3.<br />contando 2 de 3.<br />contando 3 de 3. |
| 4        | contando 1 de 4.<br />contando 2 de 4.<br />contando 3 de 4.<br />contando 4 de 4. |

---
6. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
repeticoes = int(input())
soma = 0
for numero in range(repeticoes):
  soma += numero        # soma = soma + numero
print(f'soma: {soma}')
```

| Entradas | Saídas |
| -------- | ------ |
| 3        | soma: 3 |
| 4        | soma: 6 |

---
7. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero_1 = int(input())
numero_2 = int(input())

resultado = numero_1 + numero_2

if resultado % 2 == 0:
  print(f'{resultado} é par.')
else:
  print(f'{resultado} é ímpar.')
```

| Entradas | Saídas |
| -------- | ------ |
| 4<br />3 | 7 é ímpar |
| 1<br />3 | 4 é par   |

---
8. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero = int(input())

if numero == 0:
  print(f'{numero} é zero.')
elif numero > 0:
  print(f'{numero} é positivo.')
else:
  print(f'{numero} é negativo.')
```

| Entradas | Saídas |
| -------- | ------ |
| 2        | 2 é positivo.  |
| 0        | 0 é zero.      |
| -2       | -2 é negativo. |

---
9. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
repeticoes = int(input())
soma = 0
for _ in range(repeticoes):
  numero = int(input())
  soma += numero        # soma = soma + numero
print(f'resultado: {soma}')
```

| Entradas | Saídas |
| -------- | ------ |
| 3<br />3<br />5<br />7 | resultado: 15 |
| 5<br />5<br />3<br />1<br />3<br />5 | resultado: 17 |

---
10. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numeros = [int(numero) for numero in input().split()]
# numeros = [23, -32, 1, -2, 3, 4, -5, 6, 7, 8, 9, 10]
resultado = 0
outro_resultado = 1
for numero in numeros:
    if numero >= 0:
        resultado += numero
    else:
        outro_resultado *= numero

print(f"1o resultado: {resultado}")
print(f"2o resultado: {outro_resultado}")
```

| Entradas | Saídas |
| -------- | ------ |
| 7 5 3 1 0    | 1o resultado: 16<br />2o resultado: 1  |
| 4 2 0 -2 4   | 1o resultado: 10<br />2o resultado: -2 |
| -2 -1 -3 1 3 | 1o resultado: 4<br />2o resultado: -6  |

---