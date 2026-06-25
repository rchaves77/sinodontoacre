Guia rápido: `background-clip` (PT-BR)
====================================

Descrição
---------
`background-clip` determina até onde o plano de fundo (background) de um elemento se estende.
Valores comuns:

- `border-box` — o fundo se estende até fora da borda.
- `padding-box` — o fundo cobre até a área do padding (padrão em muitos casos de uso).
- `content-box` — o fundo cobre apenas a área do conteúdo.

Exemplo para caixas (uso padrão):

```css
.card {
  background: rgba(255,200,100,0.12);
  border: 2px solid rgba(255,200,100,0.08);
  background-clip: padding-box; /* evita que o background fique por baixo da borda */
}
```

Exemplo para texto com gradiente (compatibilidade):

```css
.gradient-text {
  background: linear-gradient(135deg,#E5BA73 0%,#C5A880 50%,#957855 100%);
  -webkit-background-clip: text; /* WebKit antigo */
  background-clip: text;        /* padrão (quando suportado) */
  -webkit-text-fill-color: transparent; /* exibe o gradiente no texto */
}
```

Observações de compatibilidade
------------------------------
- `background-clip: text` tem suporte histórico melhor em navegadores WebKit quando usado com `-webkit-`.
- Para efeitos em texto, mantenha sempre o `-webkit-` e depois a propriedade sem prefixo.
- Teste em navegadores alvo; fallback pode ser necessário para navegadores que não suportam `background-clip: text`.

Licença
-------
Conteúdo livre para uso no projeto SINODONTO/AC.
