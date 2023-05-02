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

## Resultado Encontrado

Em busca de obter resultados sobre quais características mais aparecem nos casos de AVC, como grupo, decidimos usar o classificador de Árvore de Decisão com poda nos dados, equilíbrio entre pessoas que tiveram AVC e que não tiveram, para assim obter as tais características mais impactantes. Para melhorar os resultados obtidos, além da poda do DataFrame mencionada acima, também foi realizada a exclusão de índices numéricos, como é o caso da idade, índice de massa corporal (IMC) e nível de glicose. Após tudo isso, realizamos o teste 10.000 vezes para, então, obter as top 5 características mais impactantes, apresentadas na tabela abaixo:

| Category                | Count |
|-------------------------|-------|
| hypertension             | 6468  |
| work_type_children       | 4330  |
| heart_disease            | 3655  |
| work_type_Private        | 3561  |
| smoking_status_smokes    | 3273  |


## Referências
De acordo com o resultado descoberto pelo algoritmo de predição, foi possível classificar a hipertensão como a principal causa de AVC: Acidente Vascular Cerebral. Abaixo, foi extraído um trecho do artigo 'Hipertensão arterial e AVC', o qual comenta essa relação.

"A hipertensão arterial (HA) é o principal fator de risco modificável para as doenças cerebrovasculares (DCV) principalmente para o AVC. Cerca de 80% dos AVCs estão relacionados à HA, que pode causar todos os diferentes tipos de AVC, como infarto, hemorragia, grandes AVCs ou lacunares e as demências vasculares. A detecção e controle da pressão arterial é um ponto básico e fundamental de qualquer programa de prevenção de AVC, devendo ser esse o maior foco." GAGLIARDI, Rubens José (2009).

"O controle da pressão arterial é um item fundamental e prioritário na prevenção primária ou secundária dos AVCs. Deve ser feito de modo exaustivo e contínuo, e, assim, estaremos oferecendo uma boa proteção aos nossos pacientes, frente a essa terrível doença que é o AVC." GAGLIARDI, Rubens José (2009).

Abaixo, selecionamos também um trecho do artigo "Smoking and stroke: the more you smoke the more you stroke", para comentar o AVC está relacionado a outro grande fator de risco encontrado pelo algoritmo, o tabagismo.

"The evidence linking smoking to stroke is extremely convincing. In short, these studies performed across various ethnicities and populations demonstrate a strong association between smoking and stroke risk, with current smokers having at least a two- to fourfold increased risk of stroke compared with lifelong nonsmokers or individuals who had quit smoking more than 10 years prior. In one study, the risk increased to sixfold when this population was compared with nonsmokers who had never been exposed to environmental tobacco smoke (i.e., second-hand smoke)." Reena S Shah & John W Cole (2010).

<hr>
GAGLIARDI, Rubens José. Hipertensão arterial e AVC. ComCiência,  Campinas,  n. 109,   2009 .   Available from <http://comciencia.scielo.br/scielo.php?script=sci_arttext&pid=S1519-76542009000500018&lng=en&nrm=iso>. access on  01  May  2023.

Reena S Shah & John W Cole (2010) Smoking and stroke: the more you smoke the more you stroke, Expert Review of Cardiovascular Therapy, 8:7, 917-932, DOI: 10.1586/erc.10.56

