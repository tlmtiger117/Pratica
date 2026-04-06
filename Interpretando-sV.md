# 06/04/26
# Interpretando -sV do Nmap:

- -sV: Flag(sinal) utilizado pelo Nmap para expecificar um scan focado em descoberta de serviços(Fingersprint/digital).
   - Fingersprint não são 100% confiáveis, já que podem ser modificados. Servem mais como um indicativo do que certeza absoluta.
     
 
- Ex de como interpretar uma saida do -sV do Nmap:
   - Saida: OpenSSH 8.2p1 Ubuntu 4ubuntu0.5 (Ubuntu Linux; protocol 2.0)
     
- OpenSSH(Serviço,ofereçe algo)
   - serviço de acesso remoto seguro (SSH)
   - permite login remoto, execução de comandos, тунelamento, etc.
     
     
- 8.2p1(Programa, o que processa os dados dessa comunicação)
   - versão do software original (upstream)
   - 8.2 versão principal
   -  define funcionalidades e possíveis vulnerabilidades conhecidas
     

- p1 (patch level 1)
   - indica revisão oficial do projeto OpenSSH
   -  geralmente inclui:

      - correções de bugs
      - pequenos ajustes
      - às vezes correções de segurança
        

- importante:
   - não quer dizer “corrigiu tudo” — só que é a revisão daquela release(lançamento da quela versão programa).

- Ubuntu
   - pacote foi adaptado pela distro(pacoten pego e modificado pela distro pra ter uma melhro funcionalidade no SO).
   - pode incluir modificações específicas do sistema
     
     
- 4ubuntu0.5
   - versão do pacote dentro do Ubuntu()
     
     
- 4ubuntu
   - número do empacotamento da distro
   - versão do pacote preparada pelos mantenedores
     
     
- 0.5
   - revisões desse pacote
   -  pode incluir:
      - 🔒 patches de segurança
      - 🐛 correções de bugs
      - 🔧 ajustes de compatibilidade
        
        
- backports (correções de versões mais novas)
   - (Ubuntu Linux; protocol 2.0)
   -  info detectada pelo Nmap
     
      
- Ubuntu Linux
   - provável sistema operacional
     
     
- protocol 2.0
  - versão do protocolo SSH
  - segura e padrão atual
  -  SSHv1 seria vulnerável
 
Repositório mencionado:
Nmap:[https://github.com/tlmtiger117/Nmap-Network-Mapper-]

 

