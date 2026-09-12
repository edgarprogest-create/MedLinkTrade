# Site MedLink

Site estático. Não precisa de build nem de servidor — são ficheiros HTML que o Cloudflare serve como estão.

## Páginas

| Ficheiro | Página |
| --- | --- |
| `index.html` | MedLink Trade (institucional, serviços, processo) |
| `casas-modulares.html` | MedLink Houses (catálogo navegável de casas) |
| `empilhadores.html` | MedLink Forklifts (catálogo navegável de empilhadores) |
| `catalogo-casas.html` | Grelha dos 11 modelos de casa |
| `catalogo-empilhadores.html` | Grelha dos 10 modelos de empilhador |
| `fichas-casas.html` | Fichas técnicas das casas |
| `fichas-empilhadores.html` | Fichas técnicas dos empilhadores |

Pastas de apoio: `assets/` (fotos de empilhadores e logótipos das transportadoras), `v3/` (fichas da nova coleção de casas), `houses/` (fotos das casas), `_ds/` (folha de estilos dos catálogos), `support.js` (runtime das páginas).

## Colocar no ar (GitHub + Cloudflare Pages)

1. **GitHub** — criar um repositório novo (ex. `medlink-site`) e carregar o conteúdo desta pasta na raiz do repositório (o `index.html` tem de ficar na raiz, não dentro de `site/`).
2. **Cloudflare** — em *Workers & Pages* → *Create* → *Pages* → *Connect to Git*, escolher o repositório.
3. Nas opções de build:
   - Framework preset: **None**
   - Build command: deixar vazio
   - Build output directory: `/`
4. *Save and Deploy*. Fica online num endereço `xxx.pages.dev`.
5. **Domínio** — no projeto do Pages, *Custom domains* → *Set up a domain* → escrever o domínio. Se o domínio já estiver na Cloudflare, os registos são criados automaticamente; se não, transferir os nameservers para a Cloudflare primeiro.

Cada alteração enviada para o GitHub publica automaticamente.
