# Analise Relatorio

Base de trabalho para transformar o acervo de PDFs em um sistema de fichas conectadas.

## Estrutura

- `00_INDEX/` - indice mestre do acervo
- `01_RELATORIOS/` - catalogo dos PDFs e metadados
- `02_FICHAS/` - fichas atomicas geradas a partir dos relatorios
- `03_TEMAS/` - fichas tematicas consolidadas
- `04_INDICADORES/` - dados, numeros e evidencias
- `05_REDES_E_LINKS/` - relacoes, cruzamentos e mapas conceituais
- `06_MATRIZES/` - matrizes tecnologicas, megatendencias e fatores
- `08_COSMOBRASIL/` - base dedicada ao acervo Cosmobrasil e ao futuro agente especialista
- `Relatorios-Finais/` - atalho para o volume externo com os PDFs

## Metodo

1. Catalogar cada PDF no indice mestre.
2. Extrair metadados e sumario.
3. Quebrar o conteudo em fichas menores.
4. Ligar fichas por tags, setor, territorio e tema.
5. Consolidar padroes entre anos.
6. Extrair matrizes tecnológicas por setor, com megatendencias, solucoes e fatores.
7. Centralizar o caso Cosmobrasil em uma base dedicada para consulta e agente especialista.

## Deploy do dashboard

O painel visual fica em `dashboard/`, mas o deploy direto no Netlify usa a raiz do repositório.

- pasta publicada: `.`
- arquivo de entrada: `index.html`
- configuracao: `netlify.toml`

O `index.html` da raiz redireciona automaticamente para `dashboard/`.

Se preferir publicar pelo painel do Netlify, use:

1. `Build command`: vazio
2. `Publish directory`: `.`
