# Hemiciclos — Atlas Legislativo

Aplicação estática para GitHub Pages em `/hemiciclos/`. Abra o endereço publicado; não exige build nem instalação. `app.js`, `style.css` e `data.json` usam caminhos relativos, preservando a publicação na raiz do Atlas.

A base contém 1.653 representantes: 513 federais, 81 senadores, 1.035 estaduais e 24 distritais. A composição é projetada para 2027, com data de referência de 29/10/2026; não é um cadastro de exercício atualizado automaticamente. Leia também `../DATA_SOURCES.md`.

Cada cadeira mantém identificador, nome, partido, UF, cargo e situação. Cores partidárias são constantes entre Casas. Agrupamento por tamanho da bancada e ordem alfabética, sem interpretação ideológica. O Congresso é exibido em duas Casas, sem somar quóruns.

Maioria absoluta: `floor(N/2)+1`; 3/5: `ceil(3*N/5)`; 2/3: `ceil(2*N/3)`. Maioria simples na simulação binária: `floor((presentes-abstenções)/2)+1`, com presença mínima de maioria absoluta. As regras estaduais são referências aritméticas, sujeitas ao regimento e à matéria. O simulador mede potencial de coalizão, não intenção de voto.

Validações: 30 vistas; um ponto por registro; quóruns de referência de 24, 81, 94 e 513 cadeiras; ausência de sobreposições geométricas; seleção de coalizão e identificação individual. Exportação CSV inclui todos os representantes da Casa e a marcação da coalizão. Busca não altera composição ou denominadores.

## Cenários de bancadas

A seleção agora usa IDs individuais. Abra uma legenda para incluir ou retirar pessoas, use o botão da legenda para selecionar todos na vista atual ou ative o modo de edição pelos pontos. O detalhe de cada parlamentar também permite incluí-lo ou retirá-lo da bancada em edição. Os grupos Governo, Oposição, Ocasião, Agro e Evangélica começam vazios; são rótulos de simulação, sem atribuição factual de participação.

Crie, renomeie ou exclua bancadas políticas e temáticas. Elas são independentes e podem se sobrepor; o cálculo de união dos grupos marcados elimina IDs repetidos. A edição vale para o grupo ativo; esvaziar ou selecionar uma legenda afeta apenas a Casa/vista atual. Mudar de Casa preserva os integrantes já escolhidos.

Cenários são salvos no localStorage do navegador (`atlas-hemiciclos-scenarios-v2`) e podem ser baixados/importados em JSON. O arquivo guarda grupos, integrantes, escala editorial e federações simuladas; não transmite informações a um servidor. CSV inclui os grupos simulados de cada parlamentar.

A ordenação esquerda–direita é uma convenção editorial inicial entre −5 e +5, inteiramente editável e sem pretensão de representar estimativas empíricas ou a posição individual dos parlamentares. Sem partido é colocado no centro por convenção. O modo por tamanho da bancada continua disponível.

Federações registradas consultadas em 29/10/2026: União Progressista (UNIÃO/PP), Renovação Solidária (PRD/Solidariedade), Brasil da Esperança (PT/PCdoB/PV), PSDB Cidadania e PSOL REDE. Fonte: https://www.tse.jus.br/partidos/federacoes-registradas-no-tse . Federações hipotéticas exigem nome e pelo menos dois partidos; agrupam cadeiras existentes e não recalculam resultados eleitorais nem registram associações jurídicas.

Validação adicional: dissidência individual sem alteração de filiação; grupos independentes e sobrepostos; união sem duplicação; adição/retirada por federação; restauração/exportação de cenários; ordenação; todas as 30 vistas e contagem separada no Congresso.
