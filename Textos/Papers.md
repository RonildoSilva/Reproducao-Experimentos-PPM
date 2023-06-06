### Robust and Generalizable Predictive Models for Business Processes

we represent the categorical features using label encoding which has been shown to perform well on ordinal data such as those found in business process logs. This also ensures that we can handle multiple attributes without a large increase in model complexity (One-hot encoding for features with many unique values, can result in high dimensional input matrices, which can adversely impact model performance.) or the number of parameters.

Moreover, when these models are trained on data with a specific distribution, and have to generalize to data with slightly different distributions, they can often fail.

Even in business processes, real-world process models can have gradual or
sudden changes, such as concept drift. In addition, the logs used to train
models could be associated with different versions of process models modified
over time, or even be customized by different departments with differing policies

was influenced by the spurious correlation of the background

This is followed by two stacked LSTM layers as described in Sect. 2.4 and a dense output layer. 
Invariant Risk Minimization (IRM) to train robust and generalizable models

-----

@inproceedings{venkateswaran2021robust,
  title={Robust and generalizable predictive models for business processes},
  author={Venkateswaran, Praveen and Muthusamy, Vinod and Isahagian, Vatche and Venkatasubramanian, Nalini},
  booktitle={Business Process Management: 19th International Conference, BPM 2021, Rome, Italy, September 06--10, 2021, Proceedings},
  pages={105--122},
  year={2021},
  organization={Springer}
}

Esse trabalho visa também a predição do tempo restante para conclusão de um processo de negócio e utiliza de diversos datasets clássicos como o [HELPDEKS] e [BPI12] representa as features como dados categóricos, que possui, nesse ambiente, um bom desempenho quando se leva em considereção a ordem dos dados, como os encontrados em logs de processos de negócios. Há também a garantia de que se possa lidar com várias features sem um grande aumento na complexidade do modelo, se opondo à one-hot-encoding, que pode gerar um conjunto de dados de grandes dimensões, reduzindo o por muitas vezes, o desempenho do modelo.

Em processos de negócios, os modelos de processos do mundo real podem sofrer mudanças aos longo do tempo. Processo se tornam mais longos, com menos etapas, com prioridades distintas, etc. Além disso, os logs usados para treinar modelos podem estar associados a diferentes versões de processos modificados ao longo do tempo. Quando esses modelos de aprendizado de máquina são treinados em dados com uma distribuição específica e são testados com dados em que suas distribuições são diferentes, os resultados que o modelo preditivo irá gerar, pode não ser útil.

Desse modo, \citeonline{inproceedings} adicionou invariant features, que são informações de forte correlação (independente do conjunto de teste) entre as features e a label em questão, garantindo predições mais precisas. O modelo de aprendizado profundo é composto por duas camadas LSTM empilhadas e uma camada de saída densa.

## Comparations

-----
@inproceedings{venugopal2021comparison,
  title={A comparison of deep-learning methods for analysing and predicting business processes},
  author={Venugopal, Ishwar and T{\"o}llich, Jessica and Fairbank, Michael and Scherp, Ansgar},
  booktitle={2021 International Joint Conference on Neural Networks (IJCNN)},
  pages={1--8},
  year={2021},
  organization={IEEE}
}

A GCN layer operates by calculating a hidden embedding vector for each node of the graph. It calculates this hidden vector by combining each node’s feature-vector with the adjacency matrix for the graph,

The Timestamp Predictor Network on the other hand consists of ReLU activation for the first two layers and a linear activation function at the last layer. The training process uses the Mean Absolute Error as the loss function. An Adam optimizer

----

Para solucionar o problema de predição de tempo restante (em dias) nos datasets [HELPDESK] e [BPI12 W], [] utiliza de Graph Neural Networks (GNNs) como arquiterura do modelo. A representação das features como um grafo se dá pelas ordem de número de activities distintas \times número de features representativas (case_id, activity_id). Internamente, as camadas ocultas tratam de operaões matriciais que envolvem vetores que representam as n activities distintas multiplicados pelas matrizes de adjacências que representam o modelo de negócio. A rede neural apresentada é simples com duas camadas densas e uma camada de ativação ReLU entre elas. Adicionalmente, uma função de ativação linear com o otimizador Adam. No que se refere aos dados utilizados, tanto o [HELPDESK] e [BPI12 W] são particões dos conjuntos originais e naturalmente, vão existir menos activities distintas (matrizes menores) e menos registros. No processo de particionamento dos conjuntos de treino, teste e validação, há uma variável que tornam as amostras aleatórias. Por tanto, não se tem a garantia de que os cases estão ordenados pelo momento em que foram criados.

## Predicting Performances in Business processes using Deep Neural Networks

@article{park2020predicting,
  title={Predicting performances in business processes using deep neural networks},
  author={Park, Gyunam and Song, Minseok},
  journal={Decision Support Systems},
  volume={129},
  pages={113191},
  year={2020},
  publisher={Elsevier}
}

Thus, in this paper, we aim at developing a method to predict the future performances of a business process at the process model level to enable proactive actions to improve the business process.    

we generate a process representation matrix that contains information on the performances in the business process

In order to evaluate the evolution of the performances in the underlying business process, we need the time window upon which we calculate the temporal performance. If we want to measure the hourly evolution of performances in
the business process, we need the time windows of an hour

----

Esse trabalho desenvolve um método para prever o desempenho futuro de um processo de negócios à nível de modelo de negócio, objetivando também o suporte à ações proativas para melhorar o processo de negócios. Os conjuntos de dados utilizados são principalmente das competições [BPI] e [HELPDESK]. As features são representadas como matrizes que contém informações sobre os desempenhos no processo de negócios.
A avaliação do desempenho do processo de negócios tem como principal fator, uma da janela deslizante de tempo (por hora) na qual calcula-se o desempenho temporal a cada etapa ou incremento de uma hora. A arquiterura em si, é um híbrido de CNN e LSTM, uma Long-term Recurrent Convolutional Networks (LRCN), uma combinação de extração de features de matrizes em sequências temporais.