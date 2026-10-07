# Origem e Justificativa do Problema

**Disciplina:** Cybersecurity
**Ano Letivo:** 2025 | **Turma:** 4ECS
**Avaliação:** Checkpoint 5

### Enunciado do Problema
Desenvolver regras de correlação de eventos no Elastic SIEM / Splunk para detectar anomalias comportamentais, tentativas de força bruta e conexões a endereços IP maliciosos conhecidos.

### Formulação Formal
$$\text{Regra SIEM}: \text{count}(\text{event.type: failed\_login}) > 5 \text{ em } 60\text{s} \implies \text{Alerta SOC Severidade Alta}$$
