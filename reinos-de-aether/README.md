# Reinos de Aether

MMORPG 3D de navegador (protótipo), feito com three.js.

- `index.html` (o jogo) + pasta `models/` (personagens 3D animados KayKit, licença CC0 — ver `models/CREDITOS.txt`)
- Gráficos: céu atmosférico, cores com tone mapping ACES, sombras suaves, grama e folhas com vento, água com reflexo; qualidade Alto/Médio/Baixo na tela inicial
- Multiplayer em tempo real via Supabase Realtime (presença dos jogadores e chat). A chave usada no código é a chave pública (anon) do projeto, feita para ficar no navegador.
- Monstros compartilhados: o jogador há mais tempo no mundo é o anfitrião e simula a IA dos monstros; os outros enviam seus golpes a ele. Quem causou dano recebe XP, ouro e loot próprio. Se o anfitrião sair, o próximo assume.
- Itens e progresso ficam salvos no navegador de cada jogador.

Para jogar localmente, basta abrir `index.html` num servidor estático.
