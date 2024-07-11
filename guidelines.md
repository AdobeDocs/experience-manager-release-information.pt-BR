---
source-git-commit: 10cbece451b46e8d4dbf473d728a20994a5e42cd
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 54%

---
# Diretrizes para colaboração na documentação do Adobe Experience Manager

## Filosofia da documentação

Os usuários do Adobe Experience Manager trabalham em ambientes extremamente competitivos, esforçando-se para criar experiências digitais para se destacar de seus concorrentes. Portanto, quando o Adobe introduz novas ferramentas avançadas no AEM, elas fornecem documentação precisa e clara. Essa abordagem permite que os clientes usem imediatamente seu investimento em AEM e maximizem o ROI.

O objetivo é disponibilizar a documentação do AEM aos usuários o quanto antes. Portanto, é criada uma documentação precisa e utilizável, que é continuamente atualizada e aprimorada.

## Contribuições à documentação

Para melhorar continuamente a documentação do AEM, toda a comunidade de usuários do AEM é bem-vinda para contribuir em sua elaboração. Seja por meio de pull requests ou problemas, as melhorias na documentação podem ser correções, esclarecimentos, expansões e mais exemplos.

## Padrões de documentação

O Adobe agradece as contribuições à documentação. Qualquer contribuição para a documentação do AEM, seja um pull request ou um problema, deve estar em conformidade com os padrões de contribuição e documentação do Adobe.

As contribuições que não cumprirem esses padrões poderão ser rejeitadas.

### O Adobe escreve sobre casos de uso padrão.

A documentação do AEM abrange casos de uso padrão. Casos de uso que não se enquadrarem no escopo de instalação e de uso padrão do produto não farão parte da documentação do AEM.

### A Adobe geralmente não documenta erros e suas soluções.

A documentação do AEM abrange casos de uso padrão. Por esse motivo, bugs, efeitos causados por bugs e soluções alternativas para bugs não são documentados.

As exceções a essa regra aplicam-se às notas de versão, nas quais problemas conhecidos podem ser listados com possíveis soluções que o Gerenciamento de produtos do AEM aprova.

### As contribuições à documentação não se destinam a responder perguntas técnicas.

Quaisquer ideias para melhorar a documentação do AEM são bem-vindas como contribuições. No entanto, comentários, problemas e pull requests destinam-se a *contribuições* somente. Elas não têm a intenção de responder suas perguntas sobre como usar o AEM, implementar seu projeto AEM ou resolver problemas técnicos.

Relate quaisquer dúvidas sobre o uso do AEM ou erros técnicos usando o [Portal de suporte corporativo Experience Cloud](https://experienceleague.adobe.com/pt-br?support-solution=General#support). Ou use o [comunidade do Experience Manager](https://experienceleaguecommunities.adobe.com/t5/adobe-experience-manager/ct-p/adobe-experience-manager-community?profile.language=pt).

***As contribuições para a documentação do AEM não substituem o atendimento ao cliente da Adobe***, e quaisquer contribuições que busquem respostas a perguntas relacionadas ao suporte serão rejeitadas.

### As contribuições devem mencionar claramente as páginas pertinentes à documentação.

Se você criar um problema para sugerir melhorias na documentação, inclua links para as páginas afetadas. Se você criar um problema usando a variável **Editar esta página** em uma página de documentação, o problema é criado automaticamente com um link para a página.

Esse processo não se aplica a pull requests, que já fazem referência à página ou páginas afetadas.

## Diretrizes de documentação

Quaisquer contribuições à documentação do devem seguir determinadas diretrizes de estilo.

Seguir essas diretrizes facilita a revisão de sua contribuição, o que agiliza a integração à documentação.

### Idioma e estilo

#### Idioma

* A documentação do AEM foi criada e mantida em inglês americano.
* Mantenha as sentenças o mais simples possível.
* Use linguagem clara e concisa.

Observe que os(as) leitores(as) da documentação do AEM estão espalhados pelo mundo, e não se espera que sejam falantes nativos ou fluentes em inglês. Evite linguagem coloquial e utilize um vocabulário claro e simples.

#### Siga o Manual de Estilo da Microsoft®

[O Manual de Estilo da Microsoft®](https://learn.microsoft.com/pt-br/style-guide/welcome/) é um guia de estilo gratuito que se concentra na documentação de softwares, e a documentação do AEM o segue sempre que possível.

### Formatação

| Item | Estilo |
|---|---|
| Elemento ou opção da interface do usuário | **negrito** |
| Nome do arquivo, caminho, entrada do usuário, valores de parâmetro | `monospaced` |
| Código, linha de comando | ```Code Block``` |

### Capturas de tela

As capturas de tela devem ser utilizadas com critério e somente quando uma descrição textual for insuficiente.

Não utilize marcadores ou outras anotações em capturas de tela (como quadros vermelhos, setas ou texto). Dessa forma, as capturas de tela são mais facilmente reutilizadas ou replicadas em versões localizadas da documentação.

### Referências específicas à versão

Idealmente, evite referências diretas a uma versão específica em todo o conteúdo da documentação, sempre que possível. Essa abordagem torna a documentação mais flexível e extensível para versões futuras.

### Uso do Day, AEM, CQ, CRX

Ao mencionar o produto pela primeira vez em um artigo, sempre use seu nome completo, **Adobe Experience Manager**. Depois disso, você pode se referir a ele como **AEM**.

Não utilize Day, Day Software, CQ e CRX, exceto quando isso for inevitável, como em nomes de classe ou em referência ao histórico do AEM.