# Bit.Country
Some information about the project
Installed node via Docker: 6 vCPU, 8 GB RAM, 80 GB SSD.
# sudo apt update && sudo apt upgrade -y
# sudo apt install docker.io
# sudo systemctl enable docker
# docker --version
# docker pull bitcountry/bitcountry-node:5f860f4
# mkdir -p /tewaiDb/bitcountry-node
# chown -R 1000 /tewaiDb/bitcountry-node
# docker create --name tewaiDb --network=host -v /tewaiDb/bitcountry-node:/bitcountry-db bitcountry/bitcountry-node:5f860f4 -d /bitcountry-db --name 'VALIDATORNAME' --chain tewai --bootnodes /ip4/13.239.118.231/tcp/30344/p2p/12D3KooW9rDqyS5S5F6oGHYsmFjSdZdX6HAbTD88rPfxYfoXJdNU --pruning archive --telemetry-url 'wss://telemetry.polkadot.io/submit/ 0'
# docker start tewaiDb
Logs: docker logs -f tewaiDb
Keys: curl -H "Content-Type: application/json" -d '{"id":1, "jsonrpc":"2.0", "method": "author_rotateKeys", "params":[]}' http://localhost:9933
