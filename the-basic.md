## Básico do Git

- Nada do que é salvo no Git é perdido. Sempre é possível voltar para versões anteriores de programas.
- O Git notifica quando a alteração de uma pessoa conflita com o arquivo de outra pessoa.
- O Git pode sincronizar alterações feitas por diferentes pessoas em diferentes máquinas.

**Projetos do Git tem duas partes:**
- Arquivos e pastas criadas pelo pragramador
- Informações adicionais do Git

Essas duas partes juntas formam um repositório. As informações adicionais do Git ficam em uma pasta chamada ".git" e nunca devem ser modificadas ou alteradas. É lá onde fica o histórico de commits feitos.

---

## Alguns comandos

`$ git status`

Retorna o status de cada arquivo no repositório indicando quais arquivos sofreram alterações desde o último commit, quais estão na "área de preparação" para serem salvos e se existem arquivos novos.

---
`$ git add filename`

Adiciona um arquivo à "área de preparação", antes dele ser submetido a um commit.

---
`$ git commit -m "Program appears to have become self-aware."`

Esse comando faz o commit, ou salva, as alterações na área de preparação com a mensagem que vem depois de `-m`, mensagem esta que é chamada de "log message".

---
`git commit --amend -m "new message"`

Caso haja um erro na mensagem do commit, é possível corrigir com o comando acima.

---
`$ git diff`

Compara as mudanças feitas no repositório desde o último commit.

---
`$ git diff filename`

Para ver apenas as mudanças no arquivo especificado.

---
`$ git diff directory`

Para ver apenas as mudanças na pasta especificada.

---
`$ git diff -r HEAD`

Compara as alterações na área de preparação com o commit mais recente

---
`$ git diff -r HEAD path/to/file`

Usando caminho para comparar apenas 1 arquivo.

*`-r` significa "comparar com uma revisão particular"*

*`HEAD` significa o commit mais recente*

---
`git log`

Este comando mostra um histórico de commits. Cada commit vem no seguinte formato:
```
commit 0430705487381195993bac9c21512ccfb511056d
Author: Rep Loop <repl@datacamp.com>
Date:   Wed Sep 20 13:42:26 2017 +0000

    Added year to report title.
```
Onde `commit` descreve uma chave hash para o commit, depois vem o autor do commit, a data do commit e a log message.

O histórico pode conter muitos commits, assim, às vezes é necessário teclar `espaço` no terminal para visualizar a próxima página de commits. Ou `q` para sair.

É possível também especificar uma pasta ou arquivo no comando para visualizar apenas o histórico de commits da pasta ou arquivo especificado.

Eu posso também usar `git log -<n> <file>` para visualizar as últimas n alterações do arquivo especificado.

---

## Exemplo de resultado de `git diff`
```
$ git diff report.txt
diff --git a/report.txt b/report.txt
index e713b17..4c0742a 100644
--- a/report.txt
+++ b/report.txt
@@ -1,4 +1,5 @@
-# Seasonal Dental Surgeries 2017-18
+# Seasonal Dental Surgeries (2017) 2017-18
+# TODO: write new summary
```

- A primeira linha do resultado mostra o que o output descreve, no caso: alterações no arquivo `report.txt`. As letras `a` e `b` no caminho do arquivo que sofreu alterações indica a primeira (a) e a segunda (b) versão dele.
- A segunda linha mostra chaves relevantes apenas para o armazemento interno do Git.
- A linha começando com `@@` indica onde as mudanças foram feitas e quantas linhas haviam naquela seção e quantas linhas existem agora. No caso, as alterações foram na linha 1, numa seção onde haviam 4 linhas e agora há 5 linhas.
- Depois vem as linhas removidas (-) e as adicionadas (+) do arquivo.

Às vezes, linhas sem - e sem + aparecem apenas para dar contexto às alterações realizadas.