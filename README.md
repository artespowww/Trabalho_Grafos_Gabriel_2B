# Problema Proposto — Cobertura de Vértices (Vertex Cover)

## 📖 Descrição do Projeto

Este projeto simula um cenário de resposta a incidentes cibernéticos em uma infraestrutura crítica utilizando grafos.

A rede corporativa é representada por um grafo não direcionado onde:

- vértices representam dispositivos da rede;
- arestas representam conexões entre dispositivos;
- o objetivo é identificar os dispositivos críticos que devem ser monitorados para cobrir todas as conexões da rede.

O problema resolvido é o:

# Vertex Cover Problem

Problema clássico da Teoria da Complexidade Computacional pertencente à classe dos problemas NP-Completos.

---

# 🎯 Objetivo

Desenvolver um sistema capaz de:

- representar uma infraestrutura de rede utilizando grafos;
- manipular vértices e arestas;
- determinar um conjunto de Vertex Cover;
- exibir os vértices críticos;
- demonstrar análise de complexidade computacional;
- visualizar a rede graficamente.

---

# 🛡️ Cenário Simulado

A empresa sofreu um ataque cibernético e o War Room precisa determinar quais dispositivos devem ser monitorados para garantir cobertura total da rede comprometida.

A topologia da rede simula:

- Firewall
- Servidores Web
- Aplicações internas
- Banco de dados
- VPN
- SIEM
- Backup
- Storage
- Core Router

---

# 🧠 Tecnologias Utilizadas

| Tecnologia | Função |
|---|---|
| Python | Linguagem principal |
| NetworkX | Manipulação de grafos |
| Matplotlib | Visualização gráfica |

---

# ⚙️ Instalação

## 1. Instalar o Python

Baixe o Python:

https://www.python.org/downloads/

Verifique a instalação:

```bash
python --version
```

---

# 2. Clonar o Repositório

```bash
git clone https://github.com/seu-usuario/seu-repositorio.git
```

Entrar na pasta:

```bash
cd seu-repositorio
```

---

# 3. Instalar as Bibliotecas

## Instalar NetworkX

```bash
pip install networkx
```

## Instalar Matplotlib

```bash
pip install matplotlib
```

---

# ▶️ Executando o Projeto

Execute:

```bash
python main.py
```

---


---

---

# 🔍 O que é Lista de Adjacência

Lista de adjacência é uma estrutura utilizada para armazenar grafos.

Cada vértice mantém uma lista contendo todos os vértices conectados a ele.

## Exemplo

```text
Firewall → Web1, Web2, VPN
Web1 → Firewall, App1
App1 → Web1, Banco, Backup
```

Essa abordagem é eficiente porque:

- utiliza menos memória;
- facilita percorrer conexões;
- é ideal para grafos grandes.

---

# 🧩 O que é Vertex Cover

Vertex Cover é um problema clássico da Teoria dos Grafos.

O objetivo é encontrar o menor conjunto de vértices capaz de cobrir todas as arestas do grafo.

Uma aresta é considerada coberta quando pelo menos um de seus extremos pertence ao conjunto escolhido.

---

# ✅ Vertex Cover Encontrado

Os vértices críticos encontrados para cobertura da rede foram:

```text
Firewall
App1
App2
Banco
CoreRouter
VPN
```

---

# 📌 Explicação da Cobertura

Os vértices escolhidos cobrem todas as conexões da rede.

| Aresta | Coberta por |
|---|---|
| Firewall — Web1 | Firewall |
| Firewall — Web2 | Firewall |
| Firewall — VPN | Firewall ou VPN |
| App1 — Banco | App1 ou Banco |
| App2 — Banco | App2 ou Banco |
| Banco — Backup | Banco |
| Backup — CoreRouter | CoreRouter |
| VPN — Admin | VPN |

---

# 🧠 Complexidade Computacional

O problema Vertex Cover pertence à classe dos problemas NP-Completos.

A solução exata possui crescimento exponencial:

```text
O(2^n)
```

Onde:

- `n` representa a quantidade de vértices do grafo.

Isso significa que o número de combinações cresce exponencialmente conforme a rede aumenta.

---


---

# 📊 Visualização Gráfica

O sistema pode desenhar a rede utilizando Matplotlib.

Os vértices pertencentes ao Vertex Cover podem ser destacados em vermelho.

---

