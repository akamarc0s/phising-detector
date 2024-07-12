# phising-detector
## Conceito do projeto
Esse projeito foi desenvolvido com o intuíto de mostrar e analisar a capacidade da IA Generativa em classificar se um texto de diferentes tipos (Email,SMS, HTML,URL) é phishing ou não. Para isso foi utilizado a API do Gemini 1.5 Pro, onde ele foi instruído usando a técnica de engenharia de prompt Chain-of-Thought (CoT) para resolver o problema passo-a-passo.

# Pré-requisitos e recursos utilizados
O projeto foi implementado em linguagem Python para tratamento dos dados, chamada da API do Gemini e geração de gráficos. Tudo isso feito no ambiente de desenvolvimento do Google Colab,  as bibliotecas e módulos utilizadas estão presentes no código. Os dados foram extraidos das seguintes fontes:
  1. Kaggle: https://www.kaggle.com/datasets/jackksoncsie/spam-email-dataset
  2. Huggingface: https://huggingface.co/datasets/ealvaradob/phishing-dataset

## Passo a passo
Para se chegar ao resultado final do projeto, seguimos os seguintes passos:
1. Estudo de artigos relacionados a classificação com o uso de IA Generativa;
2. Estudo de notebooks Python relacionados a engenharia de prompt;
3. Busca por datasets;
4. Manipulação dos datasets;
5. Conexão com a API do Gemini;
6. Construção do prompt que passado para API;
7. Execução do código e análise prévia do desempenho das chamadas à API;
8. Análise de resultados.

## Instalação
Passos necessários para se recriar o projeto:
1. Clonar/abrir o python notebook via Google Colab;
2. [Criação de chave de API Gemini](https://ai.google.dev/gemini-api/docs/api-key?hl=pt-br). Isso é necessário para gerar as respostas da IA;
3. Instalação dos datasets que estão na pasta: PREENCHER AQUI!;
4. Colocar datasets baixados na seção 'Montando o dataset' no notebook python (certifique-se de que colocou o caminho para o arquivo corretamente);
5. Caso coloque os datasets no Drive, conceda acesso a ele para o Google Colab durante a execução do notebook. Nós fizemos dessa maneira.

## Execução
1. Importação de bibliotecas
2. Conexão com Gemini API
3. Montando dataset
4. Prompt do modelo
5. Execução do modelo
6. Tratamento de resultados
7. Análise de resultados
## Bugs/problemas conhecidos
- Limitações da versão da IA
- Quantidade de amostras
- Tratamento e análise de possíveis erros
## Autores 
- André Luís de Sousa Oliveira
- Marcos Antônio de Santana Júnior

## Referências
Olhar doc de links úteis
[Colab bootcamp](https://colab.research.google.com/drive/1kxThsa3xEng6bupj4mOaW2PMlq1UNSKI?authuser=1)
[Gráficos/matriz de confusão](https://medium.com/data-hackers/entendendo-o-que-%C3%A9-matriz-de-confus%C3%A3o-com-python-114e683ec509)
Artigos:
- [ChatSpamDetector: Leveraging Large Language
Models for Effective Phishing Email Detection](https://arxiv.org/pdf/2402.18093)
- [SecureNet: A Comparative Study of DeBERTa and
Large Language Models for Phishing Detection](https://arxiv.org/pdf/2406.06663)
## Imagens
- Cálculos métricas
- Matriz de confusão
- Gráficos gerados
