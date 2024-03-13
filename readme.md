# PicPay technical challenge (back-end)


## About the application environment:


-   Choose any framework you feel **comfortable** working with. This test **doesn't make** any preferences, so decide on the one you'll be most confident in presenting and talking to us in the interview ;)

-   You can even not choose any framework. In this case, we recommend implementing the service via script to reduce the overhead of creating a web server.

-   Still, if you opt for a framework, try to avoid using too many magical methods or ready-made shortcuts. We know that these facilites increase day-to-day productivity, but here we want to see **your* code and your way of solving problems.

-   We value a good container structure created by you.

## Objective: Simplified PicPay

We have 2 types of users, ordinary users and retailers, both have wallets with money and make transfers between them. Let's pay attention **only** to the transfer flow between two users.


Requirements:

-   For both types of user, we need the Full Name, CPF or CNPJ, Email and Password. CPF/CNPJ and emails must be unique in the system. Therefore, your system must only allow one registration with the same CPF or email address.

-   Users can send money (transfer) to merchants and between users.

-   Validate whether the user has a balance before the transfer.

-   Before completing the transfer, you must consult an external authorizing service, use this mock to simulate (https://run.mocky.io/v3/5794d450-d2e2-4412-8131-73d0293ac1cc).

-   The transfer operation must be a transation (i.e. reversed in any case of inconsistency) and the money must return to the sending user's wallet.

-   Upon receipt of payment, the user or retailer needs to receive  notification (email, SMS) sent by a third party serviec and this service may eventually be unavailable/unstable. Use this mock to simulate the submission (https://run.mocky.io/v3/54dc2cf1-3add-45b5-b5a9-6bf7e7f1f4a6).

-   This service must be RESTFul.

### Payload

Make a **proposal** :heart: payload, if you prefer, we have an example here:

POST /transaction

```json
{
    "value": 100.0,
    "payer": 4,
    "payee": 15
}
```

# Assessment
Present your solution using the framework you want, justifying your choice.
Pay attencion to fulfilling most of the requirements, as you can partially  fulfill them and during the assessment we will chat about what was missing.

We will have 2 parts of the evaluation:

Objective correction will be carried out using an automated correction script. You **can** run it on your local machine or use another tool:
 
```
docker run -it --rm -v $(pwd):/project -w /project jakzal/phpqa phpmd app text cleancode,codesize,controversial,design,naming,unusedcode
```

Qualitative correction will be made during the interview and will take into account the following criteria:


## What will be evaluated and we value :heart:

-   Documentation

-   If it's for a senior position, focus a lot on **architectural design**

-   Clean and organized code (nomenclature, etc.)

-   Knowledge of patterns (PSRs, design patterns, SOLID)

-   Be consistent and know how to argue your choices

-   Present solutions you master

-   Data Modeling

-   Code maintainability

-   Error handling

-   Be careful with security items

-   Architecture (structure your thoughts before writing)

-   Care about decoupling components (other layers, service, repository)

According to the criteria above, we will evaluate your test to advance to the technical interview.
If you have not acceptably achieved what we are proposing above, we will not proceed with the process.

## What will NOT be evaluated :warning:

-   User and retailer registration flow

-   Frontend (we will only evaluate the (Restful API)[https://www.devmedia.com.br/rest-tutorial/28912])

-   Authentication

## What will be a Differentiator

-   Use of Docker

-   [Integration testing](https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)

-   [Unit testing] (https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing)

-   Use of Design Patterns

-   Documentation

-   Proposal for improvement in architecture

## Useful materials

-   https://picpay.com/site/sobre-nos

-   https://hub.packtpub.com/why-we-need-design-patterns/

-   https://refactoring.guru/

-   http://br.phptherightway.com/

-   https://www.php-fig.org/psr/psr-12/

-   https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing

-   https://github.com/exakat/php-static-analysis-tools

-   https://martinfowler.com/articles/microservices.htm

-   https://docs.guzzlephp.org/en/stable/request-options.html

-   https://www.devmedia.com.br/rest-tutorial/28912
