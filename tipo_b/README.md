# 2026 - ILP - Atividade avaliativa no. 02 do 2o bimestre

## Informações gerais
- **Objetivo**:
  - avaliar conhecimento dos alunos.
  - almpliar a "caixa de ferramentas" do aluno na construção de lógica.
- **Público alvo**: alunos da disciplina de [Introdução a lógica e programação](https://github.com/infoweb-logica/) do curso de [Infoweb](https://diatinf.ifrn.edu.br/cursos/tecnico-em-informatica-para-internet/) na [DIATINF](https://diatinf.ifrn.edu.br/) no [CNAT-IFRN](https://portal.ifrn.edu.br/campus/natalcentral/).
- **Professor**: [L A Minora](https://github.com/leonardo-minora/)

---

São 3 as avaliações:
- [avaliação a](../tipo_a/)
- **avaliação b**
- [avaliação c](../tipo_c/)

---
## Avaliação 2.b - 2º bimestre

1. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero_1 = int(input())
numero_2 = int(input())

resultado = numero_1 + numero_2
if resultado % 2 == 0:
  print(f'{resultado} é par.')
else:
  print(f'{resultado} é ímpar.')
```

Entradas
Saídas

---
2. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero = int(input())

if numero == 0:
  print(f'{numero} é zero.')
elif numero > 0:
  print(f'{numero} é positivo.')
else:
  print(f'{numero} é negativo.')
```

Entradas
Saídas

---
3. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numero = int(input())
for contador in range(numero):
  print(f'contando {contador+1} de {numero}.')
```

Entradas
Saídas

---
4. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
repeticoes = int(input())
resultado = 0
for numero in range(repeticoes):
    resultado += numero
print(f'resultado: {resultado}')
```

Entradas
Saídas

---
5. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
repeticoes = int(input())
numeros = [int(numero) for numero in input().split()]
resultado = 0
for indice in range(repeticoes):
    resultado += numeros[indice]
print(f'resultado: {resultado}')
```

Entradas
Saídas

---
6. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numeros = [int(numero) for numero in input().split()]
for numero in numeros:
    if numero < 0:
        print(f'{numero} é negativo.')
    else:
        fatorial = 1
        
        for i in range(1, numero + 1):
            fatorial *= i
        print(f'{numero}! = {fatorial}')
```

Entradas
Saídas

---
7. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
repeticoes = int(input())
numeros = [int(numero) for numero in input().split()]
for indice in range(repeticoes):
    numero = numeros[indice]
    if numero <= 0:
        print(f"{numero} não é perfeito.")
    else:
        soma_divisores = 0
        for i in range(1, numero):
            if numero % i == 0:
                soma_divisores += i        
        if soma_divisores == numero:
            print(f"{numero} é perfeito!")
        else:
            print(f"{numero} NÃO é perfeito.")
```

Entradas
Saídas

---
8. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numeros = [int(numero) for numero in input().split()]
numeros_perfeitos = []
for numero in numeros:
    if numero <= 0:
        print(f"{numero} não é perfeito.")
    else:
        soma_divisores = 0
        for i in range(1, numero):
            if numero % i == 0:
                soma_divisores += i        
        if soma_divisores == numero and numero not in numeros_perfeitos:
            numeros_perfeitos.append(numero)

print(f"Números perfeitos: {numeros_perfeitos}")
```

Entradas
Saídas

---
9. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
lista = [int(numero) for numero in input().split()]

maior_trecho = 1
trecho_atual = 1
trecho = []
for indice in range(1, len(lista)):
    if lista[indice] > lista[indice - 1]:
        trecho_atual += 1
    else:
        if trecho_atual > maior_trecho:
            trecho = lista[indice - trecho_atual:indice]
            maior_trecho = trecho_atual
        trecho_atual = 1
        
if trecho_atual > maior_trecho:
    maior_trecho = trecho_atual
if maior_trecho > 1:
    print(f"trecho {trecho}, tamanho {maior_trecho}")
else:
    print("sem trecho")
```

Entradas
Saídas

---
10. Execute o programa abaixo e registre as saídas na tabela abaixo.
```python
numeros = [int(numero) for numero in input().split()]
mdc = []
mmc = []
for indice in range(len(numeros) - 1):
    numero_a = numeros[indice]
    numero_b = numeros[indice + 1]
    while numero_b != 0:
        numero_a, numero_b = numero_b, numero_a % numero_b
    mdc.append(numero_a)
    mmc.append(abs((numeros[indice] * numeros[indice + 1]) // numero_a))
print(f"lista mdc: {mdc}")
print(f"lista mmc: {mmc}")
```

Entradas
Saídas
---