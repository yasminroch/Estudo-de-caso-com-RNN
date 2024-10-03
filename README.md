# Estudo de caso com RNN
O presente trabalho foi realizado pelos alunos da primeira turma de Ciência da Computação da faculdade INTELI, os quais destacam-se:

* Gabriel Carneiro;
* Gabriel Nhoncanse;
* João Alcaraz;
* Pedro Munhoz;
* Pedro Romão;
* Sarah Ribeiro;
* Yasmin Vitória Rocha.

Com base na atividade proposta na quinta semana, referente a RNN com biblioteca, abaixo é possível visualizar os seguintes pontos de análise efetuada em equipe:
* Estudo de caso utilizado (Qual problema a implementação resolveu);
* Pontos positivos e negativos da implementação;
* Métrica utilizada (por exemplo: MAE, MSE e os valores obtidos)

Desse modo, a tabela tem a seguinte estruturação e corpo obtido após tal análise:
| Estudo de Caso                                                   | Métrica                                | Pontos Fortes                                                                 | Pontos Fracos                                                                                                                        |
|------------------------------------------------------------------|----------------------------------------|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| Nível de poluição de cidades no mundo ao longo dos anos           | MSE - 0,2796, MAE - 0,3150, R2 score - 0,8110 | O modelo conseguiu chegar muito próximo do real em todas as previsões, com grande assertividade. | Evolução da poluição de uma cidade ao longo do tempo não possui um padrão recorrente, o que dificulta a adequação do modelo ao mundo real. |
| Previsão do preço do boi gordo com base em dados históricos        | MAE - 0,0175                           | Normalização dos dados com MinMaxScaler, o que ajuda o modelo a convergir mais rapidamente. | Pode ser difícil prever os valores, pois podem ser afetados por fatores externos.                                                      |
| Predição de Receita para Diferentes Meses com Base na Quantidade de Vendas | MAE - 0.3                             | O dataset apresenta uma grande quantidade de meses, com dados que abrangem o período de 2015 a 2022. A implementação utilizando LSTM é enxuta e demonstra um treinamento estável. | A métrica final não apresenta um bom resultado, com um MAE muito alto. O modelo não utiliza fine-tuning para melhorar sua performance.    |
| Preço da cerveja ao longo dos meses                               | MSE - 0.0111                           | O dataset parece apresentar um padrão bem definido e boa performance durante o treinamento. | Modelo pode ter se ajustado demais aos dados específicos de treinamento, levando a um overfitting.                                     |
| Prever o valor total de transações em uma carteira digital com base nos dados históricos | MSE - 23009.42                              | Agrupamento das transações por data, o que facilitou a modelagem.                                | Não foi implementada nenhuma medida para mitigar overfitting.                                                                          |
| Prever o valor de uma cota da ação da Google | MSE - 165.82769, MAE - 9.10968, R2 score - 0.23701                                  | Base de dados simples e organizada, não necessitou muito pré-processamento. Modelo conseguiu treinar rapidamente.                                | Os valores alcançados nas métricas escolhidas não foram muito satisfatórios e, através de gráficos sobre o treinamento realizado, foi possível ver que um dos principais motivos para isso foi que o modelo não conseguiu aprender eficientemente, indicando que o treinamento poderia ter sido melhorado. |
| Prever a tendência dos preços de ações da Apple ao longo dos anos | MSE - 8.5295e-08                                  | Captura de tendências temporais: O modelo foi capaz de capturar a tendência geral dos dados, conseguindo acompanhar a curva dos valores reais; Generalização dos dados: O modelo consegue aprender a dinâmica temporal, tornando-o aplicável a dados financeiros similares de outras empresas como a Google por exemplo.                                | Mesmo com uma boa captura da tendência geral dos dados, o modelo apresentou dificuldades em capturar picos e vales, ou seja, prever grandes variações bruscas nos preços; Também foi observado que o MSE penaliza dando maior peso a grandes erros, sendo negativo para variações menores que podem ser toleradas.|

