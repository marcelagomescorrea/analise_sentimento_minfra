
<a href="https://ibb.co/CspPFFd"><img src="https://i.ibb.co/KzcKHHZ/Design-sem-nome.png" alt="Design-sem-nome" border="0"></a>

<!---Esses são exemplos. Veja https://shields.io para outras pessoas ou para personalizar este conjunto de escudos. Você pode querer incluir dependências, status do projeto e informações de licença aqui--->

![GitHub repo size](https://img.shields.io/github/repo-size/iuricode/README-template?style=for-the-badge)
![GitHub language count](https://img.shields.io/github/languages/count/iuricode/README-template?style=for-the-badge)
![GitHub forks](https://img.shields.io/github/forks/iuricode/README-template?style=for-the-badge)
![Bitbucket open issues](https://img.shields.io/bitbucket/issues/iuricode/README-template?style=for-the-badge)
![Bitbucket open pull requests](https://img.shields.io/bitbucket/pr-raw/iuricode/README-template?style=for-the-badge)

# Análise de sentimento do MINFRA

> Treinamento supervisionado de modelo de Machine Learning de classificação e Análise de Sentimento com base no texto dos comentários dos twitters coletados  do perfil institucional do Ministro de Infraestrutura no Twitter.
> 

### Ajustes e melhorias

O projeto ainda está em desenvolvimento e as próximas atualizações serão voltadas nas seguintes tarefas:

- [x] Análise exploratória
- [x] Limpeza e preparação dos dados 
- [x] Treinamento e teste cego de modelos de classificação
- [x] Otimização de hiperparâmetros
- [x] Avaliação e interpretação de resultados
- [ ] Colocar o modelo em produção

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:
<!---Estes são apenas requisitos de exemplo. Adicionar, duplicar ou remover conforme necessário--->
* Você tem uma máquina `<Windows / Linux / Mac>`.
* Criar uma conta no Google Colaboratory `<Jupter Notebook/ Python/ Sklearn>`

## 🚀 Descrição do problema

O Ministério da Infraestrutura tem como visão tornar o Brasil líder em infraestrutura de transportes na América Latina e para isso é preciso “mensurar” o quão perto isso está de acontecer. Uma das formas de se fazer isso, seria utilizar os dados do Twitter analisando o que os cidadãos têm falado sobre as rodovias brasileiras, por exemplo. 

No entanto, analisar os dados de maneira manual e **classificar os tweets** nas classes **positivo, negativo ou questionamento** é uma tarefa **custosa, complexa** e passível de **erro humano** ou **subjetividade**.


## ☕ Descrição da solução de IA

**Treinamento supervisionado** de modelo de **Machine Learning** de **classificação** e Análise de Sentimento com base no texto dos comentários dos twitters coletados  do perfil institucional do Ministro de Infraestrutura no Twitter.>


## 📫 Fonte dos dados
As bases de dados utilizadas são abertas e não possuem dados sigilosos. 

1.   [Banco de dados do MInfra:]() contém Tweets coletados e classificados manualmente pela área de negócio do MINFRA;
2.   [Base de dados do Kaggle com tweets já classificados](https://www.kaggle.com/augustop/portuguese-tweets-for-sentiment-analysis): para aumento do número da classe 'negativo';
3.   [Base de dados complementar:]()Tweets coletados e classificados manualmente por nós para aumento do número da classe 'questionamento';


## Variáveis independentes
Atributo **texto_reply**: contém os textos dos comentários do Tweeter.


## Variáveis dependentes
Atributo **classificacao**: expressa três classes de sentimentos <positivo, negativo ou questionamento>

## 🤝 Técnicas utilizadas
1. Exploração de dados: **Pandas, Numpy**
2. Visualização de dados: **Seaborn, Matplotlib**
3. Limpeza e Preparação dos dados: **Regex**
4. Processamento de Linguagem Natural: **NLTK, Spacy**
5. Treinamento: **Train Test Split, Cross validation**
6. Modelos de Machine Learning: **SGDClassifier, SVC, DecisionTreeClassifier, RandomForestClassifier, MultinomialNB, XGBClassifier**
7. Otimização de hiperparâmetros: **GridSearchCV**
8. Avaliação dos resultados: **F1-score, DummyClassifier, Matriz de Confusão**
9. Interpretação do modelo: **SGDClassifier.coef_, Eli5**

## 🤝 Considerações Finais 
As **redes sociais** são, atualmente, **grandes fontes de dados** capazes de capturar a **opinião pública** sobre os mais **diversos assuntos**. Dessa forma, podem contribuir significativamente para o aumento da **participação social** nas **políticas públicas**.

Esse projeto buscou mensurar a opinião pública sobre o tema de negócio  **rodovias**, do **Ministério de Infraestrutura** e avaliar sua aplicabilidade para **melhoria da tomada de decisão** no âmbito institucional. 

Os resultados aferidos pela aplicação da **análise de sentimento** foram capazes de identificar com **precisão satisfatória** o número de opiniões positivas, negativas e questionamentos referentes ao tema "rodovias" adotado como objeto de estudo.

Conforme demonstrado pela métrica **F1 score**, que combina precisão e *recall*, houve **qualidade geral** do modelo de **80% **que indica a possibilidade de aplicação em produção, inclusive em conjunto de **dados desbalanceados**.

Segue abaixo, demais considerações sobre o modelo desenvolvido:

### **Benefícios para o Negócio**


*    Extração de *insights*, que permitem ao gestor atuar de forma proativa e redefinir estratégias de ação (cidadão como parceiro e coprodutor de políticas públicas):
       - Reclamações sobre o preço dos pedágios;
       - Questionamento sobre duplicação de trechos rodoviários e BR470;
      
*   Entendimento de como os clientes enxergam o negócio (cidadão como sensor e não apenas alvo de informações do governo):
      - Verificou-se uma maior quantidade de comentários positivos em relação aos negativos e questionamentos, no período apurado. 

*   Visão abrangente e próximo do tempo real do *feedback* dos usuários em todo território nacional.



---



### **Pontos de melhoria**

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
        <img src="https://avatars3.githubusercontent.com/u/31936044" width="100px;" alt="Foto do Iuri Silva no GitHub"/><br>
        <sub>
          <b>Iuri Silva</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://s2.glbimg.com/FUcw2usZfSTL6yCCGj3L3v3SpJ8=/smart/e.glbimg.com/og/ed/f/original/2019/04/25/zuckerberg_podcast.jpg" width="100px;" alt="Foto do Mark Zuckerberg"/><br>
        <sub>
          <b>Mark Zuckerberg</b>
        </sub>
      </a>
    </td>
    <td align="center">
      <a href="#">
        <img src="https://miro.medium.com/max/360/0*1SkS3mSorArvY9kS.jpg" width="100px;" alt="Foto do Steve Jobs"/><br>
        <sub>
          <b>Steve Jobs</b>
        </sub>
      </a>
    </td>
  </tr>
</table>


## 😄 Seja um dos contribuidores<br>

Quer fazer parte desse projeto? Clique [AQUI](CONTRIBUTING.md) e leia como contribuir.

## 📝 Licença

Esse projeto está sob licença. Veja o arquivo [LICENÇA](LICENSE.md) para mais detalhes.

[⬆ Voltar ao topo](#nome-do-projeto)<br>

