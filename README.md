# Projeto 2 - Computacao Grafica

Cena 3D em OpenGL para o Projeto 2 da disciplina de Computacao Grafica.

O cenario representa uma balada urbana. O ambiente interno e um clube moderno
com pista de danca central, varias pessoas texturizadas, palco para o som,
sofas, bancos, luminarias e bola de discoteca. O ambiente externo e uma
rua/estacionamento com piso de asfalto, entrada metalica, postes alinhados,
carro e lixeira. Todo o codigo esta em
`Projeto_2_Computacao_Grafica.ipynb`.

Fora do notebook existem apenas arquivos de dados: modelos `.obj`, materiais
`.mtl`, imagens de textura prontas e `assets/sources/ASSET_SOURCES.txt` com as
fontes/licencas.

## Requisitos Atendidos

- Ambiente interno e ambiente externo com objetivo coerente.
- O ambiente interno tambem e um modelo `.obj`: `club_room`.
- A balada foi fechada com parede frontal texturizada.
- A area externa inclui entrada metalica em `.obj` separado.
- Piso interno e piso externo com texturas prontas diferentes, com a pista como quadrado central.
- Pessoas adicionadas com texturas de imagem prontas (`party_person_01` e `party_person_male_01`).
- Skybox trocado por um ceu noturno limpo, sem cidade ou montanhas.
- Carro trocado por outro modelo normal do pacote automotivo.
- Bola de discoteca com textura correta de mosaico espelhado.
- Camera com matrizes Model, View e Projection.
- Limite de movimentacao da camera dentro do terreno/ceu.
- Visualizacao da malha poligonal com a tecla `P`.
- Transformacoes independentes por teclado:
  - translacao no carro externo;
  - rotacao na bola de discoteca;
  - escala no boombox.
- Sem efeitos de iluminacao.
- Sem uso de funcoes obsoletas como `glBegin`, `glEnd`, `glTranslate`,
  `glRotate`, `glScale`, `glLight`, `glMaterial` ou matrizes fixas do OpenGL.

## Estrutura

```text
.
├── Projeto_2_Computacao_Grafica.ipynb
├── README.md
└── assets
    ├── models
    │   ├── bar_chair_round_01.obj / bar_chair_round_01.mtl
    │   ├── boombox.obj / boombox.mtl
    │   ├── club_room.obj / club_room.mtl
    │   ├── dance_floor.obj / dance_floor.mtl
    │   ├── disco_ball.obj / disco_ball.mtl
    │   ├── disco_support.obj / disco_support.mtl
    │   ├── lounge_floor.obj / lounge_floor.mtl
    │   ├── modern_ceiling_lamp_01.obj / modern_ceiling_lamp_01.mtl
    │   ├── night_skybox.obj / night_skybox.mtl
    │   ├── corrado_car_01.obj / corrado_car_01.mtl
    │   ├── oga_trash_can_01.obj / oga_trash_can_01.mtl
    │   ├── parking_lot.obj / parking_lot.mtl
    │   ├── party_person_male_01.obj / party_person_male_01.mtl
    │   ├── party_person_01.obj / party_person_01.mtl
    │   ├── sofa_01.obj / sofa_01.mtl
    │   ├── street_lamp_01.obj / street_lamp_01.mtl
    │   ├── rollershutter_door.obj / rollershutter_door.mtl
    │   └── trash_can_01.obj / trash_can_01.mtl
    ├── sources
    │   └── ASSET_SOURCES.txt
    └── textures
        └── imagens `.jpg`/`.png` usadas pelos materiais
```

## Como Executar

Instale as dependencias:

```bash
pip install numpy PyOpenGL glfw PyGLM Pillow notebook ipykernel
```

Abra o notebook:

```bash
jupyter notebook Projeto_2_Computacao_Grafica.ipynb
```

Execute as celulas em ordem. A ultima celula abre a janela OpenGL.

## Controles

- `W`, `A`, `S`, `D`: mover a camera no plano horizontal.
- `Espaco` / `C`: subir e descer a camera.
- Mouse: olhar ao redor.
- `P`: exibir ou ocultar a malha poligonal.
- `T` / `G`: transladar o carro externo.
- `R` / `F`: rotacionar a bola de discoteca.
- `Z` / `X`: alterar a escala do boombox.
- `Esc`: fechar a janela.

## Fontes dos Assets

As origens dos modelos e texturas usados na cena estao documentadas em:

- [assets/sources/ASSET_SOURCES.txt](assets/sources/ASSET_SOURCES.txt)

Resumo dos principais assets:

- `club_room.obj`, `lounge_floor.obj`, `dance_floor.obj` e `parking_lot.obj`: modelados/ajustados localmente para este projeto.
- `party_person_01` e `party_person_male_01`: modelos humanos com textura pronta, vindos do CadNav.
- `corrado_car_01`: carro com textura pronta, vindo do OpenGameArt.
- `oga_trash_can_01`: lixeira com textura pronta, vinda do OpenGameArt.
- `boombox`, `bar_chair_round_01`, `sofa_01`, `modern_ceiling_lamp_01` e `street_lamp_01`: assets prontos.
- `rollershutter_door`: asset pronto usado na entrada externa.
- `night_skybox`, `dance_floor`, `disco_ball`, paredes e outros materiais: texturas prontas listadas no arquivo de fontes.
