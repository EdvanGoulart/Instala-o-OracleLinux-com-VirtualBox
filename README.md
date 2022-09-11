# Instalação Oracle Linux v8.6 no Virtual Box
## Introdução 
Esse projeto documenta todo processo de instalação de um servidor linux usando Oracle Linux v8.6 no ambiente Virtual Box.

### Ferramentas Necessárias
Para a Virtualização estamos utilizando o [VirtualBox](https://www.virtualbox.org).<br>
Para o Servidor Linux estamos utilizando a distribuição [Oracle Linux](https://yum.oracle.com/oracle-linux-isos.html).

Versões Utilizadas:
* Oracle Linux v8.6
* VirtualBox v6.1

## 1. Criar Máquina Virtual
Depois de fazer a instalação do Virtual Box, vamos inicia-lo e na tela principal iremos selecionar a opção "Novo".

![vm1](https://user-images.githubusercontent.com/78823528/189496765-157a631b-925d-4336-bcfa-28f3d6caa25c.png)

### Configuração Inicial

Depois de clicar em "Novo" aparecerá uma nova aba, onde faremos a configuração a seguir.

**Nome e Sistema Operacional**

* O nome de sua preferência para sua Máquina (Caso coloque o nome de uma distribuição ou SO o Virtual Box já preenche os demais campos automaticamente)
* Selecione o diretório de instalação para sua Máquina Virtual
* O tipo do Sistema Operacional (Linux)
* A distribuição/Versão do Sistema Operacional (Oracle 64bits)

**Tamanho da Memória**

O tamanho de memória RAM a ser instalada na sua máquina, por padrão o Virtual Box define 1GB, mas recomendamos 2GB para que não sofra com lentidão ao usa-la.
> OBS: Não ultrapasse o limite de memória que está ilustrado na cor VERDE.

**Disco Rígido**

Selecione a opção "Criar um novo disco rígido virtual agora" e clique em "Criar".

![vm2](https://user-images.githubusercontent.com/78823528/189500534-c85fe176-0634-4d15-9657-b76a5977ed11.png)

### Criar Disco Rígido Virtual

Ao clicar em "Criar" aparecerá uma aba para fazermos a configuração de Disco Rígido.

**Localização do arquivo**

Informe o diretório para o disco.

**Tamanho do arquivo**

Informe o tamanho do disco que deseja, neste projetos deixamos apenas 12GB, mas é recomendado mais dependendo de seu uso.

**Tipo de Arquivo de Disco**

Deixe selecionado a opção Padrão "VDI(VirtualBox Disk Image)", que pode montar um disco rígido separado, criando uma nova máquina virtual utilizando VirtualBox.

**Armazenamento em disco físico**

Deixe selecionado a opção "Dinamicamente Alocado".


<br>


Após fazer as configurações acima clique em "Criar", para finalizar a criação da Máquina Virtual.




![vm3](https://user-images.githubusercontent.com/78823528/189500711-35b8099c-4c32-4fb8-bc0b-cd786973a757.png)


## 2. Configurando a Máquina Virtual

Depois de criarmos a máquina virtual devemos seleciona-la e clicar em "Configurações".

![vm4](https://user-images.githubusercontent.com/78823528/189504970-9d21cf31-2839-451c-af34-9571f54fb8b3.png)


### Sistema

Em Sistema, selecione a coluna "Processador", nela é recomendado utilizar dois CPUs para maior performance, como o Linux é leve isso será suficiente.

![vm5](https://user-images.githubusercontent.com/78823528/189505364-db5788d4-e02e-4e99-ac52-b3f5e700cf46.png)

### Armazenamento

Em Armazenamento, você vai selecionar "Vazio" abaixo de "Controladora: IDE", depois a direita em "Drive Óptico selecionar o ícone de CD, onde você irá clicar em "Escolher uma imagem de disco" para pegar a ISO do Oracle Linux que foi baixada.

![vm6](https://user-images.githubusercontent.com/78823528/189505785-6f8504d2-ee6e-4727-a21c-b3c99440943f.png)

### Rede

Por fim, na Rede em "adptador1" mude a conexão em "Conectado a :" de "NAT" para "Placa em modo Bridge".

![vm7](https://user-images.githubusercontent.com/78823528/189506371-c8c046ad-a322-47ae-ace1-c0a3f3345a16.png)



## 2.  Instalando e Configurando o Oracle Linux 

Depois de a máquina estar configurada, iremos intalar e configurar o Oracle linux.
Clique em "Iniciar", para iniciar a máquina virtual.

![vm8](https://user-images.githubusercontent.com/78823528/189506967-4ecd1fdb-ff30-4be1-8c9f-caa64fdc6317.png)

### Instalação

Após iniciar, selecione a opção "Install Oracle Linux 8.6.0"

![vm9](https://user-images.githubusercontent.com/78823528/189507613-0ca46bbb-32b7-40e6-8f17-3bc4e9c05e56.png)

### Selecionando o idioma 

Nessa parte selecionaremos o idioma do Sistema Operacional, neste projeto mantivemos o padrão Inglês.
Selecione o idioma desejado e clique em continuar.

![vm10](https://user-images.githubusercontent.com/78823528/189507726-73314056-3d1e-4382-8b75-3ed3245dda34.png)

### Sumário de Instalação

Após clicar em continuar, chegamos ao Sumário de instalação onde Faremos algumas configurações conforme a numeração.

![vm11](https://user-images.githubusercontent.com/78823528/189510091-bb0d9444-8b7e-4f53-b8f7-0d9cf05e3ebd.png)

#### 1 - Keyboard (Teclado)

Após selecionar a opção Keyboard, clique na opção de lingua inglesa e remova-a clicando no ícone "-" abaixo.
Após remover, clique no ícone "+" e adicione a opção "Portuguese (Brasil)", depois clique em "Done" acima para confirmar a alteração.

![vm12](https://user-images.githubusercontent.com/78823528/189508093-96f1712a-f421-4114-990e-32ae78d16d15.png)

#### 2- Time & Date (Data e Hora)

Na opção Time e Date, basta selecionar sua região nos devidos campos para que o horário seja definido de acordo com sua região.


![vm13](https://user-images.githubusercontent.com/78823528/189508535-40352ecd-0206-4bc1-854a-22634c02f704.png)


#### 3- Software Selection

Nesta opção iremos marcar a opção de Minimal Install, para que o Oracle Linux não possua interface gráfica e possua apenas configurações básicas.

![vm14](https://user-images.githubusercontent.com/78823528/189509227-507f0468-6564-4851-908e-8979629884cd.png)

#### 4- Installation Destine

Nesta opção, manteremos as configurações padrões pois não utilizaremos nada avançado.

![vm15](https://user-images.githubusercontent.com/78823528/189510115-26d839f9-dd7e-4f77-a80f-03d06cae05e2.png)

#### 5- Network e Host Name
Como nossa Máquina está condigurada em Modo Bridge, podemos altera-la clicando no botão e passando pra "ON", para que a máquina já suba com o IP e acesso a internet.

![vm16](https://user-images.githubusercontent.com/78823528/189509734-0dad697b-a145-47b7-be25-475b63f43046.png)

#### 5- Root Password

Nesta opção definimos a senha para o administrador do Sistema Operacional e depois basta clicar na opção "Begin Installation", para concluir a instalação.

![vm17](https://user-images.githubusercontent.com/78823528/189510008-35dcc073-748e-41ee-99c9-2bf1f8e2459e.png)





















  


