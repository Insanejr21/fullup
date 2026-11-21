# FullUp — Function do CaveBot

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-online-3ddc84?style=flat-square&logo=github)](https://insanejr21.github.io/fullup/)
[![License](https://img.shields.io/badge/licença-não%20informada-8296a8?style=flat-square)](#)

> **Site no ar:** **https://insanejr21.github.io/fullup/**

Function (waypoint script) em **Lua** para o **CaveBot** (Tibia) que tira o bot do **hunt** e o manda para o label **`templo`** **3 minutos antes** de cada horário cadastrado no
[fullup](https://github.com/Insanejr21/fullup), segurando lá por 5 minutos depois.

## O que o site mostra

- Visualizador do `function.txt` com destaque de sintaxe Lua, numeração de linhas e contagem de linhas/bytes;
- Botão **COPIAR** (clipboard + fallback para navegadores antigos);
- Botão **ATUALIZAR** (busca a versão mais recente do `function.txt`, sem cache);
- Download do arquivo e link para a versão *raw* no GitHub;
- Fallback embutido do código: funciona até aberto via `file://`.

## Como usar

1. Abra **https://insanejr21.github.io/fullup/**
2. Clique em **COPIAR**
3. No CaveBot, abra o editor de waypoints, apague a função antiga e cole
4. Ajuste os labels (`templo` / `hunt`) e as constantes se precisar

## Estrutura

| Arquivo         | Papel                                             |
|-----------------|---------------------------------------------------|
| `index.html`    | Página única publicada pelo GitHub Pages          |
| `function.txt`  | Fonte Lua da function (edite este arquivo!)       |
| `favicon.svg`   | Ícone do site                                     |
| `404.html`      | Página de erro do GitHub Pages                    |
| `.nojekyll`     | Desativa o processamento Jekyll (site estático)   |

## Atualizando a function

Edite **somente o `function.txt`** e dê commit. O GitHub Pages republica automaticamente em ~1 minuto — não é preciso mexer no HTML. Depois, clique em **ATUALIZAR** no site.

## Parâmetros principais (`function.txt`)

```lua
local LABEL_TEMPLO = "templo"   -- label para onde o bot vai antes do horário
local LABEL_HUNT   = "hunt"     -- label de caçada normal
local ANTECEDENCIA_MIN = 3      -- sair quantos minutos antes
local SEGURAR_DEPOIS_MIN = 5    -- segurar no templo quantos minutos depois
```

## Publicação

Site estático servido pelo **GitHub Pages** a partir da branch `main` (pasta raiz).
Qualquer push na `main` republica o site automaticamente.
