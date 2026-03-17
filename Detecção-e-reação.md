# 17/03/26
# Detecção e reação

- A prática de hoje foi bem simples:
   - 1° gerar tráfego de com um scanner(Nmap)
   - 2° Observar o tráfego no wireshark(sniffer)
   - 3° reação: Criar regras de firewall para esse host em específico.
     - Nesse caso, os comandos que eu utilizei, 1° logava quem fez o scan(host específico) e depois reagia(RST do firewall).

- É algo simples, mas pra mim está sendo uma experiência no mínimo interessante(pensar como atacante,SOC e ADM de firewall).
