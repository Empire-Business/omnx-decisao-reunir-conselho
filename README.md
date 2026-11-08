# Reunir conselho

Guia visual: abra o `COMO-FUNCIONA.html` desta pasta (dois cliques; funciona sem internet).

Coloca papéis fictícios (o do preço, o da marca, o do caixa, o do contra e outros) para debater uma decisão de negócio em duas rodadas. Um decisor escolhe um caminho e sai uma ata e um plano. **É opinião simulada, não é prova:** o plano traz o que precisa ser verificado. Antes de começar, a skill diz quantos ajudantes de IA vai abrir e espera a sua autorização.

## Como instalar

**Direto do GitHub:** no Claude Code, diga: "Instale a skill a partir de https://github.com/Empire-Business/omnx-decisao-reunir-conselho". Para atualizar, diga: "Atualize a skill a partir de https://github.com/Empire-Business/omnx-decisao-reunir-conselho". A IA baixa e copia os arquivos.

Se você já baixou esta pasta:

1. Abra o Claude Code (aplicativo do Claude, aba **Code**, ambiente **Local**).
2. Escreva: **"Instale a skill omnx-decisao-reunir-conselho a partir desta pasta: `<caminho desta pasta>`"**.
3. A IA copia a skill para o lugar certo. Você não digita comando nenhum e vê um aviso de que terminou.
4. Abra uma conversa nova e peça, por exemplo: **"Reúne o conselho: fico em dúvida entre lançar um curso barato ou uma mentoria cara."**.

### Instalar à mão

- **Mac ou Linux:** rode `bash install.sh` nesta pasta (dá para rodar de qualquer lugar, com o caminho entre aspas). A skill vai para `~/.claude/skills/omnx-decisao-reunir-conselho`. Se editar algo aqui, rode de novo.
- **Windows:** copie esta pasta, sem o `install.sh`, para `%USERPROFILE%\.claude\skills\omnx-decisao-reunir-conselho`. Ou peça para a IA fazer isso.

## O que ela não faz

- Não simula pessoas reais, mesmo a pedido.
- Não trata debate simulado como prova.
- Não inventa dado de mercado: o que não vier de você é marcado como suposição.
- Oferta e preço são do Bento; copy, da Rita; análise de dados, do Tales.

## Pedidos que funcionam

- "Reúne o conselho: fico em dúvida entre lançar um curso barato ou uma mentoria cara."
- "Debate essa decisão: contrato alguém ou terceirizo o atendimento?"
- "Quero pontos de vista opostos sobre subir meu preço."
- "Mesa redonda sobre abrir um novo canal de vendas."

## Outro sistema operacional e outra ferramenta

Funciona em Mac, Windows e Linux, no Claude Code e no Codex. Na instalação, a própria IA faz as adaptações necessárias para o seu computador.
