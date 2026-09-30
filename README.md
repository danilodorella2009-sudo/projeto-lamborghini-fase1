# 🏎️ AUTOMOBILI LAMBORGHINI — Site Institucional & Configurador

Um site institucional e promocional de alta performance inspirado no ecossistema digital da **Automobili Lamborghini**. Desenvolvido com **HTML5**, **CSS3** e **JavaScript Vanilla**, o projeto foca na experiência do usuário (*UX/UI*), oferecendo interatividades fluidas, animações nativas e um estúdio interativo para o modelo **Revuelto SV**.

---

## 🔗 Links Rápidos

* 📄 **[[Tópico / Código HTML](#)** *(lamborghini)*
* 📚 **[Documentação Completa](#)** *(documentacao-site-lamborghini (2).pdf)*

---

## 🗺️️ 1. Mapeamento de Rotas e Navegação

A navegação foi projetada para simular a experiência fluida do site oficial da Lamborghini:

* **Página Inicial (`index.html`)**
  * 🔍 Ícone de busca ➔ Redireciona para a página de busca (`search.html`).
  * 📍 "Find your dealer" ➔ Acesso direto ao localizador de concessionárias (`dealer-locator.html`).
  * ⚡ "Explore the model" / "Iniciar configuração" ➔ Entrada para o configurador interativo (`configurador/configurator.html`).
  * 🏎️ Linha de Modelos ➔ Acesso às páginas exclusivas do **Urus SE**, **Miura SV** e **Revuelto SV**.
  * 📋 Menu Principal ➔ Redireciona para o catálogo geral de modelos (`models.html`).
* **Páginas Específicas de Veículos e Subpastas**
  * ⬅️ Navegação e botões de retorno integrados direcionando de volta para a Home (`index.html`).

---

## 💻 2. Visão Geral das Páginas

### 2.1 Página Inicial (`index.html`)
* **Header Fixo:** Contém o menu overlay, logo oficial e ícones de suporte/busca.
* **Hero Carrossel:** Apresentação em vídeo (`.mp4`) do Revuelto SV e imagens em alta resolução do Miura SV e Urus SE, com transição automática e pausa manual.
* **Carrossel de Modelos:** Vitrine em fundo claro para Revuelto, Urus e Temerario com seletores de variantes e indicadores visuais.
* **Dealer Locator:** Seção panorâmica com chamada para busca de concessionárias.
* **Configurador (Preview):** Abas interativas para atalho de configuração e consulta de modelos.
* **Suporte & Rodapé:** Módulo deslizante "ASK ME", links corporativos e termos legais.

### 2.2 Catálogo de Veículos (`models.html`)
* Leitura em tema claro da vitrine de automóveis com barra de navegação escura.
* Atualização dinâmica de especificações técnicas, slogans e imagens de fundo conforme o modelo selecionado.

### 2.3 Sistema de Busca (`search.html`)
* Interface minimalista focada na busca de modelos, serviços de propriedade (*Ownership*) e soluções personalizadas (*Custom Solutions*).

### 2.4 Localizador de Concessionárias (`dealer-locator.html`)
* Painel lateral interativo com divisões por tipo de serviço (*Showroom*, *Service*, *Collision Center*), seleção de países e mapa ilustrativo.

### 2.5 Páginas Exclusivas de Modelos (`revuelto-sv`, `miura-sv`, `urus-se`)
* Apresentação de dados de performance (potência em CV, aceleração 0-100 km/h e velocidade máxima).
* Seções dedicadas à aerodinâmica, conjunto mecânico e seletores de modos de condução (ex: Strada, Sport, Corsa, Neve, Terra).

### 2.6 Estúdio Virtual (`configurador/configurator.html`)
* Visualizador interativo com troca de cor do veículo em tempo real (*Azzurro Thetys*, *Rosso Mars*, *Bianco Monocerus*).
* Modais integrados para seleção de idiomas e geração de código de configuração único (**L-Code**).

---

## ⚙️ 3. Recursos Técnicos e Interatividade

* **Modais e Menus Sem JavaScript (`:target`):** A abertura e o fechamento do menu principal, chats e janelas modais utilizam a pseudo-classe CSS `:target`, alterando o estado visual via link âncora (`#menuOverlay`) sem sobrecarregar a execução de scripts.
* **Hero Automático Nativo em CSS (`@keyframes`):** A alternância dos mídias no cabeçalho utiliza animações CSS puras com suporte a pausa através de um `<input type="checkbox">` oculto acionando a propriedade `animation-play-state: paused`.
* **Lógica Dinâmica em Vanilla JS (`script.js`):** Gerencia a navegação circular do carrossel, troca de abas de variantes e atualização dos detalhes técnicos sem bibliotecas externas.

---

## 🎨 4. Diretrizes de Design & Tipografia

* **Paleta de Cores:**
  * **Amarelo Lamborghini (Destaque):** `#FFC000`
  * **Fundo Escuro (Dark Mode):** `#000000` / `#181818`
  * **Estúdio / Configurador:** `#111214`
  * **Textos e Linhas:** `#FFFFFF`, `#9A9A9A`, `#555555`
* **Tipografia Responsiva:** Google Fonts (**Anton**, **Oswald**, **Inter** e **Roboto**) ajustadas dinamicamente com a função CSS `clamp()`.

---

## 🔧 5. Requisitos e Execução

### Pré-requisitos
* Qualquer navegador web moderno (Google Chrome, Mozilla Firefox, Microsoft Edge ou Safari).
* Não requer instalação de Node.js, gerenciadores de pacotes (npm/yarn) ou compiladores.

### Como Rodar
1. Baixe ou clone o repositório.
2. Certifique-se de manter os arquivos em suas pastas originais para preservar os caminhos relativos de imagens, fontes e arquivos CSS/JS.
3. Execute o arquivo `index.html` diretamente no navegador ou utilize a extensão **Live Server** no VS Code.

---

## 🤝 6. Contribuição e Licença

Contribuições, correções de bugs e sugestões de melhorias são bem-vindas! Sinta-se à vontade para abrir uma *Issue* ou enviar um *Pull Request*.

*Projeto desenvolvido com fins educacionais e de demonstração baseados na identidade visual da Automobili Lamborghini S.p.A.*
