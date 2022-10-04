# Facebook-Login-Test: Plano de Teste

## Nome do projeto

Verificando a funcionalidade do login do Facebook

## Resumo

O sistema de login do Facebook, hospedado em [https://www.facebook.com/login](https://www.facebook.com/login), permite que os usuários da rede social acessem seus usuário por meio de e-mail e senha corretos, portanto, deve-se verificar a funcionalidade correta deste módulo por meio da validação dos dados de login, a fim de comprovar que os usuários possuem uma interface segura para o acesso. Dessa forma, este plano de teste propõe a realização de testes funcionais de caixa-preta, à nível de integração, aplicando a técnica de casos de uso durante o processo de testes, afim de verificar a funcionalidade deste módulo.

## Pessoas envolvidas

O testador responsável pela execução dos testes será o aluno Guilherme Feitosa, estudante do IFTO Campus Palmas, matriculado no curso superior de Tecnologia em Sistema para internet.

## Funcionalidades ou Módulos a serem testados

- Módulo de login de usuários

## Local dos testes

Os testes serão realizados no laboratório LabDes localizado dentro do estabelecimento do Instituto Federal de Educação, Ciência e Tecnologia (IFTO) Campus Palmas.

## Recursos necessários

- Computadores com acesso à internet e navegador devidamente instalado e atualizado.

## Critérios usados

- Para que a funcionalidade seja considerada correta, todos os casos de teste devem ser
executados com sucesso;
- Os dados de e-mail e senha podem ser classificados em válido, inválido ou em branco, possuindo os seguintes significados para e-mail e senha:
    - E-mail válido: um e-mail já cadastrado no sistema;
    - E-mail inválido: um e-mail ainda não cadastrado no sistema;
    - Senha válida: uma senha compatível com o e-mail informado;
    - Senha inválida: uma senha incompatível com o e-mail informado;
    - Em branco: nenhum valor informado.
- Os dados de e-mail e senha são *case sensitive;*
- O sistema pode considerar a entrada de e-mails inválidos, caso ele considere que o usuário tenha cometido um leve erro de escrita, informando o e-mail possivelmente correto.
- Visando a grande quantidade de classificação dos dados informados, será utilizado a técnica de casos de uso;

### **Dados do Teste:**

| E-mail | Senha | Resultado |
| --- | --- | --- |
| guilherme.milhomem2@estudante.ifto.edu.br | c14YyW3h3NtA3mvY9gLTbA== | Válido |
| bordeaux55@optonline.net | j121903j | Inválido |
| krsscheer@centurytel.net | terry2 | Inválido |
| mhelies@yahoo.com | skipternet1 | Inválido |

### **Casos de Teste:**

| Caso de Uso | Entrada | Saída |
| --- | --- | --- |
| CT1 | E-mail: em branco | Senha: em branco | O sistema exibe a mensagem “O email ou o número de celular que você inseriu não está conectado a uma conta. Encontre sua conta e entre.” |
| CT2 | E-mail: válido | Senha: em branco | O sistema exibe a mensagem “A senha inserida está incorreta. Esqueceu a senha?” |
| CT3 | E-mail: válido | Senha: inválida | O sistema exibe a mensagem “A senha inserida está incorreta. Esqueceu a senha?” |
| CT4 | E-mail: inválido | Senha: em branco | O sistema exibe a mensagem “O email que você inseriu não está conectado a uma conta. Crie uma nova conta do Facebook.” |
| CT5 | E-mail: inválido | Senha: inválida | O sistema exibe a mensagem “O email que você inseriu não está conectado a uma conta. Crie uma nova conta do Facebook.” |
| CT6 | E-mail: válido | Senha: válida | Usuário redirecionado para a Página Inicial |

## Riscos

Como a funcionalidade pertence a um site, será necessário apenas um computador
com conexão com a internet e um browser instalado. Os riscos desse cenário estão
relacionados à ausência de conexão com a internet e de um browser atualizado. Esses
riscos devem ser mitigados da seguinte forma:

- Ausência de internet
    - Se o servidor/máquina do professor estiver desligado, ligue-o. Espere alguns
    minutos e tente novamente.
    - Caso o computador escolhido não tenha conexão com a internet, escolha um outro
    equipamento em uma outra bancada. Caso ele possua internet, usá-lo, caso
    contrário, faça uma nova escolha até que todas as bancadas tenham sido
    verificadas. Se ainda assim, não houver conexão, dirigir-se a um outro laboratório
    de informática do IFTO.
- Browser antigo
    - Atualizar o browser usando o procedimento padrão do sistema operacional
    existente no equipamento.

## Como os resultados do teste serão divulgados

## Cronograma
