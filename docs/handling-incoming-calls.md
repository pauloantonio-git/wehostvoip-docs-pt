## Lidando com chamadas recebidas com o plano de discagem visual

Por enquanto, você tratou as chamadas recebidas diretamente para um assinante. Tudo bem, porém temos algo muito mais sofisticado para receber chamadas chamado Plano de Discagem Visual. Siga as instruções passo a passo abaixo para receber chamadas para um IVR.

Para este guia de primeiros passos, lidaremos com as chamadas recebidas desta maneira:

1. Verifique se o horário de funcionamento. Se estiver em horário comercial, toque o IVR ou toque uma mensagem informando ao usuário qual é o nosso horário comercial.
2. No IVR, vamos criar um menu 1 para vendas, 2 para finanças, 3 para suporte técnico.
3. Se o usuário não digitar nada ou digitar um número inválido, tente novamente 3 vezes
4. Para vendas, crie uma lista de assinantes para tocar simultaneamente
5. Para suporte técnico envie a ligação para bob
6. Para finanças, ligue para alice

## Etapa 1 Crie o horário comercial

Crie um período de tempo chamado default e defina o horário de segunda a sexta, das 9h às 17h, como mostrado abaixo.

![imagem](https://user-images.githubusercontent.com/4958202/154132378-9d6729ff-5ef2-4c45-b66f-375e99d585b2.png)

## Etapa 2 Crie um plano visual

Você receberá uma tela como abaixo

![imagem](https://user-images.githubusercontent.com/4958202/154132687-01e6fac2-0d88-4fa4-ae01-60afa695a8c4.png)

Adicione o bloco de timerouting, crie uma reprodução se não estiver em horário comercial e um ivr se estiver em horário comercial.

![imagem](https://user-images.githubusercontent.com/4958202/154132917-e5acbffb-b66f-4a99-beba-2f7fbc4e1e96.png)

Agora vamos personalizar a mensagem para horas de folga. Selecione texto para fala, use Joanna como voz.

![imagem](https://user-images.githubusercontent.com/4958202/154133123-82135458-37c6-48a0-b2ca-91833d2af4fd.png)

Então vamos personalizar o IVR. O plano visual final deve ficar como abaixo.

![imagem](https://user-images.githubusercontent.com/4958202/154133613-0f2384f8-09c9-4935-963f-ad17058dea0c.png)

**Não se esqueça de salvar seu plano**

## Etapa 3 Associar um número de telefone a um Plano Visual

Crie um assinante chamado vdp (Visual Dial Plan)

![imagem](https://user-images.githubusercontent.com/4958202/154134154-9fa813c8-ab44-4534-8c20-439ee16f40d0.png)

Agora no número do telefone, altere o usuário associado de Alice para vdp

## Etapa 4 Testar uma chamada recebida