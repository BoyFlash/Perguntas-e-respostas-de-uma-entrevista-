# Perguntas e respostas de uma entrevista:

## Perguntas;

1. O que um tipo de documento faz?

2. Como você veicula uma página com conteúdo em vários idiomas?

3. Com que tipo de coisas você deve ter cuidado ao projetar ou desenvolver sites multilíngues?

4. Para que servem os atributos de dados?

5. Considere o HTML5 como uma plataforma web aberta. Quais são os blocos de construção do HTML5?

6. Descreva a diferença entre cookie, sessionStorage e localStorage.

7. Descreva a diferença entre <script>, <script async> e <script defer>.

8. Por que geralmente é uma boa ideia posicionar <link>s CSS entre <head></head> e <script>s JS logo antes de </body>? Você conhece alguma exceção?

9. O que é renderização progressiva?

10. Por que você usaria um atributo srcset em uma tag de imagem? Explique o processo que o navegador usa ao avaliar o conteúdo deste atributo.

11. Você já usou diferentes linguagens de templates HTML antes?

12. Qual é a diferença entre canvas e svg?

13. O que são elementos vazios em HTML?

## Respostas;

#### 1.  O tipo de documento (doctype) no HTML informa ao navegador qual versão do HTML a página está usando. Isso ajuda o navegador a renderizar a página corretamente.

#### 2.  Para veicular uma página com conteúdo em vários idiomas, você pode usar várias abordagens. Aqui estão algumas das mais comuns:

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>usando varias linguas</title>
</head>
<body>
    <p lang="en">This is an English paragraph.</p>
    <p lang="es">Este es un párrafo en español.</p>
    <p lang="fr">Ceci est un paragraphe en français.</p>
</body>
</html>

#### 3. Projetar e desenvolver sites multilíngues envolve várias considerações importantes para garantir uma experiência de usuário consistente e eficaz. Aqui estão alguns pontos chave a serem observados:

1 - Localização vs. Internacionalização

2 - Internacionalização (i18n): Processo de preparar o seu site para suportar múltiplos idiomas sem precisar de grandes mudanças no código.

- Localização (l10n): Adaptação do conteúdo e outras funcionalidades para um público específico, incluindo tradução, formatos de data/hora, moedas, etc.

#### 4.  Os atributos de dados, também conhecidos como atributos de data ou data attributes, são usados para armazenar informações adicionais em elementos HTML. Esses atributos não são exibidos ao usuário, mas podem ser acessados e manipulados via JavaScript e CSS para adicionar funcionalidades dinâmicas ao site.

#### 5.  HTML5 é uma plataforma web aberta que traz consigo uma série de novas funcionalidades e tecnologias projetadas para criar uma experiência de usuário rica e interativa. Aqui estão os principais blocos de construção do HTML5:

### Estrutura Semântica

HTML5 introduz várias tags semânticas que melhoram a estrutura e a acessibilidade do conteúdo da web:

<header>: Define a seção de cabeçalho de um documento ou seção.
<nav>: Define uma seção de navegação.
<section>: Define uma seção genérica de um documento.
<article>: Define um conteúdo independente e autocontido.
<aside>: Define conteúdo relacionado, como uma barra lateral.
<footer>: Define a seção de rodapé de um documento ou seção.
<main>: Define o conteúdo principal de um documento.
<figure> e <figcaption>: Define conteúdo ilustrativo e sua legenda.

e etc...


#### 6. Cookies, sessionStorage e localStorage são todas tecnologias usadas para armazenar dados no navegador do usuário, mas têm características e usos distintos. Vamos ver as diferenças entre elas:

 ### Cookies
 
  Características:
 
 - Armazenamento de Pequenos Dados: Cookies são geralmente usados para armazenar pequenas quantidades de dados (até 4 KB por cookie).
   
- Enviados com Requisições HTTP: Cookies são enviados ao servidor com cada requisição HTTP, permitindo que o servidor leia e escreva dados no cliente.

- Expiração e Persistência: Cada cookie pode ter uma data de expiração. Cookies podem ser persistentes (durando além da sessão do navegador) ou de sessão (expirando quando o navegador é fechado).
  
### Uso Comum:
  
Autenticação e gerenciamento de sessões.
Rastreamento de usuário e personalização.
  
#### Escopo: Cookies têm escopo de domínio e caminho, o que significa que eles são acessíveis apenas nas páginas que pertencem ao domínio e caminho especificados.

### sessionStorage

 Características:

- Armazenamento Temporário: Dados são armazenados apenas durante a sessão do navegador (até que a aba ou janela do navegador seja fechada).

- Não Enviado com Requisições HTTP: Dados no sessionStorage não são enviados ao servidor com cada requisição.

- Escopo: Os dados são específicos à aba ou janela e não são compartilhados entre abas ou janelas diferentes, mesmo que pertençam ao mesmo domínio.
  
### Uso Comum:

- Armazenamento de dados temporários, como informações de formulário que não precisam persistir além da sessão.

### localStorage

 Características:

- Armazenamento Persistente: Dados persistem mesmo depois de fechar a aba ou janela do navegador e são mantidos até serem explicitamente removidos.

- Não Enviado com Requisições HTTP: Dados no localStorage não são enviados ao servidor com cada requisição.

- Escopo: Os dados são específicos ao domínio, mas são acessíveis em todas as abas e janelas que pertencem ao mesmo domínio.
  
### Uso Comum:

- Armazenamento de dados que precisam persistir entre sessões, como preferências do usuário, temas, configurações de layout.

  Comparação Resumida
  
| Característica | Cookies | sessionStorage | localStorage | 
|----------------|---------|----------------|--------------|
| Persistência   | Definida pela expiração	    | Apenas durante a sessão  | Persistente |
| Envio ao Servidor      | Sim, com cada requisição HTTP    | Não | Não    |
| Tamanho   | Geralmente até 4 KB por cookie    | Belo HorizonteCerca de 5 MB por domínio | Cerca de 5 MB por domínio |
| Escopo  | Domínio e caminho | Aba/janela específica  | Domínio |

#### 7. Quando Usar Cada Um:

- <script>: Use quando o script precisa ser executado imediatamente e/ou depende de elementos HTML que estão sendo carregados.

- <script async>: Use quando o script não depende de outros scripts ou do conteúdo do HTML, e a ordem de execução não é crítica.

- <script defer>: Use quando você deseja garantir que o script seja executado apenas após o carregamento completo do documento HTML, ou quando a ordem de execução é importante, mas você deseja carregar o script de forma assíncrona para melhorar o desempenho de carregamento da página.

8. Posicionar os elementos <link> para CSS entre as tags <head></head> e os scripts JavaScript logo antes de </body> é uma prática recomendada por várias razões, relacionadas principalmente ao desempenho e à experiência do usuário. Aqui estão alguns motivos principais:

- Carregamento Assíncrono: Os navegadores geralmente começam a renderizar a página assim que encontram o <head>. Colocar os <link> para folhas de estilo CSS no <head> permite que o navegador comece a baixar e processar os estilos CSS enquanto continua a analisar o restante do documento HTML. Isso é crucial para a renderização inicial rápida e para melhorar a percepção de carregamento rápido da página.

- Prioridade Visual: O CSS controla o layout, a aparência e a animação da página. Tê-lo disponível cedo evita que os elementos da página sejam renderizados sem estilos aplicados, evitando flashes de conteúdo não estilizado (FOUC - Flash of Unstyled Content).
  
#### <script> no Final do <body>

- Carregamento Paralelo: Colocar os scripts JavaScript no final do <body> permite que o navegador carregue e execute os scripts após o conteúdo principal da página ter sido renderizado. Isso melhora a percepção de desempenho, pois o usuário vê o conteúdo visível antes de quaisquer scripts serem executados.

- Menor Impacto na Renderização: Scripts JavaScript podem ser bloqueantes, o que significa que a renderização do conteúdo pode ser interrompida enquanto o navegador executa o script. Colocá-los no final do <body> minimiza esse impacto, garantindo que o conteúdo visível seja priorizado.

### 9. A renderização progressiva é um conceito fundamental no design de interfaces de usuário e no desenvolvimento web, que se refere à prática de apresentar conteúdo inicial de forma rápida e gradualmente melhorar a apresentação à medida que mais dados são carregados ou processados. Isso não se limita apenas à web, mas também se aplica a aplicativos móveis e outras interfaces digitais. 

### 10. O atributo srcset é usado em elementos <img> para fornecer ao navegador uma lista de URLs de imagens e suas respectivas larguras de pixel, permitindo ao navegador escolher a melhor imagem para renderizar com base no contexto de exibição do usuário. Isso é especialmente útil em dispositivos com diferentes resoluções de tela, como monitores de alta definição (HD), telas de dispositivos móveis e tablets.

### 11. Não

### 12. Canvas e SVG são duas tecnologias distintas para renderização gráfica em páginas web. Cada uma tem suas próprias características, vantagens e casos de uso ideais. 

Conclusão

A escolha entre Canvas e SVG depende muito do tipo de gráficos que você está tentando criar e das necessidades específicas do seu projeto. Canvas é poderoso para gráficos dinâmicos e interativos, enquanto SVG é excelente para gráficos vetoriais escaláveis e interativos.

### 13. Elementos vazios em HTML são elementos que não possuem conteúdo entre suas tags de abertura e fechamento. Em outras palavras, eles não têm conteúdo textual nem outros elementos aninhados dentro deles. Eles são formados apenas pela tag de abertura, possíveis atributos e pela tag de fechamento, que pode ser explícita (como em XHTML) ou implícita (em HTML5).

