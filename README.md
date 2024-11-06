Explorando designs modernos para sites, me deparei com um trecho de código que me deixou intrigado:

```javascript
function IconSearchSubmit({ className }) {
    return (
      <svg className={className} viewBox="0 0 24 24">
        <path d="M21.172 24l-7.387-7.387c-1.388.874-3.024 1.387-4.785 1.387-4.971 0-9-4.029-9-9s4.029-9 9-9 9 4.029 9 9c0 1.761-.514 3.398-1.387 4.785l7.387 7.387-2.828 2.828zm-12.172-8c3.859 0 7-3.14 7-7s-3.141-7-7-7-7 3.14-7 7 3.141 7 7 7z" />
      </svg>
    );
}

```
A primeira coisa que notei foi a quantidade de números no atributo `d`. Aquilo parecia um "caminho" ou algo assim, mas eu realmente não fazia ideia do que significava. Resolvi pesquisar e descobri que esse bloco era, na verdade, um SVG.

# O que é SVG?

SVG (Scalable Vector Graphics) é uma linguagem baseada em XML usada para descrever gráficos vetoriais bidimensionais. Diferente de imagens em bitmap, como JPEG ou PNG, os gráficos SVG podem ser redimensionados sem perder qualidade. Por isso, eles são muito utilizados em ícones, logos e ilustrações em sites modernos, onde responsividade e clareza visual são essenciais.

No SVG acima, o elemento `<path>` define o desenho do ícone, e o atributo `d` (que estava cheio daqueles números) descreve precisamente o caminho que o gráfico deve seguir. Cada número representa uma coordenada ou instrução para o desenho, o que faz com que o ícone seja definido matematicamente.

Decidi colocar esse trecho de código em um visualizador SVG para ver como realmente funcionava. Utilizei o seguinte código no CodePen:
```javascript
<svg width="100" height="100" viewBox="0 0 24 24">
    <path d="M21.172 24l-7.387-7.387c-1.388.874-3.024 1.387-4.785 1.387-4.971 0-9-4.029-9-9s4.029-9 9-9 9 4.029 9 9c0 1.761-.514 3.398-1.387 4.785l7.387 7.387-2.828 2.828zm-12.172-8c3.859 0 7-3.14 7-7s-3.141-7-7-7-7 3.14-7 7 3.141 7 7 7z" fill="currentColor" />
</svg>

```
Resultado no CodePen:
