> [!TIP]
> Atalho para o editor online Visual Studio Code do GitHub = .

# Comandos Git – Básicos e Avançados

| Comando                             | Descrição                                                                | Exemplo prático                                                   |
|-------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------|
| `git config --global`               | Define configurações globais do Git (nome, e-mail etc.)                  | `git config --global user.name "Seu Nome"`<br>`git config --global user.email "email@exemplo.com"` |
| `git config user.name`              | Exibe o nome de usuário configurado no Git local                         | `git config user.name`                                           |
| `git config user.email`             | Exibe o e-mail configurado no Git local                                  | `git config user.email`                                          |
| `git config init.defaultBranch`     | Exibe o nome padrão da branch inicial ao criar novos repositórios        | `git config init.defaultBranch`                                  |
| `git config --global init.defaultBranch <branch>`       | Define `main` como a branch padrão para novos repositórios               | `git config --global init.defaultBranch main`                                                     |
| `git config --global --list`        | Lista todas as configurações globais do Git                              | `git config --global --list`                                     |
| `git-credential-manager --version`  | Exibe a versão do Git Credential Manager instalado                       | `git-credential-manager --version`                               |
| `git config --global credential.helper store`           | Salva credenciais em texto plano para reutilização                       | Requer token do GitHub e ação como `git clone` para solicitar login e token                                                            |
| `git config --global credential.helper cache`           | Armazena credenciais em cache temporário                                 | Requer token do GitHub e ação como `git clone` para solicitar login e token                                                            |
| `git config --global credential.helper`                 | Verifica qual helper de credencial está configurado                      | `git config --global credential.helper`                                                          |
| `git config --global --show-origin credential.helper`   | Mostra a origem e valor da configuração de helper de credencial          | `git config --global --show-origin credential.helper`                        |
| `cat .gitconfig`                    | Exibe o conteúdo do arquivo `.gitconfig` do usuário                      | Executar na pasta do usuário `~`                                 |
| `cat .git-credentials`              | Exibe credenciais salvas (se `store` ou `cache` estiverem ativos)        | Executar na pasta do usuário `~`                                 |
| `git init <pasta>`                  | Inicializa um novo repositório Git local                                 | `git init meu-projeto`                                           |  
| `git clone <url>`                   | Clona um repositório remoto para o local                                 | `git clone https://github.com/user/repo.git`                     |
| `git clone <url> <nome-da-pasta>`   | Clona um repositório remoto em uma pasta específica                      | `git clone https://github.com/user/repo.git projeto-clonado`     |
| `git clone <url> --branch <branch> --single-branch`     | Clona apenas a branch `sandbox` de um repositório remoto                   | `git clone https://github.com/user/repo.git --branch sandbox --single-branch` |
| `git status`                        | Mostra o estado atual dos arquivos no repositório                        | `git status`                                                     |
| `git log`                           | Mostra o histórico de commits                                            | `git log`                                                        |
| `git add <arquivo>`                 | Adiciona um arquivo específico à área de staging                         | `git add README.md`                                              |
| `git add .`                         | Adiciona todos os arquivos modificados à área de staging                 | `git add .`                                                      |
| `git commit -m "mensagem"`          | Salva alterações com uma mensagem descritiva                             | `git commit -m "docs: Adiciona README"`                          |
| `git commit -a -m "mensagem"`       | Adiciona e commita arquivos rastreados (sem `git add`)                   | `git commit -a -m "docs: Atualiza README"`                       |
| `git commit --amend -m "mensagem"`  | Altera a mensagem do último commit                                       | `git commit --amend -m "docs: Corrige descrição"`                |
| `git commit --amend (esc,:,w,q)`    | Edita o último commit via editor Vim                                     | `git commit --amend`                                             |
| `git branch -M <branch>`            | Renomeia a branch atual para "main"                                      | `git branch -M main`                                             |
| `git branch`                        | Lista todas as branches locais                                           | `git branch`                                                     |
| `git branch <nome>`                 | Cria uma nova branch                                                     | `git branch sandbox`                                             |
| `git branch -v`                     | Lista as branches locais com o último commit de cada uma                 | `git branch -v`                                                  |
| `git branch -d <branch>`            | Exclui a branch local chamada `sandbox`                                  | `git branch -d sandbox`                                          |
| `git remote add origin <url>`       | Conecta um repositório remoto a um existente localmente                  | `git remote add origin https://github.com/user/repo.git`         |
| `git remote -v`                     | Lista os repositórios remotos configurados                               | `git remote -v`                                                  |
| `git push -u origin <branch>`       | Envia a branch "main" e define upstream                                  | `git push -u origin main`                                        |
| `git push --force origin <branch>`  | Força commit após usar o --amend localmente e já ter enviado o mesmo commit anteriomente para o repositório remoto | `git push --force origin main`   |
| `git push origin <branch>`          | Envia os commits para o repositório remoto                               | `git push origin main`                                           |
| `git pull origin <branch>`          | Baixa e mescla alterações do repositório remoto                          | `git pull origin main`                                           |
| `git fetch <repositório>`           | Baixa alterações do repositório remoto sem mesclar                       | `git fetch origin`                                               |
| `git fetch <repositório> <branch>`  | Busca atualizações da branch `main` do repositório remoto                | `git fetch origin main`                                          |
| `git merge <branch>`                | Mescla outra branch à branch atual                                       | `git merge sandbox`                                              |
| `git merge <repositório>/<branch>`  | Mescla as alterações da branch remota `main` na branch atual             | `git merge origin/main`                                          |
| `git checkout <branch>`             | Muda para outra branch                                                   | `git checkout main`                                              |
| `git checkout -b <nome>`            | Cria e muda para uma nova branch                                         | `git checkout -b nova-feature`                                   |
| `git diff`                          | Compara alterações entre arquivos ou commits                             | `git diff`                                                       |
| `git diff <branch> <repositório>/<branch>`  | Compara a branch local `main` com a versão remota `origin/main`  | `git diff main origin/main`                                      |
| `git stash`                         | Salva alterações temporariamente                                         | `git stash`                                                      |
| `git stash apply`                   | Restaura alterações salvas com `stash`                                   | `git stash apply`                                                |
| `git stash list`                    | Lista os stashes salvos (alterações temporárias não commitadas)          | `git stash list`                                                 |
| `git stash pop`                     | Aplica o último stash e o remove da lista                                | `git stash pop`                                                  |
| `git reset --hard`                  | Desfaz todas as alterações e volta ao último commit                      | `git reset --hard`                                               |
| `git reset --hard <hash>`           | Restaura o estado do repositório para um commit específico               | `git reset --hard a1b2c3d`                                       |
| `git reset --mixed <hash>`          | Restaura o commit, mas mantém alterações locais                          | `git reset --mixed a1b2c3d`                                      |
| `git reset --soft <hash>`           | Restaura o commit e mantém tudo na staging                               | `git reset --soft a1b2c3d`                                       |
| `git restore <arquivo>`             | Restaura um arquivo para o último commit                                 | `git restore README.md`                                          |
| `git reset <arquivo>`               | Remove um arquivo da área de staging                                     | `git reset README.md`                                            |
| `git reflog`                        | Mostra o histórico de referências (inclusive commits perdidos)           | `git reflog`                                                     |
| `git restore --staged <arquivo>`    | Remove o arquivo da staging sem apagar alterações locais                 | `git restore --staged README.md`                                 |
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
| `git rebase -i HEAD~3`              | Rebase interativo para editar, combinar ou remover os últimos 3 commits  | `git rebase -i HEAD~3`                                           |

# Comandos Bash – Essenciais para Git Bash

| Comando                             | Descrição                                                                | Exemplo prático                                                   |
|-------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------|
| `ls`                             | Lista os arquivos e pastas no diretório atual                 | `ls`                                                      |
| `mkdir <pasta>`                  | Cria uma nova pasta no sistema de arquivos                    | `mkdir meu-projeto`                                              |
| `cd <pasta>`                     | Acessa a pasta especificada                                   | `cd meu-projeto`                                              |
| `touch <arquivo>`                | Cria um arquivo vazio chamado README.me                       | `touch README.md`                                                       |
| `touch <pasta>/.gitkeep`         | Cria um arquivo vazio para manter a pasta no Git              | `touch meu-projeto/.gitkeep`                                     |
| `echo "conteúdo" > <arquivo>` | Cria um novo arquivo com conteúdo inicial usando redirecionamento | `echo "Comandos Git" > README.md`                                         |
| `echo <pasta>/ > .gitignore`     | Adiciona a pasta ao `.gitignore`                              | `echo meu-projeto/ > .gitignore`                                |
| `cd .git`                        | Acessa a pasta oculta de configurações do Git                 | `cd .git`                                                      |
| `rm -rf .git`                    | Remove completamente o repositório Git local                  | `rm -rf .git`                                                      |
| `cat config`                     | Exibe o conteúdo do arquivo de configuração do Git            | `cat config`                                                   |
| `clear`                          | Limpa a tela do terminal                                      | `clear`                                                   |
| `pwd`                            | Mostra o diretório atual                                      | `pwd`                                                     |
| `ls -la`                         | Lista arquivos com detalhes e ocultos                         | `ls -la`                                                      |
| `rm <arquivo>`                   | Remove arquivos                                               | `rm arquivo.txt`                                                      |	
| `rm -r <pasta>`                  | Remove uma pasta e seu conteúdo                               | `rm -r pasta-antiga`                                             |
| `mv <origem> <destino>`          | Move ou renomeia arquivos/pastas                              | `mv antigo.txt novo.txt`                                                 |
| `cp <origem> <destino>`          | Copia arquivos                                                | `cp arquivo.txt copia.txt`                                                |
| `echo "texto"`                   | Imprime texto no terminal                                     | `echo "Olá, mundo"`                                                   |
| `cat <arquivo>`                  | Exibe o conteúdo de um arquivo                                | `cat README.md`                                                       |
| `nano <arquivo>`                 | Edita arquivos diretamente no terminal                        | `nano README.md`                                                       |
| `exit`                           | Encerra o terminal                                            | `exit`                                                    |
| `chmod +x <arquivo>`             | Torna um arquivo executável                                   | `chmod +x script.sh`                                                       |
| `grep "texto" <arquivo>`         | Procura por texto dentro de arquivos                          | `grep "import" README.md`                                                |
| `find . -name "<arquivo>"`       | Procura arquivos no diretório atual                           | `find . -name "*.py"`                                                      |