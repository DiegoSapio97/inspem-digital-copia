# INSPEM Digital

Site da clínica **INSPEM** — psicoterapia em Terapia Cognitivo-Comportamental no Bom Fim, Porto Alegre. Construído em [Astro](https://astro.build).

## O que tem no site

Landing page única com:

- Hero e chamada para triagem pelo WhatsApp
- Para quem é a clínica, como funciona e como começar
- Investimento das sessões (R$ 95)
- Equipe e supervisoras
- Reconhecimento (nota no Google)
- Localização no Edifício Baltimore, em frente ao Parque da Redenção
- Galeria: fachada empilhada e salas em carrossel horizontal
- FAQ (itens começam fechados) e rodapé com dados legais

## Como rodar

Requer Node.js 22.12 ou superior.

```sh
npm install
npm run dev
```

O servidor sobe em `http://localhost:4329`.

| Comando | O que faz |
| --- | --- |
| `npm run dev` | Servidor de desenvolvimento |
| `npm run build` | Build de produção em `./dist/` |
| `npm run preview` | Preview do build local |

`npm install` também instala a fonte Newsreader (`@fontsource/newsreader`).

## Fotos

As fotos já estão em `public/assets/` com os nomes atuais do repositório. Catálogo em `src/data/photos.ts`.

A fachada é a única foto empilhada. As salas deslizam no carrossel: atendimento, espera, entrada, sala da equipe.

O wordmark novo do header não entra pelo MCP (WebP corrompe). O site usa o logo que já está no repositório. Para trocar, faça upload pelo GitHub em `public/assets/` e atualize o `src` em `src/data/photos.ts`.

## Estrutura

```text
src/
├── components/   seções da landing (Hero, Equipe, FAQ…)
├── data/         textos, contato, endereço, fotos e supervisoras
├── layouts/      layout HTML base
├── pages/        index.astro
└── styles/       CSS global, mobile, fontes e refinamentos
public/assets/    fotos da clínica e da equipe
```
