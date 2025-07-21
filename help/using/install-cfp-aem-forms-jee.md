---
title: Instalação de pacotes de correções cumulativos no AEM Forms JEE
description: Resumo das etapas para instalar e configurar o pacote de correções cumulativo (CFP) no AEM Forms JEE.
contentOwner: AK
exl-id: eed01a42-f4ab-4392-8b8e-eb5bbe2410a0
source-git-commit: 953752d32794cbc32fd6e9747928b809bfe68066
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 97%

---

# Instalação de Cumulative Fix Packs no AEM [!DNL &#x200B; Forms] JEE {#installing-cumulative-fix-packs-on-aem-forms-jee}

## Instalar o CFP no AEM 6.3 [!DNL Forms JEE] {#install-cfp-forms-6-3}

Para instalar o pacote de correções cumulativo no AEM 6.3 [!DNL Forms JEE], execute a seguinte sequência de etapas.

1. Para obter o instalador do AEM 6.3 [!DNL Forms JEE] para o CFP, entre em contato com o [suporte da Adobe](https://experienceleague.adobe.com/pt-br?support-solution=General&support-tab=home#support).
1. Execute o instalador do CFP e configure o AEM [!DNL Forms JEE] conforme descrito em [Instalar e configurar o AEM [!DNL Forms JEE]](#install-and-configure-aem-forms-jee).
1. Instale o AEM CFP 6.3.3.x mais recente.
1. Instale o pacote complementar do [!DNL Forms] para o AEM CFP [6.3.3.x](aem-forms-releases.md)

### Instalar pacote do AEM [!DNL Forms JEE]  {#install-aem-forms-jee-bundles-package}

O pacote do AEM [!DNL &#x200B; Forms JEE] (aemfd-jee-bundles-package-6.3CFP1; versão 1.0.2) fornece ao usuário do [!DNL Forms] no AEM [!DNL Forms JEE] os mesmos direitos e recursos encontrados no AEM [!DNL Forms OSGi]. Verifique os pacotes instalados no Gerenciador de pacotes e instale o pacote se ele ainda não estiver instalado.

### Instruções adicionais para o CQ-4208044 {#additional-instructions-for-cq}

Se estiver usando o servidor AEM 6.3 [!DNL Forms JEE] com banco de dados Oracle, defina as seguintes configurações após a implantação do CFP1, ou seja, após a execução do Gerenciador de configuração. Essa configuração é necessária para sincronizar usuários, grupos e membros de grupo quando a sincronização do domínio corporativo for executada.

1. Faça logon na interface do **administrador**.
1. Navegue até **[!UICONTROL Configurações]** > **[!UICONTROL Gerenciamento de usuários]** > **[!UICONTROL Configuração]** > **[!UICONTROL Importar e exportar arquivo de configuração]**
1. Exporte o arquivo config.xml.
1. Modifique a entrada “`groupMemberDBQueryBatchSize`” nas configurações do seu domínio em *config.xml*. Exemplo de entrada::

   &lt;entry key=&quot;groupMemberDBQueryBatchSize&quot; value=&quot;999&quot;/>

1. Importe o arquivo modificado e execute novamente a sincronização.

## Instalar o CFP no AEM 6.2 [!DNL &#x200B; Forms JEE] {#install-cfp-on-aem-62-forms-jee}

Para instalar o pacote de correções cumulativo no AEM 6.2 [!DNL Forms JEE], execute a seguinte sequência de etapas.

1. Para obter o instalador do AEM 6.2 [!DNL Forms JEE] para o CFP, entre em contato com o [suporte da Adobe](https://experienceleague.adobe.com/pt-br?support-solution=General&support-tab=home#support).
1. Execute o instalador do CFP e configure o AEM [!DNL Forms JEE] conforme descrito em [Instalar e configurar o AEM [!DNL Forms JEE]](install-cfp-aem-forms-jee.md#install-and-configure-aem-forms-jee).
1. Instale o AEM Hotfix 12785 versão 7.0.
1. Instale o AEM 6.2 Service Pack 1.
1. Instale o release-notes-aem-6-2-cumulative-fix-pack.md mais recente.
1. Instale o pacote complementar do [!DNL Forms] para o AEM 6.2 Service Pack 1 CFP.

### Instalar pacote do AEM [!DNL Forms JEE]  {#install-aem-forms-jee-bundles-package-1}

O pacote do AEM Forms JEE (aemfd-jee-bundles-package-6.2CFP5; versão 1.0.2) fornece ao usuário do [!DNL Forms] no AEM [!DNL Forms JEE] os mesmos direitos e recursos encontrados no AEM [!DNL Forms OSGi]. Verifique os pacotes instalados no Gerenciador de pacotes e instale o pacote se ele ainda não estiver instalado.

### Configuração de tempo limite para operações no nível do componente (NPR-16774) {#configuring-timeout-for-operations-at-component-level-npr}

>[!NOTE]
>
>Após o AEM 6.2 CFP4, é possível usar as seguintes instruções para configurar o tempo limite para operações de DSC, caso surjam problemas de tempo limite durante o processo de atualização.

A implantação do DSC leva um tempo variável, o que pode acarretar falha. Para alterar o tempo limite de operações de DSC, como Instalar, Carregar, Iniciar e Parar, você deve definir o `adobe.component.registry.timeout` usando o argumento JVM com a opção `-D`.

Especifique o valor da chave em segundos. Por exemplo: `-Dadobe.component.registry.timeout=300`

Também é possível alterar os tempos limite no nível do componente usando as três propriedades a seguir:

1. `adobe.all-component.timeout`: substitui os tempos limite de todos os serviços do produto.
1. `adobe.<serviceName>.timeout`: substitui o tempo limite somente para o serviço (&lt;serviceName>) mencionado na chave. Se o valor no nível de serviço for definido, o uso desse comando substituirá somente o valor do tempo limite do serviço especificado, caso ele seja definido no nível do Aplicativo.
1. `adobe.<serviceName>.<operationName>.timeout`: substitui somente o tempo limite da operação do serviço específico(&lt;serviceName>.&lt;operationName>) mencionado na chave. Se o valor for definido no nível da Operação, o uso desse comando substituirá somente o valor do tempo limite do serviço especificado, caso ele esteja definido no nível do Aplicativo ou do Serviço.

**Exemplos:**

Use os seguintes comandos para definir o tempo limite no nível do componente:

1. Para definir o tempo limite de todas as operações de serviço para 600 segundos:

   set “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.all-component.timeout=600`”

1. Para definir o tempo limite de valores de operação `DesigntimeService` para 500 segundos, use:

   set “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.timeout=500`”

1. Para definir o tempo limite de valores de operação `DesigntimeService's previewLCA` para 700 segundos, use:

   set “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.DesigntimeService.previewLCA.timeout=700`”

1. Para definir `DSC operations`, como carregar e instalar, para 600 segundos, use:

   set “`JAVA_OPTS=%JAVA_OPTS% -Dadobe.component.registry.timeout=600`”

## Instalar e configurar o AEM [!DNL Forms JEE] {#install-and-configure-aem-forms-jee}

1. Faça backup da pasta /deploy. Isso é necessário caso você decida desinstalar a correção rápida.
1. Interrompa o servidor de aplicativos.
1. Extraia o arquivo do instalador de correção para o disco rígido.
1. No diretório nomeado de acordo com o seu sistema operacional:

   **Windows**

   Navegue até o diretório na mídia de instalação ou a pasta onde você copiou o instalador.

   * (`Windows 32-bit`): `Disk1\InstData\Windows\VM`
   * (`Windows 64-bit`): `Disk1\InstData\Windows_64bit\VM`

   Em seguida, clique duas vezes no arquivo:

   * aemforms63_cfp_install.exe **(AEM [!DNL Forms] 6.3**)
   * aemforms62_cfp_install.exe **(AEM [!DNL Forms] 6.2**)
   * aemforms61_cfp_install.exe (**AEM [!DNL Forms] 6.1**)

   **Linux®, Solaris™, AIX®**

   Navegue até o diretório apropriado:

   * (Linux®): Disk1/InstData/Linux/NoVM
   * (Solaris™): Disk1/InstData/Solaris/NoVM
   * (AIX®): Disk1/InstData/AIX/VM

   Em um prompt de comando, digite:

   * ./aemforms63_cfp_install.bin (**AEM [!DNL Forms] 6.3**)
   * ./aemforms62_cfp_install.bin (**AEM [!DNL Forms] 6.2**)
   * ./aemforms61_cfp_install.bin (**AEM [!DNL Forms] 6.1**)

   O assistente de instalação é iniciado para fornecer orientação.

1. No painel de Introdução, clique em **[!UICONTROL Próximo]**.
1. Na tela Escolher pasta de instalação, verifique se o local padrão da instalação existente está correto. Ou clique em **[!UICONTROL Procurar]** para selecionar a pasta alternativa em que o AEM [!DNL Forms] está instalado e clique em **[!UICONTROL Próximo]**.
1. Leia as informações no Resumo de correção rápida e clique em **[!UICONTROL Próximo]**.
1. Leia as informações no Resumo de pré-instalação e clique em **[!UICONTROL Instalar]**.
1. Quando a instalação estiver concluída, clique em **[!UICONTROL Próximo]** para aplicar as atualizações de correção rápida aos arquivos instalados.
1. A caixa de seleção Iniciar gerenciador de configurações está selecionada por padrão. Clique em **[!UICONTROL Concluído]** para executar o Gerenciador de configurações.

   Para executar o Gerenciador de configurações posteriormente, desmarque a opção **[!UICONTROL Iniciar gerenciador de configurações]** antes de clicar em **[!UICONTROL Concluído]**. É possível iniciar o Gerenciador de configurações posteriormente usando o script apropriado no diretório *`[AEM_forms_root]`/configurationManager/bin*.

1. Dependendo do servidor de aplicativos, escolha um dos seguintes documentos e siga as instruções na seção *Configuração e implantação do AEM [!DNL Forms]*.

   Para o AEM [!DNL Forms] 6.3, consulte:

   * Instalação e implantação do AEM [!DNL Forms] para JBoss®
   * Instalação e implantação do AEM [!DNL Forms] para WebSphere®
   * Instalação e implantação do AEM [!DNL Forms] para WebLogic

1. Reinicie o servidor do AEM [!DNL Forms] JEE.
