# Conectando seu ISP a uma operadora

Para concluir este tutorial, você deve ter uma conta válida na AWS.

Neste capítulo, vamos integrar o WeHostVoIP com o signalwire e o conector de voz da AWS.

Você pode conectar praticamente qualquer provedor de serviços SIP. Nesta seção, mostraremos como se conectar ao conector de voz da AWS. A razão pela qual estamos usando a AWS é porque ela é simples e amplamente disponível. Não endossamos nem recomendamos o conector do AWS Voice, estamos apenas usando-o como exemplo. Se você é um provedor de serviços e quer aparecer no WeHostVoIP, entre em contato.

## Etapa 1 Criando o tronco SIP na AWS

Acesse o console CHIME na AWS

https://console.chime.aws.amazon.com/

## Etapa 2 Crie um novo conector de voz na AWS

Chamando=>Conector de Voz

* Nome: começando
* Região (leste-se - N.Virgínia)
* Criptografia: Desativado.

![imagem](https://user-images.githubusercontent.com/4958202/153879892-fb23e423-ecce-42d5-ac72-6d9a482f9548.png)

## Etapa 3 Criar uma rescisão na AWS

Clique em começar

Selecione a guia **Rescisão**

Habilite e autorize o endereço demo.wehostvoip.io. Ao gravar as instruções o host era 44.196.134.37. Use ping para demo.wehostvoip.io e confirme este endereço pelase. Pode mudar no futuro.

![imagem](https://user-images.githubusercontent.com/4958202/153880399-2980628f-b5f8-4939-96f1-e869482a8ff1.png)

![imagem](https://user-images.githubusercontent.com/4958202/153880754-4883710f-32e1-4309-9ea7-36a4e6ef719d.png)

Defina chamadas por segundo para 1, plano de chamadas, autorize apenas seu próprio país. Nenhuma credencial necessária o IP está autorizado.

## Etapa 4 Crie uma nova operadora em WHV

Agora você precisará criar uma operadora e um gateway no lado WeHostVoIP. Ao criar um gateway, adicione o nome do host de saída como o endereço e do domínio.

![imagem](https://user-images.githubusercontent.com/4958202/153885655-f3177ec0-57b1-48b6-9f21-ad1ff8babc96.png)

Após adicionar o gateway associado à operadora. Na descrição defina AWS-CHIME

![imagem](https://user-images.githubusercontent.com/4958202/153885698-6088271c-b336-4bd2-828d-db32c99f18e1.png)

Depois que a terminação for criada, você poderá ligar para outros números nos EUA.

## Etapa 5 Atribua um número de telefone na AWS

A AWS não oferece suporte ao recebimento de chamadas sem um ID do chamador no formato E164. Então vamos assing um novo nember. Alocar um número de telefone no AWS-CHIME em

chamando=>gerenciamento de números de telefone.

Aloque um número e associe-o ao seu conector.

![imagem](https://user-images.githubusercontent.com/4958202/153887696-6bd46880-d549-4a6d-b2a5-0cf6247f926e.png)

## Etapa 6 Altere a operadora no Locatário em WHV

Para usar esta operadora, você deve alterá-la na configuração do locatário (interface ISP)

![imagem](https://user-images.githubusercontent.com/4958202/153886446-6ed243e5-34f3-4f08-abf9-2ef5a0168025.png)

## Etapa 7 Adicione os prefixos ao grupo de segurança

Vá para os grupos de segurança, adicione os prefixos para EUA selecionando o país. Adicione também o prefixo para chamadas gratuitas, adicione 18 como prefixo, abrange todas as variações de chamadas gratuitas.

## Etapa 8 Tente fazer uma chamada externa

Ligue para um número gratuito, como 8004337300

## Etapa 9 Adicione o número da AWS ao inventário

Na interface do ISP, vá para o inventário de números e insira o registro do número.

![imagem](https://user-images.githubusercontent.com/4958202/153927472-3781c1d5-7e23-45a9-82ed-bcdf452cb739.png)

Os dados a serem inseridos dependem do número alocado na AWS

Após adicionar o número deve aparecer no sistema

![imagem](https://user-images.githubusercontent.com/4958202/153927704-dfce1b66-8ccf-471c-8cb6-3dffa82cfbe2.png)

## Passo 10 - Associe o número a um usuário em WHV

Na interface do locatário em número de telefone, crie o número e associe a Alice.

![imagem](https://user-images.githubusercontent.com/4958202/153927979-5bd640aa-21e4-46a7-b579-2915b9837fe3.png)

## Passo 11 - Disque o número de um telefone externo

Verifique se a chamada chegou bem.