# Relatório Técnico sobre Acesso SSH no EC2

## Autora: 

<a href="https://www.linkedin.com/in/anna-aragao/"> Anna Aragão </a>

## Sumário 

- [Relatório Técnico sobre Acesso SSH no EC2](#relatório-técnico-sobre-acesso-ssh-no-ec2)
  - [Autora:](#autora)
  - [Sumário](#sumário)
- [1. Introdução](#1-introdução)
- [2. Objetivo](#2-objetivo)
- [3. Materiais](#3-materiais)
- [4. Método](#4-método)
- [5. Conclusão](#5-conclusão)


# 1. Introdução 

&nbsp;&nbsp;&nbsp;&nbsp;A instância EC2 (Elastic Compute Cloud) na AWS (Amazon Web Services) é uma máquina virtual que provisiona e executa na infraestrutura de nuvem da AWS, ou seja, ao invés de despender do próprio recurso de infraestrutura, utiliza-se a coleção de elementos de hardware e software da AWS para permitir a computação em nuvem, como a capacidade de computação, rede e armazenamento e a interface para os usuários acessarem os recursos que estão virtualizados. 

&nbsp;&nbsp;&nbsp;&nbsp;A criação de uma instância EC2 leva fatores como os requisitos do aplicativo que será trabalhado ou carga de trabalho, visando a identificação do tipo de instância que melhor atenda ao usuário. Como exemplo, existem instância otimizadas para computação, armazenamento, análise de dados e outros tipos de instâncias. 

&nbsp;&nbsp;&nbsp;&nbsp;Desta forma, as instâncias EC2 são altamente escaláveis e flexíveis, auxiliando o usuário a aumentar ou diminuir a sua capacidade computacional de acordo com a sua necessidade de uma forma rápida, prática e menos custosa. 

# 2. Objetivo 

&nbsp;&nbsp;&nbsp;&nbsp;O objetivo deste relatório técnico é fornecer um passo a passo sobre o acesso SSH (Secure Shell) em instâncias EC2 na plataforma da AWS. O relatório destina-se a oferecer orientalhões para garantir a segurança e eficácia do acesso SSH a instância EC2, abordando aspectos como:
1. Configuração inicial;
2. Gerenciamento de Chaves;
3. Configuração de redes;
4. Conexão com Putty. 

&nbsp;&nbsp;&nbsp;&nbsp;Ao seguir o passo a passo, pode-se compreender os fundamentos para o acesso SSH em instâncias EC2 de forma segura e bem gerenciada. 

# 3. Materiais

&nbsp;&nbsp;&nbsp;&nbsp;Para compreender o acesso SSH em instâncias EC2 na AWS, é essencial estar familiarizado com os materiais que serão utilizados no processo, que são o SSH, EC2, AWS, PuTTY e GitHub. Cada um dos materiais desempenha um papel crucial na configuração e utilização segura das instâncias. A seguir, serão explorados detalhadamente cada um desses elementos: 

1. SSH (Secure Shell): 
&nbsp;&nbsp;&nbsp;&nbsp;Protocolo de rede que permite a comunicação segura entre os dispositivos, utilizado para acesso remoto a servidores e sistemas. Desta forma, o usuário acessa, controle e/ou transfere dados de uma maneira segura por meio de uma conexão criptografada. 

2. EC2 (Elastic Compute Cloud):
&nbsp;&nbsp;&nbsp;&nbsp;Serviço de computação em nuvem oferecido pela AWS que provisiona e executa máquinas virtuais, sendo altamente escaláveis e flexígeis em suas configurações e demandas de uso. 

3. AWS (Amazon Web Services): 
&nbsp;&nbsp;&nbsp;&nbsp;Plataforma de computação em nuvem presente globalmente que oferece serviços de infraestrutura, armazenamento e outros serviços. É possível gerenciar seus aplicativos na nuvem de forma flexível e escalável. 

4. PuTTY: 
&nbsp;&nbsp;&nbsp;&nbsp;Software que permite criar conexões com servidores e dispositivos remotamente. 

5. GitHub: 
&nbsp;&nbsp;&nbsp;&nbsp;Plataforma de hospedagem de código e utiliza o controle de versionamento do Git, auxliando no trabalho em conjunto de equipes de desenvolvedores. 

# 4. Método

&nbsp;&nbsp;&nbsp;&nbsp;O método consiste na explicação detalha e de passo a passo para a criação de uma instância na plataforma da AWS. Ao executar o passo a passo, o usuário conseguirá ter acesso SSH em instâncias EC2 na plataforma da AWS. Para ser o mais didático possível, será fornecido apoio visual de todo o processo. 

**1. Acessar AWS:**

<div align = "center">
<sub> Figura 01 - Acessar conta AWS  </sub>
<img src="/assets/aws.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;O primeiro passo se baseia em acessar a sua conta da AWS. Caso não tenha, cadastre-se para poder seguir o passo a passo corretamente. No caso do exemplo, esta é uma conta estudantil. 

**2. Acessar Painel de Controle:**

<div align = "center">
<sub> Figura 02 - Acessar Painel de Controle  </sub>
<img src="/assets/painelControle.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ao entrar na página, encontre o Painel de Controle e escolha a opção a melhor opção que irá favorecer a criação de sua instância. Nesse caso, por ser uma conta estudantil, iremos escolher a opção "AWS Academy Learner Lab [72994]". Nele, selecione o "Módulos" e escolha a opção "Iniciar os laboratórios de aprendizagem da AWS Academy". 


**3. Acessar o Lab:**

<div align = "center">
<sub> Figura 03 - Acessar Learner Lab  </sub>
<img src="/assets/Lab.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Preste atenção no símbolo vermelho da AWS. Após você clicar em "Start Lab" no menu superior a direita e aguardar alguns segundos, o símbolo vermelho ficará verde e ao clicar nele, você irá acessar o Learner Lab. 

**4. Página Inicial do Console:**

<div align = "center">
<sub> Figura 04 - Página Inicial do Console  </sub>
<img src="/assets/paginaConsole.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Você será redirecionado para a Página Inicial do Console, onde iremos buscar na barra de busca pela palavra "EC2", que é a máquina virtual onde iremos executar a nossa primeira instância. Agora, clique no EC2 que você buscou na barra e clique novamente em "Instâncias". 

**5. Instâncias:**

<div align = "center">
<sub> Figura 05 - Instâncias </sub>
<img src="/assets/instancias.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Essa página nos mostra quais instâncias temos em execução atualmente e nos permite criar outras instâncias. Clique no botão laranja no canto superior direito da tela chamado "Executar Instâncias". 

**6. Criando Instância:**

<div align = "center">
<sub> Figura 06 - Criando Instância parte 1  </sub>
<img src="/assets/instancia1.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Vamos iniciar o processo de criação da nossa instância. Primeiro, iremos escolher o "Norte da Virgínia" como o data center que iremos criar essa instância. Entenda que mesmo que esse processo seja realizado em nuvem, virtualmente falando, existe um data center real que iremos usufruir de seus serviços. Nesse caso, criaremos nossa instância no data center da AWS localizado em Norte da Virgínia. Também existe um localizado em São Paulo. 

&nbsp;&nbsp;&nbsp;&nbsp;Agora, daremos um nome para a instância. No meu caso, irei colocar "inst-anna". 

<div align = "center">
<sub> Figura 07 - Imagens de aplicação e de sistema operacional  </sub>
<img src="/assets/instancia2.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Vamos escolher a configuração do software, ou seja, o sistema operacional para executar a instância. No meu caso, escolhei o Amazon Linux, mas sinta-se à vontade para escolher outro sistema que melhor te favoreça. 

<div align = "center">
<sub> Figura 08 - Tipo de Instância e Par de chaves  </sub>
<img src="/assets/instancia3.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Na área de Tipo de instância, podemos continuar com o t2.micro, pois é qualidade para o nível gratuito (e neste caso como estamos somente testando, não precisamos de grande poder computacional). Abaixo, temos Par de Chaves, ou seja, ele vai ser como se fosse a nossa senha para conectar à instância com segurança. Clique em "Criar novo par de chaves". 

<div align = "center">
<sub> Figura 09 - Criando Par de Chaves  </sub>
<img src="/assets/instancia4.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ao clicar, abrirá essa pequena tela pedindo o nome das suas chaves, o tipo e o formato. Irei colocar o nome como "keys", o tipo RSA e o formato do arquivo em .ppk para utilizar com o PuTTY (não se preocupe, iremos explicar no final de todo esse processo). Ao final, clique em "Criar par de chaves" e escolha em qual pasta você irá guardar o arquivo. **Lembre-se de guardar muito bem esse arquivo, pois ele será muito útil daqui a pouco**. 

<div align = "center">
<sub> Figura 10 - Configurações de rede </sub>
<img src="/assets/instancia6.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

<div align = "center">
<sub> Figura 11 - Configurações de rede </sub>
<img src="/assets/instancia5.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>


&nbsp;&nbsp;&nbsp;&nbsp;Agora, iremos configurar a rede. Iremos primeiro habilitar todas as opções do grupo de segurança e depois clicar em "Editar". 

<div align = "center">
<sub> Figura 12 - SSH </sub>
<img src="/assets/instancia7.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ao clicar em Editar, a parte mais importante é verificar se um dos tipos habilitados é o **ssh** e o Tipo de origem é de **Qualquer lugar**. Lembre-se que ao lado em Origem, deve ter a marcação 0.0.0.0/0, pois significa que as regras com origem 0.0.0.0/0 permitem que todos os endereços IP acessem sua instância.

<div align = "center">
<sub> Figura 13 - Executar Instância </sub>
<img src="/assets/instancia8.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Continuaremos com a mesma configuração de armazenamento e iremos clicar no lado direito inferior no botão "Executar instância". 

<div align = "center">
<sub> Figura 14 - Êxito ao Executar Instância </sub>
<img src="/assets/instancia9.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Caso você visualize essa tela, PARABÉNS!!! Você criou a sua primeira instância dentro da AWS! Caso não tenha conseguido, não fique triste. Reveja todo o passo a passo da documentação e veja se não esqueceu de algo! Estamos aqui justamente para te ajudar. 

&nbsp;&nbsp;&nbsp;&nbsp;Agora, instale o PuTTY para acessarmos o SSH pelo cliente PuTTY SSH. 

<div align = "center">
<sub> Figura 15 - Configurações do PuTTY </sub>
<img src="/assets/putty.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

<div align = "center">
<sub> Figura 16 - Endereço de IP </sub>
<img src="/assets/ip.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Em "Host Name", adicione o endereço de IP da sua instância. Depois, na barra lateral esquerda, clique no botão de "+" ao lado de "SSH", faça o mesmo para "Auth" e clique em "Credentials". 

<div align = "center">
<sub> Figura 17 - Private key </sub>
<img src="/assets/key.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Clique no botão "Browse..." do Private key file for authentification e escolha **aquele par de chaves que salvamos nas primeiras etapas do processo de criação da instância**. Depois disso, clique em "Open" e "Accept". 

<div align = "center">
<sub> Figura 18 - Login </sub>
<img src="/assets/login.png">

<sup> Fonte: Material produzido pelos autores (2024) </sup>
</div>

&nbsp;&nbsp;&nbsp;&nbsp;Ao entrar, o PuTTY irá pedir o seu login, onde você colocará "ec2-user". PARABÉNS! Sua autentificação foi concluída! 

# 5. Conclusão

&nbsp;&nbsp;&nbsp;&nbsp;Utilizar instâncias EC2 permite obter alta flexibilidade e escalabilidade para a computação em nuvem, fornecendo recursos computacionais de acordo com as necessidades do usuário. 
&nbsp;&nbsp;&nbsp;&nbsp;Desta forma, o relatório forneceu um passo a passo para um acesso SSH a essas instâncias da AWS, passando pela configuração geral da instância, gerencimaneto de chaves e conexão ao PuTTY. 
&nbsp;&nbsp;&nbsp;&nbsp;Ao ler o relatório, o usuário entenderá os procedimentos e poderão garantir um acesso seguro das instâncias na plataforma e aproveitar da melhor maneira possível os recursos da AWS. 