# Tutorial de Configurações

## Visão geral

O comando `git config` é utilizado para configurar preferências e comportamentos do Git no seu ambiente de trabalho. Essas configurações vão desde a identidade do usuário até a forma como o Git lida com merge, cores no terminal, editores padrão, entre outros.

As configurações podem ser aplicadas em três níveis de escopo:

* **Local (`--local`)**: válidas apenas para um repositório específico.
* **Global (`--global`)**: aplicadas ao usuário em todos os repositórios no sistema.
* **System (`--system`)**: válidas para todos os usuários da máquina (menos comum).



## Diferença entre `--global` e `--local`

* `--global`: aplica a configuração ao seu usuário no sistema. As definições são salvas em um arquivo como `~/.gitconfig` e valem para todos os repositórios.
* `--local`: aplica a configuração apenas ao repositório atual. As definições ficam registradas em `.git/config`, dentro da pasta do projeto.

O Git sempre usa a configuração mais específica. Ou seja, se houver uma configuração local, ela prevalece sobre a global.



## Configurando sua identidade

Uma das primeiras configurações obrigatórias no Git é definir quem você é. Isso é feito com os comandos:

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
```

Esses dois valores são gravados em cada commit que você fizer, servindo como identificação do autor. Quando alguém visualizar o histórico do projeto ou analisar um pull request, será possível saber **quem fez cada alteração** e **em qual momento**.

Se você estiver trabalhando em diferentes contextos (por exemplo, projetos pessoais e projetos da empresa), pode definir identidades separadas com o `--local`:

```bash
git config --local user.name "Fulano Empresa"
git config --local user.email "fulano@empresa.com"
```

Essas informações **não têm relação com o login ou senha do GitHub**. Elas apenas indicam a autoria de commits, podendo inclusive usar e-mails fictícios ou privados (como os do GitHub `noreply`).


## Visualizar configurações

Você pode listar todas as configurações ativas com:

```bash
git config --list
```

Este comando mostra o conjunto de configurações atuais, considerando os três níveis (local, global e system).


