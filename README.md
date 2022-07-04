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


## Referências

- [Usando Git Direito | Limpando seus Commits!](https://youtu.be/6OokP-NE49k)
- [Git: Documentation](https://git-scm.com/docs)
