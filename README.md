# DIO_CSSgrid-responsive

## Aula sobre `grid-area` e Responsividade com CSS Grid

Este repositório contém exemplos de código sobre o uso da propriedade `grid-area` em CSS Grid para criar layouts responsivos. A aula aborda como posicionar elementos de forma clara e adaptá-los para diferentes tamanhos de tela, tornando o design responsivo e fácil de manter.

## O que é `grid-area`?

A propriedade **`grid-area`** do CSS Grid permite nomear áreas específicas da grade, facilitando o posicionamento e organização de elementos no layout. Isso torna o código mais legível e ajuda a criar layouts flexíveis e organizados.

### Exemplo Básico de `grid-area`

Para usar `grid-area`, primeiro configuramos um **container de grid** e definimos áreas com `grid-template-areas`. Em seguida, aplicamos `grid-area` nos elementos filhos, indicando em que parte do layout eles devem aparecer.

#### CSS

```css
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: auto auto;
  grid-template-areas: 
    "header header"
    "sidebar main";
}

.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;
}

.main {
  grid-area: main;
}
```

#### Nesse exemplo, o layout possui três áreas principais

- Header: ocupa a linha superior.
- Sidebar: está na coluna esquerda.
- Main: ocupa a coluna direita.

#### Criando um Layout Responsivo

Com a ajuda do CSS Grid e grid-area, podemos usar media queries para alterar o layout conforme o tamanho da tela, sem reorganizar o HTML. Abaixo, temos um exemplo que adapta o layout para telas menores (como dispositivos móveis).

```bash
@media (max-width: 600px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-areas: 
      "header"
      "main"
      "sidebar";
  }
}
```

Neste exemplo, para telas com largura menor que 600px:

- O layout muda para uma única coluna.
- O Header aparece primeiro, seguido pelo Main e depois pelo Sidebar.

#### Como Usar Este Código

1 - Clone este repositório:

```bash
git clone https://github.com/seu-usuario/nome-do-repositorio.git
```

2 -Abra o arquivo index.html no seu navegador para visualizar o layout.
3 - Ajuste o tamanho da janela do navegador para ver como o layout se adapta automaticamente para diferentes larguras de tela.

#### Recursos Adicionais

- Documentação CSS Grid no MDN
- Exemplos de grid-template-areas e grid-area

Este exemplo prático mostra como grid-area e CSS Grid podem ser usados juntos para construir layouts flexíveis e responsivos, essenciais para uma boa experiência do usuário.

#### Licença

Este projeto está licenciado sob a licença MIT
