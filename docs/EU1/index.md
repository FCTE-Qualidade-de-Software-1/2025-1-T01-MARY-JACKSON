# Introdução - Avaliação de Qualidade AgroMart

## Apresentação do Projeto

Este documento apresenta a **avaliação inicial de qualidade** do software **AgroMart**, conduzida pela equipe **MARY-JACKSON** no contexto da disciplina de Qualidade de Software (2025.1) da Universidade de Brasília.

---

## 🎯 **Propósito da Avaliação**

Realizar uma avaliação estruturada da qualidade de usabilidade do sistema AGROMART, baseada na norma **ISO/IEC 25010:2011**, identificando oportunidades de melhoria e fornecendo recomendações práticas para otimizar a experiência do usuário.

### Objetivos Específicos

- ✅ **Avaliar a usabilidade** das interfaces web e mobile segundo ISO 25010
- ✅ **Aplicar o framework GQM** para estruturar métricas de qualidade
- ✅ **Identificar gaps de acessibilidade** e conformidade WCAG
- ✅ **Propor melhorias concretas** baseadas em evidências observadas

---

## 📱 **Sobre o AgroMart**

### Visão do Produto

O **AgroMart** é uma solução digital que conecta **Comunidades que Sustentam a Agricultura (CSA)** a consumidores locais, promovendo uma cadeia de produção e consumo sustentável.

### Componentes Avaliados

| Componente | Público-Alvo | Funcionalidades Principais |
|------------|--------------|----------------------------|
| **🖥️ Interface Web (Strapi Dashboard)** | Administradores de CSA | • Gestão de conteúdo<br>• Controle de usuários<br>• Gerenciamento de pedidos<br>• Configuração de pagamentos |
| **📱 Interface Mobile (App)** | Consumidores/Co-agricultores | • Login e autenticação<br>• Histórico de pedidos<br>• Busca por lojas/produtos<br>• Carrinho de compras<br>• Planos de assinatura |

### Limitações do Ambiente de Teste

!!! warning "Contexto de Avaliação"
    - **Ambiente local**: Sistema executado localmente, não em produção
    - **Dados simulados**: Ausência de dados reais de uso
    - **APIs limitadas**: Algumas funcionalidades com falhas de conectividade
    - **Sem publicação oficial**: App não disponível em lojas oficiais

---

## 🌍 **Conexões com os ODS**

O projeto AgroMart contribui diretamente para os **Objetivos de Desenvolvimento Sustentável (ODS)**:

### 🏙️ **ODS 11 - Cidades e Comunidades Sustentáveis**
- Fortalece cadeias locais de abastecimento
- Reduz distâncias de transporte de alimentos
- Promove segurança alimentar urbana

### 🌱 **ODS 15 - Vida Terrestre** 
- Incentiva práticas agrícolas sustentáveis
- Apoia biodiversidade através de CSAs
- Reduz uso de agrotóxicos via agricultura orgânica

---

## 🔬 **Metodologia de Avaliação**

### Framework Principal: **ISO/IEC 25010:2011**

Focamos nas seguintes **características de qualidade**:

1. **🎯 Usabilidade** (prioridade máxima)
   - Reconhecimento da adequação
   - Aprendizado
   - Operabilidade
   - Proteção contra erros
   - Estética da interface
   - Acessibilidade

2. **🛡️ Confiabilidade** (segunda prioridade)
   - Maturidade
   - Disponibilidade
   - Tolerância a falhas

### Métodos Complementares

- **Heurísticas de Nielsen (1994)**: Validação prática de usabilidade
- **Framework GQM**: Estruturação Goal → Question → Metric
- **Observação direta**: Análise hands-on das interfaces

---

## 📊 **Estrutura da Avaliação EU1**

| Documento | Conteúdo | Objetivo |
|-----------|----------|----------|
| **[📋 Modelo de Qualidade](modelo-qualidade.md)** | Priorização ISO 25010, stakeholders, justificativas | Estabelecer requisitos de avaliação |
| **[🎯 Plano GQM](gqm.md)** | Goals, Questions, Metrics com rastreabilidade ISO | Estruturar medição objetiva |
| **[👥 Equipe](equipe.md)** | Contribuições, metodologia, % participação | Transparência e responsabilidades |
| **📈 Síntese de Resultados** | Tabela consolidada de achados | Quick wins e prioridades |

---

## 🔍 **Síntese de Resultados**

### Tabela de Avaliação (Resumo Executivo)

| Sub-característica | ✅ Pontos Fortes | ⚠️ Oportunidades de Melhoria |
|--------------------|------------------|------------------------------|
| **Reconhecimento da Adequação** | Menu lateral claro (web)<br>Layout direto (mobile) | Falta onboarding sobre CSAs |
| **Aprendizado** | Navegação consistente<br>Ícones familiares | Ausência de tutoriais contextuais |
| **Operabilidade** | Fluxo de pedidos funcional<br>Ações diretas | Melhorar feedbacks de interação |
| **Proteção contra Erros** | Validações básicas<br>Campos obrigatórios | Mensagens de erro mais específicas |
| **Estética da Interface** | Design moderno e limpo<br>Cores agradáveis | Preencher espaços vazios |
| **Acessibilidade** | Tipografia legível<br>Botões grandes | Implementar WCAG 2.1, leitores de tela |

---

## 🎯 **Principais Conclusões**

### ✅ **Aspectos Positivos**
- **Proposta sólida** com relevância social clara
- **Interfaces funcionais** e relativamente intuitivas
- **Design visual agradável** e moderno
- **Fluxos básicos** operacionais

### ⚠️ **Áreas Prioritárias para Melhoria**
1. **Acessibilidade**: Conformidade WCAG 2.1
2. **Onboarding**: Explicação do conceito CSA
3. **Feedback**: Mensagens de erro e confirmações
4. **Tutoriais**: Guias contextuais para novos usuários

---

## 🚀 **Próximos Passos (EU2)**

### Planejamento de Aprofundamento

| Atividade | Responsável | Método | Timeline |
|-----------|-------------|--------|----------|
| **Testes de Usabilidade** | Gabriel + Pablo | Sessões moderadas (5-8 usuários) | EU2 |
| **Métricas Automatizadas** | Vinicius | Lighthouse CI, análise estática | EU2 |
| **Auditoria de Acessibilidade** | Guilherme | WAVE, axe-core, testes manuais | EU2 |
| **Plano de Avaliação Detalhado** | Lucas | ISO 25040 Fases 2-3 | EU2 |

---

## 📚 **Bibliografia**

- **ISO/IEC 25010:2011** – Systems and software quality models
- **Nielsen, Jakob (1994)** – Usability Engineering  
- **Barbosa, S. D. J. et al. (2021)** – Interação Humano-Computador e Experiência do Usuário
- **CSA Brasil** – [https://csabrasil.org/csa/](https://csabrasil.org/csa/)
- **AgroMart GitHub** – [https://github.com/AgroMart/mobile-client](https://github.com/AgroMart/mobile-client)

---

## Histórico do documento

| Versão | Data | Descrição | Autor |
|--------|------|-----------|--------|
| 1.0 | 01/05/2025 | Criação do documento | [Vinicius Vieira](https://github.com/viniciusvieira00) |
| 1.1 | 01/05/2025 | Adição do conteúdo completo do relatório | [Vinicius Vieira](https://github.com/viniciusvieira00) |
| 2.0 | 01/05/2025 | Reestruturação como introdução da EU1 | [Vinicius Vieira](https://github.com/viniciusvieira00) |
