# RabbitMQ
# RMQ
We used RabbitMQ management plugin website (https://www.rabbitmq.com/management.htmltutorial) to set up communication layer between host. First we enabled rabbitMQ management on our ubuntu. For that we used rabbitmq-plugins enable rabbitmq_management command. Management UI access by using localhost:15672. 

1.	We login by default user in RabbitMQ login.
2.	We create another user and give all permission.
3.	Created vhost and gave set permission.
4.	Created Exchanges and Queues for testing

We used testServer for DB connection and apiSever for API connection. We added this information into our testRabbitMQ.ini file. We used user, password, exchange, queue and vhost which and everything else kept same.

[testServer]
BROKER_PORT = 5672
USER = test
PASSWORD = test
VHOST = IT490
EXCHANGE = test
QUEUE = test
EXCHANGE_TYPE = topic
;AUTO_DELETE = ???

 We created another vhost, exchange and queue for apiServer,but everything else kept same. 

Connection problems: 
Whenever we had connection problems like waiting for localhost, socket error, AMQP connection error. Our initial step was to check all physical connection with router and our devices.
Second, we reboot our Ubuntu and last thing was to restart apache by using command  - sudo service apache restart. 

For the second part, we used three VM’s for RabbitMQ ,too. We kept everything same for RabbitMQ, did not change anything. We reserved IP addresses by using DHCP, so it won’t change automatically.

