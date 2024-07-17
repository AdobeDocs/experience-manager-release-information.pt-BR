---
title: Pacote de correções cumulativo do AEM 6.2
description: Saiba mais sobre as notas de versão do Pacote de correções cumulativo do AEM 6.2.
exl-id: f1c2d4ff-590b-46b5-b2b1-e2b5141f7cc0
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: ht
source-wordcount: '21082'
ht-degree: 100%

---

# Notas de versão do Pacote de correções cumulativo do AEM 6.2{#release-notes-aem-cumulative-fix-pack}

<!-- TBD: Should we keep this article published after AEM 6.2 content is archived by way of UGP-1894. If an AEM version is EOL should we discard its details RNs but still retain its docs?
-->

## Informações da versão {#release-information}

| **Produto** | Adobe Experience Manager |
|---|---|
| **Versão** | 6.2 |
| **Versão** | Cumulative Fix Pack 6.2 SP1-CFP20 |
| **Pré-requisitos** | [AEM 6.2 Service Pack 1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) |
| **Disponibilidade geral** | 6 de junho de 2019 |

### Cumulative Fix Pack {#cumulative-fix-pack}

A Adobe apresentou um modelo de entrega única para lançar correções. Em vez de lançar hot fixes para problemas individuais, a Adobe agora lança um Cumulative Fix Pack (CFP) mensalmente (sujeito à aprovação em verificações de qualidade). Um CFP é um pacote de conteúdo agregado com várias correções. Os CFPs incluem principalmente correções de erros, mas também podem incluir Pacotes de recursos. Eles têm as seguintes vantagens em relação às versões de hotfixes individuais:

* Natureza cumulativa (por exemplo, um CFP contém correções fornecidas por CFPs anteriores)
* Maior garantia de qualidade
* Instalação simplificada (o usuário instala um CFP como pacote único e sem dependências, exceto no caso do pacote de serviços mais recente)

Para obter mais informações sobre o CFP e outros tipos de versões, consulte [Veículo de versão de manutenção](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

## Sobre a versão {#about-the-release}

O Pacote de correções cumulativo do AEM 6.2 SP1-CFP20 é o último pacote de correções cumulativo para o AEM 6.2. É uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilidade geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

>[!CAUTION]
>
>Aplicar o CFP sem validar a compatibilidade entre os pacotes de recursos instalados pode resultar em falha do sistema ou perda de configurações personalizadas, o que pode exigir a restauração do backup para solucionar o problema.

>[!NOTE]
>
>* Um novo pacote de Sling `discovery- api`, o Johnzon 1.0.0, vem com o pacote de correções cumulativo do AEM 6.2 SP1-CFP10. Além disso, um sling-discovery para usuário de serviço foi adicionado com os privilégios de leitura e gravação para o nó */var/discovery* no repositório CRX.
>
>* O pacote de email do Apache Commons **org.apache.commons/commons-email/1.5** foi adicionado, substituindo **com.day.commons.osgi.wrapper/com.day.commons.osgi.wrapper.commons-email/1.2.0-0002**.
>
>* A Adobe recomenda a implantação do CFP por meio da pasta de instalação para clientes que têm muitos usuários na instância do AEM.
>

## Problemas incluídos {#issues-included}

Esta seção lista todos os problemas e hotfixes incluídos no CFP atual.

Além disso, esse CFP inclui hotfixes fornecidos em [cumulative fix packs anteriores](#previous).

### Integração {#integration}

* Backport de várias melhorias na personalização de direcionamentos de campanhas. NPR-29163: Hotfix do CQ-4264126
* com.day.cq.personalization.impl.TeaserResourceEventHandler entra em um loop infinito e atualiza os nós em instâncias de publicação. NPR-28561: Hotfix do CQ-4263096

### DAM - Geral {#dam-general}

* Não é possível exibir/ocultar o botão de replicação para usuários não administradores em pastas específicas de DAM. NPR-29026: Hotfix do CQ-4265361

### Vulnerabilidade {#vulnerability}

* A estrutura de proteção do CSRF não está funcionando com formulários fundamentais do AEM. NPR-28612: hotfix do GRANITE-22231

### Forms {#forms}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package}

>[!NOTE]
>
>Para clientes do AEM Forms, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer pacote de serviços, pacote de correções cumulativo ou pacote de recursos do AEM.

>[!NOTE]
>
>Os pacotes complementares do AEM Forms ajudam a alinhar a funcionalidade dos AEM Service Packs e dos Cumulative Fix Packs. Sendo assim, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Service Pack, Cumulative Fix Pack ou Feature Pack do AEM.

#### Formulários adaptáveis {#adaptive-forms}

* Problemas de usabilidade com o componente de rabisco para dispositivos iOS 12.1. NPR-29082: Hotfix do CQ-4261765

#### Forms - Segurança de documentos {#forms-document-security}

* A verificação de todas as assinaturas em um PDF usando o PDF Advanced Electronic Signatures (PAdES) gera InvalidOperationException. NPR-27848: Hotfix do CQ-4244837

#### Forms - Correspondência {#forms-correspondence}

* Ao visualizar a correspondência como PDF, o campo de texto colocado na página principal não respeita o valor inserido na guia de dados ou a vinculação de dados especificada. NPR-29239: hotfix do CQ-4266856.

#### Forms - Comunicação interativa {#forms-interactive-communication}

* Ao adicionar um apóstrofo, os campos preenchidos previamente na correspondência aparecem como caracteres ASCII em vez de alfabetos regulares. NPR-28863: Hotfix do CQ-4262900

### Instalador do Forms no JEE {#forms-jee-installer}

* Nenhuma nova correção para o instalador do AEM Forms no JEE.

## Correções e Feature Packs incluídos em Cumulative Fix Packs anteriores {#hotfixes-and-feature-packs-included-in-previous-cumulative-fix-packs}

### Cumulative Fix Pack 19 {#cumulative-fix-pack-1}

O AEM Cumulative Fix Pack 6.2 SP1-CFP19 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Os principais destaques desse Cumulative Fix Pack são:

* Suporte habilitado para a API 3.0 do MS® Translator para AEM 6.2
* Mensagem de log adicionada após a instalação bem-sucedida do pacote para todos os SPs, CFPs e HFs.

### Ativos {#assets}

* Não é possível renomear a pasta do DAM se a permissão Editar ACL estiver ausente. NPR-27555: hotfix do CQ-104652
* Ferramenta do editor de predefinição de imagem não está responsiva na versão 6.2.1 CFP 17 e posterior. NPR-28147: hotfix do CQ-4261041

### Sites {#sites}

* O Verificador de links não conclui o trabalho, fica preso a links que não respondem. NPR-27373: Hotfix do CQ-4256030
* O arquivo de segmento não é carregado corretamente devido a um caminho raiz adicional que quebra o caminho do segmento. NPR-28014: Hotfix do CQ-4260332

### Integração {#integration-1}

* O cancelamento da herança da Live Copy não funciona corretamente em contêineres direcionados. NPR-28129: Hotfix do CQ-4259813
* As `cq:actions` não são consideradas para um componente direcionado. NPR-27616: hotfix do CQ-4257497

* A exibição de ícone para quebra de herança não é coerente. NPR-27671: hotfix do CQ-4257779

### Felix {#felix}

* O detalhe do componente do console da Web falha com 500 após a instalação do CFP 18 na instância do AEM 6.2 SP1. NPR-28350: Hotfix do CQ-4261095

### Tradução {#translation}

* Habilitação do suporte para o serviço MS® Translator no AEM 6.3 após a atualização do MS® Translator para a API v3.0. NPR-28123: hotfix do CQ-4259096

### IU - Foundation {#ui-foundation}

* O Calendário do Sites OOTB mostra datas incorretas. NPR-28392

### Granite {#granite}

* O dicionário não é invalidado para pacotes de recursos que usam `sling:basename`. NPR-27624

### Sustentação {#sustenance}

* Os registros de atividades do gerenciador de pacotes devem ser extraídos em um arquivo de registro separado. NPR-27323: hotfix do Granite-14866
* Uma frase/texto/linha(s) de registro padronizada(s) no error.log será exibida quando a instalação for concluída. NPR-27835
* O plugin do pacote do Granite está escolhendo a dependência de uma versão inferior de org.apache.sling.i18n. Hotfix do CQ-4263245
* O pacote com.adobe.cq.com.adobe.cq.ui.commons é excluído ao instalar o CFP mais recente após o 6.2SP1-CFP15. Hotfix do CQ-4258808

### Forms {#forms-1}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-1}

#### Formulários adaptáveis {#adaptive-forms-1}

* Vulnerabilidade de injeção XML com o AEM Forms. NPR-27843: Hotfix do CQ-4257315

### Instalador do Forms no JEE {#forms-jee-installer-1}

* Nenhuma nova correção para o instalador do AEM Forms no JEE.

### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included}

O texto seguinte documenta a lista de pacotes OSGi e os pacotes de conteúdo incluídos no CFP.

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP19

[Obter arquivo](assets/do-not-localize/cfp19_osgi_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP19

[Obter arquivo](assets/do-not-localize/cfp19_content_packages.txt)

### Cumulative Fix Pack 18 {#cumulative-fix-pack-2}

O AEM Cumulative Fix Pack 6.2 SP1-CFP18 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Os principais destaques desse Cumulative Fix Pack são:

* Inclusão de suporte no CommandLineProcess do DAM para eliminar o processo de longa duração.
* Correção de vazamento de sessão em ReplicationEventListener.
* Adição de suporte de redirecionamento ao componente da página principal.

### Ativos {#assets-1}

* Os processos de `Camera RAW` ficam presos durante períodos de assimilação massiva, o que eventualmente bloqueia todo o processamento de fluxo de trabalho. NPR-26990: hotfix do NPR-23860
* A funcionalidade de download usa o AEM Assets por meio do servlet de download de ativo, permitindo que usuários anônimos baixem todos os ativos. NPR-27054, Hotfix do CQ-4254732
* Caracteres especiais aparecem quebrados na linha de assunto dos modelos de email no AEM. NPR-26470: Hotfix do CQ-4252368

### Sites {#sites-1}

* Devido ao comportamento incorreto da classe ConfigPostProcessor, a suspensão da imagem principal remove o tipo de mixagem `cq:LiveRelationship` da página secundária. NPR-26745: hotfix do CQ-4254163
* Adição de suporte de redirecionamento ao componente da página principal. NPR-26576: hotfix do CQ-110529
* Migração do hub de contexto para `jQuery` 3. NPR-26956: hotfix do CQ-4255472
* Os campos de entrada de âncora aparecem fora da seção visível do navegador na caixa de diálogo até serem maximizados. NPR-26852: Hotfix do CQ-4255019
* Recurso de copiar e colar texto inserindo &lt;br> indesejado no fragmento de conteúdo. NPR-26660: Hotfix do CRTE-151
* O administrador clássico do site não renderiza a lista no painel direito de algumas páginas. NPR-27247: Hotfix do CQ-4251621
* (Interface Clássica) As tentativas de mover/renomear páginas geram o erro: &quot;Ocorreu um erro ao mover a página.&quot; NPR-27179: Hotfix do CQ-4235907

### Integração {#integration-2}

* com.day.cq.personalization.impl.BrandsRetriever percorre toda a árvore para coletar as marcas disponíveis. NPR-27060: Hotfix do CQ-4255790

### WCM - Componentes do Foundation {#wcm-foundation-components}

* Problema da funcionalidade Pesquisar com o componente de lista do Foundation. NPR-26817: Hotfix do CQ-4250324

### Plataforma {#platform}

* Devido ao caractere especial traço, o editor está tendo problemas para limpar o cache. NPR-27199: Hotfix do CQ-4242790

### Granite {#granite-1}

* O Validador de pacotes não valida pacotes incluídos no CFP/SP. NPR-26775: Hotfix do Granite-22825

### Replicação {#replication}

* Vazamento da Sessão JCR no ReplicationListener. NPR-27063: Hotfix do CQ-4232088

### Forms {#forms-2}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-2}

* Não há novas correções no pacote complementar do AEM Forms.

### Instalador do Forms no JEE {#forms-jee-installer-2}

* Nenhuma nova correção para o instalador do AEM Forms no JEE.

#### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-1}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP18

[Obter arquivo](assets/do-not-localize/62cfp18updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP18

[Obter arquivo](assets/do-not-localize/content_package_62sp1_cfp18.txt)

### Cumulative Fix Pack 17 {#cumulative-fix-pack-3}

O AEM Cumulative Fix Pack 6.2 SP1-CFP17 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Os principais destaques desse Cumulative Fix Pack são:

* Inclusão de suporte a URLs sem extensão do site em at-integration.js
* Remoção do importador de enquetes S7 da configuração do serviço na nuvem S7.
* Alterações na exibição de público-alvo para dar suporte à estrutura de pastas na implementação de vários locatários.
* Atualização para jqueryui clientlib v1.12.1.

### Ativos {#assets-2}

* A inicialização de workflows da interface do usuário do Assets requer que o usuário tenha permissões de gravação/exclusão/alteração. NPR-25688: Hotfix do CQ-4250140
* Os botões Publicar e Cancelar publicação permanecem visíveis mesmo para os usuários sem permissões de &quot;replicação&quot;. NPR-25094
* (Fluxo de trabalho) O fluxo de trabalho do Smart Tag Asset não é processado pela configuração de proxy do AEM. NPR-25915: Hotfix do CQ-4248202
* Remoção do importador de enquete S7 da configuração do serviço na nuvem S7. NPR-25239: Hotfix do CQ-95236

### Sites {#sites-2}

* Workflows iniciados pelo Editor -> Informações da página contêm o caminho de contexto na carga. NPR-26389: Hotfix do CQ-76804
* (Linkchecker externo) Links https inválidos são exibidos como links válidos. NPR-25541: hotfix do CQ-4201333
* (Interface clássica) Ao criar uma página autônoma em uma Live Copy, a página é criada como uma live copy. NPR-25610: Hotfix do CQ-4249801
* Problemas com recursos de publicação associados ao componente Importador de design quando uma página é ativada. NPR-25638: Hotfix do CQ-102532
* A barra de ferramentas do RTE (Editor Rich Text) cobre a lista selecionada. NPR-25165: hotfix do CQ-4248948
* Migração do hub de contexto para jQuery 3. NPR-25059: hotfix do Granite-19902
* Para um componente parsys aninhado, o primeiro design satisfatório (com o caminho menos aninhado) é sempre aplicado, a partir de vários componentes disponíveis. Para obter mais informações, consulte [Resolução do caminho de design](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-25250: Hotfix do CQ-4246276

### Integração {#integration-3}

* Usando a integração de público-alvo pronta para uso, o direcionamento de um componente renderiza a página inteira em vez de um componente direcionado vazio. NPR-25273: hotfix do CQ-4248003
* No modo de direcionamento, a interrupção de uma herança ainda mostra o componente como direcionado com a herança não interrompida no modo de edição. NPR-25324: hotfix do CQ-4248162
* Quando uma personalização é definida em uma página e um público-alvo é resolvido, a experiência correspondente é exibida no modo de edição. NPR-25731: Hotfix do CQ-4249465
* URL de teaser incorreto ao usar o AEM com um caminho de contexto não padrão. NPR-25971: Hotfix do CQ-4250953
* Renderização em branco ao usar a recusa. NPR-25295: hotfix do CQ-4246792
* As experiências excluídas do ambiente de criação nunca são removidas do site publicado na ativação da página. NPR-24869: hotfix do CQ-4247832

### DAM - Cliente DM {#dam-dm-client}

* (Chrome, Firefox) O VideoPlayer ignora cliques do mouse em dispositivos habilitados para toque. Hotfix do CQ-4247370

### Plataforma {#platform-1}

* Permissão para configurar o número máximo de tentativas ao adquirir/liberar um pacote. NPR-25328: Hotfix do Granite-22376
* Registro incorreto se houver erros de replicação. NPR-25308: Hotfix do CQ-4249402
* A instalação do Forms AEM 6.2 Forms CFP8 para CFP14 causa falha do Apache POI. NPR-25053: Hotfix do Granite-21771

### Granite {#granite-2}

* Processo de sincronização do usuário falhando com a exceção OakConstraint0022. NPR-25729: Hotfix para Oak-7428

### Communities {#communities}

* O pacote cq-social-as-provider não inicia com as versões 3.x do driver Mongo. NPR-26271: hotfix do CQ-4252710

### IU - Foundation {#ui-foundation-1}

* Atualização para jqueryui clientlib v1.12.1. NPR-25090: hotfix para Granite-21981, CQ-4248897

* (Omnisearch): A propriedade “Title” está vulnerável à Criação de script entre sites (XSS) no Sites. NPR-24994: Hotfix do Granite-19933

### Forms {#forms-3}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-3}

#### Formulários adaptáveis {#adaptive-forms-2}

* Codificação incorreta ao enviar dados do formulário adaptável. NPR-25539

#### Forms - Gerenciamento {#forms-management}

* Ativos de formulário não relacionados relatados como referências ao publicar a página. NPR-26167: Hotfix do CQ-4251004

### Forms - Instalador JEE {#forms-jee-installer-3}

#### Segurança de documentos {#document-security}

* A variável é preenchida como o tipo de dados Lista, o subtipo é string, mas ocorre um erro “não é possível forçar o objeto”. NPR-26194: Hotfix do CQ-4252287
* Não é possível acessar as configurações de marca d&#39;água após a instalação do 6.2-SP1-CFP15. NPR-26130: Hotfix do CQ-4250984

### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-2}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP17

[Obter arquivo](assets/do-not-localize/62cfp17updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP17

[Obter arquivo](assets/do-not-localize/content_package_62sp1_cfp17_2.txt)

### Cumulative Fix Pack 16 {#cumulative-fix-pack-4}

O AEM Cumulative Fix Pack 6.2 SP1-CFP16 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Os principais destaques desse Cumulative Fix Pack são:

* Inclusão de suporte STARTTLS no Day CQ Mail Service.
* Correção do alinhamento dos ícones do ContextHub no popover do perfil.
* Correções na funcionalidade mostrar/ocultar do componente suspenso.
* Atualização para a versão mais recente do Jackson 2.8.11

### Ativos {#assets-3}

* Não é possível iniciar um fluxo de trabalho a partir de uma visualização de lista. NPR-24393: Hotfix do CQ-4245788
* (Firefox/Chrome) Não é possível baixar ativos na página Compartilhamento de ativos. NPR-24523: Hotfix do CQ-4224408
* Melhoria da qualidade padrão da pré-visualização de vídeo no AEM. NPR-24148: Hotfix do CQ-4244310

### Integração {#integration-4}

* Quando um componente é direcionado na instância de publicação, uma oscilação aparece para mostrar a experiência padrão antes da experiência direcionada. NPR-23992: hotfix do CQ-4242038
* As experiências excluídas do ambiente de criação nunca são removidas do site publicado na ativação da página. NPR-24869: hotfix do CQ-4247832

### Plataforma {#platform-2}

* Patch jQuery 1.12.4 do clientlib para incluir a correção de segurança. NPR-24129: Hotfix do Granite-20058
* Inclusão de suporte STARTTLS no Day CQ Mail Service. NPR-23941: Hotfix do CQ-4240397
* Remoção do padrão MERGE_PRESERVE aclHandling. NPR-24593: Hotfix do Granite-21889
* Falho do LineChecker ao externalizar links quando a solicitação contém parâmetros de consulta inválidos. NPR-24127: hotfix do CQ-4241893

### MSM {#msm}

* Hotfixes proativos para ataques de criação de script entre sites (XSS). NPR-21893: hotfix do CQ-4223385
* MSM LiveRelationship: RolloutConfig efetivo está errado se BlueprintConfig estiver na raiz. NPR-23999: hotfix do CQ-4243000

### Sites {#sites-3}

* A criação de uma experiência em uma área de live copy requer primeiro que a herança seja interrompida para que possa ser configurada. NPR-24995, Hotfix do CQ-4248209
* (Interface para toque) Vários ícones na barra de ferramentas superior desaparecem ao bloquear ou desbloquear uma página. NPR-23954: Hotfix do CQ-4243345
* Os campos não estão alinhados corretamente no hub de contexto. NPR-23958
* Ação de publicação na página bloqueada interrompe a criação. NPR-23970: Hotfix do CQ-4243203
* Os relatórios OOTB em /etc/reports/ não estão funcionando corretamente e não mostram nenhum gráfico de dados históricos. NPR-20035: Hotfix do CQ-4220180
* Falha na criação de lançamentos ao iniciar o fluxo de trabalho “Solicitar lançamento” em um projeto. NPR-24255: Hotfix do CQ-4245030
* Tags e atributos de HTML ignorados por emails após a instalação CFP10. NPR-24287: Hotfix do CQ-4240028
* TagPicker: a Sugestão de tags, no campo de tags de esquemas de metadados, consulta nós para marcação, o que leva à lentidão no carregamento. NPR-24347: Hotfix do CQ-4244291
* A integração do Salesforce falha com configurações de proxy. NPR-24418: Hotfix do CQ-4245300
* (WCM) O PageManager deixa a página marcada em Exceção durante a criação de Revisão. NPR-24565: Hotfix do CQ-4246203
* O botão Device Emulator desaparece do modo de edição e pré-visualização após aplicar o CFP14. NPR-24566: Hotfix do CQ-4247060
* (Interface clássica) Todas as tags aparecem como vazias quando criadas na caixa de diálogo. NPR-24688, hotfix do CQ-4246407
* Não é possível criar a versão na primeira tentativa. NPR-24774: Hotfix do CQ-4232176
* Os relatórios OOTB em /etc/reports/ não estão funcionando corretamente e não mostram nenhum gráfico de dados históricos. NPR-24138: Hotfix do CQ-4220180

### Vulnerabilidade {#vulnerability-1}

* A integração do Salesforce está vulnerável à Falsificação de solicitação do lado do servidor (SSRF). NPR-24289: Hotfix do CQ-4245277
* Vulnerabilidade do SSRF (Server Side Request Forgery) em ReportingServicesProxyServlet. NPR-24657: Hotfix do CQ-4246880

### Granite {#granite-3}

* As operações de leitura de metadados não estão sendo encerradas. NPR-24240: Hotfix do Granite-19866
* Atualização do Jetty para 9.4.11.v20180605 para corrigir vulnerabilidades. NPR-25033: Hotfix do Granite-22120

### WCM - Componentes do Foundation {#wcm-foundation-components-1}

* O PageComparator gera ClassCastException ao classificar páginas. NPR-24123: Hotfix do CQ-4244048
* A funcionalidade Mostrar/Ocultar do componente de formulário suspenso não está funcionando como esperado. NPR-24562: Hotfix do CQ-4222853

### Interface do usuário {#user-interface}

* A alta utilização da CPU é observada devido a muitas solicitações na funcionalidade de pesquisa do administrador. NPR-23588: hotfix do Granite-21286
* (Interface Clássica) O componente exibe os valores padrão mesmo se o serviço de modelo de dados de formulário associado estiver definido como campo vazio. NPR-21903: hotfix do GRANITE-19744
* Vários campos lançando o NPE quando nenhum FormData está presente para solicitação. NPR-24513: hotfix do Granite-21055

## Forms {#forms-4}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-4}

#### Núcleo {#core}

* (OSGi) AEM Forms OSGi afetado pelo alerta de segurança de vínculo de dados Jackson. NPR-24274: Hotfix do CQ-4230245

#### Rights Management {#rights-management}

* Falha no Apache POI após a instalação do AEM 6.2 SP1-CFP14. NPR-25054, NPR-25052: Hotfix do CQ-4245898, CQ-4244778

#### Formulários HTML5 {#html-forms}

* Os dados não são preenchidos com o preenchimento prévio de campos de várias linhas na pré-visualização do HTML. NPR-23357: Hotfix do CQ-4244212
* Quando uma carta é visualizada através de uma visualização padrão, o mapeamento do fragmento de layout não é exibido mesmo quando ele aparece corretamente ao clicar em Visualizar. NPR-22993: Hotfix do CQ-4237745
* Problema com a pré-visualização de HTML de um campo de texto quando um padrão de Número de Segurança Social é aplicado a um modelo. NPR-23205

#### Formulários adaptáveis {#adaptive-forms-3}

* Erro “Guidelib não está definido” ao adicionar o formulário do AEM ao componente Parsys. NPR-24269: Hotfix do CQ-4244546

### Instalador do Forms no JEE {#forms-jee-installer-4}

#### Forms-Install-LCM {#forms-install-lcm}

* Os finais de linhas de janelas em arquivos de script Shell fazem com que o LCM não seja executado no UNIX®. NPR-22958

### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-3}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP16

[Obter arquivo](assets/do-not-localize/6_2cfp16_bundlecomparison-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP16

[Obter arquivo](assets/do-not-localize/6_2cfp16_contentpackage-list.txt)

### Cumulative Fix Pack 15 {#cumulative-fix-pack-5}

O AEM Cumulative Fix Pack 6.2 SP1-CFP15 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do [AEM 6.2 SP1](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

Os principais destaques desse Cumulative Fix Pack são:

* Correções de segurança proativas na tabela do Foundation para manter a consistência do design.
* Inclusão de suporte para typeHint para salvar valores como string.
* Oferece segurança aprimorada para o serviço de preenchimento prévio do Forms
* Atualize para o arquivo adobe-reader-extensions-dsc.jar mais recente para fazer correções na extensão do leitor.
* O gancho de validação foi ajustado para considerar itens `:invalid` na entrada do número de reforço.

### Ativos {#assets-4}

* Os dados EmbedXMP são sempre definidos como “ativos” para o processo de geração de pirâmide TIFF. NPR-22776: Hotfix do CQ-4234498
* Não é possível definir vários valores padrão em campos de Vários valores. NPR-22900: Hotfix do CQ-4239000
* (Dynamic Media) Ao marcar a caixa de seleção Representações dinâmicas, o arquivo zip baixado gera a imagem TIFF original com um arquivo de zero bytes. NPR-22410: Hotfix do CQ-4198471
* (Interface para toque) Local de upload padrão para ativos na exibição em Coluna. NPR-23475: Hotfix do CQ-4237057

### Integração {#integration-5}

* No modo de direcionamento, autores podem modificar um componente herdado do blueprint sem cancelar a herança. NPR-22751: hotfix do CQ-4237907
* A variável de caminho não é codificada corretamente, resultando em uma criação de script entre sites (XSS) não persistente. NPR-22851

### MSM {#msm-1}

* Durante a implantação de uma Live Copy com várias configurações de implantação, se um ResourceNameConflict surgir abaixo da raiz, o fluxo de implantação será encerrado sem incluir todas as ramificações. NPR-22842: Hotfix do CQ-4236188

### Plataforma {#platform-3}

* Implementação de um limite de pesquisa em uma solicitação para aplicação reversa. NPR-23351: Hotfix do Granite-21135****
* A alteração no padrão da mensagem não é refletida em agentes personalizados. NPR-23486: Hotfix do CQ-4241974

### Sites {#sites-4}

* A criação de um link em um texto de um Editor de Rich Text para um documento com espaços ou outros caracteres especiais não funciona. NPR-22289: Hotfix do CQ-4224321
* Salvar o segmento com um valor enorme (10000000000) define o aumento para 0, causando uma mensagem de erro. NPR-22524: hotfix do CQ-4237006
* Não é possível clicar em Adicionar item no componente Vários campos. NPR-22552: hotfix do CQ-4237404
* A barra de rolagem horizontal não é visível quando o segmento tem um título longo. NPR-22615: Hotfix do CQ-4237001
* O carregamento de um público-alvo vazio gera um código JavaScript incorreto. NPR-22974: Hotfix do CQ-4238734
* Ao programar uma ativação ou desativação, o título do fluxo de trabalho é obrigatório, portanto, o título do fluxo de trabalho personalizado não é traduzido na linha do tempo. NPR-23121: Hotfix do CQ-4237552
* Solicitação de correções para problemas em segmentos de Públicos-alvos no Sites. NPR-23128
* (Firefox) A caixa de seleção para a persona selecionada não é a correta. NPR-23345
* Os rótulos para os diferentes modos são exibidos junto com os ícones. NPR-23275
* Erro &quot;Valor inválido do seletor de recursão&quot; ao migrar um componente do AEM 6.0 para o AEM 6.2. NPR-23503: Hotfix do CQ-4241258

### Communities {#communities-1}

* As notificações por email e Web não são acionadas devido à falha de mensagem nos grupos. NPR-23447: Hotfix do CQ-4242880

### Tradução {#translation-1}

* Cópias de idioma do ativo são criadas quando o ativo “Não traduzir” é definido na configuração de tradução. NPR-22540: Hotfix do CQ-4237962

### Interface do usuário {#user-interface-1}

* O uso do Omnisearch para consulta com hífen retorna um erro de servidor. NPR-22999: Hotfix do Granite-19674
* DatePicker não é compatível com a definição manual de dicas de tipo externo definidas por um campo oculto. A alteração da dica de tipo aciona um erro de conversão. NPR-23333: Hotfix do Granite-21194

### WCM - Componentes do Foundation {#wcm-foundation-components-2}

* O componente CAPTCHA foi descontinuado para melhorar a segurança. Se você usar o componente CAPTCHA, a mensagem “O componente Captcha está obsoleto e não deve ser usado” será exibida após a instalação da versão 6.2 SP2-CFP15 ou posterior. O componente do AEM pode ser personalizado para incluir o reCAPTCHA para melhor segurança NPR-22151: Hotfix do CQ-4220052
* O componente “Tabela” do WCM Foundation é vulnerável a Scripts armazenados entre sites. NPR-23206: Hotfix do CQ-4240760

### Vulnerabilidade {#vulnerability-2}

* Criação de script entre sites (XSS) nos links de Projeto da interface do usuário do administrador. NPR-23272: Hotfix do CQ-4241795

## Forms {#forms-5}

### Pacote complementar do Forms {#forms-add-on-package-5}

#### Gerenciamento de correspondência {#correspondence-management}

* Quando uma carta é visualizada através de uma visualização padrão, o mapeamento do fragmento de layout não é exibido mesmo quando ele aparece corretamente ao clicar no botão Visualizar. NPR-23335: hotfix do CQ-4237745
* Os dados na carta que correspondem aos vínculos definidos em XDP não são preenchidos ao usar o URL direto da carta. NPR-24145: hotfix do CQ-4244290

#### Formulários para publicação de conteúdo para dispositivos móveis {#mobile-forms}

* (Gerenciamento de correspondência) Desalinhamento de dados ao carregar a correspondência com o XML do público-alvo. NPR-22993: Hotfix do CQ-4237663

#### Serviço de extensões do Reader {#reader-extensions-service}

* Não é possível aplicar a extensão do Reader no Adobe PDF. NPR-23067

#### Gerenciador do Forms {#forms-manager}

* Os formulários incorporados ao site não são publicados ao republicar a página do site. NPR-23014: hotfix do CQ-4236566

#### Vulnerabilidade {#vulnerability-3}

* Hotfixes proativos para criação de script entre sites. NPR-20624: hotfix do CQ-4206055
* Vulnerabilidade de criação de script entre sites (XSS) armazenada na guia Observações do Gerenciador de formulários. NPR-27157: hotfix do CQ-4255556

#### Serviço de criptografia {#encryption-service}

* (OSGI) [JEE] Status de assinatura incorreto para PDF com anexo ao verificar com “Validar processo PDF”. NPR-23269, NPR-23737

### Instalador do Forms no JEE {#forms-jee-installer-5}

#### Núcleo {#core-1}

* Os problemas relatados na análise de código estático do Core-ext devem ser corrigidos. NPR-13947

#### Serviço PDFG {#pdfg-service}

* O conversor de HTML para PDF não está funcionando. NPR-21545

### Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-4}

O texto seguinte documenta a lista de pacotes OSGi e os pacotes de conteúdo incluídos no CFP.

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP15

[Obter arquivo](assets/do-not-localize/6_2cfp15updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP15

[Obter arquivo](assets/do-not-localize/6_2_cfp15contentpackage-list.txt)

### Cumulative Fix Pack 14 {#cumulative-fix-pack-6}

O AEM Cumulative Fix Pack 6.2 SP1-CFP14 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Aprimoramento da capacidade de edição das propriedades de metadados de ativos.
* O processo de Notificação de expiração de senha foi reconfigurado para ativos que já estão expirados.
* O console da interface de toque foi personalizado para estender mais localidades.
* cq-msm-core atualizado para uma sincronização eficiente do Livecopyindex.
* Funcionalidade de replicação simplificada para várias implantações.

### Ativos {#assets-5}

* Os usuários não conseguem baixar ativos com avisos e nomes de arquivos longos. NPR-22163: hotfix do CQ-4235274
* Um caractere de aspas simples impede a atualização de metadados na exibição em massa e a interface é interrompida ao abrir as propriedades de um ativo usando as ações rápidas da barra de ferramentas. NPR-22317, NPR-22353: hotfix do CQ-4236990, CQ-4236469
* O trabalho notificação de expiração de ativos não desativa os ativos expirados. NPR-22346: Hotfix do CQ-4237188
* O download de ativos falha ao usar o Gerenciamento de direitos digitais nos Ativos do Safari. NPR-22378: Hotfix do CQ-4236460
* A representação da Web de imagens pequenas possui um tamanho de pixels incorreto. NPR-22435: hotfix do CQ-4236742

### Sites {#sites-5}

* (Interface de toque) Tags movidas são exibidas nos locais antigos e novos nas propriedades da página. NPR-21921, Hotfix do CQ-4238598
* (Interface para toque) O Editor de Rich Text remove todos os atributos exceto a ID da tag &lt;a>. NPR-22045: Hotfix do CQ-4234133
* Colar conteúdo diretamente no Editor de Rich Text usando CTRL+V ignora as quebras de linha. NPR-22117: Hotfix do CUI-5881
* (Interface de toque) Não é possível mostrar mais de 40 tags sob um namespace. NPR-22290: Hotfix do CQ-99114
* Problemas de Feed RSS, porta -1 do AEM 6.2 NPR-22158: Hotfix do CQ-4233339
* (IE) Ao criar qualquer caractere no campo de Rich Text pela primeira vez, um espaço à direita é adicionado ao caractere. NPR-22443: hotfix do CQ-4235343
* Ao tentar corresponder ao nome do pacote, o objeto de uso Java™ congela o SightlyJavaCompilerService devido a um caractere de espaço à direita na declaração do pacote. NPR-22557: Hotfix do Granite-20836
* O console da Interface para toque não coleta novos idiomas para marcação. NPR-22250: Hotfix do CQ-4239194

### Mobile On-Demand {#mobile-on-demand}

* (Digital Publishing Suite) Tanto a data de publicação quanto a data de capa são campos obrigatórios para os fólios antes de serem enviadas para o DPS. NPR-22484

### Commerce {#commerce}

* Várias vulnerabilidades de criação de script entre sites (XSS) no assistente de criação de catálogo de comércio. NPR-22344: hotfix do CQ-4237017

### MSM {#msm-2}

* A sincronização do LiveCopyIndex ocasiona o congestionamento de threads durante longas atualizações de índice. NPR-22214: Hotfix do CQ-90667
* A propriedade `cq:cugEnabled` é desabilitada quando outro campo em uma live copy é editado, tornando a página desprotegida. NPR-22246: Hotfix do CQ-4236050
* A ação de Implantação de páginas falha ao atualizar páginas secundárias quando uma página é suspensa. NPR-22483: Hotfix do CQ-4236956
* A implantação de uma estrutura que foi movida em um lead principal gera um erro `cq:moveTarget`.  NPR-22373: hotfix do CQ-4232536

### Integração {#integration-6}

* Tentar classificar ofertas na biblioteca do seletor de ofertas resulta em comportamento irregular. NPR-22208: Hotfix do CQ-4235439
* O TargetContentImpl torna o AEM lento durante consultas de longa duração. NPR-22361: hotfix do CQ-4236907
* O mecanismo de destino (mbox.js, at.js) não usa URLs desconfigurados e usa URLs que contêm dois pontos que podem falhar em determinadas implantações. NPR-22366: Hotfix do CQ-4237854
* A personalização da página exige a publicação diretamente no nó da marca. NPR-22370: Hotfix do CQ-4236895

### Foundation {#foundation}

* Os modelos de Apache Sling Scripting Sightly utilizam o pacote do Provider **org.apache.sling.scripting.sightly.models.provider/1.0.18**. NPR-22614: Hotfix para Sling-5944, Sling-6866

### Projetos {#projects}

* O Iniciador do fluxo de trabalho não pode aceitar o valor de string TypeHint. NPR-22436: hotfix do CQ-4237855

### Tradução {#translation-2}

* Investigue problemas com a funcionalidade Visualização. NPR-22201: Hotfix do CQ-4223753

### Interface do usuário {#user-interface-2}

* (Interface Clássica) O componente exibe os valores padrão mesmo se o serviço de modelo de dados de formulário associado estiver definido como campo vazio. NPR-21903: hotfix do GRANITE-19744

### WCM - Componentes do Foundation {#wcm-foundation-components-3}

* Erro ao publicar uma página de Live Copy que aponta para uma página de Importador no Adobe Campaign. NPR-22470: Hotfix do CQ-4237164
* Erros de JavaScript ao abrir o Editor de Fragmentos de experiência. NPR-22598: Hotfix do CQ-4238415

### Fluxo de trabalho {#workflow}

* O Serviço de notificação por email do fluxo de trabalho do Day CQ aciona um email por nó Mongo para notificações WorkflowCompleted e WorkflowAborted. NPR-22486: Hotfix do CQ-4238172

## Forms {#forms-6}

### Pacote complementar do Forms {#forms-add-on-package-6}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

#### Formulários adaptáveis {#adaptive-forms-4}

* Inconsistência no valor do espaço reservado suspenso do formulário adaptável no IE11 e Chrome. NPR-22405: hotfix do CQ-4227096

### Instalador do Forms no JEE {#forms-jee-installer-6}

#### Instalar o LCM {#install-lcm}

* Atualize o Jsafe Jars para Cryptoj 6.1.3.1 no instalador e no LCM. NPR-22744

### Feature Packs incluídos {#feature-packs-included}

#### Gerenciamento de processos {#process-management}

* (Espaço de trabalho HTML) Quando uma pessoa reivindica uma tarefa, a contagem da fila é atualizada somente para o usuário em questão. Isto é, a menos que a página seja atualizada. NPR-19778: hotfix do CQ-4233665

### Pacotes OSGi e pacotes de conteúdo incluídos no CFP14 {#osgi-bundles-and-content-packages-included-in-cfp}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP14

[Obter arquivo](assets/do-not-localize/6_2cfp14updated_bundles.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP14

[Obter arquivo](assets/do-not-localize/6_2_cfp14contentpackage-list.txt)
O AEM Cumulative Fix Pack 6.2 SP1-CFP13 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Habilitar a configuração do campo Parâmetro estático nas Configurações do componente de direcionamento ao usar AT.js como biblioteca do cliente.
* Correções na funcionalidade mostrar/ocultar do componente suspenso.
* Correções para usar audiências de sincronização de públicos-alvos.
* Mais versatilidade do Gerenciamento de correspondência para acomodar caracteres especiais.

### Ativos {#assets-6}

* A Remoção de versões falha ao remover versões antigas de ativos. NPR-21682: Hotfix do CQ-4212996
* A reorganização de pastas sob uma pasta reorganizável não é mantida. NPR-21964: hotfix do CQ-4231761

### Sites {#sites-6}

* (Interface para toque)(Interface Clássica) Várias vulnerabilidades de Criação de script entre sites (XSS) em HTL e componentes principais. NPR-21532: Hotfix do CQ-4232305 e CQ-4232511
* A criação/formatação de conteúdo (por exemplo, atribuição/remoção de novos estilos de lista) em um texto selecionado não funciona bem no Internet Explorer 11. NPR-21533: hotfix do CQ-4230689
* (Safari) Os usuários não conseguem visualizar todos os ativos no painel do Localizador de ativos. NPR-21981: hotfix do CQ-4213720
* O Timewarp retorna o erro “RecursionTooDeepException” com uma página distorcida e nenhuma nova versão é criada mesmo quando a data é alterada. NPR-21707: hotfix do CQ-4199536
* Ao carregar uma página no editor, o WorkflowStatusProvider (pageinfo.json) é carregado três vezes, causando lentidão na instância do AEM. NPR-21778: hotfix do CQ-59232

### Integração {#integration-7}

* A criação de audiências do Type &amp; Browse para publicação de conteúdo para dispositivos móveis no modo de criação de Públicos-alvos não está funcionando no AEM. NPR-21676, NPR-21681: Hotfix do CQ-4232100
* Sob alta latência durante a atualização de um componente direcionado, é possível adicionar outra oferta antes que o componente seja atualizado completamente. NPR-21744: Hotfix do CQ-4233158/CQ-4234293
* Usuários não podem ver valores de Parâmetros estáticos de teste na chamada da mbox que podem ser vistos ao testar AT.js como a biblioteca do cliente na configuração de nuvem. NPR-21930: hotfix do CQ-4234520

### Plataforma {#platform-4}

* Problemas de desempenho com a sincronização de usuários quando o número de usuários ou grupos é grande. NPR-20431: hotfix do CQ-4223282
* Usuários não conseguem sincronizar com a sincronização de usuários usando a distribuição do Sling. NPR-21911: Hotfix do Granite-20404
* Coibição de palavras de interrupção sendo realçadas em trechos de pesquisa (em uma página de Geometrixx). NPR-21835: hotfix do Granite-21067 
Observação: Essa correção requer o Oak CFP 1.4.20 ou superior.

### Tradução {#translation-3}

* A propriedade jcr está ausente da ID de usuário do Iniciador ao criar um projeto de tradução. NPR-21715: hotfix do CQ-4230713

### WCM - Componentes do Foundation {#wcm-foundation-components-4}

* A funcionalidade Mostrar/Ocultar do componente de formulário suspenso não está funcionando como esperado. NPR-22164: Hotfix do CQ-4235288

## Forms {#forms-7}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-7}

#### Formulários adaptáveis {#adaptive-forms-5}

* Inserção de Injeção de Entidade Externa XML (XXE) nos Formulários adaptáveis. NPR-21982: Hotfix do CQ-109878
* (iOS11) Ao clicar no componente do anexo de arquivo, o anexo de arquivo abre a câmera em vez do navegador de arquivos do dispositivo. NPR-21926: hotfix do CQ-4214348
* A ausência de título na interface de criação de tema está causando exceções e falhas na renderização da caixa de diálogo. Hotfix do CQ-4236143

#### Gerenciamento de correspondência {#correspondence-management-1}

* Problemas de renderização com dados xml contendo caracteres especiais. NPR-21712: Hotfix do CQ-4229137

### Instalador do Forms no JEE {#forms-jee-installer-7}

#### Serviço de Assembler {#assembler-service}

* O arquivo PDF gerado usando `6.2.0-ASM-1017-003` está danificado. NPR-21427: hotfix do CQ-4228046

#### Serviço PDFG {#pdfg-service-1}

* Falha de OCR devido ao tamanho inesperado da página (PDF) de arquivos PNG, JPEG e TIFF. NPR-19489: Hotfix do CQ-4209079

## Pacotes OSGi e pacotes de conteúdo incluídos no CFP13 {#osgi-bundles-and-content-packages-included-in-cfp-1}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP13

[Obter arquivo](assets/do-not-localize/cfp13_bundlecompare-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP13

[Obter arquivo](assets/do-not-localize/cfp13_contentpackage-list.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP12.1 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Manuseio de metadados aprimorado para campos multivalor.
* Suporte para códigos de países de múltiplos caracteres (mais de dois) em fluxos de trabalho de tradução.
* Melhoria na renderização de páginas com vários componentes aninhados.
* Sincronização aprimorada das datas de publicação para ativos entre o AEM e o Adobe Digital Publishing Suite.

### Ativos {#assets-7}

* Muitos caracteres no OmniSearch podem causar falha no servidor do AEM. NPR-21083: hotfix do CQ-4223602
* Os valores especificados na segunda opção em um campo multivalor no esquema de metadados não são anexados aos valores especificados anteriormente no CRX-de. NPR-21220: Hotfix do CQ-4224526
* O download de ativos falha ao usar o Gerenciamento de direitos digitais nos Ativos do Safari. NPR-21387: Hotfix do CQ-4230287

### Sites {#sites-7}

* (DAM) (Interface Clássica) Várias vulnerabilidades de Criação de script entre sites (XSS) em alguns arquivos SWF na inicialização rápida do Author/Publish do AEM CQ. NPR-21073, NPR-21074: Hotfix do NPR-20612
* O seletor de tags não traduz as tags disponíveis em vários idiomas. NPR-21221: hotfix do CQ-78855
* A renderização de problemas com o console de artigos do AEM, como o uso de vários componentes aninhados, torna o console lento. NPR-21271: Hotfix do CQ-4224158

### Integração {#integration-8}

* Ao adicionar uma estrutura de público-alvo, o modo de direcionamento não está disponível na lista de seleção de modo no editor. NPR-21047

### Mobile-on-demand {#mobile-on-demand-1}

* (Digital Publishing Suite) As datas de publicação dos fólios no AEM não correspondem às datas que aparecem no Produtor de fólios. NPR-21145

### MSM {#msm-3}

* O processo de redefinição da Live Copy é interrompido após a exclusão da primeira página local na LC. NPR-21276: hotfix do CQ-4229743

### Plataforma {#platform-5}

* O tag lib personalizado que faz referência a tags implementadas como script não foi encontrado após a atualização para o AEM 6.3. NPR-20149: hotfix do Granite-18433

### Tradução {#translation-4}

* Os fluxos de trabalho de tradução falham com códigos lang_country com mais de dois caracteres. NPR-21088: hotfix do CQ-4197439
* Não envie uma página de ativo novamente para um projeto de tradução até que o projeto seja concluído. NPR-21219: hotfix do CQ-4209908

### Interface do usuário {#user-interface-3}

* O componente Selecionar não exclui a propriedade de destino durante o envio do formulário. NPR-21163: hotfix do GRANITE-14125
* A expansão dupla do HTTP.encodePathOfURI codifica o sinal de mais “+”. NPR-21417: hotfix do GRANITE-16340

### Vulnerabilidade {#vulnerability-4}

* Criação de script entre sites (XSS) no editor de metadados do DAM. NPR-21434: hotfix do CQ-83472
* Vários arquivos SWF são vulneráveis à criação de script entre sites (XSS). NPR-20612: hotfix do CQ-4213297

## Forms {#forms-8}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-8}

#### Gerenciamento de correspondência {#correspondence-management-2}

* (IE11) A renderização inicial do conteúdo HTML ocorre somente no lado esquerdo enquanto o lado direito é carregado intermitentemente após a interface do usuário ser completamente carregada. NPR-21554
* O botão de envio de visualização da carta é desativado após a instalação do AEM 6.2 SP1-CFP9. NPR-21547
* Ao selecionar o tipo de vínculo de ativo, a janela Seletor de ativo não é aberta no assistente Editar vínculo de dados da carta. NPR-21164: Hotfix do CQ-4194567
* Para editar um módulo de texto incorporado ou editável, toque no ícone Editar relevante ou clique duas vezes no módulo de texto relevante na pré-visualização de correspondências. NPR-21402

#### Formulários adaptáveis {#adaptive-forms-6}

* O componente de botão Enviar do AEM Forms exibe type=&quot;button&quot; em vez de type=&quot;submit&quot;. NPR-21007
* Os dados permanecem persistentes ao adicionar ou excluir novos painéis para painéis repetíveis. NPR-21408

### Instalador do Forms no JEE {#forms-jee-installer-8}

#### Núcleo {#core-2}

* A atualização para o Java™ 8 mais recente (Atualização 131) gera uma exceção: “O provedor JsafeJCE está desabilitado, uma autoverificação de integridade FIPS 140 necessária falhou”. NPR-21355

**Observação:** Este NPR requer mais configurações. Consulte [Atualização mais recente do Java™ 8](#latest-java-update-throws-an-exception-npr).

* O Jsafe Jars atualizou para CryptoJ 6.1.3.1 no Núcleo, Criptografia, Assinatura e Segurança de documentos. NPR-21360, NPR-21361, NPR-21356, NPR-21358

#### Instalar o LCM {#install-lcm-1}

* Atualize o Jsafe Jars para CryptoJ 6.1.3.1 no instalador e LCM. NPR-21362

#### Serviço PDFG {#pdfg-service-2}

* Atualize o Jsafe Jars para CryptoJ 6.1.3.1 em PDFG. NPR-21359

#### Gerenciamento de processos {#process-management-1}

* (Workspace HTML) Habilitação do redimensionamento de colunas para que a categoria de nomes não apareça truncada. NPR-19770: Hotfix do CQ-4233668

#### Serviço de extensões do Reader {#reader-extensions-service-1}

* O Jsafe Jars atualizou para CryptoJ 6.1.3.1 no RE. NPR-21357

## Pacotes OSGi e pacotes de conteúdo incluídos no CFP12.1 {#osgi-bundles-and-content-packages-included-in-cfp-2}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP12.1

[Obter arquivo](assets/do-not-localize/cfp12_bundlecomparsion-list1.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP12.1

[Obter arquivo](assets/do-not-localize/cfp12_contentpackage-list.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP11 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* cq-msm-core atualizado para uma sincronização eficiente do Livecopyindex.
* Melhoria na eficiência da edição de Fragmentos de conteúdo.
* Fornece uma opção de validação no gerenciador de pacotes para detectar permissões de ACL.
* Habilitação do Campaign para inclusão de ID de email para correspondência do cliente.
* Aprimoramento das capacidades de codificação de vídeo para arquivos do Dynamic Media.
* Correções no componente Sightly e LiveCopies.

### Ativos {#assets-8}

* Falha na codificação de vídeos do Dynamic Media para arquivos que incluem espaços no nome. NPR-20818: Hotfix do CQ-102469
* Várias vulnerabilidades de Criação de script entre sites (XSS) em alguns arquivos SWF na inicialização rápida do Author/Publish do AEM CQ. NPR-21071, NPR-21072
* Os usuários não conseguem baixar ativos com avisos e nomes de arquivos longos. NPR-20255: hotfix do CQ-4222139

### Sites {#sites-8}

* Integração do AEM e do Campaign: links especiais são regravados no Adobe Campaign, impedindo que os clientes enviem hiperlinks de mailto: em seus emails. NPR-20787: Hotfix do CQ-4225760
* (Interface para toque) Problemas de usabilidade e de desempenho do AEM quando o idioma é definido para francês. NPR-20854: Hotfix do CQ-4227628
* Vincular um arquivo de ativo codificado usando um plug-in de link no RTE retorna um link vazio. NPR-20626, NPR-21059: hotfix do CQ-4223011
* O editor de metadados de fragmentos de conteúdo impede que os autores de conteúdo salvem alterações em fragmentos de conteúdo. NPR-20641: Hotfix do CQ-4224755
* O alias de propriedade da página leva à Solicitação de publicação/Solicitação de cancelamento de publicação. NPR-20731: Hotfix do CQ-4226227
* Problemas de componentes de texto com a codificação do link no elemento de RTE. NPR-20755: Hotfix do CQ-4224321

### Plataforma {#platform-6}

* ResourceResolverImpl.map() não invoca o ResourceDecorator. NPR-20788: Hotfix do GRANITE-19718
* `org.apache.sling.i18n.DefaultLocaleResolver` não consegue processar solicitações por meio de org.apache.sling.engine.SlingRequestProcessor. NPR-20706: Hotfix do CQ-94880
* Solicitação de adição de uma opção de validação no Gerenciador de pacotes para detectar se quaisquer permissões/privilégios de ACL foram alterados em um pacote específico. Hotfix do CQ-4229196

### Fluxo de trabalho {#workflow-1}

* Problemas de estabilidade com a implantação do servidor de produção do AEM. NPR-20979: Hotfix do Granite-19104

### Projetos {#projects-1}

* (Interface para toque) Impossibilidade de adicionar membros do grupo a um projeto. NPR-20990: Hotfix do CQ-4205375

### WCM-Componentes do Foundation {#wcm-foundation-components-5}

* O componente de imagem Sightly “link to” gera um erro 403 devido à ausência da extensão .html. NPR-20823: Hotfix do CQ-4195909
* Em um site de blueprint usando a Live Copy, tentar excluir um componente de formulário lança uma exceção de ponteiro nulo e adiciona o componente de formulário em vez de excluí-lo. NPR-20855: Hotfix do CQ-4204628
* A sincronização do LiveCopyIndex ocasiona o congestionamento de threads durante longas atualizações de índice. NPR-20634: Hotfix do CQ-90667

### Segurança {#security}

* Atualização proativa da biblioteca XSS. NPR-21174
* Atualização para o Apache Commons Email 1.5, que apresenta uma API simplificada para enviar emails. NPR-20509: Hotfix do Granite-18240
* Correção de segurança aplicada à API de proteção do Apache Sling XSS para eliminar a possibilidade de ignorar XSS. NPR-21290: Hotfix do GRANITE-19924
* Desvio de XSS na função XSSAPI#getValidHref. NPR-21174: Hotfix do Granite-19924

### Aplicativos móveis {#mobile-apps}

* Correção de problemas com solicitações curl Head para ativos OOTB no AEM. NPR-20511: Hotfix do CQ-4221520 e CQ-103024

## Forms {#forms-9}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

Os principais destaques do AEM Forms são:

* Ativação da autenticação de certificado para usuários do Workbench.
* Correções de usabilidade para o Gerenciamento de correspondência, formulários HTML5 e área de trabalho do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-9}

#### Formulários HTML5 {#html-forms-1}

* Problemas de usabilidade com o componente de rabisco em dispositivos iOS 10 e 11. NPR-21092

#### Gerenciamento de correspondência {#correspondence-management-3}

* (Interface de correspondência) Desabilite o botão Enviar após um clique. NPR-21078

### Instalador do Forms no JEE {#forms-jee-installer-9}

#### Serviço de Assembler {#assembler-service-1}

* docConvertor falha ao produzir PDF/A com o erro “O prefixo “stEvt” do elemento `stEvt:action` não está vinculado”. NPR-21032: hotfix do CQ-4222540
* Uma exceção com o nome `java.lang.IllegalArgumentException message:No enum constant com.adobe.internal.pdfm.docbuilder.signature.PathValidationFailureReason.SIGNED_IN_FUTURE` é acionada ao chamar o serviço OMPFSubmission/PDFA/PDFtoPDFA. Esta exceção impede que o processo de verificação de assinatura de curta duração seja concluído até que o servidor seja reiniciado. NPR-20792

#### Workbench {#workbench}

* Ativação da autenticação de certificado para usuários do Workbench. NPR-17548: Hotfix do CQ-4214486

#### Gerenciamento de processos {#process-management-2}

* O processo de preparação de dados é chamado várias vezes quando o formulário para dispositivos móveis é renderizado com parâmetros dataref. NPR-19801: hotfix do CQ-4230427: CQ-4230400

## Pacotes OSGi e pacotes de conteúdo incluídos no CFP11 {#osgi-bundles-and-content-packages-included-in-cfp-3}

Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP11

[Obter arquivo](assets/do-not-localize/cfp11_bundlecomparsion-list.txt)

Lista de pacotes de conteúdo incluídos no AEM 6.2 SP1-CFP11

[Obter arquivo](assets/do-not-localize/cfp11_contentpackage-list.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP10 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Adição de uma função utilitária onDialogLoaded para testes.
* Inclusão de testes e configurações de unidade de front-end ao ClientLibraryProxyServlet.
* Correções de desempenho no componente Editor in-loco de várias imagens.
* Atualizações de configuração no Apache Sling JCR ResourceBundleProvider.

### Ativos {#assets-9}

* A pré-visualização de ativos não funciona se os fluxos de trabalho de atualização de ativos estiverem desativados. NPR-20543: Hotfix do CQ-4204986
* Problemas de renderização com a classe adicionada ao Granite: propriedade de classe (cq-damadmin-admin-assets-upload). NPR-20514: Hotfix do CQ-4219238
* Ativos em miniatura com caracteres especiais no título mostram o objeto Java™ no atributo alternativo do NPR-20347: hotfix do CQ-4223620
* Substituição do código de comparação de versão pelo código proprietário da Adobe devido a problemas de licenciamento. NPR-20273: Hotfix do CQ-4223758
* Problemas de processamento ao fazer upload de arquivos CMYK PSB com várias camadas alfa. NPR-20251: Hotfix do CQ-4220869
* Os dicionários de internacionalização funcionam se o servidor for reiniciado em org.apache.sling.i18n 2.5.6. NPR-20525: hotfix do Granite - 19490
* Nenhum despejo de thread está sendo gerado de acordo com o período do scheduler com a configuração padrão do Coletor de despejo de thread (inicialização padrão do AEM). NPR-20288: hotfix do GRANITE-19488/GRANITE-12741 CQ-90647.

### Sites {#sites-9}

* Se o filtro de datas modificado for alterado após a abertura da pesquisa salva, não haverá efeito nos resultados. E os resultados exibidos são os mesmos que o valor salvo anterior do filtro de data modificado. NPR-19739: Hotfix do CQ-4219425
* Falha ao carregar páginas com componentes aninhados. NPR-20312
* O fluxo de trabalho de Solicitação de exclusão é acionado na exclusão de pacotes de fluxos de trabalho. NPR-20266: Hotfix do CQ-4221686
* (Interface para toque) Problema com Copiar/Colar com a área de transferência do OS e a área de transferência interna do AEM. NPR-20228: Hotfix do CQ-4220383
* Lentidão na instância do AEM com a visualização de lista quando vários ativos (mais de 100) estão sendo carregados. NPR-20034: Hotfix do CQ-4222695
* (Interface de toque) A exclusão de inicializações por meio do console da interface clássica torna todas as páginas não editáveis. NPR-20520: hotfix do CQ-4225074
* A lista suspensa de direcionamento não funciona com vários componentes RTE em uma caixa de diálogo. NPR-20345: hotfix do CQ-4220981

### Plataforma {#platform-7}

* Quando acessado usando uma sessão anônima, o ClientLibraryProxyServlet não faz proxy de solicitações para bibliotecas de clientes na instância publicada e aciona o erro “HTTP 404 não encontrado”. NPR-20195: hotfix do Granite-14409

### Integração {#integration-10}

* Selecionar o Adobe Target como mecanismo de direcionamento impede que o componente seja carregado e gera um erro no log do servidor. NPR-20058: hotfix do CQ-88071, CQ-109698, CQ-4201600

### Commerce {#commerce-1}

* Nenhuma mensagem pop-up de confirmação ou redirecionamento aparece ao criar produtos fora da mesma página. NPR-20257: hotfix do CQ-4223414

### Interface do usuário {#user-interface-4}

* Quando o Seletor de data é um campo em vários campos, os valores salvos nos campos de data não são mantidos durante a edição do componente. NPR-20077: Hotfix do GRANITE-19147
* As consultas anteriores não são abortadas caso consultas consecutivas sejam acionadas, resultando em resultados incorretos. NPR-20397: Hotfix do GRANITE-19306

### WCM - Componentes do Foundation {#wcm-foundation-components-6}

* A propriedade ImageMap ainda existe mesmo depois de remover as imagens do componente Editor local de várias imagens. NPR-20142: hotfix do CQ-4222982

## Forms {#forms-10}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-10}

#### Formulários adaptáveis {#adaptive-forms-7}

* O Script valueCommit é executado duas vezes para DropDownList quando alterado pela interface. NPR-19989: hotfix do CQ-110212

### Instalador do Forms no JEE {#forms-jee-installer-10}

**Gerenciamento de processos**

* O pacote CFP contém AEM Forms HTML Workspace versão 2.2.26. NPR-20099
* O formulário pré-preenchido não funciona quando o formulário para dispositivos móveis é configurado para visualização como PDF. NPR-20566

**Rights Management**

* A caixa de diálogo CAC/Seleção de certificado de autenticação mútua deve exibir certificados com Enhanced Key Usage (EKU) como autenticação de cliente ou logon de cartão inteligente. NPR-20708
* O Forms JEE é compatível com autenticação mútua PKCS#11. NPR-15001

## Pacotes OSGi e pacotes de conteúdo incluídos no CFP10 {#osgi-bundles-and-content-packages-included-in-cfp-4}

Lista de pacotes OSGi incluídos no AEM CFP 6.2 SP1-CFP10

[Obter arquivo](assets/do-not-localize/bundle-list-cfp10.txt)

Lista de pacotes de conteúdo incluídos no AEM CFP 6.2 SP1-CFP10

[Obter arquivo](assets/do-not-localize/contentpackage-list-cfp10.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP9 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Configuração da interface clássica do Analytics adaptada para entrada secreta.
* Correções para o cache de persistência independente do hub de contexto.
* Computação precisa das dimensões do Assets.
* Otimização do desempenho do AEM ao publicar ativos no Brand Portal.
* Correções no valor `Resourcetype` no nó da tela.
* Ativada a funcionalidade de pesquisa de caracteres especiais e de diferenciação de maiúsculas e minúsculas para o conteúdo do fragmento de documento.
* Aprimoramento dos Formulários adaptáveis para anexar PDF no Safari.
Essa experiência fornece uma nova mídia dinâmica que se conecta à nova infraestrutura de publicação do Dynamic Media para uma replicação mais rápida e expansível.

### Ativos {#assets-10}

* A AEM Assets não consegue extrair referências de subativos para ativos do InDesign, incluindo links duplicados para o ativo. NPR-19006: Hotfix do CQ-4204186
* A opção Classificar não funciona para ativos dentro da coleção Comércio. NPR-19508: Hotfix do CQ-4213622
* Quando um ativo com o mesmo nome de um ativo pré-existente é movido para o mesmo local, o valor de `cq:lastReplicationAction` para os ativos é trocado entre si, o que resulta na criação de metadados incorretos. NPR-19531
* Uma mensagem de erro é exibida ao publicar um grande número de ativos, mesmo se todos forem publicados corretamente. NPR-19629: Hotfix do CQ-4219611
* As representações estáticas são listadas com dimensões fixas e não refletem o tamanho da representação real. NPR-20004
* A instância do AEM fica lenta quando vários ativos (mais de 4) são publicados no Brand Portal. NPR-20009

### Sites {#sites-10}

* O AEM exibe um comportamento inesperado quando um usuário tenta publicar a versão do `/unpublish/create` de uma página bloqueada por outro usuário. NPR-19249; hotfix do CQ-4215298 e CQ-4203856
* Ao promover a inicialização aninhada manualmente, a página secundária é excluída. NPR-19704
* Problemas de persistência quando o armazenamento do ContextHub sobrepõe a camada de persistência padrão durante a inicialização. NPR-19979: Hotfix do CQ-4218399
* Os fragmentos de conteúdo são sobrepostos com outros botões. NPR-19980: Hotfix do CQ-4221519
* A página do site não é exibida quando visualizada usando um alias no SiteAdmin. NPR-20053: Hotfix do CQ-4221478
* Erro ao publicar uma página de Live Copy que aponta para uma página de Importador no Adobe Campaign. NPR-20066: Hotfix do CQ-4220846

### Plataforma {#platform-8}

* Atualização do Apache POI para a versão 3.16 para oferecer suporte à inclusão da imagem de plano de fundo dos slides PPT em representações. NPR-18286
* Problemas de renderização com o Internet Browser 11 e o Edge ao fazer upload de vários ativos na mesma pasta. NPR-20062

### Integração {#integration-11}

* O arquivo at.js personalizado não é publicado quando acessado com o usuário anônimo. NPR-19542: Hotfix do CQ-4219592
* Migração de credenciais existentes do Analytics para a Autenticação WSSE. NPR-19962

### Brand Portal {#brand-portal}

* Habilitando as tags de publicação da AEM para o Brand Portal a partir do console tagadmin/tagging. NPR-20271

## Forms {#forms-11}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

### Pacote complementar do Forms {#forms-add-on-package-11}

#### Gerenciamento de correspondência {#correspondence-management-4}

* Ativação da funcionalidade para pesquisar o texto real em fragmentos de documentos quando uma correspondência é visualizada. NPR-19712

#### Formulários adaptáveis {#adaptive-forms-8}

* Aprimoramento dos Formulários adaptáveis para anexar PDF no Safari. Para dar suporte ao mesmo recurso nos formulários já existentes, altere a configuração no dispositivo de anexo e em “Tipos de arquivo compatíveis” atualize o valor para application/pdf, em vez de .pdf. NPR-19623

#### Gerenciador do Forms {#forms-manager-1}

* Se validationState for indefinido em um campo de formulário adaptável e o evento elementFocusChanged ocorrer, um evento de erro (errorState) será retornado ao servidor do Adobe Analytics. NPR-19513

### Instalador do Forms no JEE {#forms-jee-installer-11}

#### Núcleo {#core-3}

* O gerenciador de conexões não está disponível durante o encerramento. O JBoss® elimina a dependência do JDBC antes que o EAR do autor tenha a implantação removida, causando problemas de corrupção. NPR-19703

## Feature Packs incluídos {#feature-packs-included-1}

* Correção de miniaturas e melhorias de transparência no Dynamic Media. NPR-15207

## Pacotes OSGi e pacotes de conteúdo incluídos no CFP9 {#osgi-bundles-and-content-packages-included-in-cfp-5}

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP9

[Obter arquivo](assets/do-not-localize/content_package-list62sp1-cfp9.txt)

Lista de pacotes OSGi atualizada no AEM 6.2SP1-CFP9

[Obter arquivo](assets/do-not-localize/content_package-list62sp1-cfp9-1.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP8 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Introdução de tags a modelos de usuário personalizados no Serviço de modelo de email da Adobe.
* Aprimoramentos de botões da interface para toque no aplicativo para desktop.
* Botão Enviar ao clicar foi desabilitado para impedir vários envios de formulários em uma página de tradução.
* Configuração de vários componentes de RTE em uma caixa de diálogo.
* Reforço de ReferenceUpdates na live copy.
* Ativação da funcionalidade de pesquisa que diferencia maiúsculas e minúsculas para o conteúdo do fragmento de documento.
* Adição da lista de bibliotecas Linux®® à documentação de instalação do AEM Forms.

### Ativos {#assets-11}

* Problemas com a aplicação do filtro Omnisearch em coleções inteligentes no navegador Safari. NPR-19511
* Os metadados de palavras-chave do PDF não são extraídos e são modificados incorretamente quando há várias palavras-chave associadas a um Ativo PDF. Para resolver o problema, a propriedade de metadados do campo Assunto foi removida para os Ativos PDF. No entanto, você pode editar o esquema de metadados para adicionar um campo de texto de vários valores para o campo Assunto. NPR-19126
* O serviço de notificação de fluxos de trabalho não codifica os links no email, o que os impede de carregar após serem clicados. NPR-19490: hotfix do CQ-4218055
* Não é possível carregar uma lista completa de páginas/ativos na exibição de coluna usando o Chrome. NPR-19458: hotfix do CQ-4214248
* Um ícone de tempo de inatividade incorreto é exibido na caixa de entrada do AEM ao ativar o fluxo de trabalho “Solicitação para ativação”. NPR-19365: CQ-4216174
* Problemas com a classificação na visualização da lista. NPR-19217: CQ-95602
* Ao alterar o título ou a imagem em miniatura nas configurações da pasta de ativos, o grupo original e as permissões da pasta são substituídos. NPR-19283: hotfix do CQ-4216080
* As estações de trabalho do `Windows 10` alternam automaticamente para o modo de toque, desabilitando o funcionamento de alguns botões. NPR-19183

### Sites {#sites-11}

* Problemas com a presença de vários componentes do RTE em uma caixa de diálogo. NPR-19311: NPR-19587
* A limpeza automática de versão no AEM 6.2 padrão funciona apenas uma vez após a inicialização do VersionManagerImpl. NPR-19315: hotfix do CQ-4217175
* A instância do fluxo de trabalho fica presa na etapa do fluxo de trabalho “Exportação do Salesforce.com”. NPR-19222: hotfix do CQ-4212976
* As páginas de cópias de idiomas criadas de live copies não são editáveis. NPR-18967
* ReferencesUpdateAction falha ao atualizar Links em uma Live Copy aninhada com alteração de hierarquia. NPR-18715: Hotfix do CQ-4214105

### Plataforma {#platform-9}

* O serviço Modelo de email da Adobe adiciona tags a modelos de usuário personalizados. NPR-19190: hotfix do CQ-4217113

### Projetos {#projects-2}

* Os editores de projeto não conseguem copiar/colar ativos na pasta de ativos do projeto. NPR-19619
* Não é possível gerar pré-visualização para Projetos de tradução após a instalação do 6.2 SP1-CFP1. NPR-16481: CQ-4204655

### Integração {#integration-12}

* Acesse as propriedades dos artigos que estão sendo definidos incorretamente na Adobe Digital Publishing Solution, na interface clássica. NPR-19366
* Renderização lenta de miniaturas devido a artigos em tamanho real no console de artigos do AEM. NPR-19086: CQ-4217148
* Comportamento incorreto de dobramento automático ao personalizar ofertas por meio do Campaign se os usuários tiverem acesso a várias áreas. NPR-19290: Hotfix do CQ-4218029
* A caixa de diálogo de direcionamento não é exibida no modo de direcionamento quando um módulo de direcionamento é editado e salvo mais de uma vez. NPR-19144: hotfix do CQ-4216708

### Fluxo de trabalho {#workflow-2}

* Usuários não conseguem filtrar notificações na Caixa de entrada por usuário/grupo na interface clássica da caixa de entrada. NPR-19122: hotfix do CQ-4215374
* O mapa de imagem não retém as coordenadas selecionadas no componente de imagem HTL. NPR-18911: CQ-4211584

## Forms {#forms-12}

* As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-12}

* Quando o conteúdo é copiado do Microsoft® Word ou de um navegador da web para o editor de texto do gerenciador de correspondência, o estilo é perdido. NPR-19530
* O conteúdo sem quebra de linha no Editor de texto não faz quebra automática. NPR-19481
* Ativação da funcionalidade para pesquisar o texto real em fragmentos de documentos quando uma correspondência é visualizada. NPR-17792: Hotfix do CQ-4214501

#### Gerenciamento de correspondência {#correspondence-management-5}

>[!NOTE]
>
>Essa funcionalidade de pesquisa para fragmentos de texto tem algumas restrições:
>
>* O conteúdo do fragmento de documento diferencia maiúsculas e minúsculas, mas os títulos não.
>* Os resultados da pesquisa não são destacados quando parte da palavra pesquisada está em um estilo diferente ou contém um caractere especial como &quot; ou &#39; ou \.
>* A pesquisa não funciona para conteúdo dinâmico (como valores de elementos do dicionário de dados ou valores de variáveis) no fragmento de documento.

#### Gerenciador do Forms {#forms-manager-2}

* As propriedades do esquema XML de formulários adaptáveis não podem ser editadas após a aplicação do CFP6 no AEM 6.2. hotfix do CQ-4219684
* Todos os serviços do pacote principal do Gerenciador do AEM Forms não são iniciados ao reiniciar o servidor. hotfix do CQ-4217014

### Instalador do Forms no JEE {#forms-jee-installer-12}

#### Instalar o LCM {#install-lcm-2}

* A tela do administrador no Microsoft® Windows exibe a versão 6.0 após a instalação do CFP6. Hotfix do CQ-4217573

## Feature Packs incluídos {#feature-packs-included-2}

* Aprimoramentos de botões da interface para toque no aplicativo para desktop. NPR-18676

## Pacotes OSGi incluídos no CFP8 {#osgi-bundles-included-in-cfp}

Lista de pacotes OSGi atualizada no AEM 6.2SP1-CFP8

[Obter arquivo](assets/do-not-localize/updated-bundles-list-cfp8.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP8

[Obter arquivo](assets/do-not-localize/6_2sp1-cfp8-contentpackagelist.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP7 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Alteração de comportamento na exibição de títulos no cartão de imagem para imagens com a propriedade dc: title definida como String (multicampo).
* Correção dos problemas de desempenho com o Dynamic Media Cloud Services, interface de toque e interfaces de segurança.
* Correções no Apache Felix Http Bridge 3.0.8
* Solução da replicação sem binários (BLR) entre o ambiente de autor e publicação.
* Suporte para o arquivo da biblioteca de públicos-alvos, AT.JS, uma biblioteca de implementação para integração do lado do cliente com o Adobe Target, foi projetada para implementações típicas da web e aplicativos de página única.
* Aprimoramento do desempenho do AEM com a introdução do período de tempo limite de conexão configurável por usuário para o Analytics, DTM e Target.

### Ativos {#assets-12}

* O teste da assimilação de vídeo com o AEM 6.3 configurado com o Dynamic Media Cloud Services ocasiona a exceção &quot;Muitos arquivos abertos&quot;. NPR-18734; Hotfix do CQ-4211407
* A configuração do URL personalizado para ativos em uma página não funciona após reiniciar a instância do AEM. NPR-18634; Hotfix do Granite-18085
* Na Interface para toque, o botão Publicar é exibido para usuários sem permissão para publicar ativos. NPR-18620; Hotfix do CQ-4214042
* A opção de representação dinâmica não está presente na caixa de diálogo de download de um ativo depois que o contrato de licença é definido para ele. NPR-18607; Hotfix do CQ-4212342
* A representação dinâmica não pode ser baixada para ativos que incluem espaços em seus nomes. NPR-18571; Hotfix do CQ-4211738
* Não é possível salvar mais de um usuário ao compartilhar a pasta de ativos com a Creative Cloud. NPR-18489; Hotfix do CQ-103297
* dc: title e dc: description não são alteradas para um valor de vários campos no crx/de. NPR-18474; Hotfix do CQ-4209086
* A operação de mover ativos afeta negativamente o desempenho. NPR-18346
* Nenhum item é exibido na Linha do tempo quando ela é aberta com o conjunto de opções padrão Mostrar tudo. NPR-18302; Hotfix do CQ-4211957
* Ocorre um erro quando um arquivo de texto ASCII/UTF-8 codificado é carregado para o AEM Assets e a geração de miniaturas falha. NPR-18006: CFP do CQ-4209345
* Os botões da ação Publicar ficam visíveis mesmo quando o usuário não tem acesso para replicação. NPR-17353; hotfix do CQ-4209269
* O Siteadmin e Miscadmin não funcionam quando a minificação é habilitada usando min:gcc;obfuscate=true. NPR-18593; hotfix do CQ-4209220
* Os itens de menu personalizados não aparecem até que a tela seja atualizada todas as vezes. NPR-18500; Hotfix do CQ-4213581
* Atualização do arquivo Moment.js para 2.10.6. NPR-18596; Hotfix do Granite-11881
* A aplicação de permissões para macros DM quebra a visualização para o usuário Administrador. NPR-18544; Hotfix do CQ-4211729
* A opção Publicar mais tarde para ativos está gerando ArgumentException ilegal. CQ-4214532

### Sites {#sites-12}

* Em um cluster de criação ativo-ativo com MongoDB, ambos os autores tentam acionar a replicação para o mesmo conteúdo, quando o tempo atinge o tempo definido para o conteúdo. NPR-18708; Hotfix do CQ-4210982
* NPE ao mover um recurso com uma referência que não tem nó de conteúdo jcr: NPR-18664
* Os espaços reservados não estão visíveis em uma página que contém vários componentes parsys. NPR-18645; Hotfix do CQ-110253
* Problemas de simultaneidade em AbstractCopyMoveCommand. NPR-18591
* Ao copiar texto para um componente parsys de outra instância do AEM, o parsys é criado sem qualquer conjunto resourceType. NPR-18511; Hotfix do CQ-4212306

### Plataforma {#platform-10}

* O instalador do JCR não atualiza a versão do pacote após a instalação do pacote. NPR-18728; Hotfix do NPR-15135
* A replicação sem binários (BLR) falha com o ambiente de autor e publicação de binários b/w. NPR-18704
* Solicitação de resolução do Apache Felix HTTP Bridge em um ambiente do AEM. NPR-18297
* A replicação falha quando várias páginas com uma estrutura semelhante são replicadas simultaneamente com a Distribuição de conteúdo de Sling. NPR-18665; Hotfix do Granite-13712
* Criação de pacotes de distribuição de Sling e não de limpeza automática. NPR-18601; Hotfix do Granite-16183

### Integração {#integration-13}

* Exibir ofertas publicadas de pastas de biblioteca resulta em NPE. NPR-18732; Hotfix do CQ-4214593
* A data de início/término de uma atividade não é atualizada no JCR e no Target quando alterada de uma data específica para &quot;Quando ativada/desativada&quot;. NPR-18612; Hotfix do CQ-104831
* A integração do Analytics com o AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18497
* A integração do DTM com o AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18495
* A integração do Target com o AEM não tem tempo limite de conexão ou soquete definido para as conexões httpclient. NPR-18494
* A atividade do Target é desativada após adicionar uma experiência extra. NPR-18227; Hotfix do CQ-4201895

### WCM-Componentes do Foundation {#wcm-foundation-components-7}

* Os mapas de imagem não retêm as coordenadas selecionadas no componente de imagem HTL. NPR-18530; Hotfix do CQ-4211584

### Tradução {#translation-5}

* Os resultados da pesquisa de tradução não incluem nomes de projetos de tradução. NPR-18224; Hotfix do CQ-4210658

### Brand Portal {#brand-portal-1}

* Habilitando as tags de publicação da AEM para o Brand Portal a partir do console tagadmin/tagging. CQ-4212165

## Forms {#forms-13}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-13}

#### Gerenciamento de correspondência {#correspondence-management-6}

* Os dados corretos não são exibidos no painel de edição até que o fragmento seja salvo. NPR-19092
* A inclusão do fragmento de documento a uma correspondência leva bastante tempo. NPR-18958
* Se existir uma declaração XML em um arquivo XML de dados e a representação da carta for iniciada por meio de uma solicitação POST, a carta correspondente não exibirá os dados. NPR-18870
* Nenhum log de auditoria é gerado para ações realizadas em ativos do CM. NPR-16618

>[!NOTE]
>
>Não instale este Pacote complementar de CFP se você for afetado com os dois problemas abaixo:
>
>* Copiar e colar do Word ou da web para o editor de texto do CM exibe o conteúdo com quebra de linha. NPR-19530
>* O conteúdo sem quebra de linha no editor de texto do CM não faz quebra automática. NPR-19449
>

#### Formulários adaptáveis {#adaptive-forms-9}

* Ao adicionar um painel para painéis repetíveis, o valor do campo suspenso no painel anterior é excluído. NPR-18772
* Campos de formulários adaptáveis marcados para aceitar apenas números inteiros também aceitam alguns caracteres especiais do teclado numérico. NPR-18680
* Um script para alterar o título do botão no evento inicializador do painel guide root não está funcionando. NPR-18476
* A barra de rolagem não é vista no painel direito para regras criadas no Editor de regras. NPR-18716

#### Aplicativo AEM Forms {#aem-forms-app}

* O Forms não é renderizado corretamente no aplicativo AEM Forms quando ele está no modo offline ou não está conectado à rede. CQ-4218368

### Instalador do Forms no JEE {#forms-jee-installer-13}

#### Serviço PDFG {#pdfg-service-3}

* O PDF Generator falha na produção de documentos PDF com níveis de marcadores especificados. Hotfix do CQ-4211102

## Pacotes OSGi incluídos no CFP7 {#osgi-bundles-included-in-cfp-1}

Lista de pacotes OSGi atualizada no AEM 6.2SP1-CFP7

[Obter arquivo](assets/do-not-localize/bundle-list-6_2sp1cfp7.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP7

[Obter arquivo](assets/do-not-localize/cfp7_content_packages.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP6 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Gerenciamento eficiente de componentes ocultos no modo de layout no tablet.
* Introdução de ações rápidas em dispositivos híbridos.
* Resolução de problemas de sincronização no nível do componente com Live Copies.

### Ativos {#assets-13}

* Um cliente é bloqueado quando o usuário que não tem a permissão necessária tenta mover uma operação em um ativo. NPR-18330; hotfix do CQ-4212560
* A mesclagem de várias configurações de serviços de conteúdo inteligente causa problemas de usabilidade. NPR-18273; hotfix do CQ-4201557
* As ações/fluxos de trabalho de check-out não estão disponíveis no console Linha do tempo uma vez aprox. Inclusão de 80 fragmentos na pasta Ativos. NPR-18257; Hotfix para CQ-4211214 e NPR-18251; Hotfix do CQ-4211216.
* O sistema falha com Falta de memória e falta de paginação durante os relatórios de Ativos. NPR-17865; Hotfix do CQ-4209759
* O vídeo publicado falha ao ser reproduzido no ativo de vídeo codificado. NPR-17849; hotfix do CQ-4210739
* A miniatura do PDF não é gerada. NPR-17831, NPR-17750; hotfix do CQ-4210547
* O trabalho de Notificação de expiração do Adobe CQ DAM não desativa os ativos expirados. NPR-17666; Hotfix do CQ-107766
* As atividades de expiração de ativos param se um ativo não tiver um proprietário atribuído. NPR-17665; Hotfix do CQ-4197946
* Uma exceção de ponteiro nulo é gerada quando uma pasta de ativos com mais de 150 referências de entrada é movida. CQ-4200981

### Sites {#sites-13}

* A personalização funciona somente para o primeiro IP quando a regra de segmentação é definida para um intervalo de IP. NPR-18121; hotfix do CQ-83767
* Falha de logon devido a NumberFormatException quando a propriedade historyShow está habilitada. NPR-18073; hotfix do CQ-101965
* As páginas excluídas marcadas estão visíveis na interface de toque. NPR-18025; Hotfix do CQ-86694
* Problemas de desempenho ao carregar uma página com públicos-alvo grandes (mais de 2000). NPR-17884; Hotfix do CQ-4209567
* Não é possível selecionar uma imagem após remover outra imagem na página. NPR-17711; Hotfix do CQ-4201323

### Plataforma {#platform-11}

* Os controles da interface de toque ficam ocultos para usuários que têm as permissões necessárias. NPR-17945; hotfix do CQ-4211231
* Tags japonesas ausentes no campo do seletor de tags. NPR-17768; Hotfix do CQ-4210456
* A consulta getsize() retorna resultados incorretos quando o FastQuerySize é ativado. NPR-18018
* O console da web na instância de espera não está acessível. NPR-17861; hotfix do Granite-14582

### Commerce {#commerce-2}

* A consulta transversal ocorre quando um blueprint de catálogo não tem nenhuma condição definida para uma seção. NPR-18229; hotfix do CQ-4211924

### Communities {#communities-2}

* PollingImporterImpl. causa atraso no encerramento do AEM. NPR-18298; Hotfix do CQ-96133

### Integrações {#integrations}

* Correção de erros de componentes de Pesquisa do AEM que podem ocorrer quando o AEM Day HTTP Client 3.1 OSGI é configurado com um Proxy que requer Autenticação Digest. NPR 18128
* Caixa de seleção para reverter a herança está ausente. NPR-17753; Solicitação de Hotfix do CQ-4210139
* Os usuários não podem configurar a prioridade ao direcionar um componente com várias atividades. NPR-18658; Hotfix do CQ-4210727
* Os usuários não conseguem navegar na pasta /etc/segmentation para selecionar um público-alvo criado na pasta /etc/segmentation/group1. NPR-18522

### Segurança {#security-1}

* O assistente de Mover ativo trava se o usuário não tiver permissão de gravação na pasta do público-alvo. NPR-18300
* Solicite o uso de uma versão atualizada do servlet org.apache.sling.servlets.post (2.3.22) na API Apache Sling para evitar uma vulnerabilidade XSS. NPR-18963

### Tradução {#translation-6}

* O envio da página do ativo não deve ser necessário novamente para um projeto de tradução até que ele seja concluído. NPR-18249; Hotfix do CQ-4209908

### WCM-Componentes do Foundation {#wcm-foundation-components-8}

* Não é possível usar o componente iparsys do WCM Foundation em modelos editáveis. NPR-18223; hotfix do CQ-4210384
* O mapa de imagem não retém as coordenadas selecionadas no componente de imagem HTL. NPR-18032; hotfix do CQ-4211584
* Quando um componente de imagem HTL é renderizado, o nome do arquivo no URL é renomeado causando a quebra do URL. NPR-17908; hotfix do CQ-4211587
* Não é possível sair das propriedades da página após fazer alterações. NPR-17832; hotfix do CQ-96110

## Forms {#forms-14}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte [Versões do AEM Forms](aem-forms-releases.md).

### Pacote complementar do Forms {#forms-add-on-package-14}

**Gerenciamento de correspondência**

* O dicionário de dados é lido repetidamente durante a renderização da carta. NPR-18482, Hotfix do CQ-4210805
* Adição do JavaDocs à classe com.adobe.livecycle.content. NPR-18467
* Ao criar uma carta, sua descrição não é salva. NPR-18039
* Quando um módulo de texto é salvo e uma expressão no módulo de texto não contém tags de expressão de abertura ou fechamento, nenhuma mensagem de erro é exibida. O módulo de texto exibe uma mensagem de erro e não é renderizado na correspondência. NPR-17798
* Erros inesperados são vistos nos logs de instalação de um pacote complementar. NPR-18295

**Gerenciador do Forms**

* A interface do AEM Forms lista todos os ativos na ordem mais antiga. Os usuários não podem reordenar os ativos na ordem mais recente. NPR-18451

### Instalador do Forms no JEE {#forms-jee-installer-14}

**Serviço de saída**

* Problema de desempenho aprimorado do Serviço de saída para o AEM Forms 6.2. NPR-18033

**Serviço de assinaturas**

* Não é possível assinar um documento PDF com um módulo de segurança de hardware remoto. NPR-18017

## Pacotes OSGi incluídos no CFP6 {#osgi-bundles-included-in-cfp-2}

Lista de pacotes OSGi atualizada no AEM 6.2SP1-CFP6

[Obter arquivo](assets/do-not-localize/6.2sp1-cfp6-bundlelist.txt)

Lista de pacotes de conteúdo atualizada no AEM 6.2SP1-CFP6

[Obter arquivo](assets/do-not-localize/6_2sp1-cfp6-contentpackagelist.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP5 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Solução de vários problemas da interface com o compartilhamento, movimentação, publicação e download de ativos.
* Maior capacidade da caixa de diálogo Mover na exibição de ativos referenciados.
* Solução de vários problemas em componentes e fluxos de trabalho do WCM, como Cancelar publicação e Limpeza de versão.
* Aprimoramento da capacidade de resposta da barra de ação ao exibir ações da barra de ferramentas e componentes do Coral.

### Ativos {#assets-14}

* Aprimoramentos de desempenho na funcionalidade de publicação no Brand Portal. NPR-17189; Hotfix do CQ-4204150
* Compartilhar um ativo usando a opção Compartilhar link não cria um arquivo zip com uma estrutura de pasta simples para download. NPR-17513; Hotfix do CQ-4209381
* Selecionar um ativo no DAM e clicar em Publicar não exibe a opção Publicar no Brand Portal na página de detalhes do ativo. NPR-17351; Hotfix do CQ-94905
* Nas etapas do fluxo de trabalho do DAM, os fluxos binários adquiridos da Sessão ou ResourceResolver devem ser fechados em um bloco final. Isso garante que não ocorram vazamentos de recursos. NPR-17385; Hotfix do CQ-4209452
* Fazer upload de um documento do Word no DAM resulta em uma exceção de ponteiro nulo e a instância do fluxo de trabalho permanece presa no estado Em execução. NPR-17160; Hotfix do CQ-4207358
* Os botões Compartilhar, Mover, Publicar e Baixar estão visíveis para ativos expirados na página Editor de metadados para usuários não administradores. NPR-16903; Hotfix do CQ-101440/CQ-104535
* Ações como Compartilhar, Mover, Publicar e Copiar devem estar visíveis para usuários administradores no console do Assets. NPR-16902; Hotfix do CQ-4207111

### Sites {#sites-14}

* Ao mover uma página usando a interface clássica ou de toque, a caixa de diálogo Mover não mostra mais do que 150 referências, impossibilitando a atualização dessas referências e que a página seja publicada novamente. Esse problema foi corrigido com a introdução de uma propriedade para a Interface clássica: “maxRefNo”, que pode ser configurada no nó de administração do site: `'/libs/wcm/core/content/siteadmin'`. Essa propriedade especifica o número máximo de referências (valor padrão 150) que são exibidas antes de uma operação de movimentação intensa. Se uma página tiver várias referências, elas não serão exibidas na caixa de diálogo movePage. Essa configuração também funciona para damadmin e miscadmin, aplicando a configuração nos nós: `'/libs/wcm/core/content/damadmin'` e `'/libs/wcm/core/content/miscadmin'` respectivamente. NPR-17222; Hotfix do CQ-85878

* Ao trabalhar com componentes WCM, os hiperlinks com espaços são removidos no Editor de Rich Text da interface para toque. NPR-17698, NPR-17570; Hotfix do CQ-4206768
* Ao disparar o fluxo de trabalho Solicitação de cancelamento de publicação das propriedades da página, erros de JavaScript são exibidos para usuários sem direitos de replicação. NPR-17294; Hotfix do CQ-102064
* A renderização ou exportação de um componente de imagem HTL altera o URL para um número, renomeando o nome do arquivo, o que causa links com falha. NPR-17245; Hotfix do CQ-59616
* A exclusão de uma inicialização em uma inicialização aninhada faz com que as inicializações secundárias fiquem órfãs. NPR-17228; Hotfix do CQ-4202639
* A execução da Limpeza de versão no AEM 6.2 com o Oak 1.4.13 aplicado causa um aviso repetido constantemente nos registros. NPR-17391; Hotfix do CQ-4206870
* Após instalar um hotfix ou uma atualização para o componente ContextHub, o pacote de conteúdo substitui todos os segmentos em /etc/segmentation/contexthub, resultando na perda de todos os segmentos personalizados do ContextHub. NPR-17250; Hotfix do CQ-79958
* Ao executar um fluxo de trabalho com grupos aninhados como usuários do fluxo de trabalho, o WorkflowStatusProvider (pageinfo.json) causa bloqueio na instância do fluxo de trabalho. NPR-17555; Hotfix do CQ-4202056
* Ao usar os componentes do editor de página WCM, existe uma grande quantidade de espaço vazio no final da página no modo de edição da interface para toque da instância do autor. NPR-17510; Hotfix do CQ-4205441
* A renderização ou exportação de um componente de imagem HTL altera o URL para um número, o que causa links com falha. NPR-17245; Hotfix do CQ-59616

### Interface {#ui}

* Selecionar um ativo e clicar em Ferramentas do desenvolvedor nem sempre exibe as ações da barra de ferramentas na barra de ações em conexões lentas e a página precisa ser recarregada. NPR-17568; Hotfix do CQ-108365
* A barra de ação deve ser atualizada para usar dois contêineres: coral-actionbar-primary e coral-actionbar-secondary, em vez de coral-actionbar-container. NPR-17591; Hotfix do GRANITE-15225

### Mobile-on-demand {#mobile-on-demand-2}

* Os usuários com permissões “Somente leitura” para o aplicativo AEM Mobile não podem visualizar conteúdos da página de gerenciamento de conteúdo do AEM Mobile. NPR-17390; hotfix do CQ-4209690

### Segurança {#security-2}

* Vulnerabilidade XSS na saída gerada por HTMLRendererServlet. NPR-17136
* Solicitação para impedir a divulgação da versão do AEM na página de feeds de sindicalização da Web do AEM. NPR-16219

### Forms {#forms-15}

#### Pacote complementar do Forms {#forms-add-on-package-15}

As correções do AEM Forms são entregues por meio de pacotes complementares e outros instaladores de patches fornecidos com a versão. Para obter mais detalhes, consulte Versões do AEM Forms.

**Formulários adaptáveis**

* Para um formulário adaptável com anexo, as entradas duplicadas para as tags afSubmissionInfo são criadas no XML enviado quando o formulário é enviado pela segunda vez. NPR-17364
* Ao usar o navegador Google Chrome, após remover um anexo de um formulário, tentar reanexar o mesmo anexo gerará um erro. NPR-17297
* Se houver painéis aninhados e repetidamente carregados com lentidão nos Formulários adaptáveis baseado em XSD ou no modelo sem formulário, os valores preenchidos no formulário não serão retidos no Documento de registro (DOR). NPR-17176
* Erros exibidos no log de erros do Editor de regras devem ser adicionados no bloco catch de um código JavaScript do bloco try/catch. NPR-16757
* Clicar em um anexo de arquivo em um formulário emite um erro de console do navegador e não exibe a pré-visualização do anexo. NPR-17174

**Gerenciamento de correspondência**

* A funcionalidade Criar interface de correspondência é quebrada em caso de texto incorporado ou de adição de uma linha em branco na interface do usuário. NPR-17748
* O navegador pisca quando uma correspondência é aberta para edição. NPR-17576
* Ao adicionar funções remotas em elementos de dicionário de dados computados, se o número de funções for maior que o comprimento da guia mostrando funções remotas, a barra de rolagem não aparecerá na guia. NPR-17359
* O método de API `com.adobe.icc.services.api.LetterInstanceService` para importar não funciona. NPR-17922, NPR-16008
* Uma variável adicionada em um módulo de texto não é visível no painel Vínculo de dados ao editar uma correspondência. NPR-17940
* A interface do gerenciamento de correspondência não inicia quando a ação de envio de HTML usa o método POST. NPR-17595

**Gerenciador do Forms**

* Com um formulário adaptável configurado para AB testing, clicar em Iniciar AB testing não inicia o teste e dá um erro no console do navegador. NPR-17838

**Serviço do Forms**

* Os problemas relatados na análise de código estático do OSGI Forms devem ser corrigidos. NPR-13951

#### Instalador do Forms no JEE {#forms-jee-installer-15}

**Serviço de saída**

* O uso do serviço de saída do AEM Forms 6.2 para mesclar um formulário específico com um XML de dados leva 20 vezes mais tempo. Isso foi corrigido em ambientes Windows e Linux®. NPR-17501

**Instalar o LCM**

* Depois de instalar a build do AEM Forms 6.2 GM e aplicar o AEM 6.2 CFP, executar o Gerenciador de configurações do LiveCycle exibe um ponto-e-vírgula indesejado nas Informações da versão e a data de instalação do patch não é atualizada. NPR-14322

**Gerenciamento de processos**

* A variável TaskContext não é preenchida para processos do AEM Forms. CQ-4211857

#### Pacote do AEM Forms JEE {#aem-forms-jee-bundles-package}

* Os recursos dos usuários de formulários, seja usando o console da interface de administrador JEE ou o console OSGi, devem ser os mesmos. NPR-17670

### Pacotes de recursos incluídos no CFP5 {#feature-packs-included-in-cfp}

**Pacote Forms JEE**

Gerenciamento de processos -HTML Workspace

* Ao atribuir uma etapa do espaço de trabalho, a guia anexos do espaço de trabalho deve mostrar um contador para os anexos ou observações, caso haja mais de um anexo ou observação. NPR-17771
* Solicitação de suporte para o Office 365 no AEM JEE Forms para recursos de email no fluxo de trabalho do formulário. NPR-13866

**Pacote complementar do Forms**

Gerenciamento de correspondência

* Ao editar fragmentos no editor de texto durante uma visualização de carta, o texto processado deve ser exibido para edição, ao invés das condições em linha usadas nos fragmentos. NPR-15748, NPR-17504

### Pacotes OSGi incluídos no CFP5 {#osgi-bundles-included-in-cfp-3}

Lista de pacotes OSGi atualizados entre o AEM 6.2 SP1 e CFP5

[Obter arquivo](assets/do-not-localize/cfp5_osgi_bundles.txt)

Lista de pacotes de conteúdo atualizados entre o AEM 6.2 SP1 e CFP5

[Obter arquivo](assets/do-not-localize/content-package-cfp5.txt)

O AEM Cumulative Fix Pack 6.2 SP1-CFP4 é uma atualização importante que inclui correções essenciais para o cliente lançadas desde a disponibilização geral do AEM 6.2 SP1.

Os principais destaques desse Cumulative Fix Pack são:

* Correções em ativos para representação de arquivo Camera Raw, visualização da linha do tempo e orientação da imagem
* Melhoria nas

   * inicializações do WCM para sites
   * Fluxo de trabalho de projetos
   * Componentes do ContextHub

* Correções para o Campaign, Mobile On-Demand e Tradução
* Melhorias de usabilidade no Editor de regras para Formulários adaptáveis
* Aprimoramento do Editor de condições embutido para o Gerenciamento de correspondência em formulários
* Correções do gerenciamento de processos e do serviço de saída para o AEM Forms em JEE
* Correção relacionada ao Designer do Forms para o Editor de scripts

### Plataforma {#platform-12}

* A adição ou personalização de colunas para os resultados do **Assets OmniSearch** sobrepondo em `/apps` não funciona. NPR-16737: hotfix do CQ-4206785
* A página **Ferramenta de diagnóstico** não funciona após uma atualização local do AEM 6.1 SP2 para o AEM 6.2 SP1. NPR-17121; Hotfix do CQ-4196786
* HTL: ao selecionar um fórum, criar um tópico e uma publicação, o `Sightly SightlyCompiledScript` adiciona a propriedade `addSelectors` incorreta à `RequestDispatcherOption`. NPR-17008: Hotfix do GRANITE-16384

* Inclusão de suporte para `CRON expressions` em `ManagedPollConfigs` usado pelo `ReportImporter`. NPR-16608: Solicitação de Hotfix do CQ-4206066

* Falha ao fazer upload de uma imagem de avatar para um usuário LDAP. NPR-16561; Hotfix do Granite-17013
* O número de resultados exibidos na tela Gerenciamento do usuário é diferente na exibição de Cartão e lista. NPR-16241; hotfix do GRANITE-16914
* Falha no carregamento de notificações de fluxo de trabalho ao exibir no navegador Google Chrome com o modo de tela cheia. NPR-17013: hotfix do CQ-4207567

### Ativos {#assets-15}

* A orientação da imagem não é aplicada corretamente ao importar uma imagem com uma orientação definida. NPR-16750: Hotfix do CQ-4204356
* A visualização Linha do tempo do Assets não exibe nenhum ativo, mesmo que &quot;Mostrar tudo&quot; esteja definido por padrão. NPR-16957: Hotfix do CQ-98780
* Os arquivos `Camera RAW` (incluindo ARW, CR2, NEF, DNG e EPS), quando adicionados como representação em ativos, não podem ser selecionados ou excluídos. Esses arquivos são baixados automaticamente quando o usuário clica neles. NPR-16949: hotfix do CQ-4206846
* Criar um PDF dentro de outro na Interface do Assets não exibe os PDFs criados na interface do DAM. No entanto, os PDF ficam visíveis no repositório do CRX. NPR-16833: Hotfix do CQ-4206501
* Fazer upload de um ativo como um nó filho a partir de si mesmo usando a interface para toque causa um problema. O ativo é carregado como um filho direto do ativo selecionado anteriormente. NPR-16534: Hotfix do CQ-4204287
* Na interface do DAM, comentar em um ativo e marcar um usuário no comentário não gera uma notificação por email. NPR-16589: Hotfix do CQ-102318

### Projetos {#projects-3}

O console de fluxo de trabalho de projetos mostra uma NullPointerException na página quando os fluxos de trabalho são eliminados. NPR-17017: hotfix do CQ-4194269

### Sites {#sites-15}

* Os arquivos no `ContextHub` não são minimizados na instância do autor. NPR-17022: Hotfix do CQ-79456
* A promoção de inicialização do WCM-Launches demora muito para promover um lançamento que consiste em uma grande árvore de uma página. NPR-16480: Hotfix do CQ-82731
* `ClientContext` O Renderizador de condição de segmento falha quando um segmento (ou público-alvo) é criado com uma regra inoperante ou inacabada. NPR-16759: Hotfix do CQ-4205104
* Em WCM Launches, as páginas associadas a um lançamento não podem ser ter a publicação cancelada quando a ação é iniciada nas propriedades da página na interface de toque. NPR-16560: Hotfix do CQ-4204681
* Vincular o Rewriter regrava falsamente os valores href contendo dois pontos, presumindo que o dois pontos “:” definem um namespace JCR. NPR-16753: Hotfix do CQ-4203762
* No importador do WCM-Design, abrir uma página do importador de teste e tentar fazer upload de um arquivo zip causará problemas se o upload desse já tiver sido feito e excluído anteriormente. NPR-16486: hotfix do CQ-90962
* Acessar o painel **[!UICONTROL Navegação global]** usando os navegadores Firefox ou Google Chrome proporciona uma experiência de usuário diferente. O navegador Firefox exibe o menu **[!UICONTROL Ferramentas]**. O navegador Google Chrome mostra o menu **[!UICONTROL Navegação]**. NPR-16770; hotfix do CQ-4200456

### Campaign {#campaign}

* Ao testar modelos de campanhas do AEM e modificar seed addresses para incluir “Dados adicionais”, o menu suspenso do Adobe Campaign desaparece no Context Hub da interface de toque. NPR-16771: hotfix do CQ-105748

### Mobile on-demand {#mobile-on-demand-3}

* Ao simular uma publicação do autor do AEM, uma ação de simulação que leva mais de cinco segundos causa um pico incomum no painel do Splunk da integração AEMM - AEM PECS, com um grande número de solicitações de status. NPR-16908: Hotfix do CQ-4207055
* O gerenciamento de configuração do AEM Mobile falha após a instalação da atualização AEM-6.2-SP1-CFP1-1.0. NPR-16909: Hotfix do CQ-4204892

### Tradução {#translation-7}

* A visualização de trabalhos de tradução não funciona após a instalação do 6.2 SP1 - CFP1. NPR-16481; Hotfix do CQ-4204655
* A cópia de idioma criada usando a tradução aponta para a raiz principal em vez da live copy do país local. NPR-17257; Hotfix do CQ-4208287

### Segurança {#security-3}

* Nenhuma validação de tipo MIME é executada ao fazer upload de binários de arquivos para o AEM. NPR-16617
* Problemas com o upload de imagens de avatar de usuários do LDAP. NPR-16561

### Forms {#forms-16}

#### Pacote complementar do Forms {#forms-add-on-package-16}

**Formulários adaptáveis**

* No Editor de formulários adaptáveis, o comentário Configuração de público-alvo em head.jsp deve ser substituído pela nova instrução do Context Hub. NPR-17173
* No Editor de regras de formulários adaptáveis, a opção **[!UICONTROL Escolher um item]** mostra o evento como “nulo”. NPR-17139
* O formulário enviado é reenviado ao navegar para frente usando a seta para frente (>). NPR-17080
* Ao enviar um formulário adaptável via AJAX, a função de retorno de chamada “erro” nunca é invocada em caso de erro. NPR-17034
* Clicar no botão **[!UICONTROL Salvar formulário]** no Editor de regras em tempo de execução não salva o formulário. NPR-16905
* O texto estático deve ser excluído da ordem de tabulação no Formulário adaptável. NPR-16749
* O valor calculado de um campo decimal é exibido incorretamente. NPR-16596
* O ícone para exibir o conteúdo da Ajuda deve ser incluído na ordem de tabulação dos Formulários adaptáveis. NPR-16484
* Suporte para expressão regular do tipo `dataRef=C:/Users/`na **[!UICONTROL Configuração do serviço de preenchimento prévio padrão]**. Esse tipo é para preenchimento prévio de dados de formulários adaptáveis. NPR-16425

* As validações não são acionadas corretamente para todos os painéis se houver um cenário de lazy-load aninhado. NPR-15821

**Gerenciamento de correspondência**

* A representação de correspondências falha se uma correspondência contiver um módulo de texto em branco (sem texto). NPR-17054
* Quebras de linha e espaços de tabulação são removidos do conteúdo depois de serem colados no Editor de texto. NPR-17039
* A exibição de referências de um módulo de texto leva muito tempo se o módulo de texto for referenciado em muitas correspondências. NPR-17035
* A edição, salvamento, exclusão e definição de referência para fragmentos de documento leva muito tempo. NPR-17033
* O texto justificado é renderizado em uma fonte diferente ao visualizar a correspondência. NPR-16976
* A funcionalidade de pesquisa não funciona corretamente se o texto pesquisado tiver várias ocorrências. NPR-16920
* A barra de ferramentas do Editor de texto é exibida intermitentemente no navegador. NPR-16919
* A criação **[!UICONTROL Salvar formulário]** do Editor de regras não funciona. NPR-16905
* O menu suspenso Fonte não preenche a família de fontes ao criar um módulo de texto com base no Dicionário de dados usando o Internet Explorer. NPR-16944
* Depois de criar um fragmento de texto, a fonte de correspondência muda na visualização da carta. NPR-16830
* Correspondências com espaços de tabulação no início ou entre expressões no fragmento de documento não podem ser renderizadas ou visualizadas. NPR-16769

**Formulários para publicação de conteúdo para dispositivos móveis**

* A pré-visualização do Formulário para publicação de conteúdo para dispositivos móveis mostra conteúdo sobreposto, embora o formulário seja exibido corretamente para renderização em PDF. NPR-17105

**Portal do Forms**

* Clicar no link **[!UICONTROL Download]** para um formulário enviado abre uma página HTML em vez de um formulário PDF. NPR-17082

* `Upload Comments` para anexos de arquivo não é exibido na interface para instâncias enviadas, embora esteja presente no XML armazenado no repositório do CRX. NPR-17075

**Serviço de extensões do Reader**

* Um arquivo específico não tem extensão do Reader na instalação do AEM Forms OSGi. NPR-16625

#### Instalador do Forms no JEE {#forms-jee-installer-16}

**Núcleo**

* Durante o processo de atualização, o Gerenciador de configurações falha com o tempo limite. NPR-16774 (Consulte [Configurar tempo limite para operações no nível do componente](install-cfp-aem-forms-jee.md#configuring-timeout-for-operations-at-component-level-npr)).

**Gerenciamento de processos - HTML Workspace**

* O ponto de partida de uma tarefa de Iniciar não começa com os dados enviados no momento do envio do ponto de partida. NPR-16917
* Clicar no botão **[!UICONTROL Retornar]** para um formulário no workspace HTML não fecha o formulário, mas o retorna à fila do grupo.
NPR-16352

**Gerenciamento de processos**

* Permite que os usuários definam o nome de exibição de tarefas anteriores para qualquer uma das tarefas seguintes em uma instância do processo. NPR-15382

**Serviço de saída**

* O serviço de saída não processa um PDF que foi modificado para incluir um campo adicional de “milli-sec” nos metadados do `date-time format`. NPR-16838

#### Designer do Forms {#forms-designer}

* O Editor de scripts do AEM Designer não respeita os padrões das Propriedades do formulário para `Calculate Event`e `Validate Event`. NPR-15921

### Pacotes de recursos incluídos no CFP4 {#feature-packs-included-in-cfp-1}

**Pacote complementar do Forms**

* Aprimoramento no Editor de condições embutido para o Gerenciamento de correspondências. NPR-10981

### Pacotes OSGi incluídos no CFP4 {#osgi-bundles-included-in-cfp-4}

Lista de pacotes OSGi atualizados entre o AEM 6.2 SP1 e o CFP4

Os principais destaques do CFP3 são:

* Recurso de pesquisa mais eficiente para a Interface clássica e para o componente de Pesquisa do AEM usando proxy com autenticação Digest
* Correção de problemas ao carregar ativos e exibir metadados de ativos
* Correção de problemas ao criar pastas e mover páginas, caso o título tenha caracteres especiais.
* Correções para usar públicos-alvo de sincronização de direcionamento, publicar campanhas e selecionar métricas de meta na interface de toque
* Resolução de problemas de sincronização para trabalhos de tradução
* Oferece segurança aprimorada para o serviço de preenchimento prévio do Forms
* Melhorias no rascunho do portal de formulários, no componente de envios e no serviço de formulários com códigos de barras
* Melhorias de usabilidade para formulários adaptáveis que contêm widgets de anexos de arquivos ou fragmentos carregados lentamente.
* Melhorias de usabilidade no Gerenciamento de correspondências, incluindo recursos de pesquisa aprimorados, registro de ativos excluídos e importação de dicionários de dados.

### Plataforma {#platform-13}

* Uma condição de raça em **ModelAdapterFactory**, que é possível quando dois threads tentam injetar o mesmo campo, resulta em falha ao construir o modelo. NPR-16443: Hotfix do SLING-6584
* Opção de validação no Gerenciador de pacotes para detectar conflitos entre o arquivo sobreposto (arquivo JSP ou JavaScript) em `/apps` e aquele contido em um hotfix em `/libs`. A sobreposição afetada pode então ser rebaseada para incluir alterações do arquivo em `/libs`. NPR-16216: hotfix do CQ-81729
* O registro no error.log às vezes para por alguns segundos após iniciar o editor e precisa ser limpo para uma nova execução. Solicitação de atualização da estrutura de registro e fornecimento de registro Sling. NPR-15913: Hotfix do Granite-15452
* Solicitação de atualização da API &quot; `use"` do JavaScript para evitar falhas na implementação da API de uso do HTL JavaScript. NPR-16461: Hotfix do SLING-6780

### Sites {#sites-16}

* Após a atualização do AEM 6.0 para o AEM 6.2, a interface clássica mostra um desempenho lento ao pesquisa tags devido a várias consultas. Para resolver o problema, as etapas mencionadas em [Desabilitar status de replicação no console de tags (Interface clássica)](#disable-replication-status-in-tagging-console-classic-ui-npr) podem ser seguidas. NPR-15842: hotfix do CQ-4201748.

* Ao criar uma página na interface de toque, a verificação de entrada para o campo “nome” não verifica o caractere especial “Apóstrofo” (o mesmo que na interface clássica). Portanto, a página não pode ser movida. NPR-16404: Hotfix do CQ-4205321.
* Aplicar estilos diferentes em duas linhas no Editor de Rich Text e depois mesclá-los remove o estilo aplicado na segunda linha. NPR-16389: Hotfix do CQ-4203835.
* Na tela de sites da interface de toque, tentar colar uma página dentro de uma página sem subpáginas não funciona, pois o botão Colar fica indisponível. NPR-15894: hotfix do CQ-4201696.
* Ao rolar a guia Páginas no painel Localizador de conteúdo, alguns conjuntos de páginas são exibidos indefinidamente na interface clássica, enquanto a interface de toque mostra um conjunto limitado de poucas páginas não repetidas. NPR-16271: Hotfix do CQ-4202371
* A abertura das Propriedades da página de uma Live Copy na interface para toque e o clique em Salvar, sem qualquer alteração, anuncia qualquer guia da Live Copy e cria um nó de configuração da LiveSync. NPR-16327: Hotfix do CQ-108562
* A restrição de formulários não consegue ler a propriedade `ConstraintMessage`. NPR-16388: Hotfix do CQ-101330
* O componente `wcm/foundation/components/parsys` não exibe o espaço reservado **[!UICONTROL “Arraste componentes aqui]**”. NPR: 16748: Hotfix do CQ-4205187

### Ativos {#assets-16}

* O rasterizador pdf para de funcionar e causa problemas de memória após a instalação do 6.2 SP1 ou do Hotfix 12430. NPR-15991
* Os metadados de uma propriedade de cadeia de caracteres, `documentNumber`, são exibidos como uma data, mas deveria ser um número. NPR-16134: Hotfix do GRANITE-16916
* Truncamentos de texto no balão de eventos da linha do tempo. NPR-16226: Hotfix do CQ-85226
* Quando uma pasta é criada na hierarquia de conteúdo com um título contendo caracteres especiais, a versão codificada desses caracteres é exibida. NPR-15935: hotfix do CQ-4202987
* O usuário não pode fazer upload de ativos ou criar pastas enquanto navega por ativos devido ao comportamento inconsistente exibido ao usar o botão “Criar”. NPR-16410: Hotfix do CQ-4204793
* Erros inesperados são encontrados durante o upload de recursos HTML compartilhados da visualização de artigos no AEM Authoring. NPR-16133: Hotfix do AEMM-4155970

### Integração {#integration-14}

* Ao habilitar a autenticação de proxy com a autenticação Digest, o componente de Pesquisa do AEM gera uma ConcurrentModificationException. NPR-15309: hotfix do CQ-4199191
* Ao criar uma atividade de teste A/B de destino no AEM, o público-alvo não sincroniza com o destino e mostra “nenhum público-alvo”. NPR-16229: Hotfix do CQ-4204210
* Depois de instalar o SP1+NPR-11577 v1.2, ao escolher &quot;Usar uma métrica do Analytics&quot; para a Métrica alvo enquanto segmenta na interface para toque, a lista suspensa de métricas nunca é carregada. NPR-16129: Hotfix do CQ-4204316
* Ao usar o direcionamento, a publicação da campanha não publica automaticamente a árvore inteira, incluindo a marca e a parte principal. NPR-15855: hotfix do CQ-94630

### Tradução {#translation-8}

* O trabalho de Sincronização de tradução agora é acionado automaticamente e a pesquisa do AEM ocorre sem executar o poke nos projetos de tradução. NPR-15163: hotfix do CQ-90856

### Forms {#forms-17}

#### Pacote complementar do Forms {#forms-add-on-package-17}

**Formulários adaptáveis**

* Ao salvar um formulário adaptável com um anexo, o caminho completo do anexo é adicionado à tag `fileAttachment` do XML gerado, em vez do nome do anexo. NPR-16529
* Em formulários adaptáveis baseados em XDP, o invólucro `afData/afBoundData` está presente no XML enviado, embora mesmo o XML de preenchimento prévio não tenha invólucros `afData/afBoundData`. NPR-16118

* Notação exponencial no campo Número: Ao usar formulários adaptáveis, se um número com uma fração decimal que exceda dez caracteres no total for inserido, o número se tornará uma notação exponencial no XML enviado. NPR-16106
* Para formulários que contêm um componente de anexo de arquivo e um fragmento carregado lento, o xml de dados enviado não contém as informações do componente de anexo de arquivo. NPR-16022
* Para um painel repetível de carregamento lento que não tenha um ancestral repetível, os filhos repetíveis dentro de uma segunda instância do painel não serão repetidos. NPR-15944
* Ao tentar salvar um fragmento dentro de outro no editor de formulários, a raiz do modelo de fragmento não preenche o valor do fragmento secundário. NPR-15943
* Ao criar uma caixa de seleção com apenas um item e tentar mostrar o título da caixa de seleção mantendo o título do item oculto, a ação de criação de dicionário acionará um `ArrayIndexOutOfBoundException` se o texto do item estiver vazio. O dicionário não é criado e nenhuma resposta de erro é gerada na tela. NPR-15816
* Para formulários adaptáveis com dispositivos de anexo de arquivo, algumas partes do formulário são desabilitadas depois que o arquivo anexado é visualizado.
NPR: 16611

* Para dispositivos de anexo de arquivo que permitem vários anexos, o envio de uma nova instância de formulário com um anexo em um dispositivo que já tem um anexo anterior resulta na exibição de um código de erro. Esse erro ocorre ao abrir o anexo adicionado em vez do conteúdo real. NPR-16258
* Proteção do serviço de preenchimento prévio de formulários do acesso não autorizado por meio de protocolos como `file://`, `http://` e `ftp://`. Consulte [Configuração do Serviço de pré-preenchimento com o Gerenciador de configuração](https://experienceleague.adobe.com/br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15414

* Solicite a renderização do formulário adaptável em formato PDF em vez de HTML na etapa de verificação e anexe todos os arquivos ao PDF para que a impressão exiba o formulário completo. NPR-9011

**Gerenciamento de correspondência**

* Ao trabalhar com fragmentos de texto em uma carta no modo Visualização ou Edição, se o texto for convertido em lista, a funcionalidade da carta inteira será interrompida e um erro de JavaScript é gerado. NPR-16460
* A importação de um arquivo XSD para criar um dicionário de dados no nó Gerenciamento de correspondências falha, pois o navegador fica sem responder toda vez que é feito o upload do XSD e o nó de raiz é selecionado. Esse problema independe do navegador e não aparece nos registros do servidor. NPR-16452
* Ao visualizar uma correspondência usando o navegador Internet Explorer e tentar editar o tamanho da fonte do conteúdo, os valores duplicados são vistos de 8 a 72 na lista suspensa do tamanho da fonte. NPR-16387
* Se um campo flutuante aparecer como um campo de entrada de um fragmento XDP, o campo não se expande na pré-visualização da carta ao usar o navegador Internet Explorer. NPR-16367
* Ao tentar enviar uma correspondência diretamente da pré-visualização, o pop-up para o nome da correspondência não é exibido corretamente por estar oculto. NPR-16353
* Os espaços de linha adicionados ao editar uma correspondência não são refletidos na janela de Pré-visualização. Para listas em fragmentos de texto, a saída PDF não mostra o espaçamento correto. NPR-16267
* Ao trabalhar em um fragmento de documento de texto usando o navegador Internet Explorer, a tentativa de fornecer recuo ao texto falha porque o cursor não permite o recuo do texto. NPR-16128
* Adicionar ou modificar um dicionário de dados em um fragmento de documento de texto leva muito tempo e a pessoa nem sempre é notificada. NPR-16102
* Ao visualizar uma carta com conteúdo rolável usando o navegador Internet Explorer, a barra de rolagem do navegador se sobrepõe à barra de rolagem da carta. Dessa forma, o conteúdo completo não pode ser visualizado para fragmentos no lado direito. NPR-16068
* Ao criar ou editar fragmentos de documento de texto usando o navegador Google Chrome, o menu suspenso de seleção de cores aparece automaticamente e não pode ser removido. O usuário precisa selecionar lista como o tipo de entrada de dados para poder editar o fragmento. NPR-16067
* Ao usar a API `Letterinstance`, o método `import com.adobe.icc.services.api.LetterInstanceService` não funciona. NPR-16008
* A alteração dos formatos de exibição de data para `locale=en_US; dateFormat=MMM dd,yyyy;` na Configuração do compositor de ativos não funciona como esperado e o formato de data é exibido como caracteres inválidos. NPR-16007
* O tipo de vinculação de dados nas cartas durante a recriação é exibido como “Usuário”, mesmo se tiver sido definido de maneira diferente anteriormente. NPR-16619

**Portal do Forms**

* Os cenários de atualização para componentes de rascunho e envio não funcionam com a implementação da amostra do banco de dados. NPR: 16752

**Serviço do Forms com código de barras (BCF)**

* A análise de código estático do Serviço do Forms com código de barras (BCF) relata problemas. NPR-13855

#### Instalador do Forms no JEE {#forms-jee-installer-17}

**Gerenciamento de processos – Espaço de trabalho HTML**

* Proteger o serviço de preenchimento prévio de formulários de acesso não autorizado por meio de protocolos como “file://,” “http://,” e ftp://.  Para obter detalhes, consulte [Configuração do serviço de pré-preenchimento usando o Gerenciador de configuração](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions). NPR-15434

**Gerenciamento de usuários**

* A tela de logon SAML mostra a versão incorreta (6.1.0) no servidor do AEM 6.2. NPR-13825
* Com o AEM Forms configurado para autenticação de Logon único (Kerberos), se a autenticação do usuário falhar ao tentar fazer logon, um código de erro &quot;404&quot; será retornado. O usuário é redirecionado para o site de logon somente depois de atualizar a página. NPR-15015

#### Designer do Forms {#forms-designer-1}

* A alteração da localidade do formulário para francês (Canadá) na verificação ortográfica do dicionário não funciona no AEM Forms Designer.
NPR-15896

### Pacotes de recursos incluídos no CFP3 {#feature-packs-included-in-cfp-2}

**Pacote complementar do Forms**

* Ao excluir qualquer ativo no Gerenciamento de correspondência, uma mensagem de aviso deve ser registrada no arquivo error.log. NPR-13225
* Aprimore a funcionalidade de pesquisa ao visualizar uma carta no Gerenciamento de correspondência para habilitar a pesquisa de texto no conteúdo do fragmento de texto, em vez de pesquisar somente o título da carta ou o rótulo. NPR-16103

### Pacotes OSGi incluídos no CFP3 {#osgi-bundles-included-in-cfp-5}

Lista de pacotes OSGi atualizados entre o AEM 6.2 SP1 e o CFP3

[Obter arquivo](assets/do-not-localize/osgi_bundle_list_for_aem-6.2sp1-cfp3.txt).
Os principais destaques do Pacote de correções cumulativo 2 são:

* Correções de estabilidade e melhorias de desempenho na plataforma do AEM, incluindo a estrutura Sling e as operações
* Aprimoramento do gerenciamento de ativos com várias correções para acessar, mover, pesquisar, fazer upload e publicar de ativos
* Aprimoramento da criação e do gerenciamento de sites com correções em Fragmentos de conteúdo, plug-in de âncora, apresentação de slides e componentes do Context Hub
* Várias correções na interface para toque, incluindo o editor de texto, o Omnisearch e o processo de criação de variantes
* Melhorias nos fluxos de trabalho de tradução. Aprimoramento do conector da Microsoft® para usar novas APIs de tradução no portal do Azure
* Correções em Projetos e no Campaign
* Aprimoramento de criação e gerenciamento com correções em formulários adaptáveis, no gerenciamento de correspondências e nos recursos do portal de formulários
* Correções nos componentes do núcleo do Forms JEE, XTG e HTML workspace

### Plataforma {#platform-14}

* O `SlingPostProcessor` é acionado se a página que faz referência direta à estrutura Sling for editada. NPR-15754: Hotfix do CQ-104153

* O valor das tags com a propriedade `tagBasePath` não é obtido na caixa de diálogo da interface clássica ao navegar para um componente de página. NPR-15543: Hotfix do CQ-4199950

* Durante a execução de operações Sling, se houver um trecho chamado “chunk_n_n-1”, o `SlingFileUpload handler.getLastChunk` é executado em infindáveis loops com trechos vazios. NPR-15455: Hotfix do SLING-5701

* Quando uma interface estende outra interface, os métodos injetáveis na superinterface não são inseridos corretamente. NPR-15202: Hotfix do SLING- 5710
* Uma possível exceção de ponteiro nulo não é evitada ao usar a chamada de função `com.adobe.granite.infocollector.impl.FilesTraversal`. NPR-15169 Hotfix do CQ-4197640
* O estado do fluxo de trabalho é inconsistente para alguns nós secundários e o erro é exibido ao despachar eventos de observação para esse nó. NPR-15701: Hotfix do GRANITE-13786
* Um usuário seleciona um nó no CRXDE (por exemplo, `/content/dam/`). A seguir, clica na guia “Controle de acesso” para confirmar se existe uma Lista de controle de acesso. Agora, arrastar e soltar alguns elementos move esses elementos, não o selecionado. NPR-15696 Hotfix do GRANITE-16300
* Selecionar um usuário na lista suspensa ao tentar representar faz com que o pop-up inteiro do usuário desapareça. NPR-15774: HotFix do CQ-4201738/GRANITE-11895
* No Omnisearch, a pesquisa por tags com sugestões preenchidas automaticamente não funciona. NPR-15088: hotfix do GRANITE-14426.
Observação: essa correção exige o Oak CFP 1.4.11 ou superior.

### AEM Author para Publicação de conteúdo para dispositivos móveis {#mobile-aem-author}

* Ao usar os pacotes do AEM Mobile e ContentSync com um aplicativo híbrido, o AEM responde a uma solicitação de busca (com carimbos de data e hora) feita pelo aplicativo com o pacote mais antigo, em vez da solicitação feita pelo aplicativo. NPR-15749: Hotfix do CQ-104153

### Sites {#sites-17}

* O status de modificação da caixa de entrada do fluxo de trabalho no núcleo do WCM não é alterado se o usuário modificar uma página depois de ativar um fluxo de trabalho. NPR-15684: hotfix do CQ-4196974
* O plug-in Âncora no Editor Rich Text para interface de toque gera HTML5 não compatível ao clicar no ícone de âncora e adicionar um nome. Um atributo “id” deveria ser adicionado em vez do atributo “name” na tag HTML5 do elemento âncora. NPR-15650: Hotfix do CQ-89782
* Quando um esquema de metadados com vários campos é criado e aplicado aos metadados do fragmento de conteúdo, nenhuma barra de rolagem é criada na tela de metadados do fragmento de conteúdo, impossibilitando a edição dos campos. NPR-15478: hotfix do CQ-4202622
* A edição do componente de campo `TagInput` não mostra os valores configurados anteriormente nos campos da caixa de diálogo. NPR-15464: hotfix do CQ-4200360

* Na interface do Editor de fragmento de conteúdo, caso variações de um fragmento de conteúdo sejam criadas, o painel lateral não mostra a barra de rolagem para navegar por todas as variações. NPR-15445: HotFix do CQ-4199444
* Quando os usuários são removidos de grupos diretos, eles são adicionados a grupos herdados. NPR-15400: Hotfix do CQ-98758
* Criação de WCM: O autor da interface para toque não permite a edição de páginas que têm vírgulas no nome. NPR-15396: Hotfix do CQ-4199723
* Ao usar a interface para toque para criação, a função `Granite.author.editableHelper.doSelectParent` passa argumentos na ordem errada, gerando um erro de JavaScript. NPR-15349: Hotfix do CQ-4198594
* O segmento ContextHub exibe a experiência mesmo se o cookie de opção de não participação estiver presente. NPR-15293: Hotfix do CQ-4198024
* O componente de Apresentação de slides na interface clássica não pode criar slides ou arrastar e soltar imagens para criá-los. NPR-15281: hotfix do CQ-4194164
* Para usuários, independentemente da permissão, são exibidas as opções “Criar”, como Criar página, Criar site, Criar live copy, Criar inicialização e Criar itens do menu Catálogo no Admin Console do site. NPR-15278: Hotfix do CQ-94436
* Depois de instalar o AEM 6.2 Service Pack 1, o controle deslizante &quot;Incluir subpáginas&quot; para de funcionar para inicializações de página. NPR-15230: Hotfix do CQ-4198449
* Solicitar o aprimoramento da Limpeza de versão para buscar e processar versões em blocos e para poder usar um caminho especificado em uma consulta XPath. NPR-15186: hotfix do CQ-109205
* O botão Limpar está ausente na guia de miniaturas de propriedades da página no componente de Sites. NPR-15143 hotfix do CQ-4196997
* Para um site que usa Live Copies, marcar a caixa de seleção “Live Copy” no painel Colunas no Admin Console do site não exibe o status da Live Copy corretamente e apenas a marcação HTML é mostrada. NPR-15108: Hotfix do CQ-97086
* Ao editar os Fragmentos de conteúdo, se o usuário clicar em Concluído (“√”) para editar antes de obter a resposta da publicação, o conteúdo editado não será salvo corretamente. NPR-15014: Hotfix do CQ-4194095
* Fechar a página Editar durante o modo Timewarp e tentar reabri-la na administração do site resulta em um erro com o status `500`. NPR-14965: Hotfix do CQ-109647:
* Na interface do Digital Asset Manager (DAM), a pesquisa Seletor de usuários para localizar autorizações gera uma exceção de &quot;Memória insuficiente&quot;. NPR: 15307: HotFix do CQ-98542

### Ativos {#assets-17}

* Depois de pesquisar um ativo no Omnisearch, selecionar um ativo e tentar editar as propriedades clicando em **Propriedades da exibição** e, em seguida, no botão **Salvar** redireciona os usuários para uma página em branco. NPR-15900: Hotfix do CQ-4202372
* A interface do usuário do Assets não responde aos eventos. Selecionar um ativo e clicar em &quot;Publicar&quot; ou &quot;Representações&quot; não resulta em nenhuma atividade. NPR-15828: Hotfix do CQ-4202247
* Ao publicar um ativo da visualização de cartão, o cartão não é atualizado para refletir um estado publicado. Em vez disso, a página é atualizada. NPR-15826: HotFix do CQ-102732
* Hotfix cumulativo contendo Hotfixes de ativos. NPR-15225
* Se o caractere E comercial (“&amp;”) for incluído no nome de uma pasta de ativos, o nome da pasta não será exibido corretamente ao navegar para o ativo. NPR-15775: Hotfix do CQ-4201735
* O uso do caractere E comercial (“&amp;”) no nome de um arquivo de ativo causa problemas ao acessar suas propriedades. NPR-15770: Hotfix do CQ-4201737
* Ao navegar pelos ativos e usar o modo de exibição “Visualização da coluna”, se o usuário atualizar a página após selecionar e clicar em um ativo, os detalhes do ativo serão exibidos em vez do conteúdo atualizado. NPR-15768: Hotfix do CQ-4201727
* A assimilação de PDS consome até 100% da utilização da CPU com um monte de bibliotecas para serviços pdf. NPR-15606 HotFix do GRANITE-12929
* O acesso à interface “Meus compartilhamentos de link” usando o navegador Firefox não exibe os itens compartilhados nem os usuários, e a tela não pode ser usada. NPR-15539: hotfix do CQ-4200992
* Ao usar o Digital Asset Manager, se uma página estiver associada a um conjunto de imagens, mover as imagens para uma nova pasta interrompe essa associação. Dessa forma, a página associada perde algumas das imagens. NPR-15538: Hotfix do CQ-111479
* No componente Visualizador do DAM, o uso do modo de execução “nosamplecontent” causa erros na mídia dinâmica. NPR-15449: Hotfix do CQ-4195425
* Ao criar perfis de vídeo, se for escolhida uma predefinição de codificação de vídeo de alta qualidade e outra de qualidade média ao mesmo tempo, as alterações feitas não serão salvas. NPR-15447: hotfix do CQ-4195482
* Embora o upload de um ativo para o Brand Portal falhe devido à resposta a erros do servidor, o status é atualizado para “Publicado” na interface do Brand Portal, dificultando o rastreamento do arquivo perdido. NPR-15442: hotfix do CQ-4197968
* Ao publicar uma pasta de ativos no Brand Portal, no qual a publicação leva mais de uma hora, não é possível publicar alguns dos arquivos. NPR-15441: hotfix do CQ-4199493
* Ao usar o console do Localizador de ativos na visualização de colunas, a tentativa de criar uma pasta falha, e só é bem-sucedida a partir da segunda tentativa. NPR-15370: hotfix do CQ-4199448
* Se um ativo ou pasta selecionada na interface do DAM tiver uma vírgula no nome, a guia Referências não estará disponível e exibirá a mensagem “A Lista de referências não está disponível para várias seleções”. NPR-15362: Hotfix do CQ-4199721
* A publicação de uma pasta no Brand Portal não altera o estado publicado da pasta, mesmo que os ativos da pasta sejam publicados com êxito. NPR-15292: Hotfix do CQ-4197667
* Ao navegar para o console do Assets na interface para toque, uma exceção é exibida ao ativar determinados ativos. NPR-15217: HotFix do CQ-108779
* Publicação de um vídeo no YouTube quando a conexão for feita por meio de um servidor proxy. NPR-15109: HotFix do CQ-110332
* O uso de um ativo com um nome contendo um ponto (.) em data-sly-resource não é resolvido para o mesmo ativo e o caminho de saída é terminado no ponto. NPR-15069: Hotfix do CQ-4195914
* Após atualizar o AEM 6.2 para o Pacote de serviços 1, ocorre falha na sincronização de ativos no Scene7. A propriedade `dam:Scene7FileStatus` exibe o status `UploadFailed` mesmo para ativos publicados. NPR-15269: hotfix do CQ-4197708

### Interface do usuário {#user-interface-5}

* Na **[!UICONTROL Interface de toque]**, a data salva é mostrada para campos de data que agora têm type=&#39;datetime&#39; ao usar o navegador Chrome versão 56.0.2924.87. NPR-15383: hotfix do GRANITE-16481
* Na **[!UICONTROL Interface para toque]**, o Editor de Rich Text remove o thread e os elementos de legenda das tabelas HTML ao renderizá-los. NPR-15267: Hotfix do CRTE-41
* O `FileUpload Validator` não trata de casos em que a inicialização automática é verdadeira ou quando `uploadFile()` é chamado manualmente e gera um relatório de validação inválido nesses casos. NPR-15295: Hotfix do GRANITE-13499

* O Omnisearch não permite que clientes que usam `/apps` adicionem uma fonte de dados de coluna, pois pressupõe que a configuração do local está listada em */libs/granite/omnisearch/content/metadata/*. NPR-13188 Hotfix do GRANITE-16479
* Ao usar a **[!UICONTROL Interface para toque]**, as variantes de produto não são criadas no mesmo nível do produto. O usuário não é informado sobre o status do processo de criação de variantes. NPR-15345: HotFix do CQ-4198948

**Scene7**

* A execução do fluxo de trabalho do Scene7 resulta em arquivos abertos que não fecham. Solicite a melhoria do serviço AEM-S7 para que ele mantenha e reutilize uma única instância HttpClient com configuração de pool compartilhado. NPR-15357: hotfix do CQ-109958

### Tradução {#translation-9}

* Ao usar projetos de tradução, atualizar cópias de idioma do inglês principal produz 11 inicializações separadas, todas com o mesmo nome e raiz de origem. No entanto, cada uma tem raízes de inicialização ligeiramente diferentes, caso o nome da página siga um padrão definido. NPR-15605: Hotfix do CQ-4200699
* Os projetos de tradução não são criados para páginas quando as raízes do idioma têm hifens e traços no nome. NPR-15171: HotFix do CQ-96286
* Solicite a atualização do conector da Microsoft® para poder usar as APIs do Microsoft® Translator que a Microsoft® disponibiliza no portal do Azure. NPR-15320: hotfix do CQ-101010

### Projetos {#projects-4}

* Somente 20 projetos inativos estão visíveis na tela Projetos, embora existam mais de 20 projetos inativos no repositório. NPR-15656: Hotfix do CQ-4200903

### Campaign {#campaign-1}

* Ao usar os componentes de integração do Campaign, Direcionamento e `MAC`, Test e Target, o cancelamento da publicação de atividades não atualiza o status da atividade na interface principal. NPR-15401: HotFix do CQ-4199839
* Ao mover um produto no AEM Commerce, o Assistente para movimentação de produtos perde os valores preenchidos previamente para o nome do produto, título, páginas referenciadas, autor de criação e data de criação. NPR-15228: Hotfix do CQ-98617

### Segurança {#security-4}

* Parâmetro de token CSRF adicionado a formulários com um método de GET. NPR-15229

### Forms {#forms-18}

#### Pacote complementar do Forms {#forms-add-on-package-18}

`**Adaptive Forms**`

* Os valores padrão são substituídos por valores vazios no xml mediante preenchimento prévio do formulário adaptável com XML de entrada. NPR-15721
* O wrapper `afData/afBoundData` está presente no XML enviado, embora mesmo o XML de preenchimento prévio não tenha o wrapper `afData/afBoundData` em formulários adaptáveis baseados em esquemas XML. NPR-15541

* Os títulos na barra do Accordion devem ser títulos HTML “h2” editáveis em vez da tag “a”. NPR-15475
* O layout do Accordion de um painel de formulário não está acessível aos usuários de leitores de tela. Os usuários não podem navegar até a guia do Accordion só pelo teclado usando um software de leitor de tela, como o JAWS ou o NVDA. NPR-15474

`**Correspondence Management**`

* Salvar, excluir e definir a referência de um fragmento de documento leva muito tempo. NPR-15939
* Alinhamento de guias definido em Gerenciar ativos em textos que contêm várias quebras de cabeçalhos na interface do CCR. NPR-15818
* As miniaturas dos módulos de Texto não mostram conteúdo alinhado, embora o texto contenha conteúdo alinhado criado com o uso de guias no Google Chrome. NPR-15819

`**Forms Portal**`

* O serviço de preenchimento prévio não funciona com formulários XDP. NPR-15466
* Ao armazenar rascunhos e envios de formulários adaptáveis ao banco de dados, o estado do formulário adaptável é corrompido quando a conectividade com o banco de dados falha por qualquer motivo (por exemplo, após um longo período de inatividade). NPR-15297

#### Instalador do Forms no JEE {#forms-jee-installer-18}

`**Core**`

* Após atualizar para a versão mais recente do Java™ 1.8.0_121-b13, a interface de administração não está acessível no AEM Forms. NPR-15330

`**XTG**`

* Ao usar o Serviço de saída para unir um formulário específico a um dataxml, o tempo de resposta é 20 vezes maior do que o tempo gasto pelo servidor ES4 SP1. NPR-15283

#### Aplicativo AEM Forms {#aem-forms-app-1}

* Ao recuperar tarefas não salvas, a mensagem mostrada precisa ser mais clara para reduzir erros. NPR-15377
* O aplicativo AEM Forms não renderiza formulários criados a partir de modelos personalizados. NPR-15892
* Usuários não conseguem fazer logon no aplicativo do AEM Forms. NPR-15891

Os principais destaques do AEM 6.2 SP2-CFP1 são:

* Simplifica a funcionalidade de replicação nos sites:

* Correções para vários problemas de Implantação, Live Copy e gravações com falhas

* Aumento da capacidade de resposta da interface para toque durante:

* pesquisas de ativos
* classificação baseada em tamanho

* Melhora o gerenciamento de tags em coleções inteligentes
* Controles de acesso mais rigorosos durante operações CRUD em pastas

### Plataforma {#previous}

* Solicitação de remoção de chamadas de API `ReplicationQueue#forceRetry` durante a inicialização de agentes de replicação, pois essas chamadas retardam significativamente a instância, especialmente quando há muitos agentes de replicação. NPR-14032: Hotfix do GRANITE-13095
* Solicitação de configuração OSGi `DurboImportConfigurationProviderService` para suportar campos que armazenem uma matriz de valores. NPR-14570: Hotfix do CQ-108684
* Usar o componente Sightly em uma página após migrar para o AEM 6.2 faz com que a caixa de diálogo Propriedades da página pare de funcionar. NPR-14328: Hotfix do CQ-108355
* O cancelamento da programação de um trabalho agendado anteriormente não remove o nó correspondente abaixo */var/eventing/Scheduled-jobs*. NPR-14253: Hotfix do SLING-5666
* Quando um administrador tenta representar como um usuário excluído, a interface do usuário falha ao atualizar. NPR-14247: Hotfix do CQ-107446
* A verificação de proteção XSS que causa codificação incorreta no componente Sightly. NPR-14004: hotfix do CQ-93821
* Solicite a atualização do Jackrabbit FileVault para a versão 3.1.30 para resolver de vários problemas. NPR-13454
* O erro de cache ocorre quando a distribuição do Sling sincroniza os pacotes de distribuição do autor para publicação. NPR-13034: hotfix do GRANITE-13970

### Sites {#sites-18}

* Problemas com o VersionManagerImpl ao remover versões incorretas do histórico de versões. NPR-14372
* O componente WCM Sightly Foundation Parsys ignora os nomes das tags de declaração do componente, `cq:htmlTag / cq:tagName`. NPR-14225
* Quando o Sightly Parsys é usado para renderizar componentes inseridos via JavaScript na interface de toque, a decoração personalizada é ignorada depois que a página é atualizada. NPR-14122
* As listas suspensas de destino não funcionam na caixa de diálogo da interface de toque quando vários campos de rich text, como links, são criados. NPR-13911
* Ao editar um campo de texto com várias propriedades do editor de rich text (RTE) em uma caixa de diálogo (interface de toque), o foco muda aleatoriamente para uma propriedade específica do RTE. NPR-13703
* O componente de vídeo pronto para uso padrão não renderiza a miniatura do vídeo. NPR-14976
* As informações são carregadas lentamente na guia Usos dinâmicos no Editor de modelo. NPR-14880: hotfix do CQ-83417
* A instalação do hotfix-10936 em uma instância do AEM 6.2 desabilita o componente iparsys. NPR-14330: Hotfix do CQ-106982
* Vários problemas com componentes de Implantação e um problema com a Live Copy após a migração para o AEM 6.1 SP1. NPR-15256
* A ação de Implantação de página não cria páginas secundárias além do primeiro nível, mesmo para várias configurações de Implantação. NPR-15055
* Ao enviar a caixa de diálogo PageProperties do editor, os dados inalterados nas guias da LiveCopy são regravados. NPR-14693
* Quando a caixa de diálogo PageProperties é enviada do Editor, o MSM Post Processor grava alguns parâmetros da solicitação em vez do parâmetro `msm:writeLiveCopyConfig`. NPR-14434
* Vários problemas relacionados ao componente de Implantação, Live Copies e outros aspectos do MSM. NPR-12235

### Ativos {#assets-18}

* O fluxo de trabalho de descompactação não consegue processar imagens com caracteres especiais no nome do arquivo de imagem. NPR-15227: Hotfix do CQ-103887
* Os ativos que têm a expressão Repetir com Condição não são exibidos corretamente. Quando a pessoa visualiza o modelo de correspondência `*CDN3835RLCEN*`, nenhum ativo localizado na área de direcionamento do corpo é exibido. Para dispositivos de anexo de arquivo que permitem vários anexos, o envio de uma nova instância de formulário com um anexo em um dispositivo que já tem um anexo anterior resulta na exibição de um código de erro. NPR-14844

* Ao criar uma coleção inteligente, a tag de estilo não é preservada quando a coleção inteligente é salva. NPR-15081: Hotfix do CQ-4195494
* Consultas de pesquisa de ativos são executadas lentamente na interface de toque durante pesquisas simultâneas de vários usuários. NPR-15019: Hotfix do CQ-4195405
* Os metadados extraídos para uma propriedade do tipo `Long[]` convertem para o tipo `String[]` quando o upload do original é refeito para um local diferente. NPR-15016: Hotfix do CQ-4195005

* Usuários não conseguem excluir uma pesquisa salva ou uma coleção inteligente. NPR-14924: hotfix do CQ-108494
* Editar metadados para ativos em massa (modo de anexação) ao usar um valor booleano para TypeHint em um campo suspenso no esquema de metadados subjacente produz um erro. NPR-14529: hotfix do CQ-106876
* Usuários sem direitos de replicação agora conseguem excluir pastas de ativos. NPR-14321: hotfix do CQ-88271
* Ao tentar editar os perfis de vídeo de um vídeo no Editor de canais, a caixa de diálogo de design não abre e gera uma exceção de ponteiro nulo no log de erros. NPR-14144: hotfix do CQ-81101
* A propriedade de carimbo de data e hora “Criado” gerada pelo sistema exibida na página de propriedades de um ativo está incorreta. NPR-13992: Hotfix do CQ-95029
* Solicitação para ativar a detecção de ativos duplicados para usuários sem acesso de Leitura no AEM Assets NPR-13851: Hotfix do CQ-102281
* Usuários não conseguem editar metadados para ativos em massa na página de propriedades. NPR-13721: Hotfix do CQ-100703
* Mensagem de erro incorreta na interface clássica ao fazer upload de um ativo duplicado. A mensagem de erro não indica por que o upload falhou. NPR-13691: Hotfix do CQ-99272
* A AEM Assets não consegue classificar mais de 50 ativos por tamanho de uma vez na visualização da Lista quando a pasta contém vários ativos. CQ-100588
* A seleção de vários ativos gera um erro com o Código de resposta – 414 (URI de solicitação muito longa) se o URI do ativo/pasta for muito longo. NPR-13516: hotfix do CQ-76076
* A página Relatório de ativos não responde quando alguém seleciona todas as opções na caixa de diálogo `Configure Columns`. NPR-13187: hotfix do CQ-95589
* Comportamento inesperado do seletor de tags no Safari e no Internet Explorer. NPR-13134
* A edição de pesquisas salvas no painel Pesquisa do administrador de ativos permite salvá-las como seleções inteligentes aninhadas, o que causa problemas de estabilidade do ambiente. NPR-13119: hotfix do CQ-99460
* Depois de mover um arquivo (ou pasta) e renomeá-lo, os metadados `cq:name` não correspondem ao novo nome do arquivo (nome da pasta). NPR-13036: hotfix do CQ-99141
* Ativos cujos nomes incluem caracteres especiais não podem ser baixados do link de download compartilhado por email. NPR-12872: hotfix do CQ-95795
* Os relatórios de ativos prontos para uso gerados quando há um número substancial de ativos causam muitos percursos nos quais a pesquisa não atinge nenhum índice e picos ocorrem no uso da CPU. NPR-12811: hotfix do CQ-84409
* Usuários na instância de criação do AEM Assets do AMS acessam de redes diferentes, incapazes de fazer upload de ativos usando o upload por partes sem privilégios de exclusão em pastas. NPR-12768: Hotfix do CQ-82715
* Em pesquisas baseadas em tags para ativos usando o painel Pesquisa de ativos, o recurso Digite adiante não se limita ao caminho raiz e exibe tags de todas os namespaces. NPR-12666
* O componente StaticRenditions gera uma exceção de ponteiro nulo. NPR-12665
* Solicitação para desativar MissingMetadataNotificationJob, pois isso faz com que a interface de notificação de emblema quebre a página com uma exceção de tempo de execução &quot;Não é possível verificar a entrada&quot;. NPR-12500: Hotfix do CQ-93573
* A opção &quot;Desativar edição&quot; para um campo de tag não funciona em páginas de propriedades de ativos na interface para toque. NPR-12429: Hotfix do CQ-88835
* Correções de API do AEM Assets 6.2 para implementação do aplicativo complementar SMB. NPR-11099
* Desde a atualização do `Jquery`, os usuários não conseguem selecionar uma coleção de ativos e confirmar a seleção no painel Conteúdo associado de um fragmento de conteúdo. NPR-14847: Backport do CQ-4194209
* Embora invoque classificação infinita no lado do cliente, somente artigos/banners/coleções exibidos atualmente na interface são classificados. NPR-14493: Hotfix do CQ-109926
* Solicitação para implementar o recurso omnisearch para o serviço AEM Mobile on-demand. A pesquisa por palavra-chave para qualquer artigo, coleção ou banner não retorna nenhuma correspondência. NPR-14093: Hotfix do CQ-101394
* Ao usar o componente de seleção Coral (*granite/ui/components/coral/foundation/form/select*) em uma caixa de diálogo, a inicialização do valor não funciona corretamente no Internet Explorer (navegadores IE11 ou Edge) quando o valor selecionado contém um único item. NPR-13395: hotfix do CQ-101013

### Projetos {#projects-5}

* Ao exportar um projeto de tradução criado com o Método de tradução como “humano” e Provedor de tradução como “nenhum”, nenhum arquivo translation_export_summary.xml é gerado pois o arquivo de mapeamento de GUID está ausente. NPR-13137: hotfix do CQ-91976
* Nos projetos do AEM, ao criar um projeto com a propriedade de data de vencimento definida, a conversão de data define o tempo incorretamente devido à diferença no fuso horário entre o servidor e o cliente. NPR-13003: Hotfix do CQ-98288
* A opção &quot;Revelar em sites&quot; é omitida do trabalho de tradução quando um projeto de tradução é atualizado. NPR-12966: Hotfix do CQ-93740
* Quando um projeto de tradução é criado para uma página do site exportada, ele não é renderizado corretamente na pré-visualização. NPR-12964: Hotfix do CQ-84627

### Fluxo de trabalho {#workflow-3}

* O link de conteúdo na guia Arquivo do console Fluxo de trabalho retorna um erro com o código de resposta “404” ao clicar nele. NPR-14993: Hotfix do CQ-4194977
* Ao usar workflows padrão do AEM, o CQ Mailer não envia uma notificação por email para o grupo que perde o endereço de email de um único membro. NPR-14804: Solicitação de Hotfix do CQ-91499
* Aprimoramentos de desempenho na caixa de entrada e no selo de notificação na interface de toque. NPR-14145: hotfix do CQ-101125
* Usuários não conseguem pré-visualizar o conteúdo no console da caixa de entrada do fluxo de trabalho ao iniciar fluxos de trabalho. NPR-13226: hotfix do CQ-100275
* O cookie “saml_request_path” configurado com o uso do Manipulador de autenticação do SAML exibe um cookie definido com um caractere `?` extra. Além disso, quando uma resposta SAML é postada de volta para o AEM, o cookie “saml_request_path” do AEM retorna um valor inválido devido a caracteres já codificados. NPR-13517: Proactive Hotfix do GRANITE-11722 e GRANITE-14414

### Dynamic Media {#dynamic-media}

* Vários trabalhos de sling do `AEM-Scene7` que foram criados e cancelados durante a ativação do AEM são registrados como trabalhos de arquivamento durante a replicação. NPR-12835: hotfix do CQ-86115

### Segurança {#security-5}

* Solicitação para resolver o problema de validação de entrada no filtro WCMDebug. NPR-12444: Solicitação de Hotfix do CQ-94890
* Solicitação proativa para corrigir o comportamento XSS ao usar o Assistente de criação de inicialização.
NPR-13062: solicitação de hotfix do CQ-99577

#### Pacote complementar do Forms {#forms-add-on-package-19}

`Adaptive Forms`

* Ao criar um painel repetível usando formulários adaptáveis, o título do painel não pode ser atualizado em tempo de execução. NPR-15325
* Se você definir um valor padrão para um botão de opção e selecionar um valor diferente ao salvar ou enviar, o preenchimento prévio não exibirá o valor selecionado. NPR-15304
* O Google Chrome mostra um comportamento incorreto ao usar o evento de opções para preencher dinamicamente a lista suspensa e enviar o valor do item selecionado. NPR-15198
* Ao criar um painel repetível usando formulários adaptáveis, o título do painel não pode ser atualizado em tempo de execução. NPR-15181
* Ao usar o modo de edição para formulários adaptáveis, erros de JavaScript, como “O manipulador do componente é inválido” e “o guidelib não está definido” são encontrados. NPR-15112
* O fragmento de carregamento lento dentro de um painel repetitivo não funciona como esperado. NPR-13916, NPR-14785

`Correspondence Management`

* Os ativos do Gerenciamento de correspondências com o conjunto de expressões `'Repeat with condition'` não são exibidos corretamente. NPR-14844
* Ao pesquisar por um ativo do Gerenciamento de correspondências (como uma carta, um fragmento de documento ou qualquer outro tipo), o ícone de Fila para download não aparece na barra de ferramentas. NPR-14745
* Ao criar um módulo de Lista, a alternância das propriedades específicas do ativo (como editável, obrigatório) não funciona. NPR-14689
* O painel Elementos de dados no utilitário Builder de expressões continua sendo carregado caso um módulo de condição seja criado sem selecionar um dicionário de dados. NPR-14688
* Ao visualizar uma correspondência, os usuários não podem usar espaços de tabulação para alinhar o conteúdo no formato tabular. NPR-14481
* Ao exportar ativos do Gerenciamento de correspondências em massa da interface, o servidor do AEM Forms gera registros desnecessários. NPR-15226
* Quando uma correspondência é visualizada, o texto justificado é exibido em uma fonte diferente. NPR-15468

`**Forms Portal**`

* Anexos de formulários enviados no Portal do Forms não ficam visíveis quando um novo rascunho do envio do portal é enviado. NPR-13515

`**Forms Manager**`

* Ao navegar no diretório *FormsandDocuments*, o botão Colar não é exibido quando o usuário copia qualquer ativo e depois navega para uma pasta diferente. CQ-111327

#### Instalador do Forms no JEE {#forms-jee-installer-19}

`Rights Management`

* O evento de auditoria relacionado ao logon do usuário é registrado com um tempo inválido. A hora correta para o evento de auditoria não é rastreável. NPR-13107
* O Adobe Acrobat Reader e o Microsoft® Office não conseguem abrir documentos protegidos com autenticação estendida. NPR-14482

`Process Management`

* Quando uma tarefa de rascunho encaminhada no espaço de trabalho HTML é retornada ao usuário inicial, ela não aparece em sua fila. NPR-15178

`Assembler Service`

* A AEM Forms não valida um PDF/A-2b com mais de duas assinaturas. NPR-14101

`XTG`

* Ao imprimir um documento usando uma bandeja de desvio da impressora, a função `GeneratePrintedOutput` não permite a obtenção de papel da bandeja de desvio direita. NPR-14079

#### Designer do Forms {#forms-designer-2}

* O Designer de formulários trava quando o usuário executa o utilitário Verificação ortográfica com o idioma do formulário selecionado como Francês (Canadá). NPR-13740
* O Designer do Forms trava quando o usuário seleciona “calcular evento” ou “validar evento” para um campo de formulário e altera a linguagem para JavaScript e insere `this.` na janela **[!UICONTROL Editor de scripts]**. NPR-12974

### Pacotes de recursos incluídos no CFP1 {#feature-packs-included-in-cfp-3}

`Mobile Forms` (Pacote complementar do Forms):

* Quando um formulário adaptável é criado de um arquivo XDP, a tabulação para acessibilidade não segue o padrão definido. NPR-12562

`Adaptive forms` (Pacote complementar do Forms):

* O Construtor de regras para formulários adaptáveis não fornece acesso baseado em função. As alterações feitas por um autor não são rastreáveis. NPR-12840

`Core` (Instalador do Forms JEE):

* A funcionalidade Compartilhamento de Recurso de Origem CoreCross (CORS) como filtro de servlet não está habilitada para JBoss®+. NPR-13050

## Instruções de download para o CFP por meio da Distribuição de software {#download-instructions-for-cfp-via-package-share}

>[!NOTE]
>
>Para clientes do AEM Forms, é essencial instalar o pacote complementar do AEM Forms após instalar qualquer Pacote de serviços, Pacote de serviços cumulativo ou Pacote de recursos do AEM.

É possível baixar o pacote CFP diretamente da Distribuição de software ou executar as seguintes etapas:

1. Abra a [Distribuição de softwares](https://experience.adobe.com/downloads). Você precisa de uma Adobe ID para fazer logon na Distribuição de softwares.
1. Clique em **[!UICONTROL Adobe Experience Manager]** disponível no menu de cabeçalho.
1. Clique no nome do pacote, selecione **[!UICONTROL Aceitar termos do EULA]** e clique em **[!UICONTROL Download]**.

## Instruções de instalação para o CFP {#installation-instructions-for-cfp}

Esta seção aborda os requisitos e as etapas para instalar o CFP.

### Antes de instalar {#before-you-install}

>[!NOTE]
>
>Os Feature Packs opcionais fornecidos pela Adobe depende da versão de lançamento e do Cumulative Fix Pack. Se você tiver algum Pacote de recursos instalado, entre em contato com a [equipe de atendimento ao cliente do AEM](https://experienceleague.adobe.com/pt-br?support-solution=General#support) para validar a compatibilidade com este Pacote de correções cumulativo para AEM 6.2.

>[!NOTE]
>
>É recomendável executar a validação em cada novo pacote de instalação antes de tentar instalá-lo. A pré-validação analisa e relata os erros encontrados antes da instalação, além de avisar os usuários sobre esses erros, sobreposições e permissões de forma proativa.
>

* O AEM 6.2 Service Pack 1 é um pré-requisito do CFP. Para obter instruções de instalação, consulte as notas de versão do [Pacote de serviços 1 do AEM 6.2](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

* O download do Pacote de correções cumulativo está disponível em [Distribuição de softwares](https://experience.adobe.com/#/downloads/content/software-distribution/br/aem.html), que está acessível diretamente da instância do AEM.
* Em uma implantação de cluster usando RDBMK ou MongoDB, o pacote CFP pode ser instalado em qualquer uma das instâncias de criação que use o Gerenciador de pacotes.

* Antes de instalar o Pacote de correções cumulativo, verifique se você fez um instantâneo ou um backup da instância do AEM.
* Não há suporte para a desinstalação do CFP.

### Instale o CFP por meio da Distribuição de software {#install-the-cfp-via-package-share}

Para instalar o Pacote de correções cumulativo em uma instância do AEM 6.2 SP1, execute as seguintes etapas:

1. Para baixar o pacote, clique em [Distribuição de software](https://experience.adobe.com/#/downloads/content/software-distribution/en/aem.html?package=/content/software-distribution/en/details.html/content/dam/aem/public/adobe/packages/cq640/cumulativefixpack/aem-6.4.8-cfp-2.0.zip).

1. Abra [Gerenciador de pacotes](http://localhost:4502/crx/packmgr/index.jsp) e clique em **[!UICONTROL Fazer upload de pacote]** para fazer upload do pacote.

1. Selecione o nome do pacote e clique em **[!UICONTROL Instalar]**.

### Instalação automática {#automatic-installation}

O CFP pode ser instalado automaticamente em uma instância em execução das seguintes maneiras:

* Coloque o pacote em ../crx-quickstart/install enquanto o servidor estiver em execução. O pacote é instalado automaticamente.
* Use a [API HTTP a partir do Gerenciador de pacotes](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions) - certifique-se de usar `cmd=install&recursive=true` - para instalar os pacotes aninhados.

### Validar instalação {#validate-installation}

1. A página Informações do produto (/system/console/ productinfo) agora deve mostrar a string da versão atualizada “Adobe Experience Manager, Versão 6.2.0.SP1-CFP20” em Produtos instalados.
1. Todos os pacotes OSGI são ou ATIVOS ou FRAGMENTOS no Console OSGi (Use o console da web: /system/console/bundles).

>[!NOTE]
>
>Ao instalar com êxito o pacote, uma mensagem informativa é exibida indicando que o pacote de conteúdo foi instalado com êxito, como “Pacote de conteúdo AEM-6.2-Cumulative-Fix-Pack-SP1-CFP20 instalado com êxito.”

>[!NOTE]
>
>A partir do AEM 6.2 SP1-CFP1, o nível de log no Jackrabbit FileVault mudou de INFO para DEBUG na maioria das mensagens. Para obter registros de instalação de um pacote de conteúdo instalado no AEM 6.2 SP1-CFP1 ou mais recente, ative o nível de registro DEBUG para `org.apache.jackrabbit.vault.packaging.impl`.

### Instalar o AEM Forms {#install-forms}

>[!NOTE]
>
>Pule esta seção se não estiver usando o AEM Forms.

#### Instalar complemento do AEM Forms {#install-aem-forms-add-on}

>[!NOTE]
>
>(**AEM Forms em JEE somente**) O procedimento para instalar um CFP no AEM Forms em JEE está descrito em [Instalação do CFP no AEM Forms JEE](install-cfp-aem-forms-jee.md#install-cfp-on-aem-forms-jee).

1. Verifique se você instalou o pacote AEM 6.2 SP1 CFP.
1. Baixe o pacote complementar do Forms correspondente listado em [Versões do AEM Forms](aem-forms-releases.md) para seu sistema operacional.
1. Instale o pacote complementar do Forms conforme descrito em [Instalação dos pacotes complementares do AEM Forms](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions).

#### Instalar pacote do AEM Forms JEE {#install-aem-forms-jee-bundles-package}

As correções no JEE do AEM Forms são entregues por meio de um instalador separado. Para obter informações sobre como instalar um CFP no AEM Forms no JEE, consulte [Instalação do CFP no JEE do AEM Forms](install-cfp-aem-forms-jee.md).

#### Instalador do Designer do Forms {#designer-installer}

1. Para instalar a atualização, execute o arquivo Designer6.2.0_&lt;Language>_Cumulative_QF.msp.
1. Na tela de boas-vindas, clique em **atualizar**. A instalação é iniciada.
1. Depois que a instalação for concluída, clique em **concluir**.

## Parâmetros de tempo limite configuráveis por usuário para conexões do DTM, Analytics e Target {#user-configurable-timeout-parameters-for-dtm-analytics-target-search-promote-connections}

Com o AEM Cumulative Fix Pack 6.2 SP1-CFP7 e versões posteriores, os períodos de tempo limite de conexão se tornaram configuráveis em todas as conexões acima, conforme os detalhes abaixo:

| **Conexões** | **Tempo limite da conexão&#42;** | **Tempo limite do soquete&#42;&#42;** |
|---|---|---|
| DTM | 30.000 milissegundos | 30.000 milissegundos |
| Analytics | 30.000 milissegundos | 30.000 milissegundos |
| Target | 60.000 milissegundos | 30.000 milissegundos |

* **Tempo limite da conexão&#42;**: tempo limite em milissegundos até que uma conexão seja estabelecida. Um valor de tempo limite zero é interpretado como um tempo limite infinito.
* **Tempo limite do soquete&#42;&#42;**: tempo limite em milissegundos para espera por dados ou um período máximo de inatividade entre dois pacotes de dados consecutivos.

## Desabilitar o status de replicação no console de marcação (Interface clássica) (NPR-15842) {#disable-replication-status-in-tagging-console-classic-ui-npr}

Caso esteja usando o CFP3 ou posterior, siga estas instruções para desativar o status de replicação no console de marcação na interface clássica:

* Sobreposição *“/libs/cq/tagging/widgets/source/widgets/admin/TagAdmin.js”* no *`/apps`*

* Adicionar `replicationStateRequired`: “false” após a linha #416.

```js
415 baseParams: {
416 count: "false",
417 "replicationStateRequired": "false"
418 },
```

## O Java™ 8 Atualização 131 gera uma exceção (NPR-21355) {#latest-java-update-throws-an-exception-npr}

>[!NOTE]
>
>Essas configurações são específicas para clientes do AEM Forms que usam a Document Security.

O NPR-21355 está incluído no CFP12.1. Se você estiver instalando o CFP12.1 ou posterior, execute o procedimento a seguir para configurar o NPR-21355 no servidor de aplicativos JBoss®. Se estiver instalando o CFP12.1 no servidor do AEM Forms em execução nos servidores de aplicativos Oracle WebLogic ou IBM® WebSphere, nenhuma configuração adicional será necessária:

1. Faça backup, exclua e crie o arquivo module.xml. O local padrão do arquivo é [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. Abra o arquivo module.xml recém-criado para edição. Adicione o seguinte código ao arquivo:

```xml
<module xmlns="urn:jboss:module:1.1"
name="com.adobe.livecycle">
<resources>
<resource-root path="cryptojcommon.jar"/>
<resource-root path="cryptojce.jar"/>
<resource-root path="jcmFIPS.jar"/>
<resource-root path="certj.jar"/>
<resource-root path="cglib.jar"/>
</resources>
<dependencies>
<module name="javax.api"/>
<module name="asm.asm"/>
</dependencies>
</module>
```

1. Crie um backup dos arquivos `jsafeFIPS.jar`, `jsafeJCEFIPS.jar` e `certjFIPS.jar` no [AEM_Forms_Installation_directory]`/jboss/modules/system/layers/base/com/adobe/livecycle/main/` e exclua os arquivos do diretório mencionado anteriormente.

Entre em contato com o [Suporte da Adobe](https://experienceleague.adobe.com/pt-br?support-solution=General#support) para obter novos arquivos JAR. Coloque os arquivos JAR obtidos de [Suporte da Adobe](https://experienceleague.adobe.com/pt-br?support-solution=General#support) em [AEM_Forms_Installation_directory]/jboss/modules/system/layers/base/com/adobe/livecycle/main/

1. (Somente para Windows) Modifique os arquivos de configuração `[AEM_Forms_Installation_directory]/jboss/standalone.conf.bat` ou `domain.conf.bat`:

* Para o servidor JBoss® em configuração independente, abra standalone.conf.bat para edição.
* Para o servidor JBoss® em configuração de cluster, abra domain.conf.bat para edição.

  Adicione as seguintes linhas no final e salve o arquivo:

  Ajustar `JAVA_OPTS=%JAVA_OPTS%-Djnlp.com.rsa.cryptoj.fips140loader=true`

  Ajustar `JAVA_OPTS=%JAVA_OPTS%-Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE`

1. (Somente para sistemas operacionais baseados em Linux) Modifique os arquivos de configuração do [AEM_Forms_Installation_directory]/jboss/standalone.conf ou domain.conf:

* Para o servidor JBoss® em configuração independente, abra standalone.conf para edição.
* Para o servidor JBoss® em configuração de cluster, abra domain.conf para edição.

  Adicione as seguintes linhas no final e salve o arquivo:

  `JAVA_OPTS="$JAVA_OPTS-Djnlp.com.rsa.cryptoj.fips140loader=true"`

  `JAVA_OPTS="$JAVA_OPTS -Dcom.rsa.cryptoj.fips140initialmode=NON_FIPS140_MODE"`

## Configurações necessárias para o NPR-19778 {#configuration-settings-required-for-npr}

>[!NOTE]
>
>O NPR-19778 faz parte do CFP14.

Quando um usuário reivindica uma tarefa, a contagem da fila compartilhada não é atualizada para os outros. Para isso, a Adobe introduziu uma nova propriedade. Siga as etapas abaixo para configurar essa propriedade na sua instância do AEM:

1. Vá para a interface do Administrador -> Serviços -> Espaço de trabalho -> Administração global.
1. Exportar configurações globais.
1. No arquivo XML baixado, adicione a tag `<client_tasksPollingInterval>10</client_tasksPollingInterval>`. Dez é o valor de exemplo em segundos. É possível modificá-la de acordo.
1. Salve o arquivo.
1. Volte para interface do Administrador -> Serviços -> Espaço de trabalho -> Administração global.
1. Importe o arquivo xml na seção Importar configurações globais.
1. Agora é possível sair do sistema e fazer logon novamente.
1. A contagem da fila compartilhada inicia a atualização para outros usuários na área de trabalho.
1. Para desativar a pesquisa, altere o valor para 0 e importe o arquivo XML novamente.

## Alterações na interface {#ui-changes}

* Alteração de comportamento na exibição de títulos no cartão Imagem para imagem com a propriedade `dc:title` definida como String [] (vários campos): somente o título alterado mais recente será exibido no cartão Imagem na interface, embora todos os títulos sejam salvos no CRX. Hotfix do CQ-4217165

## Problemas conhecidos {#known-issues}

* Atualizar o AEM 6.2SP1-CFP19 e o AEM 6.2SP1-CFP20 do CFP18 altera o redirecionamento raiz para a página de boas-vindas da interface clássica em vez de /sites.html/content. Talvez seja necessário corrigir a sling: Propriedade de público-alvo de /welcome.html para /index.html com o CRX Explorer. Esse problema não é observado na atualização do CFP17 ou versão anterior.

Os seguintes erros transitórios podem ocorrer ao instalar o AEM 6.2 SP1-CFPx. No entanto, não é necessária nenhuma resolução para esses erros, pois eles não afetam sua instância do AEM e desaparecem depois que o CFP é instalado:

* Ao atualizar a instância do AEM 6.2SP1-CFP20 para o AEM 6.5, alguns URLs personalizados podem não funcionar como:

* */projects.html*
* */sites.html*

No entanto, a solução alternativa é reiniciar a instância do AEM após uma atualização.

* O erro interno do servidor HTTP 500 é recebido quando a página de detalhes do componente do console da web é aberta.
* Erros como **Criar instância de componente** e **A fábrica de serviço retornou nulo** ocorrem devido à reinicialização do repositório:

* com.day.cq.cq-personalization [com.day.cq.personalization.impl.DefaultProfileProvider(938)] Cannot create component instance due to failure to bind reference profileManager
* org.apache.sling.commons.scheduler FrameworkEvent ERROR (org.osgi.framework.ServiceException: Service factory returned null. (Componente: com.day.cq.tagging.impl.TagGarbageCollector (1687)))

* Erro observado na instalação do CFP em Mongo e DB2®: **org.apache.sling.discovery.oak.TopologyWebConsolePlugin addDiscoveryLiteHistoryEntry: Exception: java.lang.NullPointerException**. Este erro não ocorrerá após a instalação de um CFP sobre o CFP8.
* (Tarefa de atualização do scheduler de manutenção do Adobe Granite) com.adobe.granite.maintenance.impl.TaskScheduler: nenhuma tarefa de manutenção encontrada com o nome WorkflowPurgeTask para a janela `granite:weekly`
* `[sling-oak-observation-8]com.day.cq.dam.scene7.impl.Scene7DamChangeEventListener checking - isAsset`
* `[sling-oak-observation-8] com.day.cq.dam.scene7.impl.Scene7UploadServiceImpl synchronizeFolder failed for (null) failed`
* `[OsgiInstallerImpl] com.adobe.granite.offloading.impl.transporter.OffloadingAgentManager Cannot disable outbox replication agent.org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.mobile.cq-mobile-core [com.adobe.cq.mobile.omnisearch.impl.MobileAppsOmniSearchHandler(3058)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.FormsAndDocumentOmniSearchHandler(2718)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored15.02.2017 08:28:06.511`
* `[OsgiInstallerImpl] com.adobe.aemds.formsmanager.adobe-aemds-formsanddocuments-core [com.adobe.aem.formsndocuments.handlers.ThemeOmniSearchHandler(2722)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.screens.com.adobe.cq.screens.dcc [com.adobe.cq.screens.dcc.impl.ScreensOmniSearchHandler(332)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.screens.com.adobe.cq.screens.dcc [158] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.OfferOmniSearchHandler(947)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.AudienceOmniSearchHandler(957)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.cq-personalization [com.day.cq.personalization.impl.omnisearch.ActivitiesOmnisearchHandler(958)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.day.cq.cq-personalization [250] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.OrdersOmniSearchHandler(623)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductsOmniSearchHandler(625)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.ProductCollectionsOmniSearchHandler(627)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.adobe.cq.commerce.cq-commerce-core [com.adobe.cq.commerce.impl.omnisearch.CatalogsOmniSearchHandler(633)] The deactivate method has thrown an exception (org.apache.sling.api.resource.LoginException: Cannot derive user name for bundle com.adobe.cq.commerce.cq-commerce-core [225] and sub service omnisearch-service)org.apache.sling.api.resource.LoginException: Login Failure: all modules ignored`
* `[OsgiInstallerImpl] com.day.cq.dam.dam-webdav-support [com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob(1697)] The deactivate method has thrown an exception (java.util.NoSuchElementException: No job found with name com.adobe.cq.dam.webdav.impl.io.DamWebdavVersionLinkingJob){code}`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker issueConnectorPings: connectorRegistry is null`
* `[sling-default-5-discovery.connectors.common.runner.d6a26647-dd1c-4665-be2c-afdd19397e77096a1c19-18ce-4051-bbf1-166caed986f2] org.apache.sling.discovery.oak.pinger.OakViewChecker announcementRegistry is null`
* Ao instalar o CFPx no AEM 6.2 SP1 que inclui o pacote de recurso de Tags inteligentes, a etapa de fluxo de trabalho adicionada anteriormente para os ativos de Tags inteligentes é excluída do fluxo de trabalho do ativo de atualização do DAM.

## Uber Jar {#uber-jar}

O Uber Jar da versão 6.2 SP1-CFP20 está disponível no repositório Maven público da Adobe.

Para usar o Uber Jar em um projeto do Maven, inclua a seguinte dependência no POM do projeto:

```XML
<dependency>
 <groupId>com.adobe.aem</groupId>
 <artifactId>uber-jar</artifactId>
 <version>6.2.SP1-CFP20</version>
 <classifier>apis</classifier>
 <scope>provided</scope>
</dependency>
```

## Pacotes OSGi e pacotes de conteúdo incluídos {#osgi-bundles-and-content-packages-included-5}

O texto seguinte documenta a lista de pacotes OSGi e os pacotes de conteúdo incluídos no CFP.

* [Lista de pacotes OSGi incluídos no AEM 6.2 SP1-CFP20](assets/do-not-localize/updated.txt)
* [Lista de pacotes de conteúdo incluídos no AEM 6.2SP1-CFP20](assets/do-not-localize/content_package_comparison_result.txt)

>[!MORELIKETHIS]
>
>* [Página de hotfixes do AEM 6.2](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/aem-releases-updates)
>* [Notas de versão do AEM 6.2 SP1](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Notas de versão do AEM 6.2](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Página do produto AEM](https://business.adobe.com/br/products/experience-manager/adobe-experience-manager.html)
>* [Documentação do AEM 6.2](https://experienceleague.adobe.com/pt-br/docs/experience-manager-release-information/aem-release-updates/previous-updates/aem-previous-versions)
>* [Atualizações de produto prioritárias da Adobe](https://experienceleague.adobe.com/pt-br/docs/release-notes/experience-cloud/current)
