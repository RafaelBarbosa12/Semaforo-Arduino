# Semaforo-Arduino

### Felipe Zilo:

| Critério                                                                                                 | Contempla (Pontos) | Contempla Parcialmente (Pontos) | Não Contempla (Pontos) | Observações do Avaliador |
|---------------------------------------------------------------------------------------------------------|--------------------|----------------------------------|--------------------------|---------------------------|
| Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores                | Até 3              | Até 1,5                            | 0                        |         3                  |
| Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo                  | Até 3              | Até 1,5                          | 0                        |                  3         |
| Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) | Até 3              | Até 1,5                          | 0                        |        3                   |
| Extra: Implmeentou um componente de liga/desliga no semáforo e/ou usou ponteiros no código | Até 1              |  Até 0,5                         | 0                        |                1           |
|  |                                                             |  | |**Pontuação Total** 10|


### Davi Basã:

| Critério                                                                                                 | Contempla (Pontos) | Contempla Parcialmente (Pontos) | Não Contempla (Pontos) | Observações do Avaliador |
|---------------------------------------------------------------------------------------------------------|--------------------|----------------------------------|--------------------------|---------------------------|
| Montagem física com cores corretas, boa disposição dos fios e uso adequado de resistores                | Até 3              | Até 1,5                            | 0                        |         3                  |
| Temporização adequada conforme tempos medidos com auxílio de algum instrumento externo                  | Até 3              | Até 1,5                          | 0                        |                  3         |
| Código implementa corretamente as fases do semáforo e estrutura do código (variáveis representativas e comentários) | Até 3              | Até 1,5                          | 0                        |        3                   |
| Extra: Implmeentou um componente de liga/desliga no semáforo e/ou usou ponteiros no código | Até 1              |  Até 0,5                         | 0                        |                1           |
|  |                                                             |  | |**Pontuação Total** 10|

Para montagem do protótipo foram necessárias 6 jumpers, protoboard, o arduíno, 3 leds e um buzzer.

Os leds vermelho, amarelo e verde foram conectados nas portas 13, 12 e 11, respectivamente. Com isso, através do código, é possível fazer os leds piscarem na mesma ordem de um semáforo. Além disso, o buzzer foi conectado na porta 10, seu objetivo é apitar sempre que o led estiver verde.

### Código:
```C++
// Definindo os pinos para cada LED e o buzzer
const int ledVermelho = 13;
const int ledAmarelo = 12;
const int ledVerde = 11;
const int buzzer = 10;

void setup() {
  // Configurando os pinos como saída
  pinMode(ledVermelho, OUTPUT);
  pinMode(ledAmarelo, OUTPUT);
  pinMode(ledVerde, OUTPUT);
  pinMode(buzzer, OUTPUT);
}

void loop() {
  // Acende o LED verde e ativa o buzzer
  digitalWrite(ledVerde, HIGH);
  tone(buzzer, 1000); // Emite um som de 1000 Hz no buzzer
  delay(2000); // Mantém o verde e o buzzer ativos por 2 segundos
  digitalWrite(ledVerde, LOW);
  noTone(buzzer); // Desativa o som do buzzer

  // Acende o LED verde e ativa o buzzer
  digitalWrite(ledVerde, HIGH);
  tone(buzzer, 1000); // Emite um som de 1000 Hz no buzzer
  delay(2000); // Mantém o verde e o buzzer ativos por 2 segundos
  digitalWrite(ledVerde, LOW);
  noTone(buzzer); // Desativa o som do buzzer

  // Acende o LED amarelo
  digitalWrite(ledAmarelo, HIGH);
  delay(2000); // Mantém o amarelo aceso por 2 segundos
  digitalWrite(ledAmarelo, LOW);

  // Acende o LED vermelho
  digitalWrite(ledVermelho, HIGH);
  delay(6000); // Mantém o vermelho aceso por 6 segundos
  digitalWrite(ledVermelho, LOW);

  // Acende o LED amarelo
  digitalWrite(ledAmarelo, HIGH);
  delay(2000); // Mantém o amarelo aceso por 2 segundos
  digitalWrite(ledAmarelo, LOW);
}
```

[Clique aqui para acessar o vídeo]([https://drive.google.com/drive/u/0/home](https://drive.google.com/file/d/1ZelHFKuD_vnEPZsj4DEaX8XDzxXph1cy/view?usp=drivesdk))
