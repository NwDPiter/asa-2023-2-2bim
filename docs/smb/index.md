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

[![Captura de tela de 2023-12-28 18-27-59](https://i.im.ge/2023/12/29/xxDG7D.Captura-de-tela-de-2023-12-28-18-27-59.png)](https://im.ge/i/xxDG7D)

Nesse imagem mostra a configuração do compartilhamento de pasta com o windows, foram criadas duas pastas [Carvalho] e [sales]

5º - Agora vamos nos conctar ao domínio que criamos pelo windows vá em:

[![PC-&amp;gt;propriedades](https://i.im.ge/2023/12/29/xxUqWG.PC-propriedades.jpg)](https://im.ge/i/xxUqWG)

Clique em **Alterar configurações**
[![alteração de config](https://i.im.ge/2023/12/29/xxU7ha.alteracao-de-config.jpg)](https://im.ge/i/xxU7ha)

Depois em alterar, aparecerá uma tela menor, nela coloque o nome do computador e o domíno como está na imagem
[![alterar e domínio](https://i.im.ge/2023/12/29/xxUaox.alterar-e-dominio.jpg)](https://im.ge/i/xxUaox)

6º - Para criar os usuários e grupos, estando na maquina windows pesquise sobre active directory e abra

[![ad](https://i.im.ge/2023/12/29/xxU6h8.ad.jpg)](https://im.ge/i/xxU6h8)

6.1º - A criação e assim: Novo -> Usuário
[![criação](https://i.im.ge/2023/12/29/xxUcXP.criacao.jpg)](https://im.ge/i/xxUcXP)
Insira as credenciais dele.

[![usuário teste](https://i.im.ge/2023/12/29/xxUYZp.usuario-teste.jpg)](https://im.ge/i/xxUYZp)

senha..

[![senha](https://i.im.ge/2023/12/29/xxU3wq.senha.jpg)](https://im.ge/i/xxU3wq)

6.2 - Criação de grupos: Novo -> Grupos

[![grupo](https://i.im.ge/2023/12/29/xxh2DM.grupo.jpg)](https://im.ge/i/xxh2DM)

Insira o nome do grupo -> ok

[![grupo-concluido](https://i.im.ge/2023/12/29/xxhOeh.grupo-concluido.jpg)](https://im.ge/i/xxhOeh)

8º - Nessa imagem e possívei ver os grupos criados e seu usuários

[![grupos](https://i.im.ge/2023/12/22/xuI2YC.grupos.jpg)](https://im.ge/i/xuI2YC)

8.1 - Para adicionar usuário no grupo é assim: Seleciona o grupo -> vai na aba de mebros -> adicionar 

[![add-grupo](https://i.im.ge/2023/12/29/xxitk4.add-grupo.jpg)](https://im.ge/i/xxitk4)

9º - Nessa etapa vemos que cada pessoa está em seu respectivo grupo

[![sales](https://i.im.ge/2023/12/22/xuI1U4.sales.jpg)](https://im.ge/i/xuI1U4)
[![carvalho](https://i.im.ge/2023/12/22/xuIOoD.carvalho.jpg)](https://im.ge/i/xuIOoD)


## Teste


[![arquivo](https://i.im.ge/2023/12/22/xuIuWY.arquivo.jpg)](https://im.ge/i/xuIuWY)
[![luciana](https://i.im.ge/2023/12/22/xuLqcz.luciana.jpg)](https://im.ge/i/xuLqcz)
[![saulo](https://i.im.ge/2023/12/22/xuLUSX.saulo.jpg)](https://im.ge/i/xuLUSX)