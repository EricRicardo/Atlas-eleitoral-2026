# Atlas Eleitoral 2026 — fontes e critérios

Consulta: 26/10/2026. Arquivos disponíveis com geração em 25/10/2026.

- TSE, candidatos: https://dadosabertos.tse.jus.br/pt_BR/dataset/candidatos-2026
- TSE, resultados: https://dadosabertos.tse.jus.br/dataset/resultados-2026
- TSE, partidos registrados: https://www.tse.jus.br/partidos/partidos-registrados-no-tse/registrados-no-tse
- Fotos de urna: pacotes `foto_cand2026_UF_div.zip`, associados exclusivamente pelo SQ_CANDIDATO.
- Geografia: IBGE, malha municipal 2025. Geometrias reutilizadas do atlas Podemos, simplificadas a 300 metros em EPSG:5880 e exibidas em Web Mercator. 5.571 municípios eleitorais; duas áreas de massas d’água sem votação.

## Semântica

Os eleitos são os classificados como ELEITO, ELEITO POR QP ou ELEITO POR MÉDIA nos arquivos de candidatura, para cargos de deputado federal, estadual, distrital, senador, governador e vice-governador. Não são incluídos suplentes nem senadores de 2022. Candidaturas classificadas para o segundo turno ficam em pendências e não contam como eleitas. Os votos dos vices são associados aos respectivos titulares pelo mesmo cargo majoritário, UF e número da chapa.

As cores mostram os votos do partido selecionado (nominais válidos + legenda válida), sem somar os demais integrantes de federações. Percentual usa todos os votos válidos do mesmo cargo e recorte. As bases municipais individuais são agregadas das zonas e as cinco maiores constam da mini bio.

## Zonas

Somente 1.915 zonas possuem área identificável pela união de municípios integralmente associados a uma única zona na base. Não constituem uma malha oficial de zoneamento. As demais 725 ficam sem preenchimento, com referências numeradas. Todos os totais de todas as zonas permanecem acessíveis. Não há rateio ou interpolação de votos.

## Verificação

Conservação exata dos votos por município, zona, UF e cargo; comparação do total de partidos com o denominador oficial; reconciliação das quantidades de eleitos por cargo; associação de fotos por identificador. As classificações são uma fotografia dos arquivos consultados e não uma auditoria jurídica individual ou uma consolidação garantida do segundo turno.

## Execução

A aplicação é estática e não exige instalação: `dist/` contém HTML, CSS, JavaScript, fotos e dados compactados. As fontes CSV brutas não são publicadas nem guardadas neste repositório. Os scripts em `pipeline/` registram o processamento executado; seus caminhos de trabalho precisam ser ajustados para uma nova execução. A malha de entrada é a mesma do atlas anterior. TSE: licença CC BY; Leaflet: BSD-2-Clause.
