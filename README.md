atalho para o editor online Visual Studio Code do GitHub = .

Comandos Git – Básicos e Avançados

| Comando                             | Descrição                                                                | Exemplo prático                                                  |
|-------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------|
| `git init`                          | Inicializa um repositório Git na pasta atual                             | `git init`                                                       |
| `git clone <url> <nome-da-pasta>`   | Clona um repositório remoto em uma pasta específica                      | `git clone https://github.com/user/repo.git projeto-clonado`     |
| `git remote -v`                     | Lista os repositórios remotos configurados                               | `git remote -v`                                                  |
| `git status`                        | Mostra o estado atual dos arquivos no repositório                        | `git status`                                                     |
| `git log`                           | Mostra o histórico de commits                                            | `git log`                                                        |
| `git add README.me`                 | Adiciona o arquivo README.me à área de staging                           | `git add README.me`                                              |
| `git add .`                         | Adiciona todos os arquivos modificados à área de staging                 | `git add .`                                                      |
| `git commit -m "descrição"`         | Salva alterações com uma mensagem descritiva                             | `git commit -m "Adiciona README"`                                |
| `git commit --amend -m "descrição"` | Altera a mensagem do último commit                                       | `git commit --amend -m "Corrige descrição"`                      |
| `git commit --amend (esc,:,w,q)`    | Edita o commit anterior via editor Vim                                   | `git commit --amend` → `(esc) :wq`                               |
| `git branch -M main`                | Renomeia a branch atual para "main"                                      | `git branch -M main`                                             |
| `git remote add origin <url>`       | Conecta um repositório remoto a um existente localmente                  | `git remote add origin https://github.com/user/repo.git`         |
| `git push -u origin main`           | Envia a branch "main" e define upstream                                  | `git push -u origin main`                                        |
git push
| `git push --force origin main       | forçar commit após usar o --amend localmente após já ter enviado o mesmo commit anteriomente para o remoto
| `git reset --hard <hash>`           | Restaura o estado do repositório para um commit específico               | `git reset --hard a1b2c3d`                                       |
| `git reset --mixed <hash>`          | Restaura o commit, mas mantém alterações locais                          | `git reset --mixed a1b2c3d`                                      |
| `git reset --soft <hash>`           | Restaura o commit e mantém tudo na staging                               | `git reset --soft a1b2c3d`                                       |
| `git restore README.me`             | Restaura o arquivo para o último commit                                  | `git restore README.me`                                          |
| `git reflog`                        | Mostra o histórico de referências (inclusive commits perdidos)           | `git reflog`                                                     |
| `git reset README.me`               | Remove o arquivo da área de staging                                      | `git reset README.me`                                            |
| `git restore --staged README.me`    | Remove o arquivo da staging sem apagar alterações locais                 | `git restore --staged README.me`                                 |
| `git init <pasta>`                  | Inicializa um novo repositório Git local                                 | `git init meu-projeto`                                           |
| `git clone <url>`                   | Clona um repositório remoto para o local                                 | `git clone https://github.com/user/repo.git`                     |
| `git status`                        | Mostra o estado atual dos arquivos no repositório                        | `git status`                                                     |
| `git add <arquivo>`                 | Adiciona um arquivo específico à área de staging                         | `git add index.html`                                             |
| `git add .`                         | Adiciona todos os arquivos modificados à área de staging                 | `git add .`                                                      |
| `git commit -m "mensagem"`          | Salva alterações com uma mensagem descritiva                             | `git commit -m "Adiciona página inicial"`                        |
| `git commit -a -m "mensagem"`       | Adiciona e commita arquivos rastreados (sem `git add`)                   | `git commit -a -m "Atualiza estilos"`                            |
| `git push origin <branch>`          | Envia os commits para o repositório remoto                               | `git push origin main`                                           |
| `git pull origin <branch>`          | Baixa e mescla alterações do repositório remoto                          | `git pull origin main`                                           |
| `git fetch origin`                  | Baixa alterações do repositório remoto sem mesclar                       | `git fetch origin`                                               |
| `git merge <branch>`                | Mescla outra branch à branch atual                                       | `git merge nova-feature`                                         |
| `git branch`                        | Lista todas as branches locais                                           | `git branch`                                                     |
| `git branch <nome>`                 | Cria uma nova branch                                                     | `git branch nova-feature`                                        |
| `git checkout <branch>`             | Muda para outra branch                                                   | `git checkout nova-feature`                                      |
| `git checkout -b <nome>`            | Cria e muda para uma nova branch                                         | `git checkout -b nova-feature`                                   |
| `git log`                           | Mostra o histórico de commits                                            | `git log`                                                        |
| `git diff`                          | Compara alterações entre arquivos ou commits                             | `git diff`                                                       |
| `git reset <arquivo>`               | Remove um arquivo da área de staging                                     | `git reset index.html`                                           |
| `git reset --hard`                  | Desfaz todas as alterações e volta ao último commit                      | `git reset --hard`                                               |
| `git stash`                         | Salva alterações temporariamente                                         | `git stash`                                                      |
| `git stash apply`                   | Restaura alterações salvas com `stash`                                   | `git stash apply`                                                |
| `git remote -v`                     | Lista os repositórios remotos configurados                               | `git remote -v`                                                  |
| `git config --global`               | Define configurações globais do Git (nome, e-mail etc.)                  | `git config --global user.name "Seu Nome"`<br>`git config --global user.email "email@exemplo.com"` |
| `git config user.name`              | | |
| `git config user.email`	      | | |
| `git config init.defaultBranch`     | | |
| `git config --global init.defaultBranch main`     | | |
| `git config --global --list`        | | |
| `git-credential-manager --version`  | | |
| `git config --global credencial.helper store`  | | | precisa do token que é gerado no github e posteriormente fazer algo pelo git, por exemplo clonar repositório para pedir para informar nome de usuário e token
| `git config --global credencial.helper cache`  | | | precisa do token que é gerado no github e posteriormente fazer algo pelo git, por exemplo clonar repositório para pedir para informar nome de usuário e token	
| `git config --global credential.helper` | | | verificar qual tipo de credencial
| `git config --global --show-origin credential.helper` | | | verificar origem e qual tipo de credencial
| `cat .gitconfig` | | | porém precisa estar na pasta do usuário "~"
| `cat .git-credentials` | | | ver credencial, porém quando usa store ou cache, porém precisa estar na pasta do usuário "~"
| `git tag <nome>`                    | Cria uma tag (marca) em um commit específico                             | `git tag v1.0`                                                   |
| `git rebase <branch>`               | Reescreve o histórico aplicando commits sobre outra branch               | `git rebase main`                                                |
| `git cherry-pick <hash>`            | Aplica um commit específico de outra branch                              | `git cherry-pick a1b2c3d`                                        |
| `git revert <hash>`                 | Cria um novo commit que desfaz um commit anterior                        | `git revert a1b2c3d`                                             |
| `git rm <arquivo>`                  | Remove um arquivo do repositório e do sistema                            | `git rm arquivo.txt`                                             |
| `git mv <origem> <destino>`         | Move ou renomeia arquivos dentro do repositório                          | `git mv antigo.txt novo.txt`                                     |
| `git show <hash>`                   | Exibe detalhes de um commit específico                                   | `git show a1b2c3d`                                               |
| `git bisect`                        | Ajuda a encontrar o commit que introduziu um bug                         | `git bisect start`                                               |
| `git blame <arquivo>`               | Mostra quem modificou cada linha de um arquivo                           | `git blame app.js`                                               |
| `git archive`                       | Cria um arquivo compactado do projeto                                    | `git archive -o projeto.zip HEAD`                                |
| `git gc`                            | Faz limpeza e otimização do repositório                                  | `git gc`                                                         |
| `git fsck`                          | Verifica a integridade do repositório                                    | `git fsck`                                                       |
| `git shortlog`                      | Mostra um resumo dos commits por autor                                   | `git shortlog -s -n`                                             |
| `git describe`                      | Gera uma descrição legível de um commit com base em tags                 | `git describe --tags`                                            |
| `git config --list`                 | Lista todas as configurações do Git                                      | `git config --list`                                              |
| `git clean -f`                      | Remove arquivos não rastreados                                           | `git clean -f`                                                   |
| `git submodule`                     | Gerencia repositórios dentro de repositórios                             | `git submodule add <url>`                                        |
| `git worktree`                      | Permite trabalhar com múltiplas cópias do mesmo repositório              | `git worktree add ../outra-pasta branch-nova`                    |
| `git cherry`                        | Lista commits que estão em uma branch e não em outra                     | `git cherry main nova-feature`                                   |
| `git apply <patch>`                 | Aplica um patch manualmente                                              | `git apply correcoes.patch`                                      |
| `git am`                            | Aplica commits formatados como e-mail                                    | `git am <arquivo.eml>`                                           |
| `git revert -n <hash>`              | Reverte um commit sem criar um novo commit automático                    | `git revert -n a1b2c3d`                                          |
| `git commit --amend`                | Altera o último commit (mensagem ou conteúdo)                            | `git commit --amend -m "Nova mensagem"`                          |
| `git rebase -i HEAD~3`              | Rebase interativo para editar, combinar ou remover   	                 | 				                                    |
echo "#commit-1-branch-main" > commit-1-branch-main.txt
git checkout -b teste
git checkout main
git branch -v
git merge teste
git branch -d teste
git branch
git fetch origin main
git diff main origin/main
git merge origin/main
git clone url --branch teste --single-branch
git stash
git stash list
git stash apply
git stash pop

Comandos Bash – Essenciais para Git Bash

| Comando                          | Descrição                                                     | Exemplo prático                                                  |
|----------------------------------|---------------------------------------------------------------|------------------------------------------------------------------|
| `ls`                             | Lista os arquivos e pastas no diretório atual                 | `ls`                                                             |
| `mkdir <pasta>`                  | Cria uma nova pasta no sistema de arquivos                    | `mkdir meu-projeto`                                              |
| `cd <pasta>`                     | Acessa a pasta especificada                                   | `cd meu-projeto`                                                 |
| `touch <arquivo>`                | Cria um arquivo vazio chamado README.me                       | `touch README.me`                                                |
| `touch <pasta>/.gitkeep`         | Cria um arquivo vazio para manter a pasta no Git              | `touch meu-projeto/.gitkeep`                                     |
| `cd .git`                        | Acessa a pasta oculta de configurações do Git                 | `cd .git`                                                        |
| `rm -rf .git`                    | Remove completamente o repositório Git local                  | `rm -rf .git`                                                    |
| `echo <pasta>/ > .gitignore`     | Adiciona a pasta ao `.gitignore`                              | `echo meu-projeto/ > .gitignore`                                 |
| `cat config`                     | Exibe o conteúdo do arquivo de configuração do Git            | `cat config`                                                     |
| `clear`                          | Limpa a tela do terminal                                      | `clear`                                                          |

| `pwd`                            | Mostra o diretório atual                                      | `pwd`                                                            |*
| `ls -la`                         | Lista arquivos com detalhes e ocultos                         | `ls -la`                                                         |*
| `rm <arquivo>`                   | Remove arquivos                                               | `rm arquivo.txt`                                                 |*	
| `rm -r <pasta>`                  | Remove uma pasta e seu conteúdo                               | `rm -r pasta-antiga`                                             |*
| `mv <origem> <destino>`          | Move ou renomeia arquivos/pastas                              | `mv antigo.txt novo.txt`                                         |*
| `cp <origem> <destino>`          | Copia arquivos                                                | `cp arquivo.txt copia.txt`                                       |*
| `echo "texto"`                   | Imprime texto no terminal                                     | `echo "Olá, mundo"`                                              |*
| `cat <arquivo>`                  | Exibe o conteúdo de um arquivo                                | `cat README.md`                                                  |*
| `nano <arquivo>`                 | Edita arquivos diretamente no terminal                        | `nano README.md`                                                 |*
| `exit`                           | Encerra o terminal                                            | `exit`                                                           |*
| `chmod +x <arquivo>`             | Torna um arquivo executável                                   | `chmod +x script.sh`                                             |*
| `grep "texto" <arquivo>`         | Procura por texto dentro de arquivos                          | `grep "import" README.md`                                        |*
| `find . -name "<arquivo>"`       | Procura arquivos no diretório atual                           | `find . -name "*.py"`                                            |*

