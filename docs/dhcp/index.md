# DHCP

## Instalação

-   dnsmasq

## Configuração

1º - Aquivo de configuração do dnsmasq é:

    /etc/dnsmasq.conf

mas, vamos criar um arquivo (exemplo.conf) no diretório (dnsmasq.d)

    /etc/dnsmasq.d/exemplo.conf

todas as configurações no arquivo(exemplo.conf) vai migra para dnsmasq.conf.

2º - Editando o arquivo **exemple.conf** a configuração padrão é essa:

* Define a interface de rede que vai ser dhcp

        EX: interface= eht1

* Define a faixa de ip   (inicial , ip final , mascara de rede , tempo que o dispositivo fica com o ip)

        EX: dhcp-range= 192.168.0.10, 192.168.0.254 , 255.255.255.0 , 12h

* Define um dns 

        EX: dhcp-option= 3 , 192.168.0.1  (3: Identifica o servidor DNS)

* Define outro dns (**Opicional**)

        EX: dhcp-option= 6 , 8.8.8.8  (6: Identifica o servidor DNS)

* Define um domínio (**Opicional**)

        EX: dhcp-option= 15, nome-domínio      (15: Especifica um domínio se caso você esteja em um)

* Informa onde será o log do serviço

        EX: log-facility= /var/log/dnsmasq.log

* Infoma os IPs fixos

        EX:dhcp-host= Ip-da-máquina, Mac-da-máquina

Arquivo de configuração do dnsmasq

[![config-dhcp](https://i.im.ge/2024/01/03/xeHYSM.config-dhcp.png)](https://im.ge/i/xeHYSM)


Esse será o modo de configura no linux (alpine)

[![config-ip](https://i.im.ge/2024/01/03/xeHcVD.config-ip.png)](https://im.ge/i/xeHcVD)

É esse no windows


[![imagem_2024-01-02_172142542](https://i.im.ge/2024/01/03/xeGUuf.imagem-2024-01-02-172142542.png)](https://im.ge/i/xeGUuf)


## Teste

[![teste](https://i.im.ge/2024/01/03/xeHb6Y.teste.png)](https://im.ge/i/xeHb6Y)
