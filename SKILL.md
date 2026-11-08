---
name: omnx-decisao-reunir-conselho
description: "Reúne um conselho de papéis fictícios (o do preço, o da marca, o do caixa, o do cliente, o da operação, o do contra) que debatem uma decisão de negócio em duas rodadas; um decisor escolhe um caminho e sai um plano de ação, com o que precisa ser verificado na vida real. Avisa o custo antes de começar e deixa claro que opinião simulada não é prova. Use quando pedirem 'reúne o conselho', 'debate essa decisão', 'mesa redonda sobre isso', 'quero pontos de vista opostos', 'estou em dúvida entre A e B no meu negócio', 'me ajuda a decidir olhando vários ângulos'. Nunca simula pessoas reais, mesmo a pedido. Não use para tarefa simples ou pergunta de uma resposta só, código (inacio), agente de IA (agenor), montar oferta ou preço (bento), copy (rita) nem análise de dados (tales)."
---

# Reunir conselho

Coloca perspectivas opostas para debater uma decisão real de negócio. Um decisor escolhe um caminho e sai um plano com o que precisa ser verificado.

**Isto é opinião simulada, não é prova.** Os papéis pensam com o que a pessoa contou e o que a IA sabe. Não têm dados novos e nunca viram o negócio. O conselho serve para achar pontos cegos e organizar o raciocínio. Diga isso no começo e no fim.

## Como conversar

Quem usa pode nunca ter feito isso. Se a pessoa chegar sem contexto, diga em duas linhas o que você faz e pergunte qual é a decisão. Uma pergunta por vez. Palavra técnica vem com meia frase de explicação. Toda resposta termina com o próximo passo. A pessoa nunca precisa digitar comando.

## Passos

1. **Entenda a decisão.** Sem isto não dá para começar: **as alternativas reais**, **o contexto** (o que vende, para quem, números que a pessoa tem), **as restrições** (dinheiro, tempo, equipe) e **o que ela quer alcançar e até quando**. Use o que ela já disse e pergunte só o que falta, um item por vez. Se for tarefa simples ou tiver uma resposta só, responda sem conselho e diga por quê. Se a decisão for jurídica, médica ou de risco financeiro grave, avise que o conselho não substitui um profissional e siga só se ela confirmar.
2. **Monte o conselho.** Leia `references/papeis.md` e escolha de 3 a 5 papéis cujos interesses batem de frente **nesta** decisão. Sempre inclua o do contra. **Cada alternativa real precisa de ao menos um papel que tenda a defendê-la.** Nunca use nome de pessoa real, nem que a pessoa peça "o que fulano diria": troque pelo papel equivalente e explique em uma frase.
3. **Avise o custo e espere o sim.** Antes de qualquer rodada, mostre:

   ```
   Conselho: <papéis>
   Vou abrir <N> ajudantes de IA: <P> papéis × 2 rodadas + 1 decisor.
   Cada ajudante é uma conversa à parte e consome do seu limite ou crédito.
   Alternativa mais barata: rodo tudo nesta conversa, numa versão enxuta, mas os papéis ficam menos independentes.
   Lembrando: é opinião simulada, não prova.
   Posso seguir? (completo / enxuto / ajustar papéis)
   ```

   Não siga sem resposta. Se a pessoa tirar papéis e sobrar alternativa sem defensor, avise antes de seguir. Pedido de rodada extra: avise de novo. Se um ajudante falhar e precisar ser refeito, o número sobe: conte quantos abriu de fato e diga na entrega.
4. **Rodada 1, posições independentes.** Abra um subagente por papel, em paralelo, cada um só com o caso e a própria ficha, sem ver os outros. Use os modelos de prompt de `references/prompts-das-rodadas.md`.
5. **Rodada 2, confronto.** Cada papel recebe todas as posições e responde: ataca o argumento mais forte de um colega, admite o que aceita e diz o que o faria mudar de ideia. Papel que só concorda não cumpriu a tarefa: refaça. Se na rodada 1 todos escolherem a mesma alternativa, peça ao do contra que, na rodada 2, defenda a melhor alternativa rejeitada.
6. **Decisão.** Um subagente novo faz o decisor. Ele lê as duas rodadas e escolhe **um caminho**, recusando os demais com motivo. Pode decidir "ainda não dá para decidir, descubra isto primeiro" se faltar um dado que muda tudo.
7. **Separe suposição de fato.** Marque todo número ou afirmação que não veio da pessoa como `[suposição]` e diga, no plano, como testar de um jeito barato. Os papéis não podem inventar dado de mercado. Prazo que a pessoa não deu também é `[suposição]`.
8. **Entregue dois arquivos** a partir de `templates/ata.md` e `templates/plano.md`. Pergunte onde salvar; a sugestão é uma pasta `conselho-<tema>-AAAA-MM-DD`. Sem resposta, entregue tudo na conversa. Mostre a decisão em poucas linhas, as suposições a verificar, quantos ajudantes abriu de fato e repita que é opinião simulada.

## Versão enxuta

Sem subagentes, ou quando a pessoa escolher, faça tudo nesta conversa: escreva as posições da rodada 1 de cada papel antes de ler as dos outros, depois a rodada 2, depois a decisão. Avise que a independência é menor, porque tudo sai da mesma cabeça. As mesmas regras e arquivos valem.

## Regras

- **Só papéis fictícios.** Nenhuma pessoa real, viva ou morta, nenhum guru, nenhuma marca como personagem.
- **Divergência é o produto.** Conselho em que todos concordam não ajudou: diga isso.
- **Nada de "faça as duas coisas"** se as restrições não permitirem.
- **Dado inventado não entra.** Sem fonte, é `[suposição]`.
- **Quem decide é a pessoa.** A decisão do conselho é uma recomendação.
- **Sem ação externa.** O conselho não publica, não contrata e não gasta nada.

## Outro sistema operacional

Esta skill não tem script: só conversa e escreve texto, então funciona igual em macOS, Windows e Linux. Adapte o que for preciso e conte à pessoa o que realmente testou.

- **Instalar:** no Windows, copie esta pasta, sem o `install.sh`, para `%USERPROFILE%\.claude\skills\omnx-decisao-reunir-conselho`. No Mac e no Linux, rode o `install.sh`.
- **Caminhos:** `~` é a pasta do usuário; no Windows é `%USERPROFILE%`. Caminho com espaço vai entre aspas.
- **Abrir um arquivo salvo para a pessoa:** `open` (macOS), `start ""` (Windows), `xdg-open` (Linux).

## Outra ferramenta (Codex e outras)

Compatível com Claude Code, Codex e outras ferramentas de agentes, em Mac, Windows e Linux. Se a pessoa pedir para instalar
fora do Claude Code, a IA dela adapta na hora, testa no computador dela e conta o que realmente funcionou:
- **Onde pôr os arquivos:** confira na documentação atual da ferramenta. No Codex, a referência em 08/11/2026 era `~/.agents/skills/<name>`.
- **Caminhos:** `references/...` e `templates/...` são relativos à pasta onde este `SKILL.md` ficou instalado.
- **Subagentes:** use o recurso equivalente da ferramenta. Se não houver, siga a versão enxuta e diga isso à pessoa.
