# 📃 Requisitos do Sistema

## ✅ Requisitos Funcionais (RF)

## 1. Módulo de Gestão de Contas de Usuário

### 1.1. Cadastro

- **RF-001:** O sistema deve permitir que um novo usuário se cadastre utilizando nome completo, CPF/CNPJ, e-mail e senha.
- **RF-002:** O sistema deve validar se o e-mail e o CPF/CNPJ informados já existem na base de dados para garantir a unicidade.
- **RF-003:** O sistema deve enviar um e-mail de confirmação para o endereço cadastrado para verificar a sua autenticidade.
- **RF-004:** O sistema deve permitir que um usuário (Cliente) inicie o processo de "Tornar-se Vendedor" a partir do seu painel de conta.
- **RF-005:** O formulário para "Tornar-se Vendedor" deve solicitar os dados adicionais obrigatórios (Nome da Loja, Dados Bancários, Endereço Comercial).
- **RF-006:** O sistema deve submeter os cadastros de novos vendedores para aprovação do Administrador.

### 1.2. Autenticação

- **RF-007:** O sistema deve permitir que o usuário faça login usando seu e-mail e senha.
- **RF-008:** O sistema deve fornecer uma funcionalidade de "Esqueci minha senha" que envie um link de redefinição para o e-mail do usuário.

### 1.3. Gerenciamento de Perfil

- **RF-009:** O sistema deve permitir que o Cliente edite suas informações pessoais (nome, telefone).
- **RF-010:** O sistema deve permitir que o Cliente adicione, edite e remova múltiplos endereços de entrega.
- **RF-011:** O sistema deve permitir que o Vendedor acesse um "Painel do Vendedor" para gerenciar suas vendas e produtos.
- **RF-012:** O sistema deve permitir que o Vendedor edite as informações da sua loja (nome da loja, descrição, etc.).

## 2. Módulo de Catálogo e Produtos

### 2.1. Gestão de Produtos (Vendedor)

- **RF-013:** O sistema deve permitir que o Vendedor cadastre um novo produto com título, descrição, categoria, preço, quantidade em estoque, peso e dimensões.
- **RF-014:** O sistema deve permitir que o Vendedor faça upload de múltiplas imagens para cada produto.
- **RF-015:** O sistema deve permitir que o Vendedor edite todas as informações de um produto já cadastrado.
- **RF-016:** O sistema deve permitir que o Vendedor visualize uma lista com todos os seus produtos cadastrados, incluindo status (ativo, pendente, indisponível).
- **RF-017:** O sistema deve atualizar automaticamente o status de um produto para "Indisponível" quando seu estoque chegar a zero.

### 2.2. Visualização de Produtos (Cliente)

- **RF-018:** O sistema deve exibir as páginas de produtos com todas as suas informações: imagens, título, descrição, preço, nome do vendedor e avaliações.
- **RF-019:** O sistema deve exibir o valor do frete calculado na página do produto, com base no CEP inserido pelo cliente.
- **RF-020:** O sistema deve exibir produtos relacionados ou da mesma categoria na página de um produto.

## 3. Módulo de Busca e Navegação

- **RF-021:** O sistema deve fornecer uma barra de busca que permita ao cliente pesquisar produtos por palavras-chave.
- **RF-022:** O sistema deve permitir a navegação por categorias e subcategorias de produtos.
- **RF-023:** A página de resultados de busca deve permitir a aplicação de filtros (faixa de preço, avaliação do vendedor, marca, etc.).

## 4. Módulo de Processo de Compra (Checkout)

- **RF-024:** O sistema deve permitir que o cliente adicione e remova produtos de um carrinho de compras.
- **RF-025:** O carrinho de compras deve exibir todos os produtos, quantidades, preços unitários e subtotais, agrupados por vendedor.
- **RF-026:** O sistema deve calcular os custos de frete separadamente para cada vendedor dentro do mesmo carrinho.
- **RF-027:** O sistema deve apresentar um resumo do pedido (produtos, endereço de entrega, valor total com frete) antes da confirmação do pagamento.
- **RF-028:** O sistema deve permitir que o cliente selecione o método de pagamento (Cartão de Crédito, Pix, Boleto).
- **RF-029:** O sistema deve gerar um pedido único para o cliente, mas internamente criar sub-pedidos para cada vendedor envolvido na compra.

## 5. Módulo de Gestão de Pedidos

### 5.1. Visão do Cliente

- **RF-030:** O sistema deve permitir que o cliente visualize seu histórico de compras.
- **RF-031:** Para cada compra, o sistema deve exibir o status atualizado do pedido (Pagamento Aprovado, Enviado, Entregue, etc.).
- **RF-032:** O sistema deve exibir o código de rastreio quando o pedido for despachado pelo vendedor.
- **RF-033:** O sistema deve permitir que o cliente inicie um processo de cancelamento ou devolução a partir do seu histórico de compras, respeitando as regras de negócio.

### 5.2. Visão do Vendedor

- **RF-034:** O sistema deve notificar o vendedor sobre novos pedidos recebidos.
- **RF-035:** O painel do vendedor deve exibir uma lista de pedidos com seus respectivos status.
- **RF-036:** O sistema deve permitir que o vendedor atualize o status de um pedido (ex: de "Pagamento Aprovado" para "Enviado").
- **RF-037:** O sistema deve exigir que o vendedor insira um código de rastreio válido para alterar o status para "Enviado".

## 6. Módulo de Avaliações (Reviews)

- **RF-038:** O sistema deve permitir que apenas clientes que compraram um determinado produto possam avaliá-lo.
- **RF-039:** A funcionalidade de avaliação deve permitir a atribuição de uma nota (1 a 5 estrelas) e um comentário em texto.
- **RF-040:** O sistema deve calcular e exibir a média de avaliações na página do produto e na página do vendedor.

## 7. Módulo Administrativo

- **RF-041:** O painel administrativo deve permitir a visualização e gestão de todos os usuários (Clientes e Vendedores).
- **RF-042:** O sistema deve permitir que o Administrador aprove ou rejeite novos cadastros de vendedores.
- **RF-043:** O sistema deve permitir que o Administrador modere e remova anúncios de produtos que violem as políticas da plataforma.
- **RF-044:** O sistema deve permitir que o Administrador visualize todos os pedidos da plataforma.
- **RF-045:** O sistema deve fornecer uma ferramenta para o Administrador mediar disputas abertas entre clientes e vendedores.
- **RF-046:** O painel administrativo deve exibir relatórios financeiros básicos (total de vendas, comissão arrecadada, etc.).
