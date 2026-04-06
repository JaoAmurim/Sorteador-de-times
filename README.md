# ⚽ Sorteador de Times

Um aplicativo web responsivo e intuitivo para sortear times de forma justa e divertida, com suporte a múltiplos esportes e sistema de rodadas completo.

## 🎯 Funcionalidades

### 📱 Seleção de Esporte
- **Futebol** (com modalidades: Quadra, Campo, Society)
- **Vôlei** (6 ou 12 jogadores)
- **Basquete** (8 ou 12 jogadores)

### 👥 Gerenciamento de Jogadores
- ✅ Adicionar jogadores um por um
- ✅ Importação em lote (colar lista)
- ✅ Suporte a múltiplos formatos (bullets, números, dashes)
- ✅ Remover jogadores
- ✅ Contador de participantes
- ✅ Campo "chamar jogador" após sorteio (caso falte jogadores)

### 🎲 Sorteio de Times
- ✅ Distribuição automática e equilibrada
- ✅ Animação visual durante sorteio
- ✅ Indicador de progresso (barra + bolinha girante)
- ✅ Suporte a 2-4 times (configuração automática)

### 🏆 Sistema de Rodadas (Tournament)
- ✅ Sorteia automaticamente quem joga próximo
- ✅ Registra resultado de cada partida
- ✅ 3 opções: Time A/B/C/D venceu ou Empate
- ✅ **Rotação automática** quando empatam
- ✅ Histórico completo de rodadas
- ✅ Contagem de vitórias por time

### 🎨 Design & UX
- ✅ Interface moderna e intuitiva
- ✅ Tema verde/amarelo/vermelho profissional
- ✅ Animações fluidas otimizadas
- ✅ **100% Responsivo** (mobile, tablet, desktop)
- ✅ Efeito de pegadas do mouse
- ✅ Notificações visual (toast)

## 📋 Requisitos

- Navegador moderno com suporte a ES6+
- Nenhuma dependência externa
- Python 3.x (apenas para servir localmente)

## 🚀 Como Usar

### Opção 1: Servidor Local (Recomendado)

```bash
cd /path/to/Teste_APP
python -m http.server 8000
```

Abra: **http://localhost:8000/sorteador_de_time.html**

### Opção 2: Arquivo Local

Abra `sorteador_de_time.html` diretamente no navegador.

> ⚠️ Nota: Alguns recursos podem ter limitações devido à política de segurança CORS ao usar file:// protocol.

## 📱 Fluxo do Aplicativo

```
1. Selecione o Esporte
   ↓
2. Escolha Modalidade (se Futebol)
   ↓
3. Adicione Jogadores
   ↓
4. Sorteie os Times
   ↓
5. Registre Resultados das Partidas
   ↓
6. Sistema rotaciona times automaticamente
```

## 🎮 Como Jogar

### Tela 1: Esporte
Selecione qual esporte será jogado (Futebol, Vôlei, Basquete).

### Tela 2: Modalidade (Futebol)
Para Futebol, escolha entre:
- **Quadra**: 5 jogadores (futsal)
- **Campo**: 11 jogadores (futebol 11)
- **Society**: 7 jogadores

### Tela 3: Jogadores
```
Digite nomes localmente:
- João
- Maria
- Pedro

Ou cole uma lista:
- João
- Maria  
- Pedro
```

Clique **"Adicionar"** ou pressione **Enter**.

### Tela 4: Sorteio
Clique em **"🎲 Sortear Times"** para distribuir.

O sistema mostrará:
- ✅ Times em campo (em verde)
- ⏸️ Próximos a jogar (em cinza)

### Tela 5: Resultado
Após a partida, selecione quem ganhou:
- 🟢 **Time A/B/C/D Venceu**: Time fica, adversário vai para banco
- 🤝 **Empate**: Todos os times em campo saem, próximos entram

## 🎨 Paleta de Cores

| Cor | Código | Uso |
|-----|--------|-----|
| Verde | #22C55E | Primário, Time A, Vitórias |
| Verde Escuro | #16A34A | Hover, Ativo |
| Amarelo | #EAB308 | Time B, Atenção |
| Vermelho | #EF4444 | Time C, Erro |
| Azul | #6366F1 | Time D |
| Branco | #FFFFFF | Background |

## 📱 Responsividade

| Breakpoint | Dispositivo | Ajustes |
|-----------|------------|---------|
| < 360px | Ultra-mobile | Font 14px, botões 100%, single column |
| 360-480px | Mobile pequeno | Font 14-16px, containers 1 coluna |
| 481-768px | Móvel/Tablet | Font 16px, grids 2 colunas |
| 769-1024px | Tablet landscape | Font 17px, grids até 3 colunas |
| > 1024px | Desktop | Font 18px, layout completo |

## ⚙️ Tecnologias

- **HTML5**: Estrutura semântica
- **CSS3**: Animações, Flexbox, Grid, Media Queries
- **JavaScript Vanilla**: Lógica pura sem frameworks
- **Python**: Servidor http.server para desenvolvimento

## 📦 Estrutura de Arquivos

```
Teste_APP/
├── sorteador_de_time.html    ← Aplicação completa
└── README.md                 ← Este arquivo
```

## 🎬 Animações Implementadas

- `fadeIn`: Transições entre telas
- `slideDown`: Entrada de modal
- `slideInLeft/Right`: Elementos de times
- `slideInUp`: Botões de resultado
- `spinBall`: Esfera girando no carregamento
- `progressFill`: Barra de progresso (0% → 100%)
- `float`: Pontinhos flutuantes
- `scaleInUp`: Containers de sorteio

## ⚡ Performance

- ✅ Código minificado
- ✅ Sem dependências externas
- ✅ Animações otimizadas (will-change)
- ✅ Carregamento instantâneo
- ✅ Funciona offline

## 🐛 Troubleshooting

**P: O app não carrega?**  
R: Use o servidor local: `python -m http.server 8000`

**P: Os times não estão equilibrados?**  
R: O algoritmo distribui proporcionalmente. Com 13 jogadores em 3 times: 5, 4, 4.

**P: Como adicionar mais jogadores após sorteio?**  
R: Clique no campo "Digite o nome do convidado..." na seção cada time.

**P: Posso resetar tudo?**  
R: Clique em **"🔄 Começar Novamente"** na tela de resultados.

## 💡 Dicas

- 📋 Use copiar/colar para adicionar múltiplos jogadores
- 🎲 Sorteie sempre após confirmar todos os jogadores
- 📊 O histórico de rodadas fica armazenado na sessão
- 🔄 A rotação é automática - empates eliminam todos em campo
- 📱 Funciona perfeitamente em qualquer dispositivo

## 🔄 Rotina de Jogo Exemplar

```
1. Sorteio Inicial: Times A vs B
   
2. Resultado: A venceu

3. Próximo: A continua (Playing) / B sai / C entra

4. Sorteio: A vs C

5. Resultado: Empate

6. Próximo: Ambos A e C saem / D e B entram
   (Rotação automática!)
```

## 📞 Suporte

Para reportar bugs ou sugerir melhorias, verifique o console do navegador (F12).

## 📄 Licença

Projeto livre para uso pessoal e comercial.

---

**Versão**: 1.0  
**Última Atualização**: Abril de 2026  
**Desenvolvedor**: GitHub Copilot
