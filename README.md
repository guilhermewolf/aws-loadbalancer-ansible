# aws-loadbalancer-ansible
Está é uma playbook no ansible para provisinarmos uma aplicação web na AWS

<div align="center" style="float: left">
  <img alt="chart" width="250" src="https://github.com/guilhermewolf/aws-loadbalancer-ansible/blob/master/chart.png" />
</div>




  > **Note:** No exemplo criei uma key pair chamada ansible e coloquei o arquivo no meu diretorio home

#  Começamos baixando nossos arquivos
```shell
git clone https://github.com/guilhermewolf/aws-loadbalancer-ansible.git
```
# Algumas alterações são necessarias
##  Vamos editar dois arquivos 

  	group_vars/all.yml
  		altere o nome da chave que você criou na AWS (key_name)
  	inventory/hosts
  		altere o local onde está a chave na sua maquina (ansible_ssh_private_key_file)

##  Vamos colocar nossas credenciais da AWS como variáveis de ambiente
```shell
export AWS_ACCESS_KEY_ID= #SUA ACESSKEY#
export AWS_SECRET_ACCESS_KEY= #SUA SECRET KEY#
```
  All set, let go!
```shell
ansible-playbook playbook.yml
```
  Agora veja toda a infraestrutura ser provisionada diante de seus olhos.
