
# Materiais

Os materiais utilizados no projeto foram:
•	(1) Placa ESP32
•	(4) LEDs 
•	(4) Resistores
•	(1) Protoboard
•	(32) Fios de conexão (Jumpers)
•	(4) Sensores ultrassônicos
•	(1) Display 

# Desenvolvimento

Ideação do aplicativo e hardware: 
Foi coletada ideias e perspectivas iniciais a fim de  iniciar a idealização de como seria o molde do aplicativo, e do sistema em hardware, quais seriam suas funções e como seria seu funcionamento. Além disso, foi discutida qual ferramenta seria utilizada no desenvolvimento do aplicativo.

Pesquisa e Análise de Viabilidade: 
Nesta fase, realizamos uma pesquisa detalhada de mercado e levantamento de tecnologias disponíveis. Analisamos sensores de ocupação (ultrassônicos, infravermelhos e magnéticos), Displays digitais e recursos de conectividade (como Wi-Fi e Bluetooth), avaliando suas respectivas vantagens e limitações.Também foi feita uma reunião de como seria o desenvolvimento da maquete que representaria o funcionamento de um estacionamento inteligente.
Foram levados em conta aspectos de custo, viabilidade técnica e retorno operacional, garantindo que a proposta estivesse alinhada com as necessidades dos usuários e dos gestores.

Planejamento e Definição dos Requisitos:
Baseado nas informações coletadas, desenvolvemos um planejamento que incluiu:
- Cronograma: Definição de prazos para entrega de cada etapa (Já definido nas instruções do trabalho).
- Orçamento: Estimativas de custo dos componentes eletrônicos e no desenvolvimento da maquete.
- Requisitos Funcionais: Por exemplo, como o sistema deve se portar quando ocorrer a ocupação de uma vaga e o tempo de resposta do app.
- Requisitos Não Funcionais: Que inclui a facilidade de uso, segurança dos dados dos usuários.

Desenvolvimento e Prototipagem:
Hardware: Desenvolvemos um protótipo utilizando placas como Arduino e sensores de presença. Aqui, o circuito eletrônico foi montado em uma protoboard. Programamos os microcontroladores para ler os sinais dos sensores, que identificavam se uma vaga estava ocupada ou desocupada, e enviar essas informações para o aplicativo.

Aplicativo: Paralelamente, iniciamos o desenvolvimento de um app para dispositivos móveis, utilizando frameworks de desenvolvimento multiplataforma. O app teve interfaces dedicadas para: Exibir a disponibilidade das vagas em tempo real. Permitir a reserva prévia de vaga. Integrar funções de pagamento digital.

Testes e Validação:
Constantemente durante a construção do hardware e do aplicativo, ambos foram submetidos a diversos testes como: precisão dos sensores, confiabilidade da comunicação, para o hardware. Já para o software foi feito uma verificação na resposta em tempo real às mudanças de status dos sensores e simulamos o fluxo completo, desde a reserva até o pagamento.

Implantação e Execução:
Simulação do circuito completo e do aplicativo em uma maquete representando uma situação comum do dia dia.


## Desenvolvimento do Aplicativo

### Interface

Durante o desenvolvimento do aplicativo para o estacionamento inteligente, utilizamos a plataforma Thunkable para criar uma interface intuitiva e funcional, garantindo que os usuários pudessem acessar informações de forma rápida e eficiente. A seguir, descrevo o processo de desenvolvimento das principais telas do aplicativo:

Tela de Login e Cadastro
-Objetivo: Permitir que os usuários façam login ou se registrem para acessar as funcionalidades completas.
-Componentes: Campos de entrada para e-mail e senha, botão de "Entrar", opção de "Esqueci minha senha" e um botão de "Registrar-se".
-Desenvolvimento: Implementamos blocos de lógica que verificam credenciais inseridas, garantindo um sistema seguro e rápido.

Tela de Mapa de Vagas Disponíveis

-Objetivo: Mostrar a ocupação das vagas em tempo real através de um layout intuitivo.
-Componentes: Ícones representando vagas livres e ocupadas e opção de reserva de vaga.
-Desenvolvimento: Busca os status dos sensores do estacionamento e a tela se atualiza dinamicamente sempre que novos dados são recebidos.

 Tela de Reserva de Vaga
 
-Objetivo: Permitir que os usuários reservem vagas antes de chegarem ao estacionamento.
-Componentes: Lista com vagas disponíveis, botão de confirmação de reserva e status do tempo restante para uso.
-Desenvolvimento: Criamos um sistema de temporização que registra as reservas e, caso a vaga não seja ocupada dentro de um limite de tempo, ela é liberada automaticamente.

Tela de Pagamento
-Objetivo: Facilitar o pagamento digital do estacionamento, evitando filas e processos burocráticos.
-Componentes: Opções de pagamento via cartão de crédito, PIX e boleto bancário, além de um botão para confirmar a transação.
-Desenvolvimento: Integração com serviços de pagamento, garantindo a segurança dos dados e automatizando o cálculo do tempo de uso da vaga.

Tela de Configurações e Perfil do Usuário
-Objetivo: Oferecer personalização da experiência, permitindo alteração de dados pessoais e preferências.
-Componentes: Formulário para edição de informações, opção de notificações e suporte ao usuário.
-Desenvolvimento: Permitiu que os usuários atualizem seus dados pessoais.

### Código

Definição da Arquitetura e Fluxo de Dados
-Como os sensores de ocupação enviam informações para o banco de dados?
-Como o aplicativo recebe e exibe essas informações para os usuários?
-Qual será o fluxo para reserva de vagas e pagamento digital?

Escolha das Ferramentas e Integrações (me falem quais foram utilizadas).
-API de Pagamentos: Para processar transações financeiras, como pagamento por PIX ou cartão.
-Serviços de Autenticação: Para login de usuários via e-mail, senha ou autenticação social.

Desenvolvimento das Funções do Aplicativo
-Autenticação: Login, registro de usuários e senha
-Leitura de Sensores: Receber os dados das vagas disponíveis e ocupadas.
-Reserva de Vaga: Criar um sistema que bloqueie a vaga após a reserva e libere caso não seja usada dentro de um período.
-Pagamento: Implementar lógica para cálculo do tempo de uso e pagamento automático.
-Notificações: Alertar o usuário sobre sua reserva, ocupação da vaga e status de pagamento.

Implementação da Interface com Blocos de Código
-Criar variáveis globais para armazenar dados do usuário e do estacionamento.
-Configurar a comunicação entre telas, garantindo que os dados sejam enviados corretamente.
-Definir interações, como botões para atualizar status das vagas e ações automatizadas.

Criar funções condicionais, por exemplo:
-Se a vaga está ocupada, bloquear reserva.
-Se o tempo da reserva expirar, liberar vaga automaticamente.

Testes e Depuração
-Verificar a conexão com o banco de dados.
-Simular reservas e pagamentos para validar as ações.
-Testar diferentes dispositivos para garantir compatibilidade.
-Corrigir possíveis falhas no fluxo de reserva e ocupação das vagas.


## Desenvolvimento do Hardware

### Montagem

O processo de montagem do estacionamento inteligente envolve a integração de componentes eletrônicos, infraestrutura física e a configuração do sistema de software para garantir a comunicação entre hardware e aplicativo.

Primeiro foi feita a preparação dos componentes e materiais a serem utilizados:
Placa microcontroladora (ESP32), sensores de ocupação (sensores ultrassônicos), módulo de comunicação (Bluetooth), fonte de alimentação (bateria ou conexão elétrica), Protoboard , fios de conexão e a estrutura física do projeto (Maquete de papelão bem estruturada).

A respeito da montagem foi feita a conexão dos sensores ao microcontrolador e a programação dos pinos de entrada e saída. Logo em seguida a Configuração dos módulos de comunicação para transmissão dos dados. E ao final um teste das conexões elétricas e a validação do funcionamento dos sensores antes da instalação definitiva.

No momento da instalação definitiva do estacionamento os sensores ultrassônicos foram instalados em cada vaga, posicionados corretamente para detectar a presença de veículos. Logo foi instalada a unidade central de processamento e comunicação, que receberá os dados dos sensores e enviará para o banco de dados.

Em seguida foi realizada a integração do aplicativo ao hardware. Com isso foram executados com a comunicação entre hardware e software, garantindo que as informações sejam atualizadas em tempo real.

### Desenvolvimento do Código

Integração com Sensores de Ocupação
Para detectar a presença de veículos nas vagas, utilizamos sensores ultrassônicos. No código, fizemos a leitura dos dados de distância retornados pelo sensor para determinar se a vaga está ocupada

Comunicação com o Aplicativo (por Bluetooth)
Utilizamos apenas Bluetooth o Arduino enviava os dados para o app por meio de mensagens via serial.
Testes e Calibração

Durante o desenvolvimento, realizamos ajustes:
•	Na sensibilidade do sensor, para evitar leituras falsas.
•	No intervalo de atualização, para não sobrecarregar a comunicação.
•	Na interpretação da distância, adaptando o código à realidade do local de instalação (altura do sensor, iluminação, posição do carro etc.)

Integração com o App
O Arduino envia dados continuamente ao aplicativo, que interpreta essas mensagens e altera o status da vaga no app. Isso foi testado em conjunto com o app desenvolvido no Thunkable, garantindo que a comunicação entre hardware e software fosse estável.


## Comunicação entre App e Hardware

Comunicação via Bluetooth 
Essa abordagem foi usada com o Arduino UNO e o módulo Bluetooth.

No Arduino: O código foi programado para ler o status do sensor (ocupado ou livre) e enviar essas informações pela porta serial, que estava conectada ao módulo Bluetooth. Usamos Serial.print() para transmitir os dados.

No App (Thunkable): Utilizamos os blocos de conexão Bluetooth do Thunkable para emparelhar o aplicativo com o módulo. Após a conexão, o app fazia a leitura constante dos dados enviados pelo Arduino e os interpretava para exibir o status da vaga na tela.
