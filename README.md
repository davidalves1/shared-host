**[English](#installing-node)**  
**[Português](#instalando-node)**  

---

# How to install Node, Gulp and Bower in a shared host

## Installing Node

- Go to your project path
- Execute this command: 
	```
	$ wget https://nodejs.org/dist/v4.5.0/node-v4.5.0-linux-x64.tar.gz --no-check-certificate
	```

- After the download finished, execute this command to extract files: 
	```
	$ tar xvf node-v4.5.0-linux-x64.tar.gz
	```	

- After files extracted, execute the command to rename path: 
	```
	$ mv node-v4.5.0-linux-x64 node
	```

- Now the file node-v4.4.2-linux-x64.tar.gz not necessar and can be deleted: 
	```
	$ rm node-v4.5.0-linux-x64.tar.gz
	```

## Installing Bower

- In the same path execute the command: 
	```
	$ node/bin/npm install bower
	```

- Create a symbolic link with the command: 
	```
	$ ln -s node_modules/bower/bin/bower bower
	```

- ***(IMPORTANT)*** Edit the path of the Node in bower to that it works normal:
	- Entre na pasta node/bin e execute o comando ```$ pwd``` para exibir seu caminho completo. Copie este caminho. Volte para a pasta do projeto ao finalizar este passo  
	
	- Abra o arquivo do Bower no editor de texto nano com o comando: 
	```
	$ nano node_modules/bower/bin/bower
	```

	- Edite a primeira linha e substitua pelo caminho completo do NodeJS copiado anteriormente. Salve com *Ctrl + O* e feche com  *Ctrl + X*

- Para instalar os componentes com o bower basta executar o comando: 
	```
	$ ./bower install "componente"
	```

- Exemplo:
	```
	$ ./bower install angular
	```

## Instalando o Gulp

- Ainda na pasta do projeto, executar o comando: 
	```
	$ node/bin/npm install gulp
	```

- Criar link simbólico com o comando: 
	```
	$ ln -s node_modules/gulp/bin/gulp.js gulp
	```
- ***(IMPORTANTE)*** Editar o caminho do NodeJS no gulp para que ele funcione localmente:
	- Entre na pasta node/bin e execute o comando ```$ pwd``` para exibir seu caminho completo. Copie este caminho. Volte para a pasta do projeto ao finalizar este passo  
	
	- Abra o arquivo do Gulp no editor de texto nano com o comando: 
	```
	$ nano node_modules/gulp/bin/gulp
	```

	- Edite a primeira linha e substitua pelo caminho completo do NodeJS copiado anteriormente. Salve com *Ctrl + O* e feche com  *Ctrl + X*. Ex: #!/home/project-name/node/bin/node

- Para executar as tarefas do gulpfile.js basta executar o comando: 
	```
	$ ./gulp
	```

---

# Como instalar o NodeJS, Bower e Gulp no servidor compartilhado

## Instalando Node

- Navegar até a pasta do projeto utilizando o terminal ssh
- Executar o comando: 
	```
	$ wget https://nodejs.org/dist/v4.5.0/node-v4.5.0-linux-x64.tar.gz --no-check-certificate
	```

- Após finalizar o download, executar o comando para extrair o conteúdo: 
	```
	$ tar xvf node-v4.5.0-linux-x64.tar.gz
	```	

- Após finalizar a extração do pacote, executar o comando para renomear a pasta: 
	```
	$ mv node-v4.5.0-linux-x64 node
	```

- Feito isso, o arquivo node-v4.4.2-linux-x64.tar.gz não é mais necessário e pode ser excluído com o comando: 
	```
	$ rm node-v4.5.0-linux-x64.tar.gz
	```

## Instalando o bower

- Ainda na pasta do projeto, executar o comando: 
	```
	$ node/bin/npm install bower
	```

- Criar link simbólico com o comando: 
	```
	$ ln -s node_modules/bower/bin/bower bower
	```

- ***(IMPORTANTE)*** Editar o caminho do NodeJS no bower para que ele funcione localmente:
	- Entre na pasta node/bin e execute o comando ```$ pwd``` para exibir seu caminho completo. Copie este caminho. Volte para a pasta do projeto ao finalizar este passo  
	
	- Abra o arquivo do Bower no editor de texto nano com o comando: 
	```
	$ nano node_modules/bower/bin/bower
	```

	- Edite a primeira linha e substitua pelo caminho completo do NodeJS copiado anteriormente. Salve com *Ctrl + O* e feche com  *Ctrl + X*

- Para instalar os componentes com o bower basta executar o comando: 
	```
	$ ./bower install "componente"
	```

- Exemplo:
	```
	$ ./bower install angular
	```

## Instalando o Gulp

- Ainda na pasta do projeto, executar o comando: 
	```
	$ node/bin/npm install gulp
	```

- Criar link simbólico com o comando: 
	```
	$ ln -s node_modules/gulp/bin/gulp.js gulp
	```
- ***(IMPORTANTE)*** Editar o caminho do NodeJS no gulp para que ele funcione localmente:
	- Entre na pasta node/bin e execute o comando ```$ pwd``` para exibir seu caminho completo. Copie este caminho. Volte para a pasta do projeto ao finalizar este passo  
	
	- Abra o arquivo do Gulp no editor de texto nano com o comando: 
	```
	$ nano node_modules/gulp/bin/gulp
	```

	- Edite a primeira linha e substitua pelo caminho completo do NodeJS copiado anteriormente. Salve com *Ctrl + O* e feche com  *Ctrl + X*. Ex: #!/home/project-name/node/bin/node

- Para executar as tarefas do gulpfile.js basta executar o comando: 
	```
	$ ./gulp
	```
