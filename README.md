🛡️ Azure Secure Access Lab: Implementação de Arquitetura Zero Trust

📝 Descrição\
Este projeto demonstra a implementação de uma infraestrutura de rede segura no Microsoft Azure, focada no isolamento total de recursos críticos. Utilizando os princípios de Zero Trust (Confiança Zero), configurei um ambiente onde servidores não possuem exposição direta à internet, mitigando vetores de ataque como varredura de portas e ataques de força bruta em protocolos administrativos (RDP/SSH).

🏗️ Arquitetura da Solução \
A rede foi desenhada com segmentação estrita utilizando os seguintes serviços:\
Virtual Network (VNet): Espaço de endereçamento isolado (vnet-lab).\
Azure Bastion (PaaS): Gateway de gerenciamento via navegador encapsulado em HTTPS (Porta 443).\
Network Security Groups (NSG): Regras de firewall granulares aplicadas para restringir o tráfego interno.\
Máquina Virtual (Windows/Linux): Host configurado estritamente com Private IP, residindo em uma sub-rede isolada.

🛠️ Detalhes da Rede (Networking)\
AzureBastionSubnet: 10.0.1.0/26 \
Workload Subnet (snet-vm): 10.0.2.0/24 \
IP Privado da VM: 10.0.2.4 

🚀 Competências Demonstradas\
Hardening de Infraestrutura: Eliminação de IPs públicos para redução da superfície de ataque. \
Segurança de Rede: Configuração e segmentação de sub-redes para isolamento de tráfego. \
Gestão de Acesso: Implementação de acesso administrativo seguro via túnel TLS/SSL.

📸 Evidências do Laboratório

1. Isolamento de Rede (Hardening)

![vm](https://github.com/user-attachments/assets/c7ad59f3-b5a2-4458-a09a-09112e5f0d91)

Nota técnica: Conforme evidenciado na captura, o campo Public IP address está como None. A VM possui apenas o IP privado 10.0.2.4, tornando-a invisível para scanners de vulnerabilidade na internet pública.

2. Segmentação de Sub-redes

![vnet](https://github.com/user-attachments/assets/c7e6ae19-c850-41d2-83d4-bcc2f698d0f5)

   
Nota técnica: Demonstração da separação lógica entre a rede de gestão e a rede de dados, seguindo as melhores práticas do Well-Architected Framework da Microsoft.

3. Acesso Seguro via Azure Bastion

<img width="1913" height="897" alt="bastion" src="https://github.com/user-attachments/assets/7730e074-0019-4f0b-87e0-d8d5b15e30a1" />

Nota técnica: Acesso realizado diretamente pelo navegador. O tráfego RDP é encapsulado em uma sessão TLS na porta 443, protegendo as credenciais contra ataques de "Man-in-the-Middle".

🛡️ Análise de Segurança: Por que usar Bastion?\
Ao invés de expor o servidor, a arquitetura implementada protege o ambiente contra:\
Port Scanning: Atacantes não encontram portas abertas para exploração.\
Brute Force: Sem IP público, não há alvo para tentativas de login automatizadas.\
Man-in-the-Middle: A conexão via Bastion garante criptografia ponta-a-ponta.

🎓 Conclusão
Este laboratório valida os conhecimentos práticos adquiridos para a certificação Microsoft SC-900, demonstrando a capacidade de arquitetar soluções que protegem a identidade e a infraestrutura em conformidade com o modelo de Confiança Zero.

Pedro Souza
Estudante de Defesa Cibernética | Desenvolvedor Full Stack | Microsoft Certified SC-900
