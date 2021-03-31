<div align="center">
    <img src="https://avatars0.githubusercontent.com/u/5429470?s=200&v=4" width="200" >

# [DOCKER](https://github.com/docker)

</div>

[Tutorial de intslação no Ubuntu (video)](https://www.youtube.com/watch?v=zJ6WbK9zFpI&feature=emb_rel_pause)

## [Instalação no Ubuntu](https://docs.docker.com/engine/install/ubuntu/)

Pirmeiro remova qualquer outra versão do docker que já esteja instalada

    sudo apt-get remove docker docker-engine docker.io containerd runc

Faça o download do script de instalação

    curl -fsSL https://get.docker.com -o get-docker.sh

Agora execute o script

    sudo sh get-docker.sh

Certifique-se de que tenha instalado executando o comando

    sudo docker version

## [Outro método de Instalação no Ubuntu](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04-pt)

Primeiro, atualize sua lista existente de pacotes:

    sudo apt update

Em seguida, instale alguns pacotes pré-requisito que deixam o apt usar pacotes pelo HTTPS:

    sudo apt install apt-transport-https ca-certificates curl software-properties-common

Então, adicione a chave GPG para o repositório oficial do Docker no seu sistema:

    curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

Adicione o repositório do Docker às fontes do APT:

    sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"

Em seguida, atualize o banco de dados do pacote com os pacotes do Docker do recém adicionado repositório:

    sudo apt update

Certifique-se de que você está prestes a instalar do repositório do Docker ao invés do repositório padrão do Ubuntu:

    apt-cache policy docker-ce

Você verá um resultado assim, embora o número da versão para o Docker possa ser diferente:

                        Output of apt-cache policy docker-ce

    docker-ce:
    Installed: (none)
    Candidate: 5:19.03.9~3-0~ubuntu-focal
    Version table:
      5:19.03.9~3-0~ubuntu-focal 500
        500 https://download.docker.com/linux/ubuntu focal/stable amd64 Package

Finalmente, instale o Docker:

    sudo apt install docker-ce

O Docker deve agora ser instalado, o daemon iniciado e o processo habilitado a iniciar no boot. Verifique se ele está funcionando:

    sudo systemctl status docker

O resultado deve ser similar ao mostrado a seguir, mostrando que o serviço está ativo e funcionando:

    Output
    ● docker.service - Docker Application Container Engine
        Loaded: loaded (/lib/systemd/system/docker.service; enabled; vendor preset: enabled)
        Active: active (running) since Tue 2020-05-19 17:00:41 UTC; 17s ago
    TriggeredBy: ● docker.socket
        Docs: https://docs.docker.com
    Main PID: 24321 (dockerd)
        Tasks: 8
        Memory: 46.4M
        CGroup: /system.slice/docker.service
                └─24321 /usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock

---

## Executando o Comando Docker Sem Sudo

Se você quiser evitar digitar sudo sempre que você executar o comando docker, adicione seu nome de usuário no grupo docker:

    sudo usermod -aG docker ${USER}

Para inscrever o novo membro ao grupo, saia do servidor e logue novamente, ou digite o seguinte:

    su - ${USER}

Confirme que seu usuário agora está adicionado ao grupo docker digitando:

    id -nG

Se você precisar adicionar um usuário ao grupo docker com o qual você não está logado, declare esse nome de usuário explicitamente usando:

    sudo usermod -aG docker username

Agora basta digitar seu usuário e senha uma única vez

    su - username

---

## Comandos Docker

Executar a instancia de uma imagem, ou seja iniciar um container

    docker run image-container

Listar todos os containers que estão sendo executados na máquina

    docker ps

Listar todos os containers existentes na máquina

    docker ps -a

Parar a execução de container

    docker stop container-name

Remover um container

    docker rm container-id

Listar todas imagens presentes na máquina

    docker images

Remover uma imagem (para remover uma imagem, todos os containers que dependem dela devem ser parados antes)

    docker rmi image-container

Executar um container por um tempo específico (o parametro _sleep_ recebe o tempo em segundos)

    docker run container-name sleep 60

Executar um comando dentro de um container que está em execução

    docker exec container-name cat /directory

Excecutar um container em modo de teste (o container será executado em segundo plano)

    docker run -D image-name

Retornar há um container específico

    docker attach container-id
