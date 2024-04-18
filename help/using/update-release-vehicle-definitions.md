---
title: Definições dos veículos de lançamentos de atualizações
description: Este artigo detalha os vários tipos de [!DNL Experience Manager] versões do, incluindo versões completas, pacotes de recursos e service packs.
contentOwner: AK
exl-id: 936b8136-9edb-4e11-9c29-f0c3108c35bd
source-git-commit: 125bfbeb881fb86097a609d198098585f6212570
workflow-type: tm+mt
source-wordcount: '731'
ht-degree: 95%

---

# Definições dos veículos de lançamentos de atualizações do [!DNL Experience Manager] {#update-release-vehicle-definitions}

Este documento inclui detalhes sobre os vários tipos de versões do [!DNL Adobe Experience Manager], incluindo versões completas, pacotes de recursos e pacotes de serviços que o [!DNL Adobe] oferece aos clientes.

>[!NOTE]
>
>Para obter a programação dos lançamentos de atualizações do [!DNL Experience Manager], consulte o roteiro de lançamentos de atualizações do [[!DNL Experience Manager] ](update-releases-roadmap.md)

## Versão completa {#full-release}

| Itens | Descrição |
|-------|------|
| Definição | <ul> <li> Lançamento programado </li> <li> Compatível com caminhos de atualizações para versões específicas, que são definidos nas notas de versão </li> </ul> |
| Nomenclatura | <ul> <li> Os números de versão dos principais lançamentos aumentam com base na fórmula X+1.Y.Z. </li> <li> Os números de versão para lançamentos secundários aumentam com base na fórmula X.Y+1.Z </li> </ul> X é o número da versão primária, Y é o número da versão secundária e Z é o número do patch. |
| Inclusões | <ul> <li> Novos recursos </li> <li>  Melhorias </li> <li>  Correções de bugs </li> </ul> |
| Documentação | <ul> <li> As notas de versão estão disponíveis no portal de documentação </li> <li> A documentação sobre recursos, melhorias e correções de bugs está disponível no portal de documentação </li> </ul> |
| Cadência | Anual |
| Disponibilidade e instalação | <ul> <li> Fornecido como instalador de produto independente </li> <li>  Disponível no site de licenciamento e no Managed Services </li> <li> O site de licenciamento pode exigir a migração do repositório de conteúdo </li> </ul> |
| Nível de teste | Totalmente validado pelo Controle de qualidade |

## Pacote de serviços {#service-pack}

| Item | Descrição |
|-----|-----|
| Definição | <ul> <li> Lançamento programado </li> <li> Atualmente, não é possível reverter </li> </ul> |
| Nomenclatura | <ul> <li> O número de versão do patch é um número de um só dígito </li> <li> Após a instalação, o dígito de correção do número de versão instalado aumentará com base na fórmula X.Y.Z.SPx </li> </ul> X é o número da versão primária, Y é o número da versão secundária e Z é o número do patch. x é o número do service pack. |
| Inclusões | <ul> <li> Novos recursos</li> <li>  Melhorias </li> <li> Correções de bugs </li> <li> Pacotes de recursos de interesses comuns (se houver) </li> </ul> |
| Documentação | <ul> <li> As notas de versão estão disponíveis no portal de documentação </li> <li> A documentação sobre recursos, melhorias, correções de bugs está disponível no portal de documentação </li> </ul> |
| Cadência | Trimestral |
| Disponibilidade e instalação | <ul> <li> Fornecido como um pacote </li> <li> Disponível na Distribuição de software</li> <li>  Requer instalação funcional existente </li> </ul> |
| Nível de teste | <ul> <li> Todas as correções validadas pelo Controle de qualidade </li> <li>  Integridade geral do pacote com execuções de automação </li> </ul> |

## Pacote de correções cumulativo  {#cumulative-fix-pack-aem}

| Item | Descrição |
|-----|-----|
| Definição | <ul> <li> Modelo de entrega único de lançamentos de correções </li> <li> Pacote de conteúdo do agregador contendo o pacote de conteúdo de componentes individuais </li> <li>  Os CFPs são sobreposições de hot fixes e não incluem nenhum aprimoramento.  </li> </ul> |
| Nomenclatura | X.Y.Z.CFPx <br> X é o número da versão primária, Y é o número da versão secundária e Z é o número do patch. x é o número do pacote de serviços cumulativos. |
| Inclusões | CFP é um Cumulative Fix Pack contendo correções de todos os componentes ao longo de datas especificadas. Por exemplo, se um cliente aplicar o CFP3, então CFP3 = CFP1 + CFP2. |
| Documentação | As notas de versão estão disponíveis no portal de documentação |
| Cadência | Trimestral |
| Disponibilidade e instalação | <ul> <li> Fornecido como um pacote </li> <li>  Disponível na Distribuição de software </li> <li>  Depende do lançamento do service pack mais recente </li> <li>  O CFP é autodependente. Os clientes não precisam se preocupar em encontrar/resolver dependências. O CFP deve ser instalado no Service Pack mais recente. </li> <li>  O CFP pode ser instalado como um pacote único, o que melhora a experiência do cliente.  </li> </ul> |
| Nível de teste | Controle de qualidade validado no nível de integração e teste de regressão |

## Sobreposição {#overlay}

| Item | Detalhes |
|-------|--------|
| Nomenclatura | overlay-&lt;ticket ID> |
| Inclusões | Correção de bugs para um arquivo JS ou JSP |
| Documentação | Nenhum |
| Cadência | Se necessário |
| Disponibilidade e instalação | <ul> <li> Fornecido como pacote pelo Atendimento ao cliente do [!DNL Experience Manager]  </li> <li> Não é necessariamente incluído em pacotes de serviços ou versões completas </li> </ul> |
| Nível de teste | Validado pelo Atendimento ao cliente |

## Pacote de recursos {#feature-pack}

| Itens | Detalhes |
|--------|-----|
| Definição | <ul> <li>Os pacotes de recursos são funcionalidades complementares fornecidas pelos Service Packs. Se uma versão do [!DNL Experience Manager] tiver lançado seu último service pack, a Adobe não fornecerá nenhum pacote de recursos para ela no futuro. </li> <li> Os FPs (pacotes de recursos) contêm aprimoramentos de produtos, programados para uma versão subsequente do produto, mas fornecidos antecipadamente com base na decisão do Gerenciamento de produtos do [!DNL Adobe's].</li> <li>  Os recursos são sempre mesclados com a próxima versão principal e, em seguida, transferidos para a versão do [!DNL Experience Manager] exigida pelo cliente </li> <li>  Os pacotes de recursos de Interesses Comuns e Disponibilidade Geral (GA) são mesclados no próximo service pack  </li> </ul> |
| Nomenclatura | `cq-<Release Version>-featurepack-<feature pack ID>-<feature pack version>` |
| Inclusões | <ul> <li> Novos recursos </li> <li> Melhorias </li> <li> Correções de bugs (atualizações de produtos incrementais) </li> </ul> |
| Documentação | A documentação está disponível em adobe.com. |
| Cadência | Varia conforme a Área do produto |
| Disponibilidade e instalação | <ul> <li>Fornecido pelos Service Packs </li> <li> Disponível na Distribuição de software. Os clientes aceitam os Termos e condições do [!DNL Adobe's] por meio da Distribuição de software. </li> </ul> |
| Nível de teste | Os pacotes de recursos de Disponibilidade geral são validados pelo Controle de qualidade. |

* 1: as correções do Oak não são fornecidas como um hotfix individual. No entanto, elas estão incluídas no hot fix do Cumulative Oak subsequente. Se necessário, um diagnóstico criado sobre o COFP mais recente pode ser disponibilizado. A condição prévia é que o cliente tenha o COFP mais recente em execução. As builds de diagnóstico somente fornecem o mesmo nível de controle de qualidade que um hot fix. Portanto, elas não fornecem o mesmo nível de controle de qualidade de um pacote de correções cumulativo, um pacote de serviços ou uma versão do produto. A correção final é fornecida com o próximo CFP.
