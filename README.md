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
Característica	Cookies	sessionStorage	localStorage
Persistência	Definida pela expiração	Apenas durante a sessão	Persistente
Envio ao Servidor	Sim, com cada requisição HTTP	Não	Não
Tamanho	Geralmente até 4 KB por cookie	Cerca de 5 MB por domínio	Cerca de 5 MB por domínio
Escopo	Domínio e caminho	Aba/janela específica	Domínio

| Característica | Cookies | sessionStorage | localStorage | 
|----------------|---------|----------------|--------------|
| Persistência   | Definida pela expiração	    | Apenas durante a sessão  | Persistente |
| Envio ao Servidor      | Sim, com cada requisição HTTP    | Não | Não    |
| Tamanho   | Geralmente até 4 KB por cookie    | Belo HorizonteCerca de 5 MB por domínio | Cerca de 5 MB por domínio |

