# Vigilantes da Luz — monitoramento de interrupções no RJ

Mapa interativo dos locais que ficaram sem luz após o temporal de 7 de novembro de 2026, em todo o estado do Rio de Janeiro. Atualizado em 18/11/2026.

Abra `index.html` no navegador (Chrome ou Edge, com internet).

## Cobertura

- **Grande Rio e Baixada** (Light e Enel): imprensa, prefeituras e relatos de moradores.
- **Região dos Lagos** (Enel): protestos em Saquarema (RJ-106, km 73) e Cabo Frio (Maria Joaquina e Jardim Caiçara), além de relatos em Iguaba, Saquarema, Cabo Frio, Búzios e Araruama.
- **Norte e Noroeste** (Enel): protestos na BR-356 em Cardoso Moreira; bairros sem luz em Cambuci e Itaperuna; pico de 13 mil unidades em Campos.
- **Serra, Sul Fluminense e Costa Verde**: não houve notícia de falta de luz ligada ao temporal; há relatos isolados de moradores em Petrópolis, Miguel Pereira e Macaé.
- **Energisa** (região de Nova Friburgo): sem relatos ligados ao temporal.

## Fontes

- Imprensa e prefeituras, 8 a 13/11 (links em cada ponto).
- Reclamações públicas no Reclame Aqui contra Light, Enel Rio e Energisa, 7 a 16/11.
- Não incluídos: X, Instagram, Facebook, Threads e Bluesky, que exigem conta para busca.

## Arquivos

| Arquivo | Conteúdo |
|---|---|
| `index.html` | Mapa com filtros (nível, concessionária, origem), raio de busca e exportação em CSV e KML |
| `dados/pontos.csv` | Todos os pontos com coordenadas, nível, horas sem luz e links das fontes |
| `dados/pontos.geojson` | Os mesmos pontos em GeoJSON |
| `dados/resumo_por_municipio.csv` | Pico de clientes sem luz (imprensa) e reclamações por município |

## Critérios

- **Crítico**: protesto no local ou 70 h ou mais sem luz.
- **Alto**: 48 h ou mais, ou apontado como o caso mais grave do município.
- **Afetado**: citado sem duração ou com menos de 48 h.

Relatos de moradores usam as horas informadas pelo próprio morador. Coordenadas marcadas como conferidas foram checadas no geocodificador da Esri; as demais são aproximadas.

## Privacidade

Nenhum nome de pessoa é publicado. Ruas aparecem sem número. As reclamações do Reclame Aqui já são públicas e mascaradas pela plataforma.

## Verificação de monitoramento — 18/11/2026, 16h40

- Não foram identificados novos pontos que cumpram simultaneamente os critérios de endereço verificável, coordenadas e evidência corroborável desde a rodada anterior.
- A base permanece com **120 registros**; **96** têm posição marcada como conferida. O ranking Top 20 foi preservado, sem reordenação.
- Foram registradas pistas novas de Paciência e Nova Jersey (Rio de Janeiro), além de relatos individuais sem logradouro identificável; permanecem fora da camada de pontos confirmados.
- O arquivo `dados/pontos.geojson` foi reconstruído a partir de `dados/pontos.csv`, sem inclusão ou alteração de ocorrências, porque a versão anterior terminava incompleta. A nova versão contém 120 feições válidas.
- Nenhum relatório PDF foi gerado nesta rodada, pois não houve novo ponto confirmado a incorporar.


## Verificação de monitoramento — 19/11/2026, 08h33

- **Nenhum novo ponto confirmado**: não apareceu candidato com rua/trecho verificável e coordenadas sustentadas por fonte suficiente. A base cartográfica permanece com **120 pontos**, dos quais **96** têm posição marcada como conferida; Top 20 preservado, sem reordenação.
- Três novas pistas públicas foram separadas em `dados/pistas_nao_verificadas.csv`: Niterói (Enel, relato de interrupções recorrentes em todo o quarteirão, sem logradouro), Maricá (Enel, rua mascarada) e município do Rio de Janeiro (Light, flutuação/falta de fase em algumas casas, sem bairro ou rua). Nenhuma foi adicionada ao CSV/GeoJSON de pontos.
- Uma reclamação de Petrópolis sobre falta de energia após troca de titularidade e pedido de religação foi triada fora da camada de interrupções de rede: o relato descreve uma ligação individual, sem evidência de falha coletiva da distribuição.
- O mapa oficial da Enel informa que os dados são dinâmicos e podem incluir interrupções momentâneas inferiores a três minutos, além de mudar após manobras de telecomando. O extrator público consultado indicou o feed Enel Rio ativo às 08h20 (horário de Brasília), com 192 registros no feed; esse número é de registros, não de clientes afetados, e não fornece, nesta consulta, evidência de endereço e coordenadas para inclusão.
- O mapa institucional da Light está publicado, mas seu mapa incorporado não entregou conteúdo textual extraível nesta rodada. Não foi localizada nova publicação de ANEEL, prefeitura, Defesa Civil ou imprensa local com endereço e coordenadas verificáveis no período.
- **Nenhum PDF foi gerado**, pois não houve ponto confirmado a incorporar. O mapa, o ranking e os arquivos de pontos foram preservados sem alteração.

Fontes consultadas: [Mapa da Energia — Enel Rio](https://www.enel.com.br/pt/Informativos/mapa-falta-de-luz.html); [Mapa de Ocorrências Emergenciais — Light](https://www.light.com.br/SitePages/MapaDeOcorrenciasEmergenciais.aspx); [feed público de estado das fontes](https://powercut.io/api/now.json); [pista Niterói](https://www.reclameaqui.com.br/enel-distribuicao-rio/estou-sem-luz-em-minha-regiao-ha-dias-e-a-enel-nao-resolve_DQ0sFIIm0SBpckhj/); [pista Maricá](https://www.reclameaqui.com.br/enel-distribuicao-rio/minha-energia-oscila-e-falta-luz-em-marica-ha-anos_LUQeC34AsGRKog8O); [pista Light — Rio de Janeiro](https://www.reclameaqui.com.br/light-servicos-de-eletricidade/problema-recorrente-de-falta-ds-energia-no-local_ZxwXCjDJjcsunCAH/).
