# Instalando o Python

Existem diferentes maneiras de preparar o ambiente para essa disciplina.
No geral, nós queremos que o interpretador python e as dependencias usuais
para trabalahos científicos sejam instalados.

Algumas opções estão descritas abaixo:

## Anaconda

Anaconda é uma distribuição de python "pronta para uso"
contendo todos os pacotes necessários já instalados.
Tanto para o [Windows](https://docs.anaconda.com/anaconda/install/windows)
quanto para o [Linux](https://docs.anaconda.com/anaconda/install/linux),
um instalador pode ser baixado do site oficial.

### Windows

1. Baixe o instalador contido no endereço
[https://repo.anaconda.com/archive/Anaconda3-5.1.0-Windows-x86_64.exe](https://repo.anaconda.com/archive/Anaconda3-5.1.0-Windows-x86_64.exe),
execute-o e continue a instalação clicando em `I Agree` e `Next`.

2. Mantenha as opções avançadas como estão e clique em `Install`.

3. Na tela `Install Microsoft VS`, você pode pular se já possuir outro
   editor de texto/IDE clicando em `skip`.

4. Procure o programa `Anaconda Navigator` no menu iniciar e execute-o.


### Linux

1. Baixe o pacote de instalação e o coloque em uma pasta de fácil acesso:

    ```shell
    cd ~/Downloads
    wget https://repo.anaconda.com/archive/Anaconda3-5.1.0-Linux-x86_64.sh
    chmod 700 Anaconda3-5.1.0-Linux-x86_64.sh
    ./Anaconda3-5.1.0-Linux-x86_64.sh
    ```

2. Role a licença até o fim com o `Enter` e concorde com ela escrevendo
   "yes", quando solicitado.

3. O instalador irá perguntar se deseja colocar o conda no seu `PATH`.
   É importante responder sim aqui.

4. Execute o programa `Anaconta Navigator` abrindo um terminal e digitando
   `anaconda-navigator`.

## Instalação local, Linux (Debian)

Se você é um usuário linux, um outro jeito "enxuto" de instalar o python
é manualmente. Aqui, você precisa descrever os pacotes a serem utilizados
individualmente:

```
sudo apt install python3 python3-dev python3-pip
python --version
pip install --user --upgrade numpy        \
                             scipy        \
                             matplotlib   \
                             scikit-learn \
                             jupyter
```

**Atenção:** é preciso garantir que `/home/{username}/.local/bin`
esteja em seu `PATH`, para que os executores sejam feitos visíveis.

Se quiser instalar globalmente:

```shell
sudo apt install python3 python3-dev python3-pip
sudo pip install --upgrade numpy        \
                           scipy        \
                           matplotlib   \
                           scikit-learn \
                           jupyter
```

Aqui não precisa de nenhum passo adicional.

Na instalação local, você não terá acesso ao Anaconda Navigator.
Entretanto, você pode executar um server jupyter (e assim ler e criar
arquivos `.ipynb`) com o seguinte comando:

```shell
jupyter notebook
``` 

# Leitura de suporte

Veja a [documentação](https://docs.anaconda.com/) do anaconda para mais
detalhes na instalação do mesmo.
