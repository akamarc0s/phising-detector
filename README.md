# phishing-detector
## Conceito do projeto

Phishing é uma técnica de ataque cibernético que busca enganar pessoas para que revelem informações sensíveis, como senhas, dados bancários ou números de cartões de crédito, através de comunicações fraudulentas que aparentam ser confiáveis. Esses ataques geralmente ocorrem via e-mails, mensagens de texto (SMS), sites falsos ou até por meio de URLs aparentemente legítimas, que direcionam as vítimas a páginas que coletam suas informações pessoais. O atacante se passa por uma entidade confiável, como um banco, uma loja online ou uma instituição governamental, para ganhar a confiança da vítima e convencê-la a fornecer esses dados.

O phishing é considerado uma das formas mais comuns de cibercrime devido à sua simplicidade e à alta taxa de sucesso, afetando tanto indivíduos quanto empresas. Por isso, métodos avançados de detecção de phishing, como  processamento de linguagem natural (Natural Processing Language - NLP), como também o uso de IA generativa para classificar automaticamente comunicações suspeitas, são essenciais para prevenir esses ataques e proteger usuários e organizações.

Este projeto foi desenvolvido com o objetivo de explorar e analisar o potencial da Inteligência Artificial Generativa na classificação de textos de diferentes tipos (Email, SMS, HTML, URL) como phishing ou não. A ferramenta utilizada para esse estudo foi a API do Gemini 1.5 Pro, que representa um dos avanços mais recentes em modelos de IA generativa. Para maximizar a precisão e a eficiência do modelo na tarefa de classificação, foi empregada a técnica de engenharia de prompt Chain-of-Thought (CoT), que permite ao modelo abordar o problema de forma sequencial, raciocinando passo a passo durante o processo de tomada de decisão. Essa abordagem não apenas melhora a compreensão da IA sobre o problema, mas também torna o processo de classificação mais transparente e explicável.

A aplicação deste método fornece insights sobre como a IA pode ser usada em cenários de cibersegurança, especialmente na detecção de tentativas de phishing, que continuam a ser uma das ameaças mais prevalentes no ambiente digital.

# Pré-requisitos e recursos utilizados
O projeto foi implementado em linguagem Python para tratamento dos dados, chamada da API do Gemini e geração de gráficos. Tudo isso feito no ambiente de desenvolvimento do Google Colab,  as bibliotecas e módulos utilizadas estão presentes no código. Os dados foram extraidos das seguintes fontes:
  1. Kaggle: https://www.kaggle.com/datasets/jackksoncsie/spam-email-dataset
  2. Huggingface: https://huggingface.co/datasets/ealvaradob/phishing-dataset

## Passo a passo
Para se construir o projeto como um todo, seguimos os seguintes passos:
1. Estudo de artigos relacionados a classificação com o uso de IA Generativa;
2. Estudo de notebooks Python relacionados a engenharia de prompt;
3. Busca por datasets;
4. Manipulação dos datasets;
5. Randomização das entradas;
6. Conexão com a API do Gemini;
7. Construção do prompt usado com a API;
8. Execução do código e análise prévia do desempenho das chamadas à API;
9. Análise de resultados;

## Instalação
Passos necessários para se recriar o projeto:
1. Clonar/abrir o python notebook via Google Colab;
2. [Criação de chave de API Gemini](https://ai.google.dev/gemini-api/docs/api-key?hl=pt-br). Isso é necessário para gerar as respostas da IA;
3. Instalação do dataset **dataset_final_250.csv** que está na pasta datasets;
4. (Opcional) Caso queira recriar a partir dos datasets iniciais, baixe os datasets referenciados na seção de Pré-requisitos. Webs.json, urls.json e texts.json da fonte HuggingFace e emails.csv do Kaggle. 
5. Caso coloque o dataset no Drive, conceda acesso a ele para o Google Colab durante a execução do notebook. Nós fizemos dessa maneira.


## Execução

Esses são os passos necessários para se reproduzir os resultados, a partir dos códigos presente na pasta 'notebooks':

1. Importação de bibliotecas;
2. Conexão com Gemini API;
3. Montar ou importar dataset;
4. Prompt do modelo;
5. Execução do modelo;
6. Tratamento de resultados;
7. Análise de resultados;
8. Criação de gráficos.

Há duas maneiras de se executar o projeto, mas todas seguem os passos de execução acima. No número 3 - *Montar/importar dataset* - é preciso decidir qual opção seguir:
1. (Padrão) Seguir com o **dataset_final_250.csv** e executar passo-a-passo do dataset **exec_model.ipynb**;
2. Criar sua própria entrada, utilizando o notebook **build_dataset.ipynb** e utilizar o resultado no notebook **exec_model.ipynb**. Na seção de instalação há os detalhes sobre o que precisa ser feito caso se opte por essa opção.

Cada célula do notebook possuí mais informações sobre o que foi feito em cada etapa.
   
## Bugs/problemas conhecidos

Sendo um projeto com IA gratuita, nossa expectiva já não estava tão alta em relação ao seu desempenho, tanto que nosso principal objetivo é analisar o potencial, ver se gratuitamente conseguimos obter um bom resultado. Ademais, a quantidade de chamadas a API é limitada, o que nos obrigou a reduzir o tamanho do dataset, devido a isso, não conseguimos trabalhar com novos reprocessamentos ou melhorias no modelo. A capacidade de generalização que nosso protótipo pode ter é questionada por esse ponto, a quantidade de amostras. Com mais testes poderiamos ser mais assertivos em relação a sua efetividade, principalmente entendendo os pontos de melhoria após a análise de resultados feita no fim do projeto.

  
## Autores 
- André Luís de Sousa Oliveira [(Contato)](https://www.linkedin.com/in/marcos-asj/)
- Marcos Antônio de Santana Júnior [(Contato)](https://www.linkedin.com/in/andre-luis-a05409211/)

## Referências
[Gráficos/matriz de confusão](https://medium.com/data-hackers/entendendo-o-que-%C3%A9-matriz-de-confus%C3%A3o-com-python-114e683ec509)

[ChatSpamDetector: Leveraging Large Language
Models for Effective Phishing Email Detection](https://arxiv.org/pdf/2402.18093)

[SecureNet: A Comparative Study of DeBERTa and
Large Language Models for Phishing Detection](https://arxiv.org/pdf/2406.06663)

## Imagens
- Cálculos métricas:
  
Essas métricas de avaliação nos ajuda a avaliar o desempenho do modelo. Tivemos **64% de acurácia de classificação**.
  
![Imagem](https://github.com/akamarc0s/phising-detector/blob/main/images/metricas.png)

- Matriz de confusão:

A matriz de confusão nos ajuda a entender como está a distribuição do nosso resultado. Utilizamos essas informação para guiar na geração dos gráficos e analisar especificamente entradas.

![Imagem](https://github.com/akamarc0s/phising-detector/blob/main/images/matriz_confusao.png)

- Gráficos gerados:

**Distribuição de tipos**

Buscamos adicionar diferentes tipos de entradas para diversificar o dataset, visto que, a maioria dos datasets são somentes de E-mails. A classificação foi feita pelo modelo.

![Imagem](https://github.com/akamarc0s/phising-detector/blob/main/images/distri_tipo_msg.png)

**Distruibição de pontuação do phishing**

Interessante observar que a API não nos retornou nenhuma resposta na faixa de 3-7, indicando que ele sempre busca indicar que suas escolhas são assertivas.

![Imagem](https://github.com/akamarc0s/phising-detector/blob/main/images/hist_dist_pont_phishing.png)

**Nuvem de palavras**

A nuvem de palavras nos ajuda a ter uma ideia de quais são osprincipais temas abordados nos textos presentes do dataset, palavras como "Enron" e "Dynergy" se referem a empresas do ramo de energia, outras palavras presentes na nuvem como "energy" e "power" nos ajuda a entender que há bastante palavras que se referem a utilização de energia. Lembrando, nosso dataset é randomizado, então, há diversos temos e a cardinalidade de temas/palavras é grande.

![Imagem](https://github.com/akamarc0s/phising-detector/blob/main/images/nuvem_palavras.png)

