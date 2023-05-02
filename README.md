# Classificador AVC
Por Alexandre Magno e Pedro Pertusi

# Descrição

# Como utilizar
* É possível instalar a aplicação de duas formas:
  - Clonagem do repositório utilizando o seguinte comando no terminal: `git clone https://github.com/PedroPertusi/Classificador-AVC`.
  - Ou baixar o arquivo zip desse repositório em `Code > Download Zip`. E descompactá-lo onde preferir.
* Em seguida, execute o comando: `pip install -r requirements.txt` no diretório principal do projeto clonado.
* Execute o programa com o seguinte comando: `python demo.ipynb`

# Modelo Matemático


# Análise e Conclusões

## Meotodologia

Para esta atividade foram elaborados dois classificadores: um classificador linear e um classificador de árvores de decisão. O objetivo desses classificadores era permitir a classificação de casos de AVC e também tirar conclusões e relações a partir dos nossos dados.

Um dos problemas iniciais veio justamente dos nossos dados, devido ao fato de um número muito maior de casos em que a pessoa não sofria um AVC, o mesmo acabava ficando enviesado, caindo assim no caso da nossa hipótese nula que apontava justamente para o quão eficiente seria o classificador, se pudéssemos apenas chutar sempre o mais frequente. Com o fim de procurar novos resultados, realizamos uma poda, que consistia em usar dados equilibrados, entre casos de AVC e não AVC. Com isso, apesar de diminuir nossa probabilidade de acerto, principalmente para o estimador em árvore, foi possível obter uma probabilidade de acerto acima da hipótese nula de 50%, ressaltando assim a influência de um dataframe não enviesado.