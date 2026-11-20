# Git para Dados

Material gratuito do QG da Engenharia de Dados. Você recebeu porque comentou **GIT**.

## Como usar este material

1. Instale o Git → [git-scm.com](https://git-scm.com/downloads)
2. Use este README como cola → os comandos estão na ordem do dia a dia
3. Copie o [.gitignore](.gitignore) para os seus projetos de dados

## Configuração (uma vez só)

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

## Começar um projeto

```bash
git init                         # cria o repositório na pasta atual
git clone URL                    # ou baixa um que já existe
```

## O fluxo do dia a dia

Editar → `git add` → `git commit` → `git push`

```bash
git status                       # o que mudou?
git add arquivo.py               # prepara um arquivo
git add .                        # prepara tudo
git commit -m "adiciona carga de clientes"
git push                         # envia para o GitHub
git pull                         # traz o que os outros enviaram
```

## Branches

```bash
git switch -c feature/carga-vendas   # cria e entra na branch
git switch main                      # volta para a main
git branch                           # lista as branches
git merge feature/carga-vendas       # junta na branch atual
```

## Fluxo com Pull Request

1. Crie uma branch → `git switch -c feature/nome`
2. Faça commits pequenos
3. `git push -u origin feature/nome`
4. No GitHub → **Compare & pull request**
5. Revisão → merge na main

## Desfazer

```bash
git restore arquivo.py           # descarta mudança não commitada
git restore --staged arquivo.py  # tira do add
git commit --amend               # corrige a mensagem do último commit (antes do push)
git revert HASH                  # cria um commit que desfaz outro (seguro depois do push)
```

## Ver o histórico

```bash
git log --oneline --graph
git diff                         # o que mudou e ainda não foi para o add
```

## Regras para projetos de dados

→ Nunca suba **senha** ou **.env** → use o `.gitignore`
→ Nunca suba **dados grandes** (CSV, Parquet) → guarde no data lake
→ Suba um **.env.example** com as variáveis sem os valores
→ Mensagens de commit dizem **o que** mudou: "adiciona teste de nulos em pedidos"

## Material completo

[Git-GitHub-Guia-Pratico](https://github.com/Walterbiel/Git-GitHub-Guia-Pratico)

## QG da Engenharia de Dados

Este material é uma amostra do que você encontra no QG.

→ Trilha completa do zero ao sênior
→ Projetos reais para o portfólio
→ Comunidade para tirar dúvidas

Acesse → [qg-engenharia-de-dados.com.br](https://qg-engenharia-de-dados.com.br)
YouTube → [@gonzagadosdados](https://www.youtube.com/@gonzagadosdados)
