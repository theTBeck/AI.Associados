# Integração — leitura dos repositórios em 22 set 2026

Fonte: README e `package.json` de cada pasta. Nada foi executado.

| Repo | Real | Serve para o clip de 15 s | Não serve |
|---|---|---|---|
| `3d-characters` | Launcher. O app 3D não está no clone. O runtime citado é a demo https://actorlab.pages.dev/ | Pré-visualizar pose e câmera no navegador, se a demo abrir | Motor 3D local, export automático para o Kling |
| `ActorLab` | Mesmo launcher, mesmo `package.json` (`actorlab-3d-characters`) | Igual ao de cima. É cópia operacional, não um segundo programa | Tratar como ferramenta diferente |
| `amazing-digital-cinema` | Pasta no `AI.Associados.code-workspace`. Lista de padrões de cinema digital (DCP, QC, mastering) | Consulta, quando a entrega for sala de cinema | Gerar imagem ou cor |
| `amazing-digital-cinema/direct-light` | Pasta no mesmo workspace. Pré-luz de estúdio branco, demo web e app Tauri, versão 1.0.5 | Kolho ensaiar posição de luz e câmera | Render físico nem fotograma final |
| `Aperture-Viewer` | Viewer de Second Life / OpenSim, com pós interno daquele mundo virtual | Nada neste pipeline | Corrigir cor de clipe Kling ou montar filme |
| `Cinemetrica` | Python: detecta corte, extrai um frame por plano, mede duração, gera paleta | Depois do mp4 existir: decupagem e paleta | Roteiro, ator, VFX. Detecção de ator está escrita como futuro |
| `ColorCorrectionPackage` | Correção científica de foto com carta de cor, para imagem de laboratório (artigo de fenotipagem de planta, 2026) | Nada, salvo ensaio com carta de cor | Grade de cinema |
| `DCCM` | Já está no workspace: atalho `/Users/admin/Documents/INTELIGENCIA-ARTIFICIAL/DCCM` → `repos-cursor-legacy/vendor/DCCM`. Manual de cor e `curves.py` (a conta fecha sozinha no arquivo) | Kolho consultar o nome da cor | Aplicar grade num mp4 |
| `DIT-Pro` | Cópia verificada de cartão (hash, manifesto MHL, relatório de diária) | Guardar o arquivo gerado com checksum | Cor, VFX, câmera |
| `grade-images` | Grade determinística de foto parada (JPEG, PNG, RAW). Não inventa luz nem grão | Corrigir a foto-chave antes do Kling, se for arquivo local | Vídeo, clipe de 15 s |
| `super-director` | Roteiro de direção: bíblia, planta de cena, decupagem em trechos de até 15 s, prompt em seis blocos | Lindeza escrever o pedido | Gerar o clipe |
| `Thiago-Beck/OpenMontage` | Três portas de geração, nenhuma é o MCP deste estúdio. `higgsfield_video` chama `https://platform.higgsfield.ai/v1/generations`, modelo padrão `seedance_2.0`. `kling_video` é fal.ai. `kling_official_video` é `api-singapore.klingai.com`. `video_compose` usa o ffmpeg deste Mac | Juntar mp4 já gerados, com ffmpeg, se um projeto OpenMontage for aberto de propósito | Substituir `cinematic_studio_2_5` e `kling3_0` do MCP |
| `bravector` | Campanha Bravecto. Não estava na lista anterior | Nada neste clipe | Entrar no estúdio |
| `raw-player` | OCTOPUS RAW Player: toca sequência CinemaDNG | Rever RAW de câmera, se houver `.dng` | Gerar ou corrigir o clipe Kling |

## Memória

As decisões deste estúdio ficam em `memory/PATROA-MEMORY.md`. O AgentDB foi retirado desta pasta.
