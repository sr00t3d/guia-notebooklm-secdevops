# 🚀 Miniguia de Estudos: SecDevOps e Automação de Infra

Este repositório foi desenvolvido como parte de um desafio prático na DIO, utilizando o **NotebookLM** como ferramenta de IA para organização de conhecimento e aprendizagem ativa.

## 📌 Contexto e Objetivos
O objetivo deste caderno temático é consolidar conhecimentos avançados em **SecDevOps**, focando na integração de segurança em pipelines de CI/CD e na automação de infraestrutura com Ansible e Shell Script. 

**Objetivos de estudo:**
* Sistematizar fluxos de análise de vulnerabilidades em tempo real.
* Criar um guia rápido de remediação para incidentes de infraestrutura.
* Otimizar a escrita de Playbooks para ambientes escaláveis.

---

## 📚 Curadoria de Fontes
Para alimentar o NotebookLM, utilizei as seguintes fontes de documentação técnica (Open Source):
1.  **Ansible Documentation (Community Guide):** Melhores práticas para automação.
2.  **OWASP DevSecOps Guideline:** Framework de segurança para desenvolvimento.
3.  **Linux Hardening Guide (CIS Benchmarks):** Parâmetros de segurança para servidores.
4.  **Google Cloud Architecture Framework (Security):** Estruturas de defesa em nuvem.

---

## 🧠 Engenharia de Prompts e "Cicatrizes"
Durante a interação com a IA, testei diferentes abordagens para extrair informações precisas sobre automação e segurança.

### Prompts Testados:
* *Prompt 1 (Genérico):* "Resuma como usar Ansible para segurança."
    * **Resultado:** Muito básico, não trouxe comandos úteis.
* *Prompt 2 (Específico):* "Com base nos documentos carregados, crie um checklist de hardening para servidores Ubuntu 22.04 usando apenas módulos nativos do Ansible."
    * **Resultado:** Excelente, trouxe parâmetros de SSH e regras de Firewall.

### 🛠 Troubleshooting (Cicatrizes):
* **Desafio:** A IA às vezes confundia sintaxes de versões antigas do Ansible.
* **Solução:** Ajustei o prompt para "Ignore módulos descontinuados e foque na sintaxe de Collections (FQCN)". Isso refinou a resposta para padrões modernos de mercado.

---

## 📖 Miniguia de Estudo (Entrega Final)

### 1. Resumo Estruturado: O Pilar SecDevOps
A integração de segurança não deve ser um gargalo. O fluxo ideal foca em:
* **Pre-commit:** Linting de código e busca por secrets expostas.
* **Build:** Análise estática (SAST) e verificação de dependências.
* **Deploy:** Aplicação de políticas de infraestrutura como código (IaC) validadas.

### 2. Glossário de Conceitos-Chave
* **Idempotência:** Capacidade de executar uma tarefa várias vezes sem alterar o resultado final além da aplicação inicial (crucial no Ansible).
* **Hardening:** Processo de mapear e fechar brechas de segurança em um sistema.
* **CI/CD Pipeline:** Esteira de integração e entrega contínua.
* **Drift Detection:** Identificar quando a configuração real do servidor diverge do código da infraestrutura.

### 3. Prompts Reutilizáveis para Revisão

> 💡 *Dica: Use estes prompts no seu dia a dia para revisar logs ou scripts.*

*Prompt para Troubleshooting de Infraestrutura:*
> Atue como um Engenheiro de SRE especializado em painéis de controle (cPanel/DirectAdmin). Analise o log de erro de automação abaixo. Identifique a causa raiz (Root Cause Analysis), correlacione com as diretrizes de permissões e dependências da documentação oficial e sugira o comando exato para correção via CLI, priorizando a manutenção da integridade dos serviços ativos. Log: SEU_LOG

 
*Prompt para Refatoração IaC (Ansible):*
> Converta o script Shell manual fornecido em uma Task do Ansible utilizando Full Qualified Collection Names (FQCN). A task deve ser estritamente idempotente, utilizar módulos nativos (evite o uso de 'shell' ou 'command' a menos que seja estritamente necessário) e incluir uma condicional 'when' para verificar o estado atual do sistema antes da execução. Script: SEU_SCRIPT

*Prompt para Auditoria de Segurança (SecDevOps):*
> Realize uma análise de segurança ofensiva e defensiva neste Dockerfile. Liste os 5 principais riscos de segurança (ex: execução como root, segredos expostos, imagens base não confiáveis). Para cada risco, forneça a recomendação de correção baseada nas melhores práticas do CIS Benchmark e reescreva o trecho de código vulnerável utilizando boas práticas de 'layer caching' e 'least privilege'.

---

### Como usar este repositório?
1. Clone o repo: `git clone https://github.com/sr00t3d/guia-notebooklm-secdevops/`
2. Utilize o arquivo `README.md` como base para seus estudos diários no NotebookLM.
