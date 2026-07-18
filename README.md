# Grávidos de Contas — Quiz de vendas

Página de quiz interativo para venda do ebook **Grávidos de Contas — O guia
financeiro para a chegada do primeiro filho sem sufoco** (R$ 67,90).

É uma página única, sem etapa de build. É só abrir o arquivo
[`index.html`](index.html) no navegador.

## Como editar

- **Pelo navegador, de qualquer PC:** abra o `index.html` aqui no GitHub e
  clique no lápis ✏️ (canto superior direito) para editar. Ao salvar
  (**Commit changes**), a página no ar atualiza sozinha em ~1 minuto.
- **No computador:** edite o `index.html` em qualquer editor de texto ou código.

## Publicação (link ao vivo)

A página é publicada gratuitamente pelo **GitHub Pages**.
O endereço fica em **Settings → Pages**.

## ⚠️ Antes de começar a vender

Trocar os placeholders dentro do `index.html`:

| Placeholder | O que é | Onde está |
|---|---|---|
| `CHECKOUT_URL` | Link do checkout de pagamento | Uma constante no topo do `<script>` — todos os botões de compra usam ela |
| `PRIVACY_URL` | Link da política de privacidade | Rodapé |
| `TERMS_URL` | Link dos termos de uso | Rodapé |
| `CONTACT_URL` | Link/página de contato | Rodapé |

## Observações

- Os dados de pesquisa citados na página (endividamento das famílias e regras do
  salário-maternidade) vêm de fontes oficiais, com links para a Agência Senado.
  Índices e regras mudam com o tempo — reveja periodicamente.
- A página é acessível (contraste WCAG AA) e funciona bem no celular.
