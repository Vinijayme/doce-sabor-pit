# 🧁 Doce Sabor — Sistema de Vendas de Cupcakes Gourmet

**Projeto Integrador — Engenharia de Software II (PIT II)**

Este repositório documenta a entrega do projeto Doce Sabor, implementado com HTML5, JavaScript (ES6+) e Firebase (abordagem code-first/tradicional), seguindo o padrão arquitetural MVC conforme diretrizes do PIT II.

## 🔗 Link público do sistema
- URL: https://docesabor-f1c2b.web.app/

## 🧱 Arquitetura (MVC — mapeamento prático)
- Model: Coleções Cloud Firestore (users, products, all_orders) e o objeto state (JS) para dados voláteis.
- View: Funções render...() (JS) que geram HTML dinâmico e o index.html estático.
- Controller: O objeto global window.app (JS) que gerencia eventos e as funções do authService e SDK do Firebase.

## ✅ Funcionalidades implementadas (mapeadas às HUs)
- HU001/HU002 — Cadastro/Login de clientes (via authService simulado).
- HU003 — Visualizar catálogo (lido dinamicamente do Firestore).
- HU004/HU005/HU006/HU007 — Carrinho: adicionar, visualizar, alterar quantidades e remover itens.
- HU008/HU009 — Checkout: formulário de endereço e seleção de pagamento simulado.
- HU010/HU011 — Acompanhar status e ver histórico de pedidos (visão do cliente).
- HU012/HU013/HU014/HU015 — [Admin] — Gerenciamento de Produtos: CRUD (adicionar, editar, excluir, marcar como indisponível).

## 🧪 Testes (verificação/validação)
Os testes de fluxo (cliente e admin) e o laudo de qualidade foram documentados em arquivos separados. O fluxo de compra do cliente e o fluxo de gerenciamento do admin foram validados com sucesso.

## 🖼️ Screenshots
Verificar pasta SCREENSHOTS.

## 🛠️ Stack técnica (Code-First)
- Front-end: HTML5, TailwindCSS, JavaScript (ES6+)
- Back-end (BaaS): Google Firebase
- Serviços Firebase: Firebase Hosting, Cloud Firestore, Firebase Storage
- Banco de Dados: Cloud Firestore (NoSQL)

## 📚 Referência ao material do PIT II
O projeto optou pela abordagem Code-First (Tradicional) para demonstrar proficiência na construção de uma Single Page Application (SPA) do zero, integrando-a manualmente com um back-end de serviços (BaaS), que é uma arquitetura de mercado moderna.

## Autor:
Vinícius Jayme
