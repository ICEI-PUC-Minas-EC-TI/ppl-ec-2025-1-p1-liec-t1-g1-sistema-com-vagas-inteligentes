# Introdução

Em meio à sobrecarga das vias, muitos motoristas enfrentam longos períodos de espera e dificuldades para encontrar vagas disponíveis, o que contribui para congestionamentos generalizados. Essa realidade não só aumenta o tempo de deslocamento nas grandes metrópoles, mas também eleva os índices de poluição e o estresse cotidiano. Nesse contexto, estacionamentos convencionais se mostram cada vez mais insuficientes para atender à demanda, exigindo a implementação de sistemas integrados e inteligentes.
O estacionamento inteligente é uma solução tecnológica inserida no conceito de cidades inteligentes, que visa otimizar a ocupação e o gerenciamento de vagas em ambientes urbanos de alta densidade de veículos. Essa abordagem utiliza uma rede de sensores, dispositivos conectados, e sistemas de comunicação para monitorar em tempo real a disponibilidade de vagas, direcionar os motoristas para os espaços livres e, assim, minimizar o tempo perdido na busca por estacionamento, reduzindo o congestionamento e contribuindo para um ambiente urbano mais sustentável.
A tecnologia empregada nesse sistema combina diversos componentes: dispositivos ultrassônicos foram instalados em cada vaga para detectar a presença de um veículo. Cada sensor envia informações sobre o status da vaga para um microcontrolador, que por sua vez processam a informação e conectividade wireless para transmitir os dados a uma central, também um Arduino foi usado para processar os sinais dos sensores e transmitir os dados para o aplicativo “Park Sync” via conexão Bluetooth. Além disso, o projeto contém um display que mostra as vagas disponíveis e ocupadas, representadas por um led verde (Disponível) e um led vermelho (Ocupadas).  O sistema inclui funcionalidades de reserva de vagas e pagamento digital, tornando a experiência mais prática e segura tanto para os motoristas quanto para os administradores do estacionamento.

Justificativa:
A justificativa para a implementação de um estacionamento inteligente se baseia na necessidade premente de otimizar a mobilidade urbana e melhorar a experiência dos usuários em contextos de alta densidade de veículos. Atualmente, o tempo perdido na busca por vagas não apenas gera estresse nos motoristas, mas também contribui para congestionamentos e aumento das emissões poluentes, agravando problemas ambientais em cidades de grande fluxo. Essa perda de tempo tem impacto direto na produtividade e na qualidade de vida, especialmente em centros urbanos intensamente movimentados.
Além disso, a ineficiência na gestão das vagas compromete a rentabilidade dos estacionamentos, pois vagas ociosas ou mal direcionadas podem significar perda de receita para os administradores. Ao integrar sensores, o sistema de estacionamento inteligente oferece uma solução que reúne dados em tempo real sobre a ocupação dos espaços, permitindo uma alocação mais eficaz dos veículos e, consequentemente, um melhor aproveitamento dos recursos disponíveis.
Outro aspecto relevante é a segurança. A implementação de um sistema automatizado de monitoramento minimiza erros humanos e cria um ambiente mais seguro para os usuários, evitando fraudes e garantindo uma gestão mais rigorosa do fluxo de veículos. Com a integração de sistemas de pagamento digital, reserva de vagas e controle de acesso, o projeto proporciona uma experiência integrada e sem atritos, que é fundamental para atrair e fidelizar os usuários em um mercado cada vez mais competitivo.
Por fim, essa inovação também serve como um importante passo na transformação urbana rumo às cidades inteligentes. Ao disponibilizar dados valiosos sobre o uso dos espaços de estacionamento, as autoridades municipais podem utilizar essas informações para planejar melhor a infraestrutura urbana, reduzir congestionamentos e criar políticas públicas voltadas para a mobilidade sustentável.
Essa justificativa reforça a ideia de que a implementação de um estacionamento inteligente não é somente uma modernização operacional, mas uma resposta necessária aos desafios contemporâneos da mobilidade urbana, segurança e sustentabilidade ambiental.



## Problema

Atualmente, o crescimento vertiginoso do número de carros nas cidades é um reflexo da urbanização acelerada e da crescente dependência do transporte individual. Esse aumento expressivo de veículos impõe desafios significativos à mobilidade urbana, evidenciando a necessidade urgente de soluções sofisticadas para o controle do trânsito e a gestão dos estacionamentos.
O estacionamento inteligente é uma solução tecnológica inserida no conceito de Cidades Digitais , que visa otimizar a ocupação e o gerenciamento de vagas em ambientes urbanos como: Centros Comerciais e Shoppings, Aeroportos e Terminais de Transporte, Hospitais e Clínicas, Empresas e Prédios Corporativos, Instituições Acadêmicas, Centros Urbanos e Estacionamentos Públicos, Hotéis e Centros de Convenções e outros.

- Dificuldade para encontrar vagas: Muitos motoristas perdem tempo procurando uma vaga disponível, o que causa estresse e atrasa seus compromissos.
  
- Congestionamentos internos: O tempo excessivo gasto na procura por vagas pode levar a um trânsito desnecessário dentro do próprio estacionamento, aumentando o risco de acidentes e dificultando a circulação. Ao direcionar os motoristas para vagas específicas, o sistema melhora o fluxo de veículos.
  
- Ineficiência na gestão do espaço: Em estacionamentos com sistemas tradicionais, a ocupação e a disponibilidade das vagas não são sempre monitoradas em tempo real, o que pode levar à má utilização do espaço disponível. Um sistema inteligente permite uma gestão mais precisa e o aproveitamento ideal de cada vaga.
- Impacto ambiental: O tempo perdido procurando uma vaga contribui para a emissão de gases poluentes, pois os veículos permanecem circulando por mais tempo. Ao diminuir esse tempo, o sistema minimiza o impacto ambiental e contribui para a melhoria da qualidade do ar.
  
- Problemas de segurança e fraudes: A gestão manual das vagas pode deixar brechas para fraudes e dificultar o controle do acesso ao estacionamento. Sensores e sistemas automatizados aumentam a segurança, monitorando a entrada e saída dos veículos de forma mais eficiente.
  
- Integração com pagamentos e reservas: A falta de integração com sistemas de pagamento ou reserva pode causar transtornos tanto para os usuários quanto para os administradores do estacionamento. Soluções inteligentes permitem a reserva antecipada e o pagamento automático, simplificando todo o processo.
 
## Objetivos

Objetivo Geral:
O objetivo deste é um projeto que utiliza tecnologia e conectividade para otimizar a gestão de vagas, melhorando a experiência dos motoristas e aumentando a eficiência do espaço urbano. Esse sistema vai além do simples controle manual, integrando sensores, microcontroladores e comunicação em rede para monitorar, em tempo real, a disponibilidade de vagas em um estacionamento.
O principal foco é criar um ambiente onde os motoristas possam encontrar e reservar vagas de forma rápida e fácil. Isso é feito por meio de dispositivos que detectam se uma vaga está ocupada ou livre e enviam essas informações para uma central no caso o aplicativo móvel “Park Sync”, que as disponibiliza em uma interface amigável. Dessa maneira, os motoristas economizam tempo e evitam o estresse de procurar vaga, enquanto os administradores do estacionamento conseguem gerenciar melhor o fluxo de veículos.
 

Objetivos específicos:
- Eficiência e Economia de Tempo: Ao indicar a vaga disponível mais próxima, o sistema reduz o tempo de procura e, consequentemente, o trânsito dentro do próprio estacionamento.
  
- Redução de Emissões: Menos tempo procurando vaga significa menos emissão de gases poluentes, contribuindo para um ambiente urbano mais limpo.
  
- Integração com Cidades Inteligentes: Esse projeto pode ser parte de uma infraestrutura maior, conectando estacionamentos a sistemas de gestão urbana, que otimizam o trânsito e a mobilidade urbana.
  
-Desafios e Extensões: A implantação de um estacionamento inteligente pode se expandir para incluir sistemas de segurança integrados, monitoramento via câmeras, manutenção preditiva das estruturas e até parcerias com aplicativos de mobilidade. Tecnologias avançadas, como o machine learning, também podem ser incorporadas para prever padrões de uso e ajustar a gestão de acordo com a demanda.

 
## Público-Alvo

Motoristas Usuários
- Conhecimentos Prévios e Habilidades Tecnológicas: A maioria dos motoristas terá conhecimentos básicos de tecnologia. Eles estão habituados a usar smartphones para navegação, pagamentos via apps e redes sociais. Não é necessário um conhecimento técnico avançado, mas a experiência com interfaces digitais intuitivas é essencial.
  
- Perfil e Hábitos: Geralmente, são adultos entre 20 e 50 anos, que atuam em diferentes áreas: profissionais, estudantes e visitantes de áreas comerciais. Estão em busca de soluções práticas que otimizem seu tempo, pois em muitos casos enfrentam o estresse de procurar vagas em horários de pico.
- 
- Expectativas em Relação ao Sistema: Esperam receber informações em tempo real sobre a disponibilidade de vagas, com notificações rápidas e um design de interface claro e simples. Além disso, a integração com sistemas de pagamento digital e reserva de vagas pode agregar valor, facilitando a experiência de uso.
Gestores e Administradores do Estacionamento

- Conhecimentos Prévios e Habilidades Tecnológicas: Este grupo possui conhecimentos intermediários a avançados em sistemas de gestão e soluções tecnológicas. Eles estão familiarizados com o uso de dashboards, análise de dados e monitoramento em tempo real, já que a eficiência operacional é um critério importante em suas responsabilidades.
  
- Perfil e Hábitos: São profissionais que buscam reduzir custos operacionais, otimizar o uso do espaço e melhorar a experiência dos usuários. Geralmente, estão envolvidos em tomada de decisões estratégicas e na gestão de recursos, acompanhando a performance do sistema através de relatórios e métricas.

- Expectativas em Relação ao Sistema: Precisam de uma plataforma robusta que facilite a gestão de dados, a análise de ocupação e o monitoramento das operações. Esperam ferramentas que permitam identificar problemas e adotar ações corretivas rapidamente, assim como a integração com outros sistemas (como pagamento e controle de acesso).
Técnicos e Equipe de Suporte

- Conhecimentos Prévios e Habilidades Tecnológicas: Este grupo é composto por profissionais com alto nível de conhecimento técnico, familiarizados com redes de sensores, manutenção de hardware e software, além do gerenciamento de infraestrutura de TI.
  
- Perfil e Hábitos: São os responsáveis pela instalação, monitoramento e manutenção do sistema. Trabalham com diagnósticos e atualizações frequentes para assegurar a operação contínua e confiável do sistema.
  
- Expectativas em Relação ao Sistema: Esperam receber ferramentas que facilitem a identificação e resolução de falhas, acesso remoto para monitoramento e uma integração que permita atualizações e expansão sem complicações. A clareza na arquitetura do sistema e a capacidade de escalabilidade são pontos cruciais para esse grupo.
