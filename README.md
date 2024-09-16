# Sistema de Previsão de Estoque de Roupas com IA

## Descrição do Projeto

Este projeto implementa um sistema de previsão de vendas de roupas baseado em Inteligência Artificial (IA). O objetivo é ajudar o usuário a tomar decisões mais informadas sobre o reabastecimento de estoque com base em dados históricos de vendas e previsões automáticas.

## Arquitetura de IA

### 1. Coleta e Entrada de Dados
- **Coleta Manual e Importação de CSV**: O sistema oferece flexibilidade para coletar dados de vendas, seja através da inserção manual (onde o usuário escolhe o modelo, tamanho e quantidade vendida) ou pela importação de um arquivo CSV.
- **Relação Temporal dos Dados**: As vendas são registradas ao longo de diferentes períodos (ex.: meses), e esses dados temporais são essenciais para o modelo de previsão de demanda.

**Objetivo**: Alimentar o modelo de IA com dados suficientes para que ele consiga aprender padrões de vendas ao longo do tempo.

### 2. Pré-processamento dos Dados
- **Pandas para Manipulação de Dados**: A biblioteca Pandas é usada para estruturar e organizar os dados de vendas. Cada entrada contém informações sobre o modelo de roupa, tamanho e o número de unidades vendidas em períodos específicos.
- **Codificação Categórica com OneHotEncoder**: Para utilizar os dados categóricos (modelos, tamanhos e períodos) em algoritmos de aprendizado de máquina, esses dados precisam ser transformados em uma representação numérica. A ferramenta OneHotEncoder converte essas categorias em variáveis binárias (0 ou 1), o que permite que o modelo de regressão os compreenda.

**Objetivo**: Preparar os dados para o treinamento do modelo, eliminando ruídos e tornando-os utilizáveis para a máquina.

### 3. Modelo de Aprendizado de Máquina
- **Algoritmo Escolhido: RandomForestRegressor**: O modelo de aprendizado de máquina escolhido é o RandomForestRegressor, uma técnica de regressão baseada em árvores de decisão. Ele cria múltiplas árvores de decisão e combina seus resultados para fazer previsões mais precisas. Essa abordagem é robusta e eficaz para prever variáveis contínuas, como o número de unidades a serem compradas para o estoque.
- **Divisão dos Dados: Treino e Teste**: O conjunto de dados é dividido em duas partes: 80% para o treino e 20% para o teste, a fim de verificar a precisão das previsões.

**Objetivo**: Utilizar o modelo para capturar padrões nos dados históricos e prever vendas futuras com base nesses padrões.

### 4. Predição
- **Entrada de Novos Períodos**: Após o treinamento do modelo, ele é utilizado para prever as vendas de um próximo período (por exemplo, o mês seguinte). O sistema identifica o último período informado e gera previsões para o subsequente.
- **Agrupamento por Modelo e Tamanho**: As previsões são feitas para cada combinação de "modelo de roupa" e "tamanho", permitindo maior granularidade na análise de estoque.

**Objetivo**: Auxiliar o usuário a decidir quais peças e tamanhos devem ser priorizados no reabastecimento do estoque, com base em previsões automáticas.

### 5. Arquitetura Tecnológica Subjacente
- **Linguagem Python**: O Python foi escolhido devido à sua vasta utilização em ciência de dados e aprendizado de máquina, bem como pela grande disponibilidade de bibliotecas adequadas.
- **Bibliotecas Usadas**:
  - **Pandas e NumPy**: Para manipulação e análise de dados.
  - **Scikit-learn**: Para o pré-processamento, treino e teste do modelo de aprendizado de máquina.
  - **RandomForestRegressor**: O modelo que treina e faz as previsões de quantidades futuras de vendas.

**Objetivo**: Garantir que a arquitetura possa lidar com dados reais e complexos, mantendo uma interface simples e intuitiva para o usuário.

### 6. Benefícios e Eficiência do Sistema
- **Escalabilidade**: A arquitetura é facilmente escalável, permitindo a adição de novos dados e modelos de roupas sem grandes modificações.
- **Eficiência Preditiva**: O uso de Random Forest proporciona previsões precisas, mesmo com várias variáveis categóricas, como diferentes modelos e tamanhos de roupas.
- **Customização e Automação**: O usuário tem controle sobre os dados inseridos, e o sistema sugere automaticamente previsões de vendas futuras.

### 7. Próximos Passos na Implementação
- **Refinamento do Modelo**: À medida que mais dados forem adicionados e as variáveis de entrada ajustadas, o modelo poderá ser melhorado, resultando em previsões ainda mais precisas.
- **Integração com Interfaces Web**: Com frameworks como Flask ou Django, o projeto poderá ser transferido para uma plataforma web, permitindo uma interação mais visual e acessível.
- **Aprimoramento da Análise de Sentimentos**: A incorporação de dados de redes sociais e a análise de sentimentos poderão refinar ainda mais as previsões, considerando tendências de mercado e preferências dos consumidores.

## Conclusão
A arquitetura de IA desenvolvida utiliza técnicas avançadas de aprendizado de máquina para coletar, organizar e analisar dados históricos de vendas, prevendo a demanda futura de roupas específicas. A integração com bibliotecas poderosas como Pandas e Scikit-learn oferece uma base sólida para o crescimento do projeto, com potencial de melhorias contínuas à medida que mais dados são incorporados e novos recursos são implementados.

---
