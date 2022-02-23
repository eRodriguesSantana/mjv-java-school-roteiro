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

Senhor(a) **Gleyson Sampaio** cpf de número **234.765.987-27**,
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
2. O projeto agua-luz-atracao deverá disponibilizar um mecanismo de inclusão dos dados de cadastro (fake banco de dados)
3. O projeto agua-luz-atracao deverá disponibilizar um arquivo de nome:
  - agua-luz-cadastros.csv obedecendo o layout padrão delimitador (;) 
  - agua-luz-cadastros.txt obedecendo o layout padrão posicional

###### Layout posicional

Segue regras para posicionamento dos campos para o layout
1. CPF: 11 dígitos sem caracteres especiais;
2. NOME: 30 dígitos
3. LOGRADOURO: 20 dígitos
4. COMPLEMENTO: 10 dígitos
5. BAIRRO: 15 dígitos
6. CIDADE_UF: 20 dígitos + UF 2 dígitos
7. CEP: 8 dígitos sem caracteres especiais;
8. PROTOCOLO:10 dígitos
9. DATA: 8 dígitos formato YYYYMMDD
10. HORA: 4 dígitos formato HHMM
11. TIPO_INSTALACAO: 1 dígito A ou L
12. VALOR: 8 dígitos removendo os símbolos e preenchendo com zero a esquerda
  
