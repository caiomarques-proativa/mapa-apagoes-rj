# Vigilantes da Luz — monitoramento de interrupções no RJ

Mapa interativo dos locais que ficaram sem luz após o temporal de 7 de novembro de 2026, em todo o estado do Rio de Janeiro. Base de pontos atualizada em 18/11/2026; triagem de pistas e monitoramento atualizados em 19/11/2026.

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


## Verificação de monitoramento — 19/11/2026, 09h05

- **Novos pontos confirmados:** nenhum. A base de pontos permanece com **120 registros**, dos quais **96** têm posição marcada como conferida. O Top 20 foi preservado, sem reordenação.
- **Novas pistas registradas:** uma reclamação da Light publicada em 18/11, às 20h17, informa uma rua sem energia por cerca de 6 horas no município do Rio de Janeiro, mas não divulga bairro ou logradouro; foi incluída em `dados/pistas_nao_verificadas.csv`.
- **Sinais operacionais agregados:** a página estadual do Powercut apresentava um retrato atualizado às **06h20 de 19/11** com **128 falhas e 7.280 clientes sem energia** no RJ. Entre as localidades identificadas, foram registradas como pistas: Pipeiras (São João da Barra, 812 clientes), Balneário da Praia de João Francisco de Paula (Quissamã, 533), São José do Vale do Rio Preto (523, rótulo municipal), Barracão (São Gonçalo, 283), Sumidouro (258, rótulo municipal), Parque Santo Antônio (Campos dos Goytacazes, 246), Canellas City (Iguaba Grande, 237), Virgem Santa (Macaé, 224) e Araçatiba (Maricá, 204). Esses números são um retrato agregado de falhas, não duração, gravidade ou confirmação de apagão persistente. A fonte informa coleta dos mapas públicos em intervalos de dez minutos, mas o snapshot acessível nesta execução é de 06h20 e não deve ser apresentado como estado em tempo real às 09h05.
- **Deduplicação:** Itaipava (Petrópolis) também apareceu no feed com 169 clientes, mas já existe ponto na localidade; não foi criada uma segunda entrada. As localidades Soledade e Bairro I não foram atribuídas a municípios porque o rótulo é ambíguo. A pista de Niterói de 18/11 e a pista de Maricá de 18/11 já constavam no arquivo e não foram duplicadas.
- **Triagem negativa:** reclamações sobre religação após troca de titularidade, nova ligação e rompimento do fio de uma residência foram excluídas da lista de candidatos coletivos, por não comprovarem falha de rede em quarteirão.
- **Fontes primárias:** o mapa da Enel estava acessível, mas o conteúdo dinâmico não expôs os números/ocorrências em texto nesta consulta; a própria Enel alerta que o painel pode incluir interrupções momentâneas inferiores a três minutos. O portal da Light confirmou a existência do mapa institucional, mas seu conteúdo interativo não ficou legível para extração. A base de interrupções da ANEEL tem frequência mensal e granularidade por conjunto de unidades consumidoras; o recurso de 2026 consultado estava atualizado em **04/09/2026**, portanto não foi usado para confirmar ocorrências do dia.
- **HTML, pontos.csv e GeoJSON:** preservados, sem alterações, pois nenhuma pista alcançou endereço e coordenadas verificáveis em nível de quarteirão. **PDF:** não regenerado, pelo mesmo motivo. O raio espacial de 2 km e o ranking Top 20 não foram recalculados.

Fontes: [Mapa da Enel](https://www.enel.com.br/pt/Informativos/mapa-falta-de-luz.html); [Mapa de Ocorrências Emergenciais da Light](https://www.light.com.br/SitePages/MapaDeOcorrenciasEmergenciais.aspx); [Powercut — Estado do RJ](https://powercut.io/br/estado-do-rio-de-janeiro/); [Powercut — Campos dos Goytacazes](https://powercut.io/br/campos-dos-goytacazes/); [reclamação Light — rua sem luz por cerca de 6 horas](https://www.reclameaqui.com.br/light-servicos-de-eletricidade/minha-horas-e-ninguem-me-da-informacao_KExPGZzVxQHUKg-S/); [ANEEL — interrupções nas redes de distribuição](https://dadosabertos.aneel.gov.br/dataset/interrupcoes-de-energia-eletrica-nas-redes-de-distribuicao).
