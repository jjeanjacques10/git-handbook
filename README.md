# Git Handbook

Guia de bolso com comandos mais avançados para utilizar o git.

- Mensagem de commit errada

``` bash
git commit -m "Mensagem de commit errada"
git commit -m "Mensagem de commit correta" --amend
```

- Apaga os commits feitos, mas não perde o que foi modificado

``` bash
git reset --soft HEAD~3 # Com a flag soft ele não remove os commits anteriores
git reset HEAD~3 # Apenas remove os últimos commits
```

- Para abrir o modo interativo, basta digitar o comando:

``` bash
git rebase -i HEAD~3 # Fara isso nos últimos 3 commits
```