# E-commerceDIO
# Projeto E-commerce

Este projeto tem como objetivo modelar um sistema de e-commerce, abrangendo os principais processos de gestão de pedidos, produtos, clientes, transporte, e estoque. Abaixo estão detalhadas as principais entidades do banco de dados, suas relações e o propósito de cada componente.

## Estrutura do Banco de Dados

### Entidades Principais

#### Cliente
- **idCliente**: Identificador único do cliente.
- **nome**: Nome completo do cliente.
- **tipo de cliente/identificação**: Tipo ou documento de identificação (CPF/CNPJ).
- **email**: Endereço de e-mail do cliente.
- **telefone**: Telefone para contato.
- **Plataforma E-commerce_idPlataforma E-commerce**: Relaciona o cliente à plataforma de e-commerce utilizada.

#### Pedido
- **idPedido**: Identificador único do pedido.
- **status da entrega**: Status atual da entrega do pedido.
- **descrição**: Detalhes adicionais sobre o pedido.
- **valor total pedido**: Valor total do pedido em reais.
- **Plataforma E-commerce_idPlataforma E-commerce**: Referência à plataforma de e-commerce em que o pedido foi realizado.
- **quantidade de produtos**: Número total de produtos no pedido.

#### Produto
- **idProduto**: Identificador único do produto.
- **descrição**: Detalhes sobre o produto.
- **categoria**: Categoria do produto.
- **valor unitário**: Preço unitário do produto.

#### Estoque
- **idEstoque**: Identificador único do estoque.
- **local**: Localização do estoque.

#### Transportadora
- **idTransportadora**: Identificador único da transportadora.
- **nome**: Nome da transportadora.
- **endereço**: Endereço da transportadora.
- **email**: Endereço de e-mail da transportadora.

#### Fornecedor
- **idFornecedor**: Identificador único do fornecedor.
- **razão social**: Razão social do fornecedor.
- **CNPJ**: Cadastro Nacional da Pessoa Jurídica do fornecedor.

#### Terceiro - Vendedor
- **idTerceiro - Vendedor**: Identificador único do vendedor.
- **razão social**: Nome da razão social do vendedor.
- **CNPJ**: CNPJ do vendedor terceirizado.

### Relacionamentos

1. **Relação Produto/Pedido**
   - Relaciona os produtos incluídos em cada pedido.
   - Campos adicionais: quantidade de produtos.

2. **Relação Plataforma/Transportadora**
   - Conecta a plataforma de e-commerce às transportadoras.
   - Campos adicionais: status da entrega, código de rastreio, e valor do frete.

3. **Relação Plataforma/Sistema Bancário**
   - Associa a plataforma de e-commerce aos sistemas bancários utilizados para pagamento.
   - Campos adicionais: forma de pagamento.

4. **Disponibilidade de Produto**
   - Relaciona os produtos ao estoque.
   - Campos adicionais: quantidade disponível.

5. **Abastecimento Estoque**
   - Conecta os fornecedores ao estoque, indicando quais fornecedores abastecem quais estoques.

6. **Relação de Produtos Vendidos por Terceiros**
   - Conecta os produtos vendidos por terceiros à respectiva entidade de vendedor terceirizado.
   - Campos adicionais: relação dos produtos vendidos.

### Plataforma E-commerce
- **idPlataforma E-commerce**: Identificador único da plataforma.
- **nome**: Nome da plataforma de e-commerce.
- **endereço**: Endereço da sede da plataforma.
- **email**: Endereço de e-mail para contato.

### Sistema Bancário
- **idSistemaBancario**: Identificador único do sistema bancário.
- **razão social**: Nome oficial do sistema bancário.
- **endereço**: Endereço do sistema bancário.
- **email**: E-mail de contato.

## Finalidade do Projeto

Este banco de dados foi projetado para gerenciar de forma eficiente as operações de um sistema de e-commerce, permitindo:
- Controle de clientes, pedidos, e produtos.
- Gestão de transporte e rastreamento de entregas.
- Integração com sistemas bancários para processamento de pagamentos.
- Administração de estoque e reposição de produtos.
- Inclusão de produtos vendidos por terceiros no marketplace.

## Possíveis Extensões
- Implementação de relatórios detalhados para monitoramento de vendas e estoque.
- Integração com módulos de BI para análise de dados.
- Automatização de comunicação com transportadoras e fornecedores.
- Desenvolvimento de APIs para integração com plataformas externas.

