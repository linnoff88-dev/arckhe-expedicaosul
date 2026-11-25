**PT** êÂ· [EN](README.en.md) êÂ· [ES](README.es.md)

# ExpediêÂ§êÂ£o Sul ê¢â¬â animaêÂ§êÂµes de trajeto

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="48" />
  <p><strong>Arckhé AI</strong></p>
</div>


[![ExpediêÂ§êÂ£o Sul](guia/assets/banner.jpg)](https://linnoff88-dev.github.io/

TrêÂªs viagens de carro pelos Andes, pelo pampa e pelo litoral do Uruguai, transformadas em **animaêÂ§êÂµes de mapa**:
satêÂ©lite real, o veêÂ­culo andando na estrada verdadeira, painel com km, altitude, paêÂ­s e estrada, e embaixo um
**diêÂ¡rio de bordo** com foto real e um fato verificado de cada lugar por onde se passa. Cada viagem sai em
**9:16** (Reels/Shorts/WhatsApp) e **16:9** (YouTube/TV), 60 fps no master.

Feito com [HyperFrames](https://hyperframes.heygen.com) (HTML ê¢â â vêÂ­deo) e Claude Code, em 24/09/2026.

## ê°Å¸ââ Guia de uso

Guia completo (os 8 vêÂ­deos + como o motor de rota funciona + passo a passo): **https://linnoff88-dev.github.io/

---

## Os vêÂ­deos

| Viagem | VeêÂ­culo | DistêÂ¢ncia | DuraêÂ§êÂ£o | 9:16 | 16:9 |
|---|---|---|---|---|---|
| **Hua Hum: nosso plano êâ nossa aventura** ê¢â¬â o plano e o que aconteceu (estrada interrompida, fronteira fechada), com as fotos da viagem | VW Taos + Land Rover Defender 110 | 54,3 km planejados êÂ· ê¢â°Ë85 km rodados | 174 s | [ver](videos/huahum-plano-e-aventura-9x16.mp4) | [ver](videos/huahum-plano-e-aventura-16x9.mp4) |
| **Hua Hum** ê¢â¬â San MartêÂ­n de los Andes (AR) ê¢âÂ¸ Pirihueico (CL) | Hyundai Tucson + Land Rover Defender 110 | 54,3 km | 74,4 s | [assistir](videos/trajeto-hua-hum-9x16.mp4) | [assistir](videos/trajeto-hua-hum-16x9.mp4) |
| **A volta** ê¢â¬â San MartêÂ­n de los Andes ê¢âÂ¸ Canela (RS) | Defender 110 | 2.797 km | 113,6 s | [assistir](videos/volta-defender-9x16.mp4) | [assistir](videos/volta-defender-16x9.mp4) |
| **A ida** ê¢â¬â Canela ê¢âÂ¸ San MartêÂ­n de los Andes | Defender 110 | 2.882 km | 95,7 s | [assistir](videos/ida-defender-9x16.mp4) | [assistir](videos/ida-defender-16x9.mp4) |

<table>
<tr>
<td align="center"><b>Hua Hum</b><br><video src="videos/trajeto-hua-hum-9x16.mp4" poster="videos/trajeto-hua-hum-9x16.jpg" width="240" controls preload="none"></video></td>
<td align="center"><b>A volta</b><br><video src="videos/volta-defender-9x16.mp4" poster="videos/volta-defender-9x16.jpg" width="240" controls preload="none"></video></td>
<td align="center"><b>A ida</b><br><video src="videos/ida-defender-9x16.mp4" poster="videos/ida-defender-9x16.jpg" width="240" controls preload="none"></video></td>
</tr>
</table>

> Os arquivos deste repositêÂ³rio sêÂ£o a versêÂ£o web (30 fps, ~43 MB). Os masters 60 fps (300+ MB) ficam fora do git.

### Hua Hum (54,3 km, 1 fronteira)
San MartêÂ­n de los Andes ê¢â â Lago LêÂ¡car ê¢â â ponto mais alto do dia (1.038 m, km 16,5, na RP48 de ripio) ê¢â â Playa de Yuco ê¢â â
Lago NonthuêÂ© ê¢â â Puerto Hua Hum ê¢â â **Paso Hua Hum** (fronteira AR ê¢âÂ¸ CL, km 43,7) ê¢â â Ruta CH-203 ê¢â â Puerto Pirehueico.

### A volta (2.797 km, 3 paêÂ­ses)
San MartêÂ­n de los Andes ê¢â â descida dos Andes pela RN 237/RN 22 ê¢â â RêÂ­o Colorado ("adeus, PatagêÂ´nia") ê¢â â BahêÂ­a Blanca ê¢â â
Azul ê¢â â Moreno ê¢â â Buenos Aires ê¢â â **balsa Colonia Express pelo RêÂ­o de la Plata (51 km, 1h15)** ê¢â â Colonia del Sacramento ê¢â â
Paso de los Toros ê¢â â **Fronteira da Paz** (Rivera/Sant'Ana do Livramento) ê¢â â BR-158/BR-290 ê¢â â Porto Alegre ê¢â â Canela.

### A ida (2.882 km, 3 paêÂ­ses)
Canela ê¢â â BR-471 pelo Taim ê¢â â **ChuêÂ­/Chuy** (BR ê¢âÂ¸ UY) ê¢â â La Paloma ê¢â â Pueblo GarzêÂ³n (a antiga estaêÂ§êÂ£o de trem) ê¢â â
Punta del Este ê¢â â San Carlos ê¢â â Colonia ê¢â â **balsa atêÂ© Buenos Aires** ê¢â â Moreno ê¢â â RN 5 ê¢â â Santa Rosa ê¢â â RêÂ­o Colorado em
25 de Mayo ("olêÂ¡, PatagêÂ´nia") ê¢â â San MartêÂ­n de los Andes.

---

## Como foi feito

Um êÂºnico **motor de animaêÂ§êÂ£o de rota** (HTML + GSAP, renderizado pelo HyperFrames) lêÂª trêÂªs arquivos de dados e desenha
tudo a partir de **um relêÂ³gio sêÂ³** ê¢â¬â posiêÂ§êÂ£o do carro, cêÂ¢mera, linha percorrida, pinos, HUD, trilho de altitude e cards
saem da mesma funêÂ§êÂ£o do tempo, entêÂ£o nada fica fora de sincronia.

| Camada | Fonte |
|---|---|
| Rota (estrada) | OSRM, por pernas entre as paradas do link do Google Maps |
| Balsa | linha OSM da **Colonia Express** (Buenos Aires ê¢â â Colonia), com a duraêÂ§êÂ£o marcada no OSM |
| SatêÂ©lite | Esri World Imagery ê¢â¬â visêÂ£o geral (z7), corredor (z8) e recortes em alta (z10/z12) em cada parada; cada recorte sêÂ³ aparece quando cobre o quadro inteiro |
| Lagos (Hua Hum) | repintados com os polêÂ­gonos de êÂ¡gua do OSM (tira manchas de reflexo do mosaico) |
| Fronteiras | OSM (admin_level=2) nas cidades de fronteira; Natural Earth na escala continental |
| Altitude | SRTM 30 m via OpenTopoData (trilho de altitude, HUD e cards de dados) |
| Fatos dos cards | Wikipedia (ES/PT/EN), cada frase com fonte salva em `*/data/facts/` |
| Fotos | Wikimedia Commons, conferidas por categoria/local, com autor e licenêÂ§a |
| VeêÂ­culos e balsa vistos de cima | gerados no flux2-klein local e recortados (chroma key) |
| Trilhas | geradas (Lyria 3 Pro) e **analisadas** (BPM, entrada do groove, silêÂªncio): o carro larga quando a batida entra, a balsa atravessa no trecho calmo e o carimbo de fronteira cai no retorno da mêÂºsica |

### Estrutura

```
trajeto-hua-hum/        vêÂ­deo Hua Hum (motor v1, dois carros) + data/ (scripts e dados)
trajeto-hua-hum-16x9/   variante 16:9
huahum-real/            Hua Hum "nosso plano êâ nossa aventura": 3 quadros (mapa geral fixo, detalhado, fotos da viagem),
                        agenda por carro com ida/volta; data/fotos.txt ê¢â â build_fotos.py; make_16x9.py prêÂ³prio
huahum-real-16x9/       variante 16:9 (gerada por huahum-real/make_16x9.py)
volta-defender/         motor genêÂ©rico de rota longa + assets/trip.js da volta
volta-defender-16x9/    variante 16:9 (assets por link simbêÂ³lico)
ida-defender/           mesmo motor + assets/trip.js da ida
ida-defender-16x9/
make_16x9.py            gera a variante 16:9 trocando sêÂ³ os blocos de layout
render_share.sh         render 60 fps + versêÂ£o de compartilhar (-14 LUFS)
tg_encode.sh            versêÂ£o ê¢â°Â¤ 44 MB (Telegram / web)
videos/                 os 8 vêÂ­deos (versêÂ£o web) + capas
FALHAS.md               changelog de falhas corrigidas
```

### Nova viagem com o motor

1. `data/`: rotas OSRM por pernas + `build_route2.py trip.json` (rota êÂºnica, balsa, fronteira, altitude, paradas).
2. `build_tiles.py route_full.json ../assets` (satêÂ©lite), `photos_search.py` / `photos_get.py` (fotos + crêÂ©ditos), `fetch_facts.py` (fatos).
3. Escrever `assets/trip.js`: agenda de chegada/saêÂ­da por parada (casada com a mêÂºsica ê¢â¬â `beat.py` mede BPM e fase), cards, carimbos, rêÂ³tulos.
4. `npx hyperframes check` ê¢â â `python3 make_16x9.py <proj> <proj>-16x9` ê¢â â `render_share.sh`.

---

## EstatêÂ­sticas de produêÂ§êÂ£o

Medido nos logs da sessêÂ£o do Claude Code (tokens por chamada), nêÂ£o estimado. Custo em **dêÂ³lar equivalente de API** pela tabela
oficial (Opus 5.5: US$ 4 entrada / 20 saêÂ­da / 0,20 leitura de cache / 8 escrita de cache 1 h, por milhêÂ£o de tokens;
Haiku 4.5: 1 / 5 / 0,10 / 2). Quem usa o Claude Code por assinatura nêÂ£o paga esse valor por uso ê¢â¬â serve para comparar.

### Custo e tempo por vêÂ­deo

| VêÂ­deo | Tempo ativo do agente | Chamadas | Custo IA (US$) | CrêÂ©ditos Magnific | Render local |
|---|---|---|---|---|---|
| Hua Hum 9:16 | 55 min | 89 | **13,12** | 190 | 3 êâ ~1m50 |
| Hua Hum 16:9 | ~5 min | 8 | **1,07** | ê¢â¬â | 1m44 |
| A volta (9:16 + 16:9) | 38,5 min | 53 + 5 subagentes | **15,18** | 180 | 4 êâ ~2m40 |
| A ida (9:16 + 16:9) | 24,4 min | 37 + 4 subagentes | **6,85** | 160 | 2 êâ ~2m15 |
| **Total** | **~2h03** | **187 + 9** | **36,22** | **530** | ~24 min |

ComposiêÂ§êÂ£o do custo: agente principal (Opus 5.5) US$ 30,97 êÂ· revisor (3 consultas, Opus 5.5) US$ 4,32 êÂ·
subagentes (Haiku 4.5, tarefas mecêÂ¢nicas: baixar satêÂ©lite e fotos, gerar sprite, renderizar) US$ 0,93.
Custo zero: geraêÂ§êÂ£o de imagem local (flux2-klein, ~2 min de GPU) e todos os renders (HyperFrames local).
CrêÂ©ditos Magnific: 3 trilhas êâ 160 + efeitos (whoosh, carimbo, buzina de navio).

### Volume de cache (tokens)

| VêÂ­deo | Lidos do cache | Gravados no cache (1 h) | Entrada sem cache | SaêÂ­da | Acerto de cache |
|---|---|---|---|---|---|
| Hua Hum 9:16 | 24,64 M | 383 mil | 538 mil (revisor) | 136 mil + 14 mil (revisor) | 98,5% |
| Hua Hum 16:9 | 3,33 M | 20 mil | ê¢â¬â | 12 mil | 99,4% |
| A volta | 29,59 M + 1,27 M (subag.) | 588 mil + 319 mil (subag.) | 439 mil (revisor) | 105 mil + 15 mil | 98,0% |
| A ida | 23,20 M + 0,63 M (subag.) | 112 mil + 224 mil (subag.) | ê¢â¬â | 48 mil + 4 mil | 99,5% |

Leitura dos nêÂºmeros:
- **98ê¢â¬â99,5% da entrada veio do cache** ê¢â¬â êÂ© o que mantêÂ©m o custo baixo apesar de ~85 M tokens lidos.
- **O revisor êÂ© caro por chamada**: manda a conversa inteira sem cache (~300ê¢â¬â540 mil tokens por consulta).
- **O 16:9 quase nêÂ£o custa** (US$ 1,07 no Hua Hum; na volta e na ida êÂ© sêÂ³ troca de layout + render).
- **A ida custou menos da metade da volta**: a volta pagou a construêÂ§êÂ£o do motor genêÂ©rico, a ida sêÂ³ reaproveitou.
- Uma pausa longa derruba o cache (validade de 1 h): uma pergunta feita 8 h depois regravou ~760 mil tokens (US$ 7,41).

---

## CrêÂ©ditos

**Mapa e dados:** Esri World Imagery (Esri, Maxar, Earthstar Geographics) êÂ· êÂ© colaboradores do OpenStreetMap (ODbL) êÂ·
Natural Earth êÂ· OSRM êÂ· SRTM 30 m via OpenTopoData êÂ· Wikipedia (ES/PT/EN).

**Fotos (Wikimedia Commons):**
- Hua Hum ê¢â¬â Albasmalko (dom. pêÂºblico) êÂ· Marco Antonio Correa Flores (CC BY-SA 4.0) êÂ· Falk2 (CC BY-SA 4.0) êÂ· Gervacio Rosales (CC BY 3.0) êÂ· Manueldutruel (CC BY-SA 4.0).
- A volta ê¢â¬â Albasmalko êÂ· Alvaro Errandonea (CC BY 3.0) êÂ· Juan Corral / Municipalidad de BahêÂ­a Blanca (CC BY 2.5 AR) êÂ· Elquache (CC BY-SA 3.0) êÂ· Walteriot (CC BY-SA 3.0) êÂ· NASA JSC Earth Sciences (dom. pêÂºblico) êÂ· Roxyuru (CC BY-SA 3.0) êÂ· Diego Delso (CC BY-SA 3.0) êÂ· bullit (CC BY 3.0) êÂ· Zeroth (CC BY-SA 4.0) êÂ· Mx. Granger (CC0) êÂ· Fernando da Rosa (CC BY-SA 3.0) êÂ· Ricardo AndrêÂ© Frantz (CC BY-SA 3.0) êÂ· Cristine Denardi Huff (CC BY-SA 4.0) êÂ· Rosanetur (CC BY 2.0) êÂ· Fernando Schultz Aldado (dom. pêÂºblico).
- A ida ê¢â¬â Rosanetur êÂ· Fernando Schultz Aldado êÂ· GiêÂ¡como Luiz Mancini (CC BY-SA 4.0) êÂ· John Seb Barber (CC BY 2.0) êÂ· Granjuanlll (CC BY-SA 3.0) êÂ· Jimmy Baikovicius (CC BY-SA 2.0) êÂ· Eduardo.terian (CC BY-SA 3.0) êÂ· MarêÂ­a Cecilia (CC0) êÂ· mriaco (CC BY 3.0) êÂ· NaBUru38 (CC BY-SA 4.0) êÂ· Diego Delso êÂ· bullit êÂ· Roxyuru êÂ· NASA JSC êÂ· Walteriot êÂ· Juanedc (CC BY 2.0) êÂ· Jmmuguerza (CC BY-SA 4.0) êÂ· Silvio omar (CC BY-SA 4.0) êÂ· Albasmalko êÂ· Marco Antonio Correa Flores.

**Gerado por IA:** veêÂ­culos e balsa vistos de cima (flux2-klein) êÂ· trilhas e efeitos sonoros (Magnific ê¢â¬â Lyria 3 Pro / ElevenLabs).

ConteêÂºdo aberto do [ARCKHê AI](https://ARCKHê AI).

---

<div align="center">
  <img src="capa/logo.svg" alt="Arckhé AI" height="32" />
  <p><strong>Arckhé AI</strong></p>
</div>