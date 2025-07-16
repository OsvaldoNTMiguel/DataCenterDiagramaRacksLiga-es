# DataCenterDiagramaRacksLiga-es
Diagrama de racks (S05, S06, S08 e S17), cada um com equipamentos organizados por unidades de rack (U). 





# Infraestrutura Cisco + SAN + NAS

Este repositório contém:

- Playbook Ansible para configurar switches Cisco, SAN e NAS.
- Inventário e variáveis de grupos.
- Runbook com passo a passo de execução e validação.

## Estrutura

- `inventory/inventory.ini`: hosts e variáveis.
- `playbooks/playbook_configuracao_infra.yml`: playbook principal.
- `playbooks/group_vars/switches.yml`: variáveis globais para switches.
- `runbooks/RUNBOOK_DEPLOY_INFRA.md`: guias de execução e testes.

## Requisitos

- Ansible 2.14+
- Coleções: `cisco.ios`, `ansible.netcommon`
- Acesso SSH aos dispositivos
- Usuário com privilégios `become` nos servidores SAN/NAS

## Instalação

```bash
git clone <repo_url>
cd infra-config-repo
ansible-galaxy collection install cisco.ios ansible.netcommon
