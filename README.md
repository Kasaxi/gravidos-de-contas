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

No topo do `<script>`, no fim do `index.html`, há um bloco `CONFIG`:

```js
const CONFIG = {
  checkoutUrl: 'https://pay.cakto.com.br/y6pagop_988893',  // checkout do Cakto (configurado)
  ga4Id: '',                     // ID do Google Analytics 4, ex.: 'G-XXXXXXXXXX'
  metaPixelId: ''                // ID do Meta Pixel, ex.: '1234567890123456'
};
```

- **`checkoutUrl`** — já aponta para o checkout do Cakto. Todos os botões de
  compra usam ele.
- **`ga4Id` / `metaPixelId`** — ainda em branco; preencha quando for medir e
  anunciar. Se preenchidos, o GA4 e/ou o Meta Pixel são carregados
  automaticamente e recebem todos os eventos do funil, com os eventos-chave
  mapeados para os padrões do Pixel (`Lead`, `ViewContent`, `InitiateCheckout`).

### 2. Páginas institucionais

Os links do rodapé já apontam para `/privacidade`, `/termos` e `/contato`,
servidas pelo Vercel (`vercel.json` com `cleanUrls`). São versões enxutas,
sem dados obrigatórios a preencher.

### 3. Elementos de venda a revisar

Alguns gatilhos **precisam refletir a realidade** — no `index.html`, procure
pelos comentários `CONFIRME`:

- **"de R$ 97"** — use um preço "cheio" que seja **verdadeiro**. Anunciar um
  valor que nunca foi praticado é propaganda enganosa.
- **"Oferta de lançamento"** — mantenha só se o preço realmente for subir depois.
- **Garantia de 7 dias** — honre a devolução. Em compras online isso também é
  direito do consumidor (CDC, art. 49).

Os depoimentos e o parcelamento (**12x de R$ 7,02**) já estão com valores reais.

## Arquivos

- **`index.html`** — a página do quiz e do funil (HTML, CSS e JS, sem dependências além da fonte).
- **`privacidade.html`**, **`termos.html`**, **`contato.html`** — páginas institucionais
  (usam a folha de estilo compartilhada `pagina.css`).
- **`pagina.css`** — estilo compartilhado das páginas institucionais.
- **`vercel.json`** — configura URLs limpas (`/privacidade`, `/termos`, `/contato`).
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
