# Água / Luz - Notification - Case

#### Case 1
Nossa fabrica de software foi designada a criar um aplicativo para notificar confirmação de `Contrato` de instalação de água e luz em `Cadastro`s realizados em sua cidade.

###### O aplicativo deverá enviar a seguinte mensagem:

Senhor(a) **Gleyson Sampaio**,
Informamos que conforme contrato com protocolo de número **2022025687** está agendado para a data **21/02/2022** as **16:00h** a instalação da **Água\Luz** com taxa de valor R$ **127,33** em sua residência localizada no endereço abaixo:

- Logradouro: **Rua das Marias, 243**
- Complemento: **Ap 207, Bloco C**
- Bairro: **Santo Antonio**
- Cidade: **São Paulo / SP**
- Cep: **27.310-657**

###### Requisitos
1. A primeira versão deverá contemplar o envio da notificação via
SMS para o número do celular cadastrado.
2. A segunda versão deverá ter uma opção no cadastro se o usuário gostaria de receber as notificações via SMS ou WhatsApp.

#### Case 2

Nossa fabrica de software foi designada a criar um aplicativo para atrair e notificar confirmação de `Contrato` de instalação de água e luz em `Cadastro`s realizados em sua cidade.

###### O aplicativo deverá enviar a seguinte mensagem:

Senhor(a) **Gleyson Sampaio**,
Informamos que conforme contrato com protocolo de número **2022025687** está agendado para a data **21/02/2022** as **16:00h** a instalação da **Água\Luz** com taxa de valor R$ **127,33** em sua residência localizada no endereço abaixo:

- Logradouro: **Rua das Marias, 243**
- Complemento: **Ap 207, Bloco C**
- Bairro: **Santo Antonio**
- Cidade: **São Paulo / SP**
- Cep: **27.310-657**

1. Podem existir cadastros fora do Brasil.
2. Valores data e momentários devem considerar a localização do cadastro
3. Existem dois serviços com valores fixos: Água R$ 137,21 e Energia R$ 132,15

###### Arquitetura

1. Serão dois projetos Java Maven denominados: agua-luz-atracao e agua-luz-notificacao
2. O projeto agua-luz-atracao deverá disponibilizar um mecanismo de inclusão dos dados de cadastro
3. O projeto agua-luz-atracao deverá disponibilizar um arquivo de nome:
  - agua-luz-cadastros.csv obedecendo o layout padrão delimitador (;) 
  - agua-luz-cadastros.txt obedecendo o layout padrão posicional 
  
