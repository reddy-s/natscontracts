# Contract artifact for all gRPC communication

## Generating classes for Java 
```bash
./gradlew generateProto
```

## Generating files for Python
```bash
for file in $(ls ./src/main/proto); do
    python3 -m grpc_tools.protoc -I./src/main/proto --python_out=.python --grpc_python_out=.python ./src/main/proto/${file};
done
```