# NexoGeo BTzap — Instalador para Windows

Instalador do painel **NexoGeo BTzap** (servidor local de WhatsApp/participações) para Windows 10/11 x64.

## Download

Baixe sempre a versão mais recente:

**https://github.com/schummerdev/btdownload/releases/latest**

Arquivo: `NexoGeo-BTzap-Setup-1.0.0.exe` (~187 MB)

Não é necessário ter Node.js instalado — o runtime vai embutido no instalador.

## Como instalar

1. Baixe o `NexoGeo-BTzap-Setup-1.0.0.exe`.
2. Dê duplo clique.
3. Opcional: marque "Criar atalho na Área de Trabalho" e "Iniciar junto com o Windows".
4. Clique em **Instalar** e aguarde (a extração leva alguns segundos).
5. Abra pelo atalho **NexoGeo BTzap** no Menu Iniciar.

O painel abre em **http://localhost:3000**.

> O Windows pode exibir aviso do SmartScreen ("Aplicativo não reconhecido") porque o
> executável não tem assinatura digital. Use **Mais informações > Executar assim mesmo**.

## O que o instalador faz

| Item | Detalhe |
|---|---|
| Pasta de instalação | `%LOCALAPPDATA%\Programs\NexoGeo BTzap` |
| Permissão | Por usuário, **sem** pedir senha de administrador |
| Runtime | Node.js embutido (`runtime\node.exe`) |
| Atalhos | Menu Iniciar e, opcionalmente, Área de Trabalho |
| Desinstalação | Configurações > Aplicativos, ou atalho "Desinstalar" |
| Atualização | Rodar o novo instalador por cima preserva banco e configurações |

## Primeiro acesso

Este pacote é distribuído **sem dados**: o banco vem vazio e os tokens do `.env`
são gerados automaticamente. Depois de instalar:

1. Abra o painel em http://localhost:3000
2. Vá em **Configurações** e informe os dados da sua instância BTzap
   (nome da instância, token da API e URL do servidor)
3. Ative a instância e aguarde o setup automático (túnel + webhook)

## Arquivos importantes na instalação

- `prisma\dev.db` — banco de dados (SQLite)
- `.env` — tokens e configurações
- `public\uploads` — imagens enviadas pelo painel
- `backup-banco.bat` — cria cópia do banco em `backups\`

## Desinstalar

Configurações do Windows > Aplicativos > NexoGeo BTzap > Desinstalar.

Uma cópia do banco é salva em `Documentos\NexoGeo-backup-dev.db` antes da remoção.

## Requisitos

- Windows 10 ou 11, 64 bits
- Porta 3000 livre

## Observação

Este repositório contém apenas o instalador e esta documentação. O código-fonte
não é publicado aqui.
