# aws-loadbalancer-ansible
Algumas alterações são necessarias
dentro de group_var/
  apague o arquivo all e crie um novo com os seguintes parametros
    ---
    db_name: demo
    db_user: demo
    db_pass: teste
    aws_access_key: ###SUACHAVE###
    aws_secret_key: ###SUACHAVE##
dentro de inventory/hosts
  altere esse parametro com sua keypair usada para provisionar as maquinas
    ansible_ssh_private_key_file=
  no exemplo criei uma key pair chamada ansible e coloquei o arquivo no meu diretorio home
