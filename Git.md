# Git

## Introdução ao Git

### O que é Git?

Git é um sistema de controle de versão distribuído. Ele permite que desenvolvedores salvem, revertam e colaborem em versões de código-fonte de forma eficiente.

---

## Conceitos-chave

- **Repositório**: Local onde o histórico do projeto é armazenado.
- **Commit**: Uma "foto" do estado atual dos arquivos.
- **Branch**: Ramificação independente do histórico.
- **Merge**: Junção de branches.
- **HEAD**: Referência ao commit atual.

---

## Configurações Iniciais

Para configurar seu nome e e-mail globalmente (usado nos commits):

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@exemplo.com"
```

---

## Iniciando um repositório Git

```bash
mkdir novo_projeto         # Cria uma nova pasta para o projeto
cd novo_projeto            # Acessa a pasta do projeto
git init                   # Inicializa um repositório Git
ls -a                      # Verifica se o diretório oculto .git foi criado
```

---

## Verificando o status

```bash
git status
```

Esse comando exibe o estado atual do repositório, incluindo:

- Branch atual
- Arquivos não rastreados
- Modificações pendentes
- Alterações já adicionadas (staged)

---

## Adicionando arquivos

```bash
git add .              # Adiciona todos os arquivos modificados ao staging area
git add nome_arquivo   # Adiciona apenas o arquivo específico
```

---

## Criando commits

```bash
git commit -m "Mensagem descritiva"
```

Um commit registra as alterações no repositório. Deve conter uma mensagem clara do que foi feito.

---

## Visualizando o histórico de commits

```bash
git log                # Exibe todos os commits detalhadamente
git log --oneline      # Exibe commits resumidamente (1 linha por commit)
```

### Outras opções úteis:

```bash
git log --graph                    # Exibe o histórico em forma de gráfico
git log --author="Nome"           # Filtra commits por autor
git log -n 5                      # Mostra os 5 commits mais recentes
git log --since="2 days ago"     # Mostra commits dos últimos 2 dias
```

---

## Trabalhando com Branches

Branches permitem trabalhar em funcionalidades isoladas sem afetar o código principal (geralmente na branch `main`).

### Comandos úteis:

```bash
git branch nome-da-branch         # Cria uma nova branch
git checkout nome-da-branch       # Muda para a branch criada
git switch nome-da-branch         # (Versão mais recente do Git)
git checkout -b nome-da-branch    # Cria e troca para a branch
git switch -c nome-da-branch      # (Git mais recente, mesma função)
```

### Visualização de branches:

```bash
git branch        # Lista as branches locais
git branch -r     # Lista branches remotas
git branch -a     # Lista todas (locais + remotas)
```

### Mesclando branches:

```bash
git checkout main                # Volta para a branch principal
git merge nome-da-branch         # Mescla a branch ao código principal
```

> ⚠️ Se houver conflitos, o Git solicitará a resolução antes de concluir a mesclagem.

---

## Excluindo branches

```bash
git branch -d nome-da-branch               # Exclui uma branch local
git branch -D nome-da-branch               # Força exclusão local
git push origin --delete nome-da-branch    # Exclui uma branch remota
```

---

## 📌 Dica final

Sempre escreva mensagens de commit claras e significativas, e use branches para manter seu projeto organizado, especialmente quando colaborar com outras pessoas.