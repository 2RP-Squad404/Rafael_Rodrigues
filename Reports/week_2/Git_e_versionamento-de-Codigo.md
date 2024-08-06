# Relatório de Estudos

**Nome do Estagiário:** Rafael Rodrigues  
**Data:** 05/08/24

**Módulos/Etapas Feitas:**  
1. **5/Entendendo o Rebase**
- pega tudo que tá no branch e move para o inicio da fila
- as branchs apontam para o mesmo commit

### Prós 
- Evita commits extras
- Histórico linear

### Contra
- Perde ordem cronológica
- usar com cuidado




2. **5/Merge e rebase na prática**
  comandos utilizados na aula: 

  - Criar pasta
  ```
  mkdir rebase-cargo
  ```
  - Navegar até a pasta

  ```
  cd rebase-cargo
  ```

  - inicializa o repositório
  ```
  git init 
  ```
  - Cria um arquivo para armazenar no repositório

  ```
  notepad foo

  ```
  - usa o git status para verificar o estado do arquivo

  ```
  git status
  ```

  - adiciona para o area de stage do git usando:

  ```
  git add foo.txt

  ```
  - faz o commit:
  
  ```
  git commit -m "add foo"
  ```

  - Cria uma nova branch
  ```
  git checkout -b test

  ```
  
  - cria mais um arquivo chamado bar

  ```
  notepad bar
  ```
  - adiciona o arquivo 
  ```
  git add bar.txt
  ```
  - Faz o commit:

  ```
  git commit -m "add bar"
  ```
  - Usa o git log para ver os commits

  ```
  git log
  ```
  Quando eu vou para a branch main eu dou o comando novamente e só vejo que existe o foo e não o bar.

  Isso ocorre pois o arquivo bar só foi criado na branch teste.

  cria mais um arquivo chamado fizz na branch main

  adiciona e commita
  
  - faz o merge com o teste

  ```
  git merge teste
  ```
  abre o editor, para sair e salvar digitar:
  :wq

  ele adiciona de forma recursiva o arquivo

  Após o merge ele fica com todos os commits na branch main
  mas ele gerou um outro commit de merge

  ### Rebase

  cria um novo arquivo chamado buzz

  adiciona e faz o commit

  cria uma nova branch com o comando: 

  ```
  git checkout -b rebase-branch
  ```

  Cria um novo arquivo:

  ```
  notepad bla
  ```
  adiciona e faz o commit

  usa o log novamente para ver os commits usando o:

  ```
  git log --graph
  ```

  Percebe-se que ele tá linear por enquanto.

  muda se para a branch main usando:

  ```
  git checkout main
  ```

  usando o git log percebe-se que não tem o arquivo bla

  ai cria mais um arquivo com o nome seila

  adiciona e faz o commit

  depois faz o rebase com o comando 
  ```
  git rebase rebase-branch
  ```
  - merge é usado em caso de pull request quando precisamos saber o que foi unido
  - pois o rebase não mostra de onde veio as alterações pois ele não gera o commit de merge

  **Use Rebase em Branches Locais: É mais seguro usar rebase em branches locais e privadas. Para branches compartilhadas, prefira merge para evitar problemas com colaboradores.**


3. **5/Criando o .gitignore**
  - Usado para evitar que arquivos subam para o repositório remoto.

4. **6/Git stash é lindo**
  - Ele guarda modificações que ainda não foram commitadas
  - Usar quando eu tenho modificações e preciso mudar de branch e eu ainda não terminei elas

  ### Comandos
  ```
  git stash
  git stash list
  git stash clear

  ```
5. **6/Alias para que te quero**
- usado para criar atalhos de comandos de forma mais simples

```
git config --global alias.s status

```
- ai o git status vai poder ser acessado com o comando: 
```
git s
```
6. **6/Versionando com Tags**
- Defini as versões do que estamos fazendo 
```
git tag -a 1.0.0 -m "Readme finalizado"
```
- Faz o push para o repositório remoto 
```
git push origin master --tags
```
- Vai no github para ver as mudanças

7. **6/Salvando sua sexta com Git Revert**
- Gera um novo commit sem as alterações do commit que eu passei 
```
git revert hash-do-commit
```
8. **Learn Git Branch**

  Referencia: [Learn git branch](https://learngitbranching.js.org/?locale=pt_BR)
  
  Comando: ```git checkout nome_commit^``` ele vai para o pai do commit
  ```git checkout nome_commit~4``` ele pega o valor e leva o HEAD.

  ```git branch -f main HEAD~3``` move a força o Ramo main 3 ancestrais acima do HEAD
  

4. ...

## Resumo dos módulos 

05/08/24

No dia de hoje até o momento eu aprendi sobre alguns novos comandos do git, como fazer mesclagem de branchs com os comandos rebase e git merge.
aprendi também que tem um comando chamado git stash que é usado para armazenar uma mudança que eu ainda não fiz o commit. 


## Links de Laboratórios (se houver)

- [Google Colab 1/Notion 1](URL_do_Lab_1)
- [Google Colab 2/Notion 2](URL_do_Lab_2)
- ...

**Recursos Utilizados:**  
- Git
- Vs Code
- Terminal
- ...

**Principais comandos: (se aplicável)**  
- git init
- git status
- git rebase nome-branch
- git commit -m "mensagem do commit"
- git add .
- git push
- git stash 
- git stash list
- git stash clear
- git log
- git log --graph
- git push origin master --tags
- git checkout nome-branch
- git merge nome-branch
- git tag -a 1.0.0 -m "Readme finalizado"
- git config --global alias.s status
- git s
- ...

**Desafios Encontrados:**  
Os desafios que eu tive foi com a internet, com distrações e o barulho na sala dificultando o entendimento e a concentração.

**Feedback e Ajustes:**  
Gostei do conteudo sobre git na Udemy, achei bem completo apesar de ser um curso básico.

**Próximos Passos:**  
Irei começar o estudo de system design.
