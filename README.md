- Instructions to run 
```
docker network create -d bridge --subnet 192.168.0.0/24 --gateway 192.168.0.1 dockernet

cd zeebe
sudo docker-compose up

cd ..
cd nginx 
sudo docker-compose up 

export ZEEBE_ADDRESS=127.0.0.1:80
cd ..
cd ./bin

./zbctl deploy ../bpmn/test-workflow.bpmn  --insecure

```

- Check the deployment http://localhost:8082
- Manage gRPC services with kong https://konghq.com/blog/manage-grpc-services-kong/