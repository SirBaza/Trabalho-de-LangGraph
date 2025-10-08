# Trabalho de LangGraph - Projetos de Agentes de IA

Este repositório contém projetos educacionais de agentes de IA desenvolvidos com LangGraph.

## Projetos

### 1. AI Fitness Coach (Projeto Principal)

Um agente de IA capaz de gerar planos de treino de musculação personalizados e detalhados. O agente é robusto, interativo e utiliza arquitetura baseada em LangGraph para orquestrar o fluxo de trabalho. A solução integra ferramentas externas para pesquisa na web, cálculos matemáticos e RAG (Retrieval Augmented Generation).

**Arquivo:** `AI-Fitness-Coach.ipynb`

**Características:**
- Coleta de dados do usuário (idade, peso, altura, objetivo)
- Geração de 12 treinos personalizados
- Integração com Tavily Search para busca na web
- Sistema RAG com Pinecone para base de conhecimento
- Cálculos de IMC, TMB e gasto calórico
- Interface interativa com ipywidgets

**Documentação:**
- [README detalhado](README-FITNESS-COACH.md)
- [Documentação técnica](DOCUMENTACAO-TECNICA.md)
- [Roteiro para vídeo](ROTEIRO-VIDEO.md)

### 2. Exemplos Básicos

**01-LangGraphBasico.ipynb**
- Introdução ao LangGraph
- Conceitos fundamentais
- Primeiro grafo simples

**02-LangGraphDecisao.ipynb**
- Grafos com decisões condicionais
- Fluxos alternativos
- Lógica de roteamento

**03-LangGraphTools.ipynb**
- Integração de ferramentas externas
- Tool calling
- Agentes com múltiplas ferramentas

**LangGraphEducação.ipynb**
- Exemplo aplicado à educação
- Conceitos avançados

## Instalação Rápida

### Pré-requisitos
- Python 3.10 ou superior
- pip

### Passo 1: Clone o repositório
```bash
git clone https://github.com/SirBaza/Trabalho-de-LangGraph.git
cd Trabalho-de-LangGraph
```

### Passo 2: Crie um ambiente virtual
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# ou
venv\Scripts\activate  # Windows
```

### Passo 3: Instale as dependências
```bash
pip install -r requirements.txt
```

### Passo 4: Configure as variáveis de ambiente
```bash
cp .env.example .env
# Edite o arquivo .env com suas chaves de API
```

### Passo 5: Execute o notebook
```bash
jupyter notebook AI-Fitness-Coach.ipynb
```

## Chaves de API Necessárias

Para o projeto AI Fitness Coach, você precisará:

1. **GROQ_API_KEY** - Obtenha em: https://console.groq.com
2. **PINECONE_API_KEY** - Obtenha em: https://www.pinecone.io
3. **TAVILY_API_KEY** - Obtenha em: https://tavily.com

Todas as chaves têm planos gratuitos disponíveis.

## Estrutura do Repositório

```
Trabalho-de-LangGraph/
├── AI-Fitness-Coach.ipynb          # Projeto principal
├── README.md                       # Este arquivo
├── README-FITNESS-COACH.md         # Documentação do projeto principal
├── DOCUMENTACAO-TECNICA.md         # Documentação técnica detalhada
├── ROTEIRO-VIDEO.md               # Roteiro para vídeo de demonstração
├── requirements.txt               # Dependências Python
├── .env.example                   # Exemplo de variáveis de ambiente
├── .gitignore                     # Arquivos ignorados pelo git
├── 01-LangGraphBasico.ipynb      # Exemplo básico
├── 02-LangGraphDecisao.ipynb     # Exemplo com decisões
├── 03-LangGraphTools.ipynb       # Exemplo com ferramentas
└── LangGraphEducação.ipynb       # Exemplo educacional
```

## Tecnologias Utilizadas

- **LangGraph**: Orquestração de agentes
- **LangChain**: Framework para LLMs
- **Groq**: Inferência rápida de LLMs
- **Pinecone**: Vector database para RAG
- **Tavily**: Busca na web
- **HuggingFace**: Modelos de embedding
- **Jupyter**: Ambiente de desenvolvimento interativo

## Funcionalidades do AI Fitness Coach

1. **Coleta e validação de dados**
   - Idade, peso, altura, sexo
   - Frequência de treino (2-6 dias/semana)
   - Objetivo (hipertrofia, emagrecimento, força, condicionamento)

2. **Análise física**
   - Cálculo de IMC
   - Taxa metabólica basal
   - Gasto calórico estimado
   - Recomendações nutricionais

3. **Geração de treinos**
   - 12 treinos completos e distintos
   - 4-6 exercícios por treino
   - Séries e repetições personalizadas
   - Dicas de execução

4. **Base de conhecimento**
   - Mais de 50 exercícios catalogados
   - Princípios de treinamento
   - Divisões por periodicidade
   - Técnicas e progressões

## Como Usar

### Modo Formulário
1. Execute o notebook `AI-Fitness-Coach.ipynb`
2. Preencha o formulário interativo
3. Clique em "Gerar Plano de Treino"
4. Aguarde a geração (1-2 minutos)
5. Visualize seu plano personalizado

### Modo Chat
1. Use a função `run_chat()` no final do notebook
2. Faça perguntas sobre treinos e exercícios
3. O agente consultará automaticamente as ferramentas necessárias

## Exemplos

### Exemplo 1: Hipertrofia - 4 dias/semana
```
Entrada:
- Idade: 25 anos
- Peso: 75 kg
- Altura: 1.75 m
- Objetivo: Hipertrofia
- Periodicidade: 4 dias/semana

Saída:
- 12 treinos (3 semanas de ABCD)
- Foco em 8-12 repetições
- Volume moderado-alto
```

### Exemplo 2: Emagrecimento - 5 dias/semana
```
Entrada:
- Idade: 30 anos
- Peso: 85 kg
- Altura: 1.70 m
- Objetivo: Emagrecimento
- Periodicidade: 5 dias/semana

Saída:
- 12 treinos com mais repetições
- Descansos curtos (30-60s)
- Circuitos e superséries
```

## Contribuindo

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch (`git checkout -b feature/MinhaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona feature'`)
4. Push para a branch (`git push origin feature/MinhaFeature`)
5. Abra um Pull Request

## Licença

Este projeto é desenvolvido para fins educacionais.

## Autor

Desenvolvido como trabalho acadêmico para a disciplina de LangGraph.

## Links Úteis

- [Documentação LangGraph](https://langchain-ai.github.io/langgraph/)
- [Documentação LangChain](https://python.langchain.com/)
- [Groq API](https://console.groq.com/docs)
- [Pinecone](https://docs.pinecone.io/)
- [Tavily Search](https://tavily.com)

## Demonstração

Um vídeo de demonstração estará disponível em breve mostrando todas as funcionalidades do AI Fitness Coach.

## Contato

Para dúvidas ou sugestões, abra uma issue no repositório.

---

Desenvolvido com LangGraph
