#### Aluno: [Máurion Lourenço de Freitas](https://github.com/link_do_github)
#### Orientador: [Felipe Borges](https://github.com/FelipeBorgesC)

---

Trabalho apresentado ao curso [BI MASTER](https://ica.puc-rio.ai/bi-master) como pré-requisito para conclusão de curso e obtenção de crédito na disciplina "Projetos de Sistemas Inteligentes de Apoio à Decisão".

- [Link para o código](https://github.com/maurionFreitas/ProjetoFinal---PUC/blob/main/Projeto%20Dieta.zip).

---

### Resumo

Com o propósito de se tentar restabelecer o peso ideal com uma dieta hipocalórica (balanceada) com base proposta no Livro “Poder sem limites”, de Tony Robbins, com algumas alterações, me deparei com algumas dificuldades na criação de refeições a dieta proposta.
Sendo assim, o objetivo está em criar uma ferramenta que gere inúmeras refeições com combinações (tentando sempre não ter os mesmos alimentos no dia) com o alvo calórico diário estabelecido (no máximo de 2 mil) obedecendo as restrições impostas pela dieta.
A dieta proposta por Tony Robbins não prioriza restrições em calorias, mas sim em combinações de alimentos que facilitam a digestão, a restrição de calorias diárias é similar a uma dieta comum de 2000 cal/dia, não podendo superar esse valor, e sim como alvo diário.
A dieta deverá ser realizada por 7 dias, podendo ser replicada por quantas semanas quiser, porém impõe o consumo de 4 refeições diárias com intervalo mínimo de 3 horas entre cada refeição.
Não é permitida a ingestão de líquidos durante as refeições.


### 1. Introdução

A dieta consiste com refeições tendo alimentos distribuídos em 4 categorias: Proteínas, Carboidratos, Vegetais e Frutas.
Cada refeição não pode conter itens de carboidratos e proteínas juntos, na mesma refeição.
Já as frutas, são permitidas no lanche da tarde porém não devem estar presente nas demais refeições.
O café da manhã possui restrições adicionais de permissão, há um campo próprio campo informando quais são permitidos ou não.
As refeições possuem no mínimo 3 e no máximo 5 itens, tirando o café da manhã, que possui somente 3 itens na sua composição, para todas as refeições é necessário que tenha 3 itens distintos no mínimo.


### 2. Modelagem

Foram cadastrados uma lista com 190 produtos, no sistema via tela de cadastro, indexados e com a quantidade de calorias, porções, categoria (proteínas, carboidratos, frutas ou vegetais) e se são permitidos ou não no café da manhã. Os alimentos e quantidades de calorias foram obtidas por pesquisa (https://www.chi.pt/tabela-de-calorias.htm) e (https://www.tabeladecalorias.net/)
Foi criado no Excel uma tabela para cada uma das 4 refeições diárias, com as respectivas quantidades de itens (em linhas) e com os 7 dias da semana (em coluna) isso para podermos validar o algoritmo.
Abaixo de cada tabela de cada refeição, foi criada uma fórmula com o retorno binário (0 para false ou 1 para true) conforme as restrições imposta para cada caso.

No PDI Pentaho foi filtrado as refeições café, lanche da tarde, almoço e janta, com o Intuito de ajustar melhor os filtros para cada condição, no café da manhã filtramos apenas produtos com flag igual a 1, no Almoço/Janta utilizamos um filtro retirando esses alimentos, lanche da tarde filtramos apenas frutas.

Ao final da Dieta verificamos o valor de caloria gerada , valido apenas entre 1800 a 2000 diaria.


### 3. Resultados

Os resultados obtidos foram ótimos, cada refeição seguindo as restrições imposta pelo problema, não ultrapassando o total por refeição de 2000 kcal diario, ou seja 100% das restrições e kcal alvo sendo atendidas.

### 4. Conclusões

Após a análise e testes ao longo do desenvolvimento, é fato que existe diversas possibilidades de desenvolvimento para teste deste tipo de problema, conforme o desenvolvimento da aplicação pude verificar que o problema alvo sendo o valor de 2000 kcal diária foi no que pude ter o melhor resultado, porém utilizando um calculo que podemos encontrar dentro de cada refeição um valor de 1800 entre 2000 mil kcal,sendo assim gerando uma refeição diária com itens distintos e que contém proteína ou carboidratos na mesma refeição, atendendo as restrições impostas pelo problema, tendo em vista o resultado, a dieta é para seguir os 7 dias da semana podendo se estender a mais tempo.
Entendo que para obter um certo resultado é recomendável manter a dieta por no mínimo 1 mês.

---

Matrícula: 202.190.281

Pontifícia Universidade Católica do Rio de Janeiro

Curso de Pós Graduação *Business Intelligence Master*
