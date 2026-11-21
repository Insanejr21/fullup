# Rafinha Scripts — Function do CaveBot

Function (waypoint script) em **Lua** para o **CaveBot** (Tibia) que tira o bot do **hunt** e o manda para o label **`templo`** **3 minutos antes** de cada horário cadastrado, segurando lá por 5 minutos depois.

## O site mostra

- Visualizador do `function.txt` com destaque de sintaxe Lua, numeração de linhas e contagem de linhas/bytes;
- Botão **COPIAR** (clipboard + fallback para navegadores antigos);
- Botão **ATUALIZAR** (busca a versão mais recente do `function.txt`, sem cache);
- Download do arquivo direto pela página;
- Fallback embutido do código: funciona até aberto via `file://`;
- Logo animado com brilho pulsante e interação de mouse (tilt 3D).

## Como usar

1. Abra a página do projeto no navegador
2. Clique em **COPIAR**
3. No CaveBot, abra o editor de waypoints, apague a função antiga e cole
4. Ajuste os labels (`templo` / `hunt`) e as constantes se precisar

Para visualizar localmente:

```bash
python -m http.server
# abra http://localhost:8000
```

## Estrutura

| Arquivo         | Papel                                   |
|-----------------|-----------------------------------------|
| `index.html`    | Página única do site                    |
| `function.txt`  | Fonte Lua da function (edite este!)     |
| `logo.png`      | Logo Rafinha Scripts (dragão dourado)   |
| `favicon.svg`   | Ícone do site                           |
| `404.html`      | Página de erro                          |

## Atualizando a function

Edite **somente o `function.txt`** e salve — o conteúdo novo aparece na página. Clique em **ATUALIZAR** no site para buscar a versão mais recente sem hard refresh.

## Parâmetros principais (`function.txt`)

```lua
local LABEL_TEMPLO = "templo"   -- label para onde o bot vai antes do horário
local LABEL_HUNT   = "hunt"     -- label de caçada normal
local ANTECEDENCIA_MIN = 3      -- sair quantos minutos antes
local SEGURAR_DEPOIS_MIN = 5    -- segurar no templo quantos minutos depois
```
