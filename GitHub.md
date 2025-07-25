# GitHub

## Introdução ao GitHub

### O que é o GitHub?

O GitHub é uma plataforma online que permite hospedar e gerenciar repositórios Git.  
Ele facilita o compartilhamento de código, a colaboração entre desenvolvedores e o controle de versão de forma eficiente.

---

## Configuração do Git com GitHub

Antes de interagir com repositórios no GitHub, é importante configurar suas credenciais:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seuemail@gmail.com"
```

---

## Conectando ao GitHub

### Adicionar repositório remoto

```bash
git remote add origin <URL-do-repositório>
```

> Conecta seu repositório local ao GitHub usando a URL do repositório remoto.

---

## Clonando repositórios

```bash
git clone <URL-do-repositório>
```

> Clona um repositório GitHub existente para o seu computador.

---

## Sincronizando mudanças

```bash
git pull
```

> Baixa e aplica automaticamente as últimas alterações do repositório remoto à sua branch atual.

```bash
git fetch
```

> Baixa as alterações do repositório remoto **sem aplicá-las automaticamente**.

---

## Enviando alterações

```bash
git push -u origin main
```

> Envia os commits da branch `main` local para o repositório remoto no GitHub.

---

## Comandos Avançados

### `git stash`

```bash
git stash
```

> Salva temporariamente alterações não commitadas para que você possa trabalhar em outra tarefa.

```bash
git stash list
```

> Lista todos os stashes salvos.

```bash
git stash pop
```

> Restaura o stash mais recente e o remove da lista.

```bash
git stash apply stash@{x}
```

> Aplica um stash específico **sem removê-lo** da lista.

```bash
git stash drop stash@{x}
```

> Remove um stash específico da lista.

---

### `git rebase`

```bash
git rebase
```

> Permite aplicar as alterações de uma branch sobre outra, reorganizando o histórico de commits.

---

### `git cherry-pick`

```bash
git cherry-pick <hash-do-commit>
```

> Aplica um commit específico de uma branch em outra, sem trazer toda a sequência de commits.

---

### `git revert`

```bash
git revert <hash-do-commit>
```

> Cria um novo commit que desfaz as alterações feitas por um commit anterior.

---

### `git reset --hard`

```bash
git reset --hard <hash-do-commit>
```

> Volta o repositório completamente para o estado de um commit anterior, apagando **todas as alterações posteriores**.

---

## 🔚 Dica Final

Utilize o GitHub com responsabilidade, mantendo seu histórico limpo, utilizando mensagens claras nos commits e trabalhando com branches para facilitar o fluxo de trabalho em equipe.