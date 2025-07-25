# Criando um Projeto com Git e GitHub

Este guia passo a passo mostra como iniciar um projeto com Git, adicionar arquivos, conectar ao GitHub e utilizar comandos úteis para o controle de versão.

---

## 1. Criando um novo repositório Git

```bash
mkdir meu_projeto
cd meu_projeto
git init
```

> Inicializa um repositório Git local.

---

## 2. Criando um arquivo e adicionando ao Git

```bash
echo "primeiro arquivo" > app.js
git add app.js
git commit -m "Adicionando arquivo inicial"
```

> Isso adiciona `app.js` ao staging e o registra no histórico com um commit.

---

## 3. Conectando ao GitHub

```bash
git remote add origin https://github.com/usuario/meu_projeto.git
git push origin main
```

> Agora o repositório está vinculado ao GitHub e sincronizado com a branch principal.

---

## 4. Criando e alternando para uma nova branch

```bash
git branch nova-feature
git checkout nova-feature
```

> Cria e alterna para a branch `nova-feature`, onde podem ser feitas novas funcionalidades.

---

## 5. Fazendo alterações e commitando na nova branch

```bash
echo "Nova funcionalidade adicionada" >> app.js
git add app.js
git commit -m "Implementando nova funcionalidade"
```

> Isso adiciona e registra as novas alterações no histórico da branch.

---

## 6. Salvando alterações temporárias com `git stash`

Caso precise mudar de tarefa sem perder progresso:

```bash
git stash
```

> Isso guarda as alterações temporariamente. Para recuperá-las:

```bash
git stash pop
```

---

## 7. Sincronizando com repositório remoto e verificando histórico

```bash
git fetch
git log --oneline
```

- `git fetch`: busca atualizações remotas sem aplicá-las.
- `git log --oneline`: mostra o histórico de commits de forma compacta.

---

## 8. Mesclando a branch `nova-feature` na `main`

```bash
git checkout main
git merge nova-feature
```

> Integra as alterações da `nova-feature` na branch principal. Para deletar a branch:

```bash
git branch -d nova-feature
```

---

## 9. Revertendo um commit

Caso um commit tenha causado problemas:

```bash
git revert <hash-do-commit>
```

> Cria um novo commit que desfaz as alterações do commit especificado.

---

## 10. Copiando um commit específico para outra branch

```bash
git cherry-pick <hash-do-commit>
```

> Copia um commit específico para a branch atual sem trazer o histórico completo.

---

## 11. Reaplicando commits com `git rebase`

Para manter um histórico limpo e organizado:

```bash
git checkout nova-feature
git rebase main
```

> Reorganiza os commits da branch `nova-feature` para alinhá-los com a `main`.

---

## 12. Resetando para um estado anterior

Caso precise descartar alterações e voltar para um commit antigo:

```bash
git reset --hard <hash-do-commit>
```

> Remove todas as alterações feitas após esse commit.

---

## ✅ Conclusão

Esse fluxo cobre as principais ações do dia a dia em projetos com Git e GitHub. Trabalhar com branches, commits bem descritos e organização de histórico são boas práticas fundamentais.