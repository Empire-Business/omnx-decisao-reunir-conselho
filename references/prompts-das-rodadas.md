# Prompts das rodadas

Preencha os campos e passe a cada subagente. O subagente não vê esta conversa: tudo que ele precisa vai no prompt. Se o debate for longo, salve as posições num arquivo temporário e passe o caminho. Antes de seguir, confira se cada resposta chegou; se vier vazia, refaça uma vez e conte o refeito no custo.

Em todos, inclua o bloco de regras:

```
Regras: você é um papel fictício, um ponto de vista. Não assuma identidade de pessoa real nem cite pessoas reais como autoridade. Use só os dados do caso. Número ou fato que não veio do caso leva [suposição] logo depois. Seja direto. Escreva em português, em até quatro parágrafos. Entregue a resposta inteira na sua mensagem final; não deixe só em arquivo.
```

## Rodada 1: posição independente

```
Você é <papel>. Sua ficha: <linha do papel em references/papeis.md>.

O caso:
<decisão, alternativas, contexto, restrições, objetivo e prazo>

Responda, sem saber o que os outros dirão:
1. Qual alternativa você defende e por quê, do seu ponto de vista?
2. Qual o maior erro que este negócio pode cometer aqui?
3. O que você precisaria saber que o caso não diz?

<bloco de regras>
```

## Rodada 2: confronto

```
Você é <papel>. Sua ficha: <linha do papel>.

O caso: <mesmo resumo>

Posições da rodada 1:
<todas as posições, com o nome do papel>

Responda:
1. Qual é o argumento mais forte de um colega contra a sua posição? Rebata ou aceite, citando o colega.
2. O que você aceita mudar para chegar a um plano possível?
3. O que você não abre mão, e por quê?
4. Que fato concreto faria você mudar de lado?

Concordar com todo mundo não cumpre a tarefa.
<bloco de regras>
```

## Decisão

```
Você é o decisor de um conselho fictício. Não tem preferência fixa. Só pesa argumentos à luz do objetivo e das restrições.

O caso: <mesmo resumo>

Debate completo:
<rodadas 1 e 2>

Responda:
1. Os dois ou três caminhos que saíram do debate, em uma linha cada.
2. Sua decisão: um caminho só, começando com "Decisão:". Se faltar dado que muda tudo, a decisão é "Ainda não decidir" e diga o que descobrir.
3. O que você aproveita e o que descarta de cada papel.
4. As suposições que sustentam a decisão, cada uma com um jeito barato de testar.
5. O fato que faria reverter a decisão.

Use só o que está no caso e no debate. Mantenha as marcas [suposição]. Não invente datas: use o prazo do caso ou marque o que propuser com [suposição]. Entregue a resposta inteira na sua mensagem final.
```
