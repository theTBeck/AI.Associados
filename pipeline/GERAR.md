# Como o estúdio gera

Isto é o procedimento. A Patroa não dispara estas chamadas. O agente executa só depois que o TheMasterBECK confirmar o prompt fechado no grill.

Nenhuma chamada abaixo foi usada para criar imagem nesta correção. O gateway só respondeu o preço.

## 1. Foto-chave

Ferramenta Higgsfield `generate_image`.

- `model`: `cinematic_studio_2_5`
- `aspect_ratio`: `16:9` (ou `9:16` / `1:1` se o clipe for vertical ou quadrado)
- `resolution`: `2k` no ensaio, `4k` na entrega
- `prompt`: a frase fechada por Lindeza, DoiDONNA e Kolho
- `get_cost`: `true` antes de gerar

Preflight em 22 set 2026, sem job: **2 créditos**.

O modelo ao vivo só aceita `resolution`. Não há slider de temperatura, contraste, grão ou bloom nesta chamada. Esses sliders existem na tela do Cinema Studio 2.5, no site. Quem disser que o agente aplicou o Colorgrade por aqui está inventando.

## 2. Clipe de 15 segundos

Ferramenta Higgsfield `generate_video`, usando o `job_id` da foto como imagem inicial.

- `model`: `kling3_0`
- `duration`: `15`
- `aspect_ratio`: o mesmo da foto, desde que seja `16:9`, `9:16` ou `1:1`
- `mode`: `pro` na entrega, `std` no ensaio
- `sound`: `off` quando o clipe for mudo
- `medias`: um item com `role` `start_image` e `value` igual ao job da foto
- `prompt`: a mesma cena, com um movimento de câmera pelo nome oficial

Preflight em 22 set 2026, 15 s, modo pro, sem som, sem job: **26,25 créditos**.

O Kling não gera 21:9.

## 3. Depois que o arquivo está no disco

Foto local, com receita JSON:

```bash
/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/Cinemetrica/.venv/bin/python \
  /Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/grade-images/skills/grade-images/scripts/grade.py \
  render FOTO --recipe RECEITA.json --output FOTO-grade.png
```

O `python3` do sistema não tem NumPy. Esse interpretador da Cinemetrica tem. Sem receita JSON o comando não pinta nada.

Mp4 já gerado:

```bash
/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/Cinemetrica/.venv/bin/python -c \
  "import sys; sys.path.insert(0,'/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/Cinemetrica'); import Cinemetrica; print(Cinemetrica.shot_detector('CLIP.mp4'))"
```

Isso mede cortes. Não gera o clipe.

## 4. O que continua fora da pasta

O manual de cor já está no workspace: `/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/DCCM`. É atalho para `repos-cursor-legacy/vendor/DCCM`. Serve para o Kolho nomear a cor. O `curves.py` não gradeia o mp4.

OpenMontage fica em `Thiago-Beck/OpenMontage`. O ffmpeg deste Mac existe. A montagem de mp4 já gerados pode passar por `video_compose`. A geração de lá não é este MCP: Higgsfield Cloud usa `platform.higgsfield.ai` e o modelo padrão `seedance_2.0`; o Kling de lá é fal.ai ou a API oficial de Singapura.

O catálogo e o ensaio de luz estão no arquivo `AI.Associados.code-workspace`:

- `/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/amazing-digital-cinema` — lista de padrões de cinema digital. Consulta. Não gera imagem.
- `/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/amazing-digital-cinema/direct-light` — pré-luz de estúdio branco. O Kolho ensaia posição de luz. Não é o fotograma final.

3D Jutsu e Motion Control continuam chamadas à parte. Não há código deles aqui.
