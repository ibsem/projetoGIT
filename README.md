# projetoGIT

## Tutorial GIT e GITHUB

1. Para INICIALIZAR uma pasta no GIT, entrar na pasta do projeto e digitar...
```
git init
ls -la "visualiza o diretório oculto .git"
```
2. Para ELIMINAR A PASTA do controle de versão, excluir a pasta .git
rm -rf .git

3. Após CRIAR UM ARQUIVO do projeto dentro da pasta VERIFICAR O STATUS, digitando o comando...
```
git status
```
Então, aparece o arquivo criado sob o estágio UNTRACKED FILE, ainda fora controle de versão do GIT.

4. Para adicionar o arquivo ao estágio STAGED intermediário de controle de versão digite...
```
git add <nome do arquivo> ou . "...para todos os arquivos da pasta"
```
O estágio que o arquivo se encontra agora é o CHANGE TO BE COMMITED ou staging
5. Para COMITAR o arquivo, digite o comando...
```
git commit -m "Meu primeiro Commit"
```
6. Para ver AS TRANSAÇÕES DE COMMIT digitar o comando...
```
git log
```
7. Se o arquivo for alterado o git marca o arquivo como alterado mas não comitado

8. Para dar um COMMIT EM VÁRIOS ARQUIVOS, digita git commit e o será aberto um editor padrão para descrever o commit
```
git commit
```
9. Para dar um COMMIT SEM PASSAR PELO ESTÁGIO ADD, basta dar o comando...
```
git commit -a -m "me segundo commit sem add"  
```
10. Opções do GIT LOG...
```
git log -p ( mostra todas as mudanças dos commits)
git log -p -2
git log --stats
git log --pretty=oneline - tudo em uma linha
git log --pretty=format:"%h - %an - %ar : %s"
```
11. Para RETORNAR AO ESTAGIO UNSTAGED...
```
git rm --cached <file>
```
12. Para VOLTAR UM COMMIT digite o comando...
```
git checkout <hash da versao>
```
13. Para DESFAZER A OPERAÇÃO E VOLTAR O COMMIT digitar o comando...
```
git switch -
```
14. Para SABER QUAL BRANCH ESTÁ operando digitar o comando...
```
git branch
```
15. Para TRABALHAR COM BRANCHS DIFERENTES (boa prática, utilizar para criar novas funcionalidades)

16. Para CRIAR UM NOVO BRANCH a partir de um branch atual
```
git checkout -b <nome do novo branch>
```
17. Para VOLTAR PARA O MASTER digite o comando...
```
git checkout master
```
18. Para MESCLAR DOIS CÓDIGOS de branchs diferentes...
```
git merge <nome do branch que tem as mudancas> 
```
19. Para usar o github com uma CHAVE PUBLICA...

20. Criar uma CHAVE PUBLICA para o GITHUB e facilitar a atualizaçao dos projetos...
```
ssh-keygen
enter, enter...
cd ~/.ssh/
vim id_rsa.pub
Copiar os dados e colar no github (administraçao da conta>>criar chave publica)
```
21. Para CRIAR UM REPOSITÓRIO REMOTO NO GITHUB e iniciar localmente a criaçao do branch e dos arquivos não utilizar a opção do read-me...
```
git remote add origin https://github.com/ibsem/interpolacaoLinear.git
git push -u origin master
```
22. Para BAIXAR O PROJETO digite...
... se o projeto ja estiver criado localmente...
```
git pull master <url>
```
... na primeira vez...
```
ou... git clone <url> 
```  
23. Para atualizar o projeto no github...
```
git push --set-upstream origin master
```
24. Para CRIAR UM NOVO repositório 
```
touch README.md
git init
git add README.md
git commit -m "Primeiro Commit"
git remote add orgin <nome do repositorio>
git push -u origin master
```

26. Para visualizar os branchs remotos no GitHub...
```
git branch -a
```
27. Para clonar outro branch...
```
git checkout -b <nome Branch> origin/<nome do branch no github>
```

28. Para dar fazer o merge dos projetos com stories diferentes
```
git pull origin master --allow-unrelated-histories
```
