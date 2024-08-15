## Padrões Essenciais de REST em APIs

- Este artigo aborda os padrões essenciais de REST (Representational State Transfer) que devem ser seguidos ao criar
  APIs.
- A adesão a esses padrões garante APIs bem estruturadas, fáceis de entender e consumíveis.

### Nomemclatura de APIs

- Substantivos no plural: Os URLs de API devem usar substantivos no plural, como 'usuários' em vez de 'usuário'.
- Anotações de verbos: Os URLs de API não devem conter anotações de verbos, como 'obter' ou 'excluir'.

### Hierarquia de Recursos

- Os recursos devem ser organizados em uma hierarquia lógica.
- Por exemplo, pedidos devem estar aninhados sob clientes.

### HTTP Status code

- Os códigos de status HTTP devem ser usados para transmitir o resultado de uma solicitação.
-
    - 100-199: Informações
-
    - 200-299: Sucesso
-
    - 300-399: Redirecionamento
-
    - 400-499: Erro do cliente
-
    - 500-599: Erro do servidor

### Verbos HTTP

- GET: Obter dados
- POST: Criar novos dados
- PUT: Atualizar dados existentes
- DELETE: Excluir dados

### Idempotência

- POST: Não idempotente (cria um novo recurso)
- GET, PUT, DELETE: Idempotentes (podem ser executados várias vezes sem efeitos colaterais)

### Controle de URI

- GET: Controle de URI do cliente (especifica o recurso para recuperar)
- POST: Controle de URI do servidor (especifica o recurso a ser criado)

## Documentação API: OpenAPI (Swegger)

### Swagger

- Swagger é uma ferramenta valiosa para documentar APIs REST.
- Ele gera documentação que descreve os recursos, métodos e parâmetros da API.

### Benefícios de seguir os padrões REST:

- APIs estruturadas e fáceis de entender
- Consistência e interoperabilidade aprimoradas
- Documentação e manutenção simplificadas
- Menos erros e retrabalhos

## Arquitetura de Log: Boas Práticas e Impactos nos Negócios

### Introdução

- O gerenciamento de logs é um aspecto crucial para o desenvolvimento de software, pois fornece insights valiosos sobre
  o comportamento e o desempenho das aplicações. Neste artigo, exploraremos as boas práticas de arquitetura de log, seus
  benefícios e as consequências financeiras de negligenciar o gerenciamento de logs.

### Severidades de Log

- Um aspecto fundamental da arquitetura de log é a utilização das severidades corretas, que são:
    - Erro: Indica falhas graves que impedem o funcionamento da aplicação.
    - Aviso: Indica problemas significativos que podem afetar a usabilidade ou o desempenho da aplicação.
    - Informação: Fornece detalhes sobre o funcionamento normal da aplicação.
    - Depuração: Contém informações detalhadas para fins de depuração, não destinadas à produção.

### Níveis de Log Recomendados

- Para ambientes de produção, recomenda-se desativar os níveis de log 'Depuração' e 'Informação', pois eles podem gerar
  grandes volumes de dados que podem sobrecarregar os sistemas e incorrer em custos adicionais. Em vez disso, use os
  níveis 'Erro' e 'Aviso'.

### Impactos Financeiros da Negligenciência do Log

- Negligenciar o gerenciamento de logs pode resultar em perdas financeiras significativas. Por exemplo, o uso indevido
  do nível 'Depuração' pode gerar volumes excessivos de dados de log, levando a:
    - Custos de armazenamento e processamento: Grandes volumes de logs requerem mais espaço de armazenamento, resultando
      em taxas mais altas.
    - Custos de replicação: Os logs são frequentemente replicados para fins de durabilidade e recuperação de desastres,
      o que pode aumentar ainda mais os custos.
    - Custos de consulta: A consulta de grandes conjuntos de dados de log pode ser complexa e dispendiosa.

### Boas Práticas de Arquitetura de Log

- Para minimizar os impactos financeiros e maximizar a eficácia do gerenciamento de logs, siga essas boas práticas:
    - Use as severidades de log corretas para evitar dados de log desnecessários.
    - Minimize a quantidade de logs de informação e depuração gerados.
    - Use variáveis de ambiente para definir os níveis de log, permitindo ajustes fáceis entre os ambientes.
    - Use rotatividade de logs para gerenciar o crescimento do arquivo de log e evitar que ele fique muito grande.
    - Implemente monitoramento de log para alertar sobre erros e avisos importantes.
    - Considere o uso de ferramentas de observabilidade para fornecer insights adicionais sobre o comportamento da
      aplicação.

## Arquitetura de Log Corporativa

- Em grandes organizações, é comum usar um gerenciamento de log corporativo, que inclui:
    - API Gateway: Recebe requisições de clientes e as encaminha para o backend.
    - Gerenciamento de API: Fornece serviços de segurança, cache e limitação de taxa para as APIS.
    - Identity Provider: Verifica a identidade dos usuários e emite tokens de acesso.

### Conclusão

- O gerenciamento de logs é crucial para garantir o funcionamento confiável e eficiente das aplicações. Ao seguir as
  boas práticas de arquitetura de log, as organizações podem minimizar os impactos financeiros da negligência de log e
  obter insights valiosos para melhorar o desempenho e a segurança da aplicação.

