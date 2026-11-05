# Discovery — Weather App

## Contexto

O negócio solicita uma aplicação de previsão do tempo para que usuários possam
consultar informações meteorológicas de cidades. A experiência deve funcionar
também em dispositivos móveis. O briefing ainda não define fonte de dados,
detalhes das informações exibidas nem regras para busca e previsão.

## Requisitos Funcionais

- **RF1 — Buscar cidades:** permitir que o usuário pesquise cidades.
- **RF2 — Clima atual:** exibir as condições meteorológicas atuais da cidade
  selecionada.
- **RF3 — Previsão:** exibir a previsão do tempo para os próximos cinco dias.
- **RF4 — Unidade de temperatura:** permitir alternar entre Celsius e
  Fahrenheit e apresentar as temperaturas na unidade escolhida.
- **RF5 — Uso em dispositivos móveis:** permitir o uso das funcionalidades
  principais em dispositivos móveis.

## Requisitos Não-Funcionais

- **RNF1 — Responsividade:** a interface deve se adaptar a telas móveis.
- **RNF2 — Usabilidade:** busca, consulta do clima e alternância de unidade
  devem ser compreensíveis e fáceis de usar.
- **RNF3 — Resiliência:** o produto deve considerar falhas de rede ou
  indisponibilidade da fonte de dados e informar o usuário de forma clara.
- **RNF4 — Acessibilidade:** controles e informações devem ser utilizáveis por
  diferentes pessoas e dispositivos de entrada.

## Riscos

| Risco | Probabilidade | Impacto | Mitigação |
| --- | --- | --- | --- |
| Fonte de dados indisponível ou com limites de uso | Média | Alto | Definir uma fonte adequada e tratar falhas com mensagens claras. |
| Busca retornar cidades homônimas ou resultados inesperados | Alta | Médio | Apresentar informações de localização suficientes para distinguir resultados. |
| Interpretação diferente do que significa “previsão de cinco dias” | Média | Médio | Definir se o período inclui o dia atual e como as datas serão apresentadas. |
| Experiência ruim em telas pequenas | Média | Alto | Priorizar layout móvel e validar em diferentes larguras de tela. |
| Conversão ou apresentação incorreta entre Celsius e Fahrenheit | Baixa | Alto | Definir a unidade de referência e validar os valores convertidos. |

## Perguntas em Aberto (Open Questions)

1. Qual fonte de dados meteorológicos deve ser utilizada? Há requisitos de custo,
   chave de API ou limites de uso?
2. Quais informações devem aparecer no clima atual e na previsão?
3. A previsão de cinco dias inclui o dia atual?
4. A busca deve oferecer sugestões e permitir desambiguar cidades com o mesmo
   nome? Quais informações de localização serão mostradas?
5. Qual deve ser a unidade padrão: Celsius ou Fahrenheit?
6. A aplicação deve detectar a localização do usuário automaticamente ou a
   consulta deve começar somente após uma busca?
7. Quais idiomas e regiões devem ser suportados?
8. É necessário guardar cidades favoritas ou manter a última busca?
9. Qual nível de suporte a navegadores, acessibilidade e funcionamento offline
   é esperado?

## Suposições (Assumptions)

- O usuário escolhe uma cidade para consultar; não há requisito confirmado de
  geolocalização automática.
- A aplicação atende consultas informativas, sem necessidade de conta ou
  autenticação.
- Deve haver conexão com a internet para obter dados meteorológicos atualizados.
- A interface precisa ser utilizável em dispositivos móveis, mas o briefing não
  determina dimensões mínimas de tela ou navegadores suportados.
- Os detalhes e a fonte dos dados ainda precisam ser decididos; as suposições
  não representam decisões definitivas de produto.
