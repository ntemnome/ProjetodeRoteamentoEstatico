# ProjetodeRoteamentoEstatico

Switch-01

enable
configure terminal
hostname SW-01
banner motd "ACESSO AUTORIZADO APENAS PARA O DEPARTAMENTO DE TI"
enable secret SenhadaEnable
line console 0
password SenhadaConsole
login
exit
service password-encryption
ip domain-name peachanddaisy.local
username administrador privilege 15 secret SenhaAdmin
username estagiario privilege 1 secret SenhaEst
line vty 0 15
transport input ssh
login local
exec-timeout 5
do wr
crypto key generate rsa general-keys modulus 1024
service password-encryption
end
enable
interface vlan 10
configure terminal
ip address 192.168.1.30 255.255.255.224
end
configure terminal
ip address 192.168.1.10 255.255.255.224


----------------------------------------

Switch-02

enable
configure terminal
hostname SW-02
banner motd "ACESSO AUTORIZADO APENAS PARA O DEPARTAMENTO DE TI"
enable secret SenhadaEnable
line console 0
password SenhadaConsole
login
exit
service password-encryption
ip domain-name peachanddaisy.local
username administrador privilege 15 secret SenhaAdmin
username estagiario privilege 1 secret SenhaEst
line vty 0 15
transport input ssh
login local
exec-timeout 5
do wr
crypto key generate rsa general-keys modulus 1024
service password-encryption
end
enable
configure terminal
interface vlan 20
ip address 10.40.15.254 255.255.240.0
end

------------------------------------------

Switch-03

enable
configure terminal
hostname SW-03
banner motd "ACESSO AUTORIZADO APENAS PARA O DEPARTAMENTO DE TI"
enable secret SenhadaEnable
line console 0
password SenhadaConsole
login
exit
service password-encryption
ip domain-name peachanddaisy.local
username administrador privilege 15 secret SenhaAdmin
username estagiario privilege 1 secret SenhaEst
line vty 0 15
transport input ssh
login local
exec-timeout 5
do wr
crypto key generate rsa general-keys modulus 1024
service password-encryption
end
enable
configure terminal
interface vlan 30
ip address 192.168.0.126 255.255.255.128

------------------------------------------

Switch-04

enable
configure terminal
hostname SW-02
banner motd "ACESSO AUTORIZADO APENAS PARA O DEPARTAMENTO DE TI"
enable secret SenhadaEnable
line console 0
password SenhadaConsole
login
exit
service password-encryption
ip domain-name peachanddaisy.local
username administrador privilege 15 secret SenhaAdmin
username estagiario privilege 1 secret SenhaEst
line vty 0 15
transport input ssh
login local
exec-timeout 5
do wr
crypto key generate rsa general-keys modulus 1024
service password-encryption
end
enable
configure terminal
interface vlan 40
ip address 172.16.43.254 255.255.254.0






























