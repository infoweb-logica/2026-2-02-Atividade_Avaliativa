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
- [avaliação b](../tipo_c/)
- **avaliação c**

---
## Avaliação 2.c - 2º bimestre

**Observação**: os algoritmos e suas entradas abaixo foram exemplos de soluções publicadas pela equipe da [Modalidade Programação da Fase 3 da OBI 2025](https://olimpiada.ic.unicamp.br/passadas/OBI2025/fase3/programacao/) baseada no caderno do [Nível 2](https://olimpiada.ic.unicamp.br/static/extras/obi2025/provas/ProvaOBI2025_f3p2.pdf) e por isso, disponibilizo o link de referência nas questões.

1. Execute o programa abaixo e registre as saídas na tabela abaixo. Links do [código](https://olimpiada.ic.unicamp.br/static/extras/obi2025/solucoes/2025f3p2_escadaria/lobo_2for.py) e dos [gabaritos](https://olimpiada.ic.unicamp.br/static/extras/obi2025/gabaritos/2025f3p2_escadaria.zip).
```python
N = int(input())
A = list(map(int, input().split()))

INF = 10**15
left = [INF] * N
right = [INF] * N

# Passagem esquerda -> direita
last_val, last_pos = -INF, -INF
for i in range(N):
    if A[i] != -1:
        last_val, last_pos = A[i], i
    if last_val != -INF:
        left[i] = last_val + (i - last_pos)

# Passagem direita -> esquerda
last_val, last_pos = -INF, -INF
for i in range(N - 1, -1, -1):
    if A[i] != -1:
        last_val, last_pos = A[i], i
    if last_val != -INF:
        right[i] = last_val + (last_pos - i)

# Combina os dois lados
ans = [min(left[i], right[i]) for i in range(N)]

for i in range(N):
    print(ans[i],end=' ')
```

| Entradas | Saídas |
| -------- | ------ |
| 5<br />5 -1 -1 -1 6 | |
| 3<br />1 -1 3       | |

---
2. Execute o programa abaixo e registre as saídas na tabela abaixo. Links do [código](https://olimpiada.ic.unicamp.br/static/extras/obi2025/solucoes/2025f3p2_hidrovias/hidrovias_dfs_py.py) e dos [gabaritos](https://olimpiada.ic.unicamp.br/static/extras/obi2025/gabaritos/2025f3p2_hidrovias.zip).
```python
import sys
sys.setrecursionlimit(10**7)

[n, m, k] = list(map(int, input().split()))

adj = [[] for i in range(n + 1)]
comp = [[0 for i in range(n + 1)] for g in range(2)]
comp_size = [[0 for i in range(n + 1)] for g in range(2)]
cur_comp = [0, 0]
cnt_rod = 0
hydro_cycle = False

for i in range(m):
  [a, b, t] = list(map(int, input().split()))
  adj[a].append((b, t))
  adj[b].append((a, t))
  if t == 2:
    cnt_rod += 1

# busca em profundidade
def dfs(g, v, p):
  global comp, cur_comp, hydro_cycle
  comp[g][v] = cur_comp[g]
  for w, t in adj[v]:
    if g == 0 and t == 2:
      continue
    if w == p:
      continue
    if comp[g][w]:
      if g == 0:
        hydro_cycle = True
      continue
    dfs(g, w, v)


for g in range(2):
  for v in range(1, n + 1):
    if not comp[g][v]:
      cur_comp[g] += 1
      dfs(g, v, 0)

if hydro_cycle:
  print("N")
  exit(0)


allowed_edges = cur_comp[0] - cur_comp[1]
forbidden_edges = cnt_rod - allowed_edges

if forbidden_edges > k:
  print("N")
else:
  print("S")
```

| Entradas | Saídas |
| -------- | ------ |
| 13 14 3<br />2 9 2<br />4 2 1<br />7 8 2<br />4 5 1<br />1 3 1<br />5 3 2<br />9 4 2<br />7 2 2<br />6 1 1<br />5 9 1<br />5 6 2<br />10 6 1<br />11 12 1<br />11 13 1 | |
| 10 9 2<br />8 2 1<br />2 3 1<br />3 4 1<br />4 5 1<br />5 6 1<br />6 7 1<br />2 5 1<br />2 6 1<br />1 10 1 | |

---
3. Execute o programa abaixo e registre as saídas na tabela abaixo. Links do [código](https://olimpiada.ic.unicamp.br/static/extras/obi2025/solucoes/2025f3p2_nasal/py_leo.py) e dos [gabaritos](https://olimpiada.ic.unicamp.br/static/extras/obi2025/gabaritos/2025f3p2_nasal.zip).
```python
n, k = map(int,input().split())

a = list(map(int,input().split()))
b = list(map(int,input().split()))

resp = 0

add = []
k+=1
k = min(k,n)

for i in range(n):
    if(a[i] >= b[i]):
        resp+=a[i]-b[i]
        add.append(b[i])
    else:
        add.append(a[i])

add.sort(key = lambda x: -x)

for i in range(k):
    resp+=add[i]

print(resp)
```

| Entradas | Saídas |
| -------- | ------ |
| 5 1<br />3 5 2 1 7<br />9 2 3 1 5 | |
| 5 2<br />1 2 3 4 5<br />2 2 2 2 2 | |
| 1 0<br />10<br />10 | |