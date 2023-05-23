<p align="center">
  <img src="icone/logo_super_2_circle.png" width="120" title="supervisão" alt="Supervisao Contabilidade e Consultoria">  
</p>

---

# Relatório de projetos

## atualizado em 08/05/2023
<a href="https://docs.google.com/spreadsheets/d/e/2PACX-1vQzWIXr6naVTXDIxoWYSsprs8w9ymNUVWulqrH_1VgjXad0DZcvVbe5stCbSTx2pSp4WlayAbWewn8p/pubhtml?gid=2033168620&amp;single=true&amp;widget=true&amp;headers=false">
<p align="center">
  <img src="img/08-05-2023.png" title="supervisão" alt="Supervisao Contabilidade e Consultoria">  
</p>
</a>

---

# Dicas para um bom commit:

## convenção para os commits
 * Especifique o tipo de commit
 * Separe o assunto do corpo do texto com uma linha em branco
 * Sua mensagem de commit não deve ter erros espaços em branco em excesso ou palavras sem espaços entre elas
 * Remova a pontuação desnecessária
 * Não termine uma linha de assunto com um ponto
 * Capitalize as palavras da linha do assunto e a primeira palavra de cada parágrafo
 * Use o modo imperativo na linha de assunto
 * Use o corpo do texto para explicar quais mudanças você fez e o motivo de tê-las feito.
 * Não presuma que o revisor entende qual era o problema original. Não se esqueça de descrever o problema.
 * Não pense que seu código é autoexplicativo
 * Siga a convenção de commit definida por sua equipe

### tipos de commits:
 - **perf: Uma alteração de código que melhora o desempenho**
 - **feat: uma nova feature (recurso) que você está adicionando a uma aplicação específica**
 - **fix: a resolução de um bug**
 - style: recurso e atualizações relacionadas à estilização
 - **refactor: refatoração de uma seção específica da base de código**
 - **test: tudo o que for relacionado a testes**
 - **docs: tudo o que for relacionado à documentação**
 - **chore: manutenção regular do código, são pequenas alterações, ou ajuste de uma linha ou outra.** (Você também pode usar [emojis](https://gitmoji.dev/) para representar os tipos de commit)
 - build: Alterações que afetam o sistema de compilação ou dependências externas (exemplos de escopos: nova lib, alterações grandes)
 - ci: Alterações em nossos arquivos e scripts de configuração de CI (exemplos: CircleCi, SauceLabs)

### modelo de exemplo:
    fix: Resumo com Capitalização e Breve (no Máximo, 50 Caracteres)

    Texto explicativo mais detalhado, se necessário. Deixe-o com, cerca de 72
    caracteres. Em alguns contextos, a primeira linha é tratada como o assunto de um e-mail e o resto do text como o corpo. A linha em branco separando o resumo do corpo é fundamental (a menos que você não escreva uma descrição detalhada); ferramentas como o rebase podem se confundir se você executar ambas em conjunto.

    Escreva sua mensagem de commit no imperativo: "Consertar o bug" em vez de "Bug consertado" ou "Conserta o bug". Esta convenção corresponde às mensagens de commit geradas por comandos como o git merge e o git revert.

    Outros parágrafos vêm após linhas em branco.

    - Colocar a descrição em itens está ok

    - Tipicamente, um hífen ou um asterisco é usado como bullet point (marcação de itens), seguido de um único espaço, envolvido por linhas em branco, mas as convenções variam

    - Use indentação

    Se você usar um rastreados de questões/problemas (issues, em inglês), adicione uma referência a eles ao final, dessa maneira:

    Resolve a issue nº 123


## O comando git commit
Olha essa dica incrível. Você pode passar um segundo parâmetro no comando git commit, nele você pode escrever mais detalhes sobre seu commit.

    $ git commit -m "Title" -m "Description"

É o mesmo comando que você já conhece, mas com uma segunda parte para a descrição. Portanto, “-m ‘title'” permite que você escreva o título abreviado do commit, e “-m ‘description'” permite que você escreva a descrição se precisar fornecer mais detalhes.
    


## fontes:
- [conventionalcommits](https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/#:~:text=A%20mensagem%20de%20commit%20DEVE,ao%20seu%20aplicativo%20ou%20biblioteca.)
- [github: angular](https://github.com/angular/angular/blob/68a6a07/CONTRIBUTING.md#commit)
- [freecodecamp: escrever boas mensagens](https://www.freecodecamp.org/portuguese/news/como-escrever-boas-mensagens-de-commit-um-guia-pratico-do-git/)
- [gitmoji](https://gitmoji.dev/)
- [udacity: styleguide](http://udacity.github.io/git-styleguide/)



---

# comandos úteis

## GIT
 - lembre se trocar o nome do **branch** de acordo com a necessidade



### iniciar o repo
    git init
    git remote add origin https://github.com/Supervisao-Contabilidade-e-Consultoria/sv000_projeto_name.git



### puxar "git pull" da branch "ajuste_01"
    git pull -f origin ajuste_01


#### ou da main, se necessário:
    git pull -f origin main




### trocar branch main
    git branch main ; git checkout main 


#### ou trocar branch para uma de teste, se for fazer algum ajuste
    git branch ajuste_01 ; git checkout ajuste_01

### gerar o venv

#### no windows, no cmd do DOS:
    C:\Users\user\AppData\Local\Programs\Python\Python39\python.exe -m venv .venv

#### no windows, no gitbash:
    /c/Users/user/AppData/Local/Programs/Python/Python39/python.exe -m venv .venv

#### no linux, no shell
    /home/user/.pyenv/shims/python3 -m venv .venv


### enviar "git push" da branch
    git add . ; git add * ; git commit -m "fix: ajuste de log debug com prints" ; git push -f origin ajuste_01


## atualizar python
    python.exe -m pip install PyInstaller
    python.exe -m pip install --upgrade pip

### instalar os requirements.txt na mão
#### usando o gitbash
     cat requirements.txt|sort|uniq | xargs -n 1 .venv/Scripts/pip3.exe install; .venv/Scripts/pip3.exe --upgrade pip ; .venv/Scripts/python.exe -m pip install --upgrade pip

#### usando o shell do linux
    cat requirements.txt|sort|uniq | xargs -n 1 .venv/bin/pip install; .venv/bin/pip --upgrade pip ; .venv/bin/python3 -m pip install --upgrade pip



## executar:

### terminal gitbash
     .venv/Scripts/python.exe  sv000_main.py

### terminal shell do linux:
    .venv/bin/python3 sv000_main.py

## compilar:
 - lembre-se de alterar o nome do executavel **".exe"** e script python **".py"** de acordo com a versão e script que vai compilar

### terminal do pycharm
    python -m PyInstaller --onefile --paths .\venv\Lib\site-packages --icon=icone\logo_super_2_circle.ico -n  sv000_main__v2.0_24042023 .\sv000_main.py ; rm sv000_main__v2.0_24042023.exe ; mv dist/sv000_main__v2.0_24042023.exe .

### terminal do gitbash
    venv/Scripts/python.exe -m PyInstaller  --onefile --paths venv/Lib/site-packages --icon=icone/logo_super_2_circle.ico -n  sv000_main__v2.0_24042023 sv000_main.py ; rm sv000_main__v2.0_24042023.exe ; mv dist/sv000_main__v2.0_24042023.exe .

---

<p align="center">
  <img src="icone/logo_super_1_circle.png" width="120" title="supervisão"  alt="Supervisao Contabilidade e Consultoria">  
</p>

