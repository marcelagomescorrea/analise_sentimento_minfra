
<a href="https://ibb.co/CspPFFd"><img src="https://i.ibb.co/KzcKHHZ/Design-sem-nome.png" alt="Design-sem-nome" border="0"></a>

<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->

![GitHub repo size](https://img.shields.io/github/repo-size/iuricode/README-template?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/iuricode/README-template?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/iuricode/README-template?style=for-the-badge)
![Bitbucket open issues](https://img.shields.io/bitbucket/issues/iuricode/README-template?style=for-the-badge)


# Análise de sentimento do MINFRA

> Treinamento supervisionado de modelo de Machine Learning de classificação e Análise de Sentimento com base no texto dos comentários dos tweets coletados  do perfil institucional do Ministro de Infraestrutura no Twitter, a fim de auxiliar na tomada de decisão.


### Etapas do projeto

O projeto ainda está em desenvolvimento e as próximas atualizações serão voltadas nas seguintes tarefas:

- [x] Análise exploratória dos dados
- [x] Limpeza e preparação dos dados 
- [x] Treinamento e teste cego de modelos de classificação
- [x] Otimização de hiperparâmetros
- [x] Avaliação e interpretação dos resultados
- [ ] Apresentação para a área de negócio
- [ ] Implantação do modelo em produção

## 💻 Pré-requisitos do sistema

Antes de começar, verifique se você atendeu aos seguintes requisitos:
<!---Estes são apenas requisitos de exemplo. Adicionar, duplicar ou remover conforme necessário--->
* Máquina com sistema operacional `<Windows / Linux / Mac>`;
* Conta no Google Colaboratory;
* Linguagem de programação`<Python>`.

## ☕ Descrição do problema

O Ministério da Infraestrutura tem como visão tornar o Brasil líder em infraestrutura de transportes na América Latina e para isso é preciso “mensurar” o quão perto isso está de acontecer. Uma das formas de se fazer isso, seria utilizar os dados do Twitter analisando o que os cidadãos têm falado sobre as rodovias brasileiras, por exemplo. 

No entanto, analisar os dados de maneira manual e **classificar os tweets** nas classes **positivo, negativo ou questionamento** é uma **tarefa custosa, complexa** e passível de **erro humano** ou **subjetividade**.


## 🚀 Descrição da solução de IA

**Treinamento supervisionado** de modelo de **Machine Learning** de **classificação** e Análise de Sentimento com base no texto dos comentários dos twitters coletados  do perfil institucional do Ministro de Infraestrutura no Twitter.>


## 📫 Fonte dos dados
As bases de dados utilizadas são abertas e não possuem dados sigilosos. 

1.   [Banco de dados do MInfra:](https://github.com/marcelagomescorrea/analise_sentimento_minfra/blob/main/dados/replies_classificadas_minfra.csv) contém Tweets coletados e classificados manualmente pela área de negócio do MINFRA;
2.   [Base de dados do Kaggle com tweets já classificados](https://www.kaggle.com/augustop/portuguese-tweets-for-sentiment-analysis): para aumento do número da classe 'negativo';
3.   [Base de dados complementar:](https://github.com/marcelagomescorrea/analise_sentimento_minfra/blob/main/dados/replies_classificadas_plus.csv)Tweets coletados e classificados manualmente por nós para aumento do número da classe 'questionamento';


## :game_die: Variáveis independentes
Atributo **texto_reply**: contém os textos dos comentários do Tweeter.


## :dart: Variáveis dependentes
Atributo **classificacao**: contém as três classes de sentimentos <positivo, negativo ou questionamento>

## :books: Bibliotecas utilizadas
1. Exploração de dados: **Pandas, Numpy**
2. Visualização de dados: **Seaborn, Matplotlib, plotly**
3. Limpeza e Preparação dos dados: **Regex**
4. Processamento de Linguagem Natural: **NLTK, Spacy**
5. Treinamento: **Sklearn <Train Test Split, Cross validation>**
6. Modelos de Machine Learning: **Sklearn <SGDClassifier, SVC, DecisionTreeClassifier, RandomForestClassifier, MultinomialNB, XGBClassifier>**
7. Otimização de hiperparâmetros: **Sklearn <GridSearchCV, Pipeline>**
8. Avaliação dos resultados: **Sklearn <F1-score, DummyClassifier, Matriz de Confusão>**
9. Interpretação do modelo: **Sklearn <SGDClassifier.coef_>, Eli5**

## :raised_hands: Considerações Finais 
As **redes sociais** são, atualmente, **grandes fontes de dados** capazes de capturar a **opinião pública** sobre os mais **diversos assuntos**. Dessa forma, podem contribuir significativamente para o aumento da **participação social** nas **políticas públicas**.

Esse projeto buscou mensurar a opinião pública sobre o tema de negócio  **rodovias**, do **Ministério de Infraestrutura** e avaliar sua aplicabilidade para **melhoria da tomada de decisão** no âmbito institucional. 

Os resultados aferidos pela aplicação da **análise de sentimento** foram capazes de identificar com **precisão satisfatória** o número de opiniões positivas, negativas e questionamentos referentes ao tema "rodovias" adotado como objeto de estudo.

Conforme demonstrado pela métrica **F1 score**, que combina precisão e *recall*, houve **qualidade geral** do modelo de **80% **que indica a possibilidade de aplicação em produção, inclusive em conjunto de **dados desbalanceados**.

Segue abaixo, demais considerações sobre o modelo desenvolvido:

### :chart_with_upwards_trend: **Benefícios para o Negócio**


*    Extração de *insights*, que permitem ao gestor atuar de forma proativa e redefinir estratégias de ação (cidadão como parceiro e coprodutor de políticas públicas):
       - Reclamações sobre o preço dos pedágios;
       - Questionamento sobre duplicação de trechos rodoviários e BR470;
      
*   Entendimento de como os clientes enxergam o negócio (cidadão como sensor e não apenas alvo de informações do governo):
      - Verificou-se uma maior quantidade de comentários positivos em relação aos negativos e questionamentos, no período apurado. 

*   Visão abrangente e próximo do tempo real do *feedback* dos usuários em todo território nacional.


### :chart_with_downwards_trend: **Pontos de melhoria**

*   A biblioteca utilizada no processo de lematização não funciona tão bem com palavras em português;
*   Melhoria do processo de limpeza, que é custoso;
*   Melhoraria e padronização do processo de coleta:
    - foram perdidos os *emojis* durante a coleta?
    - houve moderação?
    - classificação enviesada por ter sido feita apenas por uma pessoa?
*   Nova coleta de tweets negativos e questionamento pela área de negócio;
*   Utilização de modelo pré-treinado, como o BERT, seria mais eficiente?
*   Utilização de técnicas de *deep learning*;
*   Aplicar técnicas capazes de melhorar a precisão da classificação automatizada em textos com alta carga de ironia e ambiguidade. 

## 🤝 Colaboradores

Agradecemos às seguintes pessoas que contribuíram para este projeto:

<table>
  <tr>
    <td align="center">
      <a href="#">
        <img src="https://media-exp1.licdn.com/dms/image/C5603AQFj0jsCGywiOg/profile-displayphoto-shrink_800_800/0/1516350646007?e=1645056000&v=beta&t=Y8a5qAi_LOnTUJgehh6PQ-HxXgYfolcCBdewhec0sf0" width="100px;" alt="Foto do Edmundo no GitHub"/><br>
        <sub>
          <b>Francisco Edmundo Andrade</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://media-exp1.licdn.com/dms/image/C4E03AQGzjEUjiIvC8g/profile-displayphoto-shrink_800_800/0/1637205640390?e=1645056000&v=beta&t=KGobfhdsFnnCbUWH9u7m02IVpc2SNd6OGWqXH0-C2sw" width="100px;" alt="Liliane Vieira Lopes"/><br>
        <sub>
          <b>Liliane Vieira Lopes</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://media-exp1.licdn.com/dms/image/C5603AQF7135aqFs7ag/profile-displayphoto-shrink_800_800/0/1517602492222?e=1645056000&v=beta&t=0nN7RJNov3ZVdy3h-JOUf9Hb06z2H8vUhsM_QeJGFec" width="100px;" alt="Foto da Marcela"/><br>
        <sub>
          <b>Marcela Gomes Corrêa</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://scontent.fbsb3-1.fna.fbcdn.net/v/t31.18172-8/340515_10150313675155895_948037750_o.jpg?_nc_cat=103&ccb=1-5&_nc_sid=174925&_nc_eui2=AeEZ2wUYSl6Hh4-GjqfW5mKaOqSqyuq0G5A6pKrK6rQbkAFDlMQg0AU3hvw1bTwe7RMNkVSRrGfRwchUpKjNn5Ph&_nc_ohc=DCVeWz8fF64AX-9aSsA&_nc_ht=scontent.fbsb3-1.fna&oh=00_AT_6bzsGquJ5-q7R8IXtVtS0cI0kdO7MdqrtbCuFWajg9A&oe=61DDE495" width="100px;" alt="Foto do Iuri Silva no GitHub"/><br>
        <sub>
          <b>Priscilla A. S. Rodrigues</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://media-exp1.licdn.com/dms/image/C4E03AQFbvlQwbdb4Kw/profile-displayphoto-shrink_800_800/0/1516338237063?e=1645056000&v=beta&t=fspFF5TSjafN5DNrVJyI5R2uHz7uwSN5msITPTZUrV8" width="100px;" alt="Foto do Jose Renato Borelli no linkedin"/><br>
        <sub>
          <b>Jose Renato Borelli</b>
        </sub>
      </a>
    </td>
  </tr>
</table>



## 📝 Licença

Esse projeto está sob licença Creative Commons. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.


[⬆ Voltar ao topo](#nome-do-projeto)<br>

<a href="https://ibb.co/6wwFdfR"><img src="https://i.ibb.co/g99JnBM/Realiza-o.png" alt="Realiza-o" border="0"></a>



