# Padrão "Prompt Rico" – Técnica FTAE (Function, Tipo, Assunto, Estilo)

- **Function**: O que voce quer que o chat faça, ex: resumir,  traduzir, criar topics, etc.
- **Tipo**: de texto, Conteudo ex: roteiro, post, poema, artigo, carrossel para instagram, etc.
- **Assunto**: Se direcionarmos, o chat sabe quais redes neurais usar, quais pontos ligar.
- **Estilo**: ex: escrever como se fosse um filosofo, escritor, alguem conhecido, informal e descontraído, etc.

Criar e consumir conteudos artificiais, que ainda nao existem na vida real, que estao no mundo da fantasia.
> Ex: Criar textos amigaveis, para um publico alvo especifico, etc.

Criar tom de voz: Dizer para quem ele deveria explicar aquele conteudo.  
> Ex: Explique-me como se eu fosse para uma criança, etc.

Hack para criar autoridade (com o poder da fantasia).
> Ex: Escrever carta de solicitacao de emprego para o diretor da empresa como se fosse um dev senior.

## Técnica 3R's (Resumo, Roteiro, Regras)

- **Campos Semânticos**: São declarados entre chaves. São áreas de restrições sobre como o modelo deve conversar.  
- **Variáveis**: São declaradas entre colchetes.
- **Regras**: São declaradas iniciando a linha com o sinal de maior.

## Exemplo

```prompt
Escreva um artigo sobre primeiros passos no Docker, em tom de conversa para uma criança de 10 anos. Agora, use os itens em {RESUMO} para o {ROTEIRO} seguindo as {REGRAS}

{RESUMO}
[Autoridade]: Felipe, um desenvolvedor FullStack
[Avatar]: Desenvolvedores Júniors
[Problema]: Como instalar o Docker

{ROTEIRO}
Olá eu sou [Autoridade] e vou ajudar o [Avatar].
Hoje vamos resolver o [Problema].

{REGRAS}
> Siga o {ROTEIRO} acima e substitua os elementos entre [] por aqueles listados em {RESUMO} acima.
> Mantenha o tom e ritmo, mas reescreva as palavras em {ROTEIRO} para que seja diferente do original, expandindo ou mudando conforme necessário.
> Use analogias simples e hipérboles.
```
