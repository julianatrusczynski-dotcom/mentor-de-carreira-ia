# Mentor de Carreira com IA (Google Colab + OpenRouter)

Projeto prático inspirado nos tópicos do curso: conectar Python a modelos de IA via API, proteger chaves, usar system prompts e guardrails, testar respostas e entender tokens/custos.

## Objetivo
Criar um mentor de carreira conversacional que ajude a pessoa a explorar caminhos profissionais, identificar habilidades, organizar objetivos e montar planos de ação. O protótipo usa OpenRouter como gateway de modelos e pode selecionar modelos com opção gratuita quando disponíveis.

## Conteúdo alinhado às aulas
- **IA no Colab:** preparar o ambiente, conectar API, fazer uma primeira solicitação.
- **Segurança de código e chaves de API:** usar `Secrets` do Colab; nunca publicar chaves; revogar se expostas.
- **System prompt e GuardRails:** definir papel, limites, formato de resposta e regras contra invenção de informações.
- **Tokens:** consultar a contagem de tokens reportada pela API, quando disponível, e explicar que tokens afetam custos/limites.
- **Desafio:** conversar com o mentor, pedir orientação para um objetivo e avaliar/ajustar as respostas.

## Como executar
1. Abra `notebooks/mentor_de_carreira.ipynb` no Google Colab (ou faça upload do notebook).
2. No Colab, abra **Secrets** (ícone de chave) e crie `OPENROUTER_API_KEY` com sua chave. Habilite o acesso do notebook.
3. Execute as células de cima para baixo.
4. Na célula de seleção de modelo, escolha um modelo que esteja disponível e, se quiser testar sem cobrança, procure os modelos marcados como gratuitos (`:free`). A disponibilidade pode mudar.
5. Faça perguntas ao mentor e confira o uso de tokens na saída.


## Segurança
- Não coloque a chave em uma célula, no README, em commits, prints ou mensagens de erro.
- Se a chave for exposta, revogue-a no painel do provedor e crie outra.
- Este protótipo não substitui aconselhamento profissional, psicológico, financeiro ou jurídico.
- Evite inserir dados pessoais ou confidenciais.

## Estrutura
```
ia-mentor-carreira/
├── README.md
├── requirements.txt
├── .gitignore
├── prompts/
│   └── mentor_system_prompt.txt
└── notebooks/
    └── mentor_de_carreira.ipynb
```

## Próximas melhorias
- Interface web simples (Streamlit)
- Histórico de conversas com opção de apagar
- Exportar plano de carreira para Markdown
- Guardrails adicionais e testes de prompt
- Monitorar custo, limites e erros de API

## Licença
MIT — veja `LICENSE`.
