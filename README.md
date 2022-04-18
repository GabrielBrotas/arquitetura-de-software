# Arquitetura de Software

## Tipos de Arquitetura

- Arquitetura Tecnológica
- Arquitetura Corporativa
- Arquitetura de Solução
- Arquitetura de Software

<br />

**Arquitetura Tecnológica**

Especialidade em tecnologias específicas de mercado, manja muito bem de uma tecnologia/ferramenta.

Geração de valor baseado em especialidades;

Conhece afundo o que tem naquela tecnologia;

Ex: Arquiteto Elastic (Kibana, Elastic Search, ...), Arquiteto Java, SQL Server, SAP

<br />

**Arquitetura Corporativa**

Políticas e regras que impactam estrategicamente a organização como um todo, 

Em uma empresa que tem milhares de funcionários o número de tecnologias que podem ser utilizadas podem chegar a N, esse arquiteto traz uma governança sólida em relação a infra/tecnologia que vai ser utilizada com uma avaliação de custos que fazem sentido para a empresa crescer.

Avaliação de licenças;

Avaliação de possível novas tecnologias;

Padronização de tecnologias ;

Planejamento de grandes implantações (SAP, Salesforce,...)

Sistemas core, migrações (Monolítico, Micro-serviços, ...)

<br />

**Arquitetura de soluções**

Fica entre a área de negócios e software, transforma os requisitos de negócios em soluções de software;

Desenhos arquiteturais da solução de um software para reproduzir como ele irá funcionar;

Diagrama C4, UML, BPMN;

Analisa os impactos comerciais em relação a uma escolha de tecnologia, analisa o contexto da empresa e da equipe para poder tomar essa decisão (ex: se a empresa está utilizando AWS faz sentido mudar para a Google só porque é a tecnologia que sua equipe sabe? Tem vantagem financeira nisso?, base de dados Oracle, faz sentido mudar para a SQL, Postgres,...?);

Pensamento a curto, médio, longo prazo;

Pode participar do processo comercial de pré-venda e venda, geralmente acompanha o cliente para entender melhor o negócio;

Analisa os impactos dos custos para o negócio, quanto custa implementar esse CRM? traz previsibilidade

Visão de alto nível (macro);

<br />

**Arquitetura de software**

Disciplina da engenharia de software, diretamente ligada ao processo de desenvolvimento de software;

Afeta diretamente na estrutura organizacional da empresa;

Formação dos times, estrutura dos componentes do software;

Como que eu consigo desenvolver esse software em componentes? Como que esses components conseguem atender os objetivos de negócios da melhor forma? todos negócio tem restrições, então eu tenho que adequar meus componentes com essas restrições (restrições financeiras, de equipe, tecnológicas,...).

É a organização fundamental de um sistema e seus componentes, suas relações, seu ambiente, bem como os princípios que guiam seu design e evolução.

Um software tem que ser construído pensando a longo prazo.

O papel do arquiteto de software é conseguir fazer com que o software retorne um valor para a empresa.

Visão micro (design, patterns, testes, implementações, clean arquiteture, code reviews, requisitos,....)

<br />

### Papel do Arquiteto de Software

- Transformar requisitos de negócio em padrões arquiteturais;
- Orquestrar pessoas desenvolvedores e experts de domínio;
- Entender de forma profunda conceitos e modelos arquiteturais;
    
    É muito comum a gente querer resolver um problema novo da mesma forma que resolvíamos os passados, ex: se sempre utilizou padrão monolítico é bem provável que o próximo desafio também vai ser uma aplicação monolítica.
    
    Quanto mais o arquiteto de software entenda de modelos arquiteturais maior vai ser seu leque de possibilidades para entender e resolver o desafio da melhor forma possível.
    
- Auxilia na tomada de decisão nos momentos de crise;
- Reforça boas práticas de desenvolvimento

<br />


### Por que aprender arquitetura de software ?

- Poder navegar da visão macro para a visão micro de um ou mais softwares;
- Entender quais são as diversas opções que temos para desenvolver a mesma coisa e escolher a melhor solução para determinado context;
- Pensar a longo prazo no projeto e sua sustentabilidade; (Prazo, Pessoas);
- Tomar decisões de forma mais fria e calculada evitando assim ser influenciado(a) por “Hypes” de mercado;
- Mergulho em padrões de projeto e desenvolvimento e suas boas práticas;
- Ter mais clareza do impacto que o software possui na organização como um todo;
- Tomar decisões com mais confiança;

<br />


### Sustentabilidade

- Desenvolver software é caro;
- Software resolve uma “dor”;
- Software precisa se pagar ao longo do tempo;
    
    A empresa deve lucrar mais por causa daquele software;
    
    O software junto com a empresa é um organismo, conforme essa evolução for acontecendo esse software tem que conseguir se manter de uma forma que o custo seja menor do que o resultado que ta trazendo para a empresa;
    
- Pensamento a longo prazo;
    
    É muito comum um software chegar a um ponto em que os devs estão desmotivados a trabalhar e querer refazer tudo do 0, o problema é que muitas vezes o software nem se pagou e vai ter que recomeçar de novo, dessa forma o software nunca vai conseguir atingir o breakeven, ponto de equilibrio entre o custo vs o que ele gera.
    
- Acompanhar a evolução do negócio;
    
    Ex: Imagina se o Nubank passar por um processo de refatoração e os clientes terem que esperar resolver os bugs para poderem utilizar o produto novamente, isso é inviável para o negócio, o software tem que ser construído com pensamento de longo prazo e sempre acompanhando a evolução do negócio.
    
- Quanto mais tempo o software ficar no ar, mais retorno gera;
- A solução precisa ser arquitetada;

<br />


### Pilares da arquitetura de software

- Estruturação
    - Fácil evolução, componentização para atender os objetivos de negócio;
- Componentização;
- Relacionamento entre sistemas; (Comunicação externa, serviços de terceiros, redes)
- Governança; (Padronização, Regras, Documentação, Protocolos, ...)
    
    Um software tem que ser independente de desenvolvedor, se uma pessoa sair deve ser fácil de outra assumir aquele cargo e continuar o projeto da maneira que estava. 
    
<br />


### Requisitos Arquiteturais

- Performance
    
    Ex: Aguentar 500 requisições por segundo, Resiliencia, ....
    
- Armazenamento de dados
    
    Ex: data centers no Brazil, Europa,...?
    
- Escalabilidade
    
    Horizontalmente, verticalmente, load balancer, ...?-
    
- Segurança
    
    SSL, Rate Limiter, Mutual TLS,...
    
- Legal
    
    Cumprir legislação de cada país (LGPD, Termos de uso, Quanto tempo os dados vão estar retidos, ...);
    
- Marketing
    
    Trackear de onde vem cada requisição, ...
    

---

## Características arquiteturais

### Operacionais

- Disponibilidade;
    
    Vai ficar no ar 24/7? Qual o nível de disponibiliade que eu quero no meu sistema? Deve estar diponível em outros países?
    
- Recuperação de desastres;
    
    Como que vou fazer para recuperar quando meu sistema estiver fora do ar? O que fazer se uma região da AWS cair? Precisa de multi cloud? 
    
    Deve existir processos para esses casos;
    
- Performance;
    
    O quanto de performance eu quero nesse sistema? 5000 requisições por segundo? Vai afetar na escolha do banco de dados, replicas, ...
    
- Recuperação (backup);
    
    Testar o backup a cada tanto tempo para ter certeza de que está funcionando.
    
- Confiabilidade e segurança;
    
    Impedir ataque de brute force, políticas de senha, captcha, ...
    
- Robustes;
    
    Consegue escalar? Consegue mudar de região caso uma caia? Tem quantidade de IP necessário, CIDR?
    
- Escalabilidade;

<br />

### Estruturais

Características do meu software para que ele funcione de forma flexível;

- Configurável
    
    Utilizar variáveis de ambiente, Abstrações, Não deve existir mudança no código fonte para fazer deploy em ambientes diferentes (dev, stage, prod)
    
- Extensibilidade
    
    Ela deve crescer de forma que as coisas possam ser plugadas nelas, ex: Gateway de Pagamento, a mudança de um gateway x para y deve ser simples, trabalhar com interfaces, abstrações.
    A aplicação não deve depender de vendors (banco de dados, gateways, modulos,...)
    
- Fácil instalação
    
    Padronização do ambiente, Infrastructure as a Code, docker compose para desenvolvimento;
    
- Reutilização de componentes
    
    Acoplar bibliotecas para que todos os serviços possam utilizar, ex: pacotes npm
    
- Internacionalização
    
    Ex: Gateway de pagamento muda? Como vai ser a conversão ? Parcelamanento,...
    
- Fácil manutenção
    
    Tornar o software simples, SOLID, entender as camadas do sistema; Correção de bugs, Adicionar novas features deve se tornar fácil.
    
- Fácil suporte (logs, debugging)
    
    Padrão na geração de logs, observabilidade, ...
    

<br />

### Cross-Cutting

- Acessibilidade
    
    Está fácil outras pessoas acessarem o site? pessoas com deficiencia? utilizar labels adequados, imagens leves,...
    
- Processo de retenção e recuperação de dados (quanto tempo os dados serão mantidos)
    
    Storage é caro, os dados que você tem hoje realmente precisa existir por 7, 30, 60 dias ?
    
    Os dados antigos podem ser mantidos em locais diferentes depois de um certo tempo para que o banco se torne mais barato.
    
- Autenticação e Autorização
    
    Em arquitetura distribuida, como que vai funcionar? utilizar o Key cloack? Api Gateway?
    
- Legal
    
    Quanto tempo os dados vão ser mantidos? encryptografados ?
    
- Privacidade
    
    LGPD, como que consegue minizar problemas em relação aos dados dos usuário vazarem?
    Evitar desenvolvedores ter acesso ao banco de dados de produção
    separar informações sensíveis em banco de dados separados ? ter um banco com dados fake para desenvolvimento ?
    
- Segurança
    
    Web Firewall, Trabalhar com mecanismo que consigam identificar robos; ....
    
- Usabilidade
    
    Como que está organizada a API? Tem documentação ? Tem um Readme ? Quem é o meu cliente?