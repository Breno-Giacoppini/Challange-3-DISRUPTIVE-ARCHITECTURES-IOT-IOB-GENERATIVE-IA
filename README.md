# Sistema de Previsão de Estoque de Roupas com IA

## Descrição do Projeto
Este projeto implementa um sistema de previsão de vendas de roupas baseado em Inteligência Artificial (IA), com o objetivo de auxiliar na tomada de decisões sobre o reabastecimento de estoque, a partir de dados históricos e previsões automáticas.

## Arquitetura de IA

1. **Coleta e Entrada de Dados**
   - **Coleta Manual e Importação de CSV**: Permite inserir dados manualmente (modelo, tamanho e quantidade vendida) ou importá-los por meio de arquivos CSV.
   - **Relação Temporal dos Dados**: As vendas são registradas ao longo de períodos específicos (ex.: meses), fundamentais para o modelo de previsão de demanda.

2. **Pré-processamento dos Dados**
   - **Pandas para Manipulação de Dados**: A biblioteca Pandas estrutura os dados de vendas, contendo informações como modelo, tamanho e unidades vendidas em diferentes períodos.
   - **Codificação Categórica**: Utilizamos OneHotEncoder para transformar dados categóricos em representações numéricas compreensíveis pelo modelo de aprendizado.

3. **Modelo de Aprendizado de Máquina**
   - **Algoritmo: RandomForestRegressor**: Esse algoritmo de regressão é utilizado para prever variáveis contínuas, como a quantidade de unidades a serem reabastecidas.
   - **Divisão dos Dados**: Os dados são divididos em 80% para treino e 20% para teste, garantindo a validação das previsões.

4. **Predição**
   - **Entrada de Novos Períodos**: Após o treinamento do modelo, o sistema prevê vendas para períodos subsequentes, agrupando previsões por "modelo" e "tamanho" de roupa.

5. **Arquitetura Tecnológica**
   - **Linguagem Python**: Escolhida por sua robustez na manipulação de dados e aprendizado de máquina.
   - **Bibliotecas**: Utilizadas Pandas, NumPy, Scikit-learn, e o algoritmo RandomForestRegressor para predições.

6. **Benefícios e Eficiência**
   - **Escalabilidade**: O sistema pode ser facilmente escalado, permitindo a adição de novos dados e modelos sem grandes modificações.
   - **Precisão nas Previsões**: Gera previsões precisas, mesmo com variáveis categóricas, como modelos e tamanhos.

7. **Próximos Passos**
   - **Refinamento do Modelo**: O modelo será ajustado à medida que novos dados forem adicionados, aprimorando as previsões.
   - **Integração com Interfaces Web**: Utilizando frameworks como Flask ou Django, o projeto será disponibilizado em plataformas web, tornando a interação mais acessível.
   - **Análise de Sentimentos**: A inclusão de dados de redes sociais permitirá prever tendências de mercado e preferências dos consumidores, refinando ainda mais as previsões.

## Integração com Outras Disciplinas

1. **Qualidade e Teste de Software**
   - **Backlogs e Sprint Planning**: As previsões de produtos com maior demanda tornam a criação de backlogs e o planejamento de sprints mais eficientes, priorizando funcionalidades essenciais.
   - **Automação de Testes**: A IA sugere cenários para testes automatizados com base nas previsões, como o aumento de vendas de determinado produto.

2. **Java (API e Interface Gráfica)**
   - **Análise de Dados em Tempo Real**: Previsões de vendas podem ser exibidas em tempo real usando Thymeleaf e APIs, garantindo informações sempre atualizadas.
   - **Previsões Inteligentes**: Aplicações Java podem consumir diretamente os dados preditivos do código em Python, auxiliando nas decisões de reabastecimento e promoções.

3. **Mobile (Aplicativos e Navegabilidade)**
   - **Interface Inteligente**: O sistema envia notificações automáticas para reabastecimento, com base nas previsões de vendas.
   - **Navegação Personalizada**: A IA sugere ações no app, como promoções ou ajustes no estoque, conforme as previsões de vendas.

4. **Banco de Dados (Procedures e Trigger de Auditoria)**
   - **Otimização de Procedures**: Consultas otimizadas para grandes volumes de dados de vendas.
   - **Relatórios Dinâmicos**: Relatórios preditivos são gerados, permitindo análise detalhada das previsões.
   - **Trigger de Auditoria**: Triggers auditam previsões e comparam com os dados reais, monitorando a consistência.

5. **DevOps (Automatização e Infraestrutura em Nuvem)**
   - **Automação de Pipelines**: O sistema de previsão pode ser integrado a pipelines de CI/CD, automatizando previsões e processos de reabastecimento.
   - **Escalabilidade em Nuvem**: A infraestrutura de nuvem permite que o sistema escale conforme novos dados são inseridos, ajustando automaticamente as previsões.

6. **C# (Desenvolvimento de Aplicações e Otimização de Código)**
   - **Lógica de Negócios Dinâmica**: A previsão de vendas permite que a lógica de negócios seja ajustada em tempo real, melhorando a alocação de recursos e o gerenciamento de estoque.
   - **Automatização de Processos**: A integração com APIs e sistemas de gerenciamento de estoque desenvolvidos em C# automatiza processos e otimiza respostas à demanda do mercado.

## Conclusão Geral
A solução de previsão de estoque com IA não apenas otimiza a gestão de estoques e decisões de reabastecimento, mas também se integra com disciplinas como Qualidade de Software, Java, Mobile, Banco de Dados e DevOps. Isso transforma o projeto em uma ferramenta poderosa para melhorar a eficiência operacional e a experiência do usuário, garantindo decisões mais assertivas.
