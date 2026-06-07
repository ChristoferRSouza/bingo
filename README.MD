# 🎲 Bingo Interativo com Patrocinadores

Um sistema de painel de bingo digital e interativo, desenvolvido com tecnologias web padrão para rodar diretamente no navegador. Ideal para eventos presenciais, projeções em telões ou transmissões ao vivo (via OBS Studio), permitindo vincular marcas e logotipos de patrocinadores a cada número sorteado.

---

## 🚀 Funcionalidades

* **Mapeamento de Patrocinadores:** Cada uma das 75 pedras exibe o nome e a logo de um apoiador específico na cartela geral.
* **Dois Modos de Sorteio:**
    * **Automático:** O próprio sistema gera e sorteia os números aleatoriamente, sem repetições.
    * **Manual:** Feito para ser usado em conjunto com um globo físico. O operador digita o número que saiu e o sistema valida a entrada na tela.
* **Prevenção de Perda de Dados (Auto-Save):** O progresso da rodada é salvo automaticamente no `localStorage` do navegador. Se a página for atualizada (F5) ou fechada acidentalmente, o jogo é restaurado instantaneamente.
* **Modal de Destaque (Tela Cheia):** Ao sortear um número, um pop-up gigante exibe a pedra e a marca do patrocinador em tela cheia, fechando automaticamente após 4 segundos ou ao clique do mouse.
* **Histórico Interativo na Grade:** É possível clicar em qualquer número já sorteado no painel geral para reabrir a tela cheia do patrocinador, facilitando o trabalho do locutor do evento.
* **Configuração Externa Desacoplada:** Um arquivo isolado (`patrocinadores.js`) permite a atualização rápida de logos e nomes de parceiros sem o risco de quebrar a lógica do código principal.

---

## 🛠️ Tecnologias Utilizadas

* **HTML5:** Estruturação semântica do painel de controle e do modal.
* **CSS3:** Estilização moderna inspirada em painéis de LED (Dark Mode), uso de CSS Grid para a cartela e animações suaves de transição.
* **JavaScript (Vanilla):** Lógica do jogo, controle de estado, persistência de dados local e manipulação do DOM sem a dependência de frameworks externos pesados ou bibliotecas.

---

## ⚙️ Como Usar (Rodando Localmente)

O sistema foi desenhado para ser "Plug and Play" e funciona 100% offline (desde que as imagens das logos estejam salvas no seu computador).

1. Faça o download dos arquivos do projeto.
2. Certifique-se de que o `index.html` e o `patrocinadores.js` estão na mesma pasta.
3. Clique duas vezes no arquivo `index.html` para abri-lo no seu navegador padrão (recomendado: Google Chrome, Edge ou Firefox).
4. Para zerar o painel e iniciar um novo jogo, basta clicar no botão vermelho **"♻️ Nova Rodada (Zerar)"** no topo da tela.

---

## 📝 Como Configurar os Patrocinadores

Para adicionar os seus patrocinadores reais, abra o arquivo `patrocinadores.js` em qualquer editor de código ou texto (como VS Code ou Bloco de Notas) e atualize o dicionário de dados conforme a estrutura abaixo:

```javascript
const sponsorConfig = {
    1: { name: "Nome da Empresa 1", logo: "caminho/para/logo1.png" },
    2: { name: "Nome da Empresa 2", logo: "caminho/para/logo2.png" },
    // E assim por diante, até o número 75...
};
```

👨‍💻 Créditos e Autoria
Idealização e Regras de Negócio: [![Linkedin Badge](https://img.shields.io/badge/-Christofer%20R.%20Souza-blue?style=flat-square&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/christofer-souza-63818116b)](https://www.linkedin.com/in/christofer-souza-63818116b)

Desenvolvimento e Arquitetura de Código: Gemini (Assistente de Inteligência Artificial do Google)

Projeto Open Source. Sinta-se livre para clonar, modificar e adaptar para as necessidades do seu evento!