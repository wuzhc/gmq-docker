```bash
docker-compose up
```

## web管理页面
http://127.0.0.1:8080/

## 测试
```bash
# 推送消息
curl -d 'data={"body":"hello world","topic":"topic-1","delay":0}' 'http://127.0.0.1:9504/push'
# 消费消息
curl http://127.0.0.1:9504/pop?topic=topic-1 
# 确认消息
curl http://127.0.0.1:9504/ack?msgId=xxxxx&topic=topic-1
```