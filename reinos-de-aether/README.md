# Reinos de Aether

MMORPG 3D de navegador (protótipo), feito com three.js.

- Arquivo único: `index.html`
- Multiplayer em tempo real via Supabase Realtime (presença dos jogadores e chat). A chave usada no código é a chave pública (anon) do projeto, feita para ficar no navegador.
- Monstros compartilhados: o jogador há mais tempo no mundo é o anfitrião e simula a IA dos monstros; os outros enviam seus golpes a ele. Quem causou dano recebe XP, ouro e loot próprio. Se o anfitrião sair, o próximo assume.
- Itens e progresso ficam salvos no navegador de cada jogador.

Para jogar localmente, basta abrir `index.html` num servidor estático.
