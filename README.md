# 🌍 ETL Weather Tracker
> Pipeline automático de dados integrado com Google Sheets e Open-Meteo API.

Este projeto foi desenvolvido para demonstrar um fluxo prático de **Engenharia de Dados (ETL)**. Ele extrai dinamicamente coordenadas geográficas cadastradas em uma planilha do Google Sheets, realiza chamadas assíncronas para a API de clima **Open-Meteo**, processa as informações em tempo real e exibe as temperaturas atuais de cada localidade.

---

## 🛠️ Tecnologias Utilizadas

| Tecnologia | Função no Projeto |
| :--- | :--- |
| **Python 3** | Linguagem principal do pipeline |
| **Pandas** | Leitura, manipulação e estruturação dos dados extraídos |
| **Requests** | Consumo e integração com a API HTTP REST |
| **Google Sheets** | Armazenamento de origem dos dados (Data Source) |
| **Open-Meteo API** | Provedor de dados meteorológicos globais em tempo real |

---

## 📂 Estrutura do Fluxo de Dados (ETL)

1. **Extração (Extract):** 
   O script lê os dados brutos em formato CSV diretamente de um link de exportação pública de uma planilha do Google Sheets.
   
2. **Transformação (Transform):**
   Com o Pandas, os dados são estruturados e as colunas de `Latitude`, `Longitude` e `Nome do local` são mapeadas para cada ponto.

3. **Carga/Consulta (Load/Query):**
   Para cada registro, é feita uma requisição dinâmica via protocolo HTTP GET para o endpoint da Open-Meteo API, retornando as condições climáticas exatas do momento.

---

## 🚀 Como Executar o Projeto

### Pré-requisitos
Você precisará ter o Python instalado ou rodar o projeto diretamente em um ambiente de Notebook (como o Google Colab ou Jupyter).

Instale as dependências necessárias:
```bash
pip install pandas requests
Executando o Script
Clone este repositório em sua máquina:
git clone https://github.com/seu-usuario/seu-repositorio.git
Abra o arquivo .ipynb no seu editor de preferência (VS Code, Jupyter, ou faça o upload no Google Colab).
Execute as células sequencialmente para ver o pipeline extraindo os dados e consultando as temperaturas atualizadas em tempo real.
📈 Próximos Passos (Roadmap)
Persistência de dados: Gravar os resultados finais de temperatura de volta em uma nova guia da planilha ou em um arquivo local CSV/JSON.
Adicionar tratamento de exceções para garantir resiliência caso a API ou a planilha fiquem instáveis.
Criar visualizações gráficas de temperatura para análises comparativas.
Desenvolvido como projeto de portfólio para demonstrar habilidades em consumo de APIs e manipulação de dados com Python.
