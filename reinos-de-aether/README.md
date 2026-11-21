# Reinos de Aether

MMORPG 3D de navegador (protótipo), feito com three.js.

- `index.html` (o jogo) + pasta `models/` (personagens 3D animados KayKit, licença CC0 — ver `models/CREDITOS.txt`)
- Gráficos: céu atmosférico, cores com tone mapping ACES, sombras suaves, grama e folhas com vento, água com reflexo; qualidade Alto/Médio/Baixo na tela inicial
- Multiplayer em tempo real via Supabase Realtime (presença dos jogadores e chat). A chave usada no código é a chave pública (anon) do projeto, feita para ficar no navegador.
- Monstros compartilhados: o jogador há mais tempo no mundo é o anfitrião e simula a IA dos monstros; os outros enviam seus golpes a ele. Quem causou dano recebe XP, ouro e loot próprio. Se o anfitrião sair, o próximo assume.
- Regiões: Vila de Aether (segura), Campos Verdes, Floresta dos Lobos, Terras de Pedra, Desfiladeiro dos Orcs (oeste, Nv 11–15, chefe Ignarok, o Dragão) e Masmorra Esquecida (chefe Lich Morvath).
- Auto-caça (H) e auto-loot (L), com painel de opções (O): raio de caça, raridade mínima para coletar, poção automática e uso de habilidade.
- Efeitos sonoros e sons de ambiente gerados no navegador (WebAudio), com volume nas opções e tecla M.
- Itens e progresso ficam salvos no navegador de cada jogador.

Para jogar localmente, basta abrir `index.html` num servidor estático.
