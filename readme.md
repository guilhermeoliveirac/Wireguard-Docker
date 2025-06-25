
## Requirements

1) Host Linux com kernel compatível com WireGuard (5.6+ ou backport)

2) WireGuard instalado no host (
 ```sh   
apt install wireguard no Debian/Ubuntu).
```
3) [Docker](https://docs.docker.com/engine/install/) e [Docker Compose](https://docs.docker.com/compose/install/linux/#install-the-plugin-manually) instalados.

4) Para usar o a senha e preciso rodar esse comando no terminal para gerar a chave Hash:
```sh
docker run ghcr.io/wg-easy/wg-easy:14 node -e 'const bcrypt = require("bcryptjs"); const hash = bcrypt.hashSync("YOUR_PASSWORD", 10); console.log(hash.replace(/\$/g, "$$$$"));'
```