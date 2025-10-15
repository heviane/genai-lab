# Serviços de Inteligência Artificial da AWS

Aqui está um resumo simples, objetivo e bem fundamentado sobre cada um:

| Serviço AWS | O Que É (Resumo) | Principal Função |
| :--- | :--- | :--- |
| **Amazon Bedrock** | Uma plataforma (sem servidor) para **construir aplicações de IA Generativa** usando modelos de fundação (LLMs, modelos de imagem, etc.) de diferentes fornecedores (Amazon, Anthropic, Stability AI, Cohere, etc.). | Oferecer acesso fácil e seguro a uma **coleção diversa de modelos de IA** em um único lugar, simplificando o desenvolvimento de GenAI. |
| **PartyRock** | Uma **plataforma de playground e prototipagem** baseada no Bedrock, projetada para usuários sem experiência em programação. | Permitir que qualquer pessoa **crie rapidamente aplicações GenAI simples** (como geradores de texto, planners, etc.) arrastando e soltando blocos de função. |
| **Amazon Nova** | O **modelo de fundação (LLM)** de geração mais recente e avançado desenvolvido pela Amazon. | Servir como o **LLM proprietário de alto desempenho da Amazon** para tarefas complexas de raciocínio, codificação e geração de texto, sendo um concorrente direto de modelos como GPT-4 e Gemini. |
| **AgentCore** | Uma **estrutura (framework)** para a orquestração e criação de **Agentes de IA** (AI Agents) complexos, dentro da plataforma Bedrock. | Automatizar tarefas complexas de múltiplos passos (como reservas de viagens ou análise de relatórios) **conectando LLMs a sistemas e bancos de dados externos** de forma confiável e segura. |

**Em essência**:

- **Bedrock** é a plataforma;
- **Nova** é o modelo principal dentro dela;
- **PartyRock** é a área de testes do Bedrock;
- **AgentCore** é a ferramenta para construir ações complexas no Bedrock.
