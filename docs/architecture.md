## Arquitetura ##

WeHostVoIP é organizado em uma arquitetura em camadas. Os principais componentes do sistema são:

1. Cluster de proxies SIP
2. Controladores de borda de sessão e mídia

O cluster de proxies SIP é responsável pela alta disponibilidade e pela centralização da sinalização. Os controladores de borda de sessão e mídia são os cavalos de trabalho do sistema. Eles processam todas as chamadas e o retransmissor de mídia entre elas. O SMBC pode ser instalado no local para máxima privacidade e a menor latência possível. A arquitetura do sistema pode ser visualizada abaixo:

![WeHostVoIP_Arquitecture](https://user-images.githubusercontent.com/4958202/147883266-19256a68-8730-4d33-aaba-678e07e7c512.png)

A vantagem para os clientes é evitar todo o trabalho necessário para balancear a carga dos servidores. É muito difícil combinar desenvolvimento de software com serviços. Ao usar o WeHostVoIP, você pode começar a vender amanhã, não em dois anos.

### Minimalismo

Restringimos recursos como Presença, Conferência e Fila. Estamos posicionando o sistema para pequenas e médias empresas, não para Contact Centers ou Grandes Empresas. O objetivo é permitir alta escalabilidade nas vendas evitando a duplicação de recursos com Microsoft Teams e Google Apps. Sabemos que a maioria das empresas está usando e-mail com uma dessas duas empresas. Não há propósito em duplicar os recursos de presença, conferência e bate-papo. O que estamos fornecendo é um complemento do sistema telefônico para usuários do Google e da Microsoft.