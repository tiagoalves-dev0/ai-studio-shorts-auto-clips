# 🎬 AI Studio YouTube Shorts Auto Clip
> 🇧🇷 **Português (PT-BR)** | [🇺🇸 Read in English](./README.en.md)
![Status](https://img.shields.io/badge/status-em%20planejamento-yellow)
![Python](https://img.shields.io/badge/Python-3.12+-3776AB?logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-TypeScript-61DAFB?logo=react&logoColor=black)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-SQLite-4169E1?logo=postgresql&logoColor=white)
![FFmpeg](https://img.shields.io/badge/FFmpeg-yt--dlp-007808?logo=ffmpeg&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)
Plataforma **full-stack, segura e multiplataforma** (Windows `.bat` e Linux `.sh`) para **automação inteligente de cortes de vídeos** (YouTube Shorts e exportação organizada para postagem manual em TikTok, Instagram Reels e Kwai).
O projeto utiliza uma arquitetura **Dashboard na Nuvem + Agente Local em Python**, garantindo **custo mínimo de servidor** e **privacidade total**: contas do YouTube, chaves de IA e renderização pesada rodam diretamente na máquina do usuário.
---
## ✨ Funcionalidades Planejadas
- **🎯 Multi-Nichos e Múltiplas IAs (*BYOK*):** Escolha entre **Google Gemini**, **OpenAI (GPT)**, **Groq (Llama)**, **Anthropic (Claude)** ou **Ollama** (100% local) usando sua própria chave de API.
- **🎨 Personalização Completa de Estilos & Presets:**
  - Edite fonte, cores, contorno, sombra, posição e animações das legendas **antes de gerar o vídeo final**.
  - Adicione marca d'água/logo do canal e escolha enquadramento (`9:16` centralizado, *blur* de fundo, *split-screen* ou *auto-reframe*).
  - Crie, salve e compartilhe seus próprios **Presets de Corte** por nicho.
- **🌍 Múltiplos Idiomas:** Transcrição e geração de legendas automáticas com `faster-whisper` no idioma desejado.
- **📺 Gestão Detalhada Multicanal com Pesos:**
  - Conecte múltiplos canais do YouTube e visualize status OAuth, nicho, cota e histórico de envios.
  - Distribua Shorts automaticamente usando **pesos configuráveis** (ex: Canal A peso `3`, Canal B peso `1`).
  - Para outras redes (TikTok, Reels, Kwai), gere pacotes prontos com vídeo, título, descrição e guia de postagem manual.
- **⚡ Dashboard Web em Tempo Real:** Acompanhe cada etapa (`download` → `transcrição` → `análise IA` → `renderização` → `upload`) em tempo real via WebSockets.
- **🔌 Agente Conector com Auto-Atualização:** Script leve em Python (`connector.py`) autenticado por **Chave de API do Usuário** (regenerável a qualquer momento no painel), com atualização automática modular e verificação de integridade (`SHA-256`).
- **☁️ Armazenamento Seguro de Vídeos Aprovados:** Metadados salvos no PostgreSQL e vídeos finais opcionais armazenados em **Object Storage privado** (Cloudflare R2 / S3) com URLs assinadas temporárias.
