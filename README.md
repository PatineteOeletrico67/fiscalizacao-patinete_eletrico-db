# fiscalizacao-patinete-eletrico-db
<h1>Integrantes:</h1>
<p>John<br>Alicia<br>Enzo<br>Arthur<br>Isaac Fabiano</p>
<h1>Referencia:</h1>
guilhermeantunes-code/fiscalizacao-patinete
<h1>Regras de velocida do grupo:</h1>
<p>Patinete elétrico - Só em vias ate 60km/h; teto própio de 25km/h</p>

<h1>Relatório ESP32</h1>
<p>O ESP32 é uma série de microcontroladores de baixo custo, alto desempenho e baixo consumo de energia, desenvolvida pela Espressif Systems e amplamente consolidada como o padrão de mercado para projetos de Internet das Coisas (IoT).</p>
<p>A principal finalidade do chip é processar dados de sensores, controlar atuadores e realizar a comunicação sem fio entre dispositivos e sistemas na nuvem.</p> 
<p>Possui conectividade integrada, que oferece Wi-Fi (802.11 b/g/n) e Bluetooth (incluindo a versão clássica e o Bluetooth Low Energy - BLE) nativos no próprio silício, dispensando módulos externos para comunicação de rede.</p>
<p>A plataforma é extremamente versátil e suporta múltiplas linguagens de programação, sendo comumente programada em C/C++ por meio da popular Arduino IDE ou do framework oficial ESP-IDF, além de aceitar Python (através do MicroPython ou CircuitPython) e Javascript.</p>
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

