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

## Atualização de 29/10/2026

`data/continuity.json` complementa os arquivos compactados sem alterar votos para deputados. Acrescenta os 12 integrantes das chapas vencedoras do segundo turno, presidente e vice-presidente e 27 mandatos de 2022, totalizando 81 cadeiras do Senado (três por UF). As pendências de segundo turno da base original deixam de ser exibidas.

Fontes consultadas:
- Agência Senado, resultados estaduais e vices: https://www12.senado.leg.br/noticias/materias/2026/10/25/definidos-governadores-em-5-estados-e-no-df-eleito-no-am-omar-deixa-senado
- Agência Senado, composição e substituições: https://www12.senado.leg.br/noticias/materias/2026/10/25/fim-da-eleicao-define-composicao-do-senado-em-2027-com-13-partidos
- Agência Senado, 27 mandatos em continuidade: https://www12.senado.leg.br/noticias/materias/2026/09/10/eleicoes-2026-quem-fica-quem-sai-e-quem-concorre-ao-senado
- TSE, resultado presidencial: https://www.tse.jus.br/comunicacao/noticias/2026/Outubro/presidente-do-tse-anuncia-reeleicao-de-lula-e-faz-balanco-do-2o-turno-das-eleicoes-2026
- TRE-SP, identificação do vice: https://www.tre-sp.jus.br/comunicacao/noticias/2026/Outubro/eleicoes-2026-lula-e-reeleito-presidente-da-republica-confira-resultado-do-2o-turno-em-sp
- Votos estaduais absolutos (exceto TO): https://mapadaseleicoes.com.br/2o-turno/ . Para TO usa-se apenas o percentual de 64,53% da Agência Senado, diante de divergência entre fontes.

A composição é uma projeção para 2027. Cheila Moreira, Alex Diniz e Luís Felipe Cunha têm assunção prevista após a saída dos titulares; não são apresentados como já em exercício em outubro de 2026. Luís Felipe Cunha é registrado no PL conforme a notícia mais recente da Agência Senado. Romário aparece em opção Sem partido. Mandatos de 2022 terminam em 31/01/2031. Retratos e bases municipais não disponíveis para os novos registros são omitidos, sem inventar votos ou coordenadas eleitorais. Presidência usa âncora institucional em Brasília e permanece visível ao filtrar UF.

Validação: sintaxe JavaScript; IDs únicos; 27 governadores e 27 vices; 81 senadores, três por UF. Sem auditoria judicial individual; a situação de candidaturas sub judice e novas filiações pode alterar a projeção.

## Retratos oficiais — 29/10/2026

Foram incorporadas fotos para os 41 representantes da atualização: 24 retratos do Senado Federal, 14 candidaturas do TSE de 2026 e três suplentes do TSE de 2022. Correspondência exata por código parlamentar ou SQ_CANDIDATO, conferida com os arquivos de candidatura. As imagens são armazenadas no próprio JSON, em JPEG reduzido, sem depender de servidores externos para carregar. Cada cartão identifica e vincula a fonte da foto. Verificação: decodificação dos 41 JPEGs e inspeção visual conjunta; testes de carregamento e cartões de seis opções partidárias.
