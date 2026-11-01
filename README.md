# Wasteland BR Launcher

Launcher oficial do servidor **Wasteland BR** (Project Zomboid, Build 42): entra direto no servidor, salva login e senha,
otimiza o jogo (aba Ajustes), mostra o status ao vivo e a Sala VIP.

**Baixar:** [Wasteland_BR_Launcher.exe (última versão)](https://github.com/Maiky636/wasteland-launcher/releases/latest/download/Wasteland_BR_Launcher.exe)

> O Windows pode avisar que o programa é desconhecido (ele não tem assinatura paga). Clique em
> **Mais informações → Executar assim mesmo**. O launcher só mexe nos arquivos do próprio Project Zomboid.

---

## Para a staff: como usar este repositório

Todo launcher aberto lê o `feed.json` deste repositório a cada 5 minutos. O que mudar nele aparece no launcher de
todos os jogadores, **sem mandar .exe novo**.

### Mudar avisos, notícias, regras, reinícios ou preços
Clique em `feed.json` → ícone de **lápis** → edite → **Commit changes**.

| Campo        | O que faz |
|--------------|-----------|
| `alertas`    | Frases do letreiro **ALERTA EBS** no rodapé. |
| `noticias`   | Aba **Rádio** e os 3 cartões do Início (as 4 primeiras). |
| `regras`     | Aba **Info**. `TÍTULO: texto` deixa o título em negrito. |
| `reinicios`  | Horas dos reinícios (horário de Brasília) para a contagem no topo. |
| `colecao`    | ID da coleção da Steam Workshop com os mods do servidor. |
| `loja`       | (opcional) troca os produtos da Sala VIP sem recompilar. |
| `launcher`   | Versão nova do launcher (abaixo). |

### Lançar uma versão nova do launcher
1. **Releases → Draft a new release**, tag `v2.5` (o número novo), anexe o `.exe` novo com o nome
   **`Wasteland_BR_Launcher.exe`** e publique.
2. No `feed.json`, troque só o número: `"launcher": { "versao": "2.5", ... }` (o link já aponta sempre para a última release).
3. Quem abrir o launcher vê **NOVA VERSÃO** e atualiza com um clique.
