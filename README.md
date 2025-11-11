# CSS 3 - Tutorial sobre Cores

Tutorial completo sobre cores em CSS 3 para iniciantes.

## 📑 Sumário

1. [Introdução](#introdução)
2. [Sistemas de Cores em CSS](#sistemas-de-cores-em-css)
   - [Cores por Nome](#1-cores-por-nome)
   - [Cores Hexadecimais](#2-cores-hexadecimais)
   - [RGB - Red, Green, Blue](#3-rgb---red-green-blue)
   - [RGBA - RGB com Transparência](#4-rgba---rgb-com-transparência)
   - [HSL - Hue, Saturation, Lightness](#5-hsl---hue-saturation-lightness)
3. [Aplicando Cores no CSS](#aplicando-cores-no-css)
   - [Cor do Texto](#cor-do-texto)
   - [Cor de Fundo](#cor-de-fundo)
   - [Outras Propriedades com Cores](#outras-propriedades-com-cores)
4. [Gradientes CSS](#gradientes-css)
   - [Gradiente Linear](#gradiente-linear-linear-gradient)
   - [Gradiente Radial](#gradiente-radial-radial-gradient)
   - [Gradientes Avançados](#gradientes-avançados)
5. [Exemplo Completo](#exemplo-completo)
6. [Recursos e Links Úteis](#recursos-e-links-úteis)

---

## Introdução

As cores são elementos fundamentais no design web. No CSS 3, existem diversas formas de especificar cores, cada uma com suas vantagens e casos de uso específicos. Este tutorial aborda os principais sistemas de cores e como aplicá-los em seus projetos.

---

## Sistemas de Cores em CSS

### 1. Cores por Nome

CSS possui 140 cores nomeadas predefinidas. É a forma mais simples de especificar cores.

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .red-text { color: red; }
        .blue-bg { background-color: blue; color: white; }
        .green-box { background-color: green; padding: 10px; }
    </style>
</head>
<body>
    <p class="red-text">Este texto é vermelho</p>
    <p class="blue-bg">Este texto tem fundo azul</p>
    <div class="green-box">Esta caixa tem fundo verde</div>
</body>
</html>
```

**Cores comuns:**
- `red`, `blue`, `green`, `yellow`, `orange`
- `black`, `white`, `gray`
- `pink`, `purple`, `brown`
- `cyan`, `magenta`, `lime`

---

### 2. Cores Hexadecimais

Sistema que usa valores hexadecimais (base 16) para representar cores. O formato é `#RRGGBB` onde:
- RR = componente vermelho (00-FF)
- GG = componente verde (00-FF)
- BB = componente azul (00-FF)

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .hex-red { color: #FF0000; }
        .hex-blue { color: #0000FF; }
        .hex-custom { 
            background-color: #FF6B6B;
            color: #FFFFFF;
            padding: 15px;
        }
        .hex-short { color: #F00; } /* Forma abreviada de #FF0000 */
    </style>
</head>
<body>
    <p class="hex-red">Vermelho em hexadecimal: #FF0000</p>
    <p class="hex-blue">Azul em hexadecimal: #0000FF</p>
    <div class="hex-custom">Cor personalizada: #FF6B6B</div>
    <p class="hex-short">Forma abreviada: #F00</p>
</body>
</html>
```

**Valores úteis:**
- `#000000` - Preto
- `#FFFFFF` - Branco
- `#FF0000` - Vermelho
- `#00FF00` - Verde
- `#0000FF` - Azul
- `#808080` - Cinza

---

### 3. RGB - Red, Green, Blue

Define cores usando valores de vermelho, verde e azul (0-255 para cada componente).

**Sintaxe:** `rgb(red, green, blue)`

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .rgb-red { color: rgb(255, 0, 0); }
        .rgb-green { color: rgb(0, 255, 0); }
        .rgb-blue { color: rgb(0, 0, 255); }
        .rgb-custom {
            background-color: rgb(100, 149, 237);
            color: rgb(255, 255, 255);
            padding: 15px;
            margin: 10px 0;
        }
        .rgb-gray { background-color: rgb(128, 128, 128); }
    </style>
</head>
<body>
    <p class="rgb-red">Vermelho RGB: rgb(255, 0, 0)</p>
    <p class="rgb-green">Verde RGB: rgb(0, 255, 0)</p>
    <p class="rgb-blue">Azul RGB: rgb(0, 0, 255)</p>
    <div class="rgb-custom">Azul personalizado: rgb(100, 149, 237)</div>
</body>
</html>
```

---

### 4. RGBA - RGB com Transparência

Similar ao RGB, mas adiciona um canal alpha para controlar a transparência (0.0 a 1.0).

**Sintaxe:** `rgba(red, green, blue, alpha)`

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        body { background-color: #f0f0f0; }
        
        .rgba-box {
            width: 200px;
            height: 100px;
            margin: 10px;
            padding: 20px;
            color: white;
            font-weight: bold;
        }
        
        .rgba-solid { background-color: rgba(255, 0, 0, 1.0); }
        .rgba-75 { background-color: rgba(255, 0, 0, 0.75); }
        .rgba-50 { background-color: rgba(255, 0, 0, 0.5); }
        .rgba-25 { background-color: rgba(255, 0, 0, 0.25); }
        
        .overlay {
            position: relative;
            background-image: url('https://via.placeholder.com/400x300');
        }
        
        .overlay-text {
            background-color: rgba(0, 0, 0, 0.7);
            color: white;
            padding: 20px;
        }
    </style>
</head>
<body>
    <h2>Níveis de Transparência</h2>
    <div class="rgba-box rgba-solid">Alpha: 1.0 (100%)</div>
    <div class="rgba-box rgba-75">Alpha: 0.75 (75%)</div>
    <div class="rgba-box rgba-50">Alpha: 0.5 (50%)</div>
    <div class="rgba-box rgba-25">Alpha: 0.25 (25%)</div>
    
    <div class="overlay">
        <div class="overlay-text">
            Texto com fundo semi-transparente
        </div>
    </div>
</body>
</html>
```

---

### 5. HSL - Hue, Saturation, Lightness

Sistema intuitivo baseado em:
- **Hue (Matiz)**: ângulo na roda de cores (0-360)
- **Saturation (Saturação)**: intensidade da cor (0%-100%)
- **Lightness (Luminosidade)**: claridade da cor (0%-100%)

**Sintaxe:** `hsl(hue, saturation%, lightness%)`

Também existe **HSLA** com transparência: `hsla(hue, saturation%, lightness%, alpha)`

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .hsl-box {
            padding: 15px;
            margin: 10px 0;
            color: white;
            font-weight: bold;
        }
        
        /* Matizes diferentes (variando Hue) */
        .hsl-red { background-color: hsl(0, 100%, 50%); }
        .hsl-orange { background-color: hsl(30, 100%, 50%); }
        .hsl-yellow { background-color: hsl(60, 100%, 50%); }
        .hsl-green { background-color: hsl(120, 100%, 50%); }
        .hsl-blue { background-color: hsl(240, 100%, 50%); }
        .hsl-purple { background-color: hsl(280, 100%, 50%); }
        
        /* Variando Saturação */
        .hsl-sat-100 { background-color: hsl(200, 100%, 50%); }
        .hsl-sat-75 { background-color: hsl(200, 75%, 50%); }
        .hsl-sat-50 { background-color: hsl(200, 50%, 50%); }
        .hsl-sat-25 { background-color: hsl(200, 25%, 50%); }
        
        /* Variando Luminosidade */
        .hsl-light-80 { background-color: hsl(200, 100%, 80%); color: black; }
        .hsl-light-60 { background-color: hsl(200, 100%, 60%); }
        .hsl-light-40 { background-color: hsl(200, 100%, 40%); }
        .hsl-light-20 { background-color: hsl(200, 100%, 20%); }
        
        /* HSLA com transparência */
        .hsla-trans { 
            background-color: hsla(120, 100%, 50%, 0.5);
            padding: 20px;
        }
    </style>
</head>
<body>
    <h2>Variação de Matiz (Hue)</h2>
    <div class="hsl-box hsl-red">Vermelho: hsl(0, 100%, 50%)</div>
    <div class="hsl-box hsl-orange">Laranja: hsl(30, 100%, 50%)</div>
    <div class="hsl-box hsl-yellow">Amarelo: hsl(60, 100%, 50%)</div>
    <div class="hsl-box hsl-green">Verde: hsl(120, 100%, 50%)</div>
    <div class="hsl-box hsl-blue">Azul: hsl(240, 100%, 50%)</div>
    <div class="hsl-box hsl-purple">Roxo: hsl(280, 100%, 50%)</div>
    
    <h2>Variação de Saturação</h2>
    <div class="hsl-box hsl-sat-100">Saturação 100%</div>
    <div class="hsl-box hsl-sat-75">Saturação 75%</div>
    <div class="hsl-box hsl-sat-50">Saturação 50%</div>
    <div class="hsl-box hsl-sat-25">Saturação 25%</div>
    
    <h2>Variação de Luminosidade</h2>
    <div class="hsl-box hsl-light-80">Luminosidade 80%</div>
    <div class="hsl-box hsl-light-60">Luminosidade 60%</div>
    <div class="hsl-box hsl-light-40">Luminosidade 40%</div>
    <div class="hsl-box hsl-light-20">Luminosidade 20%</div>
    
    <h2>HSLA com Transparência</h2>
    <div class="hsla-trans">hsla(120, 100%, 50%, 0.5)</div>
</body>
</html>
```

---

## Aplicando Cores no CSS

### Cor do Texto

Use a propriedade `color` para definir a cor do texto.

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .text-red { color: red; }
        .text-hex { color: #3498db; }
        .text-rgb { color: rgb(231, 76, 60); }
        .text-hsl { color: hsl(280, 70%, 50%); }
        
        .paragraph {
            font-size: 18px;
            margin: 15px 0;
        }
        
        /* Diferentes partes do texto */
        .highlight { color: #e74c3c; }
        .emphasis { color: #2ecc71; font-weight: bold; }
    </style>
</head>
<body>
    <p class="paragraph text-red">Texto em vermelho usando nome</p>
    <p class="paragraph text-hex">Texto azul usando hexadecimal #3498db</p>
    <p class="paragraph text-rgb">Texto vermelho usando RGB</p>
    <p class="paragraph text-hsl">Texto roxo usando HSL</p>
    
    <p class="paragraph">
        Você pode combinar 
        <span class="highlight">diferentes cores</span>
        no mesmo parágrafo para 
        <span class="emphasis">dar ênfase</span>
        em partes específicas.
    </p>
</body>
</html>
```

---

### Cor de Fundo

Use a propriedade `background-color` para definir a cor de fundo de elementos.

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        body {
            background-color: #f5f5f5;
            font-family: Arial, sans-serif;
        }
        
        .bg-section {
            padding: 20px;
            margin: 15px 0;
            border-radius: 8px;
        }
        
        .bg-blue {
            background-color: #3498db;
            color: white;
        }
        
        .bg-green {
            background-color: rgb(46, 204, 113);
            color: white;
        }
        
        .bg-yellow {
            background-color: hsl(48, 100%, 67%);
            color: #333;
        }
        
        .bg-transparent {
            background-color: rgba(52, 152, 219, 0.3);
            color: #333;
        }
        
        /* Combinando cores de texto e fundo */
        .card {
            background-color: white;
            color: #333;
            padding: 20px;
            margin: 15px 0;
            border-left: 5px solid #e74c3c;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }
        
        .card-title {
            color: #e74c3c;
            margin-top: 0;
        }
    </style>
</head>
<body>
    <div class="bg-section bg-blue">
        Fundo azul usando hexadecimal
    </div>
    
    <div class="bg-section bg-green">
        Fundo verde usando RGB
    </div>
    
    <div class="bg-section bg-yellow">
        Fundo amarelo usando HSL
    </div>
    
    <div class="bg-section bg-transparent">
        Fundo semi-transparente usando RGBA
    </div>
    
    <div class="card">
        <h3 class="card-title">Card Estilizado</h3>
        <p>Exemplo de combinação de cores de texto e fundo para criar um card atraente.</p>
    </div>
</body>
</html>
```

---

### Outras Propriedades com Cores

Além de `color` e `background-color`, várias outras propriedades CSS aceitam valores de cor.

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        /* Bordas */
        .border-example {
            border: 3px solid #3498db;
            padding: 15px;
            margin: 10px 0;
        }
        
        /* Sombras de texto */
        .text-shadow-example {
            font-size: 32px;
            color: #2c3e50;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
        }
        
        /* Sombras de caixa */
        .box-shadow-example {
            background-color: white;
            padding: 20px;
            margin: 20px 0;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        /* Outline */
        .outline-example {
            outline: 3px dashed #e74c3c;
            outline-offset: 5px;
            padding: 15px;
            margin: 20px 0;
        }
        
        /* Bordas múltiplas */
        .multi-border {
            border-top: 4px solid #e74c3c;
            border-right: 4px solid #3498db;
            border-bottom: 4px solid #2ecc71;
            border-left: 4px solid #f39c12;
            padding: 20px;
            margin: 20px 0;
        }
    </style>
</head>
<body>
    <div class="border-example">
        Elemento com borda colorida: border: 3px solid #3498db;
    </div>
    
    <div class="text-shadow-example">
        Texto com Sombra
    </div>
    
    <div class="box-shadow-example">
        Caixa com sombra usando RGBA para transparência
    </div>
    
    <div class="outline-example">
        Elemento com outline (contorno externo)
    </div>
    
    <div class="multi-border">
        Bordas com cores diferentes em cada lado
    </div>
</body>
</html>
```

---

## Gradientes CSS

Gradientes permitem criar transições suaves entre duas ou mais cores.

### Gradiente Linear (linear-gradient)

Cria um gradiente em linha reta.

**Sintaxe básica:**
```css
background: linear-gradient(direção, cor1, cor2, ...);
```

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .gradient-box {
            height: 150px;
            margin: 15px 0;
            padding: 20px;
            color: white;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
        }
        
        /* Gradiente vertical (padrão) */
        .gradient-vertical {
            background: linear-gradient(#3498db, #2ecc71);
        }
        
        /* Gradiente horizontal */
        .gradient-horizontal {
            background: linear-gradient(to right, #e74c3c, #f39c12);
        }
        
        /* Gradiente diagonal */
        .gradient-diagonal {
            background: linear-gradient(45deg, #9b59b6, #3498db);
        }
        
        /* Gradiente com múltiplas cores */
        .gradient-multi {
            background: linear-gradient(to right, #e74c3c, #f39c12, #2ecc71, #3498db, #9b59b6);
        }
        
        /* Gradiente com pontos de parada */
        .gradient-stops {
            background: linear-gradient(to right, 
                #3498db 0%, 
                #3498db 30%, 
                #e74c3c 30%, 
                #e74c3c 100%
            );
        }
        
        /* Gradiente com transparência */
        .gradient-transparent {
            background-color: #3498db;
            background-image: linear-gradient(
                to bottom, 
                rgba(255, 255, 255, 0), 
                rgba(0, 0, 0, 0.5)
            );
        }
    </style>
</head>
<body>
    <h2>Gradientes Lineares</h2>
    
    <div class="gradient-box gradient-vertical">
        Gradiente Vertical (top to bottom)
    </div>
    
    <div class="gradient-box gradient-horizontal">
        Gradiente Horizontal (left to right)
    </div>
    
    <div class="gradient-box gradient-diagonal">
        Gradiente Diagonal (45deg)
    </div>
    
    <div class="gradient-box gradient-multi">
        Gradiente com Múltiplas Cores
    </div>
    
    <div class="gradient-box gradient-stops">
        Gradiente com Pontos de Parada Definidos
    </div>
    
    <div class="gradient-box gradient-transparent">
        Gradiente com Transparência
    </div>
</body>
</html>
```

---

### Gradiente Radial (radial-gradient)

Cria um gradiente circular a partir de um ponto central.

**Sintaxe básica:**
```css
background: radial-gradient(forma tamanho at posição, cor1, cor2, ...);
```

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .radial-box {
            height: 200px;
            margin: 15px 0;
            padding: 20px;
            color: white;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
        }
        
        /* Gradiente radial simples */
        .radial-simple {
            background: radial-gradient(#3498db, #2c3e50);
        }
        
        /* Gradiente radial circular */
        .radial-circle {
            background: radial-gradient(circle, #e74c3c, #c0392b, #000);
        }
        
        /* Gradiente radial elíptico */
        .radial-ellipse {
            background: radial-gradient(ellipse, #2ecc71, #27ae60, #16a085);
        }
        
        /* Gradiente radial posicionado */
        .radial-positioned {
            background: radial-gradient(circle at top left, #f39c12, #e67e22, #d35400);
        }
        
        /* Gradiente radial com tamanho */
        .radial-sized {
            background: radial-gradient(circle closest-side at 50% 50%, #9b59b6, #8e44ad, #2c3e50);
        }
        
        /* Múltiplos gradientes radiais */
        .radial-multi {
            background: 
                radial-gradient(circle at 20% 50%, rgba(255, 0, 0, 0.5), transparent 50%),
                radial-gradient(circle at 80% 50%, rgba(0, 0, 255, 0.5), transparent 50%),
                #2c3e50;
        }
    </style>
</head>
<body>
    <h2>Gradientes Radiais</h2>
    
    <div class="radial-box radial-simple">
        Gradiente Radial Simples
    </div>
    
    <div class="radial-box radial-circle">
        Gradiente Radial Circular
    </div>
    
    <div class="radial-box radial-ellipse">
        Gradiente Radial Elíptico
    </div>
    
    <div class="radial-box radial-positioned">
        Gradiente Radial Posicionado (top left)
    </div>
    
    <div class="radial-box radial-sized">
        Gradiente Radial com Tamanho Definido
    </div>
    
    <div class="radial-box radial-multi">
        Múltiplos Gradientes Radiais
    </div>
</body>
</html>
```

---

### Gradientes Avançados

**Exemplos de código:**

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <style>
        .advanced-box {
            height: 200px;
            margin: 15px 0;
            padding: 20px;
            color: white;
            font-weight: bold;
            display: flex;
            align-items: center;
            justify-content: center;
            border-radius: 8px;
            text-align: center;
        }
        
        /* Gradiente repetido linear */
        .repeating-linear {
            background: repeating-linear-gradient(
                45deg,
                #3498db,
                #3498db 10px,
                #2c3e50 10px,
                #2c3e50 20px
            );
        }
        
        /* Gradiente repetido radial */
        .repeating-radial {
            background: repeating-radial-gradient(
                circle,
                #e74c3c,
                #e74c3c 10px,
                #c0392b 10px,
                #c0392b 20px
            );
        }
        
        /* Gradiente cônico (conic-gradient) */
        .conic-gradient {
            background: conic-gradient(
                from 0deg,
                red, yellow, lime, cyan, blue, magenta, red
            );
        }
        
        /* Combinação de gradientes */
        .combined {
            background: 
                linear-gradient(45deg, transparent 30%, rgba(255, 255, 255, 0.3) 30%),
                linear-gradient(-45deg, transparent 30%, rgba(255, 255, 255, 0.3) 30%),
                linear-gradient(to bottom, #3498db, #2c3e50);
        }
    </style>
</head>
<body>
    <h2>Gradientes Avançados</h2>
    
    <div class="advanced-box repeating-linear">
        Gradiente Linear Repetido<br>(Listras Diagonais)
    </div>
    
    <div class="advanced-box repeating-radial">
        Gradiente Radial Repetido<br>(Anéis Concêntricos)
    </div>
    
    <div class="advanced-box conic-gradient">
        Gradiente Cônico<br>(Roda de Cores)
    </div>
    
    <div class="advanced-box combined">
        Combinação de Múltiplos Gradientes
    </div>
</body>
</html>
```

---

## Exemplo Completo

Aqui está um exemplo completo que integra todos os conceitos aprendidos neste tutorial:

```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CSS3 Cores - Exemplo Completo</title>
    <style>
        /* Reset básico */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        /* Body com gradiente de fundo */
        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }
        
        /* Container principal */
        .container {
            max-width: 1200px;
            margin: 0 auto;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 15px;
            padding: 40px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
        }
        
        /* Cabeçalho */
        header {
            text-align: center;
            margin-bottom: 40px;
        }
        
        h1 {
            color: #2c3e50;
            font-size: 2.5em;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
        }
        
        .subtitle {
            color: #7f8c8d;
            font-size: 1.2em;
        }
        
        /* Grade de cartões */
        .card-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 25px;
            margin-bottom: 30px;
        }
        
        /* Estilos de cartões usando diferentes sistemas de cores */
        .card {
            border-radius: 10px;
            padding: 25px;
            color: white;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
            cursor: pointer;
        }
        
        .card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
        }
        
        .card h3 {
            margin-bottom: 15px;
            font-size: 1.5em;
        }
        
        .card p {
            line-height: 1.6;
        }
        
        /* Card 1: Nome de cor */
        .card-1 {
            background-color: tomato;
        }
        
        /* Card 2: Hexadecimal */
        .card-2 {
            background-color: #3498db;
        }
        
        /* Card 3: RGB */
        .card-3 {
            background-color: rgb(46, 204, 113);
        }
        
        /* Card 4: RGBA com transparência */
        .card-4 {
            background-color: rgba(155, 89, 182, 0.9);
        }
        
        /* Card 5: HSL */
        .card-5 {
            background-color: hsl(48, 100%, 50%);
            color: #333;
        }
        
        /* Card 6: HSLA */
        .card-6 {
            background-color: hsla(14, 100%, 53%, 0.85);
        }
        
        /* Seção de gradientes */
        .gradient-section {
            margin-top: 40px;
        }
        
        .gradient-section h2 {
            color: #2c3e50;
            margin-bottom: 20px;
            font-size: 2em;
        }
        
        .gradient-showcase {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 20px;
        }
        
        .gradient-item {
            height: 150px;
            border-radius: 10px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: white;
            font-weight: bold;
            text-align: center;
            padding: 20px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        }
        
        .gradient-1 {
            background: linear-gradient(45deg, #ff6b6b, #ee5a6f);
        }
        
        .gradient-2 {
            background: linear-gradient(135deg, #667eea, #764ba2);
        }
        
        .gradient-3 {
            background: radial-gradient(circle, #f093fb, #f5576c);
        }
        
        .gradient-4 {
            background: linear-gradient(to right, #4facfe, #00f2fe);
        }
        
        .gradient-5 {
            background: conic-gradient(
                from 0deg,
                #ff6b6b, #feca57, #48dbfb, #ff9ff3, #ff6b6b
            );
        }
        
        .gradient-6 {
            background: repeating-linear-gradient(
                45deg,
                #2ecc71,
                #2ecc71 10px,
                #27ae60 10px,
                #27ae60 20px
            );
        }
        
        /* Painel de informações */
        .info-panel {
            margin-top: 40px;
            background: linear-gradient(to right, #141e30, #243b55);
            color: white;
            padding: 30px;
            border-radius: 10px;
        }
        
        .info-panel h2 {
            color: #3498db;
            margin-bottom: 15px;
        }
        
        .info-panel ul {
            list-style-position: inside;
            line-height: 2;
        }
        
        .info-panel li {
            color: rgba(255, 255, 255, 0.9);
        }
        
        /* Rodapé */
        footer {
            margin-top: 40px;
            text-align: center;
            color: #7f8c8d;
            padding-top: 20px;
            border-top: 2px solid #ecf0f1;
        }
        
        .tag {
            display: inline-block;
            background-color: #e74c3c;
            color: white;
            padding: 5px 10px;
            border-radius: 5px;
            margin: 5px;
            font-size: 0.9em;
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1>🎨 CSS3: Trabalhando com Cores</h1>
            <p class="subtitle">Exemplo completo de todos os sistemas de cores</p>
        </header>
        
        <section>
            <h2 style="color: #2c3e50; margin-bottom: 20px;">Sistemas de Cores</h2>
            <div class="card-grid">
                <div class="card card-1">
                    <h3>Nome da Cor</h3>
                    <p>background-color: tomato;</p>
                    <p>Forma mais simples e intuitiva de definir cores.</p>
                </div>
                
                <div class="card card-2">
                    <h3>Hexadecimal</h3>
                    <p>background-color: #3498db;</p>
                    <p>Sistema tradicional usado por designers.</p>
                </div>
                
                <div class="card card-3">
                    <h3>RGB</h3>
                    <p>background-color: rgb(46, 204, 113);</p>
                    <p>Define cores por valores de Vermelho, Verde e Azul.</p>
                </div>
                
                <div class="card card-4">
                    <h3>RGBA</h3>
                    <p>background-color: rgba(155, 89, 182, 0.9);</p>
                    <p>RGB com controle de transparência (alpha).</p>
                </div>
                
                <div class="card card-5">
                    <h3>HSL</h3>
                    <p>background-color: hsl(48, 100%, 50%);</p>
                    <p>Baseado em Matiz, Saturação e Luminosidade.</p>
                </div>
                
                <div class="card card-6">
                    <h3>HSLA</h3>
                    <p>background-color: hsla(14, 100%, 53%, 0.85);</p>
                    <p>HSL com controle de transparência.</p>
                </div>
            </div>
        </section>
        
        <section class="gradient-section">
            <h2>Gradientes CSS</h2>
            <div class="gradient-showcase">
                <div class="gradient-item gradient-1">
                    Gradiente Linear<br>45deg
                </div>
                <div class="gradient-item gradient-2">
                    Gradiente Linear<br>135deg
                </div>
                <div class="gradient-item gradient-3">
                    Gradiente Radial<br>Circle
                </div>
                <div class="gradient-item gradient-4">
                    Gradiente Horizontal<br>Left to Right
                </div>
                <div class="gradient-item gradient-5">
                    Gradiente Cônico<br>Color Wheel
                </div>
                <div class="gradient-item gradient-6">
                    Gradiente Repetido<br>Stripes
                </div>
            </div>
        </section>
        
        <section class="info-panel">
            <h2>💡 Dicas para Trabalhar com Cores</h2>
            <ul>
                <li>Use nomes de cores para prototipagem rápida</li>
                <li>Hexadecimal é ótimo para ferramentas de design</li>
                <li>RGB/RGBA é ideal quando você precisa de transparência</li>
                <li>HSL é perfeito para criar variações de uma mesma cor</li>
                <li>Gradientes adicionam profundidade e modernidade ao design</li>
                <li>Sempre teste o contraste entre texto e fundo para acessibilidade</li>
            </ul>
        </section>
        
        <footer>
            <p><strong>Conceitos aplicados neste exemplo:</strong></p>
            <div>
                <span class="tag">Color Names</span>
                <span class="tag">Hexadecimal</span>
                <span class="tag">RGB</span>
                <span class="tag">RGBA</span>
                <span class="tag">HSL</span>
                <span class="tag">HSLA</span>
                <span class="tag">Linear Gradient</span>
                <span class="tag">Radial Gradient</span>
                <span class="tag">Conic Gradient</span>
                <span class="tag">Box Shadow</span>
                <span class="tag">Text Shadow</span>
            </div>
        </footer>
    </div>
</body>
</html>
```

---

## Recursos e Links Úteis

### 📚 Documentação Oficial

- [MDN Web Docs - CSS Colors](https://developer.mozilla.org/pt-BR/docs/Web/CSS/color_value) - Documentação completa sobre valores de cores em CSS
- [MDN - CSS Gradients](https://developer.mozilla.org/pt-BR/docs/Web/CSS/CSS_Images/Using_CSS_gradients) - Guia completo sobre gradientes
- [W3C CSS Color Module](https://www.w3.org/TR/css-color-3/) - Especificação oficial do W3C

### 🛠️ Ferramentas Úteis

- [Adobe Color](https://color.adobe.com/) - Crie paletas de cores harmoniosas
- [Coolors](https://coolors.co/) - Gerador de paletas de cores
- [CSS Gradient Generator](https://cssgradient.io/) - Crie gradientes visualmente
- [ColorZilla](https://www.colorzilla.com/) - Extensão de navegador para capturar cores
- [Paletton](https://paletton.com/) - Ferramenta avançada para esquemas de cores
- [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/) - Verificador de contraste para acessibilidade

### 📖 Tutoriais e Guias Avançados

1. **Teoria das Cores para Web Design**
   - Psicologia das cores
   - Harmonias cromáticas
   - Cores complementares e análogas

2. **CSS Color Functions (Avançado)**
   - `color-mix()` - Mistura de cores
   - `color-contrast()` - Contraste automático
   - Variáveis CSS com cores

3. **Acessibilidade com Cores**
   - WCAG 2.1 Guidelines
   - Contraste de cores adequado
   - Daltonismo e design inclusivo

4. **Animações com Cores**
   - Transições de cores suaves
   - Animações de gradientes
   - Efeitos hover com cores

5. **Modo Escuro (Dark Mode)**
   - Implementação de temas claro/escuro
   - CSS Variables para temas
   - `prefers-color-scheme` media query

### 🎓 Cursos e Vídeos

- [CSS Color Properties - W3Schools](https://www.w3schools.com/css/css_colors.asp)
- [CSS Gradient Tutorial - YouTube](https://www.youtube.com/results?search_query=css+gradient+tutorial)
- [Web Design Color Theory - Coursera](https://www.coursera.org/)

### 🔗 Artigos Recomendados

- "Understanding CSS Color Spaces" - Explorando espaços de cor modernos
- "The Science of Color in Web Design" - Como as cores afetam a experiência do usuário
- "CSS Custom Properties and Colors" - Usando variáveis CSS para gerenciar cores
- "Building a Design System with CSS Colors" - Criando sistemas de design escaláveis

### 💡 Tópicos Avançados para Estudo

1. **LCH e Lab Color Spaces** - Novos espaços de cor em CSS
2. **CSS Color Module Level 4** - Recursos futuros de cores
3. **Color Blending Modes** - Modos de mistura de cores
4. **SVG Color Manipulation** - Trabalhando com cores em SVG
5. **Performance com Gradientes** - Otimização de gradientes complexos

### 🌐 Comunidades e Fóruns

- [Stack Overflow - CSS Tag](https://stackoverflow.com/questions/tagged/css)
- [CSS-Tricks](https://css-tricks.com/)
- [CodePen](https://codepen.io/) - Explore exemplos práticos
- [Reddit - r/webdev](https://www.reddit.com/r/webdev/)

---

## 📝 Conclusão

Este tutorial cobriu os fundamentos essenciais sobre cores em CSS3, desde sistemas básicos de cores até gradientes avançados. Com esses conhecimentos, você está preparado para criar designs web modernos e atraentes. Continue praticando e explorando os recursos avançados para aprimorar suas habilidades!

**Bons estudos! 🚀**
