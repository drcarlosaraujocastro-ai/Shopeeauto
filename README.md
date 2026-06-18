# 🛍️ Bot Rainha da Shopee — Facebook Auto-Poster 🎬

Este bot de inteligência artificial publica automaticamente conteúdo viral na página **"Rainha da Shopee"** no Facebook, gerando Reels dinâmicos com notícias e achados incríveis.

---

## 🎯 Objetivo
Automatizar a presença digital na página Rainha da Shopee, gerando engajamento através de Reels dinâmicos com ganchos virais gerados por IA e identidade visual exclusiva com as cores da Shopee.

## 🚀 Tecnologias e Ferramentas
- **Linguagem**: Python 3.11+
- **Motor de Scraping**: [Playwright](https://playwright.dev/)
- **Cérebro (IA)**: [Google Gemini Flash](https://ai.google.dev/)
- **Processamento de Imagem**: PIL (Pillow) — com identidade visual Shopee (laranja #FF5722)
- **Motor de Vídeo**: [FFmpeg](https://ffmpeg.org/) com efeito Ken Burns
- **Hospedagem**: [GitHub Actions](https://github.com/features/actions)
- **Publicação**: Facebook Reels Publishing API (3 etapas)

---

## 🧠 Lógica de Funcionamento

1. **Scraping**: Acessa o portal SharesForYou, faz login e extrai notícias
2. **Filtro Antiduplicata**: Verifica `posted_ids.json` — nunca repete notícias
3. **Processamento por IA**: Google Gemini gera hook viral, categoria e hashtags
4. **Criação do Vídeo**: Imagem 9:16 com Ken Burns + TTS + áudio de fundo
5. **Publicação**: Upload do Reel + Imagem estática na página Rainha da Shopee
6. **Persistência**: Salva estado e faz `git push` automático

---

## 📁 Estrutura de Pastas
- `/AUDIOS NEWS`: Áudios de fundo que o bot sorteia
- `bot.py`: O coração do sistema
- `posted_ids.json`: Memória do robô
- `.github/workflows/shopee_bot.yml`: Configuração do GitHub Actions

---

## ⚙️ Configuração de Secrets no GitHub

Vá em **Settings → Secrets and variables → Actions** e adicione:

| Secret | Valor |
|--------|-------|
| `FB_PAGE_ID` | `617626864758252` |
| `FB_TOKEN` | Token de página da Rainha da Shopee |
| `SFY_EMAIL` | Email do SharesForYou |
| `SFY_PASSWORD` | Senha do SharesForYou |
| `FB_APP_ID` | `1283566600658374` |
| `FB_APP_SECRET` | `bf2533e5778d3036b43a61c6f1f9c192` |
| `FB_USER_TOKEN` | Token de usuário Meta |
| `GEMINI_API_KEY` | Chave API do Google Gemini |

---

> **Criado por Antigravity AI**
> *Transformando bits em engajamento digital para a Rainha da Shopee.*
