# Plano GQM – Projeto MARY-JACKSON

## Framework Goal-Question-Metric (GQM)

O plano GQM estabelece uma estrutura hierárquica que conecta **objetivos de qualidade** (Goals) a **questões mensuráveis** (Questions) e **métricas específicas** (Metrics), garantindo rastreabilidade entre metas de negócio e evidências quantitativas.

---

## Estrutura GQM para AgroMart

### 🎯 **Goal 1: Usabilidade - Aprendizado**

**Objetivo:** Garantir que novos usuários consigam realizar tarefas essenciais com eficiência, atingindo uma curva de aprendizado aceitável para o contexto de CSAs.

| **Question** | **Metric** | **Fonte ISO** | **Tipo** | **Escala** | **Limite EU1** |
|-------------|------------|---------------|----------|------------|---------------|
| Q1.1: Novos usuários conseguem criar uma conta em tempo adequado? | M1.1: *Task completion time for account creation* | ISO 25022 §4.2.2 | Externa | Intervalar (segundos) | ≤ 180s |
| Q1.2: Usuários compreendem o fluxo de pedidos sem ajuda? | M1.2: *Task effectiveness* (taxa de sucesso) | ISO 25022 §4.2.1 | Externa | Razão (%) | ≥ 85% |
| Q1.3: Quantos erros ocorrem durante aprendizado inicial? | M1.3: *User error frequency* | ISO 25022 §4.2.4 | Externa | Absoluta (nº/tarefa) | ≤ 2 erros/tarefa |

---

### 🛡️ **Goal 2: Confiabilidade - Disponibilidade**

**Objetivo:** Assegurar que o sistema mantenha alta disponibilidade durante operações críticas, minimizando impacto na receita das CSAs.

| **Question** | **Metric** | **Fonte ISO** | **Tipo** | **Escala** | **Limite EU1** |
|-------------|------------|---------------|----------|------------|---------------|
| Q2.1: O sistema permanece disponível durante horários comerciais? | M2.1: *Service availability ratio* | ISO 25023 §4.3.4 | Externa | Razão (%) | ≥ 99.5% |
| Q2.2: Quanto tempo o sistema leva para recuperar após falhas? | M2.2: *Mean time to recovery (MTTR)* | ISO 25023 §4.3.6 | Externa | Intervalar (minutos) | ≤ 15 min |
| Q2.3: Com que frequência ocorrem falhas críticas? | M2.3: *Failure density* | ISO 25023 §4.3.2 | Interna | Razão (falhas/semana) | ≤ 1 falha/semana |

---

### ⚡ **Goal 3: Eficiência de Performance - Comportamento Temporal**

**Objetivo:** Garantir resposta adequada do sistema mesmo em conexões limitadas (contexto rural), mantendo competitividade com e-commerces tradicionais.

| **Question** | **Metric** | **Fonte ISO** | **Tipo** | **Escala** | **Limite EU1** |
|-------------|------------|---------------|----------|------------|---------------|
| Q3.1: As páginas carregam em tempo aceitável? | M3.1: *Response time* | ISO 25023 §4.1.1 | Externa | Intervalar (segundos) | ≤ 3s (web), ≤ 2s (mobile) |
| Q3.2: O sistema suporta picos de demanda (safra)? | M3.2: *Throughput* | ISO 25023 §4.1.2 | Externa | Razão (req/segundo) | ≥ 100 req/s |
| Q3.3: O app consume recursos adequadamente? | M3.3: *Memory utilization* | ISO 25023 §4.1.4 | Interna | Razão (%) | ≤ 200MB RAM |

---

### 🔒 **Goal 4: Segurança - Integridade**

**Objetivo:** Proteger dados pessoais e transações financeiras contra violações, mantendo confiança dos usuários na plataforma.

| **Question** | **Metric** | **Fonte ISO** | **Tipo** | **Escala** | **Limite EU1** |
|-------------|------------|---------------|----------|------------|---------------|
| Q4.1: Existem vulnerabilidades críticas detectadas? | M4.1: *Number of critical OWASP findings* | ISO 25023 §4.5.2 (adapt.) | Interna | Absoluta | = 0 |
| Q4.2: Dados são transmitidos com segurança adequada? | M4.2: *Encryption coverage ratio* | ISO 25023 §4.5.1 (adapt.) | Interna | Razão (%) | = 100% |
| Q4.3: Tentativas de acesso não autorizado são bloqueadas? | M4.3: *Access attempt success ratio* | ISO 25023 §4.5.3 | Externa | Razão (%) | ≤ 0.1% |

---

## Rastreabilidade Goal ↔ ISO 25010

| Goal GQM | Característica ISO 25010 | Sub-característica | Justificativa de Prioridade |
|----------|--------------------------|-------------------|---------------------------|
| **Goal 1** | Usabilidade | Aprendizado | **Crítica**: Diversidade de perfis de usuário (rural + urbano) |
| **Goal 2** | Confiabilidade | Disponibilidade | **Alta**: Impacto direto na receita das CSAs |
| **Goal 3** | Eficiência de Performance | Comportamento temporal | **Média-Alta**: Contexto de conectividade limitada |
| **Goal 4** | Segurança | Integridade | **Média**: Transações financeiras e dados pessoais |

---

## Limitações e Transparência para EU1

### Dados Disponíveis
- ✅ **Métricas internas**: Análise estática, cobertura de testes
- ✅ **Métricas de usabilidade**: Observação direta, heurísticas Nielsen
- ❌ **Métricas em produção**: Sistema local, sem dados reais de carga

### Baseline TBD (To Be Determined)
Alguns limites serão refinados na **EU2** com:
- Testes de usabilidade moderados (5-8 usuários)
- Testes de carga simulados
- Auditoria de segurança automatizada

---

## Instrumentação Planejada

### Automação em CI/CD
```bash
# Métricas internas automatizadas
- Cobertura de testes: Jest/PyTest
- Análise estática: ESLint, SonarQube
- Vulnerabilidades: OWASP ZAP, Snyk
```

### Ferramentas Externas
```bash
# Métricas de performance
- Lighthouse CI (mobile/desktop)
- WebPageTest (conexões limitadas)
- LoadRunner/K6 (testes de carga)
```

---

## Cronograma de Coleta

| Métrica | EU1 (Baseline) | EU2 (Aprofundamento) | EU3 (Consolidação) |
|---------|---------------|--------------------|-------------------|
| **Usabilidade** | Heurísticas + observação | Testes moderados | Quantificação final |
| **Confiabilidade** | Análise de logs locais | Simulação de falhas | Métricas de produção |
| **Performance** | Lighthouse básico | Testes de carga | Otimização validada |
| **Segurança** | Scan automatizado | Pentest manual | Compliance final |

---

## Referências GQM

- **Basili, V. R.** (1992). Software modeling and measurement: the Goal/Question/Metric paradigm
- **ISO/IEC 25023:2016** - Measurement of system and software product quality
- **ISO/IEC 25022:2016** - Measurement of quality in use
- **OWASP Top 10** - Application Security Risks

---

## Histórico do documento

| Versão | Data | Descrição | Autor |
|--------|------|-----------|--------|
| 1.0 | 01/05/2025 | Criação do plano GQM inicial | [Vinicius Vieira](https://github.com/viniciusvieira00) | 