# DockerHandbook
Aplicação dos estudos do básico sobre Docker.

## Docker 

### Comandos

docker - Descrição de todos os comandos do docker com descricao

docker info - Descrição do docker com informações de configs.

docker ps - Descrição de container, portas, imagens, sendo utilizadas.

docker ps -a - Exibe todos os containers, mesmo os desabilitados.

docker images - Imagens baixadas que estão na máquina.

docker pull ubuntu:18.04 - Baixa uma imagem do SO selecionado, nesse caso o ubuntu versão 18.04

docker run - Para criar um container

	docker run -it --name teste(nome container) debian (nome imagem) 

	docker run -i -t ubuntu:14.10(imagem e versão) /bin/bash(comando associado ao container)
	
	docker run -it -p 8080:8080(associando a porta do host com a porta do container executado) --name hyperledger-composer-playground hyperledger/composer-playground
	
docker attach CONTAINER ID - Acessa o container com o container id obtido na lista do docker ps.

docker diff CONTAINER ID - Visualiza todas a modificações feitas desde o momento de criação do container, mostra os arquivos criados, deletas e modificados.

docker commit CONTAINER ID nome-descricao:versao - Essa a forma que se tem de salvar um container com a imagem formada e reutilzar, versionando os containers. Outra forma é dizer que será criada uma imagem a partir do container.

	Ex.: docker commit -a Irlan(Autor) -m "Primeira imagem gerada"(Comentário) 8ab9ea12e4a1 debian/minha_imagem:1.0

docker stop CONTAINER ID - Parar o container, acho que quando não está salvo ele mata o container com tudo.

docker inspect CONTAINER ID - Obter todas as informações importantes sobre o container.

docker start CONTAINER ID - Executa o container que está pausado pelo id.

docker rm CONTAINER ID - Remove/apaga o container.

docker rmi IMAGE ID - Remove/apaga a imagem.

## Comandos do Teclado

Ctrl + D - Sai do container e o mata.

Ctrl + P + Q - Saí do container e deixa executando.

