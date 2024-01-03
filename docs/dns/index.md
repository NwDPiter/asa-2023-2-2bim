# DNS

## Instalação

-   samba
-   krb5

## Configuração
    
1º - Vamos configurar o nome de nossa máquina com o nome de nosso dominio em: (/etc/hostname)

    EX: berlin.alemanha.lab

2º - Agora configura a linha do local host em: (/etc/hosts)

    EX: berlin.alemanha.lab

2.1 - Faça um backup do arquivo smb.conf que está em: (/etc/samba/smb.conf)

3º - Após isso vamos configura nosso domínio usando:

-   samba-tool domain provision --use-rfc2307 --interactive


Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração.

Cinco registros (4 pontos cada):

- 3 do tipo A (Endereços);
- 2 do tipo CNAME (`www` e `docs`);

## Teste

[![dns](https://i.im.ge/2023/12/22/xuDmFM.dns.jpg)](https://im.ge/i/xuDmFM)
