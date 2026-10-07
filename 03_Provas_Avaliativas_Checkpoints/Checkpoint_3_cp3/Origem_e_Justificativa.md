# Origem e Justificativa do Problema

**Disciplina:** Cybersecurity
**Ano Letivo:** 2025 | **Turma:** 4ECS
**Avaliação:** Checkpoint 3

### Enunciado do Problema
Configurar regras de inspeção profunda de pacotes (DPI) em firewall industrial para inspecionar protocolos Modbus TCP e CIP bloqueando comandos não autorizados de escrita em registradores.

### Formulação Formal
$$\text{Filtro DPI}: \text{Modbus TCP Function Code } 0x05 / 0x06 \xrightarrow{\text{Bloqueio se IP } \notin \text{ WhiteList}} \text{DROP}$$
