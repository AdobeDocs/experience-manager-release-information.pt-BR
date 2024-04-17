---
title: AEM 6.3 Cumulative Fix Pack
description: Notas de versão do AEM 6.3 Cumulative Fix Pack.
exl-id: 04969587-a904-44cb-83e0-51707ac6a87f
source-git-commit: 426c19d12d87b22c86c49a0606465db162ef3434
workflow-type: tm+mt
source-wordcount: '17150'
ht-degree: 83%

---

# Notas de versão do AEM 6.3 Cumulative Fix Pack {#release-notes-aem-cumulative-fix-pack}

## Informações da versão {#release-information}

| **Produto** | Adobe Experience Manager |
|---|---|
| **Versão** | 6.3 |
| **Versão** | Cumulative Fix Pack 6.3.3.8 na [Distribuição de softwares](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq630/cumulativefixpack/aem-6.3.3-cfp-8.0.zip) |
| **Pré-requisitos** | [AEM 6.3 Service Pack 3 (6.3.3.0)](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR) |
| **Disponibilidade geral** | sexta-feira, 5 de março de 2020 |

### Cumulative Fix Pack {#cumulative-fix-pack}

A Adobe apresentou um modelo de entrega única para lançar correções. Em vez de lançar hot fixes para problemas individuais, a Adobe agora lança um Cumulative Fix Pack (CFP) mensalmente (sujeito à aprovação em verificações de qualidade). Um CFP é um pacote de conteúdo agregado com várias correções. Os CFPs incluem principalmente correções de erros, mas também podem incluir Pacotes de recursos. Eles têm as seguintes vantagens em relação às versões de hotfixes individuais:

* Natureza cumulativa (por exemplo, um CFP contém correções fornecidas por CFPs anteriores)
* Maior garantia de qualidade
* Instalação simplificada (o usuário instala um CFP como pacote único e sem dependências, exceto no caso do pacote de serviços mais recente)

Para obter mais informações sobre o CFP e outros tipos de versões, consulte [Definições de veículo de versão de manutenção.](https://experienceleague.adobe.com/docs/)

## Sobre a versão {#about-the-release}

O AEM Cumulative Fix Pack 6.3.3.8 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.8 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.20.

>[!CAUTION]
>
>Aplicar o CFP sem validar a compatibilidade entre os pacotes de recursos instalados pode resultar em falha do sistema ou perda de configurações personalizadas, o que pode exigir a restauração do backup para solucionar.

>[!NOTE]
>
>Para instâncias AEM com uma versão inferior a 6.3.3.0, o Adobe recomenda a implantação do SP/CFP por meio da pasta de instalação para clientes que têm muitos usuários na instância do AEM.

>[!NOTE]
>
>O MongoDB Enterprise 3.6 é compatível a partir da versão AEM 6.3.3.1.

## Lista de problemas {#changes}

Esta seção lista todos os problemas e hotfixes incluídos no CFP atual.

Além disso, esse CFP inclui hotfixes fornecidos em [cumulative fix packs anteriores](#previous).

### Ativos {#assets}

* A página Adicionar à coleção não mostra todas as coleções disponíveis na Exibição de cartão ao adicionar ativos à coleção (NPR-32537).

### Sites {#sites}

* Ao selecionar um Parsys e um componente dentro dele e usar o atalho de teclado para excluir itens selecionados, a ação exclui o componente e seu Parsys principal (NPR-32071).
* Quando as propriedades de uma página são salvas, um nó incorreto é criado (NPR-31774).

### Integrações {#integrations}

* ReportSuitesServlet está vulnerável a SSRF (NPR-32162).

### Campaign - Direcionamento {#campaign-targeting}

* O conteúdo de um componente alterado na instância do Autor e ativado não estará visível na instância de Publicação até que o componente seja reiniciado **com.day.cq.personalization.impl.TargetedContentManagerImpl** (NPR-32489 e NPR-32232).
* O desempenho do hub de contexto falha na publicação (NPR-31170).

### Brand Portal {#brand-portal}

* O Adobe Developer não está integrado ao Adobe Experience Manager 6.3 para Brand Portal (NPR-32056).

### Forms {#forms}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

#### Pacote complementar do Forms {#forms-add-on-package}

>[!NOTE]
>
>Os pacotes complementares do AEM Forms ajudam a alinhar a funcionalidade dos AEM Service Packs e dos Cumulative Fix Packs. Sendo assim, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Service Pack, Cumulative Fix Pack ou Feature Pack do AEM.

* Designer: se a opção de marcação estiver ativada, a borda do subformulário desaparecerá na saída de PDF gerada (NPR-32324 e NPR-32545).
* Designer: se houver células mescladas em uma tabela, o teste de acessibilidade falhará para o arquivo PDF de saída convertido de um formulário XDP usando o serviço de saída (NPR-32068).
* Segurança de documentos: um arquivo PDF protegido falha ao abrir offline com a opção `DisableGlobalOfflineSynchronizationData` definida como `True` (NPR-32080).

**Problemas corrigidos em 6.3.0-0047**

* (Somente JEE) Vulnerabilidades críticas de segurança (CVE-2021-44228 e CVE-2021-45046) relatadas para o Apache `Log4j2`.

## Correções e Feature Packs incluídos em Cumulative Fix Packs anteriores {#previous}

### Cumulative Fix Pack 6.3.3.7 {#cumulative-fix-pack-1}

O AEM Cumulative Fix Pack 6.3.3.7 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.7 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

### Ativos {#assets-1}

* Os ativos selecionados (na exibição em Coluna, na interface de toque) antes de marcar a opção de filtro na lista suspensa Somente conteúdo e, em seguida, selecionar a opção de movimentação também são movidos (NPR-30693).
* A variável `${extension}` não é renderizada na instância do autor no processamento do fluxo de trabalho (NPR-31694).
* O valor de expiração (tempo de funcionamento do cache do cliente) configurado para o modo Híbrido do Dynamic Media não é replicado no ambiente de entrega do Dynamic Media (NPR-31114).
* Os ativos são replicados para a instância Publicar a partir da instância Autor em execução na implantação do Dynamic Media - Scene7, mesmo após o uso dos filtros padrão (NPR-30856).

### Sites {#sites-1}

* Falha ao carregar as propriedades de uma página principal e uma exceção de ponteiro nulo é retornada. O problema é resolvido ao adicionar o `cq:blueprin`(NPR-30901).
* As configurações de implantação não são recuperadas corretamente do blueprintConfig no nó raiz. A desativação é acionada para blueprints e live copies. Acione somente a desativação para o blueprint (NPR-30866).
* Quando um usuário implanta uma página, a caixa de diálogo de configuração de implantação exibe caminhos de Live Copy duplicados (NPR-30438).
* Pronto para uso, o Editor de Rich Text scaffolding (RTE). aplica o tamanho da fonte incorporado a elementos, inesperadamente (NPR-31283, NPR-30922).
* Não é possível sincronizar a campanha no Adobe Campaign que contém o componente de importador de design pronto para uso (NPR-30890).
* O Editor de Rich Text (RTE) não permite inserir uma Tabela incorporada como um item de lista (NPR-30878).
* Quando um usuário foca nos campos do painel à esquerda e usa um atalho do teclado para colar o conteúdo, ele cola o conteúdo da área de transferência do editor de páginas em vez do conteúdo copiado dos campos do painel à esquerda (NPR-31173).
* Quando um usuário edita um fragmento de conteúdo, a variação já excluída do fragmento de conteúdo é restaurada (NPR-31272).
* O site do AEM não cria uma cópia de idioma (NPR-30690).
* As ações do Editor de páginas não têm os controles para implantar live copies (NPR-30613).

### Communities {#communities}

* Os títulos Atividades e Notificações são inconsistentes (NPR-30940).
* Os relatórios do Analytics não são preenchidos no ambiente de autor do AEM. Uma página em branco é exibida (NPR-30905).
* A paginação não funciona corretamente nos blogs do Communities (NPR-30827).

### Foundation {#foundation}

* As atualizações na configuração de tamanho do buffer do serviço HTTP baseado em Java não são salvas (NPR-30925).

### Forms {#forms-1}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-1}

>[!NOTE]
>
>Os pacotes complementares do AEM Forms ajudam a alinhar a funcionalidade dos AEM Service Packs e dos Cumulative Fix Packs. Sendo assim, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Service Pack, Cumulative Fix Pack ou Feature Pack do AEM.

#### Formulários adaptáveis {#adaptive-forms}

* Os valores flutuantes calculados usando um script não são exibidos corretamente em um formulário que faz parte de um conjunto de formulários (NPR-30802).

#### Formulários HTML5 {#html-forms}

* A geração da visualização HTML5 de um formulário XDP exibe uma oscilação ao adicionar instâncias de um subformulário (NPR-30908).

### Instalador do Forms JEE {#forms-jee-installer}

#### Serviços do Acrobat {#document-services}

* O OutputService exibe uma resposta incorreta após aplicar uma correção para solucionar problemas de HTML em PDF (NPR-31504).

#### Serviço PDFG {#pdfg-service}

* A contagem máxima de reutilização do console JMX não é exibida para o serviço HTML2PDF (NPR-30305).

#### Foundation JEE {#foundation-jee}

* A contagem máxima de reutilização do console JMX não é exibida para o serviço HTML2PDF (NPR-30136).

### Cumulative Fix Pack 6.3.3.6 {#cumulative-fix-pack-2}

O AEM Cumulative Fix Pack 6.3.3.6 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.6 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

### Ativos {#assets-2}

* A agregação de vídeo pelo Dynamic Video retorna somente os 100 itens principais no conjunto de resultados. NPR-30441; Hotfix do CQ-4213561
* Problema de conectividade de tag inteligente do Adobe por meio da alimentação de dados. NPR-30026: Hotfix do CQ-4269457
* Não é possível abrir a descompactação de um arquivo compactado com uma pasta que tenha um sinal de porcentagem (%) em seu nome usando a interface do Assets. NPR-29989: Hotfix do CQ-4270467
* O processamento de subativos de arquivos PDF grandes causa uma exceção OutOfMemoryError (OOME). NPR-29851: Hotfix do CQ-4269574

### Sites {#sites-2}

* Erro do ContextHub durante a integração do AEM e do Campaign. NPR-30624: Hotfix do CQ-4250790
* As propriedades de metadados &quot;onTime&quot; ou &quot;offTime&quot; salvas em ativos não são recuperadas se o servidor AEM for reiniciado. NPR-30412: Hotfix do CQ-4272784
* Ao gerar uma exportação de arquivos CSV, a adição de colunas personalizadas à exibição em lista interrompe o relatório. NPR-30208: Hotfix do CQ-4273344
* Os relatórios OOTB em /etc/reports/ não funcionam corretamente e o gráfico de dados históricos não é exibido. NPR-30016: Hotfix do CQ-4220180
* O valor do parâmetro de solicitação resourceType é copiado no valor de um atributo de tag HTML entre aspas duplas. NPR-29832: Hotfix do CQ-4255365

### Communities {#communities-1}

* Problema de conteúdo duplicado no console de moderação do AEM Communities. NPR-30667: Hotfix do CQ-4276829

### Tradução {#translation}

* Problema de tradução - somente alguns componentes são traduzidos pela tradução automática. NPR-30079: Hotfix do CQ-4273764
* Ao usar a estrutura de tradução, a adição de páginas a vários trabalhos de tradução aciona um erro. NPR-29746: Hotfix do CQ-4270953

### Forms {#forms-2}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-2}

>[!NOTE]
>
>Os pacotes complementares do AEM Forms ajudam a alinhar a funcionalidade dos AEM Service Packs e dos Cumulative Fix Packs. Sendo assim, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Service Pack, Cumulative Fix Pack ou Feature Pack do AEM.

#### Formulários HTML5 {#html-forms-1}

* Ao usar o NonVisual Desktop Access no modo Procurar para ler um formulário HTML5, o navegador Chrome lê &quot;gráfico&quot; antes de cada Gráfico de vetor escalonável (SVG) no design do formulário. NPR-30451: Hotfix do CQ-4274732

#### Forms - Integração de backend {#forms-backend-integration}

* Não é possível ver o serviço/fonte de dados da conexão de banco de dados ao criar o Modelo de Dados de Formulário (FDM). NPR-30108: Hotfix do CQ-4273359

### Instalador do Forms JEE {#forms-jee-installer-1}

#### Forms - Serviços da Acrobat {#forms-document-services}

* Quando um teste de carga é executado no serviço HTML para PDF, ele falha com um erro e as configurações de tipo de arquivo são removidas do AEM Forms Server. NPR-30111, NPR-30086: Hotfix do CQ-4271495

### Cumulative Fix Pack 6.3.3.5 {#cumulative-fix-pack-3}

O AEM Cumulative Fix Pack 6.3.3.5 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.5 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.17.

### Ativos {#assets-3}

* Atualização da interface DAM DMGateway para oferecer suporte a várias partes S3. NPR-29740: Hotfix do Q-4226303
* Não é possível excluir uma representação de imagem em um ativo de vídeo da página Detalhes do ativo. NPR-29417: Hotfix do CQ-4268675
* O proprietário não pode criar uma pasta privada dentro de uma pasta privada. NPR-29397: Hotfix do CQ-4229830
* O upload de um arquivo de arte do Adobe Illustrator com mais de 2 GB gera um erro de espaço de heap Java™. NPR-29265: Hotfix do CQ-4226217
* Os ativos ficam inutilizáveis depois que o serviço de tipo MIME do DAM CQ aplica texto para m3u8. NPR-29259: Hotfix do CQ-4264052
* A opção Criar não funciona ao tentar criar coleções no Edge. NPR-29248: Hotfix do CQ-4265699 e CQ-4265438
* O compartilhamento de link do ativo exibe cartões cinza em branco para alguns ativos na pasta. NPR-29831: Hotfix do CQ-4270187
* As novas tags adicionadas aos ativos não são salvas e desaparecem das propriedades. Hotfix do CQ-4271931, CQ-4270476

### Sites {#sites-3}

* O CoralUI, quando usado com Vários campos, armazena o fileReferenceParameter no nível do componente em vez do nível de vários campos. NPR-29535: Hotfix do CQ-4266129
* Problema ao tentar comparar a versão de página mais recente e atual no AEM 6.3.3.3. NPR-29532: Hotfix do CQ-4269639
* O campo de caminho é aberto no caminho raiz independentemente do caminho especificado na pesquisa. NPR-29398: Hotfix do CQ-4268897
* (Fragmentos de experiência) O FacebookApplication#setUpApp usa API obsoleta, que não funciona mais. NPR-29213: Hotfix do CQ-4266630
* Um alerta de erro é gerado ao adicionar componentes à página WCM quando a minificação está habilitada na instância. NPR-29476: Hotfix do CQ-4266197
* Propriedades vazias e várias propriedades não são propagadas do blueprint durante a implantação. Redefinir a Live Copy com o blueprint não funciona para componentes. NPR-29252: Hotfix do CQ-4264928, CQ-4264926, CQ-4267722
* Minimizar o Editor de Rich Text da tela cheia enquanto está no modo de edição de origem resulta em perda de conteúdo. NPR-28838: Hotfix do CQ-4260584

### Communities {#communities-2}

* Visitantes e membros sem privilégios de moderador podem ver publicações não aprovadas e pendentes colando o URL. NPR-29726: Hotfix do CQ-4271124
* Um alto tempo de resposta, de 40 a 50 segundos, é observado no logon do usuário na comunidade. NPR-29679: Hotfix do CQ-4269444
* Não é possível redefinir a senha quando conectado com um nome de usuário e email diferentes, pois a chave parece ser gerada com um nome de usuário e email trocados. NPR-29281: Hotfix do CQ-4268694

### Fragmentos de experiência {#experience-fragments}

* Não é possível exportar os Fragmentos de experiência para o destino quando a imagem inteligente é usada. Hotfix do CQ-4269606

### Replicação {#replication}

* O componente Agente de replicação é suscetível a uma vulnerabilidade que exibe informações confidenciais para usuários não autorizados. NPR-29613: Hotfix do Granite-25070
* Os dados fornecidos pelo usuário não são escapados na saída no componente `cq/replication/components/agent`, resultando em uma vulnerabilidade de script entre sites (XSS). NPR-29452: Hotfix do CQ-4266263

### Forms {#forms-3}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-3}

* Não há novas correções no pacote complementar do AEM Forms.

### Instalador do Forms JEE {#forms-jee-installer-2}

* Nenhuma nova correção no instalador do AEM Forms JEE.

### Pacotes OSGI e de conteúdo incluídos na 6.3.3.5 {#osgi-bundles-and-content-packages-included-in}

Lista de pacotes OSGi incluídos no AEM 6.3.3.5

[Obter arquivo](assets/do-not-localize/6_5-bundle-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.3.5

[Obter arquivo](assets/do-not-localize/content_packages6335.txt)

### Cumulative Fix Pack 6.3.3.4 {#cumulative-fix-pack-4}

O AEM Cumulative Fix Pack 6.3.3.4 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.4 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.16.
* Tempo limite do soquete e do tempo limite da conexão foram adicionados aos agentes de replicação do Brand Portal.

### Ativos {#assets-4}

* Se um arquivo for recarregado com o mesmo nome, as representações não serão geradas para os novos ativos processados. NPR-28643: Hotfix do CQ-4262286
* O CommandLineProcess do fluxo de trabalho falha ao ter um nome de arquivo com aspas simples. NPR-28805: Hotfix do CQ-4262287
* Os valores são diferentes entre a página de coleção e a página de coleção ao usar o filtro. NPR-28642: Hotfix do CQ-4261405
* CommitFailedException aciona com o upload de ativos de arquivamento zip grandes. NPR-28528: Hotfix do CQ-4260903
* Falha ao salvar metadados da pasta ao editar uma pasta que contém caracteres especiais. NPR-28211: Hotfix do CQ-4260401
* Não é possível excluir representações de imagem de um ativo de vídeo da página Detalhes do ativo. NPR-29149: Hotfix do CQ-4266073
* A entrega de vídeo de desktop do DMS7 usando o DMComponent usa o download progressivo para reproduzir vídeo no modo de publicação e não faz stream. NPR-28754: Hotfix do CQ-4263732
* Não é possível criar/editar predefinições de imagem, pois a restrição de acesso a /etc/dam/video/dynamicmedia desabilita recursos para Gerenciadores de imagem. NPR-28662: Hotfix do CQ-4263022
* O compartilhamento de links com arquivos de vídeo codificados no DMS7 resulta em pastas vazias. NPR-28851: Hotfix do CQ-4206743
* A replicação do AEM no Brand Portal fica paralisada por longos períodos. NPR-28913: Hotfix do CQ-4254932

### Communities {#communities-3}

* Não é possível abrir mensagens com anexos no Outlook enviados e na pasta da caixa de entrada. NPR-28559: Hotfix do CQ-4217072

### Sites {#sites-4}

* Criação de script entre sites (XSS) no SuggestionHandler para 6.3. NPR-28692: Hotfix do CQ-4253821
* A implantação profunda é concluída sem conter todas as ramificações na respectiva LiveCopy. NPR-29175: Hotfix do CQ-4239472
* (MSM) Implemente o LiveCopyIndex usando oak-index. NPR-29198: Hotfix do CQ-4222472
* O arquivo &quot;coral.js&quot; inclui uma versão vulnerável da biblioteca &quot;handlebars.js&quot;. NPR-26973: Hotfix do CQ-4255377
* Usar um componente do Target com um Contêiner de layout aninhado e um Componente de texto aciona um erro de JavaScript &quot;Não é possível ler a propriedade currentPos de nulo&quot; ao editar o texto ou clicar no contêiner. NPR-29077: Hotfix do CQ-4246594
* (Interface de toque) Não é possível atualizar tags em massa para páginas que já estão marcadas por tags diferentes. NPR-28729: Hotfix do CQ-4262922
* Abrir a variação na Visualização de cartão causa um erro 500. NPR-28611: Hotfix do CQ-4263571
* Implantação de uma estrutura que foi movida em um cliente potencial principal para um incorreto `cq:moveTarget`. NPR-28968: Hotfix do CQ-4265280

### Integração {#integration}

* (Configurações de Cloud Service) A caixa de seleção &quot;herdado de&quot; que aparece no nível raiz deve ser removida. NPR-28771: Hotfix do CQ-4259676
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra em um loop infinito e atualiza os nós em instâncias de publicação. NPR-28561: Hotfix do CQ-4263096
* Falha ao usar a credencial do Bright Edge com erro de conexão. NPR-29167: Hotfix do CQ-4265872
* Problema de compilação no OfferproxyTandtProvider.java devido à falta de instrução de importação para a classe &quot;Resource&quot;: declaração de importação ausente: importe org.apache.sling.api.resource.Resource. NPR-28772

### Commerce {#commerce}

* A opção Classificar não funciona para ativos dentro da coleção Comércio. NPR-28755: Hotfix do CQ-4213622

### Jetty {#jetty}

* Exceções de Java no error.log a cada redirecionamento 302 após a instalação do CFP2 sobre a 6.3.3. NPR-28606: Backport do CQ-4262844

### IU - Foundation {#ui-foundation}

* Clicar em uma tag remove o evento de mouse global e a caixa de diálogo fica congelada no &quot;modo arrastável&quot;. NPR-28641: Hotfix do CUI-7294

### WCM - MSM {#wcm-msm}

* A implantação do PushOnModify no PageManager move os compromissos várias vezes de duas sessões que causam uma condição de corrida. NPR-28880: Hotfix do CQ-4266191

### Vulnerabilidade {#vulnerability}

* A estrutura de proteção do CSRF não está funcionando com formulários fundamentais do AEM. NPR-28612: Hotfix do GRANITE-22231

### Forms {#forms-4}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

Os principais destaques do AEM Forms são:

* Habilitada a opção para selecionar itens por página na página Exibição do conjunto de políticas.
* A funcionalidade Compartilhar fila foi adicionada para todos os navegadores.

### Pacote complementar do Forms {#forms-add-on-package-4}

#### Forms - Fluxo de trabalho {#forms-workflow}

* A tarefa de resposta de fila compartilhada abre um elemento flash no espaço de trabalho do HTML5. NPR-29161: Hotfix do CQ-4266498
* Não é possível enviar do Espaço de trabalho se o botão contiver um caractere Umlaut. NPR-29014: Hotfix do CQ-4263172

#### Forms - Segurança de documentos {#forms-document-security}

* Habilite a opção para selecionar itens por página na página Exibição do conjunto de políticas. NPR-29243: Hotfix do CQ-4268567 e CQ-4265132

#### Forms - Serviços da Acrobat {#forms-document-services-1}

* O OSGi Forms Assembler não funciona em arquivos Acrobat. NPR-29049: Hotfix do CQ-4254426

#### Formulários HTML5 {#html-forms-2}

* Há um comportamento diferente ao visualizar um XDP como PDF em relação ao mesmo XDP como HTML no Designer. NPR-28602: Hotfix do CQ-4260239

### Instalador do Forms JEE {#forms-jee-installer-3}

* Nenhuma nova correção no instalador do AEM Forms JEE.

### Pacotes OSGI e de conteúdo incluídos na 6.3.3.4 {#osgi-bundles-and-content-packages-included-in-1}

Lista de pacotes OSGi incluídos no AEM 6.3.3.4

[Obter arquivo](assets/do-not-localize/list_of_osgi_bundlesincludedinaem633.4)

Lista de pacotes de conteúdo incluídos no AEM 6.3.3.4

[Obter arquivo](assets/do-not-localize/list_of_content_packagesincludedinaem633.4)

### Cumulative Fix Pack 6.3.3.3 {#cumulative-fix-pack-5}

O AEM Cumulative Fix Pack 6.3.3.3 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.3 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte as notas de versão do [AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.16.
* A paginação de lista de definição de política muda para limitar 50 registros por página.
* Adição de representante: armazenamento em cache nos nós ignoráveis no Ouvinte de sincronização de usuário do AEM Communities nas instâncias de publicação.
* Adição do aria-label à lista e ao botão de exibição de cartão.
* Um caractere de escape foi incluído na vírgula quando qualquer pesquisa é executada.
* Habilitado suporte de recursos sintéticos para a política de conteúdo.

#### Ativos {#assets-5}

* Não é possível baixar vários arquivos do tipo `.jp2`, `.max`, `.oft`, `.msg`. NPR-28002: Hotfix do CQ-4210856
* As configurações de publicação do ImageServer não são replicadas na entrega híbrida. NPR-28329: Hotfix do CQ-4253030

#### Communities {#communities-4}

* Navegação por teclado habilitada para componentes de habilitação do AEM Communities no Publish. NPR-27739: Hotfix do CQ-4253856
* Navegação por teclado habilitada para acionar a reprodução do conteúdo. NPR-27738: Hotfix do CQ-4254026
* Adição do aria-label à lista e ao botão de exibição de cartão. NPR-27736: Hotfix do CQ-4254027
* (Backport) Adição de representante: armazenamento em cache nos nós ignoráveis no Ouvinte de sincronização de usuário do AEM Communities nas instâncias de publicação. NPR-27841: Hotfix do CQ-4247234
* Os caracteres especiais recebem o caractere de escape (\) como prefixo na caixa de pesquisa no nível da interface. NPR-27839: Hotfix do CQ-4259757
* Erro ao pesquisar caracteres como `(` , `+` , `?` na pesquisa rápida. NPR-28212: Hotfix do CQ-4260969
* Não é possível excluir comentários no Conteúdo gerado pelo usuário usando a API. NPR-28075: Hotfix do CQ-4260534
* Os comentários postados na próxima página são destacados em amarelo quando um novo comentário é postado. NPR-28148: Hotfix do CQ-4259681
* Não é possível abrir mensagens com anexos nas pastas Enviados e Caixa de entrada do Outlook. NPR-28559: Hotfix do CQ-4217072

#### Sites {#sites-5}

* A execução da Limpeza de versão no AEM 6.3 causa um aviso repetido constantemente nos registros. NPR-27750; Hotfix do CQ-4206870
* O plug-in de estilo não é compatível com o modo de tela cheia do Editor de Rich Text. NPR-27622: Hotfix do CQ-4258674
* A lista &quot;loaderPromises&quot; não é apagada depois que o quadro de conteúdo é carregado no editor.js NPR-27768: Hotfix do CQ-4205337
* Não é possível definir a política de modelo em Parsys aninhados sem definir no componente principal. NPR-27987: Hotfix do CQ-4246095
* O navegador de componentes não está limpando a entrada do usuário e, portanto, pode gerar erros de JavaScript. NPR-27986: Hotfix do CQ-4247590
* A página aparece em branco quando o usuário tenta editar o fragmento de conteúdo. NPR-27669
* O destaque da anotação desaparece quando o usuário clica na anotação. BPR-27196: Hotfix do CQ-4254423

#### Integração {#integration-1}

* O ResourceResolver não soluciona vários domínios do componente do Target. NPR-28265: Hotfix do CQ-107847
* O cancelamento de herança da LiveCopy não funciona corretamente em contêineres direcionados, pois nenhuma ação é exibida. NPR-28129: Hotfix do CQ-4259813

#### Replicação {#replication-1}

* DispatcherFlushRules pode interromper a replicação na 6.3.3.1 NPR-28150: Hotfix do CQ-4261401

#### Campaign - Direcionamento {#campaign-targeting-1}

* NullPointerException em TargetedContentManager. Hotfix do CQ-4263485

#### Social - SCORM {#social-scorm}

* Remova a referência à Nuvem do modelo de referência de objeto do conteúdo compartilhável (SCORM) no reprodutor. Hotfix do CQ-4260779

#### DAM - Geral {#dam-general}

* O download por meio do email de compartilhamento de link retorna o zip vazio/corrompido. Hotfix do CQ-4259686

#### `MAC` - Integração do Test&amp;Target {#mac-test-target-integration}

* A opção Configurar o componente do Target não está disponível para os públicos-alvo, exceto para o público-alvo padrão. Hotfix do CQ-4261370

#### Tradução {#translation-1}

* Ativação do suporte para o serviço MS® Translator no AEM 6.3 após a atualização do MS® Translator para a API v3.0. NPR-28365: Hotfix do CQ-4259096

### Forms {#forms-5}

### Pacote complementar do Forms {#forms-add-on-package-5}

#### Forms - Fluxo de trabalho {#forms-workflow-1}

* Não é possível renderizar formulários PDF no espaço de trabalho HTML5. NPR-28059: Hotfix do CQ-4260373

#### Forms - Serviços da Acrobat {#forms-document-services-2}

* Não é possível visualizar Conjuntos de políticas além dos primeiros 1000 listados na exibição Conjuntos de políticas no Admin Console. NPR-28060, NPR-26047: Hotfix do CQ-4249865
* Uma exceção é lançada com o nome `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` impedindo a conclusão do processo de curta duração. NPR-28652

#### Forms - Formulários adaptáveis {#forms-adaptive-forms}

* Adicionar ou remover itens na lista suspensa não atualiza ao marcar os itens da caixa de seleção. NPR-28224: Hotfix do CQ-4252834

### Forms - Instalador JEE {#forms-jee-installer-4}

* Nenhuma nova correção no instalador do AEM Forms JEE.

### Pacotes OSGI e de conteúdo incluídos na 6.3.3.3 {#osgi-bundles-and-content-packages-included-in-2}

Lista de pacotes OSGi incluídos no AEM 6.3.3.3

[Obter arquivo](assets/do-not-localize/6333_bundle_list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.3.3

[Obter arquivo](assets/do-not-localize/content_package_list_6333.txt)

### Cumulative Fix Pack 6.3.3.2 {#cumulative-fix-pack-6}

O AEM Cumulative Fix Pack 6.3.3.2 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.2 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte Notas de versão do AEM 6.3 Service Pack 3.

Os principais destaques do AEM Cumulative Fix Pack são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.15.
* Adicionado suporte para a guia Regras e sua aplicação na Pasta ativos no Esquema de metadados de pasta.
* Ativação de suporte à paginação para a página de listagem de grupo na publicação.
* Permissão para a notificação unreadCount ser configurada com qualquer número. Valor padrão definido como 20.
* Correções no Linkchecker externo.

#### Assets {#assets-6}

* As listas suspensas dinâmicas não oferecem suporte à cascata. NPR-27044; Hotfix do CQ-4252564
* Consulta aprimorada para usar o recurso ExpiryNotification. NPR-26999: Hotfix do CQ-4251188
* Migração de regras do Esquema de metadados para o Esquema de metadados de pasta. NPR-27771: Backport do CQ-4257737, CQ-4257735, CQ-4259822
* O ajuste de referência do ativo falha ao atualizar referências de ativos que fazem parte do Sling ResourceCollections. NPR-26759: Hotfix do CQ-4252605
* O download por meio do email de compartilhamento de link retorna o arquivo zip vazio/corrompido. NPR-27997: Hotfix do CQ-4259686
* A codificação de vídeo híbrido não é concluída e nenhuma miniatura é criada. NPR-27122: Hotfix do CQ-4255080

#### Sites {#sites-6}

* Suspender página principal remove o tipo de mixagem cq:LiveRelationship da página ausente. NPR-26996: Hotfix do CQ-4254113
* (Linkchecker externo) Os links internos são exibidos como corrompidos em páginas individuais, mas não funcionam para links externos. NPR-27481: Hotfix do CQ-4257780
* A herança da configuração do Cloud Service é corrompida ao editar outras propriedades da página. NPR-27311: Hotfix do CQ-4256785
* Exceção de ponteiro nulo ao usar um formulário dos Componentes principais junto com um formulário do Foundation. NPR-27333: Hotfix do CQ-4249176
* O Editor de Rich Text remove a tag alt vazia. NPR-26938: Hotfix do CQ-4253267
* (Interface clássica) Problemas de desempenho com o ouvinte de alteração de seleção se houver vários menus suspensos. NPR-27115: Hotfix do CQ-4237215
* Quando o Editor de Rich Text é combinado com vários campos, ocorre o erro Uncaught TypeError: fieldAPI.getName não é uma função em foundation.js. NPR-27146: Hotfix do CQ-4253155/CQ-4259967
* O foco/cursor permanece no Editor de Rich Text mesmo ao clicar em um botão de opção no navegador Safari. NPR-27144: Hotfix do CQ-4249635
* A página aparece em branco quando o usuário tenta editar o fragmento de conteúdo. NPR-27669
* Não foi possível criar uma versão dos Fragmentos de experiência. NPR-27689: Hotfix do CQ-4259009

#### Integração {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever percorre toda a árvore para coletar as marcas disponíveis. NPR-27060: Hotfix do CQ-4255790
* A variável `cq:actions` não são considerados para um componente direcionado. NPR-27616: Hotfix do CQ-4257497

#### Sling {#sling}

* Quando data-sly-use é usado em classes com um nome idêntico, o código não compatível é produzido. NPR-27282: Hotfix do Sling-7581

#### Commerce {#commerce-1}

* Atualização para Apache Felix Http Jetty 4.0.6. NPR-26472: Hotfix do Granite-22916

#### DAM - Cliente DM {#dam-dm-client}

* Uma imagem não é exibida após especificar pontos de interrupção no componente do Dynamic Media. Hotfix do CQ-4256168

#### DAM - DMServices {#dam-dmservices}

* MixedMediaSet com vídeo relacionado não é sincronizado corretamente. Hotfix do CQ-4251650
* O vídeo não é reproduzido no editor de Predefinição do visualizador do Conjunto de mídias mistas. Hotfix do CQ-4251442

#### DAM - Geral {#dam-general-1}

* O link para o modelo de Fragmento de conteúdo está ausente após a aplicação da correção SP3. Hotfix do CQ-4259029

#### DAM - IU {#dam-ui}

* A interface do esquema de metadados de pasta é corrompida após a instalação do SP3. Hotfix do CQ-4257737

#### Communities {#communities-5}

* Adicionado suporte de paginação para a listagem de grupos na publicação. NPR-26953: Hotfix do CQ-4246525
* A notificação de contagem não lida não pode ser definida para além de 21. NPR-27496: Hotfix do CQ-4252829
* O número de assinaturas do usuário é limitado a 1.000. NPR-27615: Hotfix do CQ-4254689
* Erro observado ao fazer upload de um anexo diferente da imagem (por exemplo, .pdf) no Fórum. NPR-27375: Hotfix do CQ-4257753
* O link para respostas não está funcionando ao clicar na linha. NPR-24556: Hotfix do CQ-4256138
* As relações com o UGC não são excluídas após a exclusão do UGC. NPR-27631: Hotfix do CQ-4258706
* Não é possível pesquisar pelo valor de endereço na Pesquisa por palavra-chave se a comunidade estiver definida com o Provedor de recursos de armazenamento do banco de dados (DSRP). NPR-27652: Hotfix do CQ-4253261
* Clicar no ícone de lixeira na imagem após a confirmação de exclusão remove o anexo permanentemente. NPR-27340: Hotfix do CQ-4255150
* As publicações e respostas do fórum são adicionadas à parte superior da segunda página e, quando atualizada, a publicação é movida para o local correto na parte superior da primeira página. NPR-27341: Hotfix do CQ-4247338
* O rótulo de status de conclusão do recurso de habilitação do Scorm aparece vazio na interface. NPR-27152: Hotfix do CQ-4249994
* Ao habilitar &#39;Permitir privilegiados&#39;, os membros com privilégios só devem poder compor para usuários que sejam membros da comunidade. NPR-27901: Hotfix do CQ-4251235

#### Sustentação {#sustenance}

* Os registros de atividade do Gerenciador de pacotes devem ser extraídos em um arquivo de registro separado. NPR-27323: Hotfix do Granite-14866

#### Tradução {#translation-2}

* A pré-visualização de tradução não funciona com o conteúdo de amostra we.retail. NPR-27170: Hotfix do CQ-4241179

* Correções proativas no platform.login. NPR-26961
* Salvar e fechar nas propriedades da página não retorna à página adequada na GUERRA contra o AEM com Tomcat. NPR-27567: Hotfix do Granite-23671

* O texto inserido é perdido pelo recurso sourceEdit depois de salvo. Hotfix do CQ-4259273

### Forms {#forms-6}

### Pacote complementar do Forms {#forms-add-on-package-6}

#### Forms - Segurança de documentos {#forms-document-security-1}

* Problema de simultaneidade com o SDK do cliente JEE. NPR-27572: Hotfix do CQ-4247156

#### Forms - Serviços da Acrobat {#forms-document-services-3}

* A criação de um modelo de dados de formulário com base em SOAP falha no WebSphere®. NPR-27692: Hotfix do CQ-4253702

#### Forms - Formulários adaptáveis {#forms-adaptive-forms-1}

* Vulnerabilidade de injeção XML com o AEM Forms. NPR-27863: Hotfix do CQ-4257315
* O Componente de container do AEM Forms fica invisível assim que o formulário errado é configurado na página de sites e a caixa de seleção &quot;formulários cobrem a largura total da página&quot; é selecionada. NPR-25972: Hotfix do CQ-4239287, CQ-4249133

### Instalador do Forms JEE {#forms-jee-installer-5}

#### Foundation JEE {#foundation-jee-1}

* A criação de um modelo de dados de formulário com base em SOAP falha no WebSphere®. NPR-27692: Hotfix do CQ-4253702

#### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included}

Lista de pacotes OSGi incluídos no AEM 6.3.3.2

[Obter arquivo](assets/do-not-localize/63332bundle_list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.3.2

[Obter arquivo](assets/do-not-localize/6332content_package.txt)

### Cumulative Fix Pack 6.3.3.1 {#cumulative-fix-pack-7}

O AEM Cumulative Fix Pack 6.3.3.1 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 3 (6.3.3.0), em setembro de 2018.

O AEM Cumulative Fix Pack 6.3.3.1 depende do AEM 6.3 Service Pack 3. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.3.x após instalar o AEM 6.3 Service Pack 3. Para obter instruções de instalação, consulte [Notas de versão do AEM 6.3 Service Pack 3](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.14.
* Melhorias de desempenho em predicados e pesquisa.
* Correção de um problema no tratamento do FormData para o valor padrão.
* FormBuilder atualizado para a versão mais recente do Handlebars.
* Adição do servlet de configuração para a configuração de edição do RTE no modo de caixa de diálogo.
* Adicionado suporte para campos compostos.
* Itens da barra de ferramentas ativados/desativados do Editor de Rich Text com uma política de conteúdo para a caixa de diálogo de edição.

#### Ativos {#assets-7}

* Com a dissociação de IDS ativada, o fluxo de trabalho Atualização de ativo do DAM não vincula mais referências. NPR-26135: Hotfix do CQ-4250933
* Não é possível abrir a descompactação de um arquivo criado pela etapa do desarquivador com uma pasta que tenha um % no nome. NPR-26275: Hotfix do CQ-4251482
* O caractere de aspas simples impede a atualização de metadados. NPR-26808: Hotfix do CQ-4254305
* (Omnisearch) Problema de desempenho ao pesquisar em uma coleção. NPR-26714: Hotfix do CQ-4253408
* O uso do GQLConverter com uma pesquisa de texto completo contendo as letras &quot;OR&quot; no texto é processado incorretamente. NPR-26564: Hotfix do CQ-4247362
* O compartilhamento do link do ativo de vários locatários pré-configura a ID do locatário, o que forma um URL inválido. NPR-26482: Hotfix do CQ-4253540
* Desative &quot;Caminho da pasta raiz da empresa&quot; na interface de configuração do Dynamic Media Cloud. NPR-26361: Hotfix do CQ-4249505
* A assimilação de arquivos .mos RAW é prolongada. NPR-26296: Hotfix do CQ-4250661
* O Compartilhamento de link de ativo não permite adicionar mais de um usuário interno com ID de usuário numérico. NPR-26206: Hotfix do CQ-4251466
* Corrupção em arquivos zip compactados com o algoritmo deflate64. NPR-26793: Hotfix do CQ-4253995
* O processo de geração de miniaturas não funciona corretamente em arquivos PDF complexos, resultando em miniaturas, em que parte da imagem está ausente. NPR-26057: Hotfix do CQ-4250944
* Problema de utilização da memória heap com a geração de miniaturas. NPR-25545: Hotfix do CQ-4246960
* A criação de muitas relações em um ativo causa um erro. NPR-26309: Hotfix do CQ-4250708
* A opção &quot;Excluir representação&quot; não funciona e emite um erro &quot;nada para excluir&quot;. NPR-26007: Hotfix do CQ-4213414
* Não é possível excluir valores padrão para campos com vários valores. NPR-25116: Hotfix do CQ-4247856
* (DM Hybrid) A replicação de catálogo falha no AEM 6.3.2 com Dynamic Media. NPR-26406: Hotfix do CQ-4251306

#### Sites {#sites-7}

* Correções proativas de Backport do Sites. NPR-26963
* As tags são criadas duas vezes quando há uma diferença no tipo de letras maiúsculas e minúsculas do Título e do Nome. NPR-26877: Hotfix do CQ-4254134
* Os recursos do Editor de Rich Text na caixa de diálogo de edição não são controlados por políticas. NPR-27059, NPR-26750: Hotfix do CQ-4241130
* Perguntas sobre o armazenamento em cache segment.js do Client Context vs o não armazenamento em cache. NPR-26622: Hotfix do CQ-4253486
* A ativação da Regra de segmentos (/etc/segmentação) de regras secundárias no clássico faz com que a publicação fique inativa. NPR-26601: Hotfix do CQ-4253588
* A adição de &quot;caractere especial&quot; rola a caixa de diálogo Editor de Rich Text para cima. NPR-26435: Hotfix do CQ-4249869
* (Interface para toque) A barra de ferramentas fica inutilizável com vários Editores de Rich Text ao alternar de tela cheia para a caixa de diálogo flutuante. NPR-25652: Hotfix do CQ-4206008
* Promover uma inicialização de várias páginas cria várias versões para cada página. NPR-26810: Hotfix do CQ-4254663
* As operações de movimentação de tags não são refletidas pelos campos de tag do modelo de fragmento de conteúdo estruturado. NPR-26801: Hotfix do CQ-4251805
* (Interface de toque) O cancelamento da publicação da página secundária no editor de página não funciona após renomear a página no blueprint. NPR-26774: Hotfix do CQ-4254175
* A página não publicada não está funcionando com referências. NPR-26749: Hotfix do CQ-4254372
* Criar a variação como Live Copy requer que o usuário atualize a página para refletir. NPR-26663: Hotfix do CQ-4254328
* (Interface clássica) Ao voltar às propriedades da página, a imagem em miniatura não usa mais a herança e desaparece do administrador e do sidekick do site, e a imagem é exibida em branco. NPR-26562: Hotfix do CQ-4252346
* Quando uma versão de uma página é criada e uma comparação é acionada, os nós de /content/versionshistory são listados na lista de live copies para o Blueprint. NPR-26506: Hotfix do CQ-4243957
* Os URLs no Editor administrativo do Fragmento de experiência não permitem sobreposições. NPR-26318: Hotfix do CQ-4252156

#### Plataforma {#platform}

* Fuga de sessão em ReplicationEventListener com eventos teste. NPR-25937: Hotfix do CQ-4251090
* A replicação usa o token expirado do OAuth, causando vários erros. NPR-25894: Hotfix do GRANITE-22388

#### Integração {#integration-3}

* Incorporação do TSDK com interrupções do AEM e uma atualização para o Handlebars 4 devido ao uso de modelos incompatíveis. NPR-26699: Hotfix do CQ-4248974
* A publicação de uma página com um novo ativo desativa a página secundária da instância de publicação sem notificação. NPR-24869: Hotfix do CQ-4247832
* A replicação usa um token expirado para oauth. NPR-25984: Hotfix do Granite-22388

#### Replicação {#replication-2}

* O transporte HTTP pode vazar sessões abertas. Hotfix do Granite-17434
* Exceções em logs enquanto o nó do token de acesso é acessado simultaneamente por mais de um agente de replicação. NPR-26964: Hotfix do GRANITE-23276, Granite-23155

#### ContextHub {#contexthub}

* O arquivo &quot;coral.js&quot; inclui uma versão vulnerável da biblioteca &quot;handlebars.js&quot;. Hotfix do CQ-4255377

#### DAM - Cliente DM {#dam-dm-client-1}

* Excluir uma cópia de um ativo de imagem torna o ativo original inutilizável. Hotfix do CQ-4251648
* Download redundante de conteúdo de imagem extra de servidores S7. Hotfix do CQ-4248770

#### Granite {#granite}

* O Provedor AEM OAuth não realiza a pesquisa que não diferencia maiúsculas de minúsculas. NPR-26133: Hotfix do GRANITE-22650
* O Validador de pacotes não valida pacotes incluídos no CFP/SP. NPR-26775: Hotfix do Granite-22825

#### Communities {#communities-6}

* Problema do delimitador com resultados de pesquisa. NPR-27051: Hotfix do CQ-4248939
* Altere o valor suspenso de Dallas para Virginia no Provedor de recurso de armazenamento da Adobe. NPR-26936: Hotfix do CQ-4254434
* Ativação do suporte para pesquisa de título localizada no SocialTagManager. NPR-26932: Hotfix do CQ-4250276
* As imagens do anexo não mostram a miniatura ao criar uma publicação no fórum. NPR-26380: Hotfix do CQ-4253105
* A opção de Colar a partir de plug-ins do Word não carrega mais de uma imagem. NPR-26728: Hotfix do CQ-4253638
* Não é possível filtrar o conteúdo na página de moderação. NPR-26697: Hotfix do CQ-4213766
* (Vulnerabilidade de segurança) Tomada de conta devido a uma configuração incorreta do JWT. NPR-26440: Hotfix do CQ-4253314
* A recuperação de dados do Provedor de recurso de armazenamento da Adobe é lenta. NPR-26237: Hotfix do NPR-24152
* A página de composição de mensagem privada se comporta de forma irregular e lenta. NPR-26120: Hotfix do CQ-4250923
* A notificação &quot;Marcar tudo como lido&quot; renderiza apenas as primeiras 10 como não lidas sem a atualização da página. NPR-27036: Hotfix do CQ-4254058
* Clique de paginação da seção Comentários do Communities e comportamento do carregamento de página. NPR-27030: Hotfix do CQ-4251228
* (Pesquisa no fórum) O botão Voltar ignora a página e transfere de volta para o forum.html. NPR-26949: Hotfix do CQ-4254804
* As notificações não lidas não aumenta mais de 21. NPR-26947: Hotfix do CQ-4251251
* (Trabalho SearchScheduledPosts) Adicione o switch ativar/desativar no ConfigMgr. NPR-26924: Hotfix do CQ-4250463
* O caminho Tomcat Context(/aempublish) é suspenso ao rolar na página Atribuições. NPR-26919: Hotfix do CQ-4254345
* NullPointerException ao criar um grupo e membro. NPR-26778: Hotfix do CQ-4248095
* O conteúdo não destacado e desvinculado do moderador não funciona com o Princípio de responsabilidade única (SRP) do MySQL. NPR-26767: Hotfix do CQ-4251520
* Problemas de funcionalidade de pesquisa com determinados caracteres. NPR-26726: Hotfix do CQ-4247744
* Habilite os deep links para a interface de moderação e recursos de ativação. NPR-26705: Hotfix do CQ-4251381
* Problema de pesquisa no componente do fórum. NPR-26577: Hotfix do CQ-4251303
* A pesquisa com o nome e sobrenome juntos nas mensagens das comunidades não retorna os resultados esperados. NPR-26377: Hotfix do CQ-4253150
* A paginação não é atualizada ao remover respostas. NPR-26327
* A exclusão da publicação funciona, mas gera um erro no console e a publicação permanece visível na interface. NPR-26292: Hotfix do CQ-4252803
* A paginação não é atualizada dinamicamente e a lista de respostas continua aumentando. NPR-26145: Hotfix do CQ-4251586
* As configurações de grupo não são carregadas em um grupo que contém de 50 a 100 mil usuários. NPR-25642: Hotfix do CQ-4238426
* Falha do reprodutor do Recurso de catálogo em caminhos de contexto. NPR-25640: Hotfix do CQ-4238426
* (Pesquisa no fórum) - Os links paginados de threads com muitas postagens não funcionam nas notificações. Hotfix do CQ-4254202
* O console de moderação exibe apenas 5 entradas com o Firefox. Hotfix do CQ-4254128
* Os grupos não ficam visíveis ao criar um site. NPR-27148: Hotfix do CQ-4251788
* Exceção de ponteiro nulo ao adicionar grupos e membros às Configurações de função e permitir o membro privilegiado na função do blog. NPR-21732, NPR-27176: Hotfix do CQ-4255909
* A edição do site e a adição de membros nas configurações de função aciona uma exceção de ponteiro nulo. NPR-27132: Hotfix do CQ-4255909

#### Interface do usuário {#user-interface}

* Correções proativas de logon da plataforma. NPR-26961
* (Multicampo) Permite que itens compostos tenham nomes personalizados. NPR-26493: Hotfix do Granite-20568
* A exibição de coluna não é atualizada após colar uma página, até que seja atualizada. NPR-26030: Hotfix do CQ-4236346
* Correções proativas do granite.ui.commons. NPR-26960
* Correções proativas do granite.ui.content. NPR-26959
* Correções proativas de log de experiência/CQ. NPR-26943
* Backports proativos da interface do Foundation. NPR-26942
* (IE11) &quot;NaN&quot; é exibido no campo de número ao digitar um valor negativo. NPR-26701: Hotfix do CQ-100826
* (Coral. Multifield) Campos aninhados usam o modelo errado para criar os itens. NPR-25649: Hotfix do CUI-6743
* Atualize os clientlibs granite coralui2 e coralui3 para remover Handlebars da build. NPR-25606: Hotfix do Granite-22116

### Forms {#forms-7}

### Pacote complementar do Forms {#forms-add-on-package-7}

#### Forms - Segurança de documentos {#forms-document-security-2}

* Exceções de substituição de chave principal nos logs do servidor para chaves in-active. NPR-26748: Hotfix do CQ-4253705
* Não é possível criar ou modificar as configurações de marca d&#39;água da Segurança de documentos. NPR-26267, NPR-26129: Hotfix do CQ-4250234

#### Forms - Serviços da Acrobat {#forms-document-services-4}

* A validação do PDF/A não exibe como válida com &quot;validar PDF/A&quot;. NPR-25934: Hotfix do CQ-4248558

#### Forms - Comunicação interativa {#forms-interactive-communication}

* A Visualização de PDF e HTML da Carta é visível e funcional na mesma janela quando um módulo editável é editado, salvo, e a Visualização de PDF é aberta/fechada. NPR-26770: Hotfix do CQ-4253217

#### Forms - Fluxo de trabalho {#forms-workflow-2}

* O Espaço de trabalho trava intermitentemente e mostra os pontos iniciais repetidamente. NPR-26461: Hotfix do CQ-4253439
* A exceção ESAPI é lançada nos logs quando chaves são usadas no nome da tarefa. Hotfix do CQ-4256627
* A exceção de ponteiro nulo é acionada quando o ponto inicial associado do formulário/conjunto de formulários adaptável não pré-preenchido é aberto. Hotfix do CQ-4256124
* Não é possível enviar email usando a configuração global. NPR-26163: Hotfix do CQ-111110
* Não é possível abrir o espaço de trabalho após aplicar o arquivo axis.jar. NPR-26131: Hotfix do CQ-4251126
* O botão de atualização não sincroniza os dados mais recentes do servidor com os formulários adaptáveis. Hotfix do CQ-4255670
* A configuração do modelo de pesquisa na interface do administrador e a utilização do mesmo para pesquisar a tarefa no espaço de trabalho do AEM Forms aciona uma exceção. Hotfix do CQ-4255649
* Os detalhes de rastreamento dos processos nos aplicativos com o símbolo de parênteses no nome não são exibidos no espaço de trabalho HTML. Hotfix do CQ-4242101
* Salvar alterações na tela de preferências do espaço de trabalho HTML aciona uma exceção. Hotfix do CQ-4241485
* A aprovação em massa é interrompida na configuração mais recente do JEE. Hotfix do CQ-4241486
* O rascunho da tarefa/ponto inicial falha no servidor JEE 6.4 mais recente. Hotfix do CQ-4241484
* Defina o parâmetro Date().getTime().toString para inicializar a sessão em vez de Date.toString(). Hotfix do CQ-4241483
* Ao abrir /lc/ws, uma exceção de caractere vulnerável é observada no parâmetro HTML. Hotfix do CQ-4241481

#### Vulnerabilidade {#vulnerability-1}

* Vulnerabilidade da Criação de script entre sites (XSS) armazenada na guia Observações do Gerenciador de formulários. NPR-27157: Hotfix do CQ-4255556

### Instalador do Forms JEE {#forms-jee-installer-6}

#### Foundation JEE {#foundation-jee-2}

* Análise de código da API de segurança corporativa. Hotfix do CQ-4255638
* Falha ao carregar esapi.properties como recurso classloader no WAS9. Hotfix do CQ-4255631
* Clicar em Adicionar autenticação durante a Configuração do domínio gera um erro. Hotfix do CQ-4255634
* O Forms JEE é compatível com autenticação mútua PKCS#11. NPR-21372
* Correção de problemas relatados na análise de código estático do Core. Hotfix do CQ-104446
* A implantação do adobe.livecycle.weblogic.ear e adobe.livecycle.websphere.ear falha ao executar o LCM. Hotfix do CQ-4255629, CQ-4255630
* Mensagens de erro inválidas no Gerenciamento de aplicativos. NPR-23289: Hotfix do CQ-4233163, CQ-4255636
* Clicar em Adicionar autenticação durante a Configuração do domínio resulta em um erro. Hotfix do CQ-4255634

#### Forms - Conector JEE {#forms-jee-connector}

* Correção de problemas relatados na análise de código estático do conector. NPR-22260

#### Serviço PDFG {#pdfg-service-1}

* Erro org.jgroups.Message nos logs após a atualização do LiveCycle para o AEM 6.2 Forms. NPR-26795: Hotfix do CQ-4220415
* AEM Forms - Erro ao migrar estilos. Hotfix do CQ-4251969
* Correção de problemas relatados no relatório de análise de código estático do PDFG. NPR-23251: Hotfix do CQ-4213930

#### Pacotes OSGI e de conteúdo incluídos na 6.3.3.1 {#osgi-bundles-and-content-packages-included-in-3}

Lista de pacotes OSGi incluídos no AEM 6.3.3.1

[Obter arquivo](assets/do-not-localize/63sp3cfp1bundlelist.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.3.1

### Cumulative Fix Pack 6.3.2.2 {#cumulative-fix-pack-8}

O AEM Cumulative Fix Pack 6.3.2.2 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 2 (6.3.2.0), em abril de 2018.

O AEM Cumulative Fix Pack 6.3.2.2 depende do AEM 6.3 Service Pack 2. Portanto, você deve instalar o pacote AEM Cumulative Fix Pack 6.3.2.x após instalar o AEM 6.3 Service Pack 2. Para obter instruções de instalação, consulte [Notas de versão do AEM 6.3 Service Pack 2](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.11.
* Subativos e visualizador de ativos de várias páginas habilitados no Brand Portal.
* O comprimento do tipo de campo foi alterado para 255 para suportar todos os tipos MIME possíveis dos diferentes tipos de anexos.
* Configuração da mensagem de erro do servidor quando uma imagem viola os critérios de upload.
* Inclusão de suporte STARTTLS no Day CQ Mail Service.
* Atualização para as versões mais recentes de cq-wcm-content e com.adobe.cq.launches.it.serverside.
* Atualização do com.adobe.granite.ui.coralui3-rte para a versão mais recente lançada.
* A condição de renderização garantida retorna um resultado seguro se expressionResolver for nulo.
* Coral.ColumnView: adição de suporte para shift+click.

### Ativos {#assets-8}

* O campo Grupo de usuários fechado da pasta de ativos (CUG) não retorna o grupo &quot;todos&quot;. NPR-23163: Hotfix do CQ-4239377
* A pesquisa por pesquisas salvas de coleção inteligente não retorna todos os resultados. NPR-23243: Hotfix do CQ-4240355
* (ExpiryNotificationJobImpl) Otimização da consulta existente. NPR-23330: Hotfix do CQ-4205249
* (Perfil de metadados) Valores de tag padrão definidos no momento de criação não estão disponíveis após salvar. NPR-23370: Hotfix do CQ-4235458
* (Interface de toque) Não é possível mover vários ativos devido ao erro JS. NPR-23395: Hotfix do CQ-4241279
* A incompatibilidade no tamanho do download versus as informações exibidas está incorreta, gerando confusão para os usuários. NPR-23418: Hotfix do CQ-4242774
* O tipo mime extraído para a extensão de arquivo LSR e SKETCH está incorreto e resulta em download de arquivo inválido. NPR-23644: Hotfix do CQ-4243260
* (Firefox/Chrome) Não é possível baixar ativos na página Compartilhamento de ativos. NPR-23963: Hotfix do CQ-4244391
* Os aspectos de pesquisa do administrador de ativos desaparecem nos painéis de pesquisa após a visualização. NPR-23964: Hotfix do CQ-4244410
* Desfazer a publicação do formulário de pesquisa remove completamente o formulário de pesquisa padrão. NPR-23291: Hotfix do CQ-4241382
* (Brand Portal) A pesquisa no predicado de diretório deve ser filtrada na replicação. NPR-23292: Hotfix do CQ-4241385
* A ação Publicar na interface do Brand Portal não está disponível. NPR-23293: Hotfix do CQ-4241161
* O botão Publicar/Desfazer publicação no Brand Portal não deve estar disponível para fragmentos de conteúdo. NPR-23318: Hotfix do CQ-4245086
* (Brand Portal) Habilita a criação de ativos secundários quando um ativo é publicado. NPR-23331: Hotfix do CQ-4242018
* As solicitações do Dynamic Media não usam o cliente comum proxy/HTTP. NPR-10727: Hotfix do CQ-45695, CQ-88800
* Não é possível anotar o ativo de vídeo MP4 de representação única no Dynamic Media S7 (DMS7). NPR-22046: Hotfix do CQ-4215912
* Os dados EmbedXMP são sempre definidos como &quot;ativos&quot; para o processo de geração de Tiff e pirâmide. NPR-22903: Hotfix do CQ-4234498
* Problemas de exibição / seleção da representação dinâmica com uma grande contagem de Predefinições de imagens. NPR-23151: Hotfix do CQ-4217511
* Problema com a Codificação de vídeo do Dynamic Media - Modificar / Carregar novamente o iniciador. NPR-23237: Hotfix do CQ-4240260
* Correção de manuseio de proxy para o encaminhador HTTP no Dynamic Media S7. NPR-24001: Hotfix do CQ-244140

### Sites {#sites-8}

* As discrepâncias do Query Builder resultam em diferentes traduções do xPath entre as versões 6.2 e 6.3. NPR-23245: Hotfix do CQ-4240396
* A guia de Miniaturas na propriedade de página não funciona na extensão da caixa de diálogo. NPR-22844: Hotfix do CQ-4241474
* O Parsys quebra a largura do quadro do dispositivo emulador e corta qualquer componente adicionado a ele. NPR-22926: Hotfix do CQ-4238224
* Ao executar as várias inicializações, a inicialização promove no Author, mas as alterações não são replicadas no servidor de publicação devido à falta de permissões de replicação. NPR-22934: Hotfix do CQ-4234746
* Uma página bloqueada por um usuário na primeira sessão pode ser modificada por outro usuário em outra sessão. NPR-23057; Hotfix do CQ-4199017
* Corrija a opção reorganizável na Exibição em lista. NPR-23065: Hotfix do CQ-4239321
* (Editor de páginas) A imagem em um componente Imagem desaparece ao abrir a caixa de diálogo novamente. NPR-23156: Hotfix do CQ-4239978
* O Editor de modelos exibe apenas 20 modelos/pastas e não carrega os outros ao rolar para a parte inferior da página. NPR-23185: Hotfix do CQ-4238483
* (Interface clássica) Um erro é gerado ao mover ou renomear as páginas. NPR-23213: Hotfix do CQ-4240971
* Não é possível editar/criar segmentos do ContextHub. NPR-23218: Hotfix do CQ-4226948
* (Editor de Rich Text) - A operação Substituir altera o formato de uma palavra. NPR-23271: Hotfix do CQ-4239677
* O botão de implantação está ausente na guia Blueprint para variações XF. NPR-23320: Hotfix do CQ-4240404
* A interface clássica não funciona para editar o CUG devido à sua descontinuação. NPR-24122: Hotfix do 4241823
* Correção proativa para proteção contra promoções de conteúdo indesejadas. NPR-24387: Hotfix do 4244993
* Quando aproximadamente 80 fragmentos são adicionados em uma pasta nos Ativos, erros encontrados quando o fluxo de trabalho é acionado no console Linha do tempo. NPR-23393; Hotfix do CQ-4211216
* Não é possível arrastar e soltar imagens na caixa de diálogo Editor de Rich Text do localizador de conteúdo. NPR-23403: Hotfix do CQ-4242094
* Erro &quot;Valor inválido do seletor de recursão&quot; ao migrar um componente do AEM 6.0 para o AEM 6.2. NPR-23532: Hotfix do CQ-4241258
* (Editor de Rich Text) As dicas de ferramentas mostram o nome da variável do plug-in em vez do nome do plug-in legível. NPR-23550: Hotfix do CQ-4243269
* Não é possível salvar a caixa de diálogo com o menu suspenso de seleção necessário na versão móvel/tablet. NPR-23904: Hotfix do CQ-4243096
* As opções de estilo do sistema aparecem em todas as páginas após a instalação da versão 6.3.2.1. NPR-23972: Hotfix do CQ-4244394
* A interface clássica não funciona para editar o CUG devido à sua descontinuação. NPR-24122: Hotfix do 4241823
* Correção proativa para proteção contra promoções de conteúdo indesejadas. NPR-24387: Hotfix do 4244993
* As referências de ativos não são atualizadas quando os ativos são movidos. NPR-23208: Hotfix do CQ-4239879

### Plataforma {#platform-1}

* A coleção inteligente não exibe os resultados após salvar se as tags forem usadas como predicado nos aspectos de pesquisa. NPR-23401: Hotfix do Granite-21278
* Patch jQuery 1.12.4 do clientlib para incluir a correção de segurança. NPR-24128: Hotfix do Granite-20058
* As traduções de internacionalização não são atualizadas, a menos que o pacote seja reiniciado. NPR-23193: Hotfix do Sling-7190
* Resolvedor de recursos não fechado em ReplicationEventListener. NPR-23240: Hotfix do CQ-4241350
* Suporte a STARTTLS no &quot;Day CQ Mail Service&quot;. NPR-23941: Hotfix do CQ-4240397
* O nome da tag de reclamação do JCR deve ser preenchido automaticamente com base no Título da tag. NPR-24173: Hotfix do CQ-4199411

### Integração {#integration-4}

* (Target) As campanhas não são ativadas ao usar o tipo de API como XML. NPR-23199: Hotfix do CQ-4240936****
* A replicação da referência de configuração falha com a estrutura de pastas intermediária. NPR-23485: Hotfix do CQ-4242751

### Vulnerabilidade {#vulnerability-2}

* A integração do Salesforce está vulnerável à Falsificação de solicitação do lado do servidor (SSRF). NPR-24289: Hotfix do CQ-424527
* Criação de script entre sites (XSS) nos links de Projeto da interface do usuário do administrador. NPR-23272: Hotfix do CQ-4241795

### WCM - Componentes do Foundation {#wcm-foundation-components}

* A tabela do Foundation é vulnerável a Scripts armazenados entre sites. NPR-23214: Hotfix do CQ-4240760

### Tradução {#translation-3}

* As propriedades da Live Copy não são excluídas ao criar cópias de idioma. NPR-23123: Hotfix do CQ-4230641

### Interface do usuário {#user-interface-1}

* O DatePicker não é compatível com a definição manual de dicas de tipo externas definidas por campo oculto. A alteração da dica de tipo aciona um erro de conversão. NPR-23371: Hotfix do Granite-21194
* Coral.ColumnView: adiciona suporte para shift+click. NPR-23404: Hotfix do Granite-13338
* Selecionar RT não valida quando um item com valor vazio é selecionado. NPR-23405: Hotfix do Granite-21283
* (OMEGA) Reportar &quot;Feature&quot; somente em inglês. NPR-23990: Hotfix do Granite-21231
* Correções na API Coral.Autocomplete. NPR-23516

### Granite {#granite-1}

* As conexões de rastreamento de clientes Http do Apache e a alta utilização do heap causam falha no servidor AEM. NPR-23906: Hotfix do Granite-21056

### Commerce {#commerce-2}

* A saída json da campanha não contém a raiz de contexto do servlet. NPR-23733: Hotfix do CQ-4243827

### Communities {#communities-7}

* A pesquisa nas comunidades falha com poucas palavras. NPR-23256: Hotfix do CQ-4240717
* Não é possível atribuir grupos para o problema de função dos gerentes da comunidade. NPR-23317: Hotfix do CQ-4241233: CQ-4221399
* Problemas na criação de recursos com nomes de ativos semelhantes. NPR-23319: Hotfix do CQ-4240700
* (ContextPath) A funcionalidade da mensagem de interrupção falha devido a configurações e erros do Jetty ao pesquisar membros do grupo na lista de membros do grupo da comunidade. NPR-23336: Hotfix do CQ-4241519/CQ-4242080
* O upload de uma imagem em um Fórum do Communities não é exibido no Provedor de recurso de armazenamento da Adobe (ASRP). NPR-23397: Hotfix do CQ-4242497
* As ideias excluídas são exibidas como links ativos em Atividades. NPR-23406
* imsmanifest.xml não pode ser carregado com o AEM em execução na raiz de contexto. NPR-23483: Hotfix do CQ-4242193
* Vulnerabilidades de segurança em uma versão mais antiga do Handlebars. NPR-23518: Hotfix do CQ-4243055
* O serviço de túnel não está funcionando. NPR-23543: Hotfix do CQ-4242217
* Problemas com componentes de comunidades quando acessados por meio do Dispatcher e do sling dynamic incluem o ativado. NPR-23586: Hotfix do CQ-4242360, CQ-4241522
* Ao pesquisar por um termo de pesquisa que produza muitos resultados e, em seguida, inserir um novo termo, a paginação não é redefinida. NPR-23739: Hotfix do CQ-4222593
* Problemas ao executar a pesquisa no componente do fórum. NPR-23838: Hotfix do CQ-4243770
* (Sinalização de moderação de comunidades) A permissão em massa de mensagens sinalizadas não está funcionando. NPR-23845: Hotfix do CQ-4243962
* O texto do botão Classificar não mostra o valor selecionado padrão apesar de selecionar a ordem de classificação padrão. NPR-23881: Hotfix do CQ-4243375
* As notificações por email e Web não são acionadas devido à falha de mensagem nos grupos. NPR-23934: Hotfix do CQ-4242880
* Nenhum detalhe é exibido sobre os usuários sinalizados e os motivos usando a configuração do DSRP. NPR-23973: Hotfix do CQ-4243205
* Os motivos da sinalização dos usuários que não estão sinalizados permanecem visíveis/ NPR-23974: Hotfix do CQ-4243822
* Anexar dois arquivos com o mesmo nome duas vezes a uma publicação de formulário resulta em um erro de servidor. NPR-24166: Hotfix do CQ-4244367
* Não é possível armazenar anexos com tipos MIME com mais de 15 caracteres usando o Desenvolvedor de recursos de armazenamento do banco de dados (DSRP). NPR-24174
* Quando uma imagem que viola os critérios de upload é arrastada e solta no texto da publicação, um erro de servidor é acionado e uma mensagem de erro genérica é exibida ao usuário. NPR-24243
* Correções de vários problemas do lado do servidor do AEM Communities. NPR-23971: Hotfix do CQ-4243144, CQ-4242145, CQ-4243365, CQ-4244098
* Correções de vários problemas do Adobe Social. NPR-24242: Hotfix do CQ-4245054, CQ-4245120, CQ-4245296

### Campaign {#campaign}

* A saída json da campanha não contém a raiz de contexto do servlet. NPR-23733: Hotfix do CQ-4243827

### MSM {#msm}

* Ao rolar a página, a livecopy não mostra as propriedades de tempo de ativação/desativação herdadas do principal. NPR-23873: Hotfix do CQ-4243431
* A operação LiveCopy não ignora nós secundários de componentes excluídos. NPR-23058: Hotfix do CQ-4211662

### Descarregamento {#offloading}

* Solicitação para que o mecanismo limpe os ativos das instâncias do trabalhador após o processamento ou regularmente. NPR-23638: Hotfix do Granite-21337

## Forms {#forms-8}

### Pacote complementar do Forms {#forms-add-on-package-8}

#### Formulários adaptáveis {#adaptive-forms-1}

* Mova ReCaptchaConfigService para o pacote interno. Hotfix do CQ-4217459
* O campo numérico não respeita o valor mínimo. NPR-23967: Hotfix do CQ-4244830
* Suporte a vários fragmentos na integração do Adaptive Forms com o Adobe Sign. NPR-23383

#### Integração de backend {#backend-integration}

* (FDM) (WebService) Compatibilidade com a construção de extensões de WSDL no analisador WSDL. NPR-23640, NPR:23236: Hotfix do 4205821
* Para incluir SDLInvokerParams no SDK do cliente do complemento do Forms. NPR-23157

### Instalador do Forms JEE {#forms-jee-installer-7}

#### Gerenciamento de processos {#process-management}

* Não é possível abrir o espaço de trabalho após aplicar o novo arquivo axis.jar. NPR-23316
* O LiveCycle é vulnerável ao XSS no PMAdmin. NPR-23267
* Depois de atualizar para o AEM 6.1 Forms, o espaço de trabalho HTML congela ao acessar a Lista de tarefas de usuários específicos. NPR-23943

#### Núcleo {#core}

* O Forms JEE é compatível com autenticação mútua PKCS#11. NPR-21372

#### Serviço PDFG {#pdfg-service-2}

* O serviço de captura de papel falha durante o processamento simultâneo de arquivos TIFF (tamanho de aproximadamente 50 KB). NPR-23556

#### Designer do Forms {#forms-designer}

* Saída do servidor do AEM Forms - Descrição alternativa ausente para anotações. NPR-22207
* Adicionar suporte de PDF/UA a formulários XML gerados por meio do Designer e do Serviço de saída. NPR-23132

### Pacotes OSGI e de conteúdo incluídos na 6.3.2.2 {#osgi-bundles-and-content-packages-included-in-4}

Lista de pacotes OSGi incluídos no AEM 6.3.2.2

[Obter arquivo](assets/do-not-localize/6_3_2_2_bundle-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.2.2

[Obter arquivo](assets/do-not-localize/6_3_2_2_content_packagelist.txt)

### Cumulative Fix Pack 6.3.2.1 {#cumulative-fix-pack-9}

O AEM Cumulative Fix Pack 6.3.2.1 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 2 (6.3.2.0), em abril de 2018.

Os principais destaques do **AEM Cumulative Fix Pack** são:

* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.10.
* Aprimoramento na renderização dos componentes Parsys na interface clássica.
* Atualização dos pacotes de modelos de sling para incluir a correção de conjunto de caracteres.
* Publicação no Brand Portal assíncrona para todos os tipos de ativos.
* Atualização do coralui-component-richtexteditor.git de 0.1.15 para 0.1.16
* Correções na funcionalidade mostrar/ocultar do componente suspenso.
* Habilitação da inversão de imagem para o Componente principal de imagem.
* Atualização de pacotes felix http para ativar os atributos da sessão.

* Remoção do cache=true dos modelos Sling devido a problemas de consumo de memória.

### Ativos {#assets-9}

* Ao alterar o título ou a imagem em miniatura nas configurações da Pasta de ativos, o grupo original e as permissões da pasta são substituídos. NPR-22171: Hotfix do CQ-4216080
* A interface gera o erro falso &quot;Falha na publicação no Brand Portal&quot;, enquanto o trabalho é adicionado à Fila de replicação e os ativos são publicados no Brand Portal. NPR-22179: Hotfix do CQ-4205273
* (Interface de toque) Local de upload padrão para ativos na exibição em Coluna. NPR-22465: Hotfix do CQ-4237057
* O AEM aciona o erro StackOverflow ao tentar copiar um esquema de ativo de /conf/global para /conf/ mytenant. NPR-22489: Hotfix do CQ-4235875
* A tentativa de descompactar um arquivo ZIP falha devido ao espaço no final do nome da pasta. NPR-22522: Hotfix do CQ-4238036
* A classificação usando a coluna Título do ativo não funciona para os resultados da pesquisa. NPR-22908: Hotfix do CQ-4239076
* O vídeo do YouTube é marcado com o caminho completo em vez do próprio nome da tag. NPR-22976: Hotfix do CQ-4238669
* A reorganização de pastas em uma pasta reorganizável não é mantida. NPR-23125: Hotfix do CQ-4231761
* HTTP 504: Erro de tempo limite do gateway ao tentar compartilhar coleções usando o link de compartilhamento. NPR-21928: Hotfix do CQ-4234507
* Os metadados de palavras-chave do PDF não são extraídos e são modificados incorretamente quando há várias palavras-chave associadas a um Ativo PDF. Para resolver o problema, a propriedade de metadados do campo Assunto foi removida para os Ativos PDF. No entanto, você pode editar o esquema de metadados para adicionar um campo de texto de vários valores para o campo Assunto. NPR-21972: Hotfix do 4215741****
* Os ativos incorretos serão excluídos se a pasta selecionada for alterada entre o momento em que os 2 pop-ups forem exibidos. NPR-21980: Hotfix do CQ-4233675
* (DAM) Várias vulnerabilidades de script entre sites (XSS) ao adicionar ao assistente de coleção. NPR-22432: Hotfix do CQ-4327086
* O download de ativos falha ao usar o Gerenciamento de direitos digitais nos Ativos do Safari. Os usuários não conseguem baixar ativos com aviso de isenção de responsabilidade e nomes de arquivo longos. NPR-22747: Hotfix do CQ-4236460 e CQ-4235274
* Torne o compartilhamento público como a opção padrão ao publicar ativos no Brand Portal. NPR-21931: Hotfix do CQ-4218816

### Sites {#sites-9}

* O novo item na caixa de entrada do Fluxo de trabalho mostra o caminho da página em vez do título da página. NPR-21634: Hotfix do CQ-4230672
* Componentes de estrutura editáveis perdem os nomes de classe CSS necessários para a grade responsiva quando editados. NPR-21741: Hotfix do CQ-4232374
* (Interface de toque) Várias vulnerabilidades de script entre sites (XSS) em componentes HTL. NPR-21899: Hotfix do CQ-4232511
* Não é possível alterar o tipo de recurso de imagem de mídia mista do fragmento de conteúdo. NPR-21907: Hotfix do CQ-4233401
* A tela cheia do RTE da caixa de diálogo de interface de toque oculta os plug-ins do RTE. NPR-22034: Hotfix do CQ-4235457
* (Interface de toque) O Editor de Rich Text remove todos os atributos exceto a ID da tag &lt;a>. NPR-22044: Hotfix do CQ-4234133
* Vários Parsys empilhados devido a consultas de longa duração (mais de 6) tornam o AEM lento. NPR-22134: Hotfix do CQ-4233904
* Não é possível alterar permissões em nós que tenham dois-pontos no nome. NPR-22136: Hotfix do CQ-4236221
* (Interface clássica) O html de saída do editor de Rich Text adiciona &quot;list-position-style: inside;&quot; como um estilo incorporado à tag &lt;ul> tag. NPR-22145: Hotfix do CRTE-114
* Fazer TreeNode voltar para o atributo de nome quando o texto estiver vazio. NPR-22146: Hotfix do CQ-4234724/CQ-4236300
* Problemas de Feed RSS, porta -1 do AEM 6.3 NPR-22176: Hotfix do CQ-4233339
* (Interface clássica) Colar o atalho de texto (Ctrl+V) não funciona para o componente de texto OOTB (Rich Text). NPR-22224: Hotfix do CQ-4236224
* A filtragem de Tagfield não está funcionando como esperado ao digitar o texto. NPR-22236: Hotfix do CQ-4236655
* (Editor de páginas) Ao colar dados de texto no componente de mapa da imagem, o componente de texto também é colado. NPR-22264: Hotfix do CQ-4236230
* O campo FileUpload da caixa de diálogo necessário causa problemas no envio da caixa de diálogo. NPR-22464: Hotfix do CQ-4222192
* Mover sem permissões de replicação inicia uma solicitação para o fluxo de trabalho de ativação se a página movida ou seus referenciadores não puderem ser ativados. NPR-22467: Hotfix do CQ-4211765
* Problemas de desempenho ao carregar uma página com públicos-alvo grandes (mais de 2000). NPR-22478; Hotfix do CQ-4209567
* Problemas de persistência quando o ContextHub armazena a camada de persistência padrão durante a inicialização. NPR-22479: Hotfix do CQ-4218399
* O Launch com várias páginas não publica subpáginas em servidores de publicação se a opção &quot;incluir subpáginas&quot; não estiver marcada na primeira raiz de conteúdo. NPR-22482: Hotfix do CQ-4237818
* (Interface para toque) A exclusão de inicializações por meio do console da interface clássica torna todas as páginas não editáveis. NPR-22491: Hotfix do CQ-4225074
* Problemas com o componente de Imagem devido ao espaço extra na caixa de diálogo. NPR-22528: Hotfix do CQ-4238183
* Ao abrir o componente usando o modo em linha, os plug-ins carregados anteriormente não ficam visíveis na segunda vez. NPR-22591: Hotfix do CQ-4236850
* A exclusão de uma inicialização em uma inicialização aninhada faz com que as inicializações secundárias fiquem órfãs. NPR-22621; Hotfix do CQ-4202639
* (Sidekick da interface clássica) A guia Fluxo de trabalho é desativada quando a página está no estágio de bloqueio de fluxo de trabalho. NPR-22722: Hotfix do CQ-4237557
* Depois de virar uma imagem adicionada ao componente de Imagem em uma página, as alterações não são salvas e a imagem original é exibida na página. O suporte à renderização foi adicionado ao componente principal da imagem por meio de [https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141](https://github.com/Adobe-Marketing-Cloud/aem-core-wcm-components/pull/141). NPR-22801: Hotfix do CQ-4221539
* Quando o usuário tenta excluir a âncora existente do menu de âncora, a janela do componente Editor de Rich Text é fechada e as alterações não são salvas. NPR-22802: Hotfix do CQ-4238167
* O filtro Omnisearch não mostra todas as ações no console Sites. NPR-22804: Hotfix do CQ-4239007
* Problema ao copiar/colar na interface do usuário de toque com a área de transferência do sistema operacional e a área de transferência interna do AEM. NPR-22807: Hotfix do CQ-4220383
* Inconsistência no destaque de Excerto retornado pela Pesquisa do Lucene. NPR-22879: Hotfix do CQ-4238513
* Ativar uma página com instâncias de publicação desativadas resulta em status verde em vez de âmbar. NPR-22927: Hotfix do CQ-4236310
* (StyleSystem) A posição da tela salta ao selecionar o estilo no pop-up. NPR-23183: Hotfix do CQ-4238867
* (Gerenciar publicação) Mover para o próximo mês do calendário requer vários cliques. NPR-23508: Hotfix do CQ-4242732

### Plataforma {#platform-2}

* O servlet do Sling Exporter não exporta caracteres japoneses corretamente. NPR-22153: Hotfix do CQ-4228920
* Bloqueio do Scheduler durante a inicialização. NPR-22440: Hotfix do Sling-7004
* Não é possível sincronizar grupos entre duas instâncias de publicação. NPR-21943: Hotfix do Granite-19564
* Problemas de desempenho com a sessão compartilhada/resolvedor de recursos org.apache.sling.i18n. NPR-23390: Hotfix do Sling-7543

### Integração {#integration-5}

* ResourceResolver não fechado em com.day.cq.analytics.sitecatalyst. NPR-22323: Hotfix do CQ-4236515
* TargetContentImpl torna o AEM lento durante consultas de longa execução. NPR-22361: Hotfix do CQ-4236907
* O mecanismo do Target (mbox.js, at.js) não usa URLs danificados e usa URLs que contêm dois pontos que podem falhar com determinadas implantações. NPR-22366: Hotfix do CQ-4237854
* Ao fornecer um at.js ou mbox.js personalizado, o script incluído é gravado na página como texto em vez de tags HTML. NPR-22441: Hotfix do CQ-4203691
* No modo Target, os autores podem modificar um componente herdado do blueprint sem cancelar a herança. NPR-22751: Hotfix do CQ-4237907
* O PersonalizationDataSource aciona uma Exceção de ponteiro nulo devido à ausência do nó jcr:content. NPR-22850: Hotfix do CQ-4222122
* A definição de metas do AEM falha ao usar idioma que não seja em inglês. NPR-22917: Hotfix do CQ-4218213
* A publicação de uma página com conteúdo direcionado não possui recursos relacionados. NPR-23064: Hotfix do CQ-4227119
* Os usuários não podem ver valores de Parâmetros estáticos de testes na chamada da mbox, que podem ser vistos ao testar o AT.js como a biblioteca do cliente na configuração da nuvem. NPR-21930: Hotfix do CQ-4234520

### WCM-Componentes do Foundation {#wcm-foundation-components-1}

* O iParsys cria o deslocamento de posição depois de desmarcar a caixa de seleção cancelar/desabilitar herança. NPR-21905: Hotfix do CQ-4230951
* A funcionalidade Mostrar/Ocultar do componente de formulário suspenso não está funcionando como esperado. NPR-22327: Hotfix do CQ-4222853
* O componente CAPTCHA foi descontinuado para melhor segurança. Se você estiver usando o componente CAPTCHA, a mensagem &quot;O componente Captcha está obsoleto e não deve mais ser usado&quot;. será exibida após a instalação da versão 6.3.2.1 ou posterior. O componente do AEM pode ser personalizado para incluir o reCAPTCHA para melhor segurança NPR-22151: Hotfix do CQ-4220052

### WCM - Editor de páginas {#wcm-page-editor}

* Script entre sites (XSS) refletido ao usar um seletor inválido. Hotfix do CQ-4270397

### Tradução {#translation-4}

* Investigue problemas com a funcionalidade Visualização. NPR-22114: Hotfix do CQ-4223753

### Interface do usuário {#user-interface-2}

* Problemas com o seletor de mês do calendário Coral quando o intervalo de datas &quot;mín&quot; e &quot;máx&quot; é definido. NPR-22716: Hotfix do CUI-7187
* (Interface clássica) O componente exibe os valores padrão mesmo se o serviço de modelo de dados de formulário associado estiver definido como campo vazio. NPR-22272: Hotfix do GRANITE-19744

### Granite {#granite-2}

* AEM Problemas de estabilidade com a instância do publicador do Compartilhamento de ativos causados por vazamento de memória. NPR-22205, NPR-23178: Hotfix do Sling-5668, Sling-7292 e Sling-7470.
* A ID de serviço instável não deve ser usada para nomes de atributos de sessão. NPR-22821: Hotfix do Granite-21059
* Quando uma sessão gerenciada por whiteboard http é invalidada, a sessão do container também é invalidada se a sessão não tiver outros atributos. NPR-23059: Hotfix do FELIX-5819
* O LogbackManager pode perder algumas configurações do OSGi no momento da inicialização. NPR-23060: Hotfix do Granite-19791

### Commerce {#commerce-3}

* Habilite a criação de fluxo de trabalho no menu de Fragmentos de experiência. NPR-22347: Hotfix do CQ-4221661
* Erros de Fragmentos de experiência reproduzíveis no WeRetail. NPR-21958: Hotfix do CQ-4220061
* Ativar uma página que contém um fragmento de experiência excluído aciona uma exceção de ponteiro nulo. NPR-23179: Hotfix do CQ-4239939

### Projetos {#projects}

* (Projeto multilíngue) O projeto não lista trabalhos de tradução com mais de 19 idiomas. NPR-22498: Hotfix do CQ-4229978

### Fluxo de trabalho {#workflow}

* (Interface clássica) A ativação ou desativação de um iniciador de fluxo de trabalho resulta em mau comportamento. NPR-22907: Hotfix do CQ-4239153

## Forms {#forms-9}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

Os principais destaques do AEM Forms são:

* Adicionado suporte para Tipo de entrada HTML5.
* Correção da Autenticação básica do cabeçalho SOAP.
* Adicionado suporte para atributo de título para hiperlink.
* Habilitação do Identificador PDF/UA na árvore de acessibilidade do Forms Designer.
* Ativação da autenticação de certificado para usuários do Workbench.
* Adição de suporte para produzir arquivos PDF compatíveis com PDF/A-2a ou PDF/A-3a.

### Pacote complementar do Forms {#forms-add-on-package-9}

#### Forms - Interface do usuário de administração {#forms-admin-ui}

* A senha é visível em texto sem formatação ao inspecionar o campo de senha das páginas de configuração dos Conectores ECM. NPR-22508: Hotfix do CQ-4236065

#### Serviço do Forms {#forms-service}

* Quando o SSL é ativado, os eventos Enviar e Abandonar não funcionam com o Form Analytics. NPR-22637; Hotfix do CQ-4237973

#### Gerenciamento de usuários {#user-management}

* Não é possível sincronizar o LDAP devido a uma versão incorreta do cglib-nodep. NPR-22493: Hotfix do CQ-4234099

#### Formulários adaptáveis {#adaptive-forms-2}

* As funções personalizadas do editor de regras estão adicionando um; a mais após chamada de função, portanto, ocorre falha na validação mesmo que a função personalizada retorne como verdadeiro. NPR-22481: Hotfix do CQ-4235499
* Independentemente do padrão de data selecionado, o componente Seletor de data não segue o padrão ao exibir mensagens de validação mínimas e máximas. NPR-22444: Hotfix do CQ-4236269
* O formato de data que está sendo enviado na solicitação de envio deve estar alinhado ao padrão fornecido no componente seletor de data. NPR-22384
* O número máximo de caracteres especificado para uma caixa de texto de formulário adaptável não é respeitado em dispositivos Android™ 6.0 Samsung. NPR-22363, NPR-22364: Hotfix do CQ-4235205
* (Microsoft® Edge) (IE11) O componente de campo de texto do formulário adaptável com campo de várias linhas exibe &quot;Null&quot; como valor padrão em vez de em branco. NPR-22284: Hotfix do CQ-69107
* A codificação de entrada SOAP UTF-8 nos formulários adaptáveis retorna erros com páginas distorcidas. NPR-20105: Hotfix do CQ-4222669
* O componente de container do AEM Forms não estará disponível para edição depois que o formulário incorreto for configurado na página Sites. Hotfix do CQ-4237456
* Os testes de desenvolvimento falham quando executados em servidores JEE. Hotfix do CQ-4222082
* Falha nos testes de AF em servidores JEE devido a problemas de minificação na estrutura Calvin. Hotfix do CQ-4217220

#### Gerenciador do Forms {#forms-manager}

* (Firefox) Não é possível atualizar as propriedades do Esquema XML dos formulários adaptáveis, pois as opções no Documento de registro (DOR) não são pré-selecionadas na página Propriedades. NPR-22298: Hotfix do CQ-4237402
* Os formulários modificados após a publicação da página não serão publicados novamente na publicação do site. NPR-23013: Hotfix do CQ-4236566

#### Integração de backend {#backend-integration-1}

* A autenticação básica OOTB de serviços SOAP não funciona para autenticação básica na integração do FDM. NPR-23238: Hotfix do CQ-4241308

#### Gerenciamento de correspondência {#correspondence-management}

* Os XDPs do OOTB, quando usados dentro da carta e visualizados, mostram o conteúdo sobreposto ao rodapé. Hotfix do CQ-4212414

#### Serviço de Assembler {#assembler-service}

* Discrepância entre os relatórios do Acrobat DC e AEM sobre o erro de verificação de conformidade do PDF/A-1b. NPR-22051, NPR-22050: Hotfix do CQ-4226128, CQ-4227671

### Instalador do Forms JEE {#forms-jee-installer-8}

#### Workbench {#workbench}

* Ativação da autenticação de certificado para usuários do Workbench. NPR-20644: Hotfix do CQ-4214486
* Baixar o log do servidor usando o Workbench funciona somente para um servidor, não para o outro. NPR-21079: Hotfix do CQ-4229842

#### Gerenciamento de processos {#process-management-1}

* (Espaço de trabalho HTML) Problemas de tamanho de tela com barras de rolagem. NPR-23288
* (Espaço de trabalho HTML) Os pontos de partida do processo não são classificados em ordem alfanumérica. NPR-22841 Hotfix do CQ-4238944
* (Espaço de trabalho HTML) A preparação de dados é acionada ao fechar o formulário no espaço de trabalho. NPR-21127: Hotfix do CQ-4224574
* (Espaço de trabalho HTML) Ao invocar um processo que requer anotações com descrições longas, o botão Expandir anotações não funciona. Hotfix do CQ-4241488

#### Núcleo {#core-1}

* Erro encontrado na inicialização ao iniciar o Scheduler. NPR-22990
* Impede que os navegadores armazenem credenciais inseridas em formulários HTML. NPR-21762: Hotfix do CQ-4206543
* Os problemas relatados na análise de código estático do Core devem ser corrigidos. Hotfix do CQ-104446

#### Serviço PDFG {#pdfg-service-3}

* O Gerador de PDF não produz documentos PDF com níveis de marcadores especificados. NPR-22921, NPR-22285: Hotfix do CQ-4230562
* Adição de suporte para produzir arquivos PDF compatíveis com PDF/A-2a ou PDF/A-3a. NPR-23021: Hotfix do CQ-4214172

#### Designer do Forms {#forms-designer-1}

* O Identificador PDF/UA fica ausente quando salvo como PDF a partir do Designer. NPR-23137
* Objetos de caminho, por exemplo: bordas, sublinhados e hiperlinks, não são marcados quando salvos como PDF a partir do Designer. NPR-23136
* O objeto de imagem não tem caixa delimitadora quando salvo como PDF a partir do Designer. NPR-23134
* Os hiperlinks em linha definidos no Designer não são marcados ou possuem texto alternativo quando salvos como PDF a partir do Designer. NPR-23133
* A abertura do Pacote de dados XML com o AEM 6.3 Forms Designer remove a formatação XHTML da origem XML. NPR-21178: Hotfix do LC-3917046

#### Instalar o LCM {#install-lcm}

* Atualize o Jsafe Jars para Cryptoj 6.1.3.1 no instalador e no LCM. NPR-21370

#### Serviço de assinaturas {#signatures-service}

* Exceção encontrada ao tentar assinar/certificar digitalmente um documento PDF por meio do HSM. NPR-21154: Hotfix do CQ-4226978

### Pacotes OSGI e de conteúdo incluídos na 6.3.2.1 {#osgi-bundles-and-content-packages-included-in-5}

Lista de pacotes OSGi incluídos no AEM 6.3.2.1

[Obter arquivo](assets/do-not-localize/bundle-list_002_.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.2.1

[Obter arquivo](assets/do-not-localize/content_package_comparison.txt)

O AEM Cumulative Fix Pack 6.3.1.2 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 1 (6.3.1.0), em outubro de 2017.

Os principais destaques do AEM Cumulative Fix Pack são:

* Interface do usuário modificada para oferecer suporte à implementação da funcionalidade de CUG no AEM Assets.
* Correção de problemas de interface na página de verificação de licença para obter melhor experiência.
* Habilitação do suporte à tarefa de fluxo de trabalho do OSGi no aplicativo AEM Forms.

### Ativos {#assets-10}

* Interface do usuário modificada para oferecer suporte à implementação da funcionalidade de CUG no AEM Assets. NPR-19485
* Fazer upload de um ativo como um nó filho a partir de si mesmo usando a interface do usuário de toque causa um problema. O ativo é carregado como um filho direto do ativo selecionado anteriormente. NPR-19736
* O predicado de Intervalo de datas e de Intervalo não funcionam ao carregar uma pesquisa salva/coleção inteligente. NPR-19844: Hotfix do CQ-4220808
* A instância do AEM fica lenta quando vários ativos (mais de 4) são publicados no Brand Portal. NPR-20009: Hotfix do CQ-4213426
* Não é possível baixar ativos com espaços da página de verificação de licença. NPR-20067: Hotfix do CQ-4216557
* Problemas de processamento ao carregar arquivos PSB com várias camadas alfa. NPR-20250: Hotfix do CQ-4220869
* Os usuários não conseguem baixar ativos com nomes de arquivo longos e aviso de isenção de responsabilidade definido. NPR-20254
* O ProductAssetsUploader deixa os arquivos temporários do cache Java™ na pasta TEMP Java™. NPR-20256: Hotfix do CQ-4221801
* Substituição do código de comparação de versão pelo código proprietário da Adobe devido a problemas de licenciamento. NPR-20272: Hotfix do CQ-4223758
* Os metadados de uma propriedade de cadeia de caracteres, documentNumber, são exibidos como uma data, enquanto deveria ser um número. NPR-20291: Hotfix do CQ-4223991
* A extração de texto para de funcionar com um PDF corrompido. NPR-20416: Hotfix do CTG-4150375
* Os arquivos compactados que incluem ativos com nomes não compatíveis com UTF-8 não são baixados corretamente. NPR-20420: Hotfix do CQ-4219961
* Muitos caracteres no OmniSearch causa falha no servidor AEM. NPR-20434: Hotfix do CQ-4223602
* O defeito dos metadados da API de ativos do DAM causa falha nas APIs xmp -write-back. NPR-20607: Hotfix do CQ-4220455
* Problemas de desempenho ao adicionar usuários às coleções. NPR-20699: Hotfix do CQ-4225733
* Publicar no Brand Portal a partir do AEM não deve ser permitido para conjuntos do Dynamic Media. NPR-20320: Hotfix do CQ-4221147
* O vídeo com espaços e acentos não resulta vídeos da página Representações. NPR-19961: Hotfix do CQ-4221014
* Solução de vários problemas de manuseio de pastas com APIs de ativos. NPR-20569
* O AEM Dynamic Media Classic (antigo Scene7) falha ao sincronizar ativos do servidor AEM quando o caminho de destino na configuração do Cloud Service aponta para uma subpasta no caminho raiz. CQ-4228265
* Pacote de email do Apache commons `{org.apache.commons/commons-email/1.5}` foi adicionado, substituindo `{com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002}`.

### Sites {#sites-10}

* Problemas de Permissão de administrador: não é possível remover membros do Grupo de usuários fechado das propriedades da página. NPR-20631
* O nome do fluxo de trabalho digitado deve estar disponível na caixa Notificações ao publicar a página por meio de Gerenciar publicação. NPR-20046: Hotfix do CQ-4221586
* Aplicar texto estilizado em duas linhas no Editor de Rich Text e, em seguida, mesclar em um parágrafo remove as extensões estilizadas. NPR-20110: Hotfix do CQ-4223051
* As alterações feitas nas propriedades do campo em várias guias na caixa de diálogo Editar propriedade às vezes não são salvas. NPR-20286
* Tag inesperada no final do conteúdo colado no Fragmento de conteúdo. NPR-20413: Hotfix do CQ-4224014
* Implementação de um mecanismo no Adobe Campaign para buscar a política de um recurso de conteúdo a partir de um recurso de direcionamento externo. NPR-20667
* O plug-in Richtext não funciona nas barras em linha e tela cheia na interface do usuário de toque de vários campos. NPR-20973

### Campaign {#campaign-1}

* Os espaços reservados não estão visíveis em uma página que contém vários componentes do Parsys. NPR-20436; Hotfix do CQ-4215000

### Commerce {#commerce-4}

* Os Fragmentos de experiência não são exibidos corretamente no Internet Explorer 11. NPR-20161: Hotfix do CQ-4223319
* Em fluxos de trabalho de comércio, uma imagem em branco é inserida automaticamente ao criar uma variante com base em um produto principal com várias imagens. NPR-20068: Hotfix do CQ-4222048
* A filtragem por tags nas páginas de coleção do console de produtos não funciona. NPR-20292: Hotfix do CQ-4224023

### Communities {#communities-8}

* Resultados de pesquisa inconsistentes com o componente searchresult. NPR-20070: Hotfix do CQ-4220913
* As notificações por email não são acionadas nas atividades relacionadas ao moderador em componentes publicados. NPR-20122
* A paginação em branco sem resultados é exibida para usuários anônimos da comunidade. NPR-20136: Hotfix do CQ-4220738
* Configure o acionador de alerta quando um UGC for detectado como spam ou quando um usuário publicar em um site pré-moderado. NPR-20274: Hotfix do CQ-96850
* Solução de vários problemas nas páginas do site AEM Communities, incluindo redirecionamentos incorretos e problemas de atualização de página. NPR-20344
* CommunityUserOperationExtension é executado em uma exceção de conversão de classe. NPR-20532: Hotfix do CQ-4224385
* Depois de criar um site Communities, os usuários não podem abri-lo a partir do mapa do site, pois o caminho do contexto não é anexado ao URL. NPR-20730

### Integração {#integration-6}

* Migração de credenciais existentes do Analytics para a Autenticação WSSE. NPR-19962: Hotfix do CQ-4218071
* A reativação do segmento após qualquer modificação falha e gera um erro. NPR-20054: Hotfix do CQ-4218401
* A configuração do serviço de nuvem Search&amp;Promote ignora o método de recuperação de formulário, tornando-o inutilizável na instância do autor. NPR-20447: Hotfix do CQ-4206076
* A definição ambígua de filtro no pacote de conteúdo faz com que os caminhos sejam substituídos quando o recurso Search&amp;Promote estiver instalado. NPR-20808

### Mobile On-Demand {#mobile-on-demand}

* As propriedades de metadados de ativos do tipo TXT são exibidos em diferentes editores de metadados sempre que as propriedades são exibidas. NPR-20239

### Plataforma {#platform-3}

* Solução de uma exceção do resolvedor de recursos não fechado. NPR-19749: Hotfix do Granite - 19143
* Solicitação para que cartões personalizados sejam exibidos junto com as verificações de integridade padrão no painel de operações. NPR-20145
* A camada de anotação do editor de página não funciona corretamente no Internet Explorer 11. NPR-20222: Hotfix do CQ-4222818
* A sessão vaza ao configurar o Agente do usuário como administrador no agente de replicação. NPR-20578
* O requestAttributes não tem a definição removida das outras declarações data-sly-resource. NPR-20639: Hotfix do 4226206
* Correção de problemas com solicitações curl Head para ativos OOTB no AEM. NPR-20781: Hotfix do CQ-4221520

### Projetos {#projects-1}

* O acesso a diferentes projetos no console Projetos leva mais tempo para carregar. NPR-20314
* A instalação do AEM 6.3.0.1 remove o armazenamento de chaves do usuário dam-update-service. NPR-20018
* Em algumas implantações personalizadas, os usuários que tentam selecionar um destinatário no módulo addTask demoram mais para preencher a lista no seletor de usuários. NPR-20283: Hotfix do CQ-4224193

### Interface do usuário {#user-interface-3}

* O campo de cor é definido como &quot;sempre obrigatório&quot; apesar dos atributos na caixa de diálogo. NPR-19702
* A barra de rolagem não é exibida para o componente de vários campos em tela cheia no Internet Explorer 11. NPR-20261: Hotfix do CQ-4219782
* As consultas anteriores não são abortadas caso consultas consecutivas sejam acionadas, resultando em resultados incorretos. NPR-20398: Hotfix do GRANITE-19306

### Fluxo de trabalho {#workflow-1}

* Os usuários não são notificados sobre as tarefas de fluxo de trabalho que recebem em sua caixa de entrada. NPR-20213: Hotfix do CQ-4221639
* O seletor de usuários OOTB granite não carrega nenhum usuário quando clicado na etapa suspensa do participante na caixa de diálogo do modelo de fluxo de trabalho. NPR-20236

## Forms {#forms-10}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-10}

#### Formulários adaptáveis {#adaptive-forms-3}

* Falta o suporte para a expressão de agregação de painéis repetidos. NPR-20861
* A lista suspensa exibe o último valor armazenado, mesmo se o serviço de modelo de dados de formulário associado não retornar um valor. NPR-20710
* Não é possível editar as regras existentes com restrições booleanas no Editor de regras. NPR-21128

#### Portal do Forms {#form-portal}

* O perfil HTML é exibido para um formulário adaptável mesmo quando seu tipo de ativo não é XDP. NPR-20079

#### Integração de backend {#backend-integration-2}

* Não é possível definir o valor do componente alternar entre verdadeiro/falso. NPR-21111

#### Fluxo de trabalho OSGI {#osgi-workflow}

* Gerenciar o envio de fluxo de trabalho lista somente dez aplicativos. CQ-4230193

#### Formulários HTML5 {#html-forms-3}

* O nome de um objeto de formulário XDP como formulário secundário é exibido como a dica de ferramenta quando não está definido nas configurações de acessibilidade. NPR-20523

### Instalador do Forms JEE {#forms-jee-installer-9}

#### Gerenciamento de processos {#process-management-2}

* O ponto de partida FormSetPrefillApp não preenche os campos do conjunto de formulários no aplicativo AEM Forms. NPR-20950

#### Forms - AEM (LiveCycle) {#forms-aem-livecycle}

* Instale a biblioteca CTJPEG2K mais recente para obter uma vulnerabilidade de segurança crítica. Isso afeta os módulos XMLFM (AEM e IfBA), RM e PDFG. NPR-20625: NPR-21337.

### Feature Packs incluídos {#feature-packs-included}

#### Aplicativo AEM Forms {#aem-forms-app}

* Habilitação do suporte à tarefa de fluxo de trabalho do OSGi no aplicativo AEM Forms. CQ-4222638

### Pacotes OSGI e de conteúdo incluídos na 6.3.1.2 {#osgi-bundles-and-content-packages-included-in-6}

Lista de pacotes OSGi incluídos no AEM 6.3.1.2

[Obter arquivo](assets/do-not-localize/6_3_1_2-bundle-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.3.1.2

[Obter arquivo](assets/do-not-localize/6_3_1_2-content-package-list.txt)
O AEM Cumulative Fix Pack 6.3.1.1 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3 Service Pack 1 (6.3.1.0), em outubro de 2017.

Os principais destaques do AEM Cumulative Fix Pack são:

* Ativação da ação Publicar no Brand Portal para o formulário de esquema de metadados padrão.
* Alteração de comportamento na exibição de títulos no cartão Imagem para imagem com a propriedade dc: title definida como Cadeia de caracteres [] (vários campos).
* Renderização de tempo do lado do servidor substituída pelo componente de tempo-base.
* Habilitação da ação Publicar tags do AEM no Brand Portal a partir do console tagadmin/tagging.
* Publicação da API JSON para consumir fragmentos de conteúdo.
* O repositório integrado (Apache Jackrabbit Oak) foi atualizado para a versão 1.6.5.

### Ativos {#assets-11}

* Mapear dois campos com a mesma propriedade e com diferentes tipos de campo de propriedade gera um erro interno. NPR-19462: HF do CQ-4216828
* dc: title e dc: description não são alteradas para um valor de vários campos no CRXDE Lite. NPR-19570: HF do CQ-4209086
* O Dynamic Viewer carrega a representação de vídeo de qualidade mais baixa para testar a experiência de reprodução de vídeo no modo autor. NPR-19004
* A representação dinâmica não pode ser baixada para ativos que incluem espaços em seus nomes. NPR-19433: Hotfix do CQ-4211738
* Não é possível carregar a lista completa de páginas/ativos na exibição em Coluna usando o Chrome. NPR-19566: Hotfix do CQ-4214248
* A opção Publicar no Brand Portal não está disponível ao selecionar qualquer esquema, aspecto de pesquisa ou predefinição. NPR-19550
* Ao selecionar um ativo na exibição em coluna e clicar em editar, a página retorna um erro. NPR-20301: Hotfix do CQ-4224052
* A exibição da Expiração do ativo é desativada ao atravessar fusos horários positivos e negativos. NPR-20329: Hotfix do CQ-4219333

### Campaign {#campaign-2}

* Os componentes do controle deslizante do Campaign não aparecem quando a experiência Padrão é selecionada para uma campanha. NPR-19213

### Integração {#integration-7}

* O arquivo at.js personalizado não é publicado quando acessado com o usuário anônimo. NPR-19542: Hotfix do CQ-4219592
* O campo Mecanismo de direcionamento no assistente de configuração é definido como ContextHub (AEM), em vez de Adobe Target. NPR-19320: HF do CQ-4218465
* A seção Público-alvo fica corrompida ao criar a experiência. NPR-19110
* A caixa de diálogo Direcionamento não é exibida no modo de direcionamento quando um módulo de destino é editado e salvo mais de uma vez. NPR-19144: Hotfix do CQ-4216708
* Acesse as propriedades dos artigos que estão sendo definidos incorretamente na Adobe Digital Publishing Solution, na interface clássica. NPR-19367
* Comportamento incorreto de dobramento automático ao personalizar ofertas por meio do Campaign se os usuários tiverem acesso a várias áreas. NPR-19290: Hotfix do CQ-4218029

### Sites {#sites-11}

* Os valores suspensos de campo multicomposto não são preenchidos novamente devido à alteração do código no Sidekick.js após a atualização da instância para AEM 6.1SP2-CFP3. NPR-19450: HF do CQ-4194771
* WCMMode.EDIT não funciona para componentes direcionados no modo de criação. NPR-19387
* Publicação da API JSON para consumir fragmentos de conteúdo. NPR-19500
* A funcionalidade de negrito, itálico e sublinhado não funciona para campos do editor de rich text na caixa de diálogo do autor. NPR-19670: NPR-19718: Hotfix do CQ-4219088

### Mobile On-Demand {#mobile-on-demand-1}

* A renderização de problemas com o console de artigos do AEM como o uso de imagens em tamanho real o torna lento. NPR-19088

### Tradução {#translation-5}

* Não é possível gerar a visualização dos projetos de Tradução. NPR-19289

### Segurança {#security}

* Erro de conexão SSL. Não é possível estabelecer uma conexão segura com o servidor. NPR-19628

### Communities {#communities-9}

* O email é acionado em publicações de conteúdo com sites pré-moderados. NPR-20008
* As notificações por email não funcionam nas atividades relacionadas ao moderador em componentes publicados. NPR-19767: HF do CQ-4218060

### Plataforma {#platform-4}

* Problemas de estabilidade com a implantação do servidor de produção do AEM. NPR-19707
* O taglib personalizado que faz referência a tags implementadas como script não é encontrada após a atualização para o AEM 6.3. NPR-19087
* Correções de erros HTL do AEM 6.3.1. NPR-19161
* O campo Richtext não é editável nos componentes de vários campos. NPR-19604: Hotfix do Granite-16755
* O serviço Modelo de email da Adobe adiciona tags a modelos de usuário personalizados. NPR-19190
* Hotfix do Oak 1.6.5. NPR-19148

### Commerce {#commerce-5}

* O botão Iniciar fluxo de trabalho, após selecionar um editor de variação XF, não tem efeito. NPR-19642: Hotfix do CQ-4207796

### Projetos {#projects-2}

* Os editores de projeto não conseguem copiar/colar ativos na pasta de ativos do projeto. NPR-19619: Hotfix do CQ-4215321

### Gerenciamento de conteúdo da Web {#web-content-management}

* Na tela Implantação, as caixas de seleção correspondentes às páginas da Live Copy não podem ser marcadas ou desmarcadas. NPR-19518
* A edição em massa das propriedades da página não pode ser usada corretamente, pois atualmente todas as guias e campos estão disponíveis para edição em massa. NPR-19451
* As propriedades do OOTB e de alinhamento de imagem não são exibidas ao editar uma imagem na interface clássica. NPR-19488: HF do CQ-4217914

### Interface do usuário {#user-interface-4}

* Ao usar o navegador Google Chrome, os usuários não conseguem carregar a lista completa de páginas/ativos usando a exibição de coluna na interface para toque. NPR-19566: Hotfix do CQ-4214248

### Brand Portal {#brand-portal-1}

* Não é possível publicar ativos do AEM com comentários e anotações. NPR-19590: Hotfix do CQ-4218386
* Ativação da ação Publicar tags do AEM no Brand Portal a partir do console tagadmin/tagging. NPR-20271: Hotfix do CQ-4223948
* Corrija o campo &quot;ativado&quot; na interface do usuário de configuração do Brand Portal cloudservice. Hotfix do CQ-4211101
* Falha na replicação do formulário de pesquisa. Hotfix do CQ-4220080

## Forms {#forms-11}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-11}

#### Formulários adaptáveis {#adaptive-forms-4}

* Enviar para o fluxo de trabalho JEE não retorna o parâmetro de saída do lado JEE para o AEM e aciona o erro &quot;Ignorado porque o valor não é primitivo&quot;. NPR-20265
* Os formulários adaptáveis não permitem PDF como anexo no Safari. NPR-19625
* RestoreGuideState substitui o mapa customcontextproperty. CQ-4222877
* Ao configurar o Google reCaptcha usando o Cloud Service, em ambientes que exigem a configuração do org.apache.http.proxyconfigurator para conexões externas, chamadas POST não parecem passar pelo PROXY. NPR-20454
* Os formulários adaptáveis baseados em esquemas XSD enviam valores XML defeituosos para campos numéricos em instalações com locais que têm um separador decimal diferente de &quot;.&quot; resultando em erros. NPR-20444
* As configurações de proxy definidas para &quot;Configuração de proxy de componentes HTTP Apache&quot; não são respeitadas ao fazer solicitação HTTP em um servidor de terceiros. Problemas de tempo limite de conexão usando chamadas HTTP GET ou POST. NPR-20457, NPR-20456, NPR-20455, NPR-20451

#### Integração de dados de formulários {#forms-data-integration}

* Caracteres UTF-8 como saída do serviço SOAP não são copiados corretamente nos campos de formulários adaptáveis em localidades cujo idioma não seja o inglês. NPR-20238: NPR-20103

#### Gerenciamento de correspondência {#correspondence-management-1}

* Copiar e colar conteúdo do arquivo Word perde a cor e a fonte do conteúdo no Editor de texto. NPR-19521

#### Serviços do Assembler {#assembler-services}

* Discrepância entre os resultados do Acrobat e do AEM durante a verificação de conformidade de um documento para o formato PDFA-1b. NPR-19280

#### Fluxo de trabalho {#workflow-2}

* Etapa de Assinatura de fluxo de trabalho para permitir que chamadas http se conectem por meio do proxy. NPR-20529

#### Formulários HTML5 {#html-forms-4}

* Adicionado suporte para o evento preSubmit. NPR-20604

### Instalador do Forms JEE {#forms-jee-installer-10}

#### Gerenciamento de processos {#process-management-3}

* As guias de anexo de fluxo de trabalho, anotações e detalhes não funcionam no espaço de trabalho quando o formulário é maximizado/minimizado e salvo como rascunho ou encaminhado. NPR-20243
* O campo de texto multilinha (TextArea) não retém o caractere de nova linha ou quebra no texto após enviar dados no espaço de trabalho HTML. NPR-20085

#### Relatório de processo {#process-reporting}

* O relatório de processo não busca dados corretamente devido à Exceção de ponteiro nulo. NPR-19759

>[!NOTE]
>
>Instale o pacote incorporado do LiveCycle listado no artigo [Versões do AEM Forms](aem-forms-releases.md) para corrigir o problema.

#### Serviços padrão {#standard-services}

* O docConvertor não oferece suporte a transparências de mesclagem no PDF e falha ao produzir um PDF/A. NPR-16228: Hotfix do CQ-4214488

#### Núcleo {#core-2}

* Quando o AEM Forms Server em execução em uma configuração de cluster no aplicativo JBoss® é interrompido, o servidor do aplicativo é desconectado do banco de dados. Isso pode levar a problemas de corrupção de dados. NPR-19724

### Feature Packs incluídos {#feature-packs-included-1}

* O campo de esquema de metadados suspenso não pode ser tornado obrigatório, pois a validação de campo obrigatória está ausente para ativos. NPR-17882: FP do CQ-4208373

### Pacotes OSGI e de conteúdo incluídos na 6.3.1.1 {#osgi-bundles-and-content-packages-included-in-7}

Lista de pacotes OSGi incluídos no AEM CFP 6.3.1.1

[Obter arquivo](assets/do-not-localize/bundle-list.txt)

Lista de pacotes de conteúdo incluídos no AEM CFP 6.3.1.1

[Obter arquivo](assets/do-not-localize/content-package-list.txt)

O AEM Cumulative Fix Pack 6.3.0.2 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3, em abril de 2017.

Os principais destaques do AEM Cumulative Fix Pack são:

* Auditabilidade do controle de acesso do usuário
* Inclui a versão 1.6.2 do repositório integrado (Apache Jackrabbit Oak)
* Solução de problemas do resolvedor de recursos não fechado
* Configuração simplificada para serviços de conteúdo inteligente
* Solução de problemas de validação de fragmento de conteúdo
* Aprimoramento da capacidade de edição de esquemas de metadados em dispositivos híbridos
* Solução de problemas de sincronização no nível do componente em Live Copies
* Aprimoramento da usabilidade de páginas com muito conteúdo na exibição em coluna
* Aprimoramento da conformidade com a convenção de nomenclatura de página para páginas com títulos longos
* Aprimoramento da experiência de personalização de campanha na interface de toque
* Correções de vários problemas com sobreposição de projetos

### Plataforma {#platform-5}

* Hotfix do Oak 1.6.2. NPR-16993
* Ao abrir o Omnisearch usando um filtro, o caminho não é mais definido. NPR-17398: Hotfix do CQ-4204870
* Requisito de auditabilidade de alterações de permissão do usuário no AEM. NPR-17061
* Conexões remanescentes aos Serviços na nuvem do DM causam exceções de &quot;muitos arquivos abertos&quot;. CQ-4211407

### Ativos {#assets-12}

* Problemas de usabilidade ao configurar os serviços de conteúdo inteligente usando opções diferentes. NPR-18200: Hotfix do CQ-4201557
* Fuga de recursos em fluxos binários com armazenamento de dados S3. NPR-18041: Hotfix do CQ-4209506
* Ocorre um erro quando um arquivo de texto ASCII/UTF-8 codificado é carregado para o AEM Assets e a geração de miniaturas falha. NPR-18006: CFP do CQ-4209345
* O esquema de metadados padrão causa falha na validação do fragmento de conteúdo. NPR-17769: Hotfix do CQ-4211111
* Resolvedor de recursos não fechado em com.day.cq.dam.s7dam.common.analytics.impl.SiteCatalystReportRunner. NPR-17598: CFP do CQ-4209018
* Solicitação para criar vários agentes de replicação para publicar ativos no Brand Portal. NPR-17189
* A tarefa de revisão de ativos na pasta do idioma japonês não funciona. CQ-4204782
* Ocorre exceção de ponteiro nulo quando um ativo é movido da página de propriedades. CQ-4204251
* O AEM não rastreia referências subsequentes a um ativo na página de propriedades se ele estiver vinculado a um documento do InDesign várias vezes. CQ-4204186
* Problemas ao adicionar novas guias no formulário de esquema de metadados quando ele é editado no Chrome em dispositivos híbridos. CQ-4201810
* Quando ativos duplicados são carregados, a opção (excluir/manter) é aplicada a todos os ativos mesmo quando não está selecionada na caixa de diálogo duplicatas detectadas. CQ-4201673
* Uma exceção de ponteiro nulo é gerada quando uma pasta de ativos com mais de 150 referências de entrada é movida. CQ-4200981
* Em uma pasta de ativos baixada, se ocorrer um conflito ao extrair o conteúdo do arquivo ZIP, a opção padrão será exibida como Criar versão em vez de Manter ambos. CQ-97800
* Os usuários com permissões Somente leitura no aplicativo não podem visualizar o conteúdo do gerenciamento de conteúdo do AEM Mobile. NPR-17486: CFP do CQ-4209690
* O botão Criar catálogo não funciona na exibição em coluna no console Catálogo. CQ-4209952

### Sites {#sites-12}

* Problemas com a incorporação de componentes de imagem/vídeo por meio do atributo data-sly-resource. NPR-18182: CFP do CQ-4212100
* Componentes localizados modificados não são restaurados ao formulário original quando a herança é reaplicada em uma LiveCopy. NPR-18172: Hotfix do CQ-4211379
* Problemas com a navegação de uma página com muito conteúdo na exibição em Coluna da interface de toque. NPR-17799: Hotfix do CQ-4199611
* Resolvedor de recursos não fechado em `com.day.cq.wcm.core.impl.VersionManagerImpl`. NPR-17789: CFP do CQ-4211152
* O nome da página não é gerado por convenção para títulos de página longos. NPR-17633: Hotfix do CQ-4209056
* Problemas com a criação de página na interface do usuário para toque no AEM 6.3 implantada no JBoss® EAP 6.4. NPR-17589: Hotfix do CQ-4210137
* O provedor de status de fluxo de trabalho faz com que a instância seja bloqueada quando grupos aninhados estão presentes. NPR-17556: solicitação CFP do CQ-4202056
* Resolvedor de recursos não fechado nos seguintes objetos:

   * `com.day.cq.wcm.undo.impl.BinaryValueManagerImpl` NPR-17497: CFP do CQ-4208673
   * `com.day.cq.commons.impl.ThumbnailProviderManagerImpl` NPR-17495: CFP do CQ-4208668
   * `com.day.cq.wcm.workflow.impl.WcmWorkflowServiceImpl` NPR-17494: CFP do CQ-4208669
   * `com.day.crx.delite.impl.AuthHttpContext` NPR-17493: CFP do GRANITE-17404

### Integrações {#integrations-1}

* Correção de erros de componentes de pesquisa do AEM que podem ocorrer quando o AEM Day HTTP Client 3.1 OSGI é configurado com um Proxy que requer Autenticação Digest. NPR 18128: Hotfix do NPR-18029
* Problemas com a personalização de campanhas e experiências associadas por meio da interface clássica. NPR-18127: Hotfix do CQ-4211559
* Ao definir uma marca/zona para uma página raiz de um site, a herança depois de cancelada não pode ser restaurada para Áreas em subpáginas. NPR-17753: Hotfix do CQ-4210139

### Fluxo de trabalho {#workflow-3}

* Em um fluxo de trabalho não transitório, o histórico de processos e as alterações de metadados feitas antes de uma etapa de processo externo não são mantidos. NPR-17848: Hotfix do GRANITE-17757
* Os valores dos campos da caixa de diálogo de fluxo de trabalho não são mantidos no nó do item de trabalho. NPR-17734: Hotfix do CQ-4210369
* Ocorre um erro de data não analisável ao editar a tarefa na caixa de entrada. CQ-4208749

### Projetos {#projects-3}

* Correções para vários problemas de sobreposição de projetos. NPR-17733
* A reestruturação dos pods no módulo de projetos o torna menos configurável. CQ-4209859
* O caminho dos ativos muda para os respectivos sites localizados quando as páginas são adicionadas ao trabalho de tradução. CQ-4206007

### Segurança {#security-1}

* Problemas com o upload de imagens de avatar de usuários do LDAP. NPR-16561
* Solicite o uso de uma versão atualizada do servlet org.apache.sling.servlets.post (2.3.22) na API Apache Sling para evitar uma vulnerabilidade de XSS. NPR-18963

## Forms {#forms-12}

As correções do AEM Forms são entregues por meio de pacote complementar e outros instaladores de patches fornecidos com a versão. Para obter detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

Os principais destaques do AEM Forms são:

* Correções nos módulos de texto de gerenciamento de correspondência, nas visualizações de cartas e na inicialização programática da interface do gerenciamento de criação de correspondência.
* Correções da validação de PDF/A-1b, conversão de arquivos de imagem grandes em PDF e documentos PDF de idioma japonês no Gerador de PDF.
* Correções de usabilidade para o gerenciamento de correspondência, segurança de documentos e Forms Workflow.
* Adição de suporte para capturar eventos de auditoria do campo de assinatura de rabisco.

### Pacote complementar do Forms {#forms-add-on-package-12}

**Gerenciamento de correspondência**

* Ao editar um fragmento de gerenciamento de correspondência, o editor de texto exibe condições em linha juntamente com o texto processado. CQ-4211930
* Ao criar uma carta de gerenciamento de correspondência, a descrição da carta não é salva. NPR-18089
* A margem extra acima e abaixo de uma lista com marcadores é visível no editor de texto, mas não na representação de HTML e PDF. NPR-18126
* Quando o envio de HTML usa o método POST, a interface de criação de correspondência não é iniciada. NPR-18202
* Quando um módulo de texto é salvo e uma expressão no módulo de texto não contém tags de expressão de abertura ou fechamento, nenhuma mensagem de erro é exibida. O módulo de texto exibe uma mensagem de erro e não é renderizado na correspondência. NPR-18535
* Quando um novo conteúdo é adicionado ou a tecla Enter é pressionada, uma tag div é adicionada ao módulo de texto. NPR-18240

**Assembler**

* Ao validar um documento PDF para conformidade com PDF/A-1b, o AEM Forms retorna um erro de validação: PDFA_CONTENT_003_DEVICE_DEPENDENT_COLOR_USED. O documento PDF não retorna o erro quando validado com o Adobe Preflight e software de terceiros. NPR-18011
* Ao validar documentos de PDF para conformidade com PDF/A-1b, o AEM Forms retorna um erro de validação: O campo de formulário tem várias aparências. Os documentos PDF são compatíveis com PDF/A-1b. NPR-18013

**Pasta monitorada**

* Ao selecionar para processar arquivos usando um fluxo de trabalho, enquanto uma pasta monitorada é criada, o menu suspenso de seleção do modelo de fluxo de trabalho aparece truncado. NPR-17566

**Formulários HTML5**

* O AEM Forms não captura eventos de auditoria do campo de assinatura de rabisco. NPR-15286

**Gerenciador do Forms**

* A interface do AEM Forms lista todos os ativos na ordem mais antiga. Os usuários não podem reordenar os ativos na ordem mais recente. NPR-18450

**Referência da API Java™**

Adição do JavaDocs à classe com.adobe.livecycle.content. NPR-18468

### Instalador do Forms JEE {#forms-jee-installer-11}

**Gerador de PDF**

* Falha do serviço Gerador de PDF ao converter imagens com mais de 100 MB em documentos PDF. Ref# CQ-4208628
* Ao usar o serviço Gerador de PDF com um OCR de idioma japonês, um PDF invertido é gerado. NPR-17602

**Gerenciamento de processos**

* A variável TaskContext não é preenchida para processos do AEM Forms. NPR-18199

**Segurança de documentos**

* O Microsoft® Excel e o Microsoft® PowerPoint demoram mais para abrir os documentos protegidos com o AEM Document Security Extension for Microsoft® Office. CQ-4212358
* Quando uma nova política é criada e uma política com o mesmo nome existe, ocorre um erro interno do servidor. NPR-18247

## Feature Packs incluídos {#feature-packs-included-2}

* Requisito de auditabilidade de alterações de permissão do usuário no AEM. NPR-17061

O AEM Cumulative Fix Pack 6.3.0.1 é uma atualização importante que inclui várias correções internas e de clientes desde a disponibilização geral do AEM 6.3, em abril de 2017. Os principais destaques do AEM Cumulative Fix Pack são:

* Melhorias nas seguintes áreas:

   * Componentes dos Fragmentos de conteúdo, Sites e Editor de Rich Text, Editor de regras e do Editor de modelos
   * Análise social e logon no Facebook Social
   * Configurar e iniciar trabalhos de Tradução
   * Tempo de resposta para acessar notificações em Comunidades sociais
   * Exibição de tarefas de revisão no repositório DAM

* Oferece a opção de validação no Gerenciador de pacotes para detectar conflitos entre sobreposição e CFP

## Instruções de download para o CFP por meio da Distribuição de softwares {#download-instructions-for-cfp-via-package-share}

Você pode baixar o pacote CFP diretamente da [Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html) ou executar as seguintes etapas:

1. Abra a [Distribuição de software](https://experience.adobe.com/downloads). Você precisa de uma Adobe ID para fazer logon na Distribuição de softwares.
1. Clique em **[!UICONTROL Adobe Experience Manager]** disponível no menu de cabeçalho.
1. Clique no nome do pacote, selecione **[!UICONTROL Aceitar termos do EULA]** e clique em **[!UICONTROL Download]**.

## Instruções de instalação {#installation-instructions}

Esta seção aborda os requisitos e as etapas para instalar o CFP.

### Antes de instalar {#before-you-install}

>[!NOTE]
>
>Os Feature Packs opcionais fornecidos pela Adobe depende da versão de lançamento e do Cumulative Fix Pack. Se você tiver algum Feature Pack instalado, entre em contato com a [equipe de Atendimento ao cliente do AEM](https://helpx.adobe.com/br/contact/enterprise-support.ec.html) para validar a compatibilidade com este Cumulative Fix Pack do AEM 6.3.

>[!NOTE]
>
>É recomendável executar a validação em cada novo pacote de instalação antes de tentar instalá-lo. A pré-validação analisa e relata os erros encontrados antes da instalação, além de avisar os usuários sobre esses erros de forma proativa.
>
>Acesse a documentação da opção Validar em [https://docs.adobe.com/content/docs/pt-BR/aem/6-3/administer/content/package-manager.html#Package%20Validator](https://docs.adobe.com/content/docs/pt-BR/aem/6-3/administer/content/package-manager.html#Package%20Validator)

* O AEM 6.3.3.0 é um pré-requisito do CFP. Visita [Atualização da documentação](https://docs.adobe.com/docs/en/aem/6-3/deploy/upgrade.html) para obter instruções detalhadas sobre como atualizar uma instalação de AEM para AEM 6.3.
* Em uma implantação de cluster usando RDBMK ou MongoDB, o pacote CFP pode ser instalado em qualquer uma das instâncias do Autor que usa o Gerenciador de pacotes.
* Antes de instalar o Pacote de correções cumulativo, verifique se fez um instantâneo ou um backup da instância do AEM.
* Não há suporte para a desinstalação do CFP.

### Adicionar novos loggers {#adding-new-loggers}

Para configurar o registro em log do nível de depuração e recuperar um registro de atividade durante a instalação de SPs/CFPs, siga as etapas abaixo:

* Você pode adicionar um novo agente de log no local padrão [http://localhost:4502/system/console/slinglog](http://localhost:4502/system/console/slinglog) com as propriedades abaixo:

   * Nível de registro: depuração
   * Aditivo: falso
   * Arquivo de log: logs/activity.log
   * Logger: org.apache.jackrabbit.vault.packaging.impl.ActivityLog

O activity.log será criado na pasta crx -quickstart /logs.

### Instale o Cumulative Fix Pack pela Distribuição de softwares {#install-the-cumulative-fix-pack-via-package-share}

Execute as seguintes etapas para instalar o Cumulative Fix Pack em uma instância do AEM 6.3 existente:

1. Clique no link [Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip) para baixar o pacote.

1. Abra [Gerenciador de pacotes](http://localhost:4502/crx/packmgr/index.jsp) e clique em **[!UICONTROL Fazer upload de pacote]** para fazer upload do pacote.

1. Selecione o nome do pacote e clique em **[!UICONTROL Instalar]**.

### Instalação automática {#automatic-installation}

O CFP pode ser instalado automaticamente em uma instância em execução das seguintes maneiras:

* Coloque o pacote em `../crx-quickstart/install` enquanto o servidor estiver em execução. O pacote é instalado automaticamente.
* Use a [API HTTP a partir do Gerenciador de pacotes](https://helpx.adobe.com/br/experience-manager/6-3/sites/administering/using/package-manager.html) - certifique-se de usar `cmd=install&recursive=true` - para instalar os pacotes aninhados.

### Validar instalação {#validate-installation}

1. A página Informações do produto ( `/system/console/ productinfo`) agora deve mostrar a cadeia de caracteres da versão atualizada &quot;Adobe Experience Manager, versão 6.3.3.8&quot; em Produtos instalados.
1. Todos os pacotes OSGI são ATIVOS ou FRAGMENTOS no Console OSGi (Use o console da Web: `/system/console/bundles`).

>[!NOTE]
>
>Ao instalar o pacote com êxito, uma mensagem informativa é exibida nos registros de erro, indicando que o pacote de conteúdo foi instalado com êxito, como &quot;Pacote de conteúdo **AEM-6.3.3-Cumulative-Fix-Pack-7** instalado com êxito&quot;.

>[!NOTE]
>
>A partir do AEM 6.3.3.1, o nível de log no Jackrabbit FileVault mudou de INFO para DEBUG na maioria das mensagens. Para obter registros de instalação de um pacote de conteúdo instalado no AEM 6.3.3.1 ou mais recente, ative o nível de registro DEBUG para org.apache.jackrabbit.vault.packaging.impl.

### Instalar o AEM Forms {#install-aem-forms}

>[!NOTE]
>
>Pule esta seção se não estiver usando o AEM Forms.

#### Instalar complemento do AEM Forms {#install-forms}

1. Verifique se você instalou o pacote AEM 6.3.3.x CFP.
1. Baixe o pacote complementar do Forms correspondente listado em [Versões do AEM Forms](aem-forms-releases.md) para seu sistema operacional.
1. Instale o pacote complementar do Forms conforme descrito em [Instalação dos pacotes complementares do AEM Forms](https://helpx.adobe.com/br/experience-manager/6-3/forms/using/installing-configuring-aem-forms-osgi.html).

#### Instalar pacote do AEM Forms JEE {#install-aem-forms-jee-bundles-package}

As correções no JEE do AEM Forms são entregues por meio de um instalador separado. Para obter informações sobre como instalar um CFP no AEM Forms no JEE, consulte [Instalação do CFP no JEE do AEM Forms](install-cfp-aem-forms-jee.md).

#### Instalador do Designer do Forms {#designer-installer}

1. Para instalar a atualização, execute o arquivo Designer 6.2.0_&lt;Language>_Cumulative_QF.msp.
1. Na tela de boas-vindas, clique em **atualizar**. A instalação é iniciada.
1. Depois que a instalação for concluída, clique em **concluir**.

## Configurações para o AEM Forms JEE (JBoss® EAP) {#configuration-settings-for-aem-forms-jee-jboss-eap}

>[!NOTE]
>
>Se estiver instalando versões 6.3.3.0 ou posteriores, execute o procedimento abaixo para definir as configurações do servidor de aplicativos JBoss®. Se estiver instalando o 6.3.3.0 no AEM Forms Server em execução nos servidores de aplicativos Oracle WebLogic ou IBM® WebSphere, nenhuma configuração adicional será necessária. Para obter mais detalhes, consulte [Notas de versão do AEM 6.3.3.0](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions.html?lang=pt-BR).

## Atualizações de configuração para a integração do Search&amp;Promote {#configuration-updates-for-search-promote-integration}

Com o AEM Cumulative Fix Pack 6.3.0.2 e versões posteriores, a configuração do OSGi usada na integração do Search&amp;Promote é a **Configuração de proxy dos componentes HTTP do Apache**. A configuração Proxy do Day Commons HTTP Client 3.1 não é mais usada.

## Problemas conhecidos {#known-issues}

* Os seguintes erros e avisos podem ocorrer durante a instalação do AEM CFP 6.3.3.x e podem ser ignorados com segurança:

   * &#42;AVISO&#42; [OsgiInstallerImpl] org.apache.jackrabbit.vault.packaging.impl.InstallHookProcessorImpl Hook /META-INF/vault/hooks/cloudservices-wfchangeinstallhook-0.0.2-jar-with-dependencies.jar acionou uma exceção de tempo de execução.
   * &#42;ERRO&#42; [OsgiInstallerImpl] com.adobe.cq.social.cq-social-jcr-provider [com.adobe.cq.social.provider.jcr.impl.SpiSocialJcrResourceProviderImpl(2174)] Tempo limite aguarda que o reg altere para conclusão não registrada. CQ-4209974.
   * org.apache.sling.engine.impl.SlingRequestProcessorImpl Serviço ServletResolver ausente, não é possível fazer solicitações de recurso, envio do status 503
   * com.day.cq.wcm.mobile.core.MobileUtil isMobileResource: não é possível verificar o recurso [/bin/receive], gerenciador de página indisponível
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver: a chamada do manipulador de erros resultou em um erro
   * org.apache.sling.servlets.resolver.internal.SlingServletResolver Erro original nulo
   * org.apache.sling.engine.impl.DefaultErrorHandler Falha no manipulador de erros:java.io.IOException
   * &#42;ERRO&#42; [FelixDispatchQueue] com.day.cq.dam.cq-dam-core FrameworkEvent ERROR (org.osgi.framework.ServiceException: fábrica de serviço retornou nulo. (Componente: com.day.cq.dam.handler.standard.ps.PostScriptHandler))

**Brand Portal**

* A partir da versão 6.3.1.2, o botão Publicar no Brand Portal para coleções inteligentes foi removido.

**Interface do usuário**

>[!NOTE]
>
>Caso seja afetado por qualquer um desses problemas, entre em contato com o [Atendimento ao cliente do AEM](https://helpx.adobe.com/br/contact/enterprise-support.ec.html).

* A alta utilização da CPU é observada devido a muitas solicitações na funcionalidade do Admin Search. NPR-24229
* PathField não está selecionado no pathBrowser ao reabrir o componente. NPR-24177

## Configurações necessárias para o NPR-27692 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>Esta configuração se aplica ao CFP 6.3.3.2 e posterior. Ela direciona para a atualização das propriedades da delegação de inicialização no arquivo de propriedades `sling` .

Para atualizar as alterações no adobe- LiveCycle® -author.ear/ cq .war manualmente, siga as etapas mencionadas abaixo:

* Interrompa o servidor AEM.
* Acesse adobe-livecycle-cq-author.ear/cq.war
* Abra adobe-livecycle-cq-author.ear/cq.war/WEB-INF/web.xml para edição:

   * Atualize o valor param-name **sling.bootdelegation.ibm** com:

   * com.ibm.xml.&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat

   * Após a alteração acima, init-param deve ser semelhante a:

   * &lt;init-param>
&lt;param-name>sling.bootdelegation.ibm&lt;/param-name> &lt;param-value>com.ibm.xml&#42;,com.ibm.crypto.pkcs11impl.provider,com.ibm.pkcs11,com.ibm.pkcs11.nat&lt;/param-value>
&lt;/init-param>

* Desinstale o arquivo de arquivamento empresarial (EAR) anterior do servidor de aplicativos WebSphere® e instale o arquivo EAR atualizado seguindo as etapas da Seção 10.2 do [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)
* Salve o arquivo e reinicie o servidor. [https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf](https://helpx.adobe.com/pdf/aem-forms/6-3/install-single-server-websphere.pdf)

## Configurações necessárias para o NPR-23208 {#configuration-settings-required-for-npr-1}

>[!NOTE]
>
>Esta configuração se aplica à versão 6.3.2.2 e posterior. Ela direciona para a atualização manual das políticas de Listas de controle de acesso (ACL) por meio do CRX-DE, pois as ACLs não são atualizadas por meio da instalação do CFP devido ao acHandling &quot;merge_preserve&quot;.

**Documentação para adicionar políticas de ACL manualmente**

Para atualizar as políticas de ACL, adicione os Controles de acesso abaixo por meio do CRX-DE:

`1)` No caminho &quot;/content&quot;
`a)` Principal: reference-adjustment-service Tipo: permitir privilégios: jcr:read , jcr:modifyProperties Restrições : rep:glob=&quot;/&#42;/jcr:content&quot;
`b)` Principal: reference-adjustment-service Tipo: permitir privilégios: jcr:read , jcr:modifyProperties Restrições : rep:glob=&quot;/&#42;/jcr:content/&#42;&quot;

`2)` No caminho &quot;/content/usergenerated&quot;
`a)` Principal: reference-adjustment-service Tipo: permitir privilégios: jcr:write

`3)` No caminho &quot;/etc&quot;
`a)` Principal: reference-adjustment-service Tipo: permitir privilégios: jcr:read , jcr:modifyProperties Restrições : rep:glob=&quot;/&#42;/jcr:content&quot;
`b)` Principal: reference-adjustment-service Tipo: permitir privilégios: jcr:read , jcr:modifyProperties Restrições : rep:glob=&quot;/&#42;/jcr:content/&#42;&quot;

## Configurações necessárias para o NPR-19450 {#configuration-settings-required-for-npr-2}

>[!NOTE]
>
>Esta configuração se aplica ao CFP 6.3.1.1 e posterior.

**Configure a propriedade CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL.**

A propriedade controla a profundidade máxima da subárvore do nó sob o nó da página ` /jcr:content`, até a qual os nós presentes no repositório devem ser usados para obter as propriedades da página. Qualquer nó presente abaixo da profundidade especificada nessa propriedade é ignorado.

O valor padrão é 1. O valor pode ser substituído ao sobrepor o arquivo constantes.js (`/libs/cq/ui/widgets/source/constants.js`) cancelando o comentário da propriedade CQ.PAGE_PROPERTIES_MAX_RECURSION_LEVEL e atribuindo o valor necessário ( a profundidade máxima sob /jcr:content da página até o qual os dados das propriedades da página são armazenados).

**Se o usuário precisar criar várias variantes de páginas, de modo que o número de nós no nó /jcr:content da página se torne maior que 1000, use as seguintes etapas para fazer alterações de configuração:**

* Configure os resultados máximos da propriedade JSON do Apache Sling
* Get Servlet usando `/system/console/ configMgr`
* Defina o valor com um número >1000 (que é o padrão atual) de modo que ele seja maior que o número total de nós na subárvore / jcr:content até a profundidade configurada acima.

Isso permite que o sling GET servlet retorne todos os nós necessários.

## Uber Jar {#uber-jar}

O Uber Jar da versão 6.3.3.8 está disponível em [repositório do Adobe Public Maven](https://repo.adobe.com/nexus/content/groups/public/com/adobe/aem/uber-jar/6.3.3.8/).

Para usar o Uber Jar em um projeto Maven, consulte o artigo [Como usar o Uber jar](https://helpx.adobe.com/br/experience-manager/6-3/sites/developing/using/ht-projects-maven.html) e inclua a seguinte dependência no POM do projeto:

```TXT
<dependency>
 <groupId>com.adobe.aem</groupId>
 <artifactId>uber-jar</artifactId>
 <version>6.3.3.8</version>
 <classifier>apis</classifier>
 <scope>provided</scope>
</dependency>
```

## Recursos removidos/obsoletos {#deprecated}

Esta seção lista os recursos e funcionalidades removidos ou descontinuados do AEM 6.3.

| Área | Destaque | Substituição | Versão |
|----|-----|-----|-----|
| Integração do Assets e da Adobe Creative Cloud | [O compartilhamento de pastas do AEM para a Creative Cloud](https://helpx.adobe.com/br/experience-manager/6-3/sites/administering/using/creative-cloud.html) foi introduzido no AEM 6.2 como uma forma de fornecer aos usuários criativos acesso aos ativos do AEM. Uma nova funcionalidade lançada no aplicativo da Creative Cloud, o Adobe Asset Link, fornece uma experiência de usuário melhor e acesso avançado a ativos do AEM diretamente do Photoshop, InDesign e Illustrator.<br /> A Adobe não fará mais aprimoramentos no recurso de compartilhamento de pastas. Embora o recurso esteja incluído no AEM, os clientes são aconselhados a usar a substituição. | Adobe Asset Link ou Aplicativo de desktop. Para obter mais informações, consulte o artigo [Integração da AEM Creative Cloud](https://helpx.adobe.com/br/experience-manager/6-3/assets/using/aem-cc-integration-best-practices.html). | AEM 6.3.3.x |

## Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-1}

Os seguintes documentos de texto listam os pacotes OSGi e os Pacotes de conteúdo incluídos no CFP.

* [Lista de pacotes OSGi incluídos no AEM 6.3.3.8](assets/do-not-localize/list_of_osgi_bundlesincludedin6338.txt)

* [Lista de pacotes de conteúdo incluídos no AEM 6.3.3.8](assets/do-not-localize/list_of_content_packageincludedin6338.txt)

>[!MORELIKETHIS]
>
>* [Versões e atualizações do AEM](https://experienceleague.adobe.com/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates.html?lang=pt-BR)
>* [Página de hotfixes do AEM 6.3](https://helpx.adobe.com/br/experience-manager/kb/aem63-available-hotfixes.html)
>* [Notas de versão do AEM 6.3](https://docs.adobe.com/docs/en/aem/6-3/release-notes.html)
>* [Página do produto AEM](http://www.adobe.com/br/solutions/web-experience-management.html)
>* [Documentação do AEM 6.3](https://docs.adobe.com/content/docs/br/aem/6-3.html)
>* Inscreva-se em [Atualizações de produtos de prioridade da Adobe](https://www.adobe.com/subscription/priority-product-update.html)
