# Git Stash

O comando git stash permite que você salve alterações em um "stash", que é um local temporário no repositório que armazena alterações não commitadas. Isso pode ser útil quando você precisa mudar de branch ou trabalhar em outra tarefa, mas não deseja perder as alterações que ainda não foram commitadas.

## Criando um stash

Para criar um stash, basta executar o comando git stash:

```shell
git stash
```

Isso salva as alterações não commitadas em um novo stash. Você pode criar vários stashes, e cada um receberá um nome único automaticamente. Se você deseja dar um nome personalizado a um stash, pode usar o exemplo abaixo:

```shell
git stash save "Minhas alterações temporárias"
```

## Listando stashes

Para listar todos os stashes em seu repositório, use o comando git stash list:

```shell
git stash list
```

Isso mostra uma lista de todos os stashes, juntamente com seus nomes e mensagens.

## Aplicando um stash

Para aplicar as alterações de um stash, use o comando git stash apply seguido do nome do stash. Por padrão, o comando apply aplica as alterações do stash mais recente:

```shell
git stash apply
```

Você também pode aplicar as alterações de um stash específico passando o nome do stash como um parâmetro:

```shell
git stash apply stash@{2}
```

## Aplicando e removendo um stash

Para aplicar as alterações de um stash e removê-lo imediatamente, use o comando git stash pop seguido do nome do stash:

```shell
git stash pop stash@{2}
```

## Visualizando alterações em um stash

Para visualizar as alterações contidas em um stash, use o comando git stash show seguido do nome do stash:

```shell
git stash show stash@{2}
```

Se você deseja ver as alterações em um formato mais detalhado, use o parâmetro -p:

```shell
git stash show -p stash@{2}
```

## Criando um novo branch a partir de um stash

Se você deseja criar um novo branch a partir das alterações em um stash, use o comando git stash branch seguido do nome do novo branch e do nome do stash que você deseja aplicar:

```shell
git stash branch novo-branch stash@{2}
```

Isso cria um novo branch chamado "novo-branch" e aplica as alterações do stash "stash@{2}".

## Removendo um stash

Para remover um stash, use o comando git stash drop seguido do nome do stash:

```shell
git stash drop stash@{2}
```

## Limpando todos os stashes

Para limpar todos os stashes em seu repositório, use o comando git stash clear:

```shell
git stash clear
```

Isso remove permanentemente todos os stashes em seu repositório. Certifique-se de que você não precisa mais das alterações antes de usar este comando.
