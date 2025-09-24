# Lab 2, ngab0016, CST8915

## Youtube Link(Unlisted):
- https://youtu.be/phUvw7KKMcY

## Reflection Questions
1. What changes did you make to the order-service and product-service to comply with the configurations and backing services factors of the 12-Factor App methodology?
-  I updated both of the services to use environment variables for their configuration variables (i.e., ports, database URLs, and API endpoints) instead of hardcoding so that these services could easily be configured for each of the their prospective environments (development, testing, production) of the app without the source code being modified which allows communication with external services like databases or message queues as replaceable resources.
2. Why is it important to use environment variables instead of hard-coding configurations in your application?
-  Storing environment variables keeps sensitive information (such as passwords, API keys, or connection strings) out of the codebase, and the codebase becomes more secure and flexible. It also creates portable deployments because the same code runs across different environments with a simple tweak of the environment settings and no code-modifying or redeployments.
3. Why is it important to have separate repositories for each microservice? How does this help maintain independence and scalability of each service?
-  Individual repositories provide individual lifecycles of each of the microservices so that teams can build, test, and deploy independently. It avoids unintentional breaking of one service due to changes made in another one, simplifies the process of scaling as each of the services can be deployed separately and enables real modularity of the system. It also helps with simpler CI/CD pipelines as each service's needs are addressed individually.

## Links to repositories
- Order-service repo link: https://github.com/ngab0016/order-service
- Product-service repo link: https://github.com/ngab0016/Product-service
- Store-front repo link: https://github.com/ngab0016/store-front

## Notes from things I noticed

You have to wait for the port to connect with your terminal, especially for product-services because it wouldn't fetch from store front unless the port is open in the terminal.