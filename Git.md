# Conceitos sobre GIT



### Afinal, o que é o Git?

**Git** é um sistema de versionamento de código distribuído, criado por *Linus Torvalds*, que tem como objetivo facilitar o desenvolvimento de projetos como um todo. Para isso, ele captura as diferentes atualizações realizadas em um mesmo projeto, deixando a possibilidade de retornar a qualquer alteração contida no histórico do código que fora realizada. 

O Git não possui uma interface gráfica como a maior parte dos softwares, sua interação é voltada totalmente para linhas de código. O sistema pode ser operado tanto no Sistema Operacional do Windows quanto do Linux, no entanto, os códigos podem ter algumas alterações entre si. A senhor, foram selecionados alguns exemplos para entendermos melhor:

**Dir  (Windows)ou LS(Linux/Windows)** - Este comando lista todos os itens contidos em uma pasta/repositório.

**CD (Windows/Linux)** - Interpretado como "change direction", o comando nos direciona para um local específico do sistema.

**CLS (Windows) ou Clear (Linux)** - Interpretado como "Clear Screen", o comando limpa a tela de código. *Obs: no Windows, usa-se também o atalho Ctrl+L*.

**Mkdir (Windows e Linux)** - O comando realiza a criação de uma pasta/repositório.

**Echo (Windows e Linux)** - um comando que espelha a saída dirigida, como se fosse um “printf”.
Exemplo: *echo hello > hello.txt* é 'printado' o hello e direcionado a um arquivo chamado hello.txt (criação e nomeação de arquivo).

**Del (Windows)** - Comando que deleta os arquivos dentro de um repositório.

**RmDir (Windows)** -  Interpretado como "Remove Direction", o comando remove um repositório/direção.

**Rm -rf (Linux)** - Comando que remove tanto um repositório quanto um arquivo/conteúdo.

Além disso, temos outros comandos extremamente importantes no manuseio do GIT, como:

- *git init* - inicializa o GIT dentro de uma pasta de arquivos criada, iniciando e criando um repositório.
- *git add ** - adiciona todos os arquivos para staged.
- *git commit -m “string de mensagem do commit”* - cria um commit para o arquivo criado.
- *git status* - comando que ajuda a monitorar o status do arquivo.
- *mv arquivo.a.mover ./pastaparamover* - Mover arquivos para uma pasta.



**Ciclo de vida de um GIT:**

Tracked - Arquivos rastreados do GIT, onde temos ciência dele. São divididos em três tipos.

- Unmodified: não modificados

- Modified: modificados.

- Staged: onde ficam os arquivos que se preparam para passarem para outro grupo de atuação.

- Untracked - Irrastreável, não se sabe sobre a existência.



O ciclo pode ser representado da seguinte forma:

Untracked -> Staged (ao adicionar o arquivo)
Unmodified -> Modified (ao editar o arquivo)
Modified -> Staged (Stage o arquivo, ao add ele novamente).
Unmodified -> Untracked (ao deletar o arquivo sem ter sofrido qualquer alteração).
Staged -> Unmodified (cria-se um commit e o ciclo se repete).
Servidor: Remote repository

Quando se cria um commit, é o mesmo que o meu repositório encontrar um local (local repository), podendo também estar alcançando um espaço remoto (remote repository).



**Podemos também adicionar um repositório no GIT para o GitHub da seguinte forma:**

git remote add origin (http do github - repositório criado na plataforma) *para criar a origem*

git remote -v *para enviar para o remoto*

git push origin master *para empurrar para o repositório remoto (github)*

**Podemos, ainda, clonar um repositório do GitHub em nossa máquina local, da seguinte forma:**

*git clone (url copiada do repositório em questão)*



**Conflitos com versionamento GIT x GitHub**

Os problemas de versionamento de código acontecem quando as alterações de um mesmo código entre pessoas diferentes têm características próprias, todavia ocorrem na mesma linha. Dessa forma, em exemplos de OpenSource, temos que puxar o código que está commitado no repositório do GitHub (alterado por um outro contribuinte) para que a nossa versão na máquina local seja atualizada conforme o que já está salvo em remote repository. 

Para, então, as mudanças serem atualizadas e empurradas após o novo commit. Assim, puxamos o código do repositório da seguinte forma:

*git pull origin master*







