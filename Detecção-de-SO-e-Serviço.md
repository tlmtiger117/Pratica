# 23/03/26
# Detecção de Sistema operacional e Serviços Em Lab LAN interno

- Atacante: Testador de Segurança ou invasor. Tem o objetivo de explorar a rede e alcançar algum objetivo pessoal.
  
- Tool: Nmap(Network-Mapper): Scanner de rede, utilizado para detectar Hosts,SO,portas,serviços firewalls e vulnerabilidades.

- Objetivo: detectar o SO e serviços de um host em rede LAN sem ser detectado facilmente(facilmente, não invisível)

- Flags utilizadas:

   - --packet-trace: mostra todo pacote enviado e recebido do nmap
   
   - --reason: mostra o por que o nmap determinou um comportamento do host como "x"(open,filtered,closed...)
   
   - -PR: ARP-ping, utiliza pacotes arp no método broatcast para enviar uma pergunta geral para a rede e receber uma resposta
          única do host perguntado (unicast)

   - 192.168.1.1-100: função de scanear um range expecífico de ips, ex:
     
        (começa no 1) (termina no host 100)
      - 192.168.1.1-100
        
   
   - -Pn: Sem verificação por ping. Util quando já se saba o estado do host ou quando o icmp está bloqueado por firewall

   
   - -sS: Half-open, conexão entre aberta, encerra a probe com RST("encerrando tentativa de conexão imediatamente")
   
   - -n: Sem resolução de domínio(pedir o nome de um site(ou o inverso)."ex: 'site.com' = 200.234.225.198"
 
   - --scan-delay: Define o delay entre cado porbe enviada(pacote de teste de reação).SYN,RST,IP,icmp...
   - 
   - -O: OS-detection, detecão de Sistema operacional. Scaneia várias portas específicas para determinar o possível SO do host.
         [!] Demora muito se utilizar um delay ALTO no scan. Recomendo de 3 a 5 segundos de delay por probe
     
   - -sV: Search-version: Tenta identificar a versão do serviço da porta com base em seu header:
     
      - 1° Cria um novo socket(conector), usado para estabelecer conexão com o servidor.
      - 2° Faz um pedido(Request) ao server, pedindo para se conectar a ele.
      - 3° Resebe a resposta do servidor(Call-Back),"chamada de retorno", aceita ou não.
      - 4° O Nmap manda uma probe TCP com pacote Null para testar a reação do server.
      - 4° Se o server aceitar/receber o null do Nmap, ele manda para o cleinte seu header:
           headers: Cabeçalho, informações indispensáveis/principais dos serviços(versão,modificação,programa...)
      - 5° O Nmap então recebe o CALL-BACK(resposta do server), lê o que o server mandou(cabeçalhos) e deleta seu próprio socket.

- [!] Se for treinar a análise de scans(Firewall/logs), sembre-se sempre de 1° criar a regrar no firewall pra logar todo tráfego.
      me esqueci disso "'perdi tempo", mas ganhei aprendizado.

- Repositórios Mencionados:
  
   - Nmap:[https://github.com/tlmtiger117/Nmap-Network-Mapper-]
     
   - Firewall:[https://github.com/tlmtiger117/Firewall]
     
   - Logs:[https://github.com/tlmtiger117/Logs]
 


 
     
   
