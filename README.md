# Apresentação para o evento: Vivenciando a Pós-Graduação em Geofísica usando Reveal.js

**Evento:** Vivenciando a Pós-Graduação em Geofísica 
**Apresentador:** Yago Moreira Castro  
**Prévia:** [https://yagomcastro.github.io/vivenciando-pos-graduacao/](https://yagomcastro.github.io/vivenciando-pos-graduacao/)

Um modelo de Leonardo Uieda foi usado para criar esta apresentação: [https://github.com/leouieda/talk-template](https://github.com/leouieda/talk-template)

---

## Identidade Visual do IAG  
- A identidade visual do IAG-USP, incluindo logotipos e elementos gráficos, está disponível na pasta `assets > logos`. Certifique-se de utilizá-los conforme as diretrizes institucionais para manter a padronização visual.

---

## Usando como modelo

1. Vá para [https://github.com/leouieda/talk-template/generate](https://github.com/leouieda/talk-template/generate) para criar um novo repositório para seus slides.
2. Altere o título do HTML (aquele que aparece na aba do navegador) em `index.html`.
3. Remova o script Plausible Analytics do `<head>` em `index.html`.
4. Visualize a apresentação servindo os slides localmente.
5. Adicione seu conteúdo a `slides.md` e imagens à pasta `assets` (remova as imagens que não deseja usar).
6. Faça o commit e envie suas alterações.
7. Torne sua apresentação pública ativando o GitHub Pages.

---

## O que está incluído

- **`index.html`**: Documento principal que configura o reveal.js e seus plugins e carrega o conteúdo dos slides de `slides.md`. Altere a tag HTML `<title>` aqui.
- **`slides.md`**: Arquivo Markdown com o conteúdo real dos slides. O modelo inclui alguns slides que demonstram as classes CSS personalizadas disponíveis. Adicione seu conteúdo aqui.
- **`css/style.less`**: Estilização personalizada e classes CSS (usando Less). Edite para ajustar cores, tamanhos, fontes, espaçamento, etc.
- **`assets`**: Imagens usadas na apresentação. Você provavelmente pode excluir todas essas ao criar seus slides. Substitua `favicon.png` por uma imagem de 32 x 32 px para personalizar o ícone (configurado em `index.html`).
- **`fonts`**: Fontes utilizadas: FontAwesome, Atkinson Hyperlegible, Ubuntu Mono. Incluídas no repositório para acesso offline. Você pode removê-las e incluir fontes de um CDN (como Google Fonts) em `index.html`.
- **`packages`**: Versões locais de reveal.js, Less e KaTeX (para matemática) utilizadas. Ter esses pacotes no repositório é importante para visualizar os slides offline (em um avião ou sala de aula sem acesso fácil à internet).
- **`serve.py`**: Script Python que serve os slides e os recarrega sempre que os arquivos de origem são alterados. Muito útil para desenvolvimento. Veja as instruções abaixo.

---

## Servindo os slides localmente

Infelizmente, você não pode simplesmente abrir o arquivo `index.html` em um navegador para visualizar seus slides. O Reveal.js exige um servidor local real. Você pode configurá-lo da maneira que preferir. Abaixo, forneço instruções para fazer isso com Python (que é o que uso na maioria das vezes), mas funcionaria com qualquer outro servidor local.

Primeiro, instale o pacote Python `livereload`:

```sh
pip install livereload
```

ou

```sh
conda install livereload -c conda-forge
```

Depois, inicie um servidor em [http://localhost:8008](http://localhost:8008) executando:

```sh
python serve.py
```

Os slides serão abertos em seu navegador padrão e serão recarregados automaticamente quando você atualizar qualquer arquivo no repositório.

---

## Publicando no GitHub Pages

Vá até **Settings > Pages** do seu repositório e selecione **Source** como a branch principal e `/ (root)`. Provavelmente, você também desejará selecionar **Enforce HTTPS**.

Seus slides devem agora estar disponíveis em `https://USERNAME.github.io/REPOSITORY` ou equivalente, caso esteja usando um domínio personalizado. Pode levar algum tempo para isso acontecer.

Por exemplo, este modelo está disponível em: [https://www.leouieda.com/talk-template](https://www.leouieda.com/talk-template)

---

## Exportando para PDF

Você pode salvar seus slides em PDF para backup ou distribuição (os alunos costumam gostar disso porque podem fazer anotações no PDF). Para fazer isso, adicione `?print-pdf` ao final da URL (seja do servidor local ou hospedado) e imprima a página em PDF.

Isso funciona melhor no Chrome/Chromium. Os slides tendem a ficar distorcidos no Firefox por algum motivo.

**ATENÇÃO:** Vídeos e gifs não funcionam em PDFs.

---

## Licença

O modelo (`slides.md`, `index.html` e `css/style.less`) está licenciado sob uma **Licença Creative Commons Atribuição 4.0 Internacional**.

