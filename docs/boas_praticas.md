# Boas Práticas com Git e GitHub


## 1. Uso de Issues no GitHub

As **Issues** são ferramentas de acompanhamento de tarefas no GitHub. Elas servem para registrar:

* Funcionalidades a serem desenvolvidas
* Correções de bugs
* Discussões sobre melhorias
* Dúvidas ou problemas encontrados

### Boas práticas com Issues:

* **Descreva claramente o problema ou a proposta**
* Use **títulos objetivos**
* Adicione **etiquetas (labels)** para organizar por tipo (ex: `bug`, `feature`, `question`)
* Atribua responsáveis (`assignees`) quando for relevante.
* Vincule **pull requests** às Issues usando `Fixes #número` ou `Closes #número` no corpo do PR

## 2. Commits Atômicos

Um **commit atômico** é um commit que faz **apenas uma alteração conceitual**, por menor que seja. Em outras palavras: ele deve conter uma única responsabilidade ou propósito.

### Por que usar commits atômicos?

* Facilita a leitura e revisão do histórico
* Ajuda a identificar a origem de bugs com mais precisão
* Permite reverter mudanças específicas sem afetar outras partes do sistema

### Exemplo ruim:

Um exemplo de prática ruim seria adicionar várias funções de uma vez em um único commit.

```bash
git commit -m "Atualiza layout, adiciona autenticação e corrige bug na página de perfil"
```

### Exemplo ideal (atômico):

Pequenos commits inserindo uma feature de cada vez. Cada alteração deve ser tratada separadamente.

```bash
git commit -m "Atualizando Layout"
...
git commit -m "Adicionando autenticação"
...
git commit -m "Corrige bug na página de perfil"
```

## 3. Commits Semânticos

Commits semânticos seguem um **padrão de nomenclatura** que torna o histórico de commits mais claro e padronizado.

### Estrutura básica:

```
<tipo>: descrição breve do que foi feito
```

### Tipos comuns:

* `feat:` adiciona uma nova funcionalidade
* `fix:` corrige um bug
* `docs:` mudanças na documentação
* `style:` formatação, identação, espaços, sem alteração de código
* `refactor:` refatoração de código (sem alterar funcionalidade)
* `test:` adiciona ou corrige testes
* `chore:` tarefas de configuração ou manutenção

### Exemplo:

```bash
git commit -m "feat: adicionando funcao de deletar usuario"
```

### Referenciando Issues nos commits

Quando se está fazendo commits com o objetivo de cumprir uma tarefa(issue) em específico, deve se incluir o numero da issue nas mensagens de commits, melhorando a rastreabilidade de qual tarefa esses commits estão resolvendo.

```bash
git commit -m "feat: adicionando funcao de deletar usuario #12"
```

Leia mais em [commits semanticos](https://blog.geekhunter.com.br/o-que-e-commit-e-como-usar-commits-semanticos/) e [conventional commits](https://www.conventionalcommits.org/pt-br/v1.0.0/#especifica%c3%a7%c3%a3o)

## 4. `.gitignore`

O arquivo `.gitignore` serve para informar ao Git **quais arquivos ou pastas não devem ser rastreados** nem versionados.

### Exemplos comuns de uso:

* Arquivos temporários (`*.log`, `*.tmp`)
* Configurações locais (`.env`, `*.local`, `*.sqlite3`)
* Diretórios de build (`/dist`, `/build`, `/node_modules`)
* Dados sensíveis ou arquivos grandes

### Por que usar `.gitignore`?

* Evita o versionamento de arquivos desnecessários ou confidenciais
* Mantém o repositório limpo e leve
* Previne erros de configuração entre diferentes máquinas e ambientes

Você pode criar o `.gitignore` manualmente ou usar templates prontos. O site [gitignore.io](https://www.toptal.com/developers/gitignore) gera `.gitignore`s com base na linguagem e ferramentas do projeto. Para a linguagem C neste repositório esta anexado um template de `.gitignore` para utilização, clique [aqui](templates/c.gitignore).