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

