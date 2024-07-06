# Teste Técnico - Analista de Integração e Suporte ao Cliente

## Parte 1: Uso da API

### Caso fictício
Um colaborador da Petiko precisa obter dados de previsão do tempo para otimizar o planejamento de entrega de produtos. A previsão é obtida algumas vezes ao dia para garantir um planejamento preciso.

### 1.2 Configuração da Solicitação no Postman

- **Método:** GET
- **URL:** `https://api.openweathermap.org/data/2.5/forecast`
- **Parâmetros:**
  - `q`: Nome da cidade (por exemplo, q=São Paulo)
  - `appid`: Chave da API (9e07ac36e69952cc8f25802a5321059a)
  - `units`: Unidade de medida (por exemplo, units=metric para obter a temperatura em Celsius)
- **Headers:** Nenhum header adicional é necessário para esta solicitação.

### 1.3 Execução da Solicitação

No Postman, configure a URL da solicitação como:
https://api.openweathermap.org/data/2.5/forecast?q=São%20Paulo&appid=chave_api_weather_api&units=metric

markdown
Copiar código
Clique em "Send" para enviar a solicitação.

**Obs:** Para obter uma chave de API e ter um retorno adequado dos dados, é necessário ter uma conta no site oficial do OpenWeather.

### 1.4 Documentação da Solicitação

1. Abra o Postman e crie uma nova solicitação.
2. Configure o método como GET.
3. Insira a URL `https://api.openweathermap.org/data/2.5/forecast`.
4. Adicione os parâmetros:
   - `q`: `São Paulo`
   - `appid`: `chave_api_fornecida_no_site`
   - `units`: `metric`
5. Clique em "Send".
6. A resposta deve ser algo como:

{
  "cod": "200",
  "message": 0,
  "cnt": 40,
  "list": [
    {
      "dt": 1596564000,
      "main": {
        "temp": 22.3,
        "feels_like": 21.8,
        "temp_min": 22.3,
        "temp_max": 22.3,
        "pressure": 1013,
        "sea_level": 1013,
        "grnd_level": 1009,
        "humidity": 83,
        "temp_kf": 0
      },
      "weather": [
        {
          "id": 801,
          "main": "Clouds",
          "description": "few clouds",
          "icon": "02d"
        }
      ],
      "clouds": {
        "all": 20
      },
      "wind": {
        "speed": 3.4,
        "deg": 150
      },
      "visibility": 10000,
      "pop": 0,
      "sys": {
        "pod": "d"
      },
      "dt_txt": "2020-08-04 03:00:00"
    },
    ...
  ],
  "city": {
    "id": 3448439,
    "name": "São Paulo",
    "coord": {
      "lat": -23.5475,
      "lon": -46.6361
    },
    "country": "BR",
    "population": 10021295,
    "timezone": -10800,
    "sunrise": 1596532300,
    "sunset": 1596573930
  }
}

## Parte 2: Simulação de Atendimento ao Cliente

### Cenário
Um colaborador da Petiko está enfrentando dificuldades para acessar relatórios no ERP.

### Simulação

**Mensagem do Cliente:** “Não consigo acessar os relatórios no sistema ERP, está dando erro.”

**Resposta Simulada:**

Olá [Nome do Cliente],

Entendo que você está tendo dificuldades para acessar os relatórios. Vamos resolver isso juntos.

Primeiramente, por favor, siga estes passos:

Limpe o cache do seu navegador. Para isso, vá para as configurações do navegador e procure a opção de limpar dados de navegação. Certifique-se de selecionar a opção de limpar o cache.

Tente acessar o sistema ERP usando um navegador diferente, como Google Chrome ou Mozilla Firefox.

Caso o problema persista, por favor, me avise para que possamos investigar mais a fundo e encontrar uma solução definitiva.

Agradeço pela sua paciência e compreensão.

Atenciosamente,

[Victor].


## Parte 3: Resolução de Problemas Técnicos

### Problema Técnico Comum
"Erro ao gerar relatórios no ERP."

#### Diagnóstico

- Verifique se o usuário tem as permissões necessárias para acessar os relatórios.
- Confirme se o servidor de relatórios está ativo.
- Cheque se há atualizações pendentes no sistema ERP.

#### Resolução

**Ajustar Permissões:**
- Verifique as permissões necessárias no painel de administração do ERP.

**Reiniciar e Aplicar Atualizações dos Serviços:**
- Reinicie o servidor de relatórios se necessário.
- Verifique e aplique todas as atualizações do sistema ERP.

## Parte 4: Comunicação por E-mail

### E-mail de Resposta ao Cliente

**Cliente:** "Estou enfrentando problemas ao tentar acessar os relatórios no sistema ERP."

**Resposta por E-mail:**

Olá [Nome do Cliente],

Entendo que você está enfrentando um problema ao gerar relatórios no ERP. Para resolver isso, por favor, siga os passos abaixo:

Verifique se você tem as permissões necessárias para acessar os relatórios. - No painel de administração do ERP, vá até a seção de gerenciamento de usuários e confirme que você tem as permissões de "Visualização de Relatórios".

Tente limpar o cache do seu navegador ou usar um navegador diferente, como Google Chrome ou Mozilla Firefox.

Verifique se o servidor de relatórios está ativo e reinicie o serviço, se necessário.

No servidor, você pode usar o comando:

bash
Copiar código
sudo systemctl restart report-server
Certifique-se de que todas as atualizações do sistema ERP foram aplicadas corretamente. No painel de administração do ERP, vá até a seção de atualizações e confirme que não há atualizações pendentes. Se houver, aplique-as e reinicie o sistema.
Caso essas soluções não funcionem, por favor, me avise para que possamos investigar mais a fundo.

Agradeço pela sua paciência e compreensão.

Atenciosamente,

[Victor].