# 🐍 Snake — Jogo da Cobrinha

Um jogo clássico da cobrinha desenvolvido com **HTML5, CSS3 e JavaScript puro**, executado diretamente no navegador, sem necessidade de instalar programas ou utilizar frameworks externos.

O objetivo é controlar a cobrinha, coletar as maçãs, acumular pontos e alcançar o maior recorde possível sem colidir com as paredes ou com o próprio corpo. 🎮

## 📋 Sobre o projeto

O **Snake** é uma aplicação web interativa que resgata a experiência do clássico jogo da cobrinha com uma interface moderna, responsiva e visualmente agradável.

O projeto foi desenvolvido com foco em simplicidade, desempenho, acessibilidade e experiência do usuário (UX/UI), oferecendo controles para computadores e dispositivos móveis.

### ✨ Principais funcionalidades

- 🎯 **Sistema de pontuação:** ganhe 10 pontos a cada maçã coletada.
- 🏆 **Recorde persistente:** o melhor resultado fica salvo no navegador utilizando `localStorage`.
- ⚡ **Velocidade progressiva:** a cobrinha fica mais rápida conforme a pontuação aumenta.
- ⏸️ **Pausar e continuar:** interrompa a partida e retome de onde parou.
- 🔄 **Reiniciar partida:** jogue novamente após o fim da partida.
- 💻 **Controles para computador:** utilize as setas do teclado ou as teclas WASD.
- 📱 **Controles para dispositivos móveis:** botões direcionais aparecem em telas menores.
- 🎨 **Interface moderna:** tema escuro, cores vibrantes, efeitos visuais e indicadores de desempenho.
- 🛡️ **Prevenção de movimentos inválidos:** a cobrinha não pode inverter diretamente a direção em 180 graus.
- 👁️ **Pausa automática:** a partida é pausada quando a janela perde o foco ou a página fica oculta.

## 🛠️ Tecnologias aplicadas

### 🌐 HTML5

Responsável pela estrutura e organização dos elementos da aplicação.

Principais recursos utilizados:

- Estrutura semântica com elementos como `main`, `header` e `section`.
- Elemento `canvas` para a área de jogo.
- Botões interativos para iniciar, pausar e controlar a partida.
- Elementos HTML para exibir pontuação, recorde e velocidade.
- Atributos de acessibilidade, como `aria-label`.

### 🎨 CSS3

Responsável pela identidade visual, estilização e adaptação da interface a diferentes tamanhos de tela.

Principais recursos utilizados:

- Variáveis CSS para padronização das cores.
- Flexbox e CSS Grid para organização dos elementos.
- Gradientes, sombras e bordas arredondadas.
- Media queries para responsividade.
- Transições para melhorar a experiência de interação.
- `prefers-reduced-motion` para respeitar a preferência do usuário por animações reduzidas.
- Layout adaptável para computadores e dispositivos móveis.

### ⚙️ JavaScript (Vanilla JS)

Responsável pela lógica, regras e funcionamento do jogo, sem dependência de bibliotecas ou frameworks externos.

Principais recursos utilizados:

- Manipulação do DOM para atualizar os elementos da interface.
- Gerenciamento do estado da partida.
- Controle de movimentos e detecção de colisões.
- Geração aleatória da posição das maçãs.
- Cálculo da pontuação e progressão da velocidade.
- Eventos de teclado e interação com botões.
- `requestAnimationFrame` para atualização contínua do jogo.
- `localStorage` para persistência do recorde.
- `try/catch` para tratar possíveis falhas de acesso ao armazenamento local.
- Funções para reiniciar, pausar, continuar e finalizar a partida.

### 🖌️ Canvas API

Utilizada para desenhar e atualizar os elementos gráficos do jogo diretamente no navegador.

O tabuleiro, a cobrinha e as maçãs são renderizados por meio da API Canvas 2D, permitindo controlar cores, formas, sombras, grade e detalhes visuais.

### 💾 Web Storage API

A API de armazenamento local é utilizada por meio de `localStorage` para salvar o recorde do jogador no navegador.

A pontuação máxima é armazenada com a chave `snake-best`, permitindo recuperá-la em visitas posteriores no mesmo navegador e origem, desde que os dados não sejam apagados.

## 🎮 Como jogar

### 1. Inicie a partida

Abra o arquivo `index.html` em um navegador moderno e clique no botão **Iniciar partida**.

### 2. Controle a cobrinha

Utilize os controles abaixo para movimentar a cobrinha pelo tabuleiro.

| Ação | Teclas |
|---|---|
| ⬆️ Mover para cima | `↑` ou `W` |
| ⬇️ Mover para baixo | `↓` ou `S` |
| ⬅️ Mover para a esquerda | `←` ou `A` |
| ➡️ Mover para a direita | `→` ou `D` |
| ⏸️ Pausar ou continuar | `Espaço` |
| ▶️ Iniciar ou reiniciar | Botão na tela |
| ▶️ Iniciar pelo teclado | `Enter`, na tela inicial ou após o fim do jogo |

Em celulares e outros dispositivos com telas menores, utilize os botões direcionais exibidos abaixo do tabuleiro. 📱

### 3. Colete as maçãs 🍎

Movimente a cobrinha até alcançar uma maçã.

- Cada maçã vale **10 pontos**.
- A cobrinha cresce a cada maçã coletada.
- Uma nova maçã aparece em uma posição livre do tabuleiro.
- A velocidade aumenta progressivamente conforme você acumula pontos.

### 4. Evite as colisões 💥

A partida termina quando a cabeça da cobrinha colide com uma das paredes ou com o próprio corpo.

**Dica:** planeje seus movimentos com antecedência, principalmente quando a cobrinha estiver maior e mais rápida.

### 5. Bata seu recorde 🏆

Acompanhe os indicadores apresentados acima do tabuleiro:

- **Pontuação:** pontos acumulados na partida atual.
- **Recorde:** maior pontuação registrada no navegador.
- **Velocidade:** multiplicador que aumenta conforme o jogo fica mais rápido.

Quando a partida terminar, clique em **Jogar novamente** para tentar superar seu melhor resultado.

## 🧠 Como funciona a lógica do jogo

O funcionamento é dividido em etapas:

1. **Inicialização:** cria a cobrinha, define sua direção inicial e posiciona a primeira maçã.
2. **Entrada do jogador:** captura os comandos do teclado ou dos botões direcionais.
3. **Movimentação:** atualiza a posição da cabeça e do corpo da cobrinha.
4. **Detecção de colisões:** verifica se houve contato com as paredes ou com o próprio corpo.
5. **Coleta de alimentos:** aumenta a pontuação, expande a cobrinha e gera outra maçã.
6. **Ajuste de velocidade:** reduz progressivamente o intervalo entre os movimentos.
7. **Renderização:** redesenha o tabuleiro e os elementos gráficos.
8. **Persistência:** salva o novo recorde quando a pontuação máxima é superada.
9. **Gerenciamento da partida:** controla os estados de início, execução, pausa e fim de jogo.

O tabuleiro utiliza uma grade de **24 × 24 células**, enquanto o elemento `canvas` possui dimensões internas de 480 × 480 pixels.

A movimentação é controlada por um intervalo que começa em 145 milissegundos e pode chegar a um mínimo de 68 milissegundos, aumentando o desafio gradualmente.

## 📁 Estrutura do projeto

O projeto está concentrado em um único arquivo HTML, facilitando sua execução e distribuição.

```text
snake-game/
└── index.html
    ├── HTML5 — estrutura da aplicação
    ├── CSS3 — estilos e responsividade
    └── JavaScript — regras e lógica do jogo
```

Essa organização elimina a necessidade de configurar um ambiente de desenvolvimento complexo ou instalar dependências externas.

## 🚀 Como executar o projeto

### Opção 1 — Abrir diretamente

1. Baixe ou copie o arquivo `index.html` para uma pasta do computador.
2. Localize o arquivo no Explorador de Arquivos.
3. Abra-o com dois cliques.
4. O jogo será carregado no navegador padrão.
5. Clique em **Iniciar partida** e divirta-se!

### Opção 2 — Utilizar o Visual Studio Code

1. Abra a pasta do projeto no Visual Studio Code.
2. Abra o arquivo `index.html`.
3. Execute-o utilizando a extensão Live Server, caso esteja instalada.
4. Acesse o endereço local fornecido pela extensão.

**Observação:** o jogo não exige conexão com a internet para executar sua lógica principal. O recorde fica armazenado localmente no navegador e não é sincronizado automaticamente entre dispositivos ou navegadores diferentes.

## 📱 Compatibilidade

O projeto foi desenvolvido para funcionar em navegadores modernos que ofereçam suporte a HTML5, CSS3, JavaScript, Canvas 2D e `localStorage`.

A interface se adapta a telas menores, disponibilizando controles direcionais para dispositivos móveis.

## 🔒 Privacidade e armazenamento

- 🔐 Não é necessário criar uma conta.
- 🌐 Não há necessidade de comunicação com um servidor para jogar.
- 💾 O recorde é armazenado localmente no navegador.
- 📡 O código do jogo não implementa envio de pontuação para serviços externos.

O armazenamento pode variar conforme as configurações de privacidade do navegador e a forma como o arquivo é aberto.

## 🔮 Possíveis melhorias futuras

O projeto pode ser expandido com novos recursos, como:

- 🔊 Efeitos sonoros para movimentos, coleta de maçãs e colisões.
- 🎵 Música de fundo com controle de volume.
- 🎨 Temas visuais alternativos.
- 🥇 Ranking de jogadores.
- 🎚️ Seleção de dificuldade.
- ⏱️ Cronômetro e desafios por tempo.
- 🏅 Conquistas e objetivos especiais.
- 📊 Estatísticas de partidas anteriores.
- 🌍 Publicação online por meio de GitHub Pages ou outra plataforma de hospedagem estática.

## 👨‍💻 Conceitos demonstrados

Este projeto demonstra a aplicação prática de conceitos importantes do desenvolvimento Front-End:

- Estruturação de páginas com HTML5.
- Estilização responsiva com CSS3.
- Programação orientada a eventos com JavaScript.
- Manipulação do DOM.
- Desenho gráfico com Canvas API.
- Lógica de jogos e gerenciamento de estados.
- Detecção de colisões e movimentação em grade.
- Persistência de dados no navegador.
- Princípios de acessibilidade e experiência do usuário.

## 📄 Licença

Nenhum arquivo de licença específico foi identificado no projeto fornecido. Caso o jogo seja publicado ou distribuído publicamente, recomenda-se definir uma licença apropriada e incluir o respectivo arquivo no repositório.

---

Feito com ❤️ utilizando **HTML5, CSS3 e JavaScript puro**.

🐍 **Prepare-se, colete as maçãs e supere seu próprio recorde!** 🎮🏆
