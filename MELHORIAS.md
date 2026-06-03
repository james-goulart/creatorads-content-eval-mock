# Redesign da tela de Avaliação de Conteúdos — o que muda

> Protótipo navegável (`index.html`) da tela
> `creatorads.brandlovrs.com/campaigns/:id/contents`.
> Abra o HTML no navegador e teste à vontade — tudo é clicável.
> Comparativo abaixo: **hoje (tela atual)** → **proposta (protótipo)**.

---

## 1. Layout geral
- **Hoje:** 3 colunas — Momentos (esq.) · Vídeo (centro) · Análise/Briefing + aprovação (dir.).
- **Proposta:** 4 colunas, com o **vídeo sempre centralizado**:
  1. **Momentos** (esquerda)
  2. **Análise / Briefing + decisão** (do lado dos Momentos)
  3. **Vídeo vertical** (centro)
  4. **Linha do tempo** (direita)

## 2. Navegação
- O **menu superior e o menu lateral** continuam, mantendo a navegação que você já conhece.
- **O que muda:** o **menu lateral passa a ser um trilho de ícones que se expande ao passar o mouse** (hoje ele ocupa uma largura fixa) e pode ser fixado aberto pelo botão ☰. Motivo: liberar espaço horizontal para as 3 colunas centrais (Análise, Vídeo e Linha do tempo).
- As abas de status do topo ganham uma **nova aba: "Contestações"**, ao lado de Pendentes · Reprovados · Aprovados — para tratar as contestações num lugar dedicado em vez de misturar com os pendentes.

## 3. Identificação do creator (anti-fraude)
- **Foto do creator bem maior**, para facilitar a conferência visual foto × vídeo.
- Exibe os **três @ (Instagram, TikTok e YouTube)** + **Creator ID** num único cabeçalho.

## 4. Avaliação por toggles (em vez de polegares)
- Cada uma das **10 linhas** (8 diretrizes de conteúdo + qualidade de áudio + segurança de marca) tem um **toggle**.
- O toggle **já vem na posição que a Guardian avaliou**. O revisor só mexe quando **discorda** da Guardian.
- Sempre que o revisor **diverge da posição original da Guardian**, a linha fica **destacada em roxo** (fica claro o que foi alterado por humano).
- Mantivemos o **✓ / ✗ da Guardian** ao lado de cada linha, para comparar a avaliação da IA com a decisão humana.
- À **esquerda de cada linha** ficam os **timestamps** onde aquela diretriz é verificada — clicando, o vídeo "pula" para aquele instante (no protótipo, abre um frame de exemplo).

## 5. Organização e ordem
- Acabaram os acordeões soltos do layout antigo. Ordem fixa, de cima para baixo:
  **Diretrizes de conteúdo → Qualidade de áudio → Segurança de marca**.
- **Qualidade de áudio** e **Segurança de marca** agora são **acordeões com subitens** (começam recolhidos):
  - *Qualidade de áudio:* Música com direitos autorais · Áudio baixo ou ausente
  - *Segurança de marca:* Discurso de ódio · Assédio · Conteúdo ilegal/falso · Conteúdo sensível
- O **toggle do topo de cada acordeão é um reflexo**: fica **desligado se qualquer subitem estiver desligado**.
- Ao alterar qualquer subitem, a **linha do topo também fica roxa** (sinaliza divergência da Guardian).

## 6. Botão de decisão mais inteligente
- O botão fica junto da Análise, com um **campo de feedback ao creator logo acima**.
- A regra segue as avaliações:
  - alguma linha recusada → botão **"Recusar"** (vermelho);
  - todas aprovadas → botão **"Aprovar"** (azul).
- Removemos o antigo botão "X" de reprovar.
- Uma **dica ao vivo** mostra quantas diretrizes ainda estão recusadas (ex.: *"2 diretrizes recusadas — aprove ou recuse o conteúdo"*), para o revisor entender por que o botão ainda está vermelho.
- Ao clicar em **Recusar**, abre um **pop-up** com as diretrizes recusadas e o feedback a ser enviado ao creator.

## 7. Linha do tempo (histórico completo do conteúdo)
- Nova coluna à direita com **todo o histórico daquele conteúdo numa única timeline**: envio → análise da Guardian → feedback enviado → contestação do creator → reenvio → nova análise, etc. (rolagem contínua).
- Cada **rodada** (v1, v2…) aparece separada.
- As **mensagens do creator têm visual próprio** (balão roxo com foto), diferenciando do feedback enviado pela operação (estilo post-it) e dos eventos do sistema.

## 8. Comportamento por aba de status
- **Pendentes:** fluxo normal de aprovar/recusar.
- **Reprovados:** botão muda para **"Reprovado — altere avaliação para contestar"**; ao mexer em qualquer toggle, vira **"Contestar"** (roxo).
- **Aprovados:** estado de conteúdo já aprovado.
- **Contestações:** mostra a **contestação do creator logo acima do botão** de decisão.
- **O creator exibido muda conforme a aba**, para o contexto ficar claro.

## 9. Outros ajustes de usabilidade
- Novo botão **"Draw in"** nos Momentos: **recolhe a coluna da esquerda** para dar mais espaço às 3 centrais.
- **Containers de Análise e Briefing maiores** que hoje (abas no topo, mais área para os checks).
- A **barra de busca dos Momentos** segue no topo da coluna, junto do novo botão de recolher.

---

### Como testar
1. Abra `index.html` no navegador.
2. Vire os toggles e veja o destaque roxo + o botão mudando entre Aprovar/Recusar.
3. Clique nos timestamps para "pular" no vídeo.
4. Troque entre as abas (Pendentes / Reprovados / Aprovados / Contestações).
5. Teste o "Draw in", o menu lateral (passe o mouse) e o pop-up de recusa.

> É um protótipo de fidelidade visual — dados são fictícios e nada é salvo.
> Feedbacks são bem-vindos! 🙏
