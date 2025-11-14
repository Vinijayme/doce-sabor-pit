# doce-sabor-pit
Página do GitHub dedicada à entrega do Projeto Transdisciplinar II do curso de Engenharia de Software UNIFRAN EAD
🧁 Doce Sabor | Sistema de Vendas de Cupcakes Gourmet

Projeto de E-commerce de cupcakes gourmet, desenvolvido como solução prática para a disciplina de Projeto Interdisciplinar (PIT) do curso de Engenharia de Software. O sistema inclui vitrine de produtos, carrinho de compras funcional, autenticação de clientes e um painel de administrador para gerenciamento de produtos e pedidos.

📖 Índice

Visão Geral

Tecnologias Utilizadas

Recursos Implementados

Mapa de Afinidades

Arquitetura (MVC)

Como Executar Localmente

Autor

🚀 Visão Geral

O sistema está hospedado e funcional. Você pode acessá-lo clicando no link abaixo:

Link do Projeto: https://docesabor-f1c2b.web.app/ (Substitua por seu link do Firebase Hosting)

🛠️ Tecnologias Utilizadas

Este projeto foi construído utilizando uma arquitetura de Single Page Application (SPA) com as seguintes tecnologias:

Ferramenta

Descrição

HTML5

Estrutura e semântica do site.

TailwindCSS

Framework de estilização utility-first para a interface.

JavaScript (ES6+)

Linguagem principal para toda a lógica de front-end, simulação de rotas e manipulação do DOM.

Firebase (BaaS)

Plataforma de Backend-as-a-Service do Google, utilizada para:

    ↳ Firebase Hosting

Hospedagem estática do site com deploy contínuo.

    ↳ Cloud Firestore

Banco de dados NoSQL para persistência de usuários, produtos e pedidos.

    ↳ Firebase Storage

Armazenamento de arquivos (para upload de fotos dos produtos).

Lucide Icons

Biblioteca de ícones SVG.

✨ Recursos Implementados

[X] Catálogo de Produtos: Carregamento dinâmico dos produtos direto do banco de dados (Firestore).

[X] Carrinho de Compras: Lógica completa para adicionar, remover e alterar a quantidade de itens.

[X] Autenticação: Sistema simulado de Cadastro e Login de usuários (Clientes e Admin).

[X] Checkout: Formulário de endereço e simulação de métodos de pagamento.

[X] Histórico de Pedidos (Cliente): O cliente pode visualizar todos os pedidos que já fez e seus status.

[X] Painel de Administrador: Rota protegida (isAdmin: true) para gerenciamento da loja.

[X] Admin: CRUD de Produtos: O Admin pode Criar, Ler, Editar e Remover sabores (incluindo preço, foto, descrição).

[X] Admin: Ativação de Produtos: O Admin pode marcar um produto como "Indisponível" para escondê-lo da loja sem excluí-lo.

[X] Admin: Gestão de Pedidos: O Admin pode visualizar todos os pedidos recebidos e alterar o status (Preparando, A caminho, Finalizado).

🗺️ Mapa de Afinidades e Histórias de Usuário

O projeto foi guiado pelas seguintes histórias de usuário, agrupadas por afinidade:

1. Autenticação e Acesso

ID

História do usuário

1

Cadastro de cliente

2

Login do cliente

2. Navegação e Catálogo

ID

História do usuário

3

Visualizar catálogo

3. Carrinho e Compras

ID

História do usuário

4

Adicionar ao carrinho

5

Visualizar carrinho

6

Remover item do carrinho

7

Alterar quantidade no carrinho

4. Pedido e Pagamento

ID

História do usuário

8

Finalizar pedido

9

Escolher forma de pagamento

10

Acompanhar status do pedido

11

Ver pedidos

5. Administração de Itens

ID

História do usuário

12

Adicionar novo item

13

Editar item

14

Excluir item

15

Alterar quantidade em estoque (implementado como "Disponível/Indisponível")

📐 Arquitetura (MVC)

Este projeto de página única (SPA) usa uma arquitetura onde as responsabilidades do MVC são mapeadas da seguinte forma:

Model (Modelo):

Firebase Firestore: Banco de dados persistente para users, products e all_orders.

Objeto 'state' (JS): Estado volátil da aplicação (dados do carrinho, usuário logado).

View (Visão):

HTML Estático: Estrutura principal da página (<nav>, <main>, etc.).

Funções render...() (JS): Funções que geram o HTML dinâmico para cada tela (home, carrinho, admin).

Controller (Controlador):

Objeto 'window.app' (JS): Controlador principal que recebe eventos (onclick) da View.

Objeto 'authService' (JS): Controlador focado na lógica de autenticação.

Funções do Firebase (JS): Controladores que lidam com a comunicação com o banco de dados (ex: loadProductsFromFirestore, processPayment).
