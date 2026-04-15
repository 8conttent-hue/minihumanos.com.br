# CLAUDE.md — MINIHUMANOS

Site gerado pelo **SF (Site Factory)** em 15/04/2026.

## Contexto do Site

**Nome:** MINIHUMANOS
**Nicho:** Educação
**Keywords:** O aplicativo Minha Rotina Especial e um software desenvolvido para auxiliar criancas
**Paleta de cores:** sunset | **Fonte:** outfit

O aplicativo Minha Rotina Especial é um software desenvolvido para auxiliar crianças com deficiência, síndromes, autismo ou déficits diversos. Um programa cuidadosamente planejado para estimular o desenvolvimento, integrando informações e deixando a rotina mais clara e organizada para crianças com diferentes desafios e que precisam de acompanhamento nas atividades do dia a dia. Criado a partir da metodologia de trabalho do Terapeuta Ocupacional Régis Nepomuceno, o aplicativo propõe a integração de informações, com a consciência de que as atividades de vida diária oferecem uma série de possibilidades de aprendizado e desenvolvimento. Quanto mais a criança conhece sua rotina, mais ela ganha confiança e autonomia e melhor os terapeutas conseguem acompanhar sua evolução e propor novos desafios a partir da informação compartilhada sobre seu dia a dia em ambientes fora da clínica.



## Componentes visuais usados

| Seção | Variante |
|-------|----------|
| Header | Header-G |
| Hero | Hero-F |
| Features | Features-I |
| About Section | About-E |
| Posts | Posts-J |
| Footer | Footer-H |
| Página Sobre | Sobre-H |
| Página Contato | Contato-J |

## Estrutura do projeto

```
src/
  sections/        # Layout escolhido pelo SF — Header, Hero, Features, About, Posts, Footer, Sobre, Contato
  data/            # JSONs com todo o conteúdo editável
  content/blog/    # Posts em Markdown
  pages/           # Rotas Astro (index, sobre, contato, blog, privacidade, termos)
  layouts/         # BaseLayout com fonte e cores dinâmicas
  styles/          # global.css com variáveis CSS de cor
public/
  images/          # hero.jpg, about.jpg, blog/*.jpg — inseridos automaticamente via Pexels
```

## O que editar

### Textos e conteúdo
- **`src/data/home.json`** — hero (título, subtítulo, botão), features (título, items), about section (título, desc, stats), posts
- **`src/data/sobre.json`** — conteúdo completo da página Sobre (hero, texto, missão)
- **`src/data/contato.json`** — título, subtítulo, email, tempo de resposta
- **`src/data/siteConfig.json`** — nome, slug, email, redes sociais, menu

### Imagens
Imagens já estão em `public/images/` (via Pexels). Para substituir, mantenha os mesmos nomes de arquivo:
- `hero.jpg` — imagem de fundo do Hero
- `about.jpg` — imagem da seção About (home)
- `sobre.jpg` — imagem de fundo da página Sobre
- `blog/{slug}.jpg` — imagens dos posts

### Posts do blog
Arquivos em `src/content/blog/`. Ajuste o tom de voz, adicione dados específicos do nicho e personalize conforme a identidade do site.

### Cores
Variáveis em `src/styles/global.css`: `--color-primary`, `--color-accent`, `--color-dark`.

## Deploy

```bash
bun install
bun run build
# Faça upload da pasta dist/ para Netlify, Vercel ou hosting estático
```
