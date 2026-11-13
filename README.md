# 📊 Simulador ContábilPro – Balanço Patrimonial

Aplicativo web para lançar o Balanço Patrimonial de três anos, calcular automaticamente a **Análise Horizontal (AH)** e a **Análise Vertical (AV)** e visualizar os resultados em dashboards.

> 🏫 Projeto da disciplina **Gestão do Desempenho Corporativo** – Fatec Ipiranga "Pastor Enéas Tognini" – Big Data para Negócios, 5º semestre (2º semestre de 2026).

---

## 🎓 Sobre o projeto

Desenvolvido pelos alunos do 5º Semestre de Big Data para Negócios (Turma 2º Semestre de 2026), sob orientação do Prof. Paulo César Pinheiro.

⭐ **Coordenação Geral:** Pablo

| Área | Integrantes |
|---|---|
| Back-End | Pablo, William Nunes e Lucas |
| Front-End | Gabi, Renato e Bruno |
| Gráficos e Dashboards | Gustavo, Renato, Cauan e Rayssa |
| Análise Vertical e Horizontal | Jefferson, Felipe e William |
| Documentação | Pedro, Thiago e Vanessa |

🎯 **Objetivo:** ajudar a entender a evolução de uma empresa a partir do balanço de três anos, transformando dados contábeis em informação para a tomada de decisão, sem cálculos manuais.

---

## 🤖 Prompt simplificado do site

Prompt resumido que descreve o site (útil para recriar ou evoluir o projeto com uma IA):

```text
Crie um app web de página única (um único arquivo HTML, com CSS e JavaScript
puros e Chart.js via CDN) chamado "Simulador ContábilPro".

Fluxo em 3 etapas:
1. Balanço: formulário com nome da empresa, 3 anos editáveis (padrão 2024, 2025
   e 2026) e contas dos Ativos (circulante, longo prazo e imobilizado) de um
   lado e dos Passivos e Patrimônio Líquido (passivo circulante, passivo de
   longo prazo e PL) do outro. Totais em tempo real, validação de
   Ativo = Passivo + PL, botões "Carregar exemplo" e "Limpar tudo".
2. Análises: tabelas de Análise Horizontal (base fixa no 1º ano = 100%, com
   índice e variação) e Análise Vertical (% do total de ativos ou de passivos
   e PL), com grupos de contas recolhíveis.
3. Dashboards: abas horizontal e vertical, com cards de KPIs por grupo,
   gráfico de linhas (evolução vs ano-base), barras (saldo por ano) e barras
   empilhadas 100% (composição).

Extras: páginas Início, Sobre e Glossário; tema claro/escuro; salvamento
automático em localStorage; layout responsivo; acessível por teclado.
Visual moderno, cards arredondados, cores azul/ciano/amarelo/rosa.
```

---

## ✅ O que foi feito

- Fluxo guiado em **3 etapas** (Balanço → Análises → Dashboards) com menu lateral e atalhos no cabeçalho.
- Entrada de dados em **tela única**, com 26 contas em 6 grupos e 3 anos por conta.
- **Validação em tempo real** da equação contábil, mostrando a diferença de cada ano quando não fecha.
- **AH de base fixa** e **AV com uma casa decimal**, com subcontas recolhíveis.
- **Dashboards** horizontal e vertical com cards de KPIs e gráficos (Chart.js).
- Dados de exemplo (Empresa Exemplo Ltda., 2024–2026, fictícios).
- Páginas **Início**, **Sobre** e **Glossário**.
- **Tema claro/escuro**, layout responsivo, navegação por teclado e salvamento automático no navegador.
- Documentação do projeto em PDF (versão 2.0).

---

## 📖 Manual do site

### 🚀 Como abrir
Abra o arquivo HTML em um navegador moderno (de preferência renomeie para `index.html`). Os gráficos e a fonte usam CDN, então é preciso ter internet.

### 🧾 Etapa 1 – Balanço
1. Informe o **nome da empresa** e ajuste os **três anos**, se necessário.
2. Preencha os valores em reais (sem pontos ou vírgulas de milhar). **Enter** passa para o campo de baixo, no mesmo ano.
3. A **depreciação acumulada** entra como número positivo; o app a subtrai do ativo imobilizado.
4. Clique no nome de um grupo para recolher ou abrir suas contas.
5. A barra inferior informa se o balanço fecha:
   - 🟢 Verde: ativos = passivos + PL.
   - 🔴 Vermelho: mostra a diferença de cada ano.
6. **Carregar exemplo** preenche tudo com dados fictícios; **Limpar tudo** apaga os dados (sem pedir confirmação).
7. Clique em **Ver análises**.

### 🔍 Etapa 2 – Análises
- **Análise horizontal:** valores dos 3 anos, base (100%) e índice dos anos seguintes, com seta e variação sobre o ano-base.
- **Análise vertical:** valor de cada conta e seu % sobre o total de ativos (lado dos ativos) ou sobre o total de passivos e PL (lado dos passivos).
- Clique em um grupo para recolher ou mostrar as subcontas.

### 📈 Etapa 3 – Dashboards
- **Análise horizontal:** 6 cards (valor no último ano e variação vs ano-base), gráfico de linhas com filtros por grupo e gráfico de barras com o saldo por ano.
- **Análise vertical:** 6 cards (peso de cada grupo no último ano) e duas barras empilhadas 100% (composição dos ativos e dos passivos e PL).

### ⚙️ Outros recursos
- **Menu (☰):** Início, Balanço, Análises, Dashboards, Sobre e Glossário.
- **Botão ◐:** alterna entre tema claro e escuro.
- Os dados ficam salvos no navegador (localStorage), sem servidor e sem cadastro.

---

## 🧮 Resumo: Balanço Patrimonial, AH e AV

### 🏦 Balanço Patrimonial
Fotografia da empresa em uma data. De um lado ficam os **ativos** (o que a empresa tem e controla); do outro, os **passivos** e o **patrimônio líquido** (de onde veio o dinheiro: terceiros ou sócios). Os dois lados sempre fecham:

```text
Ativo = Passivo + Patrimônio Líquido
```

| Grupo | O que é |
|---|---|
| Ativo circulante | Vira dinheiro em até 12 meses (caixa, contas a receber, estoques) |
| Ativo de longo prazo | Realiza-se depois de 12 meses (investimentos, IR diferido) |
| Ativo imobilizado | Bens duradouros (imóveis, máquinas), já descontada a depreciação |
| Passivo circulante | Obrigações a pagar em até 12 meses |
| Passivo de longo prazo | Dívidas com vencimento após 12 meses |
| Patrimônio líquido | Capital dos sócios + lucros acumulados − prejuízos |

### 📐 Análise Vertical (AV)
Mostra o **peso de cada conta** em relação a uma base do **mesmo ano**. É uma análise estática: retrata a estrutura da empresa.

```text
AV (%) = (Valor da conta ÷ Valor da conta base) × 100
```
Base dos ativos: total de ativos. Base dos passivos: total de passivos + PL.

### 📅 Análise Horizontal (AH)
Mostra a **evolução de cada conta ao longo do tempo** em relação a um ano de referência. É uma análise dinâmica: mostra o ritmo de crescimento ou redução. No app, a base é fixa (o 1º ano vale 100%).

```text
Índice (%)  = (Valor do ano ÷ Valor do ano-base) × 100
Variação (%) = Índice − 100
```

### 💡 Exemplo (dados fictícios)
Com a Empresa Exemplo Ltda., o ativo circulante vai de R$ 130.000 (2024) para R$ 202.500 (2026):
- **AH:** índice de 155,8% (+55,8% sobre 2024).
- **AV:** peso passa de 46,4% para 52,0% do total de ativos.

> 💡 As duas análises se complementam: o crescimento de uma conta só preocupa se aumentar sua relevância na estrutura.

---

## 🎨 Referência de design

Inspiração visual: templates da comunidade do Figma  
https://www.figma.com/community/website-templates?resource_type=files

---

## 🤝 Desenvolvido com Claude

Este projeto contou com o apoio de IA da [Anthropic](https://www.anthropic.com/):

- **Modelo:** Claude Sonnet 5.5 (`claude-sonnet-5-5`)
## 🛠️ Tecnologias

- HTML, CSS (variáveis de tema) e JavaScript puro, em um único arquivo
- [Chart.js](https://www.chartjs.org/) 4.4.1 (CDN)
- Fonte Inter (Google Fonts)
- `localStorage` para persistência

