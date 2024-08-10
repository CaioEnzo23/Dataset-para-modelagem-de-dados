# Desafio: Prepare seu dataset para modelagem de dados
Este projeto foi criado com o intuito de aprimorar habilidades em Python utilizando um modelo de Dataset. 
O objetivo neste projeto é construir um código em Python que gera um output também csv, porém contendo apenas a identificação do cliente e métricas RFM.

Portanto separei este projeto em 10 partes : 

# Inspecão dos dados

Pesquisei os produtos que já existem hoje e seus diferenciais. Apresentei de forma clara os concorrentes diretos e indiretos, e destaquei seus diferenciais e pontos fortes.
Utilizei o describe para verificar a distribuição dos dados.

![image](https://github.com/user-attachments/assets/8ae806d3-2768-4bb8-a973-55324b94e679)

# Valores faltantes na identificação do cliente

Verifiquei os valores nulos com o "isna" e utilize a função "sum" para a somar a quantidade de nulos.
Também utilizei a função dropna para remover os nulos.

![image](https://github.com/user-attachments/assets/a9cdd537-d544-4ffd-bbc6-df6ca7c9ed0e)

# Preços unitários e quantidade de produtos iguais ou inferior a 0

Realizei um filtro para verificar se existem dados nulos ou menor que zero na coluna de preços.
Filtrei o dataset para conter preços acima de zero.
Realizei um filtro para verificar se existem dados nulos ou menor que zero na coluna de quantidade.
Filtrei o dataset apenas para conter quantidade acima de zero.

![image](https://github.com/user-attachments/assets/374df2fc-62be-49de-b167-d1872bfb9e51)

![image](https://github.com/user-attachments/assets/e9946ecb-7292-40ff-a521-0ef50ab66d3f)

# Verificação de linhas duplicadas

Verifiquei se tem linhas duplicadas com a função "duplicated".
Dropei as linhas duplicadas

Pois não faz sentido uma mesma compra para o mesmo cliente no mesmo horário, com mesmos valores etc.

![image](https://github.com/user-attachments/assets/95ec2c82-6e3f-4dba-94a7-052d6b344793)

# Tipos de dados da coluna

Corriji os tipos de dados do "CustomerID" e "InvoiceDate"

![image](https://github.com/user-attachments/assets/0642df34-20e3-42bd-9e84-0f246fb5cedf)

# Tratando os outliers

Visualizei os outliers e removi os outliers extremos em que a quantidade do item na compra é superior a 10.000, e o preço unitário é maior que 5.000.

![image](https://github.com/user-attachments/assets/b03f17a2-d45f-4508-98ac-73f23b8be604)

# Criação de uma coluna adicional

Criei uma coluna adicional com o preço total da compra. Utilizando as colunas "Quantity" e "UnitPrice".

![image](https://github.com/user-attachments/assets/65c52fb0-48d8-40e6-a630-639f91c58461)

# Última data

Calculei a data da última compra no dataset como um todo, utilizando a função "max()" .
Pois utilizei este valor como data de comparação para cálculo da recência.

![image](https://github.com/user-attachments/assets/8df8aeec-fa36-4fc5-8b02-cb8269baa3d1)

# Plotando gráficos

Lista de Gráficos feitos:
- Top 10 países com maior valor em vendas
- Top 10 produtos mais vendidos
- Valor de venda total por mês
- Valor de venda total por mês e por país (considere apenas os top 10)

![image](https://github.com/user-attachments/assets/8fb47c86-b67c-489a-99ee-833bbbf2426a)

![image](https://github.com/user-attachments/assets/bd29a67f-17fe-4295-8366-3e9ebeca32ed)

# Cálculo do RFM

Agrupei os dados por cliente e pedido/compra (InvoiceNo) e obtendo a data e o preço total do pedido.
Com isso, agrupei novamente apenas por cliente e calculei o RFM, onde:

- R é a recência, diferença em dias da última compra do cliente e da
última compra disponível no conjunto de dados.
- F é a frequência, ou seja, a quantidade de compras feitas pelo
cliente;
- M é o ticket médio, ou seja, a média das compras feitas pelo cliente.

![image](https://github.com/user-attachments/assets/71f42d9c-b3b4-4fbc-94fd-e98e01f36b39)

![image](https://github.com/user-attachments/assets/0d1d0750-5366-4e77-a588-647a163c0641)
