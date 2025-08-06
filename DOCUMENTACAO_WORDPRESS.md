# Documentação para Implementação da Landing Page no WordPress

## Dra. Ana - Terapia Cognitivo-Comportamental para Ansiedade

**Versão:** 1.0  
**Data:** 15 de julho de 2025  
**Autor:** Manus AI  

---

## Índice

1. [Visão Geral](#visão-geral)
2. [Requisitos do Sistema](#requisitos-do-sistema)
3. [Métodos de Implementação](#métodos-de-implementação)
4. [Implementação via Elementor](#implementação-via-elementor)
5. [Implementação via Código Personalizado](#implementação-via-código-personalizado)
6. [Configuração de Imagens](#configuração-de-imagens)
7. [Configuração de Formulários](#configuração-de-formulários)
8. [Otimização e Performance](#otimização-e-performance)
9. [SEO e Meta Tags](#seo-e-meta-tags)
10. [Responsividade](#responsividade)
11. [Manutenção e Atualizações](#manutenção-e-atualizações)
12. [Solução de Problemas](#solução-de-problemas)
13. [Recursos Adicionais](#recursos-adicionais)

---

## Visão Geral

Esta documentação fornece instruções detalhadas para implementar a landing page da Dra. Ana em um site WordPress existente. A landing page foi desenvolvida com foco em conversão, utilizando as melhores práticas de UX/UI para psicólogos especializados em TCC para ansiedade em jovens adultos.

### Características da Landing Page

- **Design responsivo** para todos os dispositivos
- **Otimizada para conversão** com CTAs estrategicamente posicionados
- **SEO-friendly** com estrutura semântica adequada
- **Carregamento rápido** com imagens otimizadas
- **Acessibilidade** seguindo padrões WCAG
- **Integração com WhatsApp** para facilitar o contato

### Estrutura da Página

A landing page é composta pelas seguintes seções:

1. **Header/Navegação** - Menu fixo com links para seções
2. **Hero Section** - Título principal, subtítulo e CTAs primários
3. **Sobre a Dra. Ana** - Apresentação profissional e credenciais
4. **Serviços** - Três principais serviços oferecidos
5. **Público-alvo** - Para quem a terapia é indicada
6. **Como Funciona a TCC** - Explicação da abordagem terapêutica
7. **FAQ** - Dúvidas frequentes com accordion
8. **CTA Final** - Chamada para ação principal
9. **Footer** - Informações de contato e dados legais

---


## Requisitos do Sistema

### WordPress

- **Versão mínima:** WordPress 5.0 ou superior
- **PHP:** Versão 7.4 ou superior
- **Tema:** Compatível com Astra (recomendado) ou qualquer tema que suporte páginas personalizadas
- **Plugins necessários:**
  - Elementor (versão gratuita ou Pro)
  - Contact Form 7 (para formulários)
  - Yoast SEO (para otimização)

### Plugins Opcionais (Recomendados)

- **WP Rocket** - Para cache e otimização de performance
- **Smush** - Para otimização automática de imagens
- **UpdraftPlus** - Para backup automático
- **Wordfence** - Para segurança
- **Schema Pro** - Para dados estruturados avançados

### Recursos do Servidor

- **Espaço em disco:** Mínimo 100MB para os arquivos da landing page
- **Largura de banda:** Adequada para tráfego esperado
- **SSL:** Certificado SSL ativo (obrigatório)
- **CDN:** Recomendado para melhor performance global

---

## Métodos de Implementação

Existem três métodos principais para implementar a landing page no WordPress:

### Método 1: Elementor (Recomendado)

**Vantagens:**
- Interface visual intuitiva
- Fácil edição posterior
- Não requer conhecimento técnico
- Responsividade automática
- Integração nativa com WordPress

**Desvantagens:**
- Requer plugin Elementor
- Pode ser mais pesado que código puro
- Limitações de customização avançada

### Método 2: Código Personalizado

**Vantagens:**
- Performance otimizada
- Controle total sobre o código
- Menor dependência de plugins
- Carregamento mais rápido

**Desvantagens:**
- Requer conhecimento técnico
- Edições futuras mais complexas
- Necessita backup antes de alterações

### Método 3: Page Builder Alternativo

**Vantagens:**
- Flexibilidade de escolha
- Pode usar Gutenberg, Beaver Builder, etc.
- Integração com tema existente

**Desvantagens:**
- Pode requerer adaptações no código
- Compatibilidade variável

---


## Implementação via Elementor

### Passo 1: Preparação

1. **Instale o Elementor**
   - Acesse `Plugins > Adicionar Novo`
   - Busque por "Elementor"
   - Instale e ative o plugin

2. **Crie uma Nova Página**
   - Vá para `Páginas > Adicionar Nova`
   - Título: "Landing Page - Dra. Ana"
   - Clique em "Editar com Elementor"

### Passo 2: Configuração Inicial

1. **Configurações da Página**
   - Clique no ícone de configurações (engrenagem)
   - Em "Layout da Página", selecione "Canvas Elementor"
   - Isso remove header e footer do tema

2. **Importar CSS Personalizado**
   - Vá para `Aparência > Personalizar > CSS Adicional`
   - Cole o conteúdo do arquivo `styles.css` (adaptado para Elementor)

### Passo 3: Construção das Seções

#### Header/Navegação

1. **Adicione uma Seção**
   - Estrutura: Uma coluna
   - Configurações da seção:
     - Posição: Fixo
     - Z-index: 1000
     - Background: Branco
     - Box Shadow: 0 2px 10px rgba(0,0,0,0.1)

2. **Adicione Widget de Menu**
   - Widget: Nav Menu
   - Selecione o menu principal
   - Estilo: Horizontal
   - Cor: #2C3E50

#### Hero Section

1. **Adicione Nova Seção**
   - Estrutura: Duas colunas (50/50)
   - Background: Gradiente linear (#F7F9FA para #E8F4F8)
   - Padding: 120px 0 80px

2. **Coluna Esquerda - Conteúdo**
   - Widget: Título
     - Texto: "Transforme sua Ansiedade em Tranquilidade"
     - Tag HTML: H1
     - Cor: #2C3E50
     - Tamanho: 48px
   
   - Widget: Texto
     - Conteúdo: "Terapia Cognitivo-Comportamental especializada..."
     - Cor: #7F8C8D
     - Tamanho: 20px
   
   - Widget: Botão (2x)
     - Botão 1: "Agendar Primeira Consulta"
       - Background: #4A90A4
       - Link: #contato
     - Botão 2: "Saiba Como Funciona"
       - Background: Transparente
       - Borda: #4A90A4

3. **Coluna Direita - Imagem**
   - Widget: Imagem
   - Selecione: hero-image.webp
   - Border Radius: 12px

#### Seção Sobre

1. **Nova Seção - Duas Colunas**
   - Background: Branco
   - Padding: 80px 0

2. **Conteúdo da Seção**
   - Título H2: "Conheça a Dra. Ana"
   - Texto introdutório
   - Lista de credenciais
   - Imagem placeholder

#### Seção Serviços

1. **Nova Seção - Três Colunas**
   - Background: #F7F9FA
   - Padding: 80px 0

2. **Cards de Serviços**
   - Widget: Icon Box (3x)
   - Ícones: User, Users, Calendar
   - Títulos e descrições conforme HTML
   - Background: Branco
   - Border Radius: 12px
   - Box Shadow: 0 4px 20px rgba(0,0,0,0.08)

#### Seção Público-alvo

1. **Nova Seção - Grid de 6 Colunas**
   - Background: Branco
   - Título centralizado

2. **Items do Público**
   - Widget: Icon Box (6x)
   - Ícone: Checkmark
   - Textos conforme especificação

#### Seção Como Funciona

1. **Nova Seção - Duas Colunas**
   - Background: #F7F9FA
   - Coluna 1: Conteúdo textual
   - Coluna 2: Imagem wellbeing-image.jpg

#### Seção FAQ

1. **Nova Seção - Uma Coluna**
   - Background: Branco
   - Widget: Accordion (se disponível no Elementor Pro)
   - Ou usar Toggle widgets

#### CTA Final

1. **Nova Seção - Uma Coluna**
   - Background: Gradiente (#4A90A4 para #3A7A8A)
   - Cor do texto: Branco
   - Botões de CTA centralizados

#### Footer

1. **Nova Seção - Quatro Colunas**
   - Background: #2C3E50
   - Cor do texto: Branco
   - Informações de contato distribuídas

### Passo 4: Configurações Avançadas

#### Responsividade

1. **Teste em Diferentes Dispositivos**
   - Use o preview responsivo do Elementor
   - Ajuste tamanhos de fonte para mobile
   - Verifique espaçamentos

2. **Configurações Mobile**
   - Títulos: Reduzir para 28px
   - Textos: Mínimo 16px
   - Botões: Width 100% em mobile
   - Colunas: Stack verticalmente

#### Animações

1. **Adicione Animações de Entrada**
   - Seções: Fade In Up
   - Delay progressivo: 0.2s, 0.4s, 0.6s
   - Duração: 0.6s

2. **Hover Effects**
   - Botões: Transform scale(1.05)
   - Cards: Transform translateY(-5px)
   - Transição: 0.3s ease

---


## Implementação via Código Personalizado

### Método 1: Template de Página Personalizado

#### Passo 1: Criar Template

1. **Acesse o Editor de Temas**
   - Vá para `Aparência > Editor de Temas`
   - Ou use FTP/cPanel para acessar arquivos

2. **Crie o Arquivo Template**
   - Nome: `page-landing-dra-ana.php`
   - Localização: `/wp-content/themes/seu-tema/`

3. **Código do Template**

```php
<?php
/*
Template Name: Landing Page Dra Ana
*/

// Remove header e footer padrão
remove_action('wp_head', 'wp_generator');
get_header(); 
?>

<!DOCTYPE html>
<html <?php language_attributes(); ?>>
<head>
    <meta charset="<?php bloginfo('charset'); ?>">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Dra. Ana - Terapia Cognitivo-Comportamental para Ansiedade</title>
    <meta name="description" content="Terapia Cognitivo-Comportamental especializada para jovens adultos que buscam superar ansiedade e estresse. Agende sua consulta com a Dra. Ana.">
    
    <!-- Google Fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
    
    <!-- CSS Personalizado -->
    <link rel="stylesheet" href="<?php echo get_template_directory_uri(); ?>/landing-page-styles.css">
    
    <?php wp_head(); ?>
</head>
<body <?php body_class(); ?>>

<!-- Aqui vai todo o HTML da landing page -->
<?php
// Incluir o conteúdo HTML da landing page
include(get_template_directory() . '/landing-page-content.php');
?>

<!-- JavaScript Personalizado -->
<script src="<?php echo get_template_directory_uri(); ?>/landing-page-script.js"></script>

<?php wp_footer(); ?>
</body>
</html>

<?php get_footer(); ?>
```

#### Passo 2: Upload dos Arquivos

1. **Faça Upload via FTP/cPanel**
   - `landing-page-styles.css` → `/wp-content/themes/seu-tema/`
   - `landing-page-script.js` → `/wp-content/themes/seu-tema/`
   - `landing-page-content.php` → `/wp-content/themes/seu-tema/`

2. **Crie o Arquivo de Conteúdo**
   - Nome: `landing-page-content.php`
   - Conteúdo: Todo o HTML da landing page (sem DOCTYPE e tags html/head)

#### Passo 3: Criar a Página

1. **Nova Página no WordPress**
   - Vá para `Páginas > Adicionar Nova`
   - Título: "Landing Page Dra Ana"
   - Template: Selecione "Landing Page Dra Ana"
   - Publique a página

### Método 2: Plugin de Código Personalizado

#### Usando Insert Headers and Footers

1. **Instale o Plugin**
   - `Plugins > Adicionar Novo`
   - Busque: "Insert Headers and Footers"

2. **Adicione CSS no Header**
   - Vá para `Configurações > Insert Headers and Footers`
   - Cole o CSS na seção "Scripts in Header"

3. **Crie Página com HTML**
   - Use o editor de blocos
   - Adicione bloco "HTML Personalizado"
   - Cole todo o HTML da landing page

### Método 3: Child Theme (Recomendado)

#### Passo 1: Criar Child Theme

1. **Crie a Pasta**
   - `/wp-content/themes/astra-child/`

2. **Arquivo style.css**
```css
/*
Theme Name: Astra Child - Dra Ana
Template: astra
Version: 1.0
*/

@import url("../astra/style.css");

/* CSS personalizado da landing page aqui */
```

3. **Arquivo functions.php**
```php
<?php
function astra_child_enqueue_styles() {
    wp_enqueue_style('parent-style', get_template_directory_uri() . '/style.css');
    wp_enqueue_style('child-style', get_stylesheet_directory_uri() . '/style.css', array('parent-style'));
}
add_action('wp_enqueue_scripts', 'astra_child_enqueue_styles');

// Enqueue scripts da landing page
function landing_page_scripts() {
    if (is_page('landing-page-dra-ana')) {
        wp_enqueue_script('landing-page-js', get_stylesheet_directory_uri() . '/landing-page-script.js', array('jquery'), '1.0', true);
    }
}
add_action('wp_enqueue_scripts', 'landing_page_scripts');
?>
```

#### Passo 2: Ativar Child Theme

1. **Vá para Aparência > Temas**
2. **Ative o "Astra Child - Dra Ana"**

---

## Configuração de Imagens

### Upload das Imagens

1. **Acesse a Biblioteca de Mídia**
   - `Mídia > Biblioteca`
   - Clique em "Adicionar Nova"

2. **Faça Upload das Imagens**
   - `hero-image.webp`
   - `meditation-image.jpg`
   - `wellbeing-image.jpg`

3. **Otimize as Imagens**
   - Instale plugin Smush ou similar
   - Configure compressão automática
   - Ative lazy loading

### Configuração de Alt Text

1. **Para cada imagem, adicione:**
   - **hero-image.webp:** "Jovem adulta em sessão de terapia online, demonstrando acolhimento e profissionalismo"
   - **meditation-image.jpg:** "Jovem adulto meditando em ambiente tranquilo"
   - **wellbeing-image.jpg:** "Representação visual do bem-estar mental e equilíbrio emocional"

### Responsive Images

1. **Configure Tamanhos Personalizados**
   - Adicione ao functions.php:

```php
// Tamanhos de imagem personalizados
add_image_size('hero-desktop', 600, 400, true);
add_image_size('hero-mobile', 400, 300, true);
add_image_size('service-icon', 100, 100, true);
```

2. **Use Picture Element para Responsividade**
```html
<picture>
    <source media="(max-width: 768px)" srcset="hero-mobile.webp">
    <source media="(min-width: 769px)" srcset="hero-desktop.webp">
    <img src="hero-desktop.webp" alt="Descrição da imagem">
</picture>
```

---


## Configuração de Formulários

### Contact Form 7 (Recomendado)

#### Passo 1: Instalação

1. **Instale o Plugin**
   - `Plugins > Adicionar Novo`
   - Busque: "Contact Form 7"
   - Instale e ative

#### Passo 2: Criar Formulário de Contato

1. **Acesse Contact > Formulários de Contato**
2. **Clique em "Adicionar Novo"**
3. **Configure o Formulário:**

```html
<div class="contact-form">
    <div class="form-row">
        [text* nome placeholder "Seu nome completo"]
    </div>
    <div class="form-row">
        [email* email placeholder "Seu melhor e-mail"]
    </div>
    <div class="form-row">
        [tel telefone placeholder "Seu telefone/WhatsApp"]
    </div>
    <div class="form-row">
        [select* tipo-consulta "Tipo de consulta" "Consulta Online" "Consulta Presencial" "Informações sobre TCC"]
    </div>
    <div class="form-row">
        [textarea mensagem placeholder "Conte um pouco sobre o que você gostaria de trabalhar na terapia (opcional)"]
    </div>
    <div class="form-row">
        [acceptance aceito-termos] Aceito os [link-termos "termos de uso"] e [link-privacidade "política de privacidade"]
    </div>
    <div class="form-submit">
        [submit "Agendar Consulta"]
    </div>
</div>
```

#### Passo 3: Configurar E-mail

1. **Aba "E-mail"**
   - Para: contato@psicologaana.com.br
   - De: [nome] <[email]>
   - Assunto: Nova solicitação de consulta - [tipo-consulta]
   - Corpo da mensagem:
```
Nova solicitação de consulta recebida:

Nome: [nome]
E-mail: [email]
Telefone: [telefone]
Tipo de consulta: [tipo-consulta]

Mensagem:
[mensagem]

---
Enviado através do site psicologaana.com.br
```

#### Passo 4: Integração com WhatsApp

1. **Adicione JavaScript Personalizado:**

```javascript
// Integração WhatsApp
document.addEventListener('DOMContentLoaded', function() {
    // Botões WhatsApp diretos
    const whatsappButtons = document.querySelectorAll('a[href*="wa.me"]');
    
    whatsappButtons.forEach(button => {
        button.addEventListener('click', function(e) {
            // Track evento no Google Analytics
            if (typeof gtag !== 'undefined') {
                gtag('event', 'whatsapp_click', {
                    'event_category': 'contact',
                    'event_label': this.textContent.trim()
                });
            }
        });
    });
});
```

### Formulário de Newsletter (Opcional)

1. **Crie Formulário Simples:**
```html
<div class="newsletter-form">
    [email* email-newsletter placeholder "Seu e-mail para receber dicas de bem-estar"]
    [submit "Inscrever-se"]
</div>
```

---

## Otimização e Performance

### Cache e Minificação

#### WP Rocket (Recomendado)

1. **Configurações Básicas**
   - Cache de página: Ativado
   - Cache mobile: Ativado
   - Cache para usuários logados: Desativado

2. **Otimização de Arquivos**
   - Minificar CSS: Ativado
   - Combinar CSS: Ativado
   - Minificar JavaScript: Ativado
   - Combinar JavaScript: Cuidado com conflitos

3. **Mídia**
   - Lazy Loading: Ativado
   - WebP: Ativado se suportado

#### Alternativa Gratuita: W3 Total Cache

1. **Configurações Gerais**
   - Page Cache: Ativado
   - Minify: Ativado
   - Database Cache: Ativado

### Otimização de Imagens

#### Plugin Smush

1. **Configurações Recomendadas**
   - Compressão: Ativada
   - Redimensionamento: Máximo 1920px largura
   - Lazy Load: Ativado
   - WebP: Ativado

#### Configuração Manual

1. **Formatos Recomendados**
   - Hero images: WebP com fallback JPEG
   - Ícones: SVG quando possível
   - Fotos: WebP ou JPEG otimizado

2. **Tamanhos Apropriados**
   - Desktop: Máximo 1920px largura
   - Mobile: Máximo 768px largura
   - Thumbnails: 300x300px

### CDN (Content Delivery Network)

#### Cloudflare (Gratuito)

1. **Configuração Básica**
   - Adicione domínio ao Cloudflare
   - Configure DNS
   - Ative proxy (nuvem laranja)

2. **Otimizações**
   - Auto Minify: CSS, JavaScript, HTML
   - Brotli: Ativado
   - Cache Level: Standard

---

## SEO e Meta Tags

### Yoast SEO

#### Configuração da Página

1. **Meta Título**
   - "Dra. Ana - Terapia Cognitivo-Comportamental para Ansiedade | TCC São Paulo"
   - Máximo 60 caracteres

2. **Meta Descrição**
   - "Psicóloga especializada em TCC para jovens adultos com ansiedade. Sessões online e presenciais. Agende sua consulta e transforme sua ansiedade em tranquilidade."
   - Máximo 155 caracteres

3. **Palavra-chave Foco**
   - Principal: "terapia cognitivo comportamental ansiedade"
   - Secundárias: "psicóloga TCC", "ansiedade jovens adultos", "terapia online ansiedade"

#### Schema Markup

1. **Dados Estruturados**
```json
{
  "@context": "https://schema.org",
  "@type": "ProfessionalService",
  "name": "Dra. Ana - Psicóloga TCC",
  "description": "Terapia Cognitivo-Comportamental especializada para jovens adultos com ansiedade",
  "url": "https://psicologaana.com.br",
  "telephone": "+5511999999999",
  "address": {
    "@type": "PostalAddress",
    "streetAddress": "Rua das Flores, 123",
    "addressLocality": "São Paulo",
    "addressRegion": "SP",
    "postalCode": "05435-000",
    "addressCountry": "BR"
  },
  "geo": {
    "@type": "GeoCoordinates",
    "latitude": "-23.5505",
    "longitude": "-46.6333"
  },
  "openingHours": [
    "Mo-Fr 08:00-18:00",
    "Sa 08:00-12:00"
  ],
  "priceRange": "$$",
  "serviceType": "Psychological Counseling"
}
```

### Open Graph e Twitter Cards

1. **Meta Tags Adicionais**
```html
<!-- Open Graph -->
<meta property="og:title" content="Dra. Ana - Terapia Cognitivo-Comportamental para Ansiedade">
<meta property="og:description" content="Psicóloga especializada em TCC para jovens adultos com ansiedade. Agende sua consulta.">
<meta property="og:image" content="https://psicologaana.com.br/wp-content/uploads/hero-image.webp">
<meta property="og:url" content="https://psicologaana.com.br">
<meta property="og:type" content="website">

<!-- Twitter Cards -->
<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Dra. Ana - Terapia Cognitivo-Comportamental para Ansiedade">
<meta name="twitter:description" content="Psicóloga especializada em TCC para jovens adultos com ansiedade.">
<meta name="twitter:image" content="https://psicologaana.com.br/wp-content/uploads/hero-image.webp">
```

### Sitemap e Robots.txt

1. **Configuração do Sitemap**
   - Yoast SEO gera automaticamente
   - URL: `https://psicologaana.com.br/sitemap_index.xml`
   - Submeta ao Google Search Console

2. **Robots.txt**
```
User-agent: *
Allow: /

Sitemap: https://psicologaana.com.br/sitemap_index.xml
```

---

## Responsividade

### Breakpoints Principais

1. **Mobile First Approach**
   - Mobile: 320px - 767px
   - Tablet: 768px - 1023px
   - Desktop: 1024px+

### Configurações CSS Responsivas

#### Media Queries Essenciais

```css
/* Mobile */
@media (max-width: 767px) {
    .hero-title {
        font-size: 1.75rem;
        line-height: 1.2;
    }
    
    .hero-container {
        grid-template-columns: 1fr;
        text-align: center;
        gap: 2rem;
    }
    
    .services-grid {
        grid-template-columns: 1fr;
    }
    
    .btn {
        width: 100%;
        justify-content: center;
    }
}

/* Tablet */
@media (min-width: 768px) and (max-width: 1023px) {
    .hero-title {
        font-size: 2.25rem;
    }
    
    .services-grid {
        grid-template-columns: repeat(2, 1fr);
    }
}
```

#### Elementor Responsivo

1. **Configurações por Dispositivo**
   - Desktop: Configuração padrão
   - Tablet: Ajustar espaçamentos e tamanhos
   - Mobile: Stack colunas, aumentar padding

2. **Testes Obrigatórios**
   - iPhone SE (375px)
   - iPhone 12 (390px)
   - iPad (768px)
   - Desktop (1200px+)

---


## Manutenção e Atualizações

### Backup Regular

#### UpdraftPlus (Recomendado)

1. **Configuração de Backup Automático**
   - Frequência: Diário para arquivos, semanal para banco de dados
   - Armazenamento: Google Drive, Dropbox ou Amazon S3
   - Retenção: Manter últimos 30 backups

2. **Backup Manual Antes de Alterações**
   - Sempre antes de atualizar plugins
   - Antes de modificar código
   - Antes de mudanças no tema

### Atualizações de Segurança

#### WordPress Core

1. **Atualizações Automáticas**
   - Ative atualizações automáticas de segurança
   - Configure no wp-config.php:
```php
define('WP_AUTO_UPDATE_CORE', 'minor');
```

#### Plugins e Temas

1. **Cronograma de Atualizações**
   - Verifique semanalmente
   - Teste em ambiente de staging primeiro
   - Mantenha lista de plugins essenciais

### Monitoramento de Performance

#### Ferramentas Recomendadas

1. **Google PageSpeed Insights**
   - Meta: Score 90+ para mobile e desktop
   - Monitore mensalmente

2. **GTmetrix**
   - Tempo de carregamento: < 3 segundos
   - Tamanho da página: < 2MB

3. **Google Analytics**
   - Taxa de rejeição: < 60%
   - Tempo na página: > 2 minutos
   - Conversões: Acompanhe cliques nos CTAs

### Atualizações de Conteúdo

#### Informações que Podem Mudar

1. **Dados de Contato**
   - Telefone e WhatsApp
   - E-mail
   - Endereço do consultório
   - Horários de atendimento

2. **Serviços e Preços**
   - Novos tipos de terapia
   - Workshops e grupos
   - Valores das consultas

3. **Depoimentos**
   - Adicionar novos depoimentos
   - Atualizar casos de sucesso

#### Como Atualizar

1. **Via Elementor**
   - Edite a página diretamente
   - Publique as alterações
   - Teste em diferentes dispositivos

2. **Via Código**
   - Edite os arquivos PHP/HTML
   - Faça backup antes
   - Teste em staging

---

## Solução de Problemas

### Problemas Comuns

#### 1. Página Não Carrega

**Possíveis Causas:**
- Conflito de plugins
- Erro no código personalizado
- Problema de cache
- Limite de memória PHP

**Soluções:**
1. Desative todos os plugins e reative um por vez
2. Verifique logs de erro no cPanel
3. Limpe cache do site e navegador
4. Aumente limite de memória PHP para 256MB

#### 2. Layout Quebrado

**Possíveis Causas:**
- CSS conflitante
- JavaScript com erro
- Imagens não carregam

**Soluções:**
1. Verifique console do navegador (F12)
2. Desative CSS personalizado temporariamente
3. Teste com tema padrão do WordPress
4. Verifique URLs das imagens

#### 3. Formulário Não Funciona

**Possíveis Causas:**
- Plugin Contact Form 7 desativado
- Configuração de e-mail incorreta
- Spam bloqueando envios

**Soluções:**
1. Verifique se plugin está ativo
2. Teste envio de e-mail do WordPress
3. Configure SMTP adequadamente
4. Adicione reCAPTCHA se necessário

#### 4. Site Lento

**Possíveis Causas:**
- Imagens não otimizadas
- Muitos plugins ativos
- Hosting inadequado
- Falta de cache

**Soluções:**
1. Otimize todas as imagens
2. Desative plugins desnecessários
3. Configure cache adequadamente
4. Considere upgrade de hosting

### Logs e Debugging

#### Ativar Debug do WordPress

1. **No wp-config.php:**
```php
define('WP_DEBUG', true);
define('WP_DEBUG_LOG', true);
define('WP_DEBUG_DISPLAY', false);
```

2. **Verificar Logs**
   - Localização: `/wp-content/debug.log`
   - Monitore erros PHP
   - Identifique conflitos

#### Ferramentas de Debug

1. **Query Monitor Plugin**
   - Monitora performance
   - Identifica queries lentas
   - Mostra hooks e filtros

2. **Health Check Plugin**
   - Verifica configuração do WordPress
   - Testa compatibilidade de plugins
   - Modo de resolução de problemas

---

## Recursos Adicionais

### Documentação Oficial

1. **WordPress Codex**
   - https://codex.wordpress.org/
   - Documentação completa do WordPress

2. **Elementor Documentation**
   - https://elementor.com/help/
   - Guias e tutoriais do Elementor

3. **Contact Form 7 Docs**
   - https://contactform7.com/docs/
   - Configuração avançada de formulários

### Ferramentas Úteis

#### Desenvolvimento

1. **Local by Flywheel**
   - Ambiente local para WordPress
   - Teste mudanças antes de aplicar

2. **Staging Environment**
   - Crie ambiente de teste
   - Muitos hosts oferecem staging

#### Análise e Monitoramento

1. **Google Search Console**
   - Monitore indexação
   - Identifique problemas de SEO

2. **Google Analytics**
   - Acompanhe tráfego
   - Meça conversões

3. **Hotjar ou Similar**
   - Heatmaps de cliques
   - Gravações de sessões

### Suporte Técnico

#### Quando Buscar Ajuda

1. **Problemas Técnicos Complexos**
   - Erros de servidor
   - Problemas de segurança
   - Performance muito baixa

2. **Customizações Avançadas**
   - Integrações com sistemas externos
   - Funcionalidades específicas
   - Automações complexas

#### Onde Buscar Ajuda

1. **Fóruns WordPress**
   - https://br.forums.wordpress.org/
   - Comunidade ativa em português

2. **Suporte do Hosting**
   - Problemas de servidor
   - Configurações técnicas

3. **Desenvolvedores WordPress**
   - Freelancers especializados
   - Agências de desenvolvimento

---

## Checklist de Implementação

### Antes de Começar

- [ ] Backup completo do site
- [ ] Acesso ao painel administrativo
- [ ] Plugins necessários instalados
- [ ] Imagens otimizadas e prontas
- [ ] Textos revisados e aprovados

### Durante a Implementação

- [ ] Página criada no WordPress
- [ ] Template ou Elementor configurado
- [ ] Todas as seções implementadas
- [ ] Imagens inseridas com alt text
- [ ] Links funcionando corretamente
- [ ] Formulários testados

### Após a Implementação

- [ ] Teste em diferentes dispositivos
- [ ] Verificação de velocidade
- [ ] SEO configurado
- [ ] Analytics instalado
- [ ] Backup da versão final
- [ ] Documentação entregue

### Testes Finais

- [ ] Navegação entre seções
- [ ] Responsividade mobile
- [ ] Formulários de contato
- [ ] Links para WhatsApp
- [ ] Carregamento de imagens
- [ ] Performance geral

---

## Conclusão

Esta documentação fornece um guia completo para implementar a landing page da Dra. Ana em WordPress. Seguindo estas instruções, você terá uma página profissional, otimizada e funcional que atende aos objetivos de conversão estabelecidos.

### Próximos Passos Recomendados

1. **Implementação Gradual**
   - Comece com a estrutura básica
   - Adicione seções progressivamente
   - Teste cada etapa

2. **Otimização Contínua**
   - Monitore métricas de performance
   - Teste diferentes versões dos CTAs
   - Colete feedback dos usuários

3. **Manutenção Regular**
   - Atualize conteúdo conforme necessário
   - Mantenha plugins atualizados
   - Monitore segurança

### Contato para Suporte

Para dúvidas sobre esta implementação ou suporte técnico adicional, consulte os recursos mencionados nesta documentação ou entre em contato com um desenvolvedor WordPress qualificado.

---

**Versão da Documentação:** 1.0  
**Última Atualização:** 15 de julho de 2025  
**Autor:** Manus AI  
**Licença:** Uso exclusivo para o projeto Dra. Ana

