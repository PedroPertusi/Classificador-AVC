# Classificador AVC
Por Pedro Pertusi e Alexandre Magno

# Descrição

# Como utilizar
* É possível instalar a aplicação de duas formas:
  - Clonagem do repositório utilizando o seguinte comando no terminal: `git clone https://github.com/PedroPertusi/Classificador-AVC`.
  - Ou baixar o arquivo zip desse repositório em `Code > Download Zip`. E descompactá-lo onde preferir.
* Em seguida, execute o comando: `pip install -r requirements.txt` no diretório principal do projeto clonado.
* Execute o programa com o seguinte comando: `python demo.ipynb`

# Análise e Conclusões

## Meotodologia

Para esta atividade foram elaborados dois classificadores: um classificador linear e um classificador de árvores de decisão. O objetivo desses classificadores era permitir a classificação de casos de AVC e também tirar conclusões e relações a partir dos nossos dados.

Um dos problemas iniciais veio justamente dos nossos dados, devido ao fato de um número muito maior de casos em que a pessoa não sofria um AVC, o mesmo acabava ficando enviesado, caindo assim no caso da nossa hipótese nula que apontava justamente para o quão eficiente seria o classificador, se pudéssemos apenas chutar sempre o mais frequente. Com o fim de procurar novos resultados, realizamos uma poda, que consistia em usar dados equilibrados, entre casos de AVC e não AVC. Com isso, apesar de diminuir nossa probabilidade de acerto, principalmente para o estimador em árvore, foi possível obter uma probabilidade de acerto acima da hipótese nula de 50%, ressaltando assim a influência de um dataframe não enviesado.

## Referência
De acordo com o resultado descoberto pelo algoritmo de predição, foi possível classificar o tabagismo como a principal causa de AVC: Acidente Vascular Cerebral. Abaixo, foi extraído um trecho do artigo Smoking and stroke: the more you smoke the more you stroke, o qual comenta essa relação.

"The evidence linking smoking to stroke is extremely convincing. In short, these studies performed across various ethnicities and populations demonstrate a strong association between smoking and stroke risk, with current smokers having at least a two- to fourfold increased risk of stroke compared with lifelong nonsmokers or individuals who had quit smoking more than 10 years prior. In one study, the risk increased to sixfold when this population was compared with nonsmokers who had never been exposed to environmental tobacco smoke (i.e., second-hand smoke)." Reena S Shah & John W Cole (2010).

Reena S Shah & John W Cole (2010) Smoking and stroke: the more you smoke the more you stroke, Expert Review of Cardiovascular Therapy, 8:7, 917-932, DOI: 10.1586/erc.10.56

## Resultado Encontrado
