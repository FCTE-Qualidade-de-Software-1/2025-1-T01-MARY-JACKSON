# Modelo de Qualidade ISO/IEC 25010

## Fase 1 do Processo ISO 25040 - Estabelecer Requisitos de Avaliação

### Propósito da Avaliação

Avaliar a qualidade do software **AgroMart** com foco em **usabilidade** e **confiabilidade**, identificando oportunidades de melhoria para otimizar a experiência do usuário e garantir a estabilidade do sistema.

### Escopo

- **Produto**: Sistema AgroMart (interface web + mobile)
- **Usuários-alvo**: Administradores de CSA e consumidores/co-agricultores
- **Contexto de uso**: Ambiente de produção simulado localmente
- **Limitações**: Testes realizados em ambiente local, sem dados reais de produção

### Stakeholders Identificados

| Stakeholder | Interesse Principal | Impacto na Avaliação |
|-------------|---------------------|---------------------|
| **Desenvolvedores** | Identificar pontos de melhoria técnica | Alto - direcionamento de refatoração |
| **Administradores CSA** | Interface web eficiente e confiável | Alto - produtividade operacional |
| **Consumidores** | App mobile intuitivo e estável | Alto - experiência de compra |
| **Investidores/Gestores** | ROI e sustentabilidade da plataforma | Médio - viabilidade do negócio |

---

## Modelo de Qualidade Selecionado

Baseado na **ISO/IEC 25010:2011**, com foco nas características mais críticas para o contexto do AgroMart.

### Priorização de Características de Qualidade

| Rank | Característica | Sub-características Priorizadas | Justificativa | Peso |
|------|----------------|--------------------------------|---------------|------|
| **1º** | **Usabilidade** | • Reconhecimento da adequação<br>• Aprendizado<br>• Operabilidade<br>• Proteção contra erros<br>• Estética da interface<br>• Acessibilidade | **Crítica**: Público diverso (CSAs rurais + consumidores urbanos) necessita interface intuitiva. Baixa usabilidade = abandono da plataforma. | 40% |
| **2º** | **Confiabilidade** | • Maturidade<br>• Disponibilidade<br>• Tolerância a falhas<br>• Recuperabilidade | **Alta**: Operações comerciais dependem de uptime. Falhas impactam renda dos produtores e confiança dos consumidores. | 25% |
| **3º** | **Eficiência de Performance** | • Comportamento temporal<br>• Utilização de recursos | **Média-Alta**: App mobile deve ser responsivo mesmo em conexões rurais limitadas. | 15% |
| **4º** | **Segurança** | • Confidencialidade<br>• Integridade<br>• Autenticidade | **Média**: Dados pessoais e transações financeiras requerem proteção adequada. | 10% |
| **5º** | **Compatibilidade** | • Coexistência<br>• Interoperabilidade | **Média**: Integração com sistemas de pagamento e APIs externas. | 5% |
| **6º** | **Manutenibilidade** | • Modularidade<br>• Reusabilidade<br>• Analisabilidade | **Baixa para EU1**: Foco inicial em aspectos externos ao usuário. | 3% |
| **7º** | **Portabilidade** | • Adaptabilidade<br>• Instalabilidade | **Baixa para EU1**: Aplicação web + mobile nativo já atende principais plataformas. | 2% |

---

## Justificativas Detalhadas

### 🥇 **Usabilidade (40%)**

**Por que é prioritária:**
- **Diversidade de usuários**: CSAs rurais (baixa familiaridade tecnológica) + consumidores urbanos (alta expectativa UX)
- **Impacto direto no negócio**: Interface complexa = perda de vendas e desistência de produtores
- **Sustentabilidade social**: Facilitar acesso a alimentos locais depende de tecnologia acessível

**Sub-características críticas:**
- **Aprendizado**: Curva de aprendizado suave para novos usuários
- **Acessibilidade**: Conformidade WCAG para inclusão digital
- **Proteção contra erros**: Evitar perdas de pedidos e dados

### 🥈 **Confiabilidade (25%)**

**Por que é segunda prioridade:**
- **Impacto econômico**: Downtime = perda de receita direta para CSAs
- **Sazonalidade**: Picos de demanda (colheitas) exigem alta disponibilidade
- **Confiança do consumidor**: Falhas recorrentes prejudicam adoção da plataforma

### 🥉 **Performance (15%)**

**Por que é terceira:**
- **Contexto rural**: Conectividade limitada em algumas CSAs
- **Mobile-first**: App deve ser otimizado para devices com recursos limitados
- **Competitividade**: Usuários comparam com e-commerces estabelecidos

---

## Exclusões Justificadas

| Característica | Motivo da Exclusão/Baixa Prioridade |
|----------------|-------------------------------------|
| **Funcionalidade** | Assumida como satisfatória na versão atual - foco em aspectos qualitativos |
| **Manutenibilidade** | Relevante para desenvolvedores, mas não impacta usuário final em EU1 |
| **Portabilidade** | Cobertura atual (web + mobile) atende 95%+ dos casos de uso |

---

## Referências Aplicadas

- **ISO/IEC 25010:2011** - Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — System and software quality models
- **ISO/IEC 25040:2011** - Systems and software engineering — Systems and software Quality Requirements and Evaluation (SQuaRE) — Evaluation process
- **WCAG 2.1** - Web Content Accessibility Guidelines (W3C)

---

## Histórico do documento

| Versão | Data | Descrição | Autor |
|--------|------|-----------|--------|
| 1.0 | 01/05/2025 | Criação da priorização de qualidade | [Vinicius Vieira](https://github.com/viniciusvieira00) | 