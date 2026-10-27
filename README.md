# PlayDev · Clone do YouTube com Flexbox

Projeto do desafio de Flexbox da trilha Front-End da [DIO](https://www.dio.co). A proposta era recriar a página inicial do YouTube usando apenas HTML e CSS, com foco em Flexbox.

Em vez de copiar a marca original, criei uma identidade própria: **PlayDev**, uma plataforma fictícia de vídeos sobre desenvolvimento web, com paleta em azul-petróleo escuro e destaque âmbar.

> Substitua esta linha por um print da página (por exemplo, `![Prévia do projeto](./preview.png)`).

## Referência

Design base no Figma: [Desafio de Flexbox - DIO](https://www.figma.com/file/lrRWUZPKnqMDZrSDJmZxUS/Desafio-de-Flexbox---DIO?node-id=0%3A1)

## O que foi construído

- **Cabeçalho fixo** com botão de menu, logo, campo de busca e ações do usuário
- **Menu lateral** com navegação principal e divisor
- **Barra de filtros** com rolagem horizontal
- **Grade de vídeos** responsiva, com miniaturas feitas só com CSS (gradientes), duração, avatar, título e metadados
- **Responsividade**: abaixo de 800px o menu lateral é ocultado e a grade passa a ocupar a largura toda

## Como o Flexbox foi usado

| Parte da página | Técnica |
| --- | --- |
| Cabeçalho | `display: flex`, `justify-content: space-between`, `align-items: center` |
| Campo de busca | `flex: 1` no input e `flex: 0 0 64px` no botão |
| Menu lateral | `flex-direction: column` com `gap` |
| Estrutura geral | `.sidebar` com largura fixa (`flex: 0 0 220px`) e `.content` com `flex: 1` |
| Filtros | `overflow-x: auto` e itens com `flex: 0 0 auto` para não encolher |
| Grade de vídeos | `flex-wrap: wrap` e `flex: 1 1 280px` em cada card |
| Card de vídeo | `flex-direction: column` para a miniatura e as informações |
| Info do vídeo | `flex` com avatar fixo e texto com `flex: 1` |
| Miniaturas | `justify-content` e `align-items: center` para centralizar o texto |

Também foram praticados outros conceitos da trilha: `position: sticky` (cabeçalho, menu e filtros), `position: absolute` com pai `relative` (duração do vídeo), `z-index`, `aspect-ratio`, variáveis CSS e `@media` queries.

## Estrutura do projeto

```
youtube-flexbox/
├── index.html
├── style.css
└── README.md
```

## Como rodar

Não há dependências. Basta clonar o repositório e abrir o `index.html` no navegador:

```bash
git clone https://github.com/DestroyerIG/youtube-flexbox-desafiodio.git
cd youtube-flexbox-desafiodio
```

## Possíveis melhorias

- Menu lateral recolhível em telas pequenas
- Tema claro e escuro
- Página de reprodução de vídeo
- Dados dos vídeos carregados com JavaScript

## Autor

**Itallo Gabriel**

- GitHub: [DestroyerIG](https://github.com/DestroyerIG)
- LinkedIn: [itallogoncalves](https://www.linkedin.com/in/itallogoncalves)
