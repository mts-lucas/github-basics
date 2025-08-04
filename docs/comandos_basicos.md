# Tutorial: Comandos Básicos do Git

## `git init`

Este comando cria um **novo repositório Git vazio** em uma pasta.

Ele inicializa a estrutura interna do Git e permite seu diretório se torne um repositório git.


## `git clone <url-do-repositório>`

Faz o **download de um repositório remoto** (por exemplo, do GitHub) para sua máquina local.

Além de baixar os arquivos, também copia o histórico de commits e as branches.


## `git status`

Exibe o **estado atual do repositório local**, incluindo:

* Quais arquivos foram modificados
* Quais arquivos ainda não foram adicionados ao controle de versão
* Se há commits pendentes


## `git branch`

Exibe uma lista de todas as branches existentes e indica qual é a branch atual.

Você também pode usá-lo para **criar ou deletar branches**, mas no uso mais simples ele apenas lista.

## `git checkout`

Este comando serve para **trocar de branch** ou **voltar a versões anteriores**.

### `git checkout nome-da-branch`

Troca para uma branch existente.

### `git checkout -b nome-da-nova-branch`

Cria uma **nova branch** e muda para ela.

## `git add`

Adiciona arquivos ao **"staging area"**, ou seja, prepara os arquivos para serem incluídos no próximo commit.

Você pode adicionar arquivos individualmente ou todos de uma vez:

```bash
git add arquivo.txt        # adiciona um arquivo
git add .                  # adiciona todos os arquivos modificados
```

## `git commit`

Marca uma nova **versão** do seu projeto, salvando as alterações adicionadas com `git add`.

É obrigatório escrever uma **mensagem descritiva** explicando o que foi feito.

```bash
git commit -m "Adiciona novo componente de login"
```

## `git pull`

Atualiza seu repositório local com as mudanças mais recentes do repositório remoto.

**NOTA:**
Use sempre antes de começar a trabalhar em algo novo, ou para manter seu projeto sincronizado com o que está no GitHub.


## `git push`

Envia seus commits locais para o repositório remoto.

É o comando que torna suas mudanças visíveis para outras pessoas que trabalham no mesmo repositório.

```bash
git push origin nome-da-branch
```

## `git merge`

Combina o histórico de uma branch com outra.
O uso mais comum é mesclar uma branch de funcionalidade (feature) com a branch principal.

```bash
git checkout main
git merge nome-da-branch
```

O Git tenta integrar as mudanças automaticamente. Se houver conflitos (modificações diferentes nas mesmas linhas de um arquivo), será necessário resolver manualmente.

