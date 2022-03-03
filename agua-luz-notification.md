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

1. Podem existir cadastros fora do Brasil que muda a formatação de algumas informações.
2. Valores data e momentários devem considerar a localização do cadastro
3. Existem dois serviços com valores fixos: Água R$ 137,21 e Energia R$ 132,15

###### Arquitetura

1. Serão dois projetos Java Maven denominados: agua-luz-atracao e agua-luz-notificacao
2. O projeto agua-luz-atracao deverá disponibilizar um mecanismo de inclusão dos dados de cadastro (fake banco de dados)
3. O projeto agua-luz-atracao deverá disponibilizar dois arquivos no diretório `C:\estudo\mjv-java-school\agua-luz-output` com os nomes abaixo:
  - agua-luz-contratos.csv obedecendo o layout padrão delimitador (;) 
  - agua-luz-contratos.txt obedecendo o layout padrão posicional
4. O projeto agua-luz-notificacao deverá realizar a leitura dos contratos pelo arquivo `agua-luz-contratos.txt` para poder criar e enviar a mensagem via Sms ou Whatsapp
5. O projeto agua-luz-notificacao deverá realizar a geração de arquivo `contrato-xxx.txt` contendo a mensagem gerada. (Este requisito é um PLUS)

###### Layout posicional

Segue regras para posicionamento dos campos para o layout

| Campo  | Ordem |Tam.|Texto Original|Texto Layout
| ------ | ----- |--- | ------------ | ------------- |
| CPF | 01 |11 | 007.324.223.21 | 00732422321 |
| NOME | 02 |30 | Raimundo Nonato Loureiro Castelo Branco | RAIMUNDO NONATO LOUREIRO CASTE |
| CELULAR | 03 |11 | (11) 99768-1515 | 11997681515 |
| LOGRADOURO | 04 |20 | Rua Sebastião Firmino| RUA SEBASTIÃO FIRMI |
| NUMERO | 05 |06 | 123| 000123 |
| COMPLEMENTO | 06 |10 | AP 210 BL CENTAURO| AP 210 BL |
| BAIRRO | 07 |15 | São Sebastião| SÃO SEBASTIÃO |
| CIDADE | 08 |30 | São Raimundo Nonato| SÃO RAIMUNDO NONATO           |
| UF | 09 |02 | Sp| SP|
| CEP | 10 |08 | 07.210.715 | O7210715 |
| PROTOCOLO | 11 |10 | 1984365 | 0001984365 |
| DATA | 12 |08 | 07/05/2022 | 20220507 |
| HORA | 13 |04 | 15:21 | 1521 |
| TIPO | 14 |01 | AGUA ou LUZ | A ou L |
| VALOR | 15 |08 | 127,35 | 00012735 |

#### Case 3

Nossa fabrica de software agora precisará armazenar os dados de atração em um banco de dados relacional PostgreSQL ou MySQL.
