# 🏠 Smart Home Dashboard com FastAPI, MODBUS e Interface Web

Este projeto integra uma **API REST em Python (FastAPI)**, comunicação com **servidor MODBUS**, **banco de dados SQLite**, e uma **interface web responsiva** com HTML, CSS e JavaScript, formando um painel de controle para monitoramento e automação residencial.

## 🚀 Funcionalidades

- 📡 Leitura de dados de sensores via protocolo MODBUS
- 📁 Armazenamento em banco de dados SQLite3
- 🔄 API RESTful com FastAPI para consulta dos dados
- 🌐 Interface web com gráficos atualizados em tempo real (JavaScript + Chart.js)
- 🤖 Regras de automação locais:
  - Ar-condicionado liga se temperatura > 30°C
  - Lâmpadas ligam se houver movimento e baixa luminosidade
  - Umidificador ativa se umidade < 40%
  - Ventilador ativa se temperatura > 28°C **e** umidade > 70%
  - Alarme liga quando há a presença detectada.
- 🖼️ Ícones dos atuadores mudam dinamicamente conforme o estado
- 📱 Layout responsivo adaptado a dispositivos móveis

## 📂 Estrutura do Projeto

```
.
├── api/
│   ├── ihm_api.py           # API FastAPI
│   ├── house_dao.py         # Acesso ao SQLite
│   ├── cliente.py           # Cliente MODBUS
│   └── house_database.db    # Cliente MODBUS
├── interface/
│   ├── index.html           # Dashboard Web
│   ├── script.js            # Lógica e integração JS
│   ├── style.css            # Estilo da interface
│   └── icons/               # Ícones PNG dos atuadores
├── servidor/
│   ├── servidor.py          # Servidor MODBUS simulado
│   └── main.py              # Inicialização do servidor
```

## ▶️ Como executar

1. **Inicie o servidor MODBUS simulado**
   ```bash
   python servidor/main.py
   ```

2. **Inicie a API FastAPI**
   ```bash
   python.exe ihm_api.py
   ```

3. **Abra a interface web**
   - Use Live Server (VS Code) ou
   - Rode um servidor simples:
     ```bash
     cd interface
     python -m http.server 5500
     ```
   - Acesse: `http://localhost:5500`

## 🛠️ Tecnologias usadas

- Python 3
- FastAPI
- SQLite3
- JavaScript (Chart.js, Fetch API)
- HTML5 + CSS3
- MODBUS (via pymodbus)
- VS Code + Live Server

## 📸 Interface

![image](https://github.com/user-attachments/assets/ed51480c-1aa6-478c-bb5b-73442e3b55bf)

## 📃 Licença

Este projeto é de uso acadêmico/educacional. Sinta-se à vontade para adaptar ou expandir.
