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

O trabalho resultou tanto na documentação institucional quanto na produção do artigo científico.

## 📥 Documentos e Artefatos Disponíveis

Clique nos links abaixo para visualizar ou baixar os documentos técnicos completos deste projeto:

* 📄 **[Relatório Final de Residência Tecnológica (PDF)](./Relatório%20Final.pdf)**
* 📘 **[Material de Treinamento e Playbooks (PDF)](./Treinamento.pdf)**, utilizado como material de treinamento para UFRGS, contendo todos os dados correspondentes aos playbooks desenvolvidos.
* 📊 **[Apresentação do Projeto (PDF)](./Apresentação%20.pdf)** *(Nota: ajuste o nome do arquivo se necessário)*

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

## 🛠️ Ferramentas, Checklists e Formulários (Guia de Consulta)

Alguns checklists interativos, formulários de registro de evidências e ferramentas operacionais estão compilados no arquivo **[Material de Treinamento (PDF)](./Treinamento.pdf)**. Abaixo está o índice de navegação rápida por página para cada módulo:

### Módulos Técnicos

![Comprometimento de Contas](https://img.shields.io/badge/-Comprometimento%20de%20Contas-5d7784?style=for-the-badge)
  * Checklist Plano de Resposta — Roteiro inicial de triagem para incidentes envolvendo contas de usuário (ex.: e-mails corporativos, VPNs, portais acadêmicos). Ajuda a identificar o escopo do comprometimento antes de ações drásticas. *Página 21*
  * Tratamento de Incidentes — Guia passo a passo para as ações de contenção, erradicação e recuperação. Inclui procedimentos para revogação global de tokens, bloqueio de contas e ativação de Acesso Condicional. *Página 22*
  * Formulário de Registro de Evidências — Documento padronizado para registrar logs de autenticação, IPs de origem e artefatos coletados, garantindo a rastreabilidade e a cadeia de custódia. *Página 23*
  * Módulo Técnico (Teoria e Ações) — Aprofundamento técnico sobre os vetores de ataque (Phishing, Bypass de MFA, Session Hijacking) e as ferramentas de mitigação disponíveis no ecossistema. *Página 38*

![Comprometimento de Servidores](https://img.shields.io/badge/-Comprometimento%20de%20Servidores-0d234f?style=for-the-badge)
  * Checklist de Resposta a Incidentes — Roteiro focado na superfície de exposição de servidores e portais institucionais, auxiliando na identificação de Web Shells, Cryptojacking e movimentação lateral. *Página 23*
  * Tratamento de Incidente de Segurança — Procedimentos táticos para isolamento da máquina afetada em VLANs de quarentena, coleta de memória RAM (Live Forensics) e bloqueio de conexões maliciosas. *Página 24*
  * Formulário de Registro de Evidências — Ficha específica para registrar artefatos de servidores (arquivos maliciosos, chaves de registro, logs de sistema), mantendo o rigor forense. *Página 25*
  * Comprometimento por Tipos de Ataques — Tabela de referência rápida que cruza o tipo de ataque detectado no servidor com a ação de resposta recomendada. *Página 26*
  * Módulo Técnico (Teoria e Ações) — Detalhamento das técnicas de invasão a servidores e dos comandos/ferramentas específicos para análise forense e contenção. *Página 60*

![Vazamento de Informações](https://img.shields.io/badge/-Vazamento%20de%20Informa%C3%A7%C3%B5es-00364c?style=for-the-badge)
  * Tratamento de Incidente de Segurança — Fluxo de resposta focado em exfiltração de dados (Slow & Low) e configurações incorretas em nuvem, com integração direta ao DPO e ao Plano de Comunicação de Incidentes. *Página 20*
  * Comprometimento por Tipos de Ataques — Guia para identificar a origem do vazamento e aplicar as medidas corretivas específicas para cada vetor de exposição de dados. *Página 21*
  * Módulo Técnico (Teoria e Ações) — Orientações técnicas sobre como conter a exfiltração de dados e o passo a passo para o cumprimento dos prazos e obrigações da LGPD (Art. 48). *Página 87*

![Ataques DoS/DDoS](https://img.shields.io/badge/-Ataques%20DoS%2FDDoS-555550?style=for-the-badge)
  * Checklist - Plano de Resposta — Roteiro de ação rápida para quando serviços críticos (como Moodle e SEI) ficam indisponíveis, focado em garantir a continuidade operacional. *Página 26*
  * Tratamento de Incidentes — Instruções para ativação de Scrubbing Centers, Rate Limiting e inspeção profunda de pacotes (WAF Camada 7) para mitigar o tráfego malicioso. *Página 27*
  * Registro Tratamento de Incidentes — Formulário para documentar o volume do ataque (ex.: requisições por segundo), a duração e as contramedidas aplicadas na infraestrutura. *Página 28*
  * Tipos de Ataques DoS/DDoS — Material de apoio que diferencia ataques volumétricos, de protocolo e de camada de aplicação, ajudando o analista a escolher a defesa correta. *Página 29*
  * Módulo Técnico (Teoria e Ações) — Explicação técnica sobre a arquitetura de rede para absorção de tráfego e as configurações de firewall necessárias para bloquear os ataques. *Página 109*

]![Governança e Resposta Global](https://img.shields.io/badge/-Governança%20e%20Resposta%20Global-050A40?style=for-the-badge)
* **Plano de Respostas a Incidentes**
  * Formulário de Registro de Evidências — Formulário mestre de Registro de Evidências, utilizado como documento consolidador para incidentes de alta criticidade que exigem acionamento do CSIRT e da alta gestão. *Página 139*

### 💻 Ferramenta Desenvolvida (Acesso Direto)
* **[Detector de Ameaças UFRGS (Streamlit)](https://detector-ameacas-ufrgs-jarr7y2ahbycccf7evdll2.streamlit.app/)** — Aplicação web interativa desenvolvida para auxiliar a equipe de TI na triagem automatizada e na detecção rápida de anomalias e artefatos suspeitos na rede, com utilização de chave API do VirusTotal em tempo real.

---

## 🔄 Pipeline de Triagem & SIEM (Wazuh)

O ecossistema integra a telemetria institucional ao **Wazuh (SIEM)** para filtragem automatizada de ruídos rotineiros e suporte à disponibilidade resiliente do SOC/CSIRT, incluindo repositórios offline de playbooks para cenários de queda severa de rede.

---

## 📁 Estrutura do Repositório

* 📄 `Apresentação.pdf` - Slides de apresentação do projeto.
* 📄 `README.md` - Documentação principal do repositório.
* 📄 `Relatório Final.pdf` - Documento técnico completo da residência.
* 📄 `Treinamento.pdf` - Guia prático com Playbooks, Checklists, Formulários e Ferramentas.
