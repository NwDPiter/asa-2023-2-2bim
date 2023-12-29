# LDAP

## Instalação

- Samba-ad
- Krb5

## Configuração

1º - Vamos configurar o nome de nossa máquina com o nome de nosso dominio em: (/etc/hostname)

    berlin.alemanha.lab

2º - Agora configura a linha do local host em: (/etc/hosts)

    berlin.alemanha.lab

2.1 - Faça um backup do arquivo smb.conf que está em: (/etc/samba/smb.conf)

3º - Após isso vamos configura nosso domínio usando:

-   samba-tool domain provision --use-rfc2307 --interactive

4º - Despois de criar seu dominio vamos configurar o aquivo smb.conf que está em: (/etc/samba)

[![config ldap](https://i.im.ge/2023/12/29/xxkqVy.config-ldap.jpg)](https://im.ge/i/xxkqVy)

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

7º - Após criar usuário, vamo criar as OU

[![create-ou](https://i.im.ge/2023/12/29/xxpjfa.create-ou.jpg)](https://im.ge/i/xxpjfa)
[![ou=teste](https://i.im.ge/2023/12/29/xxp5SG.outeste.jpg)](https://im.ge/i/xxp5SG)
[![ou-criado](https://i.im.ge/2023/12/29/xxp9Nx.ou-criado.jpg)](https://im.ge/i/xxp9Nx)

8º Como podemos ver que foi criados duas OUS (vendedores e rh)

[![ous](https://i.im.ge/2023/12/29/xxvzB6.ous.jpg)](https://im.ge/i/xxvzB6)

8.1 Essa imagens mostram cada grupo e usuário em suas OUS

[![sobrenome2](https://i.im.ge/2023/12/29/xxnvFX.sobrenome2.jpg)](https://im.ge/i/xxnvFX)
[![sobrenome1](https://i.im.ge/2023/12/29/xxnJ98.sobrenome1.jpg)](https://im.ge/i/xxnJ98)

Incluir o(s) nome(s) e o conteúdo do(s) arquivo(s) de configuração.

- Criar duas OU: `vendedores` e `rh`;
- Mover o grupo `sobrenome1` e seus membros para a OU `vendedores`;
- Mover os grupo `sobrenome2` e seus membros para a OU `rh`.

## Teste

[![ou](https://i.im.ge/2023/12/22/xuDrQT.ou.jpg)](https://im.ge/i/xuDrQT)
[![carvalho](https://i.im.ge/2023/12/22/xuDX80.carvalho.jpg)](https://im.ge/i/xuDX80)
[![sales](https://i.im.ge/2023/12/22/xuDo5W.sales.jpg)](https://im.ge/i/xuDo5W)
