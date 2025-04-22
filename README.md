# Capítulo 2 - Prática 1 - Dashboard Analítico de Vendas


![](cap02/pratica1.gif)


## *Objetivo*

**1. Qual o valor total vendido?**  
   Essa pergunta é respondida pelo elemento visual de cartão que conta com o somatório da coluna ***Total_Vendas***, o visual em questão está localizado no canto superior direito abaixo da versão do dashboard e tem o título de ***Total Vendas Global***.

**2. Quantas vendas foram realizadas por categoria de produto?**  
   Essa pergunta é respondida pelo elemento visual de gráfico de pizza que conta com a coluna de ***Categoria*** no campo ***legenda*** e com a ***contagem*** da coluna ***ID_Pedido*** no campo ***valores***, o visual em questão está localizado no ponto superior central e tem o título de ***Total Vendas por Categoria***.

**3. Quantas vendas foram realizadas por país considerando a prioridade de entrega?**
   Essa pergunta é respondida pelo elemento visual de gráfico de barras empilhadas que conta com o contagem da coluna ***ID_Pedido*** no ***eixo x***, com a coluna ***Pais*** no ***eixo y*** e a coluna ***Prioridade*** no campo ***legenda***, o visual em questão está localizado no canto inferior direito e tem o título de ***Total de Vendas por País e Prioridade***.

**4. Qual foi a média de desconto nas vendas por subcategoria de produto?**
    Essa pergunta é respondida pelo elemento visual de gráfico de barras clusterizado que conta com a coluna ***SubCategoria*** no ***eixo y*** e média da coluna ***Desconto*** no ***eixo x***, o visual em questão está localizado no canto superior esquerdo e tem o título de ***Média de Desconto por Subcategoria***. 

**5. Quais países tiveram maior média de valor de venda?**
    
   Essa pergunta é respondida pelo elemento visual de mapa e conta com a coluna ***Pais*** no campo ***localização*** e tem o tamanho da bolha definido pela média da coluna da coluna ***Total_Vendas***, o visual em questão está localizado no canto inferior esquerdo e tem o título de ***Média de Desconto por País***.

# Capítulo 3 - Prática 1 - Vendas, Custos, Margem de Lucro e KPI


![](cap03/pratica2.gif)


## *Objetivo*

**1. Qual foi o total de valor venda considerando cada modo de envio dos pedidos?**  
   
   Essa pergunta é respondida pelo elemento visual gráfico de cascata que conta com a coluna ***Pedido[ Modo Envio ]*** no campo categoria e a somatória da coluna ***Venda[ Valor Venda ]*** no eixo y, o visual em questão está localizado no canto inferior direito e tem o título de ***Total de Valor Venda por Modo Envio***.

**2. Quais mercados tiveram o maior custo médio de envio dos produtos vendidos?**  
   
   Essa pergunta é respondida pelo elemento visual gráfico treemap que conta com a coluna de ***Clientes[ Mercado ]*** no campo categoria e com a média da coluna ***Vendas[ Custo Envio ]*** no campo valores, o visual em questão está localizado no ponto superior direito e tem o título de ***Média de Custo Envio por Mercado***.

**3. A empresa tem como objetivo (meta) manter uma média de 350 para o valor de venda todos os meses. Mostre um indicador (KPI–Key Performance Indicator) com o valor médio de venda. A empresa ficou abaixo ou acima da meta no mês de Abril/2014?**
   
   Essa pergunta é respondida pelo elemento visualde indicador que conta com o médiada da coluna ***Venda[ Valor Venda ]*** no campo valor, também foi necessário adicionar os valores 0, 500 3 350 respectivamente para os campos Mín, Máx e Destino no Eixo do medidor.
   O visual em questão está localizado no lado superior esquerdo e tem o título de ***KPI - Média de Valor Venda***.

**4. Considere que o lucro é equivalente a: valor venda - custo envio. Qual categoria de produto apresentou maior lucro médio.**
   
   Essa pergunta é respondida pelo elemento visual de gráfico de rosca que conta com a coluna ***Produtos[ Categoria ]*** no no campo legenda e com média da coluna ***Vendas[ Lucro ]*** no campo valores, essa coluna ***Vendas[ Lucro ]*** foi criada neste dashboard com a seguinte expressão DAX: 
    
         Lucro = Vendas[Valor Venda] - Vendas[Custo Envio]

   
   O visual em questão está localizado no canto superior central e tem o título de ***Média de Lucro por Categoria***. 

**5. Qual foi o comportamento da margem de lucro ao longo do tempo? Considere amargem de lucro como o lucro dividido pelo valor venda.**
   
   Essa pergunta é respondida pelo elemento visual gráfico de linhas e conta com a coluna ***Pedidos[ Data Pedido]*** (ano e mês) no eixo x e a média da coluna ***Vendas[ Margem de Lucro ]*** no eixo y, essa coluna ***Vendas[ Lucro ]*** foi criada neste dashboard com a seguinte expressão DAX: 
    
         Margem de Lucro = DIVIDE(Vendas[Lucro], Vendas[Valor Venda], 0)
   

   O visual em questão está localizado no canto inferior esquerdo e tem o título de ***Média de Margem de Lucro por Ano e Mês***.
 
