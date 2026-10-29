# Hemiciclos — Atlas Legislativo

Aplicação estática para GitHub Pages em `/hemiciclos/`. Abra o endereço publicado; não exige build nem instalação. `app.js`, `style.css` e `data.json` usam caminhos relativos, preservando a publicação na raiz do Atlas.

A base contém 1.653 representantes: 513 federais, 81 senadores, 1.035 estaduais e 24 distritais. A composição é projetada para 2027, com data de referência de 29/10/2026; não é um cadastro de exercício atualizado automaticamente. Leia também `../DATA_SOURCES.md`.

Cada cadeira mantém identificador, nome, partido, UF, cargo e situação. Cores partidárias são constantes entre Casas. Agrupamento por tamanho da bancada e ordem alfabética, sem interpretação ideológica. O Congresso é exibido em duas Casas, sem somar quóruns.

Maioria absoluta: `floor(N/2)+1`; 3/5: `ceil(3*N/5)`; 2/3: `ceil(2*N/3)`. Maioria simples na simulação binária: `floor((presentes-abstenções)/2)+1`, com presença mínima de maioria absoluta. As regras estaduais são referências aritméticas, sujeitas ao regimento e à matéria. O simulador mede potencial de coalizão, não intenção de voto.

Validações: 30 vistas; um ponto por registro; quóruns de referência de 24, 81, 94 e 513 cadeiras; ausência de sobreposições geométricas; seleção de coalizão e identificação individual. Exportação CSV inclui todos os representantes da Casa e a marcação da coalizão. Busca não altera composição ou denominadores.
