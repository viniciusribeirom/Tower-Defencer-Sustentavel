# 🏰 Tower Defense – v2.0

Tower Defense profissional em Java com LWJGL 2 e Slick2D.

## 📋 Requisitos

- **Java 8+** (JDK recomendado)
- **LWJGL 2.9.x** + **Slick2D** + **lwjgl_util**
- **IDE**: Eclipse, IntelliJ IDEA, ou VS Code

## 📁 Estrutura do Projeto

```
src/          → Código-fonte Java
res/          → Assets (sprites, tiles, sons)
├── *.png     → Texturas do jogo
└── sounds/   → Efeitos sonoros (adicione seus arquivos)
```

## 🎮 Como Executar

### Opção 1: IDE (Eclipse/IntelliJ)
1. Importe como projeto Java existente.
2. Adicione ao Build Path:
   - `lwjgl.jar`
   - `lwjgl_util.jar`
   - `slick.jar`
3. Configure **Native Library Location** para a pasta `native/` do LWJGL.
4. Execute `data.Boot` como classe principal.

### Opção 2: Linha de Comando
```bash
javac -cp "lib/*:src" -d bin $(find src -name "*.java")
java -Djava.library.path=native/ -cp "lib/*:bin:data" data.Boot
```

## 🕹️ Controles

| Tecla | Ação |
|-------|------|
| **1** | Modo Build – Torre de Fogo |
| **2** | Modo Build – Torre de Gelo |
| **3** | Modo Build – Torre Elétrica |
| **C** | Modo Build – Torre Normal |
| **U** | Upgrade na torre sob o mouse |
| **RMB** | Vender torre / Cancelar build |
| **ESC / P** | Pausar jogo |
| **SPACE** | Pular intervalo entre waves |
| **LMB** | Construir torre (em build mode) |

## ⚡ Sistemas Implementados

- ✅ 4 tipos de torres com upgrades (3 níveis)
- ✅ 4 classes de inimigos (Verde, Vermelho, Azul, Boss)
- ✅ Sistema de waves procedural com dificuldade escalonada
- ✅ Efeitos de status (DOT de fogo, slow de gelo, chain lightning)
- ✅ Partículas visuais (morte, construção, venda, sparks)
- ✅ Save/Load de partidas
- ✅ High Score ranking persistente
- ✅ HUD com barras de progresso
- ✅ Preview de alcance e validação de build
- * Música e efeitos sonoros - trabalhando nisso

## 🛠️ Tecnologias & Padrões

- **POO**: Abstração, Herança, Encapsulamento, Polimorfismo
- **Factory Pattern**: `TowerFactory`
- **Template Method**: `State` / `Entity`
- **Singleton**: `StateManager`
- **DTO**: `GameSnapshot`, `TowerData`

## 📄 Licença

Projeto educacional. Assets criado como IA e referencia do canal inde programer.
