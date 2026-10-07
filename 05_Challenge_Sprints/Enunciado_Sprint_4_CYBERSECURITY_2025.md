# Challenge Sprint 4 - CYBERSECURITY

**Título do Challenge:** SPI / METAINDÚSTRIA - SMART ROBOTICS
**Turma:** 4ECS | **Ano:** 2025
**Período para Entrega:** 01/10/2025 - 31/10/2025
**Status:** NOTA: 100
**Cabeçalho Original:** CYBERSECURITY - Henrique Siqueira Nunweiler NOTA: 100

## 1. Enunciado e Instruções do Professor

**4º Entregável | Challenge Sprint | Cybersecurity | 2025**

Como o professor Sérgio Rota explicou no enunciado do seu Challenge Sprint, a segurança cibernética é assunto de máxima importância em empresas de tecnologia, ou em empresas que usam tecnologia para cumprir seus propósitos comerciais.

Como estamos estudando questões relacionadas a Segurança Cibernéticas em ambientes industriais, segue um questionário de boas práticas de segurança da informação aplicado ao desenvolvimento de software para controladores:

IMPORTANTE: A avaliação será realizada exclusivamente pela aba Trabalhos, no Teams, na disciplina de CyberSecurity.

[Exibir atribuição: "Sprint Challenge #4 - Cybersecurity"](https://teams.microsoft.com/l/entity/66aeee93-507d-479a-a3ef-8f494af43945/classroom?context=%7B%22subEntityId%22%3A%22%7B%5C%22version%5C%22%3A%5C%221.0%5C%22%2C%5C%22config%5C%22%3A%7B%5C%22classes%5C%22%3A%5B%7B%5C%22id%5C%22%3A%5C%220c6d0992-d414-40d5-8be9-4be11b1c2eb4%5C%22%2C%5C%22assignmentIds%5C%22%3A%5B%5C%22b956d056-51b7-4a7a-b86a-d37bb03f8d84%5C%22%5D%7D%5D%7D%2C%5C%22action%5C%22%3A%5C%22navigate%5C%22%2C%5C%22view%5C%22%3A%5C%22assignment-viewer%5C%22%2C%5C%22appId%5C%22%3A%5C%22ccb65bcd-04ba-421a-8791-a299a70904b6%5C%22%2C%5C%22deeplinkType%5C%22%3A4%7D%22%2C%22channelId%22%3Anull%7D)
 **1. Ao desenvolver um código para Arduino que recebe um comando via porta serial (ex: "ligar"), qual é a prática de segurança mais eficaz para processar essa entrada e evitar comportamentos inesperados?**

a) Confiar que o usuário sempre enviará o comando correto.

b) Usar a função delay() para dar tempo ao processador.

c) Converter a entrada para um número inteiro imediatamente.

d) Validar a entrada contra uma lista de comandos permitidos (ex: "ligar", "desligar") e ignorar todo o resto.

e) Aumentar o tamanho do buffer de recepção serial para evitar perdas.

 

**2. Um Arduino controla uma fechadura e recebe senhas via rede. Para prevenir um ataque de força bruta, onde um atacante tenta milhares de senhas por segundo, qual medida de defesa de software é mais simples e eficaz?**

* Reiniciar a placa controladora após cada tentativa falha.
* Aumentar o comprimento da senha para mais de 50 caracteres.
* Introduzir um atraso obrigatório (delay()) de alguns segundos após cada tentativa de senha incorreta.
* Limpar o buffer serial com mais frequência.
* Usar um LED de cor diferente para indicar uma tentativa falha.
 

**3. Ao conectar um Arduino a uma rede Wi-Fi, qual é a principal vulnerabilidade de segurança ao se escrever const char* password = "Senha12345"; diretamente no código-fonte principal (.ino) e compartilhá-lo em um repositório público como o GitHub?**

* A senha pode ser facilmente alterada por outros desenvolvedores.
* O código-fonte fica mais longo e difícil de ler.
* A senha (um "segredo") fica exposta publicamente, permitindo que qualquer pessoa com acesso ao código se conecte à sua rede Wi-Fi.
* O compilador pode otimizar a variável, causando erros de conexão.
* A senha precisa ser digitada toda vez que o Arduino é reiniciado.
 

**4. Se um dispositivo Arduino envia dados de um sensor para um servidor na internet via Wi-Fi, qual é a maneira correta de proteger a confidencialidade desses dados durante o trânsito na rede?**

* Enviar os dados usando o método HTTP POST em vez de GET.
* Usar uma biblioteca cliente que implemente criptografia TLS (ex: HTTPS, MQTTS).
* Codificar os dados em Base64 antes de enviá-los.
* Contar apenas com a criptografia da rede Wi-Fi (WPA2/WPA3).
* Definir um endereço IP fixo para o Arduino.
 

**5. Mesmo que o seu código seja perfeitamente seguro contra ataques de rede, qual é o principal risco de segurança se um atacante obtiver acesso físico à placa controladora?**

* O atacante pode tentar adivinhar a senha de acesso pela porta serial.
* O atacante pode conectar um cabo de rede para realizar um ataque de DoS.
* O atacante pode usar pinos de hardware específicos (interface ISP) para extrair o firmware compilado diretamente da memória do microcontrolador.
* O atacante pode medir o consumo de energia da placa.
* O atacante pode alterar o endereço IP do dispositivo.
 

**6. No loop() de um Arduino, qual das seguintes práticas de programação pode ser mais facilmente explorada por um atacante para causar uma Negação de Serviço (DoS), tornando o dispositivo lento ou irresponsivo?**

* Usar a função digitalWrite() para alterar o estado de um pino.
* Usar Serial.println() para enviar mensagens de log.
* Usar uma estrutura if-else para tomar decisões.
* Usar uma chamada bloqueante como delay() ou um laço while() que pode ser manipulado por uma entrada externa para demorar muito tempo.
* Definir o modo de um pino com pinMode() repetidamente.
 

**7. Um ataque de "Buffer Overflow" em um Arduino ocorre tipicamente quando:**

* A função loop() executa rápido demais.
* O programa tenta escrever mais dados em um array de caracteres (char[]) do que o espaço alocado para ele, sobrescrevendo áreas adjacentes da memória.
* A placa fica sem portas digitais disponíveis para uso.
* A memória EEPROM é lida muitas vezes seguidas.
* O objeto String é usado para concatenar textos muito longos, causando fragmentação da memória.
 

**8. O "Princípio do Menor Privilégio", quando aplicado ao firmware de um Arduino, significa que:**

* O código deve ser o menor possível para caber na memória Flash.
* O dispositivo deve consumir a menor quantidade de energia possível.
* Uma função ou componente de software deve ter acesso apenas aos recursos e dados estritamente necessários para realizar sua tarefa.
* O Arduino deve ter o menor número de conexões físicas possível.
* A senha de acesso deve ser a mais curta e simples possível.
 

**9. Ao implementar uma funcionalidade de atualização de firmware Over-the-Air (OTA) para um dispositivo, qual é a medida de segurança mais crítica para garantir que o Arduino não instale um firmware malicioso enviado por um atacante?**

* Verificar se o novo arquivo de firmware é menor que o anterior.
* Usar um servidor de atualização com senha de acesso HTTP.
* Exigir que o arquivo de firmware tenha uma assinatura digital válida, que é verificada pelo dispositivo antes da instalação.
* Compactar o firmware antes de enviá-lo pela rede.
* Garantir que o nome do arquivo do firmware siga um padrão específico.
 

**10. Em um produto final, por que a prática de deixar múltiplas chamadas Serial.println() para fins de depuração no código pode representar um risco de segurança?**

* Elas tornam o loop() principal mais lento, criando uma vulnerabilidade de DoS.
* Elas consomem uma quantidade significativa de memória RAM.
* Se um atacante obtiver acesso à porta serial, essas mensagens podem vazar informações sensíveis sobre o funcionamento interno do sistema, variáveis e senhas.
* Elas podem causar um Buffer Overflow no buffer de transmissão serial.
* Elas só funcionam se o Monitor Serial estiver aberto na Arduino IDE.

## 2. Anexos e Links de Referência

- [Exibir atribuição: "Sprint Challenge #4 - Cybersecurity"](https://teams.microsoft.com/l/entity/66aeee93-507d-479a-a3ef-8f494af43945/classroom?context=%7B%22subEntityId%22%3A%22%7B%5C%22version%5C%22%3A%5C%221.0%5C%22%2C%5C%22config%5C%22%3A%7B%5C%22classes%5C%22%3A%5B%7B%5C%22id%5C%22%3A%5C%220c6d0992-d414-40d5-8be9-4be11b1c2eb4%5C%22%2C%5C%22assignmentIds%5C%22%3A%5B%5C%22b956d056-51b7-4a7a-b86a-d37bb03f8d84%5C%22%5D%7D%5D%7D%2C%5C%22action%5C%22%3A%5C%22navigate%5C%22%2C%5C%22view%5C%22%3A%5C%22assignment-viewer%5C%22%2C%5C%22appId%5C%22%3A%5C%22ccb65bcd-04ba-421a-8791-a299a70904b6%5C%22%2C%5C%22deeplinkType%5C%22%3A4%7D%22%2C%22channelId%22%3Anull%7D)

