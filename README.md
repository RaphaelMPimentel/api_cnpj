# Automação de Prospecção via CNPJ

Este projeto foi desenvolvido para automatizar o processo de coleta de informações de empresas a partir de CNPJs usando o portal da Assertiva Localize. Antes da automação, o time de prospecção realizava esse processo manualmente, o que tomava cerca de **10 minutos por CNPJ**, limitando a produtividade para **20 a 30 CNPJs por dia**. 
> Agora, com a API criada, uma planilha com **até 500 CNPJs** pode ser processada automaticamente, otimizando significativamente o tempo do time.

## Benefícios da Automação
- **Redução drástica de tempo**: de 10min/CNPJ para segundos.
- **Volume de dados ampliado**: de ~20 CNPJs/dia para 500.
- **Foco no que importa**: o time atua diretamente na abordagem dos leads, e não na coleta de dados.

## Tecnologias Utilizadas
- Python
- Selenium
- Pandas
- Regex

## Informações Extraídas
Para cada CNPJ consultado, são extraídas as seguintes informações:
- Nome Fantasia
- Situação Cadastral (ex: ativa, baixada)
- Telefones
- Endereço
- Sócios
- E-mail

Além disso, os CNPJs com **situação "baixada"** ou **sem formas de contato** são automaticamente filtrados.

## Como Funciona
1. O script acessa o portal Assertiva Localize.
2. Lê uma planilha com a lista de CNPJs.
3. Para cada CNPJ, coleta os dados diretamente da página.
4. Armazena os dados em um dicionário.
5. Exporta os resultados em um novo arquivo `.xlsx`.

## Estrutura do Projeto
```
├── chromedriver
├── Listagem.Xlsx         # Planilha com os CNPJs para consulta
├── resultados_assertiva_final.xlsx  # Planilha gerada com os dados
├── script.py             # Script principal da automação
└── README.md             # Este arquivo
```

## Observações
- É necessário realizar login manualmente no portal no início da execução.
- O script exige o `chromedriver` compatível com sua versão do Chrome.

## Ideias Futuras
- Agendamento da automação para rodar diariamente.
- Integração com banco de dados.
- Painel com métricas de conversão por lead extraído.

### Autor
Desenvolvido por Raphael Pimentel. Em caso de dúvidas ou sugestões, entre em contato!
**Este projeto foi criado com o objetivo de apoiar o time comercial, otimizando tempo e melhorando a eficiência do processo de prospecção.**
