# 1CCA-Python-FIAP-2026
## Pipeline de Análise de Carga Elétrica ONS com IA (Gemini)

Pipeline automatizada em Python para consumo, tratamento e análise estatística de dados de carga elétrica do **Operador Nacional do Sistema Elétrico (ONS)** para o estado de São Paulo, integrada à API do **Google Gemini** para geração automática de relatórios técnicos.

---

## Objetivo
Transformar dados brutos de demanda elétrica obtidos via API REST do ONS em relatórios operacionais completos, automatizando todo o fluxo desde a coleta até a exportação final.

---

## Funcionalidades
- **Consumo de Dados:** Requisição e ingestão automatizada via API REST do ONS.
- **Tratamento de Dados:** Validação e conversão de tipos com Pandas (`Data_Hora`, `Carga_MW`).
- **Estatística Descritiva:** Cálculo de média, mediana, pico máximo, carga mínima e amplitude.
- **Análise de Estresse:** Identificação de momentos de alta demanda (limiar de 90% da carga máxima).
- **Visualização Gráfica:** Geração de série temporal e histograma com Matplotlib.
- **Inteligência Artificial:** Integração com a API do Gemini (`gemini-2.5-flash`) para emissão de parecer técnico.
- **Exportação:** Salvamento e download automático do relatório em arquivos `.md` e `.txt`.

---

## Tecnologias Utilizadas
- **Linguagem:** Python 3
- **Ambiente:** Google Colab
- **Manipulação de Dados:** Pandas, NumPy
- **Visualização:** Matplotlib
- **Inteligência Artificial:** `google-generativeai` (API Gemini)

---

## Configuração da Chave de API
Para executar o envio ao Gemini (Desafio 8):
1. Crie uma chave gratuita no [Google AI Studio](https://aistudio.google.com/app/apikey).
2. No Google Colab, vá na aba **Secrets** 
3. Adicione um novo segredo:
   - **Name:** `GEMINI_API_KEY`
   - **Value:** *Sua chave gerada no AI Studio*
4. Ative o botão **Notebook access**.

---

## Estrutura do Projeto
O notebook está organizado em **9 Desafios sequenciais**:
1. Ingestão e Requisição de Dados (ONS)
2. Padronização e Tratamento da Base (Pandas)
3. Cálculo das Estatísticas Descritivas
4. Filtro e Análise de Alta Demanda (>90%)
5. Comparação entre Critérios de Consumo
6. Criação dos Gráficos (Série Temporal e Histograma)
7. Estruturação do Resumo Executivo
8. Chamada da API do Gemini e Geração do Relatório
9. Exportação e Download dos Arquivos Finalizados

---

## 📄 Licença
Este projeto foi desenvolvido para fins acadêmicos sob a licença [MIT](LICENSE).
