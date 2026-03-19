# 19/03/26
# Firewall X Nmap(-sS)

- Ferramentas:
   - Nmap(Network-Mapper)
   - Wireshark(scniffer/capturador de pacotes)
   - iptables(programa que prioriza regras criadas pelo user com base no Netfilter do kernel).
     

- Testei algumas regras de firewall consegui fazer uma combinação interessante, onde eu analisava os pacotes TCP + Flags.
  Com isso, consegui Detectar um scan -sS(half-open/Entre-aberto do Nmap). Essa é a Flag mais utilizada por quem usa essa tool,
  pois ela gera menos tráfego(mas isso não impede sua detecção por sniffers ou firewalls).
  

- Comando utilizado:
   - sudo iptables -A INPUT -p tcp --tcp-flags SYN,RST SYN,RST -m recent --set -j LOG --log-prefix "(AVISO)"
     
   - Eu diria que a parte mais importante e a "--tcp-flags", pois é lá que o kernel decide o tipo de pacote a ser
     analisado + analisar pacotes expecíficos juntos (nesse caso, foi o SYN,RST SYN,RST) que basicamente diz:
     "analisar os pacotes SYN e RST separadamente, depois analisar o SYN e o RST juntos" (isso cria a nossa regra).


- Repositórios mencionados:

   - Nmap: [https://github.com/tlmtiger117/Nmap-Network-Mapper-]
   - Wireshark: [https://github.com/tlmtiger117/Wireshark-Sniffers-de-Rede]
   - iptables(firewall): [https://github.com/tlmtiger117/Firewall/blob/main/Flags_Firewall.md]




