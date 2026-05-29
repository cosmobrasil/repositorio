---
name: analise-pdfs-taxonomia-ontologia
description: Use when turning consultative PDFs into .md fichas, taxonomy, ontology, themes, indicators, and linked analytical structures.
---

# Analise de PDFs, taxonomia e ontologia

Use esta skill para transformar PDFs em um acervo de fichas `.md` conectadas, com taxonomia consistente, ontologia operacional e organizacao tematica reutilizavel.

## Objetivo

Converter cada PDF em conhecimento estruturado, mantendo rastreabilidade para a fonte original e separando:

- ficha do relatorio
- fichas atomicas
- temas consolidados
- indicadores e dados
- relacoes semanticas
- matrizes tecnologicas, quando existirem
- grupos visuais para navegacao no Obsidian

## Principios

- Preserve a evidencia: toda afirmacao relevante deve apontar para a origem no PDF.
- Separe tipos de conhecimento: conceito, tema, indicador, recomendacao, ator, setor, territorio e matriz nao devem ser misturados.
- Reutilize fichas: o que se repete vira tema ou conceito; o que e especifico fica como ficha de relatorio.
- Prefira estrutura leve e consistente a descricoes longas e soltas.
- Registre incerteza quando algo nao puder ser inferido com seguranca.
- Trate grupos como camadas de navegacao: cada ficha pode pertencer a um grupo principal e a um conjunto limitado de conexoes.
- Use cores como sinal visual de grupo, nao como classificacao semantica adicional.

## Fluxo de trabalho

### 1. Inventariar o PDF

- Identifique ano, titulo, setor, territorio, tipo de documento e nome do arquivo.
- Registre o PDF no indice mestre.
- Se houver ambiguidade, marque como `nao inferido` em vez de adivinhar.

### 2. Ler a estrutura do documento

- Leia capa, sumario, introducao, metodologia, diagnostico, proposicoes e anexos.
- Anote a logica interna do PDF: plano, mapa estrategico, gestao tecnologica, planejamento, mercado, inovacao ou outro.
- Capture a linguagem recorrente do documento, pois ela orienta a taxonomia.

### 3. Extrair unidades de conhecimento

Separe o conteudo em unidades minimas reutilizaveis:

- conceitos
- dados e numeros
- recomendacoes
- atores institucionais
- territorios
- setores
- solucoes tecnologicas
- fatores de priorizacao
- megatendencias

Cada unidade deve ser representada por uma ficha `.md` quando tiver valor reutilizavel fora do relatorio.

### 4. Criar a ficha do relatorio

A ficha do relatorio e a base de entrada do sistema.

Ela deve conter:

- metadados essenciais
- resumo rapido
- temas principais
- dados relevantes
- recomendacoes
- fichas vinculadas

Use esta ficha para centralizar a leitura do PDF e apontar para as outras fichas derivadas.

### 5. Criar fichas atomicas

Quebre o relatorio em fichas curtas quando a informacao puder ser reaproveitada.

Regras:

- uma ficha para um conceito estavel
- uma ficha para um dado ou indicador
- uma ficha para uma recomendacao recorrente
- uma ficha para um ator institucional
- uma ficha para uma relacao estrutural relevante

Cada ficha deve ter:

- titulo claro
- origem no relatorio
- tags minimas
- links relacionados

### 6. Construir a taxonomia

Organize o acervo por eixos estaveis.

Taxonomia minima:

- setor
- territorio
- tipo de documento
- tema
- conceito
- indicador
- recomendacao
- matriz

Regras de classificacao:

- se aparece em varios relatorios, vira tema
- se expressa mecanismo, metodo ou nocao transversal, vira conceito
- se e numero, medida ou comparacao, vira indicador
- se e solucao, tendencia ou fator de priorizacao, vira matriz ou componente de matriz
- se e caso especifico, vira ficha de relatorio

### 6.1 Organizar em grupos

Depois da taxonomia, distribua as fichas em grupos de navegacao.

Regras de grupo:

- cada grupo deve ter uma finalidade clara
- um grupo pode reunir varias fichas relacionadas por tema, setor, territorio ou metodo
- uma ficha deve ter um grupo principal e, se necessario, grupos secundarios limitados
- grupos nao devem duplicar a taxonomia; eles devem facilitar leitura e acesso
- grupos muito amplos devem ser divididos

Sugestao de grupos:

- relatorios
- fichas conceituais
- temas
- indicadores
- matrizes
- atores
- territorios
- conexoes transversais

### 6.2 Atribuir cores aos grupos

Cada grupo deve receber uma cor fixa para facilitar leitura visual no Obsidian.

Regras de cor:

- uma cor por grupo principal
- manter a mesma cor em todo o acervo
- usar a cor no frontmatter, em tags ou em qualquer campo padronizado adotado no vault
- evitar mais de uma cor por ficha
- cores devem apoiar navegacao, nao substituir a classificacao semantica

Exemplo de regra operacional:

- relatorios = cinza
- fichas conceituais = azul
- temas = verde
- indicadores = amarelo
- matrizes = laranja
- atores = roxo
- territorios = vermelho
- conexoes transversais = teal

### 6.3 Estabelecer conexoes entre fichas

Toda ficha deve declarar suas relacoes essenciais.

Tipos de conexao recomendados:

- `origem`
- `relacionado_com`
- `deriva_de`
- `repetido_em`
- `contrasta_com`
- `compoe`
- `aponta_para`

Regras:

- conectar primeiro com a ficha do relatorio de origem
- conectar depois com conceitos, temas, indicadores e matrizes relevantes
- preferir poucas conexoes fortes a muitas conexoes fracas
- sempre que possivel, ligar fichas do mesmo grupo e de grupos adjacentes

### 6.4 Padrão Obsidian

Ao usar Obsidian, mantenha o vault organizado com:

- frontmatter consistente
- tags estaveis
- links internos entre fichas
- grupos visuais baseados em cor
- notas centrais para cada grupo

Se o vault usar propriedades, inclua campos como:

- `grupo`
- `cor`
- `tipo`
- `origem`
- `links`

Se o vault usar grafo, as conexoes devem refletir:

- hierarquia de origem
- proximidade conceitual
- recorrencia transversal
- dependencia analitica

### 7. Montar a ontologia operacional

A ontologia deve explicitar os tipos de entidades e as relacoes entre elas.

Entidades principais:

- relatorio
- ficha
- tema
- conceito
- indicador
- matriz-tecnologica
- setor
- territorio
- ator
- recomendacao

Relacoes principais:

- `gera`
- `origina`
- `cita`
- `se repete em`
- `se relaciona com`
- `aponta para`
- `deriva de`
- `contrasta com`
- `compoe`

Regra:

- a ontologia nao precisa ser abstrata; ela deve servir para navegacao, recuperacao e cruzamento do acervo.

### 8. Consolidar temas

Agrupe fichas repetidas em temas consolidados quando houver recorrencia sem perda de sentido.

Um tema deve:

- reunir fichas compativeis
- manter um eixo semantico unico
- evitar duplicacao de conteudo
- servir como hub de navegacao

### 9. Estruturar indicadores

Tudo que for comparavel, mensuravel ou quantificavel deve sair do texto geral e virar ficha de indicador.

Inclua:

- numero
- unidade
- contexto
- fonte
- leitura comparativa, quando houver

### 10. Estruturar matrizes

Quando o PDF trouxer leitura estrategica completa, extraia a matriz tecnologica.

Elementos tipicos:

- megatendencias
- solucoes tecnologicas
- fatores empresariais
- fatores setoriais
- fatores sistemicos
- indice de relevancia
- indice de incerteza
- prioridade

### 11. Vincular tudo

Conecte as fichas por uma rede simples e consistente:

- ficha do relatorio aponta para conceitos, temas, indicadores e matrizes
- tema aponta para fichas relacionadas
- conceito aponta para usos recorrentes
- indicador aponta para a evidencia numerica
- matriz aponta para o relatorio de origem e para seus componentes
- grupo aponta para suas fichas membro e para seu hub principal
- a cor acompanha o grupo em toda a navegacao

### 12. Revisar consistencia

Antes de finalizar:

- confira se o mesmo termo foi classificado do mesmo modo em todo o acervo
- elimine duplicacoes desnecessarias
- verifique se toda ficha tem origem explicita
- confirme se as tags seguem o mesmo padrao
- confirme se o nome do arquivo descreve o conteudo sem ambiguidade
- confirme se cada grupo tem cor fixa e conexoes coerentes

## Padrao de escrita das fichas

- Escreva curto e reutilizavel.
- Use linguagem objetiva.
- Evite copiar blocos longos do PDF.
- Prefira sinteses curtas com fonte clara.
- Se necessario, registre notas de leitura separadas da interpretacao.

## Estrutura de decisao

Quando encontrar um trecho do PDF, decida nesta ordem:

1. isso e especifico do documento?
2. isso se repete em mais de um documento?
3. isso e conceito, tema, dado, ator, recomendacao ou matriz?
4. isso deve virar ficha separada?
5. isso precisa entrar na ontologia como relacao?

## Saidas esperadas

Ao final do processamento, o agente deve ter:

- o PDF catalogado
- a ficha do relatorio criada
- fichas atomicas extraidas
- temas consolidados atualizados
- indicadores separados
- relacoes semanticas registradas
- matriz tecnologica estruturada, quando aplicavel

## Criterios de qualidade

- rastreabilidade completa
- taxonomia estavel
- ontologia util para busca e cruzamento
- fichas pequenas e reutilizaveis
- separacao clara entre fato, interpretacao e recomendacao
- consistencia entre anos, setores e territorios

## Regra final

Se uma informacao nao melhora a consulta, a navegacao ou a reutilizacao do acervo, nao a transforme em ficha.
