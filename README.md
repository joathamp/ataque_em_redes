Base de Dados das imagens(.box) usadas no treinamento de Ataque em Redes - Daryus
=============================

Repositório para armazenar os DUMPS usados para o treinamento de Ataque em Redes da **Daryus**

Dependências
------------

Para a criação do laboratório é necessário ter pré instalado os seguintes softwares:

* [Git][2]
* [VirtualBox][3]

> Para as máquinas com MAC OS aconselhamos, se possível, que as instalações sejam feitas pelo gerenciador de pacotes **brew**.

Maquina do Pentester
-----------

Para que o **Lab** aconteca, estamos levando em consideracao que estamos trabalhando com a modalidade BlackBox, desta forma nem uma informacao nos 'e fornecida:


Nesse laboratório, que está centralizado nas **.Box** do [Vagrant][3], são sugeridas 2 distribuicoes que auxiliam no processo de Pentest:

Nome       | vCPUs | Memoria RAM | IP             | S.O.¹           | Link para Download²
---------- |:-----:|:-----------:|:--------------:|:---------------:| -----------------------------
Kali Linux | 1     | 3072MB      | 192.168.56.100 | Kali Linux      | [https://www.kali.org/get-kali/][5]
Parrot     | 1     | 3072MB      | 192.168.56.101 | Parrot          | [https://www.parrotsec.org/][6]

> **¹**: Esses Sistemas operacionais estão sendo utilizado no formato de OVAs (Open Virtualization Appliances), é a forma como o VirtualBox chama as imagens do sistema operacional utilizado.

> **²**: Link para o Download de cada distribuicao sugerida

Criação do Laboratório 
----------------------

O Laboratório será criado utilizando o [Vagrant][7]. Ferramenta para criar e gerenciar ambientes virtualizados (baseado em Inúmeros providers) com foco em automação.

Nesse laboratórios, que está centralizado no arquivo [Vagrantfile][8], serão criadas 4 maquinas com as seguintes características:

Nome       | vCPUs | Memoria RAM | IP            | S.O.¹           
---------- |:-----:|:-----------:|:-------------:|:---------------
SD    | 1     | 3072MB      | 192.168.56.110 | ????        | 
MR | 1     | 3072MB      | 192.168.56.120 | ???? 
XXXX    | 1     | 4092MB      | 192.168.56.30 | ????       
XXXX | 1     | 2048MB      | 192.168.56.40 | ???? 

> **¹**: Esses Sistemas operacionais estão sendo utilizado no formato de Boxes, é a forma como o vagrant chama as imagens do sistema operacional utilizado, sendo que a que vamos utilizar são as imagens preparadas por mim: **joatham/Daryus_SD**, **joatham/Daryus_MR**, 


Para ter acesso as maquinas que usaremos nas Invasoes é necessário fazer o `git clone` desse repositório e realizar a descompactacao dos arquivos, conforme abaixo:

```bash
git clone https://github.com/joathamp/ataque_em_redes.git
cd ataque_em_redes/
```

Por fim, para melhor utilização, abaixo há alguns comandos básicos do vagrant para gerencia das máquinas virtuais.

Comandos                | Descrição
:----------------------:| ---------------------------------------
`vagrant init`          | Gera o VagrantFile
`vagrant box add <box>` | Baixar imagem do sistema
`vagrant box status`    | Verificar o status dos boxes criados
`vagrant up`            | Cria/Liga as VMs baseado no VagrantFile
`vagrant provision`     | Provisiona mudanças logicas nas VMs
`vagrant status`        | Verifica se VM estão ativas ou não.
`vagrant ssh <vm>`      | Acessa a VM
`vagrant ssh <vm> -c <comando>` | Executa comando via ssh
`vagrant reload <vm>`   | Reinicia a VM
`vagrant halt`          | Desliga as VMs

> Para maiores informações acesse a [Documentação do Vagrant][13]


Contato
----------------------

Entre em contato conosco.

Continue aprofundando seus conhecimentos, utilize este material para continuar praticando. 


Um forte abraco do Jota e do Vitor e de toda a equipe da Daryus, bons estudos e a gente se ve por ai:

* **Msc. Joatham Pedro**
  * **Perito Computacional**
  * **Pentester**
  * **Mestre em Sistemas e Computação** 
  * **Analista Sênior de Segurança da Informação - 4Linux** 
  * **Analista/Gerente de Seguranca - IFTO**   
  * **Instrutor MBA Cybersecurity Gov TI - FATEC Cuiabá**
  * **Instrutor  MBA Cybersecurity - IMPACTA**
  * **Instrutor Pos Graduacao Computação Forense - Daryus**
  * **Linux Professional Institute I** 
  * **Linux Professional Institute II** 
  * **Linux Professional Institute III - Security** 
  * **Datacenter Techical Specialist** 
  * **Novell Certified Linux Administrator (CLA)** 
  * **Computer Hacking Forensic Investigation - C|HFI** 
  * **Ec-Concil Incident Handler - EC|IH** 
  * **Certified Ethical Hacker - C|EH** 
  * **Exin Ethical Hacker - EXIN** 
  * **DevOps Essential Professional - DEPC** 
  * **Pos-Graduado em Redes de Computadores**
  * **Bacharel em Ciencia da Computacao**
  * **https://www.youtube.com/c/EaiQualteupapo**
  * **https://www.linkedin.com/in/joatham-pedro-44a3351b/**
  * **https://www.instagram.com/qualteupapo/**
  * **https://www.instagram.com/joatham.pedro/**

[1]: https://impacta.com.br/
[2]: https://git-scm.com/downloads
[3]: https://www.virtualbox.org/wiki/Downloads
[5]: https://www.kali.org/get-kali/
[6]: https://www.parrotsec.org/
