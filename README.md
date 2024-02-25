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