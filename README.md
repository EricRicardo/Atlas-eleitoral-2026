# Atlas Eleitoral 2026 — Partidos do Brasil

Uma análise de distribuição dos principais cargos eletivos brasileiros com base no último pleito eleitoral brasileiro. No futuro adicionarei a esse mapa a inclusão de dados de eleições municipais atualizadas.

Site estático com seleção de partido, eleitos por UF e cargo, fotos oficiais, votação total e camadas de votação por município e zona eleitoral.

## Publicação no GitHub Pages

1. Use o repositório público `EricRicardo/Atlas-eleitoral-2026`.
2. Coloque estes arquivos na raiz do repositório, preservando a pasta `data/`.
3. Em **Settings → Pages → Build and deployment**, escolha **Deploy from a branch**, branch **main**, pasta **/(root)**, e salve.
4. Aguarde a implantação. O endereço esperado é `https://ericricardo.github.io/Atlas-eleitoral-2026/` (ainda não publicado por este pacote).

Não há dependências de instalação nem etapa de build. A página carrega somente os dados do partido selecionado. Todos os caminhos de arquivos são relativos e funcionam no subdiretório do GitHub Pages. As fotos estão incorporadas nos arquivos de dados de cada partido. Não altere ou descompacte manualmente os arquivos `.bin`.

## Dados e limites

30 partidos; 1.668 eleitos classificados nos arquivos do TSE gerados em 25/10/2026, consultados em 26/10/2026. Candidaturas majoritárias ainda pendentes nessa base ficam separadas dos eleitos. Somente 1.915 das 2.640 zonas possuem áreas identificáveis pelo agrupamento municipal; as outras 725 têm referências numeradas e dados consultáveis. Consulte `DATA_SOURCES.md` e **Método e fontes** no site.

Os dados eleitorais e fotos são públicos, do TSE; limites municipais são do IBGE. O site é estático e não usa APIs de inteligência artificial durante a consulta.
