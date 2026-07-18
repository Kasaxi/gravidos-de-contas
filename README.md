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

### 1. Link do checkout e rastreamento

No topo do `<script>`, no fim do `index.html`, há um bloco `CONFIG`. Preencha:

```js
const CONFIG = {
  checkoutUrl: 'CHECKOUT_URL',   // link do checkout de pagamento (obrigatório)
  ga4Id: '',                     // ID do Google Analytics 4, ex.: 'G-XXXXXXXXXX'
  metaPixelId: ''                // ID do Meta Pixel, ex.: '1234567890123456'
};
```

- **`checkoutUrl`** — obrigatório. Todos os botões de compra usam ele. Enquanto
  continuar `'CHECKOUT_URL'`, os botões ficam inativos e avisam no console (assim
  ninguém cai numa página quebrada durante os testes).
- **`ga4Id` / `metaPixelId`** — opcionais. Se preenchidos, o GA4 e/ou o Meta Pixel
  são carregados automaticamente e recebem todos os eventos do funil. Se deixados
  em branco, nenhum rastreamento externo é carregado. Os eventos-chave já são
  mapeados para os eventos padrão do Pixel (`Lead`, `ViewContent`,
  `InitiateCheckout`), úteis para otimizar campanhas.

### 2. Links do rodapé

Trocar os placeholders no rodapé do `index.html`:

| Placeholder | O que é |
|---|---|
| `PRIVACY_URL` | Link da política de privacidade |
| `TERMS_URL` | Link dos termos de uso |
| `CONTACT_URL` | Link/página de contato |

### 3. Elementos de venda a revisar

A página usa gatilhos de venda que **precisam refletir a realidade** — no
`index.html`, procure pelos comentários `CONFIRME` e pela tag `Exemplo`:

- **Depoimentos** — a seção está pronta com espaços `[...]` e a etiqueta
  `Exemplo`. Preencha com depoimentos **reais** (com autorização de quem
  escreveu) e apague as etiquetas. Depoimento inventado é propaganda enganosa
  (CDC/CONAR) e pode derrubar a página e os anúncios. Prints reais de conversas
  convertem ainda mais.
- **"de R$ 97"** — use um preço "cheio" que seja **verdadeiro**. Anunciar um
  valor que nunca foi praticado é propaganda enganosa.
- **"Oferta de lançamento"** — mantenha só se o preço realmente for subir depois.
- **"12x de R$ 6,79"** — ajuste para o parcelamento real do seu checkout.
- **Garantia de 7 dias** — honre a devolução. Em compras online isso também é
  direito do consumidor (CDC, art. 49).

## Arquivos

- **`index.html`** — a página inteira (HTML, CSS e JS, sem dependências além da fonte).
- **`favicon.svg`** — ícone da aba do navegador.
- **`og-image.png`** — imagem de pré-visualização ao compartilhar o link (WhatsApp,
  Instagram, anúncios). Já referenciada no `<head>`. Ao publicar num domínio
  próprio, o ideal é apontar as tags `og:image`/`twitter:image` para a **URL
  absoluta** da imagem (ex.: `https://seusite.com/og-image.png`) — alguns
  aplicativos exigem o endereço completo.

## Observações

- Os dados de pesquisa citados na página (endividamento das famílias e regras do
  salário-maternidade) vêm de fontes oficiais, com links para a Agência Senado.
  Índices e regras mudam com o tempo — reveja periodicamente.
- A página é acessível (contraste WCAG AA) e funciona bem no celular.
