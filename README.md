# aws-loadbalancer-ansible
Está é uma playbook no ansible para provisinarmos uma aplicação web na AWS

<div align="center" style="float: left">
  <img alt="chart" width="250" src="https://github.com/guilhermewolf/aws-loadbalancer-ansible/blob/master/chart.png" />
</div>



# Algumas alterações são necessarias
## Dentro de group_var/
  Apague o arquivo all e crie um novo com os seguintes parametros:

    ---
    db_name: demo
    db_user: demo
    db_pass: teste
    aws_access_key: ###SUACHAVE###
    aws_secret_key: ###SUACHAVE##
## Dentro de inventory/hosts
  Altere esse parametro com sua keypair usada para provisionar as maquinas

    ansible_ssh_private_key_file= ##SUACHAVE##
  > **Note:** No exemplo criei uma key pair chamada ansible e coloquei o arquivo no meu diretorio home
