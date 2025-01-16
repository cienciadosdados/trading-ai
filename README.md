# AI Trading Agent 🤖
Este é um agente financeiro de IA como prova de conceito. O objetivo deste projeto é explorar o uso de IA para pesquisa de investimentos. Este projeto é destinado apenas para fins educacionais e não é indicado para negociações ou investimentos reais.

👋 Demo: Você pode acessar uma demonstração ao vivo deste projeto aqui.

<img width="1709" alt="Captura de tela em 2025-01-06 às 17:53:59" src="https://github.com/user-attachments/assets/7ef1729b-f2e1-477c-99e2-1184c1bfa1cd" />
Aviso Legal
Este projeto é apenas para fins educacionais e de pesquisa.

Não é indicado para negociações ou investimentos reais.
Nenhuma garantia ou responsabilidade é fornecida.
Desempenhos passados não indicam resultados futuros.
O criador não assume responsabilidade por perdas financeiras.
Consulte um consultor financeiro para decisões de investimento.
Ao utilizar este software, você concorda em usá-lo exclusivamente para fins de aprendizado.

Tabela de Conteúdo 📖
Recursos
Configuração
Uso
Dados Financeiros
Implemente Sua Própria Versão
Recursos 🌟
AI SDK
API unificada para geração de texto, objetos estruturados e chamadas de ferramentas com LLMs.
Hooks para construir interfaces de chat e geração dinâmicas.
Suporte a OpenAI (padrão), Anthropic, Cohere e outros provedores de modelos.
Financial Datasets API
Acesso a dados do mercado de ações em tempo real e históricos.
Dados otimizados para agentes financeiros de IA.
Cobertura total do mercado com mais de 30 anos de dados financeiros.
Documentação disponível aqui.
shadcn/ui
Estilização com Tailwind CSS.
Componentes primitivos do Radix UI para acessibilidade e flexibilidade.
Configuração 🛠️
bash
Copiar
Editar
git clone https://github.com/virattt/ai-financial-agent.git
cd ai-financial-agent
Se você não possui o npm instalado, faça o download aqui.

Instale o pnpm (caso ainda não esteja instalado):
bash
Copiar
Editar
npm install -g pnpm
Instale as dependências:
bash
Copiar
Editar
pnpm install
Configure suas variáveis de ambiente:
bash
Copiar
Editar
# Crie um arquivo .env para suas chaves de API
cp .env.example .env
Defina as chaves de API no arquivo .env:

makefile
Copiar
Editar
# Obtenha sua chave de API OpenAI em https://platform.openai.com/
OPENAI_API_KEY=sua-chave-de-api-openai

# Obtenha sua chave de API Financial Datasets em https://financialdatasets.ai/
FINANCIAL_DATASETS_API_KEY=sua-chave-de-api-financial-datasets

# Obtenha sua chave de API LangSmith em https://smith.langchain.com/
LANGCHAIN_API_KEY=sua-chave-de-api-langsmith
LANGCHAIN_TRACING_V2=true
LANGCHAIN_PROJECT=ai-financial-agent
Nota: Não comprometa o arquivo .env no repositório, pois ele expõe segredos que permitem a outros acessar suas contas de OpenAI e provedores de autenticação.

Se desejar implantar sua própria versão do Agente Financeiro de IA em produção, você precisará vincular sua instância local às contas do Vercel e GitHub.

Instale o CLI do Vercel: npm i -g vercel
Vincule a instância local às contas do Vercel e GitHub (cria o diretório .vercel): vercel link
Baixe suas variáveis de ambiente: vercel env pull
Uso 🎮
Após concluir as etapas acima, execute o seguinte comando para iniciar o servidor de desenvolvimento:

bash
Copiar
Editar
pnpm dev
O template do seu app estará rodando em localhost:3000.

Dados Financeiros
Este template utiliza a Financial Datasets API como provedora de dados financeiros. A API é projetada especificamente para agentes financeiros de IA e LLMs.

A Financial Datasets API fornece dados do mercado de ações em tempo real e históricos, cobrindo 100% do mercado dos EUA nos últimos 30 anos.

Os dados incluem demonstrações financeiras, preços de ações, dados de opções, transações de insiders, propriedade institucional e muito mais. Você pode saber mais sobre a API na documentação aqui.

Nota: Os dados são gratuitos para AAPL, GOOGL, MSFT, NVDA e TSLA.

Se não quiser usar a Financial Datasets API, é fácil alternar para outro provedor de dados modificando algumas linhas de código.

Implemente Sua Própria Versão 🚀
Você pode implantar sua própria versão do Agente Financeiro de IA em produção pelo Vercel com um clique:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fvirattt%2Fai-financial-agent&env=AUTH_SECRET,OPENAI_API_KEY&envDescription=Learn%20more%20about%20how%20to%20get%20the%20API%20Keys%20for%20the%20application&envLink=https%3A%2F%2Fgithub.com%2Fvercel%2Fai-financial-agent%2Fblob%2Fmain%2F.env.example&demo-title=AI%20Financial%20Agent&demo-description=An%20open-source%20financial%20agent%20chat%20template%20built%20with%20the%20AI%20SDK%20by%20Vercel%20and%20Financial%20Datasets%20API.&demo-url=https%3A%2F%2Fchat.vercel.ai&stores=[{%22type%22:%22postgres%22},{%22type%22:%22blob%22}])


