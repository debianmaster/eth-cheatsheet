## docker.io
```sh
apt install docker.io
```

## Run ETH node
```sh
docker run -d --name ethereum-node -v /ethdata:/root  \
-p 8545:8545 -p 30303:30303  \
ethereum/client-go --fast --cache=512 --rpc --rpcaddr "0.0.0.0" --rpcapi "personal,eth,web3"
```

## API calls
```sh
curl --request POST     --header 'Content-type: application/json'     --data '{"jsonrpc":"2.0","method":"personal_newAccount","params":["pass"],"id":74}'     http://localhost:8545
```

```sh
curl -H "Content-Type: application/json" -X POST -d '{"method":"eth_accounts","id":1}' 127.0.0.1:8545
```
