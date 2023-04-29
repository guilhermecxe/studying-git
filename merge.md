# Merge

Quando unimos, ou damos um merge, entre uma branch (chamada de `source`) e outra (chamada de `destination`) o Git incorpora as mudanças da branch `source` na outra branch e, se não houver conflitos, é criado um novo commit de `destination` com a união das duas branches.

O comando para o merge de duas branches é `$ git merge <source> <destination>`

Quando houver conflito o Git informará no momento do merge, além disso, é deixada uma mensagem, no caso de arquivos .txt, onde houve o conflito (não sei para outros tipos de arquivo). Quando esse conflito é constatado é necessário fazer as alterações necessárias, salvá-las e dar o merge novamente.