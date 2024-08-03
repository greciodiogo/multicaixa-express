# Objetivo: multicaixa-express-server
Multicaixa Express, aplicativo de pagamentos 

O Multicaixa Express é um aplicativo de pagamentos simplificado. Nela é possível depositar e realizar transferências de dinheiro entre utilizadores. Os utilizadores podem realizar transferências entre eles por intermédio do IBAN ou pelo número de telemovel

# Requisitos
A seguir estão algumas regras de negócio que são importantes para o funcionamento do Muticaixa Express:

Usuários podem enviar dinheiro (efetuar transferência) para lojistas e entre usuários;

Validar se o usuário tem saldo antes da transferência;

Antes de finalizar a transferência, deve-se consultar um serviço autorizador externo, use este mock https://util.devi.tools/api/v2/authorize para simular o serviço utilizando o verbo GET;

Cadastro de setores (telecomunicações, serviços públicos, pagamentos por referência)

Transferência entre contas 
	por IBAN (iban, valor)
	transferência express (numero, valor, nome ordenante, mensagem(opcional))
	salvar dados como favoritos
 
Funcionalidade de Levantamentos sem cartão (montante e código secreto)

Funcionalidade de pagamentos 
	- pagamentos por referência (entidade, referência, valor)
	- pagamentos por estado (referência)
	- pagamentos outros pagamentos (setor )

	carregamentos (entidade, produto, n-telemovel, valor)

	Actividades (listagem de actividades no aplicativo (created_at, categoria, total29) (data-hora, montante, estado, transação, entidade, referencia)
	deve mandar por email (meter um email disponivel) guardar ou partilhar
)

	Gestão de cartões (limite diário, Bloquear cartão, remover cartão, editar nome cartão)

	listagem de saldo da conta, autorizado e contabilístico
	movimentos (data,descricao (transfer, transfer interb), (+,-)montante)
	listagem de IBAN


Fluxo --> carregamento, resumo carregamento, serviço autorizador

A operação de transferência deve ser uma transação (ou seja, revertida em qualquer caso de inconsistência) e o dinheiro deve voltar para a carteira do usuário que envia;

No recebimento de pagamento, o utilizador precisa receber notificação (envio de email, sms) enviada por um serviço de terceiro e eventualmente este serviço pode estar indisponível/instável. Use este mock https://util.devi.tools/api/v1/notify)) para simular o envio da notificação utilizando o verbo POST;

Este serviço deve ser RESTFul.

Tente ser o mais aderente possível ao que foi pedido, mas não se preocupe se não conseguir atender a todos os requisitos. Durante a entrevista vamos conversar sobre o que você conseguiu fazer e o que não conseguiu.

Avaliação
Apresente sua solução utilizando o framework que você desejar, justificando a escolha. Atente-se a cumprir a maioria dos requisitos, pois você pode cumprir-los parcialmente e durante a avaliação vamos bater um papo a respeito do que faltou.

# O que será avaliado ❤️
Habilidades básicas de criação de projetos Fullstack:

Conhecimentos sobre REST
Uso do Git
Uso do Docker
Serviço de Email
Capacidade analítica
Apresentação de código limpo e organizado
Conhecimentos intermediários de construção de projetos manuteníveis:

Aplicação e conhecimentos de SOLID
Identificação e aplicação de Design Patterns
Noções de funcionamento e uso de Cache
Conhecimentos sobre conceitos de containers (Docker, Podman etc)
Documentação e descrição de funcionalidades e manuseio do projeto
Implementação e conhecimentos sobre testes de unidade e integração
Identificar e propor melhorias
Boas noções de bancos de dados relacionais
Aptidões para criar e manter aplicações de alta qualidade:

# Aplicação de conhecimentos de observabilidade
Utlização de CI para rodar testes e análises estáticas

Conhecimentos sobre bancos de dados não-relacionais

Aplicação de arquiteturas (CQRS, Event-sourcing, Microsserviços, Monolito modular)

Uso e implementação de mensageria

Noções de escalabilidade

Boas habilidades na aplicação do conhecimento do negócio no software

Implementação margeada por ferramentas de qualidade (análise estática)

# O que será um Diferencial
Uso de Docker

Uma cobertura de testes consistente

Uso de Design Patterns

Documentação

Proposta de melhoria na arquitetura

Ser consistente e saber argumentar suas escolhas

Apresentar soluções que domina

Modelagem de Dados

Manutenibilidade do Código

Tratamento de erros

Cuidado com itens de segurança

Arquitetura (estruturar o pensamento antes de escrever)

Carinho em desacoplar componentes (outras camadas, service, repository)
