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
    
<br />

---
<br />

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
    
<br />

---
<br />

## Arquitetar Software de Qualidade
<br />

### **Performance**

É o desempenho que um software possui para completar um determinado workload.

Como que eu consigo verificar o desempenho que ele ta tendo para desempanhar aquela ação?

Para medir performance precisamos de dados;

As unidades de medida para avaliarmos a performance de um software são:

- **Latência** ou “**response time**” ⇒ tempo de requisição e processamento do workload;
- **Throughput** ⇒ Quanto de requisição consegue aguentar;

Ter um software performático é diferente de ter um software escalável

Objetivo:

- Diminuir latência, normalmente medida em miliseconds; É afetada pelo tempo de processamento da aplicação, rede e chamadas externas
- Aumentar o throughput, permitir que o software consiga aguentar mais requisições; está diretamente ligado a latência

**Principais razões de performance baixa:**

- Processamento ineficiente;
    
    Ex: Algoritimos, forma que a aplicação está lidando com os dados, queries mal feitas, etc.
    
- Recurso computacionais limitados;
    
    CPU, RAM, Memória,...
    
- Trabalhar de forma bloqueante;
    
    Todas as vezes que você faz uma requisição e se essa requisição bloquear a aplicação para ficar lidando especificamente com aquela requisição a aplicação vai diminuir o throughput, pois não vai conseguir lidar com milhares requisições de forma paralela.
    
    Separar cada requisição em uma thread.
    
- Acesso serial a recursos;
    
    Cada vez que vai acessar uma API espera terminar e chama o próximo, um após o outro, isso diminui o troughput.
    

**Principais formas de aumentar a eficiência:**

- Escala da capacidade computacional (CPU, Disco, Memória, Rede);
- Lógica por trás do software (Algoritmos, queries, overhead de framework);
- Concorrência e paralelismo; Lidar com diversos processos ao mesmo tempo;
- Bancos de dados (tipos de bancos, schema);
- Caching;

**Capacidade Computacional: Escala Vertical vs Horizontal**

**Escala Vertical ⇒** Aumentar a capidade computacional da máquina, fazendo com que a aplicação consiga receber mais requisições;

**Escala Horizontal ⇒** Aumenta a quantidade de máquinas colocando um load balancer na frente para balancear as cargas;

**Concorrência e Paralelismo**

“Concorrência é sobre lidar com muitas coisas ao mesmo tempo. Paralelismo é fazer muitas coisas ao mesmo tempo.”

**Concorrência ⇒** Lida com várias coisas mas não necessáriamente são executadas ao mesmo tempo; Quando duas ou mais tarefas podem começar a ser executadas e terminar em espaços de tempo que se sobrepõem, não significando que elas precisam estar em execução necessariamente no mesmo instante.

Ou seja, você tem concorrência quando:

- Mais de uma tarefa progride ao mesmo tempo em um ambiente com múltiplos CPUs/núcleos;
- Ou no caso de um ambiente single core, duas ou mais tarefas podem não progredir no mesmo *exato momento,* mas mais de uma tarefa é processada em um mesmo *intervalo de tempo,* não esperando que uma tarefa termine por completo antes de dar início a outra.

**Paralelismo ⇒** Fazer ações de forma simultânea. Acontece quando duas ou mais tarefas são executadas, literalmente, ao mesmo tempo. Necessita, obviamente, de um processador com múltiplas cores, ou múltiplos processadores para que mais de um processo ou thread seja executado ao mesmo tempo.

Imaginando um web server com um worker:

- Trabalhando de forma serial - único processo
- Atendendo 5 requests

```docker
10ms -> 10ms -> 10ms -> 10ms -> 10ms 
------------------------------------
              50ms
```

**Forma concorrente / paralela**

- 5 threads atendendo 1 request cada

```docker
10 ms ->
10 ms ->
10 ms ->
10 ms ->
10 ms ->
--------
  10ms
```

<br />


### **Caching**

Pegar coisas que já foram processadas antes e devolver de forma mais rápida para o usuário final.

- **Cache na borda / Edge computing**
    
    O usuário não chega a bater na máquina (ec2,ecs,lambda,...) pois esse tipo de cache vai cachear os dados em uma borda que fica antes do servidor principal.
    Ex de serviços: Cloudflare, Cloudfront.
    
    Cloudfront cachea os arquivos státicos (imagens, css, js, ...)em alguma availability zone e os usuários que estão próximos a elas vão receber os dados quase de forma instântanea
    
    Tipos de edge cache: 
    
    - Dados estáticos;
    - Páginas web;
    - Funções internas;
        - Evitar reprocessamento de algorítmos pesados colocando um TTL de 30min por ex;
        - Acesso ao banco de dados (Evitar I/O desnecessários).
    - Objetos;
    
    **Problema:** a netflix tem milhões de acesso em sua aplicação web, se o datacenter está nos estados unidos os usuários de todo o mundo vão ter que percorrer de seu local até o eua para pegar esses terabites de dados para poder acessar o site, congestionando a rede da netflix e a internet no geral e gerando bastante latência para acessar um conteúdo.
    
    **Solução: Edge computing**, cachear esses dados nas regiões onde seus usuários estão localizados, evitando que os usuarios precisem trafegar por toda a internet para bater no datacenter. Vai dar melhor experiencia para o usuario (baixa latencia) e a gente vai pagar menos pois vamos ter menos requisição nos nossos servidores.
    
    - Cache realizado mais próximo ao usuário. O usuários não precisa bater nos EUA para poder pegar uma imagem
    - Evita a requisição chegar até o Cloud Provider / Infra.
    - Normalmente arquivos estáticos. (Mais barato, Mais rápido)
    - CDN - Content Delivery Network; (Malha de servidores, espalha seu conteúdo para os outros data centers), EX: CDN da akamai → Mais de 500 pontos no Brazil, espalha seus conteúdos (Vídeos) para as regiões do Brazil.
        
        Se você ta em Portugal seu vídeo deve ser carregado de um CDN de Portugal
        
        Custo:
        
        - Custo da CDN
        - Custo de distribuição: Se a AKAMAI não estiver com o vídeo/imagem no CDN dela ela mesmo vai buscar o conteúdo no servidor (ex: us-east-1), baixar e disponibilizar para você, uma vez que ela baixou ela vai fazer algo chamado de Midgress, significa que agora vai pegar esse conteúdo e vai distribuir entre os pontos estratégicos, e esse espalhamento de conteúdo consome banda e você paga por esse tráfego para espalhar pelos edges. Origin → CDN → midgress →...
    - Cloudflare workers ⇒ Plataform de edge computing
    - Vercel
    - Akamai

<br />


### Escalabilidade

Escalabilidade é a capacidade de sistemas suportarem o aumento (ou a redução) dos workloads incrementando (ou reduzindo) o custo em menor ou igual proporção.

Enquanto performance tem o foco em reduzir a latência e aumentar o throughput, a escalabilidade visa termos a possibilidade de aumentar ou diminuir o throughput adicionando ou removendo a capacidade computacional.

Escala vertical - Escala horizontal

**Escalando software - Descentralização**

As máquinas são descartáveis, então seu sistema tem que ser independente da máquina que está sendo utilizada.

- **Disco efêmero →** Tudo que você salvar em disco pode ser apagado na hora que precisar. Precisamos do poder de matar a máquina na hora que quisermos.
- **Servidor de aplicação vs Servidor de assets →** Servidor tem o código da aplicação, assets ficam em um servidor de assets (s3 bucket).
- **Cache centralizado →** O cache não fica na própria máquina, fica em um servidor especifico para cache. ex: DynamoDB.
- **Sessões centralizadas →** O software não pode armazenar estado.
- **Upload / Gravação de Arquivos →** Bucket / servidor de arquivos

Tudo pode ser destruído e criado facilmente

**Escalando banco de dados**

- Aumentando recursos computacionais; Mais disco, memória, cpu,...;
- Distribuindo responsabilidades (escrita vs leitura); Criar réplicas;
- Shards de forma horizontal; Criar várias máquinas de leituras;
- Otimização de queries e índices;
- Serverless / Bancos cloud; (Dynamo, Aurora, Fauna,...);

Utilizar um sistema de APM (Application performance monitoring) para identificar os gargalos nas queries e problemas que estão acontecendo. 

- Explain na queries → identificar o que está acontecendo nas queries
- CQRS (Command Query Responsability Segregation)
- 

**Proxy reverso**

Proxy = Procurador, uma pessoa que fala em seu nome

Redireciona usuários,;

Proxy é um serviço que routea o trafico entre o cliente e outro sistema. ele pode regular o trafico de acordo com politicas presentes, enforçar segurança e bloquear IP desconhecidos.

Proxy reverso é um servidor que fica na frente de todos os servidores, ele possue regras, e essas regras fazem com que encaminhe a sua requisição para determinado servidores que possam resolve-lá . Diferente de proxy normal, que fica do lado do cliente, o proxy reverso é feito para proteger os servidores. ele aceita a requisição do cliente e encaminha a requisição para um ou mais servidores e retorna o resultado processado. O cliente se comunica diretamente com o reverse proxy e não sabe do servidor que processou.

**Solução de Proxy Reverso:**

- Nginx
- HAProxy (HA = High Availability)
- Traefik

<br />


### Resiliência

É um conjunto de estratégias adotadas intencionalmente para a adaptação de um sistema quando uma falha ocorre.

No software, se um erro acontecer ele apenas lança uma exception ? ou ele tem uma estratégia para que mesmo que dê erro atenda a requisição do cliente, mesmo que parcialmente.

Resiliéncia é o poder de se adaptar caso algo aconteça.

Como que eu consigo cadastrar o usuário mesmo que a API dos correios não esteja funcionando para pegar o CEP ? Como que eu consigo pegar essa venda se meu serviço de pagamento não está funcionando?

A unica coisa que temos certeza é que nosso software vai falhar em algum momento, porém temos que ter resiliência para lidar com essas falhas.

Ter estratégias de resiliência nos possibilita minimizar os riscos de perda de dados e transações importantes para o negócio.

**Estratégias de resiliências**

- **Proteger e ser Protegido**
    
    É muito comum hoje uma aplicação está baseada em um ecosistema com vários outros serviços. Um sistema em uma arquitetura distribuida precisa adotar mecanismos de autopreservação para garantir ao máximo sua operação com qualidade.
    
    Um sistema não pode ser “egoísta” ao ponto de realizar mais requisições em um sistema que está falhando.
    
    **Ex:** 
    
    Sistema A mandando requisição para saber a tabela de preço para o Sistema B, mas o sistema B não responde, e o sistema A fica mandando várias requisições em seguida, eventualmente o Sistema B vai sair do ar.
    
    Então um sistema não pode ficar mandando diversas requisições para outro até cair, não adianta chutar cachorro morto.
    
    Um sistema lento no ar muitas vezes é pior do que um sistema fora do ar. (Efeito dominó).
    
    **Ex:**
    
    Sistema A chama Sistema B que chama o Sistema C, se o sistema C está lento vai atrasar a resposta do B, que consequentemente vai atrasar a resposta do A, e se vem mais requisições chegando vai acabar derrubando algum serviço e eventualmente talvez todos.
    
    Então em alguns momentos se um sistema não está aguentando requisição é melhor retornar 500 para todo mundo até se estabilizar novamente.
    
    Uma forma de proteção é identificar que você não aguenta requisição ou que o outro serviço não está mais aguentando ou demorando demais para responder.
    
- **Health check**
    
    Verificar a saúde da aplicação;
    
    “Sem sinais vitais não é possível saber a saúde de um sistema”.
    
    Importante para saber se está podendo receber requisições ou não, ...., se estiver ruim já retorna um erro 500 para as outrar aplicações saberem se está indisponível.
    
    Um sistema que não está saudável possui uma chance de se recuperar caso o tráfego pare de ser direcionado a ele temporariamente.
    
    Self healing, dar um tempo para o servidor se auto recuperar, parar de mandar requisições para ele.
    
    **Health check de qualidade,** geralmente as pessoas só colocam uma rota /health para verificar se a aplicação está saudável, porém isso não consegue medir se a aplicação está saudável de verdade, pois nas outras rotas geralmente tem processamento, consulta ao banco, formatação de dados, etc.
    
- **Rate limiting**
    
    Protege o sistema baseado no que ele foi projetado para suportar.
    
    Para saber esse limite podemos fazer teste de estress e/ou orçamento da empresa para saber quanto tráfego pode ter.
    
    **Ex:** 100 requisições por segundo, “é até que eu aguento”, retorna um erro 500 caso ultrapasse.
    
    Também podemos trabalhar com prioridade, reservar 60 requisições para um cliente importante e 40 para o resto.
    

- **Circuit breaker**
    
    Proteje o sistema fazendo com que as requisições feitas para ele sejam negadas. EX: 500
    
    Se a api estiver dando problema o circuito abre o ‘interruptor’ e não permite mais a passagem de requisições.
    
    **Circuito Fechado =** requisições chegam normalmente;
    
    **Circuito Aberto** = requisições não chegam ao sistema. Erro instantâneo ao client;
    
    **Meio Aberto** = Permite uma quantidade limitada de requisições para verificação se o sistema tem condições de voltar ao ar integralmente.
    
- **API Gateway**
    
    Centraliza o recebimento de todas as requisições da aplicação, toda as requisições passam por ela e ela aplica as regras politicas/validação para depois fazer o forward da requisição para quem vai resolver.
    
    Consegue entender as necessidades individuais de cada aplicação.
    
    Garante que requisições ‘inapropriadas’ cheguem até o sistema:
    
    Ex: usuário não autenticado.
    
    Tiramos a responsabilidade de autenticação da aplicação e passamos para o API Gateway, só de fazermos isso já reduzimos o gasto de recurso para verificar se o usuário está autenticado ou não.
    
    É como se morassemos em um condomínio e a pessoa só entra no apartamento se passar pela portaria (API Gateway) antes.
    
    Implementa políticas de Rate Limiting, Health check, etc...
    
    Ex de serviços: Kong
    
- **Service mesh**

Controla o tráfego de rede.

Ao invés de os serviços se comunicarem diretamente entre si eles batem em um proxy chamado sidecar e esse sidecar manda a requisição para o sidecar de outro sistema.

```docker
[ Sistema A ] (Sidecar) ----> (Sidecar) [Sistema B]
```

Toda comunicação de rede é efetuada via proxy, assim tudo que está passando na rede pode ser controlado.

Evita implementações de proteção pelo próprio sistema.

Você consegue analisar tudo que está acontecendo na rede, todo tráfego, e com isso consegue definir as regra de Rate Limiter, Circuit Breaker,...

mTLS → encryptografar a rede para se certificar que o Serviço A é ele mesmo e o B é ele mesmo.

- **Comunicação assíncrona**

Com menos recurso computacional consegue dar vazão a mais recurso computacional do que poderia dar.

Não precisa entregar a resposta das requisições imediatamente.

Evita perda de dados;

Não há perda de dados no envio de uma transação se o server estiver fora;

**Ex:** de forma sincrona se fizermos um pagamento e o servidor não estiver de pé vai dizer para tentar novamente mais tarde, porém, de forma assíncrona permite a gente manda a mensagem/informação para um intermediário (Redis, RabbitMQ, AWS SNS, Kafka,...) para lidar com a ação pois a outra ponta não precise da resposta naquele momento.

Servidor pode processar a transação em seu tempo quando estiver online;

- **Garantias de entrega com Retry**

Quando a gente quer resiliência na requisição precisamos ter certeza que a mensagem que estamos enviando ela está chegando no destino, agora nem sempre a mensagem pode chegar pois o outro sistema pode estar lento, fora do ar, ... e por conta disso uma das formas de ter resiliencia e minimizar esse problema é termos politicas de Retry, manda uma mensagem, se o sistema não responder manda outra, e outra,...

Porém temos um **problema**, se 10 serviços mandam uma req e o servidor não aguenta 10 requisições simultaneas, mesmo se os outros servidores tiverem policitas de retry e ficarem mandando mensagem de 2 em 2s não vai adiantar pois todos estão tentando acessar o servidor ao mesmo tempo e assim sempre vai retornar erro.

Para isso temos o **Exponential backoff - Jitter,** fazemos uma espera de forma exponencial 2s, 4s, 8s, 16s,..., para dar mais tempo ao servidor se recuperar e com o Jitter ele tem um algoritimo que vai adicionar um ruído aleatorio nas requisições para que não aconteçam de forma simultânea, ex: (2.1s, 2.5, 2.0), (4.7, 4.01, 4.12,...) para que mesmo que os serviços estejam mandando de forma simultânea o ruído vai fazer com que cheguem de forma diferente.; 

- **Garantias de entrega com Kafka**

- **Situações complexas**
    - O que acontece se o message broker cair? (Kafka, RabbitMQ, SNS,...)
    - Haverá perda de mensagens?
    - Seus sistema ficará fora do ar?
    - Como garantir resiliência em situações inusitadas?
    
    Sempre temos alguns SPF (Single point of failure).
    
    Por exemplo, se toda resiliencia que você vai se apoiar é no Apache Kafka significa que o seu SPF está no Apache Kafka.
    
    Como que conseguimos evitar isso? para que se o kafka cair o sistema não perca informações ?
    
    Isso tudo envolve gerenciamento de risco, quanto mais resiliência garantimos mais caro vai sair para a empresa.
    
    Se a AWS cair ? Vale a pena trabalhar com multi cloud ?
    
    Sempre vai ter um limite a sua resiliência, quanto mais resiliência, mais esforço e mais custo.
    
    A responsabilidade de definir qual o nível de resiliência do sistema é do CTO / CEO que define o risco que aquilo vai gerar para o negócio.