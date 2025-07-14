# Subscription Platform Challenge!

Para sua sorte temos um mega desafio para você, mas não se preocupe, não é tão complexo de implementar quanto parece ;) Queremos entender como você aborda problemas complexos, sua capacidade de estruturar soluções robustas, e como implementa boas práticas de arquitetura e qualidade de código. 

Boa sorte!

## O Problema...
Temos uma plataforma SaaS e precisamos gerenciar de forma resiliente e eficiente a cobrança para nossos clientes.

## O Desafio...

Você irá desenvolver uma API para gerenciar um sistema de assinatura para uma plataforma nossa plataforma de onboarding. 

A API permitirá:
1.	Gestão de Assinaturas: Criar, atualizar e cancelar assinaturas.
2.	Gestão de Pagamentos: Registrar, listar e atualizar pagamentos associados às assinaturas.
3.	Integração com Terceiros: Realizar chamadas a uma API de pagamentos externa para processar e validar transações.
4.	Consulta de Relatórios: Fornecer endpoints para consulta de relatórios detalhados de assinaturas e pagamentos.

## Requisitos

1.	API Restful:
    - Criar uma API em Go ou Java (à sua escolha) que expõe os recursos necessários para os casos de uso descritos.
	- Implementar autenticação e autorização usando OAuth2 ou JWT.
2.	Entidades:
```json
// Subscription
{
    "id": "12345",
    "clientId": "67890",
    "plan": "PREMIUM",
    "status": "ACTIVE",
    "startDate": "2023-01-01T00:00:00Z",
    "endDate": "2024-01-01T00:00:00Z",
    "createdAt": "2023-01-01T00:00:00Z",
    "updatedAt": "2023-06-01T12:00:00Z"
}
```
```json
// Payment
{
    "id": "98765",
    "subscriptionId": "12345",
    "amount": 49.99,
    "status": "APPROVED",
    "method": "CREDIT_CARD",
    "paymentDate": "2023-07-15T10:30:00Z",
    "createdAt": "2023-07-01T08:00:00Z",
    "updatedAt": "2023-07-15T11:00:00Z"
}
```
3.	Gestão de Assinaturas e Pagamentos:
	- Permitir criação, atualização e cancelamento de assinaturas.
	- Para pagamentos, permitir a criação, listagem e atualização. Utilizar status como pendente, aprovado, recusado.
4.	Integração com API de Pagamentos Externa:
	- Implementar uma integração com uma API de pagamentos externa (pode simular um serviço externo usando um mock).
	- Utilizar esta integração para criar transações de pagamento e atualizar seu status.
5.	Cache e Desempenho:
	- Implemente cache para consultas de assinaturas e relatórios, utilizando Redis.
	- Avaliar as principais métricas de desempenho e otimizar consultas.
6.	Resiliência e Escalabilidade:
	- Use padrões de resiliência, como retry e circuit breaker, para chamadas à API de pagamentos.
	- Implementar um padrão de filas (RabbitMQ, Kafka, etc.) para processamento assíncrono de atualizações de status de pagamento.
7.	Relatórios:
	- Criar um endpoint que permita a consulta de relatórios de pagamentos e assinaturas, incluindo dados como total de assinaturas ativas, receitas por período, e assinaturas canceladas.
8.	Documentação e Testes:
	- Documentação completa dos endpoints, pode utilizar Swagger.
	- Cobertura de testes unitários (90% ou mais) e testes de integração.
	- Descreva em um README o processo de setup e uso da API, incluindo as instruções para rodar em containers Docker.

## Avaliação

Este desafio será avaliado com base nos seguintes critérios:
1.	Qualidade do Código e Boas Práticas: Limpeza, modularização, consistência e uso de boas práticas de código.
2.	Arquitertura e Design de Software: Implementação de um design escalável e com responsabilidade distribuída de forma eficaz.
3.	Resiliência e Escalabilidade: Aplicação de padrões de resiliência e escalabilidade na solução.
4.	Documentação e Testes: Cobertura de testes, documentação clara e concisa.
5.	Performance: Uso adequado de cache e práticas para otimização de desempenho.

Boa sorte e esperamos ver seu código em breve!

## Prazo
A entrega deve ser feita em até 5 dias a contar do recebimento por e-mail, com a possíbilidade de extensão do prazo por mais 12 horas mediante solicitação por e-mail antes do fim do prazo.

Suba seu projeto para um repositório Git público de sua escolha e envie o link para os endereços abaixo:

Destinatário: leonardo.brito@esphero.tech

Cópia: victor.ximenis@esphero.tech, veronica.abrahao@baseservice.io
