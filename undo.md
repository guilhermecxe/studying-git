# Desfazendo

**`$ git reset HEAD`**

Isso tira os arquivos atualmente na área de preparação. Eu posso especificar um arquivo ou pasta depois de `HEAD`. Posso também não especificar `HEAD` e mesmo assim funcionará da mesma forma.

---

**`git checkout -- <file>`**

Isso descarta as alterações feitas em um arquivo desde o último `git add`. Ou seja, as alterações que não foram para a área de restauração. Eu posso restaurar todo o repositório deixando `<file>` em branco ou usando `.`, mas sempre com `--`.

---

**`git checkout <hash> <file>`**

Isso restaura a versão do arquivo especificado do commit referente ao hash.

---

**`$ git rm <file>`**

Usado para remover um arquivo do repositório e, ao mesmo tempo, colocar essa remoção na área de preparação.

## `.gitignore`

Eu posso adicionar um arquivo chamado `.gitignore` na raiz do diretório e especificar arquivos que devem ser ignorados. Exemplo:

```
build # ignora pastas (e seus conteúdos) ou arquivos chamados "build"
*.mpl # ignora arquivos terminados com ".mpl"
```