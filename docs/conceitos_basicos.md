# Conceitos Básicos

## O que é Git

Git é um sistema de controle de versão distribuído. Ele permite acompanhar e registrar as alterações feitas em arquivos ao longo do tempo, possibilitando que múltiplas pessoas trabalhem simultaneamente no mesmo projeto, de forma segura e organizada. 

Com o Git, é possível visualizar o histórico completo de modificações, identificar quem fez cada alteração, reverter mudanças específicas e trabalhar em diferentes versões do mesmo projeto sem conflitos.


## O que é GitHub

GitHub é uma plataforma online que hospeda repositórios Git. Além de armazenar projetos na nuvem, o GitHub oferece recursos para colaboração, revisão de código, controle de acesso, integração com outras ferramentas e automações.

Na prática, ele funciona como uma interface para interagir com os repositórios Git, especialmente em projetos com múltiplos desenvolvedores. É muito utilizado em projetos open source e também em ambientes corporativos.


## O que é um repositório

Um repositório é a estrutura onde um projeto Git é armazenado.
Ele contém todos os arquivos do projeto, bem como o histórico de commits, branches e outras informações de versionamento.

Repositórios podem ser locais, armazenados na máquina do desenvolvedor, ou remotos, hospedados em plataformas como o GitHub, o GitLab ou o Bitbucket. Um projeto pode ter múltiplos repositórios, mas geralmente há um repositório principal e cópias que os desenvolvedores usam para contribuir.


## O que é um commit

Um commit representa um ponto no histórico do projeto. Ele registra um conjunto de alterações realizadas em arquivos, acompanhado de uma mensagem descritiva que explica o que foi feito.

Cada commit possui um identificador único e contém informações como o autor, a data e hora da mudança, e o conteúdo modificado. Commits permitem rastrear a evolução do projeto e ajudam na identificação de erros ou regressões.


## O que é uma branch

Uma branch, ou ramificação, é uma linha de desenvolvimento independente dentro do repositório.
Ela permite que mudanças sejam feitas em paralelo, sem interferir diretamente na versão principal do projeto.

A branch principal costuma ser chamada de `main` ou `master` (use main por favor), enquanto novas branches são criadas para desenvolver funcionalidades, corrigir bugs ou testar novas ideias. Após o término do desenvolvimento em uma branch, as mudanças podem ser integradas de volta à branch principal.



## O que é um pull request

Um pull request é uma solicitação de revisão e integração de mudanças de uma branch para outra, geralmente da branch de desenvolvimento para a branch principal.
Ele é utilizado para facilitar a revisão de código e promover boas práticas de colaboração.

No GitHub, o pull request permite que outras pessoas avaliem as mudanças, façam comentários, testem o código e aprovem ou rejeitem a integração. Ele é um dos principais mecanismos de trabalho colaborativo em projetos com múltiplos contribuidores. Em outras plataforma como Gitlab também é conhecido como Merge Request.



## O que é um merge

Merge é o processo de combinar duas branches em uma única linha de desenvolvimento.
Ele é utilizado, por exemplo, quando se deseja integrar as mudanças feitas em uma branch de funcionalidade à branch principal do projeto.

Durante o merge, o Git tenta unir automaticamente as diferenças entre as branches. Se houver conflitos entre arquivos modificados em ambas as branches, será necessário resolvê-los manualmente antes de concluir a mesclagem.

