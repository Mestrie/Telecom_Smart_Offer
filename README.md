#  Otimização de Ofertas em Telecom: Segmentação e Eficiência Operacional

Este projeto demonstra como a análise de dados pode transformar uma operação de Call Center, saindo de ofertas genéricas para uma estratégia de segmentação baseada no perfil financeiro e tecnológico do cliente.

##  Contexto de Negócio
O objetivo principal foi identificar ineficiências em uma campanha de vendas onde os planos eram ofertados sem considerar o gasto atual do cliente. Através da análise, busquei reduzir o desperdício operacional e proteger a receita da empresa (evitando downgrades).

##  Tecnologias e Metodologias
* **Linguagem:** Python
* **Bibliotecas:** Pandas (Tratamento), Seaborn & Matplotlib (Visualização)
* **Técnicas:** EDA (Análise Exploratória de Dados), Data Cleaning e Lógica de Negócio Aplicada.

##  Etapas do Projeto

### 1. Preparação e Limpeza
* Padronização de nomes de colunas (Lower Case) para garantir robustez ao código.
* Conversão de tipos de dados e tratamento de valores ausentes na coluna `totalcharges`.

### 2. Análise Exploratória (EDA)
Identifiquei um comportamento **bimodal** na distribuição de gastos mensais, revelando que a base é dividida entre clientes de baixo ticket e clientes premium. O cruzamento com a variável `internetservice` revelou que clientes sem internet possuem uma barreira de preço significativa para os planos padrão de R$ 38,00.

### 3. Implementação do Filtro Inteligente
Desenvolvi uma função lógica para categorizar a base em 4 pilares estratégicos:
1. **Alvo de Upgrade (DSL):** Clientes com tecnologia legada e potencial de aumento de ticket.
2. **Não ligar:** Clientes com baixíssima propensão de conversão (evitando custo de discagem).
3. **Manutenção:** Clientes de alto valor (Fibra) onde a oferta padrão representaria perda de receita.
4. **Oferta Padrão:** Clientes alinhados ao ticket médio da campanha.

##  Impacto Operacional
A aplicação do filtro resultou na seguinte distribuição da base:
* **41.3%** identificados como alvo prioritário para Upgrade.
* **17.5%** de economia em esforço operacional (leads descartados).
* **40.5%** de proteção de receita (bloqueio de downgrade).

---
*Este projeto faz parte do meu portfólio de análise de dados. Sinta-se à vontade para explorar os notebooks!*