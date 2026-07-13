# Fechado com Malaquias — Gerador de foto de apoiador

Página web onde apoiadores adicionam a própria foto dentro do círculo da moldura oficial
**"Fechado com Malaquias"** (pré-candidato a Deputado Estadual) e baixam / compartilham a arte.

## O que faz

- 📷 **Tirar foto ou escolher da galeria** (funciona no celular e no computador)
- 🎯 A foto entra **dentro do círculo branco** da moldura, com recorte automático
- 🔍 **Zoom** (barra ou pinça) e **arrastar** para posicionar o rosto; girar e centralizar
- 🖼️ Escolha do **formato de saída**: `1:1`, `3:2`, `2:3`, `4:3`, `3:4`, `5:4`, `4:5`, `16:9`, `9:16` ou **personalizado**
- ⬇️ Baixar como **PNG** ou **PDF**
- 🟢 **Enviar no WhatsApp** (compartilhamento direto no celular)

## Privacidade

Tudo é processado **no próprio aparelho do usuário** (100% no navegador). Nenhuma foto é
enviada para servidores.

## Como funciona / arquivos

- `index.html` — a aplicação inteira (interface + lógica de composição, exportação PNG/PDF e compartilhamento). Sem dependências externas.
- `moldura-data.js` — a moldura oficial embutida como *data URI* (torna a página autocontida e evita problemas de CORS ao exportar).
- `moldura.jpg` — arquivo original da moldura (referência).

O posicionamento do círculo está calibrado para a moldura de `1254×1254` px
(centro `423,732`, raio `294`).

## Rodar localmente

Basta abrir `index.html` no navegador, ou servir a pasta:

```bash
python3 -m http.server 8099
# abra http://localhost:8099
```

## Publicar

É um site estático — pode ser hospedado em GitHub Pages, Vercel, Netlify, etc.
(apenas servir os arquivos da pasta).

---

Feito para a campanha **#FechadoComMalaquias**.
