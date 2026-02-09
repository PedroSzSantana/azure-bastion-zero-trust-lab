🛡️ Azure Secure Access Lab: Implementação de Arquitetura Zero Trust

📝 Descrição

Este projeto demonstra a implementação de uma infraestrutura de rede segura no Microsoft Azure, focada no isolamento total de recursos críticos. Utilizando os princípios de Zero Trust (Confiança Zero), configurei um ambiente onde servidores não possuem exposição direta à internet, mitigando vetores de ataque como varredura de portas e força bruta em RDP/SSH.

🏗️ Arquitetura da Solução
A rede foi desenhada com segmentação estrita utilizando os seguintes serviços:
Virtual Network (VNet): Espaço de endereçamento isolado (vnet-lab).
Azure Bastion (PaaS): Gateway de gerenciamento via navegador (Porta 443).
Network Security Groups (NSG): Regras de firewall granulares (vm-lab-nsg).
Máquina Virtual (Linux/Windows): Configurada com Private IP apenas.

🚀 Competências Demonstradas
Hardening de Infraestrutura: Remoção de IPs públicos de servidores para redução de superfície de ataque.
Segurança de Rede: Configuração de VNets e Subnets específicas (snet-vm).
Gestão de Identidade e Acesso: Implementação de acesso administrativo seguro via túnel TLS/SSL (Bastion).

📸 Evidências do Laboratório

1. Isolamento de Rede (Hardening)

![Captura de tela_9-2-2026_135915_portal azure com](https://github.com/user-attachments/assets/32a084cb-0798-4498-a030-ece960538227)


2. Acesso via Azure Bastion (Sessão Segura)

Nota técnica: O acesso administrativo é realizado via portal do Azure, onde o Bastion encapsula o tráfego RDP/SSH em uma sessão HTTPS (porta 443).

🎓 Conclusão

Este laboratório valida os conhecimentos adquiridos na certificação Microsoft SC-900, aplicando na prática conceitos de segurança em nuvem e proteção de perímetro.
Pedro Souza Estudante de Defesa Cibernética | Microsoft Certified SC-900
