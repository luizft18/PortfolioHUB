# PortfolioHUB
Compêndio dos componentes do meu portfólio.

O **PortfolioHUB** é uma plataforma centralizada projetada para exibir, gerenciar e documentar de forma estruturada minha trajetória acadêmica e profissional, competências, experiências e projetos realizados. 

Este ecossistema foi desenvolvido como o entregável consolidado da matéria de **Bootcamp I** do curso de **Análise e Desenvolvimento de Sistemas** no **Centro Universitário de Brasília (CEUB)**. Toda a sua arquitetura de implantação, governança de código e segurança foi realizada com o apoio e co-pilotagem da IA **Google Gemini**.

---

## 📂 Estrutura do Repositório

O repositório está organizado de forma modular para garantir a separação de conceitos (Clean Code) e fácil navegabilidade:

*   `📂 src/` - Código-fonte e arquivos estruturais da plataforma PortfolioHUB.
*   `📂 docs/` - Documentação acadêmica, relatórios e arquivos PDFs das entregas do semestre.
*   `📂 public/` - Arquivos de acesso público.

---

## 🛠️ Tecnologias e Ferramentas Utilizadas

*   **Versionamento Local:** Git
*   **Hospedagem e Governança:** GitHub
*   **Hospedagem Estática:** GitHub Pages
*   **Ferramenta de Apoio e Guia de Engenharia:** Google GEMINI

---

## 🔐 Gestão de Usuários e Políticas de Segurança

A implantação do PortfolioHUB priorizou a segurança da informação e o controle estrito de acessos, seguindo as diretrizes sugeridas pelo assistente Google Gemini:

1.  **Controle de Acesso Baseado em Funções (RBAC):**
    *   **Proprietário/Administrador (Luiz Felipe):** Permissões totais de escrita, configuração de ambiente e gerenciamento de deploys.
    *   **Leitores (Avaliadores/Recrutadores):** Permissões estritas de leitura (*Read-only*) do código-fonte público, garantindo a integridade do código sem riscos de alterações externas não autorizadas.
2.  **Proteção de Dados Sensíveis:**
    *   Utilização rigorosa de um arquivo `.gitignore` configurado para mitigar o vazamento de chaves de API, tokens de acesso pessoal (PAT), variáveis de ambiente (`.env`) ou dependências locais pesadas (`node_modules/`).
3.  **Segurança Automatizada:**
    *   **Dependabot Alerts:** Ativado para varredura contínua e automatizada de vulnerabilidades em bibliotecas de terceiros.
    *   **Secret Scanning:** Configurado para interceptar e bloquear ativamente qualquer tentativa de *push* que contenha credenciais expostas de forma acidental.

---

## 🔄 Fluxo de Trabalho e Controle de Versão (Branching Strategy)

Para garantir a estabilidade do ambiente de produção e simular um cenário real de mercado, a governança de código do PortfolioHUB adota o seguinte fluxo de trabalho:

*   **Branch `main`:** É a ramificação de produção. Ela contém exclusivamente o código testado, homologado e estável. Esta branch possui **Regras de Proteção Ativas** (*Branch Protection Rules*), impedindo commits diretos e exigindo a abertura de um *Pull Request* (PR) para qualquer alteração.
*   **Branch `develop`:** É a ramificação utilizada no dia a dia para o desenvolvimento de novas funcionalidades, ajustes na interface e integração dos projetos passados.