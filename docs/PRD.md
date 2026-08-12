### Visão do Produto & Problema de Negócio

**Problema:** A rede de distribuição da LogiTech está sendo prejudicada por um problema de falta de localização eficiente das cargas. Carga que vão parar em locais indesejados, causando deslocamentos desnecessários e desperdício de tempo.

**Visão:** Ao implementar a solução do serviço de telemetria para Frota da LogiTech, pretendemos aumentar o desempenho da logística, reduzir os danos das mudanças no trajeto e minimizar os custos associados à localização imprecisa das cargas.

**Público-Alvo:** Personas:
- **Operador de Logística**: Realiza o controle de caminhões na frota.
- **Coleta**: Gerencia a entrega da carga para as locais desejados.
- **Entrega**: Monitora os entregadores e coordena com operadores logísticos.

### Casos de Uso (Use Cases)

#### UC01 - Localizar Caminhoes
**Ator:** Operador de Logística

**Pré-condição:** Sistema inicial, com todas as informações sobre a frota atualmente disponíveis.

**Fluxo Principal:**
1. Selecionar o caminhão específico.
2. Solicitar visualização das rotas anteriores da carga para localizar sua posição atual.
3. Verificar se há alguma inconsistência em termos de localização da informação, como um movimento reciente que não tenha sido identificado.

**Critérios de Aceite:**
- Visualização correta do trajeto atualizado com base nas informações históricas.
- Resposta eficaz e rápida para qualquer incompatibilidade entre as rotas anteriores.

#### UC02 - Seguir caminhoes
**Ator:** Entrega

**Pré-condição:** Sistema inicial, com todas as informações sobre a frota atualmente disponíveis.

**Fluxo Principal:**
1. Selecionar o caminhão específico para entrega.
2. Solicitar visualização das rotas anteriores da carga que está sendo entregue.
3. Verificar se há alguma inconsistência em termos de localização do caminho atual.

**Critérios de Aceite:**
- Visualização correta dos trajetos atuais e possíveis ajustes necessários para a entrega eficaz.

#### UC03 - Marcar Entrega
**Ator:** Coleta

**Pré-condição:** Sistema inicial, com todas as informações sobre a frota atualmente disponíveis.

**Fluxo Principal:**
1. Selecionar o caminhão específico para realizar uma nova coleta.
2. Solicitar visualização das rotas anteriores da carga que está sendo coletada.
3. Verificar se há alguma inconsistência em termos de localização dos dados históricos.

**Critérios de Aceite:**
- Visualização correta do trajeto atualizado e possíveis ajustes necessários para a coleta eficaz.

### Requisitos Não-Funcionais (RNFs) & SLAs

- **Segurança:** Implementar autenticação OAuth2, OIDC, RBAC.
- **Desempenho:**
  - RPS (Response per second)
  - Tempo de resposta p95/p99 (para garantir que a resposta seja concluída em mais de 95% do tempo).
- **Escalabilidade:** Implementar serviços containerizados utilizando Docker/Kubernetes para garantir escalabilidade e reconfiguração automatizada.
- **Conteinerização:** Usar Kubernetes para gerenciar os containers dos serviços, permitindo a replicação fácil e reconfiguração rápida das máquinas virtuais da infraestrutura.

Esta é uma visão inicial do PRD que pode ser desenvolvido com base nesta metodologia.
