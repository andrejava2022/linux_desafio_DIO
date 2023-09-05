# Desafio Linux
## Incrível desafio da DIO 

#!/bin/bash

#echo "Criando diretórios..."

mkdir /publico
mkdir /adm
mkdir /ven
mkdir /sec 

echo "Criando grupos..."

groupadd GRP_ADM
groupadd GRP_VEN
groupadd GRP_SEC

echo "Criando usuários..."

useradd carlos -m -s /bin/bash
useradd maria -m -s /bin/bash
useradd joao -m -s /bin/bash
useradd debora -m -s /bin/bash
useradd sebastiana -m -s /bin/bash
useradd roberto -m -s /bin/bash
useradd josefina -m -s /bin/bash
useradd amanda -m -s /bin/bash
useradd rogerio -m -s /bin/bash

echo "Colocando o root como dono dos diretórios..."

chown root /adm
chown root /publico
chown root /ven
chown root /sec

echo "Dando permissão total para usuarios somente aos seus respectivos diretorios, e nenhuma permissão para intrusos..."

chmod 700 /carlos
chmod 700 /maria
chmod 700 /joao
chmod 700 /debora
chmod 700 /sebastiana
chmod 700 /roberto
chmod 700 /josefina
chmod 700 /amanda
chmod 700 /rogerio

echo "Dando permissão de acesso aos diretórios de grupo somente quem faz parte do grupo..."

chown root:GRP_ADM adm
chown root:GRP_VEN ven
chown root:GRP_SEC sec


