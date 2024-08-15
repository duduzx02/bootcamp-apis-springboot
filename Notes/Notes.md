## Padrões Essenciais de REST em APIs

Este artigo aborda os padrões essenciais de REST (Representational State Transfer) que devem ser seguidos ao criar APIs.
A adesão a esses padrões garante APIs bem estruturadas, fáceis de entender e consumíveis.

### Nomemclatura de APIs

Substantivos no plural: Os URLs de API devem usar substantivos no plural, como 'usuários' em vez de 'usuário'.
Anotações de verbos: Os URLs de API não devem conter anotações de verbos, como 'obter' ou 'excluir'.

### Hierarquia de Recursos

Os recursos devem ser organizados em uma hierarquia lógica.
Por exemplo, pedidos devem estar aninhados sob clientes.

### HTTP Status code

Os códigos de status HTTP devem ser usados para transmitir o resultado de uma solicitação.
100-199: Informações
200-299: Sucesso
300-399: Redirecionamento
400-499: Erro do cliente
500-599: Erro do servidor

### Verbos HTTP

GET: Obter dados
POST: Criar novos dados
PUT: Atualizar dados existentes
DELETE: Excluir dados

### Idempotência

POST: Não idempotente (cria um novo recurso)
GET, PUT, DELETE: Idempotentes (podem ser executados várias vezes sem efeitos colaterais)

### Controle de URI

GET: Controle de URI do cliente (especifica o recurso para recuperar)
POST: Controle de URI do servidor (especifica o recurso a ser criado)

