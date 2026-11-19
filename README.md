# 🛡️ Plano de Resposta a Incidentes (PRI) & Playbooks Táticos — UFRGS

[![NIST SP 800-61r3](https://img.shields.io/badge/Framework-NIST%20SP%20800--61r3-blue.svg)](https://csrc.nist.gov/publications/detail/sp/800-61/rev-3/final)
[![MITRE ATT&CK](https://img.shields.io/badge/TTPs-MITRE%20ATT%26CKS-orange.svg)](https://attack.mitre.org/)
[![LGPD Compliance](https://img.shields.io/badge/Conformidade-LGPD%20%2F%20Art.%2048-green.svg)](https://www.planalto.gov.br/ccivil_03/_ato2015-2018/2018/lei13709.htm)
[![Status](https://img.shields.io/badge/Status-Concluído%20%2F%20Implantado-success.svg)]()

Repositório oficial contendo a arquitetura de governança, o **Plano de Resposta a Incidentes (PRI)** e os **Playbooks Táticos** desenvolvidos para a **Universidade Federal do Rio Grande do Sul (UFRGS)**, estruturados no âmbito da Residência Tecnológica em Resposta a Incidentes e Forense Digital (Programa Hackers do Bem / RNP / UFRGS).
Observação: O arquivo disponibilizado corresponde à versão técnica/pública do relatório final de residência, enquanto o documento assinado permanece arquivado para fins institucionais.

---

## 📋 Sobre o Projeto

Este projeto aborda a transição de ecossistemas reativos para estruturas de defesa proativas em instituições de ensino e pesquisa de grande porte. A iniciativa traduz diretrizes de segurança internacional e requisitos legais em um ecossistema operacional documentado, escalável e voltado para a mitigação de riscos críticos na infraestrutura acadêmica.

O trabalho resultou tanto na documentação institucional quanto na produção do artigo científico 

## 📥 Documentos e Artefatos Disponíveis

Clique nos links abaixo para visualizar ou baixar os documentos técnicos completos deste projeto:

* 📄 **[Relatório Final de Residência Tecnológica (PDF)](./Elzilene%20Montanha%20Machado%20-%20Relatório%20Final.pdf)**
* 📘 **[Material de Treinamento e Playbooks (PDF)](./Treinamento.pdf)**, utilizado como material de treinamento para UFRGS, contendo todos os dados correspondentes ao playbooks desenvolvidos.

---

## 🏛️ Os 3 Pilares da Governança de Resposta

A arquitetura do PRI fundamenta-se em três eixos estratégicos para eliminar ambiguidades decisórias em cenários de crise:

1. **Matriz de Riscos Institucionais:** Classificação de incidentes orientada ao impacto finalístico (Formação e Ensino, Pesquisa e Inovação, Extensão Universitária, Ambiente de Trabalho e Sustentação Financeira).
2. **Matriz RACI e Comunicação:** Definição clara de papéis e responsabilidades (*Responsible, Accountable, Consulted, Informed*) e integração com o DPO para o cumprimento dos prazos legais da LGPD (notificação à ANPD em até 48 horas úteis).
3. **Cultura de Registro (*Live Forensics*):** Preservação da cadeia de custódia e coleta de evidências voláteis (memória RAM) durante a fase de contenção, garantindo validade jurídica.

---

## ⚡ Playbooks Táticos Especializados

O repositório disponibiliza módulos operacionais ("instruções de combate") mapeados às táticas do **MITRE ATT&CK** e ao ciclo de vida do **NIST SP 800-61r3**:

* **🔐 1. Comprometimento de Contas:** Foco em mitigação de *Phishing*, *Bypass de MFA* e *Session Hijacking*. Ações críticas: revogação global de tokens, bloqueio de contas e Acesso Condicional.
* **🖥️ 2. Comprometimento de Servidores:** Voltado para a superfície de exposição de portais institucionais. Detecção de *Web Shells*, *Cryptojacking* e movimentação lateral, com isolamento em VLANs de quarentena e análise forense de RAM.
* **📂 3. Vazamento de Informações:** Tratamento de exfiltração furtiva (*Slow & Low*) e configuração incorreta em ambientes de nuvem, integrando o fluxo técnico com o DPO.
* **🌐 4. Ataques DoS / DDoS:** Mitigação de indisponibilidade em serviços críticos (Moodle, SEI) via ativação de *Scrubbing Centers*, *Rate Limiting* e inspeção profunda de pacotes (WAF Camada 7).

---

## 🔄 Pipeline de Triagem & SIEM (Wazuh)

O ecossistema integra a telemetria institucional ao **Wazuh (SIEM)** para filtragem automatizada de ruídos rotineiros e suporte à disponibilidade resiliente do SOC/CSIRT, incluindo repositórios offline de playbooks para cenários de queda severa de rede.

---

## 📁 Estrutura do Repositório

*  docs-                 Documentação completa do PRI em PDF e Markdown
*  playbooks-            Módulos táticos operacionais (Contas, Servidores, Vazamento, DDoS)
*  schemas-              Matrizes RACI, fluxogramas e diagramas conceituais (.png / .drawio)
*  README.md -           Documentação principal do repositório
