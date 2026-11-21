# Vigilantes da Luz — monitoramento de interrupções no RJ

Mapa interativo dos locais que ficaram sem luz após o temporal de 7 de novembro de 2026, em todo o estado do Rio de Janeiro. Base de pontos revisada em 19/11/2026; triagem de pistas e monitoramento atualizados em 19/11/2026.


## Atualização matinal — 21/11/2026 (08h29 BRT)

**Resultado cartográfico:** nenhum novo ponto confirmado. Nenhum candidato novo apresentou, simultaneamente, endereço de ocorrência verificável e coordenadas verificáveis. O Top 20, dados/pontos.csv, dados/pontos.geojson, dados/resumo_por_municipio.csv e index.html foram preservados.

### Sinais novos em investigação

- **São Gonçalo — Portão do Rosa, Rua Fernandes de Mendonça:** reclamação publicada em 20/11 às 22h03 diz que a rua estava sem luz e que moradores já haviam reclamado. A existência do logradouro e sua associação ao bairro são corroboradas por referência pública de endereço, mas não foi obtida coordenada verificável do trecho. Prioridade alta; não inserir no mapa até geocodificação confiável.
- **Arraial do Cabo:** relato publicado em 20/11 às 18h31 descreve interrupções diárias desde 17/11, transformador antigo e troca de poste; sem bairro ou rua.
- **São Francisco de Itabapoana:** relato de 20/11 às 23h55 afirma 5–6 interrupções por dia e baixa tensão em várias residências; sem localidade.
- **Belford Roxo:** relato de 21/11 às 04h26 diz que a energia oscilou desde a tarde de 20/11 e caiu totalmente à noite; bairro e rua não informados.
- **Nova Iguaçu — Botafogo:** relato de 21/11 às 04h27 descreve quedas repetidas em casas vizinhas desde 20/11; sem rua.
- **Rio de Janeiro (capital):** duas reclamações novas na janela de publicação: uma relata falta desde 19/11 às 14h36 (36h50 até a publicação de 21/11 às 03h26); outra, publicada em 20/11, afirma falta desde 11/11 e aponta possível problema em fase no poste. Ambas sem bairro/logradouro; não há confirmação de abrangência coletiva.
- **Saquarema:** menção municipal genérica publicada em 21/11 às 05h50. Pode se sobrepor tematicamente às pistas anteriores de Saquarema e Vilatur; não contar como ocorrência distinta.
- **Rio de Janeiro — Edifício Portobianco:** relato de 20/11 às 22h48 atribui a interrupção ao corte/furto de cabos no poste em frente ao edifício. Endereço mascarado e possível sobreposição com reclamação anterior de condomínio; não contar separadamente até deduplicação.

### Snapshot operacional agregado

Powercut, às **08h20 de 21/11**: **173 faltas** e **3.049 clientes sem energia** na página estadual. Maiores agrupamentos identificados como Enel Rio: Cidade Parque Paulista (572), Guapimirim (441), Araruama (421), São José do Vale do Rio Preto (218), Santa Lúcia (182), Itatiaia (134), Itaperuna (114), Tamoios (110), Jacuacanga (67), Casimiro de Abreu (66), Cantagalo (61) e Jaconé (46).

Comparação com o snapshot estadual de 20/11 às 08h40 (212 faltas e 4.545 clientes): redução de 39 registros e 1.496 clientes no retrato agregado. Isso não prova que cada ocorrência anterior foi encerrada. O total estadual pode reunir mais de uma distribuidora; os agrupamentos acima aparecem identificados como Enel Rio. O agregador declara coletar os mapas públicos a cada 10 minutos e não fornece endereço, início, duração ou coordenadas individuais.

### Qualidade e cobertura das fontes

- **Enel:** página oficial do Mapa da Energia acessível; mapa dinâmico não apresentou tabela preenchida na extração desta rodada. A própria página alerta que os registros podem incluir desligamentos inferiores a três minutos e refletir manobras operacionais.
- **Light:** Mapa de Ocorrências Emergenciais acessível, mas sem conteúdo textual legível para extração nesta consulta.
- **ANEEL:** indicadores coletivos DEC/FEC disponíveis; atualização mensal e granularidade por conjunto de unidades consumidoras, inadequados para localizar ocorrência diária por rua.
- **Prefeituras/Defesa Civil/Procons e imprensa:** nenhuma nova publicação com endereço e coordenadas verificáveis foi localizada na janela pesquisada.

### Auditoria da base

- 120 pontos no CSV e 120 feições no GeoJSON.
- 96 registros com posicao_conferida=sim; isso indica conferência de posição, não necessariamente precisão de quarteirão.
- Precisão declarada no CSV: 24 registros rua, 15 ponto e 81 bairro.
- Nenhuma coordenada nova foi criada, nenhuma posição foi alterada e o Top 20 foi preservado.
- As 9 pistas desta rodada e o snapshot agregado foram acrescentados a dados/pistas_nao_verificadas.csv; permanecem fora da camada cartográfica.

**PDF:** não gerado nesta rodada porque não houve novo ponto confirmado para incorporar. O relatório de investigação fica registrado nesta seção e no CSV de pistas.



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

## Verificação de monitoramento — 19/11/2026, 16h23

- **Novos pontos confirmados: nenhum.** A base cartográfica permanece com **120 registros**, dos quais **96** têm posição marcada como conferida. O Top 20 foi preservado, sem reordenação; nenhum endereço ou coordenada foi criado.
- **Nova pista coletiva não verificada:** reclamação publicada pela Light às 09h24 relata interrupções recorrentes em uma rua do município do Rio, com cerca de dez condomínios supostamente dependentes de um único transformador; a rua teria ficado sem energia durante toda a noite anterior e novamente no momento da publicação. O resultado público não informa bairro nem logradouro. Pista adicionada a `dados/pistas_nao_verificadas.csv`, sem coordenadas e fora da camada de pontos.
- **Reforço institucional de Paquetá:** a Defensoria Pública do RJ informou em 18/11 a abertura de procedimento administrativo sobre a Light, após relatos de apagões por semanas. A DPRJ relata que a Light enviou quatro geradores como medida paliativa e que, antes disso, havia interrupções de 1 a 3 horas em partes da ilha e de até três dias em regiões específicas. A fonte foi acrescentada ao registro já existente de Ilha de Paquetá no CSV e no GeoJSON; coordenadas, precisão, nível e ranking não foram alterados.
- **Snapshot operacional às 16h20:** Powercut registrou **268 falhas e 13.945 clientes sem energia** na página estadual. Principais rótulos identificados como Enel Rio: Barra de São João (4.106), Tamoios (732), Cascatinha (710), Guia de Pacobaíba (463), Duas Barras (412), Itaperuna (405), Cidade Parque Paulista (350), Parque Jóckey Club (348), Piratininga (332), Petrópolis (293), Maricá (261) e Ajuda de Cima (257). Às 12h20, o mesmo painel mostrava 267 falhas e 9.183 clientes; diferença de +1 falha e +4.762 clientes no snapshot das 16h20. São contagens dinâmicas e agregadas, sem endereço, hora inicial, duração ou coordenadas; não foram convertidas em pontos. O painel também informa que reúne dados de mais de um operador, portanto o total estadual não deve ser tratado como total exclusivo da Enel Rio.
- **Deduplicação:** Engenho do Mato, Piratininga, Petrópolis, Maricá e outras áreas já aparecem na base ou em pistas anteriores; a leitura operacional não gerou novas feições. Rótulos como Barra de São João, Tamoios e Cascatinha permanecem sinais a investigar, não endereços.
- **Triagem negativa:** foram excluídos como candidatos coletivos relatos de residência isolada sem energia após manutenção, medidor com aquecimento/fogo em uma única unidade, divergência cadastral de medidor, ligação/religação individual e corte por cobrança. Uma reclamação de fase parcial em residência sem bairro/logradouro também não foi promovida a ponto.
- **Fontes primárias e limitações:** o mapa da Enel informa dados dinâmicos por município e alerta que pode refletir desligamentos momentâneos inferiores a três minutos; o mapa institucional da Light existe, mas o conteúdo interativo não foi extraível em texto nesta consulta. A base pública da ANEEL foi atualizada em **12/11/2026**, tem frequência mensal e granularidade por conjunto de unidades consumidoras, não por rua. A Defensoria Pública trouxe a nova confirmação institucional sobre Paquetá.
- **Arquivos:** `dados/pistas_nao_verificadas.csv` recebeu a nova pista coletiva e o snapshot agregado; `dados/pontos.csv` e `dados/pontos.geojson` receberam apenas o reforço de fonte/fato do registro existente de Paquetá. Nenhuma nova feição foi criada. `index.html`, resumo municipal e Top 20 não foram alterados. **PDF não regenerado**, pois não houve novo ponto confirmado.

Fontes: [DPRJ — atuação pela normalização do fornecimento em Paquetá](https://defensoria.rj.def.br/noticia/detalhes/33174-DPRJ-atua-pela-normalizacao-do-fornecimento-de-energia-eletrica-em-Paqueta-que-sofre-com-apagoes); [reclamação Light — interrupções recorrentes em rua com cerca de dez condomínios](https://www.reclameaqui.com.br/light-servicos-de-eletricidade/minha-rua-esta-sem-energia-eletrica-constantemente-e-minha-geladeira-quebrou_EDatL2KTomyVIo0S/); [Powercut — Estado do RJ](https://powercut.io/br/estado-do-rio-de-janeiro/); [Mapa da Enel](https://www.enel.com.br/pt/Informativos/mapa-falta-de-luz.html); [Mapa de Ocorrências Emergenciais da Light](https://www.light.com.br/SitePages/MapaDeOcorrenciasEmergenciais.aspx); [ANEEL — interrupções nas redes de distribuição](https://dadosabertos.aneel.gov.br/dataset/interrupcoes-de-energia-eletrica-nas-redes-de-distribuicao).


## Verificação de monitoramento — 20/11/2026, 08h46

- **Novos pontos confirmados: nenhum.** A base dados/pontos.csv permanece com **120 registros**, dos quais **96** têm posição marcada como conferida; dados/pontos.geojson mantém **120 feições**. O ranking Top 20 foi preservado, sem reordenação. Não foram criados endereços ou coordenadas. A auditoria dos campos de precisão mostra **24 registros marcados como rua, 15 como ponto e 81 como bairro**; portanto, os 96 marcados como posição conferida não equivalem a 96 localizações em nível de quarteirão. Os 81 registros de bairro permanecem como legado da base, sem serem promovidos a precisão de rua.
- **Pista prioritária — Vilatur, Saquarema (Enel):** reclamação pública de 20/11 às 00h17 relata interrupções frequentes, oscilações e falta de energia no momento da publicação. O bairro é identificável, mas não há rua/trecho, início exato ou duração do episódio. Como sinal auxiliar, o Powercut listou Vilatur com **660 clientes** no snapshot de 19/11 às 19h20; no snapshot das 08h40 de 20/11 Vilatur não aparece entre as 12 maiores localidades, o que não prova normalização nem persistência. Mantida apenas como pista, sem coordenadas.
- **Pista genérica — Saquarema (Enel):** reclamação de 19/11 às 21h12 relata queda de fase todas as noites e equipamentos oscilando, sem bairro ou rua. Mantida separada de Vilatur porque não há prova de que seja a mesma ocorrência.
- **Pista de qualidade de fornecimento — Mesquita (Light):** reclamação de 19/11 às 22h46 atribui quedas frequentes na rua a possível transformador insuficiente. Não informa logradouro e também descreve uma interrupção individual/histórica antes da regularização em 2026; não confirma falta coletiva atual. Mesquita já tem pontos na base, mas a falta de endereço impede deduplicação espacial.
- **Snapshot operacional agregado — 20/11 às 08h40:** Powercut apresentava **212 faltas e 4.545 clientes sem energia** na página estadual. Maiores rótulos identificados como Enel Rio: Triunfo (501), Itacurussá (418), Arraial do Cabo (292), Mangaratiba (232), Maricá (221), São José do Vale do Rio Preto (215), Itaperuna (164), Monsuaba (155), Parque Bela Vista (150), Itambi (145), Petrópolis (136) e Itaipava (115). O total da página reúne mais de um operador e não é exclusivo da Enel Rio; o agregador não fornece rua, início, duração ou coordenadas. Em relação ao snapshot de 19/11 às 16h20 (268 falhas e 13.945 clientes), a leitura atual é menor em 56 falhas e 9.400 clientes, mas essa diferença entre retratos agregados não prova quais ocorrências foram encerradas.
- **Triagem negativa:** reclamações novas sobre religação/corte de uma unidade em Campos dos Goytacazes, furto de cabos e dano de medidor em uma residência na capital, corte individual em Nova Iguaçu e dano de aparelhos em uma residência de São Gonçalo não foram promovidas a ocorrências coletivas de rede. Permanecem fora do mapa.
- **Qualidade e cobertura das fontes:** o mapa oficial da Enel foi acessado, mas seus valores dinâmicos não ficaram legíveis na extração textual; a própria página descreve cobertura municipal da Região Metropolitana e alerta que os números podem refletir interrupções momentâneas inferiores a três minutos. O mapa institucional da Light está publicado, mas o conteúdo interativo não apresentou dados extraíveis nesta consulta. O Powercut é um agregador de mapas públicos e lista Enel Rio, CEMIG e outras operações; não inclui Light entre as fontes exibidas, portanto não cobre sozinho o estado. O conjunto da ANEEL tem frequência mensal e granularidade por conjunto de unidades consumidoras; o recurso de interrupções de 2026 consultado estava atualizado em 04/09/2026, sem utilidade para confirmar ocorrências de rua em 20/11. Não foi localizada nova publicação de prefeitura, Defesa Civil, Procon ou imprensa local com endereço e coordenadas verificáveis na janela.
- **Arquivos:** dados/pistas_nao_verificadas.csv recebeu três novas pistas e o snapshot de 20/11 às 08h40. dados/pontos.csv, dados/pontos.geojson, dados/resumo_por_municipio.csv e index.html não foram alterados. Top 20 preservado. **PDF não gerado**, pois não houve novo ponto confirmado a incorporar.

Fontes: [Reclamação — Vilatur, Saquarema](https://www.reclameaqui.com.br/enel-distribuicao-rio/minha-energia-eletrica-em-vilatur-saquarema-esta-com-falhas-constantes-e-oscilacoes_6lHz9YbNnhq-yy6_/); [Reclamação — Saquarema, queda de fase diária](https://www.reclameaqui.com.br/enel-distribuicao-rio/minha-energia-tem-queda-de-fase-todo-dia-e-nao-consigo-reclamar_HeID0Z2PXsJ9zFGT/); [Reclamação — Mesquita, transformador](https://www.reclameaqui.com.br/light-servicos-de-eletricidade/minha-energia-eletrica-cai-toda-hora-e-a-light-nao-instala-transformador_giWb4lkj6fMqXQv3/); [Powercut — Estado do RJ](https://powercut.io/br/estado-do-rio-de-janeiro/); [Mapa oficial da Enel](https://www.enel.com.br/pt/Informativos/mapa-falta-de-luz.html); [Mapa de Ocorrências Emergenciais da Light](https://www.light.com.br/SitePages/MapaDeOcorrenciasEmergenciais.aspx); [ANEEL — interrupções nas redes de distribuição](https://dadosabertos.aneel.gov.br/dataset/interrupcoes-de-energia-eletrica-nas-redes-de-distribuicao).

## Verificação de monitoramento — 20/11/2026, 09h25

- **Novos pontos definitivos:** nenhum. A base principal permanece com 120 registros; os 96 pontos marcados com posição conferida e o Top 20 foram preservados. Não houve endereço e coordenadas de quarteirão novos que justificassem alterar dados/pontos.csv, dados/pontos.geojson ou o HTML.
- **Nova pista coletiva da Light — município do Rio de Janeiro:** reclamação publicada em 20/11 às 05h29 informa que dois andares de um condomínio, totalizando 25 apartamentos, estavam sem luz desde 19/11 às 15h40. Duração aproximada até a publicação: 13h49. Bairro e logradouro não aparecem; também não é possível distinguir falha da rede de problema interno do condomínio. Registrada como pista, não como ponto.
- **Atualização da pista de Vilatur, Saquarema:** a reclamação de 20/11 às 00h17 já estava registrada. No snapshot Powercut de 19/11 às 19h20, a localidade aparecia com 660 clientes; no retrato de 20/11 às 08h40, aparece na listagem completa em 105º lugar, com 2 clientes. Isso indica redução no retrato agregado, mas não comprova normalização nem elimina a recorrência alegada pelo consumidor. Sem rua e coordenadas, continua fora do mapa.
- **Nova evidência municipal para Guapimirim:** a Prefeitura informou oficialmente que, após o temporal de 07/11, registrou 13 ocorrências de grande porte em diferentes bairros; 10 ainda estavam sem solução no levantamento e a Ouvidoria recebeu 56 reclamações de interrupções superiores a 72 horas. É evidência forte da gravidade municipal, mas sem discriminação dos bairros/ruas e sem coordenadas. A pista foi adicionada separadamente. No snapshot Powercut de 20/11 às 08h40, Guapimirim ainda aparecia com 15 clientes afetados; esse número é apenas um retrato agregado.
- **Ocorrências excluídas da triagem de apagão coletivo:** reclamação de Campos dos Goytacazes publicada em 20/11 às 04h04 descreve corte individual por alegada irregularidade e demora de religação; reclamação da Light publicada às 03h56 descreve furto de cabos e dano ao medidor de uma residência. Nenhuma comprova interrupção coletiva da rede no quarteirão.
- **Fontes oficiais:** a página da Enel Rio exibe mapa municipal dinâmico e alerta que os registros podem incluir interrupções momentâneas inferiores a três minutos ou cenários já reduzidos por manobras. O conteúdo do mapa incorporado não forneceu nesta consulta a tabela municipal legível. O mapa da Light abriu sem conteúdo textual extraível. O recurso 2026 da ANEEL consultado continua com última atualização em 04/09/2026, portanto não confirma ocorrências de 20/11.
- **Arquivos:** dados/pistas_nao_verificadas.csv atualizado; HTML, pontos.csv, pontos.geojson e Top 20 preservados. PDF não regenerado porque nenhum ponto definitivo foi incluído.

Fontes: [Powercut — retrato estadual de 20/11 às 08h40](https://powercut.io/br/estado-do-rio-de-janeiro/); [reclamação coletiva da Light no Rio](https://www.reclameaqui.com.br/light-servicos-de-eletricidade/meus-2-andares-do-condominio-estao-sem-luz-desde-ontem-e-a-light-nao-aparece_srT4aBDi4cJx2EiE/); [Prefeitura de Guapimirim — dados da Ouvidoria e ocorrências na rede](https://guapimirim.rj.gov.br/2026/11/justica-determina-que-enel-cumpra-imediatamente-ordem-de-restabelecimento-de-energia-em-guapimirim/); [Vilatur — reclamação de oscilações](https://www.reclameaqui.com.br/enel-distribuicao-rio/minha-energia-eletrica-em-vilatur-saquarema-esta-com-falhas-constantes-e-oscilacoes_6lHz9YbNnhq-yy6_/); [Mapa da Enel Rio](https://www.enel.com.br/pt/Informativos/mapa-falta-de-luz.html); [Mapa da Light](https://mapa-ocorrencias.light.com.br/); [ANEEL — base histórica de interrupções](https://dadosabertos.aneel.gov.br/dataset/interrupcoes-de-energia-eletrica-nas-redes-de-distribuicao).
