# fiscalizacao-patinete-eletrico-db
# Integrantes:
<p>John<br>Alicia<br>Enzo<br>Arthur<br>Isaac Fabiano</p>

## Referência:
guilhermeantunes-code/fiscalizacao-patinete
## Regras de velocidade do grupo:
<p>Patinete elétrico - Só em vias ate 60km/h; teto própio de 25km/h</p>

# Relatório ESP32
## Sobre
<p>O ESP32 é uma série de microcontroladores de baixo custo, alto desempenho e baixo consumo de energia, desenvolvida pela Espressif Systems e amplamente consolidada como o padrão de mercado para projetos de Internet das Coisas (IoT).</p>
<p>A principal finalidade do chip é processar dados de sensores, controlar atuadores e realizar a comunicação sem fio entre dispositivos e sistemas na nuvem.</p> 
<p>Possui conectividade integrada, que oferece Wi-Fi (802.11 b/g/n) e Bluetooth (incluindo a versão clássica e o Bluetooth Low Energy - BLE) nativos no próprio silício, dispensando módulos externos para comunicação de rede.</p>
<p>A plataforma é extremamente versátil e suporta múltiplas linguagens de programação, sendo comumente programada em C/C++ por meio da popular Arduino IDE ou do framework oficial ESP-IDF, além de aceitar Python (através do MicroPython ou CircuitPython) e Javascript.</p>

## Desenvolvimento
<p>Começamos o projeto conectando o ESP32 no computador usando um cabo USB e encaixando a placa na protoboard para ficar firme. O primeiro passo foi instalar o driver do chip USB-Serial no computador, para que ele conseguisse reconhecer a placa e criar a porta de comunicação (COM). <br>Com isso resolvido, fomos para o Arduino IDE e adicionamos o link da Espressif nas configurações para conseguir baixar e instalar o pacote de placas do ESP32. Depois que a instalação terminou, selecionamos o modelo da placa e a porta COM certa nos menus do programa. <br>Para testar se tudo estava conversando bem, carregamos o código para fazer o LED piscar e mandamos o arquivo para a placa. O teste deu certo: o LED azul que vem integrado na placa começou a piscar de um em um segundo, o que provou que toda a instalação e a placa estavam funcionando perfeitamente.</p>
<table>
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/cdd6cb60-485c-410a-bd7f-edc5df57d407" width="400px" alt="Placa ESP32"><br>
      <b>Figura 1:</b> Placa ESP32 conectada ao PC piscando o LED azul.
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/7f4c6ffe-d177-41dd-8e1f-d6121b145704" width="400px" alt="Código no Arduino"><br>
      <b>Figura 2:</b> Código de programação utilizado no Arduino IDE.
    </td>
  </tr>
</table>

# Projeto com Raspberry Pi

## Objetivo

Configurar uma Raspberry Pi para utilizar Docker, MariaDB e Node-RED, permitindo a comunicação e o armazenamento de dados em um banco de dados.

## Desenvolvimento

Inicialmente, a Raspberry Pi deveria ser conectada a uma rede Wi-Fi específica e acessada remotamente através do **SSH**.

Durante os testes, a conexão Wi-Fi apresentou instabilidade, caindo frequentemente e desconectando a Raspberry Pi. Por esse motivo, foi alterada a forma de conexão para a rede cabeada do laboratório, mantendo o acesso remoto através do SSH.

Após conseguir acessar a Raspberry Pi, iniciamos a configuração do Docker e do MariaDB utilizando um arquivo `docker-compose.yml`. O arquivo contém as configurações do banco de dados, armazenamento e rede dos containers.

Também foi planejada a utilização do Node-RED para realizar testes de comunicação com o MariaDB, utilizando fluxos para:

- Enviar dados para o banco;
- Ler dados do banco;
- Visualizar os resultados através do Debug.

## Problemas encontrados

O primeiro problema foi a instabilidade da rede Wi-Fi, que causava desconexões frequentes da Raspberry Pi. Para solucionar isso, passamos a utilizar a rede cabeada do laboratório.

Depois, encontramos um problema na configuração da rede utilizada pelos containers Docker. A rede definida no `docker-compose.yml` não estava sendo criada automaticamente.

Por falta de tempo, não conseguimos realizar a configuração manual da rede e, consequentemente, não foi possível finalizar os testes de comunicação entre o Node-RED e o MariaDB.

## Situação atual

Até o momento, conseguimos:

- Acessar a Raspberry Pi remotamente através do SSH;
- Configurar parte do ambiente Docker;
- Preparar o MariaDB;
- Iniciar a configuração do Node-RED.

Ainda falta concluir a configuração da rede Docker e realizar os testes de leitura e escrita entre o Node-RED e o MariaDB.

## Próximos passos

1. Configurar a rede dos containers;
2. Verificar o funcionamento do MariaDB;
3. Conectar o Node-RED ao banco;
4. Testar a escrita e leitura de dados;
5. Validar o funcionamento completo do sistema.

