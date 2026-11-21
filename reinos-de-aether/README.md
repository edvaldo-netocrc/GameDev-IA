# Reinos de Aether

MMORPG 3D de navegador (protótipo), feito com three.js.

- `index.html` (o jogo) + pasta `models/` (personagens 3D animados KayKit, licença CC0 — ver `models/CREDITOS.txt`)
- Gráficos: céu atmosférico, cores com tone mapping ACES, sombras suaves, grama e folhas com vento, água com reflexo; qualidade Alto/Médio/Baixo na tela inicial
- Multiplayer em tempo real via Supabase Realtime (presença dos jogadores e chat). A chave usada no código é a chave pública (anon) do projeto, feita para ficar no navegador.
- Monstros compartilhados: o jogador há mais tempo no mundo é o anfitrião e simula a IA dos monstros; os outros enviam seus golpes a ele. Quem causou dano recebe XP, ouro e loot próprio. Se o anfitrião sair, o próximo assume.
- Regiões: Vila de Aether (segura), Campos Verdes, Floresta dos Lobos, Terras de Pedra, Desfiladeiro dos Orcs (oeste, Nv 11–15, chefe Ignarok, o Dragão) e Masmorra Esquecida (chefe Lich Morvath).
- Missões: o Capitão Aldric (o ! dourado na vila) dá uma campanha de 9 missões, das Geleias até o dragão Ignarok, com XP, ouro, poções e itens. Depois dela, caçadas repetíveis.
- Habilidade suprema no nível 10 (tecla 3): Fúria do Guerreiro (+50% ataque, −35% dano recebido) e Chuva de Meteoros do Mago.
- Pergaminho de Retorno (tecla R) volta à vila em 3 s; mapa-múndi na tecla M (som passou para a tecla N).
- Refinamento no Ferreiro Borin: itens equipados de +1 a +7 (+12% nos atributos por nível; chance cai a cada nível e, de +5 em diante, a falha volta 1 nível).
- Perfil (tecla P): 13 conquistas que liberam títulos exibidos acima do nome (visíveis no multiplayer) e ranking online do servidor (Top 10 por nível e XP, gravado no Supabase pela função `submit_score`).
- Auto-caça (H) e auto-loot (L), com painel de opções (O): raio de caça, raridade mínima para coletar, poção automática e uso de habilidade.
- Sons gravados (Kenney e OpenGameArt, CC0) com sons sintetizados no navegador (WebAudio) como reserva; volume nas opções e tecla N para ligar/desligar.
- Itens e progresso ficam salvos no navegador de cada jogador.

Para jogar localmente, basta abrir `index.html` num servidor estático.
