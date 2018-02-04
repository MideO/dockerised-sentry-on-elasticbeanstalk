# dockerised-sentry-on-elasticbeanstalk
[Sentry](https://sentry.io/) currently deployed [here](http://sentry.fus4jjjt8w.eu-west-2.elasticbeanstalk.com/sentry/) 

Dockerised Sentry onpremise with AWS elasticbeanstalk deployment configured and circleCi continuous deployment

#### Sentry Credentials:

 `admin: admin@localhost`   
 `password: password`  
 `SENTRY_SECRET_KEY: changeme`


#### Docker MultiContainer Setup:
 * nginx on port 80
 * sentry web
 * sentry worker x 3 
 * cron
 * redis
 * postgres
 * memcached
 * smtp

#### Beanstalk Setup:
   * DefaultPlatform: Multi-container Docker running on 64bit Amazon Linux/2.8.4
   * InstanceProrilE: t2.large
   
#### Create beanstalk environment
`./bin/create`

#### Deployment to beanstalk
`./bin/deploy`

#### Run locally:
`docker-compose up`  
`Access your instance at localhost:9000!`