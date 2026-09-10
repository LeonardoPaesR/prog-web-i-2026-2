# Análise de Comportamento: Block vs Inline (Atividade Prática 03)

## 1. Tabela de Classificação dos Elementos

| Elemento | Block ou Inline? | Justificativa do Comportamento |
| :--- | :--- | :--- |
| `h1`, `h2`, `h3` | **Block** | Ocupa 100% da largura da linha disponível. Faz sentido semanticamente porque um título introduz uma nova seção temática e precisa isolar visualmente o início do bloco. |
| `p` | **Block** | Ocupa toda a largura da linha e força quebra antes e depois. Parágrafos são blocos autônomos de texto estruturado na leitura. |
| `ul`, `ol` | **Block** | Ocupa a largura inteira disponível, contendo os itens agrupados verticalmente como uma unidade de lista estrutural. |
| `a` (link no menu) | **Inline** | Ocupa estritamente o espaço da largura do texto que contém. Faz sentido para permitir a inserção fluida de hiperlinks no meio de frases ou itens sem forçar quebras de linha indesejadas. |
| `strong` dentro de `p` | **Inline** | Ocupa apenas a área das palavras destacadas. Permite enfatizar termos específicos mantendo o fluxo contínuo do parágrafo de texto. |
| `img` | **Inline** *(Inline-block)* | Por padrão, flui inline com o texto ao redor ocupando apenas suas dimensões declaradas (`width` e `height`), permitindo compor ícones ou imagens ao lado de textos. |

---

## 2. Experimento Comparativo: `strong` vs `p`

* **Dois elementos `<strong>` consecutivos no mesmo parágrafo:**
  * **Comportamento observado:** Ficam posicionados um exatamente ao lado do outro na mesma linha física horizontal. 
  * **Motivo:** Elementos *inline* não iniciam nova linha e ocupam estritamente o espaço de seus conteúdos.

* **Dois elementos `<p>` consecutivos:**
  * **Comportamento observado:** O segundo parágrafo é empurrado obrigatoriamente para a linha de baixo, existindo uma margem vertical nativa separando ambos.
  * **Motivo:** Elementos *block* ocupam toda a largura horizontal da janela e forçam o próximo elemento a começar em uma nova linha.

---

## 3. Respostas do Desafio Opcional

* **Diferença entre `<figure>`/`<figcaption>` vs `<img>` + `<p>`:**
  O `<figure>` cria uma associação semântica formal entre o conteúdo de mídia e sua legenda (`<figcaption>`). Leitores de tela e motores de busca compreendem que aquela legenda descreve diretamente a mídia, além de permitir mover a figura para qualquer parte do documento sem quebrar a coerência textual. Um `<p>` solto seria interpretado apenas como texto comum independente.
* **Uso de `<caption>` na tabela em vez de `<h3>`:**
  O elemento `<caption>` é o título semanticamente vinculado à tabela. Leitores de tela anunciam o `<caption>` imediatamente antes de iniciar a leitura das linhas e colunas, permitindo que usuários com deficiência visual identifiquem sobre o que a tabela se trata antes de percorrer seus dados.