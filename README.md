## ⛅ Cloud9
My home server running Kubernetes + ArgoCD on a GMKTec K16. 

Hosts the following:

### ![Vanilla Server Logo](https://raw.githubusercontent.com/TomasBorsje/Cloud9/refs/heads/main/assets/vanilla-minecraft-server-icon.png) Vanilla Minecraft - `vanilla.borsje.co.nz`
Fabric Minecraft with Discord integration, Voxyserver, and some other quality of life tweaks. Must be whitelisted to join.

### ![Vanilla Server Logo](https://raw.githubusercontent.com/TomasBorsje/Cloud9/refs/heads/main/assets/modded-minecraft-server-icon.png) All The Mods 10 - `atm10.borsje.co.nz`
All The Mods 10 Minecraft server. Must be whitelisted to join.

### Terraria - `terraria.borsje.co.nz`
Vanilla Terraria server, password protected.


## Cheatsheat
Useful commands for administrating the server.

### Creating a Sealed Secret
```bash
kubectl create secret generic <name> --dry-run=client -o yaml --from-file=<path to folder>
kubeseal --format yaml < unlocked-secret.yaml > sealed-secret.yaml
```
Then commit the secret for ArgoCD to deploy it.
