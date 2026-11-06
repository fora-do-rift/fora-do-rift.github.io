# Rift Mercado — CBLOL 2027

Protótipo funcional offline de um portal de transferências do CBLOL, com três funcionalidades:

1. **Planilha visual** por equipes e rotas, status com cores, filtros e detalhes de jogadores;
2. **Central de movimentações** com notícia resumida e link direto para fonte;
3. **Simulador de elencos** com 5 rotas, alertas de imports e vínculos listados.

## Executar

Abra `index.html` em um navegador moderno. Não requer instalação nem servidor.

## Recursos

- Adicionar movimentos com fonte e data (salva no `localStorage` deste navegador).
- Exportar CSV para Excel com separador `;`.
- Simular elencos com validação ilustrativa de até dois imports.
- Funciona em celular e computador.

## Limitações importantes

- Esta é uma **primeira versão local**, não um portal hospedado. Alterações feitas por uma pessoa não aparecem para outra.
- As referências contratuais de 2026 **não** são escalações confirmadas para 2027.
- Notícias e fontes não se atualizam automaticamente.
- O status de residência competitiva foi inspirado nos registros de 2026 e precisará de validação para 2027 (nacionalidade não é igual à residência competitiva).
- Alguns times e jogadores são apenas um recorte da base inicial, e não uma lista exaustiva de elencos ou rumores.
- Dados de mercado consultados em 5 de novembro de 2026.

## Próxima etapa para produção

Migrar para Next.js, banco Supabase/Postgres, autenticação de editores, logs de revisão, URLs compartilháveis de simulações e fluxo de verificação/aprovação de fontes. Aplicar as diretrizes da Riot quanto a marcas e uso dos ativos de LoL.

## Fontes

- https://maisesports.com.br/contratos/league-of-legends
- https://www.sheepesports.com/pt/all/transfers/cblol
- https://obewise.com.br/index.php/2026/10/30/cblol-2026-a-decisao-de-xyno-pode-mudar-o-cblol-2027/
- https://lolesports.com/pt-BR/news/cblol2026
- https://www.migalhas.com.br/depeso/459611

## Imagens locais

Logos dos oito times e retratos dos jogadores ficam em `assets/teams/` e `assets/players/`, com os links de origem registrados nos respectivos arquivos `sources.json`. SuperCleber e BUERO usam retratos transparentes da Sheep Esports. Os demais retratos vêm de Mais Esports/PandaScore e LoL Esports. As imagens são salvas localmente para funcionar offline.

## Planilha 2027

Revisão por equipe em 05/11/2026: 57 registros de mercado, dos quais 36 aparecem no mapa. A planilha inclui chegadas, compras, retornos, permanências e renovações com fonte. Saídas e casos indefinidos ficam somente na Central. Os registros locais do usuário são preservados.

As fontes editoriais são @SheepEsportsBR, @luisshowtana, @maisesportsbr e @Correslol. Anúncios oficiais das organizações servem para confirmar ou corrigir os relatos. Parte dos posts foi consultada em versões públicas indexadas, com links para o original; as respostas foram conferidas junto às perguntas.

- Confirmado: anúncio oficial ou afirmação categórica da fonte; a ficha identifica qual.
- Vínculo vigente: contrato verificado para 2027, sem garantir escalação ou titularidade.
- Previsto: expectativa ou projeção, identificada como tal na ficha.
- Negociação/proposta: conversas ou oferta, sem acordo confirmado.
- Interesse: consulta ou desejo de contratar/renovar.

A data de consulta de contratos é identificada como consulta, não como data de anúncio. Na visão de 2027, Agente Livre substitui Sem contrato e vínculos com término até 2026. Prazos desconhecidos não são presumidos livres.

Dados: data/rumors-2027.json. Revisão dos oito times e histórico das correções: data/team-audit-2027.json. Correções de jogadores: data/market-player-updates.json. Os dados são incorporados no HTML para uso offline, sem atualização automática.
