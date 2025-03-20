# Inclusão/Exclusão de Usuários


- [ ] Google G Suite (<https://admin.google.com>)
  - Criar usuário (<https://admin.google.com/u/1/ac/users>)
  - Unidade organizacional = [Site Principal / Vek]
  - E-mail secundário = [E-mail pessoal]
  - Telefone = celular (formato internacional [+55 dd nnnnn-nnnn])
  - Gerar senha segura, anotar e passar para o usuário (<https://www.lastpass.com/pt/password-generator>)
  - [Não] Solicitar uma alteração de senha no próximo login
  - Adicionar no grupo [proj.cielovendas] [Vek Users]
- [ ] Amazon AWS/IAM (<http://console.aws.amazon.com>)
- [ ] Gerar Chaves Pública/Privada (Pode ser feito de 2 maneiras)
  - **Via console AWS:**
    - Rode os seguintes comandos em uma console Linux ou Git-bash:

      ```bash
      bash <(curl -s https://s3.amazonaws.com/downloads.vek.com.br/scripts/vek-ssh-keygen-aws.sh)
      ```

  - **Via console linux:**
    - [Documentação](https://gitlab.com/help/ssh/README#generating-a-new-ssh-key-pair)
    - Rode os seguintes comandos em uma console Linux ou Git-bash:

      ```bash
      bash <(curl -s https://s3.amazonaws.com/downloads.vek.com.br/scripts/vek-ssh-keygen-local.sh)
      ```

- [ ] Copiar as Chaves Pública/Privada para a *Home Directory* da máquina do usuário
  - Salve os arquivos .pem/.pub em algum diretório, abra uma console Linux ou Git-bash no mesmo diretório e rode os seguintes comandos:

    ```bash
    bash <(curl -s https://s3.amazonaws.com/downloads.vek.com.br/scripts/vek-ssh-keycopy.sh)
    ```

- [ ] Jumpcloud (<https://console.jumpcloud.com>)
  - Importar a Chave Pública do Certificado gerado (`${vek_login}.pub`)
- [ ] Amazon CloudWatch (<https://console.aws.amazon.com/cloudwatch/>)
- [ ] Microsoft Account (<https://account.microsoft.com> - <https://login.live.com>)
- [ ] Domínio vek.com.br: Microsoft Azure Domain (<https://portal.azure.com> - <https://portal.microsoft.com> - <https://www.office.com>) -> login win wks pro
- [ ] Portal Self Service (<https://login.vek.com.br/>)
- [ ] Portal VPN (<https://vpn-portal.vek.com.br/>)
- [ ] Domínio vek.com.br: Servidor de Gerenciamento (rdp://s005-swp-mgt001.vek.com.br) -> login srv mgt
- [ ] Domínio vek.local (rdp://007swinmgt001p.vek.com.br) -> vpn, check_mk/monitor
- [ ] Banco de Dados (portal-oracle, game-mysql, ecases-mysql)
- [ ] Servidor de Monitoramento (<https://stats.uptimerobot.com/oZvGAFXO31>)
- [ ] Uptime Robot (<https://uptimerobot.com>)
- [ ] Slack (<http://vek-servicos.slack.com>)
- [ ] Discord (<https://discord.com>)
  - **Convite colaborador Vek**
    - 1º baixar o aplicativo e instalar no site: https://discord.com/download
    - 2º entrar no grupo **Vek** com este convite <https://discord.gg/rjapdGBfmU>
    - 3º registrar o **NOME DE USUARIO** como "vek.login vek" **Ex: vek.andre.moraes**
    - 4º cadastrar e-mail da Vek @vectorinf.com.br e confirmar a validação
  - **Convidados Vek**
    - Entrar no grupo Vek com este convite <https://discord.gg/72wJsB8w4t>
- [ ] Servidor de VPN (<https://pfsense.vek.com.br>)
- [ ] Gitlab (<https://gitlab.com>)
  - Registrar no Gitlab usando a conta Google [login]@vectorinf.com.br (<https://gitlab.com/users/sign_in>)
  - Mudar o [username] para vek-[login] (<https://gitlab.com/-/profile/account>)
  - Adicionar a [Public SSH Key] (<https://gitlab.com/-/profile/keys>)
  - Criar um Token de Acesso [Link](https://gitlab.com/-/profile/personal_access_tokens?name=gitlab-repo&scopes=api,read_user,read_api,read_repository,write_repository,read_registry,write_registry)
    - 1°) Criar e salvar o token gerado no gitlab exemplo: w6Mz6SNvozw9kb8uK66E
    - 2°) Criar as variáveis de ambiente no Sistema Operacional e/ou Eclipse:
      - [gitlab_maven_repo=true | aws_maven_repo=true] -> escolha 1 dos repositórios, Gitlab ou AWS/S3
      - gitlab_access_id=Private-Token
      - gitlab_access_secret=aqui_token_gerado
    - 3°) Instalar o plug-in [Environment Variables Preferences Page] no Eclipse
    - 4°) Configurar as variáveis no Eclipse: Menu [Preferences / General / Environment Variables]
    - 5º) Importar o projeto e informar (digitar) o profile: [gitlab_maven_repo | aws_maven_repo] (caso ainda não tenha importado o projeto)
    - 6°) Selecionar o profile [gitlab_maven_repo | aws_maven_repo]: Menu [clique direito sobre o projeto / Maven / Select Maven Profiles]
    - **Windows**
      https://www.supertutoriais.com.br/pc/como-criar-variaveis-personalizadas-windows-10/
    - **Linux**
      https://www.todoespacoonline.com/w/2015/07/variaveis-de-ambiente-no-linux/
    - **Eclipse**
      https://www.ti-enxame.com/pt/java/variaveis-de-ambiente-no-eclipse/940245140/
  - *Adicionar* > git config --global user.name "Fulano de Tal"
  - *Adicionar* > git config --global user.email fulanodetal@vectorinf.com.br
  - *Adicionar* > vek-[login] para o grupo [vek-servicos] como [guest] (<https://gitlab.com/groups/vek-servicos/-/group_members>)
  - *Adicionar* > vek-[login] para o grupo [community] como [developer] (<https://gitlab.com/groups/vek-servicos/community/-/group_members>)
  - **Direitos Adicionais:**
    - Direitos adicionais deverão ser solicitados por e-mail por algum superior do usuário
    - Direitos adicionais deverão ser solicitados e concedidos por projeto GIT
    - Tipos de Direitos: Reporter, Developer, Maintainer
    - Documentação: (<https://docs.gitlab.com/ee/user/permissions.html>)
- [ ] Github (<https://github.com>)
- [ ] Docker (<https://www.docker.com> - <https://hub.docker.com>)
- [ ] Helm (<https://helm.sh> - <https://hub.helm.sh>)
- [ ] MongoDB Cloud (<https://cloud.mongodb.com>)
- [ ] Skeddly (<https://www.skeddly.com>)
- [ ] Jenkins (<https://jenkins.vek.com.br>)
- [ ] Elastic Cloud (<https://www.elastic.co>)
  - Admin Console (<https://cloud.elastic.co>)
  - Kibana Console (<https://logs.vek.com.br>)
    - [Criar usuário](https://b8980235e69e41aa86d38402b3133f08.us-east-1.aws.found.io/app/management/security/users)
    - [Dashboard](https://vek-servicos.kb.us-east-1.aws.found.io:9243/app/dashboards#/view/0acdd6d0-3d9b-11ec-bcd8-5f2b9510446f?_g=h@42b0d52)
- [ ] Jira (<https://jira.vek.com.br>)
- [ ] Portal Cielo Vendas
  - Homologação (<https://hml-www.cielo.vek.com.br>)
  - Produção (<https://www.cielo.vek.com.br>)
- [ ] Whatsapp Grupo Vek (<https://chat.whatsapp.com/DNW2LmfFrVN6wSqZClMR1D>)
- [ ] Convidar login@vectorinf.com.br para a _Daily Meeting_ no Calendário do Google
  - <https://meet.google.com/nom-oxbz-otq>
- [ ] Computador: Criar Usuário
  - **Windows:** wks-vek-admin@vectorinf.com.br
  - **Linux:** vek-w
  - [Instalar Apps Principais](http://boxstarter.org/package/anydesk.install,chocolateygui,choco-cleaner,wps-office-free,discord.install,googlechrome,microsoft-edge,k-litecodecpackfull,notepadplusplus.install,speedtest,bandizip,openvpn,git.install,WhatsApp)
    ***Anydesk** ***WPS Office** ***Discord** ***Chrome** ***Edge** ***K-Lite** ***NotePad++** ***Git** ***Bandizip** ***Openvpn** ***WhatsApp**
  - **OpenVPN**
    - [vpn-client_config](https://drive.google.com/file/d/1-86AEzJmwL0j9AAiURr3akULNCx0hxH_/view?usp=sharing)
    - [vpn-client_windows](https://drive.google.com/file/d/1-4zuMbzQsOgQH3MK0XSp7YNWNdJ1ALZM/view?usp=sharing)
  - **JumpCloud**
    - Chave: [45992f254fc744a8f1d316b68ec412d27865bb3f]
    - Windows

      ```powershell
      cd $env:temp | Invoke-Expression; Invoke-RestMethod -Method Get -URI <https://raw.githubusercontent.com/TheJumpCloud/support/master/scripts/windows/InstallWindowsAgent.ps1> -OutFile InstallWindowsAgent.ps1 | Invoke-Expression; ./InstallWindowsAgent.ps1 -JumpCloudConnectKey "45992f254fc744a8f1d316b68ec412d27865bb3f"
      ```

    - Mac

      ```bash
      curl -s <https://raw.githubusercontent.com/TheJumpCloud/support/master/scripts/macos/install_agent_and_serviceaccount.sh> -o $TMPDIR/install_agent_and_serviceaccount.sh && sudo bash $TMPDIR/install_agent_and_serviceaccount.sh -k 45992f254fc744a8f1d316b68ec412d27865bb3f && rm $TMPDIR/install_agent_and_serviceaccount.sh
      ```

    - Amazon Linux; Amazon Linux 2; CentOS 6, 7, 8; RHEL 6, 7, 8; Debian 9, 10; Ubuntu 16.04, 18.04, 19.04, 20.04, Linux Mint 19, 20 Cinnamon (64 bit)

      ```bash
      curl --tlsv1.2 --silent --show-error --header 'x-connect-key: 45992f254fc744a8f1d316b68ec412d27865bb3f' <https://kickstart.jumpcloud.com/Kickstart> | sudo bash
      ```

  - **Windows Update Remoto**
    - 1 - Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Bypass -Force; Set-ExecutionPolicy Bypass -Scope Process -Force; 
Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy ByPass -Force; Get-ExecutionPolicy -list;
    - 2 - [Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; Install-PackageProvider NuGet -Force; 
Set-PSRepository PSGallery -InstallationPolicy Trusted;
    - 3 - Install-Module -Name PSWindowsUpdate; Enable-WURemoting; Get-Command -Module PSWindowsUpdate;
    - 4 - Get-WindowsUpdate -AcceptAll -Install -IgnoreReboot -Verbose
  - **Chocolatey**
    - 1 - Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Bypass -Force; Set-ExecutionPolicy Bypass -Scope Process -Force; Set-ExecutionPolicy -Scope LocalMachine -ExecutionPolicy ByPass -Force; Get-ExecutionPolicy -list
    - 2 - [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
    - 3 - choco feature enable -n allowGlobalConfirmation
    - 4 - choco install anydesk.install, chocolateygui, choco-cleaner, wps-office-free, discord.install, googlechrome, microsoft-edge, k-litecodecpackfull, notepadplusplus.install, speedtest, bandizip, openvpn, git.install, WhatsApp --yes --ignore-checksums --no-progress
    
## Links

- [guide-mastering-markdown](https://guides.github.com/features/mastering-markdown/)
