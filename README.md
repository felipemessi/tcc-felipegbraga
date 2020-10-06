# tcc-felipegbraga

# Introdução

Usar a fala para pedir ou fazer uma requisição é algo que os humanos fazem (ou pelo menos tentam) desde bebês quando soltam o primeiro "mamá" solicitando que a necessidade de alimentação seja atendida. Desde a década de 50, estudos na área de Inteligência Artificial (Artificial Intelligence - AI) buscam utilizar a voz como meio de interação humano-máquina, uma vez que a voz é uma das formas mais naturais de interação entre as pessoas (SILVA; MARTINS; FERNANDES, 2012). 

Com o avanço dos estudos e consequente evolução da tecnologia, o mouse, o teclado e o monitor de vídeo deixaram de ser as únicas interfaces humano-máquina e permitiram a chegada, nas últimas décadas, das telas sensíveis ao toque (touch screen), além das interfaces de reconhecimento de imagem e voz (NEGRI; LEDEL,  2016). O progresso na área  de processamento de sinais de fala tem permitido o aprimoramento dos sistemas STT (Speech-to-Text), possibilitando o desenvolvimento de aplicações de voz que fossem capazes de atuar em diversos cenários, como nos programas de acessibilidade, para agilizar uma tarefa ou até evitar a intervenção física do usuário em determinado ambiente (LEITE ET AL, 2014).

Quem nunca brincou com a Cortana no Windows ou com o "Ok google" no Android ou "Siri" no IOS fazendo as mais diversas perguntas?  Pensando nessa facilidade dos seres humanos em se comunicar e tentar atender os seus desejos por comandos de voz e a crescente demanda desse mercado, por que não aliar essa tecnologia à programação de sistemas de informação? Fazer uma requisição por voz pode ser muito mais intuitivo, diminuindo assim a curva de aprendizado, é rápido e simples, além de ajudar na produtividade.

Para responder a pergunta de como fazer essa união de comandos de voz e programação é necessário entender qual seria a maneira de atingir mais pessoas com essa solução. A pesquisa sobre os principais editores de códigos apontou que o Visual Studio Code (VS Code) da Microsoft era um excelente candidato, porque além de ser de código aberto é o que possui mais estrelas no github entre os editores de código (GITHUB, 2020a) (GITHUB, 2020b) (GITHUB, 2020c).

Com a escolha do Visual Studio Code ficou claro que uma das melhores formas de fazer a integração da solução de comando de voz com programação seria através de uma extensão do Visual Studio Code, que é uma maneira de adicionar novas funcionalidades ao editor de texto. Além de integrarem muito bem a ferramenta, as extensões permitem que o usuário consiga instalar de maneira simples através da loja de extensões do VS Code.

### 1.1 Objetivo

Desenvolver uma extensão para o VSCode que implemente funcionalidades que auxiliem no aprendizado e produtividade no desenvolvimento de Sistemas de informação através de comando de voz.

### 1.2 Organização

Este trabalho está divido entre os seguintes capítulos:
2 - Fundamentação Técnica
O capítulo expõe as tecnologias necessárias para o desenvolvimento deste trabalho.
3 - Desenvolvimento
Este capítulo aborda detalhadamente o desenvolvimento de uma extensão para o Visual Studio Code que adiciona a capacidade de fazer requisições de voz no editor de texto.
4 - Resultados
Neste capítulo são expostos os resultados alcançados com o uso da extensão aplicada em ambiente real de desenvolvimento.
5 - Considerações Finais
Este capítulo apresenta as conclusões obtidas através dos resultados dos experimentos e sugere novas funcionalidades a serem implementadas no futuro.

# 2 - **Fundamentação Técnica**

O presente capítulo contempla o embasamento técnico do projeto, explorando as ferramentas, bibliotecas e tecnologias utilizadas no desenvolvimento do projeto. A apresentação deste capítulo está organizada da seguinte maneira:

2.1 - Reconhecimento de voz

2.2 - API Speech to Text 

2.3 - Visual Studio Code

### 2.1 Reconhecimento de voz

Reconhecimento de voz é a capacidade de um dispositivo eletrônico de conseguir "entender" a fala humana. O dispositivo recebe como entrada um sinal analógico (voz) através de um microfone, processa e por fim interpreta o sinal através de um software de reconhecimento de voz que será o responsável por atribuir algum significado digital ao som recebido (OLIVEIRA, 2019).

![https://github.com/felipemessi/tcc-felipegbraga/blob/master/Untitled.png](https://github.com/felipemessi/tcc-felipegbraga/blob/master/Untitled.png)

O desenvolvimento contínuo da tecnologia de reconhecimento de voz tem permitido o desenvolvimento de aplicações principalmente para as áreas de saúde, marketing, segurança e uso cotidiano. E é fácil identificar uma boa aplicação para essa tecnologia, basta pensar em situações em que você tem as mão, olhos ou mobilidade limitada (OLIVEIRA, 2019). 

Porém, é necessário reconhecer que existem algumas limitações que precisam de atenção ao utilizar o reconhecimento de voz em alguma aplicação, dentre as principais limitações estão o idioma de entrada, a fadiga de falar continuamente e a velocidade de reação que é menor do que a visual (Shneiderman, 2000).

### 2.2 API Web Speech

Desenvolvida pela Mozilla e pelo Google a Web Speech API é uma API JavaScript que permite incorporar o processamento de dados de voz principalmente em aplicações Web. No presente estudo será utilizada a funcionalidade de Speech-to-Text apesar da API possuir capacidade de operar nos dois sentidos (voz para texto e texto para voz).  A Web Speech API tem uma variedade de eventos bem completa e documentação amigável e permite um nível de configuração de confiança, erros e controle basta profundo (GOOGLE, 2020).

![](https://github.com/felipemessi/tcc-felipegbraga/blob/master/Untitled%20(1).png)

A API Web Speech foi escolhida para a utilização nesse projeto pois ela apresenta diversas conveniências, bem como, ser gratuita (até 50 minutos por mês), utilizar a linguagem de programação Javascript que é a mesma que será utilizada em todo o projeto, ter suporte ao idioma Português Brasileiro e ter o suporte do Google e acesso a ampla comunidade técnica acerca dessa tecnologia (GOOGLE, 2020).

### 2.3 Visual Studio Code

O Visual Studio Code (VS Code) é um editor de código desenvolvido pela Microsoft, gratuito e *open source* e que inclui diversas funcionalidades, dentre elas a possibilidade de debugging, intelligent code completion, code refactoring e integração com o Git. Além disso o VS Code tem suporte para inúmeras linguagens de programação, bem como Java, C, C++. C#, Javascript, Python, etc (MICROSOFT, 2020).

![](https://github.com/felipemessi/tcc-felipegbraga/blob/master/Untitled%20(2).png)

Extensões do VS Code são uma maneira de você adicionar alguma funcionalidade nova ao software, ampliando suas capacidades. Uma extensão pode acrescentar um visual diferente, suporte à uma linguagem, ou alguma maneira diferente de executar um comando. Para criar uma extensão para o VS Code é necessário utilizar a API do VS Code (MICROSOFT, 2020).

![](https://github.com/felipemessi/tcc-felipegbraga/blob/master/Untitled%20(3).png)

# Referências

NEGRI, F.; LEDEL, L. C. Plataforma de  Hardware e  Software com  Interface de Reconhecimento. 2016. Disponível em: <http://hto.ifsp.edu.br/portal/images/thumbnails/images/IFSP/Cursos/Coord_ADS/Arquivos/TCCs/2016/TCC_FelipeNegriDeOliveira.pdf>. Acesso em: 06 out. 2020.

OLIVEIRA, B. Integração de Reconhecimento, Síntese e Gravação de Voz no Sistema de Tratamento de Atas. 2019. Disponível em: <https://comum.rcaap.pt/bitstream/10400.26/29856/1/Bruno-Miguel-Fernandes-Oliveira.pdf>. Acesso em: 06 out. 2020.

LEITE et al. Avaliação de Vozes Artificiais: Inteligibilidade, Compreensibilidade e Naturalidade. 2014. Disponível em:<https://siaiap32.univali.br/seer/index.php/acotb/article/view/5314/2776>. Acesso em: 06 out. 2020.

SHNEIDERMAN, B. The Limits of Speech Recognition. 2000. Disponível em: <https://www.cs.umd.edu/users/ben/papers/Shneiderman2000limits.pdf>. Acesso em: 06 out. 2020

GOOGLE. Web Speech API Specification. Disponível em: <https://wicg.github.io/speech-api/>. Acesso em: 06 out. 2020.

GITHUB. VS Code Repositório do Github. Disponível em:<https://github.com/microsoft/vscode>. Acesso em: 06 out. 2020a. 

GITHUB. Atom Repositório do Github. Disponível em:<https://github.com/atom/atom>. Acesso em: 06 out. 2020b.

GITHUB. Vim Repositório do Github. Disponível em:<https://github.com/vim/vim>. Acesso em: 06 out. 2020c.
