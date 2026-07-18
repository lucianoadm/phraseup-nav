# PhraseUp — Refinador de Linguagem 🧠✨

**Módulo Cognitivo do Ecossistema LexOS**  
Versão: `1.1.0 - Focus & Zero Trust Engine`

O **PhraseUp** é uma interface de processamento linguístico restrito e determinístico. Ele atua como um motor de refinamento que recebe frases de rascunho (inputs informais ou brutos) e utiliza modelos fundacionais de inteligência artificial para retornar variáveis otimizadas (ex: tom profissional, tom assertivo/positivo), garantindo que a factualidade da mensagem original permaneça inalterada.

---

## 🚀 Principais Funcionalidades

*   **Multi-Gateway API:** Suporte nativo e roteamento direto via requisições do lado do cliente para os principais provedores de IA do mercado:
    *   Anthropic (Claude 3)
    *   OpenAI (GPT-4o)
    *   Google Gemini (Gemini 2.5 Flash)
*   **Zero Trust Engine & CoVe:** Utiliza engenharia de prompt avançada (Chain of Verification) para forçar o modelo a responder estritamente em um formato JSON pré-definido, evitando alucinações de formatação ou texto não solicitado.
*   **Armazenamento Seguro (Client-Side):** As chaves de API (`API Keys`) são mantidas no `localStorage` do navegador do usuário, garantindo privacidade e segurança sem a necessidade de um banco de dados centralizado.
*   **Vault (Biblioteca Local):** Sistema integrado para salvar frases refinadas favoritas. Permite busca em tempo real, cópia rápida para a área de transferência e exclusão.
*   **Exportação de Dados:** Funcionalidade de exportação de todo o histórico do Vault para o formato `.csv`, ideal para auditoria, relatórios ou treinamento futuro de modelos.
*   **UI/UX "Deep Focus":** Interface minimalista baseada em ondas cerebrais Alfa/Teta. Fundo escuro (`dark mode` nativo), acentos em tons neon contidos (roxo, verde e âmbar) e design 100% responsivo.

---

## 🛠️ Stack Tecnológico

O aplicativo foi desenvolvido com foco em máxima velocidade, leveza e ausência de dependências externas complexas:

*   **HTML5:** Estrutura semântica.
*   **CSS3:** Estilização nativa com variáveis dinâmicas (CSS Custom Properties), animações fluidas (`@keyframes`) e tipografia importada via Google Fonts (Instrument Serif e DM Sans).
*   **Vanilla JavaScript (ES6+):** Lógica de roteamento de APIs, manipulação do DOM, gestão de estado via Local Storage e processamento assíncrono (Async/Await, Fetch API).

---

## ⚙️ Instalação e Uso

Por ser uma aplicação construída puramente em tecnologias web nativas (Client-Side), **não é necessária nenhuma instalação ou build de servidor** (Node.js, npm, etc).

1.  **Clone ou baixe** este arquivo HTML (`index.html`).
2.  **Abra o arquivo** diretamente em qualquer navegador web moderno (Chrome, Edge, Firefox, Safari).
3.  **Configuração de Gateway:**
    *   No painel superior "Configuração de Gateway API", selecione o provedor desejado (Anthropic, OpenAI ou Google Gemini).
    *   Insira a sua chave de API (`API Key`) correspondente ao provedor escolhido.
    *   Clique em **Autorizar**.
4.  **Refinamento:**
    *   Digite um texto informal na caixa de entrada inferior (ou clique em um dos atalhos rápidos/chips).
    *   Pressione `Enter` ou o botão de enviar.
    *   O sistema processará a requisição e retornará cards com diferentes tons e explicações.
5.  **Biblioteca:**
    *   Clique em "⭐ Salvar no Vault" em qualquer sugestão.
    *   Acesse o botão "📚" no canto inferior direito para visualizar, buscar ou exportar suas frases salvas.

---

## 🧠 Protocolo Cognitivo (Under the Hood)

O sistema opera sob uma restrição severa de output (Protocolo LexOS). O prompt de sistema força as IAs a atuarem de forma analítica e não conversacional:

```json
// Exemplo do formato exigido pelo Zero Trust Engine
{
  "contexto": "Profissional",
  "v1": { "tag": "Refinamento Profissional", "frase": "...", "motivo": "..." },
  "v2": { "tag": "Tom Otimizado", "frase": "...", "motivo": "..." }
}