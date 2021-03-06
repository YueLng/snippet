# Go code for RabbitMQ tutorials


Here you can find Go code examples from [RabbitMQ tutorials](http://www.rabbitmq.com/getstarted.html).


## Requirements

To run this code you need [Go RabbitMQ client](https://github.com/streadway/amqp):

    go get github.com/streadway/amqp


## Code

Code examples are executed via `go run`:

[Tutorial one: "Hello World!"](http://www.rabbitmq.com/tutorial-one-go.html):

    go run send.go
    go run receive.go

[Tutorial two: Work Queues](http://www.rabbitmq.com/tutorial-two-go.html):

    go run new_task.go hello world
    go run worker.go

[Tutorial three: Publish/Subscribe](http://www.rabbitmq.com/tutorial-three-go.html)

    go run receive_logs.go
    go run emit_log.go hello world

[Tutorial four: Routing](http://www.rabbitmq.com/tutorial-four-go.html)

    go run receive_logs_direct.go info warn
    go run emit_log_direct.go warn "a warning"

[Tutorial five: Topics](http://www.rabbitmq.com/tutorial-five-go.html)

    go run receive_logs_topic.go "kern.*" "*.critical"
    go run emit_log_topic.go kern.critical "A critical kernel error"

[Tutorial six: RPC](http://www.rabbitmq.com/tutorial-six-go.html)

    go run rpc_server.go
    go run rpc_client.go 10

To learn more, see [Go RabbitMQ client](https://github.com/streadway/amqp).

## 应用程序的异步与解耦
## 消息缓冲
## 消息分发
## P 生产者 rabbitmq 交换机与队列 C 消费者
## 虚拟主机,交换机,队列,和绑定(交换机与队列多对多绑定)
# sudo systemctl start rabbitmq-server
# sudo invoke-rc.d rabbitmq-server restart

# 广播消息,跨集群走消息队列
# 队列消息最小化原则,如果数据量大使用数据库