## Description

[Nest](https://github.com/nestjs/nest) framework TypeScript starter repository.

## Project setup

```bash
$ npm install
```

## Compile and run the project

```bash
# development
$ docker-compose up

# production mode - change target in docker-compose.yml to production intead of development
$ docker-compose up
```

## Notes

each module (ie. orders, billing, auth) need their own enviroment variables, that beeing said, use the `env-model` to add the needed variables in each apps/(service) you may have.

.env example

```
# apps/orders/.env
MONGODB_URI=mongodb://root:password123@mongodb-primary:27017/

PORT=3000

RABBIT_MQ_URI=amqp://rabbitmq:5672
RABBIT_MQ_BILLING_QUEUE=billing
RABBIT_MQ_AUTH_QUEUE=auth

# apps/billing/.env
RABBIT_MQ_URI=amqp://rabbitmq:5672
RABBIT_MQ_BILLING_QUEUE=billing
RABBIT_MQ_AUTH_QUEUE=auth

# apps/auth/.env
PORT=3001

JWT_EXPIRATION=3600
JWT_SECRET=your-secret-here-:)

MONGODB_URI=mongodb://root:password123@mongodb-primary:27017/

RABBIT_MQ_URI=amqp://rabbitmq:5672
RABBIT_MQ_AUTH_QUEUE=auth
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.

## Resources

Check out a few resources that may come in handy when working with NestJS:

- Visit the [NestJS Documentation](https://docs.nestjs.com) to learn more about the framework.
- For questions and support, please visit our [Discord channel](https://discord.gg/G7Qnnhy).
- To dive deeper and get more hands-on experience, check out our official video [courses](https://courses.nestjs.com/).
- Deploy your application to AWS with the help of [NestJS Mau](https://mau.nestjs.com) in just a few clicks.
- Visualize your application graph and interact with the NestJS application in real-time using [NestJS Devtools](https://devtools.nestjs.com).
- Need help with your project (part-time to full-time)? Check out our official [enterprise support](https://enterprise.nestjs.com).
- To stay in the loop and get updates, follow us on [X](https://x.com/nestframework) and [LinkedIn](https://linkedin.com/company/nestjs).
- Looking for a job, or have a job to offer? Check out our official [Jobs board](https://jobs.nestjs.com).

## Support

Nest is an MIT-licensed open source project. It can grow thanks to the sponsors and support by the amazing backers. If you'd like to join them, please [read more here](https://docs.nestjs.com/support).

## Stay in touch

- Author - [Kamil Myśliwiec](https://twitter.com/kammysliwiec)
- Website - [https://nestjs.com](https://nestjs.com/)
- Twitter - [@nestframework](https://twitter.com/nestframework)

## License

Nest is [MIT licensed](https://github.com/nestjs/nest/blob/master/LICENSE).
