# Unichain-Node: How To Run

![image](https://github.com/user-attachments/assets/7fd251b6-c4e8-4114-a8aa-63f8e406320f)


1) Update Sudo
```
sudo apt update && sudo apt upgrade -y
```


2) Install Docker
```
sudo apt install docker.io
```


3) Install Docker Compose
```
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```


4) Clone the Unichain Repository
```
git clone https://github.com/Uniswap/unichain-node
```


5) Unichain Directory
```
cd unichain-node
```


6) Open .env.sepolia file
```
nano .env.sepolia
```


7) Edit OP_NODE_L1_ETH_RPC and OP_NODE_L1_BEACON

- OP_NODE_L1_ETH_RPC to: https://ethereum-sepolia-rpc.publicnode.com

- OP_NODE_L1_BEACON to: https://ethereum-sepolia-beacon-api.publicnode.com


8) Run the Node
```
docker-compose up -d
```


9) Curl
```
curl -d '{"id":1,"jsonrpc":"2.0","method":"eth_getBlockByNumber","params":["latest",false]}' \
  -H "Content-Type: application/json" http://localhost:8545
```

Done!
