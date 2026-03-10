# 10/03/26
# Wireshark Retransmissão

- A opção -sS do nmap não causa retrasmissão por justamente não atuar nessa camada de conexão(camada 5)
   - A opção -sT (Connect-sca) essa sim causa retransmissão, por justamente atuar an camada 5(confirma que recebu dados(SYN-ACK)).
      - SYN = "vamos estabelecer conexão". Nesse contexto, sendo usado para dizer:
               "Claro, vamos conversar(SYN). Recebendo seus dados(ACK)"
        
      - ACK = "confirmando que recebi seus dados"
      - -sS = "voumandar uma pacote de teste(probe) pra ver a realção do host." ele não se conecta pra fazer isso (camada 4).

- [link estudo retransmissão] -> https://github.com/tlmtiger117/Wireshark-Sniffers-de-Rede/blob/main/Retransmiss%C3%A3o.md
