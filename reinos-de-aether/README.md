# Reinos de Aether

MMORPG 3D de navegador (protótipo), feito com three.js.

- `index.html` (o jogo) + pasta `models/` (personagens 3D animados KayKit, licença CC0 — ver `models/CREDITOS.txt`)
- Gráficos: céu atmosférico, cores com tone mapping ACES, sombras suaves, grama e folhas com vento, água com reflexo; qualidade Alto/Médio/Baixo na tela inicial
- Cenário modelado no Blender (`models/env/`): tendas, totens, paliçadas e fogueiras no acampamento orc; árvores retorcidas, cogumelos que brilham à noite e a cabana da bruxa sobre palafitas no pântano; pilares de obsidiana com runas e braseiros na Arena do Azgaroth; na Masmorra Esquecida, colunas góticas com caveiras, o trono do Lich com cristais, sarcófagos com runas, jaulas penduradas, candelabros e ossadas, além de um portal de pedra com arco na entrada; baús de tesouro no loot; pedras com musgo, arbustos floridos e flores do campo (instanciados para rodar leve no celular).
- Multiplayer em tempo real via Supabase Realtime (presença dos jogadores e chat). A chave usada no código é a chave pública (anon) do projeto, feita para ficar no navegador.
- Monstros compartilhados: o jogador há mais tempo no mundo é o anfitrião e simula a IA dos monstros; os outros enviam seus golpes a ele. Quem causou dano recebe XP, ouro e loot próprio. Se o anfitrião sair, o próximo assume.
- Regiões: Vila de Aether (segura), Campos Verdes, Floresta dos Lobos, Terras de Pedra, Desfiladeiro dos Orcs (oeste, Nv 11–15, chefe Ignarok, o Dragão), Pântano Assombrado (sul, Nv 16–22, chefe Rei Fungorr) e Masmorra Esquecida (chefe Lich Morvath).
- Mapas novos por portais (arcos de pedra logo ao norte da vila): ❄️ Picos Gelados (Nv 20–26: Elemental de Gelo, Urso Glacial e o chefe Kryos, a Serpe Glacial, que faz chover gelo) e 🌋 Caldeira Ardente (Nv 26–32: Elemental de Magma, Salamandra de Fogo e o chefe Vulkar, o Senhor das Chamas, que faz chover meteoros). Rios de lava queimam quem pisa. Cada mapa tem céu, neve ou brasas, minimapa próprio e portal de volta à vila. Monstros e cenário modelados no Blender.
- Missões: o Capitão Aldric (o ! dourado na vila) dá uma campanha de 12 missões, das Geleias até o dragão Ignarok, com XP, ouro, poções e itens. Depois dela, caçadas repetíveis.
- Habilidade suprema no nível 10 (tecla 3): Fúria do Guerreiro (+50% ataque, −35% dano recebido) e Chuva de Meteoros do Mago.
- Pergaminho de Retorno (tecla R) volta à vila em 3 s; mapa-múndi na tecla M (som passou para a tecla N).
- Venda no Ferreiro Borin (aba 💰 Vender): marque itens da mochila um a um ou use a venda rápida por raridade (Comuns, Incomuns, Raros). Itens melhores que o equipado (⬆) e refinados ficam fora da venda rápida; vender épicos, refinados ou melhores pede confirmação. Itens refinados valem +50% por nível de refino.
- Refinamento no Ferreiro Borin: itens equipados de +1 a +7 (+12% nos atributos por nível; chance cai a cada nível e, de +5 em diante, a falha volta 1 nível).
- Perfil (tecla P): 13 conquistas que liberam títulos exibidos acima do nome (visíveis no multiplayer) e ranking online do servidor (Top 10 por nível e XP, gravado no Supabase pela função `submit_score`).
- Chefe mundial: Azgaroth, o Senhor Demônio, desperta na Arena (norte das Terras de Pedra) por 12 minutos a cada meia hora (relógio igual para todos); recompensa todos que ajudarem.
- Grupo (Perfil → Grupo): até 4 jogadores; cada abate dá 60% do XP aos membros a até 70 m e conta para as missões de todos.
- Classes: Guerreiro (Golpe Giratório / Fúria), Mago (Explosão Arcana / Chuva de Meteoros) e Bárbaro (Investida / Sede de Sangue: ataques mais rápidos e roubo de vida).
- Salvamento na nuvem: o herói é salvo no Supabase (funções `save_char`/`load_char`, protegidas por chave secreta). Em Opções há um código para continuar o mesmo herói em outro aparelho.
- Recompensa diária: 7 dias seguidos com prêmios crescentes (ouro, poções, pergaminhos, itens raro e épico).
- Celular (Android/iPhone): layout próprio de toque em pé e deitado (joystick à esquerda, botões de combate à direita, menu de ícones no alto), botão de tela cheia e instalação como app ("Adicionar à tela inicial" abre em tela cheia, deitado).
- Amigos e sussurros (Perfil → Amigos): lista salva no herói, aviso quando um amigo entra, mensagens privadas com /s Nome mensagem e /r para responder.
- Emotes (tecla G ou /comemorar, /girar, /magia, /morto, /susto): gestos animados que todos veem. /ajuda lista os comandos.
- Mascotes (loja do Ferreiro Borin): Geleia Mascote (busca baús, +10% ouro), Filhote de Lobo (+10% XP) e Dragãozinho (voa, busca baús, +10% ouro, +5% ataque; liberado após derrotar Ignarok). Visíveis no multiplayer.
- Duelos PvP (Perfil → Grupo → ⚔️ ou /duelo Nome): 1x1 fora da vila, contagem de 3 s, 60% do dano normal, termina em 10% da vida (ninguém morre) ou em 90 s; vitórias contam para a conquista Duelista.
- 8 classes do Priston Tale, cada uma com modelo 3D, arma própria, habilidade (2) e suprema (3, nível 10): 🛡️ Cavaleiro (espada e escudo — antigo Guerreiro), 🪓 Guerreiro (machado — antigo Bárbaro), ⚙️ Mecânico (martelo, escudo, Bomba Mecânica e Armadura Metálica), 🔱 Pikeman (lança, Lança Terrestre e Tornado), 🏹 Arqueira (arco, Flecha Múltipla e Chuva de Flechas), 🎯 Atalanta (azagaias, Lança Tripla e Tempestade de Raios), 🔮 Mago e ✨ Sacerdotisa (Cura Sagrada para o grupo e Raios Celestiais). Os 5 modelos KayKit compartilham esqueleto e uma biblioteca de 22 animações (models/rogue.glb). O registro das classes (CDEF no código) permite trocar o modelo de uma classe sem mexer no resto.
- Gerações de equipamento (modeladas no Blender): itens de nível 1 são de ferro e couro, de nível 8 de aço, de nível 18 de mithril com runas brilhantes e de nível 25 de ouro de dragão com brasas. Cada geração tem espada, escudo, cajado, machado, elmo do guerreiro, chapéu do mago, elmo com chifres do bárbaro, armadura de placas, manto do mago, peles do bárbaro e a joia do anel, que flutua ao redor do herói. Equipar qualquer peça muda o visual na hora (e os outros jogadores veem).
- Visual do equipamento: a roupa (placas, couro ou manto), o chapéu (elmo, capuz de urso, chapéu de mago) e a arma (espada e escudo, lâminas gêmeas, espadão, machados, cajado, varinha e livro) mudam conforme o item equipado; a raridade muda a cor (bronze, aço, dourado) e itens raros/épicos ou +5 brilham. Visível no multiplayer.
- Troca de itens (Perfil → Grupo → 🔁 ou /trocar Nome): até 4 itens + ouro de cada lado, a até 12 m; os dois confirmam e qualquer mudança desfaz as confirmações; itens recebidos são validados.
- Menu do jogador: clicar/tocar em outro jogador (ou no nome dele) abre Convidar para o grupo, Trocar itens, Desafiar para duelo, Sussurrar e Adicionar amigo.
- Montaria (tecla V): Lobo Branco, +70% de velocidade; atacar ou levar dano desmonta.
- Auto-caça (H) e auto-loot (L), com painel de opções (O): raio de caça, raridade mínima para coletar, poção automática e uso de habilidade.
- Sons gravados (Kenney e OpenGameArt, CC0) com sons sintetizados no navegador (WebAudio) como reserva; volume nas opções e tecla N para ligar/desligar.
- Itens e progresso ficam salvos no navegador de cada jogador.

Para jogar localmente, basta abrir `index.html` num servidor estático.
