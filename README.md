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
git reset HEAD~3 # Apenas remove os últimos 3 commits
```

- Apaga apenas o último commit feito sem remover o código modificado

``` bash
git reset --soft HEAD^
```

- Para abrir o modo interativo, basta digitar o comando:

``` bash
git rebase -i HEAD~3 # Fara isso nos últimos 3 commits
```

Irá abrir o arquivo de edição para o modo interativo.
    pick 054cf5f fixing
    pick 9c54854 fixing
    pick 38d7aec add rebase

    # Rebase f5fc633..38d7aec onto f5fc633 (3 commands)
    #
    # Commands:
    # p, pick <commit> = use commit
    # r, reword <commit> = use commit, but edit the commit message
    # e, edit <commit> = use commit, but stop for amending
    # s, squash <commit> = use commit, but meld into previous commit
    # f, fixup [-C | -c] <commit> = like "squash" but keep only the previous
    #                    commit's log message, unless -C is used, in which case
    #                    keep only this commit's message; -c is same as -C but
    #                    opens the editor
    # x, exec <command> = run command (the rest of the line) using shell
    # b, break = stop here (continue rebase later with 'git rebase --continue')
    # d, drop <commit> = remove commit
    # l, label <label> = label current HEAD with a name
    # t, reset <label> = reset HEAD to a label
    # m, merge [-C <commit> | -c <commit>] <label> [# <oneline>]
    # .       create a merge commit using the original merge commit's
    # .       message (or the oneline, if no original merge commit was
    # .       specified); use -c <commit> to reword the commit message
    #
    # These lines can be re-ordered; they are executed from top to bottom.
    #
    # If you remove a line here THAT COMMIT WILL BE LOST.
    #
    # However, if you remove everything, the rebase will be aborted.
    #

- Altera nome da branch

``` bash
# Local
git branch -m <nome-branch>

# Altera branch remota
git push origin --delete <nome-branch>
git push origin -u bugfix
```

- Atualiza branch remota

``` bash
git remote origin set-url <url>
```

## Log

- Exibe o histórico dos últimos commits

``` bash
git log
```

- Exibe histórico de commits de forma resumida em apenas uma linha

``` bash
git log --pretty=oneline

# output
5aedf3372f40d89f6813a428430b564e86ca07d5 (HEAD -> main) add license
84ff2d267214fa53d8c3fbe775f5808435858c4f add references
635edb6c582531c03b1057916a513d59851b2286 add rebase info
2cfe25aa48ed56038a925f165f5f835b946b30e9 add rebase
f5fc633acc731b6f781083fb7f52a10be09a6448 explaining reset
6cfdc6ac39350c0da432f0bef565616c428172dd Mensagem de commit correta
```

## Referências

- [Usando Git Direito | Limpando seus Commits!](https://youtu.be/6OokP-NE49k)
- [Git: Documentation](https://git-scm.com/docs)
