# 📊 Dashboard Financeiro — Ateliê AC

Sistema completo de gestão financeira para ateliês de cerâmica, ilustração e artesanato. Monitore receitas, custos, mão de obra e lucratividade em tempo real.

**Versão:** 1.8  
**Status:** ✅ Funcional e em produção  
**Deploy:** https://nathanvasc-ship-it.github.io/dashboard-atelie/

---

## 🎯 Funcionalidades

### 1️⃣ **Aba Vendas** — Visão geral operacional

- **Cards de resumo** com valores e indicadores visuais:
  - Receita total (com tooltip de saúde)
  - Custo material (% da receita com avaliação)
  - Mão de obra total (% da receita com avaliação)
  - Lucro líquido (em destaque verde se saudável)
  - Pedidos + cortesias
  - Ticket médio
  - Clientes únicos

- **Tooltips inteligentes** — passe o mouse sobre os percentuais e veja se estão dentro das faixas saudáveis:
  - 🟢 Verde: Faixa ideal
  - 🟡 Amarelo: Atenção (ligeiramente fora)
  - 🔴 Vermelho: Crítico (muito fora)

- **Filtros interativos:**
  - Filtrar por mês
  - Filtrar por status (Pago / Cortesia / Pendente)
  - Ordenar por receita ou quantidade

- **Gráficos visuais:**
  - Status das vendas (pizza interativa)
  - Situação dos pagamentos (pizza interativa — clique para filtrar)

- **Seção "Horas trabalhadas no período":**
  - Total de minutos/horas do mês
  - Equivalente em dias úteis (5h/dia)
  - Média de tempo por venda
  - Breakdown por produto

- **Campo "Valor da hora"** (padrão R$ 80):
  - Editável em tempo real
  - Alimenta cálculos de MO em todas as abas

---

### 2️⃣ **Aba Precificação** — Gestão de catálogo

- **Tabela completa de produtos** com:
  - Código e nome
  - Categoria
  - Custo unitário
  - Tempo de produção (editável)
  - MO calculada (baseado em valor/hora)
  - Custo total (material + MO)
  - Preço atual
  - **Margem de lucro** com check visual ✓/✗
  - **Preço mínimo** (40% de lucro — conservador)
  - **Preço ideal** (50% de lucro — recomendado)
  - Status (Saudável / Baixa / Crítica)

- **Cards de métricas:**
  - Valor da hora (parametrizável)
  - Produtos saudáveis vs total
  - Quantidade que precisa ajuste
  - Tempo médio de produção

- **Alertas destacados:**
  - Linha laranja + badge "⚠ abaixo" para margem < 40%
  - Diferencia baixa (30-39%) de crítica (<30%)

- **Filtro por categoria** — refina a visualização

- **Recomendação automática de preço:**
  - Verde quando ≥ 40% de lucro
  - Amarelo quando 30-40%
  - Vermelho quando < 30%

---

### 3️⃣ **Aba Simulador** — Duas calculadoras em uma

#### A) **Simulador de margem** — Brinque com os números

Valores parametrizáveis:
- Preço de venda (R$)
- Custo material (R$)
- Tempo produção (min)
- Valor da hora (R$)

Visualizações:
- **Barra colorida** mostrando divisão Custo / MO / Lucro
- **4 cards com checks visuais ✓/✗:**
  1. Custo material → ideal 10-25%
  2. Mão de obra → ideal 25-35%
  3. Lucro líquido → ideal 40-55%
  4. **Equilíbrio geral** → mostra quantas faixas estão ok (0/3 a 3/3)

- **Diagnóstico automático** em cores:
  - 🟢 Verde: tudo saudável
  - 🟡 Amarelo: precisa ajuste
  - 🔴 Vermelho: crítico (prejuízo)

- **Sugestão de preço em 3 faixas:**
  - **Mínimo** (40% lucro) — borda amarela
  - **Ideal** (50% lucro) — borda verde
  - **Ótimo** (55% lucro) — borda verde escuro

---

#### B) **Calculadora reversa** — Descubra sua margem ideal

Para quem não sabe como precificar e quer aprender.

**Entrada:**
- Preço atual/desejado
- Custo do material
- Tempo de produção
- **Valor agregado (0-100%)** — slider para produtos com técnica especial

**Classificação automática por tempo:**
- ≤30 min = **Simples**
- 31-60 min = **Médio**
- >60 min = **Complexo**

**Saída — 3 cenários lado a lado:**

1. **Conservador** (iniciante, produto comum)
   - MO: 25-30%
   - Lucro: 40%
   - Borda amarela

2. **Equilibrado** (intermediário, boa técnica)
   - MO: 30-35% (ajustado pelo tempo + valor agregado)
   - Lucro: 45-50%
   - Borda verde

3. **Premium** (avançado, alta exclusividade)
   - MO: 35-40%
   - Lucro: 50-55%
   - Borda verde escuro

**Cada card mostra:**
- Valor de MO e Lucro em R$
- % do valor disponível
- Resumo completo: Custo + MO + Lucro = Total
- ✓ se cabe / ✗ se falta dinheiro
- Quanto sobra ou falta

**O que é valor agregado?**
Use para aumentar a MO mesmo em produtos rápidos:
- Técnicas especiais (pintura à mão, bordado)
- Design exclusivo
- Edição limitada
- Personalização detalhada
- Quantidade maior = mais exclusividade = maior agregado

---

### 4️⃣ **Aba Relatório** — Análise estratégica mensal

**Visão 360° do negócio com métricas e gráficos.**

#### Cards de resumo:
- Receita total (com número de vendas)
- Custo material (% dinâmico com cor)
- Mão de obra (% dinâmico com cor)
- Lucro líquido (destaque se ≥40%)
- Horas trabalhadas + dias úteis equivalentes
- Ticket médio

#### Controles:
- **Seletor de mês** — "Todos os meses" ou um mês específico
- **Valor da hora editável** — recalcula tudo em tempo real

#### Comparativo com mês anterior:
- Só aparece quando um mês está selecionado
- Mostra variação % de receita e lucro
- Cores dinâmicas: verde (crescimento), amarelo (estável), vermelho (queda)

#### Gráfico de evolução mensal (barras):
- Receita (azul claro) vs Lucro (verde) mês a mês
- Visualiza tendência ao longo do tempo
- Eixo Y formatado em R$

#### Top 5 produtos por lucro:
- Ranking numerado com badge verde
- Nome + quantidade vendida + receita
- Lucro em destaque

#### Gráfico de composição (rosca):
- Divisão visual: Custo (laranja) / MO (azul) / Lucro (verde)
- Tooltip mostra R$ e %
- Legenda na parte inferior

---

## 📐 Paradigmas de Precificação

### Faixas saudáveis para ateliê artesanal:

| Componente | Mínimo | Ideal | Máximo |
|---|---|---|---|
| **Custo material** | 5% | 10-25% | 30% |
| **Mão de obra** | 15% | 25-35% | 40% |
| **Lucro líquido** | 30% | 40-55% | ∞ |

### Margem dinâmica por tempo de produção:

Para produtos com MO incorporada, aplicamos margem mínima variável:
- **Até 30 min** → 50% de lucro mínimo
- **31-60 min** → 55% de lucro mínimo
- **61-120 min** → 62% de lucro mínimo
- **Mais de 120 min** → 68% de lucro mínimo

**Rationale:** Quanto mais tempo, mais tempo = recurso escasso = maior margem necessária.

### Divisão financeira ideal do preço de venda (100%):

```
R$ 200 (exemplo com valor/hora R$ 80)
├─ Custo material: R$ 30-50 (15-25%) — Laranja 🟠
├─ Mão de obra: R$ 50-70 (25-35%) — Azul 🔵
└─ Lucro líquido: R$ 80-120 (40-55%) — Verde 🟢
```

---

## 🔗 Integração com Google Sheets

### Planilhas usadas:

1. **Valores 2.0** (gid=21694616)
   - Columns: Codigo, Produto, Categoria, Tempo(min), Custo Unitario, Preco Venda, Mao de Obra, Custo Total, Lucro Total
   - Fonte para tabela de precificação
   - Link CSV:
     ```
     https://docs.google.com/spreadsheets/d/e/2PACX-1vStwozPUCnYfE3O-EJVpTrQtgdsttloV1O57Bw_WPLArse5TIUDozd48vz5rTid-Eartf3D92EczYhR/pub?gid=21694616&single=true&output=csv
     ```

2. **Vendas** (gid=2115485472)
   - Columns: DATA, COD_PRODUTO, PRODUTOS, VALOR, STATUS, SITUAÇÃO, CLIENTES
   - Fonte para dashboard de vendas
   - Link CSV:
     ```
     https://docs.google.com/spreadsheets/d/e/2PACX-1vStwozPUCnYfE3O-EJVpTrQtgdsttloV1O57Bw_WPLArse5TIUDozd48vz5rTid-Eartf3D92EczYhR/pub?gid=2115485472&single=true&output=csv
     ```

### Como publicar suas planilhas:

1. Abra a planilha no Google Sheets
2. **Arquivo → Publicar na web**
3. Selecione a aba desejada
4. **CSV** como formato
5. Copie o link
6. Substitua as URLs no código

### Tratamento de CORS:

Usa proxy público (`allorigins.win`, `corsproxy.io`, `thingproxy`) com fallback automático e cache-busting para garantir dados sempre atualizados.

---

## 🛠️ Tecnologia

- **Frontend:** HTML5, CSS3, Vanilla JavaScript
- **Gráficos:** Chart.js 4.4.1
- **Dados:** Google Sheets (CSV exportado)
- **Deploy:** GitHub Pages
- **Sem dependências externas** (exceto Chart.js)

---

## 📁 Arquivos

```
/outputs/
├─ index.html                          # Dashboard principal (v1.8)
├─ calculadora_precificacao_atelie.html # Calculadora standalone (v2.2)
└─ README.md                           # Este arquivo
```

### Arquivos de origem (Google Sheets):
- **Valores 2.0:** Catálogo de produtos com precificação
- **Vendas:** Histórico de vendas e status

---

## 🚀 Como usar

### Online (Deploy)

1. Acesse: https://nathanvasc-ship-it.github.io/dashboard-atelie/
2. Selecione a aba desejada (Vendas, Precificação, Relatório, Simulador)
3. Use os filtros e controles
4. Edite valores em tempo real (valor/hora, tempo de produção, etc.)

### Localmente

1. Clone ou baixe o repositório
2. Abra `index.html` em um navegador moderno
3. Funciona offline após primeira carga (dados são em cache)

### Atualizar dados

- Clique no botão **"Atualizar"** no canto superior direito
- Ou edite as planilhas Google Sheets (mudanças refletem automaticamente após refresh)

---

## 💡 Casos de Uso

### Para iniciantes:
1. Use a **Calculadora Reversa** para entender como precificar
2. Brinque com os valores no **Simulador** para ver o impacto
3. Acompanhe a evolução no **Relatório** mensal

### Para intermediários:
1. Configure a **Aba Precificação** com todos os produtos
2. Monitore a saúde financeira na **Aba Vendas**
3. Use o **Relatório** para identificar produtos lucrativos

### Para avançados:
1. Ajuste margens por produto na **Precificação**
2. Use valor agregado na **Calculadora Reversa** para produtos especiais
3. Analise tendências mensais e tome decisões estratégicas no **Relatório**

---

## 🎨 Design & UX

- **Minimalista e limpo** — foco nos dados
- **Cores significativas:**
  - 🟠 Laranja: Custo material
  - 🔵 Azul: Mão de obra
  - 🟢 Verde: Lucro/Saudável
  - 🟡 Amarelo: Atenção
  - 🔴 Vermelho: Crítico/Prejuízo

- **Responsivo** — funciona em desktop, tablet e mobile
- **Modo claro** com fundo bege (`#f5f4f0`)

---

## 🔧 Configurações

### Padrões:

| Config | Padrão | Onde mudar |
|---|---|---|
| Valor da hora | R$ 80 | Campo "Valor da hora" em Vendas, Simulador ou Relatório |
| Preço simulador | R$ 200 | Campo "Preço de venda" em Simulador |
| Custo simulador | R$ 60 | Campo "Custo material" em Simulador |
| Tempo simulador | 30 min | Campo "Tempo produção" em Simulador |

Todos os valores são editáveis em tempo real e sincronizados automaticamente.

---

## 📊 Exemplos de análise

### Exemplo 1: Produto com margem baixa

**Situação:**
- Preço: R$ 100
- Custo: R$ 40
- Tempo: 60 min
- Valor/hora: R$ 80

**Cálculo:**
- MO = (60/60) × R$ 80 = R$ 80
- Custo total = R$ 40 + R$ 80 = R$ 120
- Lucro = R$ 100 - R$ 120 = **-R$ 20 (PREJUÍZO)**

**Solução:** Aumentar preço para R$ 170 (mínimo) ou R$ 200 (ideal)

---

### Exemplo 2: Produto rápido mas exclusivo

**Situação:**
- Preço: R$ 150
- Custo: R$ 30
- Tempo: 20 min (simples)
- Valor agregado: 80% (pintura à mão detalhada)

**Calculadora Reversa sugere:**
- Conservador: MO R$ 32 + Lucro R$ 48
- Equilibrado: MO R$ 44 + Lucro R$ 56
- Premium: MO R$ 52 + Lucro R$ 63

**Recomendação:** Usar Equilibrado ou Premium, pois o produto tem técnica especial

---

### Exemplo 3: Análise mensal

**Situação:** Visualizar Janeiro/2025 no Relatório

**Métricas:**
- Receita: R$ 4.500 (25 vendas)
- Custo: R$ 800 (17,8%)
- MO: R$ 1.200 (26,7%)
- Lucro: R$ 2.500 (55,6%) ✓ Excelente
- Horas: 15h = 3 dias
- Ticket médio: R$ 180

**Top produto:** Placa baby — R$ 850 de lucro

**Comparativo vs Dezembro:**
- Receita: +12% (crescimento!)
- Lucro: +18% (ainda melhor)

---

## 🐛 Troubleshooting

### "Não carrega dados da planilha"
- Verifique se publicou a aba como CSV no Google Sheets
- Teste o link do CSV diretamente no navegador
- Clique "Atualizar" para tentar novamente

### "Valores zerados em Mão de Obra"
- Certifique-se que a coluna "Tempo(min)" está preenchida na aba Valores
- Ou use o campo editável na tabela de Precificação

### "Gráficos não aparecem"
- Recarregue a página (Ctrl+F5)
- Limpe o cache do navegador
- Teste em outro navegador

### "Diferença nos cálculos de MO"
- Verifique o "Valor da hora" — deve estar consistente em todas as abas
- Se alterou o valor/hora, clique "Atualizar" para recalcular

---

## 📝 Histórico de versões

| Versão | Data | O que mudou |
|---|---|---|
| v1.0 | 2025-01 | Dashboard inicial + calculadora básica |
| v1.1 | 2025-01 | Fix MO calculation from tempoMin |
| v1.2 | 2025-02 | Campo valor/hora editável (padrão R$ 80) |
| v1.3 | 2025-02 | Aba Simulador adicionada |
| v1.4 | 2025-02 | Checks visuais nos cards, sugestão de preço |
| v1.5 | 2025-03 | Tooltips nos totais de Vendas, Precificação linkaagora |
| v1.6 | 2025-03 | Precificação voltou como aba interna (não mais link externo) |
| v1.7 | 2025-03 | Calculadora Reversa adicionada ao Simulador |
| **v1.8** | **2025-04** | **Aba Relatório com análise mensal, gráficos e comparativos** |

---

## 🚧 Roadmap (Futuras melhorias)

- [ ] Sugestão de meta mensal baseado em histórico
- [ ] Alerta para produtos com margem baixa (automático)
- [ ] Exportar relatório como PDF
- [ ] Gráfico de rentabilidade por categoria
- [ ] Integração com WhatsApp/email para alertas
- [ ] Suporte a múltiplas moedas
- [ ] Modo escuro (dark mode)
- [ ] Aplicativo mobile nativo

---

## 📧 Contato & Suporte

Para dúvidas, sugestões ou bugs:
1. Abra uma issue no GitHub
2. Ou envie mensagem para contato do projeto

---

## 📄 Licença

Open source — use livremente para seu ateliê ou negócio.

---

## 🙏 Créditos

Desenvolvido para o **Ateliê AC** (Aline Coelho) — cerâmica fria, ilustrações digitais, pingentes e combos.

Inspirado em boas práticas de UX, design de dados e educação financeira para pequenos negócios.

---

**Dúvidas? Teste a calculadora, explore as abas e deixe seus dados no Google Sheets!** 📊✨