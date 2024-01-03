# SMB

## Instalação

-   samba-ad
-   krb5-config

## Configuração


1º - Vamos configurar o nome de nossa máquina com o nome de nosso dominio em: (/etc/hostname)

    berlin.alemanha.lab

2º - Agora configura a linha do local host em: (/etc/hosts)

    berlin.alemanha.lab

2.1 - Faça um backup do arquivo smb.conf que está em: (/etc/samba/smb.conf)

3º - Após isso vamos configura nosso domínio usando:

-   samba-tool domain provision --use-rfc2307 --interactive

4º - Despois de criar seu dominio vamos configurar o aquivo smb.conf que está em: (/etc/samba)

![Alt text](Fotos-SMB/Foto1.png)

Nesse imagem mostra a configuração do compartilhamento de pasta com o windows, foram criadas duas pastas [Carvalho] e [sales]

5º - Agora vamos nos conctar ao domínio que criamos pelo windows vá em:

![Alt text](Fotos-SMB/Foto2.jpg)

Clique em **Alterar configurações**
![Alt text](Fotos-SMB/Foto3.jpg)

Depois em alterar, aparecerá uma tela menor, nela coloque o nome do computador e o domíno como está na imagem
![Alt text](Fotos-SMB/Foto4.jpg)

6º - Para criar os usuários e grupos, estando na maquina windows pesquise sobre active directory e abra

![Alt text](Fotos-SMB/Foto5.jpg)

6.1º - A criação e assim: Novo -> Usuário
![Alt text](Fotos-SMB/Foto6.jpg)

Insira as credenciais dele.
![Alt text](Fotos-SMB/Foto7.jpg)

senha..
![Alt text](Fotos-SMB/Foto8.jpg)

6.2 - Criação de grupos: Novo -> Grupos
![Alt text](Fotos-SMB/Foto9.jpg)

Insira o nome do grupo -> ok
![Alt text](Fotos-SMB/Foto10.jpg)

8º - Nessa imagem e possívei ver os grupos criados e seu usuários

![Alt text](Fotos-SMB/Foto11.jpg)

8.1 - Para adicionar usuário no grupo é assim: Seleciona o grupo -> vai na aba de mebros -> adicionar 

![Alt text](Fotos-SMB/Foto12.jpg)

9º - Nessa etapa vemos que cada pessoa está em seu respectivo grupo

![Alt text](Fotos-SMB/Foto13.jpg) ![Alt text](Fotos-SMB/Foto14.jpg) [Alt text](index.md)


## Teste

