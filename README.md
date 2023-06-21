
APRESENTAÇÃO E STACKS UTILIZADAS:
O RevendaPlus é um projeto desenvolvido com ReactJS (frontend) + Asp .NET 6 (backend). 
A aplicação trabalha com Entity Framework para fazer as operações de procedures e functions no banco de dados (SQL Server). 
Para o frontend foi utilizado Styled Components, Bootstrap e Material UI para trabalhar a responsividade, estilização dos botões e componentização das páginas e elementos da aplicação.

OBJETIVO:
O objetivo é buscar produtos da API do Mercado Livre e disponibilizar para o usuário (revendedor) o cadastro desses produtos no banco do sistema da RevendePlus.

Ele conseguirá ter acesso aos produtos, sku, preço de compra, foto, e em cima destes dados precificar com base na taxa de lucro que deseja ter nas vendas, além de inserir a quantidade comprada.
Dessa forma ele conseguirá ter um controle das compras de produtos. Além disso, uma outra tabela estoque pra inserir os produtos que foram comprados e suas respectivas quantidades.
O sistema conta ainda com um formulário e listagem de vendas. A proposta é desenvolver um sistema que não só cadastra os produtos e estoque, como também controla entrada e saída de produtos, lucratividade mensal, etc.

Endpoints:

ESTOQUE:
Dados: 
- id_produto: foreign key da tabela Produto.
- quant_estoque

GET
/api/Estoque

POST
/api/Estoque

GET
/api/Estoque/{id}

PUT
/api/Estoque/id

DELETE
/api/Estoque/id

/****************************************************************************************/

PRODUTO:
Dados: 
- quantidade
- taxa_lucro
- preco_unit_compra
- preco_venda
- preco_total_compra
- data_hora
- nome_produto
- categoria
- sku

GET
/api/Produto

POST
/api/Produto

GET
/api/Produto/{id}

PUT
/api/Produto/id

DELETE
/api/Produto/id

/****************************************************************************************/

VENDA:
Dados: 
- id_produto (foreign key da tabela Estoque)
- quant_vendida
- data_hora
- descricao

GET
/api/Venda

POST
/api/Venda

GET
/api/Venda/{id}

DELETE
/api/Venda/id
