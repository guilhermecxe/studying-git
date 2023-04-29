# Colaborando

**`$ git init <project-name>`**

Esse comando cria um repositório com o nome dado.


---
**`$ git init`** ou **`$ git init <path>`**

Esse comando cria um repositório a partir de uma pasta já existente com um projeto.

---
**`$ git clone URL`** ou **`$ git clone <path>`** 

Usado para clonar um repositório remoto (usando a URL) ou local (usando path). O repositório é criado com o mesmo nome do repositório original, caso queira usar um outro nome basta escrevê-lo depois da URL ou do path.

---
**`$ git remote`** ou **`$ git remote -v`**

Mostra onde o repositório está salvo remotamente, por exemplo, de onde os códigos foram clonados. Pode haver mais de 1 local remoto.

`origin` é nome dado para o local de onde o repositório foi clonado.

---
**`git remote add <remote-name> URL`**

Para adicionar uma localização remota do repositório com o nome dado.

---
**`git remote rm <remote-name>`**

Para remover a localização remota do repositório com o nome dado.

---
**`git pull <remote-name> <branch-name>`**

Isso obtém, para a branch atual, as alterações mais recentes da branch com o nome dado do local remoto informado.

Às vezes esse comando pode dar erro por haver alterações locais não salvas ainda. A solução é salvá-las ou descartá-las.

---
**`git push <remote-name> <branch-name>`**

Para enviar as alterações feitas localmente para o repositório remoto especificado e para a branch especificada dele.

Essa operação, às vezes, pode dar conflito com o repositório remoto. Para evitar isso o Git não permite que um push seja feito sem que haja um merge do trabalho local, que está tentando ser salvo, com o trabalho atual remoto. Então caso haja esse erro a solução é dar `git pull` do local remoto que assim será feito um `merge` com o trabalho local e aí sim o trabalho local poderá realizador o push.