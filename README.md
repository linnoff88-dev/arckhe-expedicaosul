**PT** Â· [EN](README.en.md) Â· [ES](README.es.md)

# ExpediÃ§Ã£o Sul â€” animaÃ§Ãµes de trajeto

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![ExpediÃ§Ã£o Sul](guia/assets/banner.jpg)](https://inematds.github.io/expedicaosul/guia/)

TrÃªs viagens de carro pelos Andes, pelo pampa e pelo litoral do Uruguai, transformadas em **animaÃ§Ãµes de mapa**:
satÃ©lite real, o veÃ­culo andando na estrada verdadeira, painel com km, altitude, paÃ­s e estrada, e embaixo um
**diÃ¡rio de bordo** com foto real e um fato verificado de cada lugar por onde se passa. Cada viagem sai em
**9:16** (Reels/Shorts/WhatsApp) e **16:9** (YouTube/TV), 60 fps no master.

Feito com [HyperFrames](https://hyperframes.heygen.com) (HTML â†’ vÃ­deo) e Claude Code, em 24/09/2026.

## ðŸ“– Guia de uso

Guia completo (os 8 vÃ­deos + como o motor de rota funciona + passo a passo): **https://inematds.github.io/expedicaosul/guia/**

---

## Os vÃ­deos

| Viagem | VeÃ­culo | DistÃ¢ncia | DuraÃ§Ã£o | 9:16 | 16:9 |
|---|---|---|---|---|---|
| **Hua Hum: nosso plano Ã— nossa aventura** â€” o plano e o que aconteceu (estrada interrompida, fronteira fechada), com as fotos da viagem | VW Taos + Land Rover Defender 110 | 54,3 km planejados Â· â‰ˆ85 km rodados | 174 s | [ver](videos/huahum-plano-e-aventura-9x16.mp4) | [ver](videos/huahum-plano-e-aventura-16x9.mp4) |
| **Hua Hum** â€” San MartÃ­n de los Andes (AR) â–¸ Pirihueico (CL) | Hyundai Tucson + Land Rover Defender 110 | 54,3 km | 74,4 s | [assistir](videos/trajeto-hua-hum-9x16.mp4) | [assistir](videos/trajeto-hua-hum-16x9.mp4) |
| **A volta** â€” San MartÃ­n de los Andes â–¸ Canela (RS) | Defender 110 | 2.797 km | 113,6 s | [assistir](videos/volta-defender-9x16.mp4) | [assistir](videos/volta-defender-16x9.mp4) |
| **A ida** â€” Canela â–¸ San MartÃ­n de los Andes | Defender 110 | 2.882 km | 95,7 s | [assistir](videos/ida-defender-9x16.mp4) | [assistir](videos/ida-defender-16x9.mp4) |

<table>
<tr>
<td align="center"><b>Hua Hum</b><br><video src="videos/trajeto-hua-hum-9x16.mp4" poster="videos/trajeto-hua-hum-9x16.jpg" width="240" controls preload="none"></video></td>
<td align="center"><b>A volta</b><br><video src="videos/volta-defender-9x16.mp4" poster="videos/volta-defender-9x16.jpg" width="240" controls preload="none"></video></td>
<td align="center"><b>A ida</b><br><video src="videos/ida-defender-9x16.mp4" poster="videos/ida-defender-9x16.jpg" width="240" controls preload="none"></video></td>
</tr>
</table>

> Os arquivos deste repositÃ³rio sÃ£o a versÃ£o web (30 fps, ~43 MB). Os masters 60 fps (300+ MB) ficam fora do git.

### Hua Hum (54,3 km, 1 fronteira)
San MartÃ­n de los Andes â†’ Lago LÃ¡car â†’ ponto mais alto do dia (1.038 m, km 16,5, na RP48 de ripio) â†’ Playa de Yuco â†’
Lago NonthuÃ© â†’ Puerto Hua Hum â†’ **Paso Hua Hum** (fronteira AR â–¸ CL, km 43,7) â†’ Ruta CH-203 â†’ Puerto Pirehueico.

### A volta (2.797 km, 3 paÃ­ses)
San MartÃ­n de los Andes â†’ descida dos Andes pela RN 237/RN 22 â†’ RÃ­o Colorado ("adeus, PatagÃ´nia") â†’ BahÃ­a Blanca â†’
Azul â†’ Moreno â†’ Buenos Aires â†’ **balsa Colonia Express pelo RÃ­o de la Plata (51 km, 1h15)** â†’ Colonia del Sacramento â†’
Paso de los Toros â†’ **Fronteira da Paz** (Rivera/Sant'Ana do Livramento) â†’ BR-158/BR-290 â†’ Porto Alegre â†’ Canela.

### A ida (2.882 km, 3 paÃ­ses)
Canela â†’ BR-471 pelo Taim â†’ **ChuÃ­/Chuy** (BR â–¸ UY) â†’ La Paloma â†’ Pueblo GarzÃ³n (a antiga estaÃ§Ã£o de trem) â†’
Punta del Este â†’ San Carlos â†’ Colonia â†’ **balsa atÃ© Buenos Aires** â†’ Moreno â†’ RN 5 â†’ Santa Rosa â†’ RÃ­o Colorado em
25 de Mayo ("olÃ¡, PatagÃ´nia") â†’ San MartÃ­n de los Andes.

---

## Como foi feito

Um Ãºnico **motor de animaÃ§Ã£o de rota** (HTML + GSAP, renderizado pelo HyperFrames) lÃª trÃªs arquivos de dados e desenha
tudo a partir de **um relÃ³gio sÃ³** â€” posiÃ§Ã£o do carro, cÃ¢mera, linha percorrida, pinos, HUD, trilho de altitude e cards
saem da mesma funÃ§Ã£o do tempo, entÃ£o nada fica fora de sincronia.

| Camada | Fonte |
|---|---|
| Rota (estrada) | OSRM, por pernas entre as paradas do link do Google Maps |
| Balsa | linha OSM da **Colonia Express** (Buenos Aires â†” Colonia), com a duraÃ§Ã£o marcada no OSM |
| SatÃ©lite | Esri World Imagery â€” visÃ£o geral (z7), corredor (z8) e recortes em alta (z10/z12) em cada parada; cada recorte sÃ³ aparece quando cobre o quadro inteiro |
| Lagos (Hua Hum) | repintados com os polÃ­gonos de Ã¡gua do OSM (tira manchas de reflexo do mosaico) |
| Fronteiras | OSM (admin_level=2) nas cidades de fronteira; Natural Earth na escala continental |
| Altitude | SRTM 30 m via OpenTopoData (trilho de altitude, HUD e cards de dados) |
| Fatos dos cards | Wikipedia (ES/PT/EN), cada frase com fonte salva em `*/data/facts/` |
| Fotos | Wikimedia Commons, conferidas por categoria/local, com autor e licenÃ§a |
| VeÃ­culos e balsa vistos de cima | gerados no flux2-klein local e recortados (chroma key) |
| Trilhas | geradas (Lyria 3 Pro) e **analisadas** (BPM, entrada do groove, silÃªncio): o carro larga quando a batida entra, a balsa atravessa no trecho calmo e o carimbo de fronteira cai no retorno da mÃºsica |

### Estrutura

```
trajeto-hua-hum/        vÃ­deo Hua Hum (motor v1, dois carros) + data/ (scripts e dados)
trajeto-hua-hum-16x9/   variante 16:9
huahum-real/            Hua Hum "nosso plano Ã— nossa aventura": 3 quadros (mapa geral fixo, detalhado, fotos da viagem),
                        agenda por carro com ida/volta; data/fotos.txt â†’ build_fotos.py; make_16x9.py prÃ³prio
huahum-real-16x9/       variante 16:9 (gerada por huahum-real/make_16x9.py)
volta-defender/         motor genÃ©rico de rota longa + assets/trip.js da volta
volta-defender-16x9/    variante 16:9 (assets por link simbÃ³lico)
ida-defender/           mesmo motor + assets/trip.js da ida
ida-defender-16x9/
make_16x9.py            gera a variante 16:9 trocando sÃ³ os blocos de layout
render_share.sh         render 60 fps + versÃ£o de compartilhar (-14 LUFS)
tg_encode.sh            versÃ£o â‰¤ 44 MB (Telegram / web)
videos/                 os 8 vÃ­deos (versÃ£o web) + capas
FALHAS.md               changelog de falhas corrigidas
```

### Nova viagem com o motor

1. `data/`: rotas OSRM por pernas + `build_route2.py trip.json` (rota Ãºnica, balsa, fronteira, altitude, paradas).
2. `build_tiles.py route_full.json ../assets` (satÃ©lite), `photos_search.py` / `photos_get.py` (fotos + crÃ©ditos), `fetch_facts.py` (fatos).
3. Escrever `assets/trip.js`: agenda de chegada/saÃ­da por parada (casada com a mÃºsica â€” `beat.py` mede BPM e fase), cards, carimbos, rÃ³tulos.
4. `npx hyperframes check` â†’ `python3 make_16x9.py <proj> <proj>-16x9` â†’ `render_share.sh`.

---

## EstatÃ­sticas de produÃ§Ã£o

Medido nos logs da sessÃ£o do Claude Code (tokens por chamada), nÃ£o estimado. Custo em **dÃ³lar equivalente de API** pela tabela
oficial (Opus 5.5: US$ 4 entrada / 20 saÃ­da / 0,20 leitura de cache / 8 escrita de cache 1 h, por milhÃ£o de tokens;
Haiku 4.5: 1 / 5 / 0,10 / 2). Quem usa o Claude Code por assinatura nÃ£o paga esse valor por uso â€” serve para comparar.

### Custo e tempo por vÃ­deo

| VÃ­deo | Tempo ativo do agente | Chamadas | Custo IA (US$) | CrÃ©ditos Magnific | Render local |
|---|---|---|---|---|---|
| Hua Hum 9:16 | 55 min | 89 | **13,12** | 190 | 3 Ã— ~1m50 |
| Hua Hum 16:9 | ~5 min | 8 | **1,07** | â€” | 1m44 |
| A volta (9:16 + 16:9) | 38,5 min | 53 + 5 subagentes | **15,18** | 180 | 4 Ã— ~2m40 |
| A ida (9:16 + 16:9) | 24,4 min | 37 + 4 subagentes | **6,85** | 160 | 2 Ã— ~2m15 |
| **Total** | **~2h03** | **187 + 9** | **36,22** | **530** | ~24 min |

ComposiÃ§Ã£o do custo: agente principal (Opus 5.5) US$ 30,97 Â· revisor (3 consultas, Opus 5.5) US$ 4,32 Â·
subagentes (Haiku 4.5, tarefas mecÃ¢nicas: baixar satÃ©lite e fotos, gerar sprite, renderizar) US$ 0,93.
Custo zero: geraÃ§Ã£o de imagem local (flux2-klein, ~2 min de GPU) e todos os renders (HyperFrames local).
CrÃ©ditos Magnific: 3 trilhas Ã— 160 + efeitos (whoosh, carimbo, buzina de navio).

### Volume de cache (tokens)

| VÃ­deo | Lidos do cache | Gravados no cache (1 h) | Entrada sem cache | SaÃ­da | Acerto de cache |
|---|---|---|---|---|---|
| Hua Hum 9:16 | 24,64 M | 383 mil | 538 mil (revisor) | 136 mil + 14 mil (revisor) | 98,5% |
| Hua Hum 16:9 | 3,33 M | 20 mil | â€” | 12 mil | 99,4% |
| A volta | 29,59 M + 1,27 M (subag.) | 588 mil + 319 mil (subag.) | 439 mil (revisor) | 105 mil + 15 mil | 98,0% |
| A ida | 23,20 M + 0,63 M (subag.) | 112 mil + 224 mil (subag.) | â€” | 48 mil + 4 mil | 99,5% |

Leitura dos nÃºmeros:
- **98â€“99,5% da entrada veio do cache** â€” Ã© o que mantÃ©m o custo baixo apesar de ~85 M tokens lidos.
- **O revisor Ã© caro por chamada**: manda a conversa inteira sem cache (~300â€“540 mil tokens por consulta).
- **O 16:9 quase nÃ£o custa** (US$ 1,07 no Hua Hum; na volta e na ida Ã© sÃ³ troca de layout + render).
- **A ida custou menos da metade da volta**: a volta pagou a construÃ§Ã£o do motor genÃ©rico, a ida sÃ³ reaproveitou.
- Uma pausa longa derruba o cache (validade de 1 h): uma pergunta feita 8 h depois regravou ~760 mil tokens (US$ 7,41).

---

## CrÃ©ditos

**Mapa e dados:** Esri World Imagery (Esri, Maxar, Earthstar Geographics) Â· Â© colaboradores do OpenStreetMap (ODbL) Â·
Natural Earth Â· OSRM Â· SRTM 30 m via OpenTopoData Â· Wikipedia (ES/PT/EN).

**Fotos (Wikimedia Commons):**
- Hua Hum â€” Albasmalko (dom. pÃºblico) Â· Marco Antonio Correa Flores (CC BY-SA 4.0) Â· Falk2 (CC BY-SA 4.0) Â· Gervacio Rosales (CC BY 3.0) Â· Manueldutruel (CC BY-SA 4.0).
- A volta â€” Albasmalko Â· Alvaro Errandonea (CC BY 3.0) Â· Juan Corral / Municipalidad de BahÃ­a Blanca (CC BY 2.5 AR) Â· Elquache (CC BY-SA 3.0) Â· Walteriot (CC BY-SA 3.0) Â· NASA JSC Earth Sciences (dom. pÃºblico) Â· Roxyuru (CC BY-SA 3.0) Â· Diego Delso (CC BY-SA 3.0) Â· bullit (CC BY 3.0) Â· Zeroth (CC BY-SA 4.0) Â· Mx. Granger (CC0) Â· Fernando da Rosa (CC BY-SA 3.0) Â· Ricardo AndrÃ© Frantz (CC BY-SA 3.0) Â· Cristine Denardi Huff (CC BY-SA 4.0) Â· Rosanetur (CC BY 2.0) Â· Fernando Schultz Aldado (dom. pÃºblico).
- A ida â€” Rosanetur Â· Fernando Schultz Aldado Â· GiÃ¡como Luiz Mancini (CC BY-SA 4.0) Â· John Seb Barber (CC BY 2.0) Â· Granjuanlll (CC BY-SA 3.0) Â· Jimmy Baikovicius (CC BY-SA 2.0) Â· Eduardo.terian (CC BY-SA 3.0) Â· MarÃ­a Cecilia (CC0) Â· mriaco (CC BY 3.0) Â· NaBUru38 (CC BY-SA 4.0) Â· Diego Delso Â· bullit Â· Roxyuru Â· NASA JSC Â· Walteriot Â· Juanedc (CC BY 2.0) Â· Jmmuguerza (CC BY-SA 4.0) Â· Silvio omar (CC BY-SA 4.0) Â· Albasmalko Â· Marco Antonio Correa Flores.

**Gerado por IA:** veÃ­culos e balsa vistos de cima (flux2-klein) Â· trilhas e efeitos sonoros (Magnific â€” Lyria 3 Pro / ElevenLabs).

ConteÃºdo aberto do [INEMA.CLUB](https://inema.club).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>