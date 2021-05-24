# Github

- Configurações
  - Configurar nome
    - git config --global user.name "Paulo Ricardo"
  - Configurar email
    - git config --global user.email "paulo.silva@ma9.com.br"
  - Configurar editor principal
    - git config --global core.editor vim


- Criar Repositório
  1 Criar uma pasta para o projeto
    - mkdir <NomeDoProjeto>

// Entrar na pasta
cd <Nome ou DiretorioDoProjeto>
// Voltar para o diretório anterior
cd .. 

// Para o repositório ser considerado parte do ecossistema do git
// Responsável por inicializar o repositório e ver todas a mudanças do projeto
git init



// Editar o texto com vim
vim Readme.md
// Aperta a tecla i para entrar no modo insert
// Após escrever o que quer aperta esc para sair do modo insert
// Aperta a tecla : que indica que vai iniciar algum comando
// Aperta w para salvar
// Aperta a tecla q para sair do modo edição


// Verificar como está o repositório
git status

// Adicionar arquivos
git add <NomeDoArquivo>

// Commitar arquivos
git commit -m "<comentário>"
git commit -am "<comentário>"



// Ver logs
git log
git log --author="<Nome do autor>" 
git show
// Mostra os logs de forma curta (os autores, quantos commits e quais foram)
git shortlog
// Mostra só a quantidade de commits e os autores
git shortlog -sn
// Mostra em forma gráfica
git log --graph
// Ver as alterações feitas nos arquivos
git diff
// Ver o nome dos arquivos que sofreram alterações
git diff --name-only


// Desfazendo alterações
// Arquivos antes de stage
git checkout <Nome do Arquivo>
// Arquivos no stage
git reset HEAD <Nome do Arquivo>


// Desfazendo commit
git reset --soft	"arquivo vai ficar em staged pronto para ser commitado"
git reset --mixed	"arquivo modificado mas não em staged"
git reset --hard	"arquivo não modificado"




// SSH é um protocolo para identificar o usuário ao servidor
//https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
//Após gerar as chaves públicas e privadas, temos que abrir a chave publica no o git
cat <nome da chave>
//Após abrir e copiar a chave, vamos no github em configurações e passamos a chave publica


// Realizar o push
// Informar o git remote
git remote add origin https://github.com/PauloRicardoMA9/CursoGit.git
// Visualiza o repositorio
git remote -v
//Realiza push
git push -u origin master	//origin = pra onde vai, master = de onde vem


