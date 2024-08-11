Desafio de Criação de Phishing da DIO: Gerador de Links de Phishing
Este projeto tem objetivo educativo, conscientização de como é fácil gerar um link falso de phishing, sobre as práticas de phishing e demonstrar a capacidade de gerar estes, utilizando um ambiente controlado para testes éticos de segurança. Não é para ser usado de forma maliciosa ou ilegal.

Descrição
As ferramentas usadas serão Social Engineering Toolkit (SeToolKit) que permite a criação de links de phishing e muito mais, sendo usada aqui para fins educativos, e o Zphisher que, assim como o SeToolkit, permite a criação de links de phishing para recuperar credenciais. Este projeto destina-se a profissionais de segurança, pesquisadores e estudantes interessados em aprender sobre as ameaças de phishing e as medidas para combatê-las. Como será usado para estudo, teste e aperfeiçoamento, serão utilizados somente IP interno nos testes.

Ferramentas
Kali Linux
Terminal Linux
SeToolKit
Zphisher
Atenção
Uso Responsável: Antes de usar esta ferramenta, obtenha permissão explícita do proprietário do sistema ou vítima a ser testado.
Legislação:Respeite as leis e regulamentos locais relacionados à segurança da informação e testes de penetração.
Propósito Educacional:Este projeto destina-se exclusivamente a fins educativos e de treinamento em segurança da informação. Não use este projeto para atividades maliciosas.
Como usar
Primeiramente tenha as ferramentas instaladas em seu sistema operacional. Siga o passo a passo de instalação das ferramentas nos sites correspondentes: SeToolKit e Zphisher Atente-se para o fato de o passo a passo será feito utilizando o Kali Linux virtualizado (WSL) e que as duas ferramentas são CLI (interfaces de linha de comando).

Iniciaremos com o SetoolKit.
A ferramenta é baseada em menus de seleção, como a ordem dos números pode alterar com o tempo, incluirei somente o nome da opção a selecionar. Caso queira explorar melhor as demais opções, a ferramenta possui uma documentação bem completa, não exite em lê-la:

Abra o terminal
Digite: sudo su
Digite sua senha na sequência
Agora digite: setoolkit
A primeira opção do menu a ser selecionada será: Social-Engineering Attacks
A segunda opção do menu a ser selecionada será: Website Attack Vectors
A terceira opção do menu a ser selecionada será: Credential Harvester Attack Method
A quarta eúltima opção do menu a ser selecionada será: Site cloner
Ao apresentar um diálogo sobre o endereço de IP que será usado, pode só clicar no enter mesmo, pois a ferramenta detecta o IP da máquina e marca ela como default.
Agora que vem a transformação do link. De acordo com a ferramenta, pode ser utilizado HTTP e HTTPS. No desafio foi utilizado o http://www.facebook.com, entretanto, provavelmente por alguma medida do Facebook, não está mais sendo possível (ao menos até o presente momento deste teste) realizar o clone de forma funcional do mesmo. Portanto iremos utilizar como exemplo o LinkedIn.
Digite o link no terminal e de enter: https://www.linkedin.com/
Para acessar o clone e testar, use o ip address que foi usado na etapa 9.
Após logar, irá aparecer log bem extensos no terminal. E, por algum motivo, a obtenção do login não aparece em "USERNAME FIELD FOUND", mas sim em PARAM: session_key=<usuário digitado> que estará logo abaixo do primeiro [*] WE GOT A HIT! Printing the output:
![Linkedin](https://github.com/user-attachments/assets/84730682-6a06-4813-8c99-b480dd34ee2a)
![Terminal-setoolkit](https://github.com/user-attachments/assets/ffd9fd85-02f2-4e59-a219-d6fd3b868f52)

Agora usaremos o Zphisher:
Aassim como o SeToolKit, é uma ferramenta baseada em menus de seleção, então, também manterei apontando as opções usadas pelo texto, e não número da opção. Caso queira explorar melhor as demais opções, esta ferramenta também possui uma documentação bem completa, não exite em lê-la: Com o Zphisher, está sendo possível clonar o facebook sem problemas. Utilizaremos ele para exemplo. Após ter clonado o Zphisher como demonstra o site oficial, você fará o seguinte:

Abra a pasta do Zphisher: No meu caso ficou /home/albus/zphisher, por tando uso cd zphisher/ estando na pasta pessoal mesmo.
Depois insida o comando: bash zphisher
Irá aparecer várias opções possíveis de utilizarmos. Mas nos ateremos ao facebook. Digite os dois números correspondente ao facebook e de enter.
Agora iremos selecionar qual das páginas do facebook iremos clonar. No meu caso, selecionei a tradicional: Traditional Login Page
Neste ponto, iremos perceber que inclusive podemos gerar um link falso pela web mesmo para poder enviar. Mas no momento iremos utilizar somente o Localhost.
Será questionado se quer altera a porta. Digite N.
Após isso ele irá abrirá uma tela com o seu localhost para clicar. Clicando será direcionado para a página fake do facebook. Os dados digitados irão aparecer nesta mesma tela do Zphisher.
![Terminal-zphisher](https://github.com/user-attachments/assets/c13eb816-104c-45e5-8ba5-6a606b367a94)
![Facebook](https://github.com/user-attachments/assets/3b2cdf07-9b3a-45c2-93ad-187d0a75521c)










