# agrinho2026
<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Projeto Agrinho 2026</title>

<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;600&family=Roboto:wght@300;500&display=swap" rel="stylesheet">

<style>
/* Reset básico */
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family: 'Roboto', sans-serif;
}

body{
    background: #f8f9fa;
    color:#333;
    line-height:1.6;
    transition: background 0.3s, color 0.3s;
}

/* Header moderno */
header{
    background: linear-gradient(135deg, #4CAF50, #2E7D32);
    color:white;
    text-align:center;
    padding:60px 20px;
    border-bottom-left-radius: 30px;
    border-bottom-right-radius: 30px;
    box-shadow: 0 5px 15px rgba(0,0,0,0.2);
}

header h1{
    font-family: 'Montserrat', sans-serif;
    font-size:2.8rem;
    margin-bottom:10px;
}

header p{
    font-size:1.2rem;
    opacity:0.9;
}

/* Menu de navegação clean */
nav{
    display:flex;
    justify-content:center;
    gap:30px;
    padding:20px 10px;
    background:#fff;
    box-shadow: 0 2px 8px rgba(0,0,0,0.1);
    position: sticky;
    top:0;
    z-index:100;
}

nav a{
    text-decoration:none;
    color:#2E7D32;
    font-weight:600;
    padding:8px 16px;
    border-radius:8px;
    transition: all 0.3s;
}

nav a:hover{
    background:#E8F5E9;
}

/* Seções */
section{
    max-width:1000px;
    margin:50px auto;
    padding:0 20px;
}

/* Cartões elegantes */
.card{
    background:white;
    padding:30px;
    margin:20px 0;
    border-radius:20px;
    box-shadow:0 8px 20px rgba(0,0,0,0.1);
    transition: transform 0.3s, box-shadow 0.3s;
}

.card:hover{
    transform: translateY(-5px);
    box-shadow:0 12px 25px rgba(0,0,0,0.15);
}

.card h2{
    font-family: 'Montserrat', sans-serif;
    color:#2E7D32;
    margin-bottom:15px;
}

.card p{
    font-size:1rem;
    opacity:0.85;
}

/* Botão moderno */
button{
    background: #2E7D32;
    color:white;
    border:none;
    padding:12px 25px;
    border-radius:12px;
    font-size:1rem;
    cursor:pointer;
    transition: all 0.3s;
}

button:hover{
    background: #1B5E20;
    transform: scale(1.05);
}

/* Footer elegante */
footer{
    text-align:center;
    background:#2E7D32;
    color:white;
    padding:30px 20px;
    border-top-left-radius: 30px;
    border-top-right-radius: 30px;
    margin-top:50px;
}

/* Responsividade */
@media(max-width:768px){
    header h1{
        font-size:2rem;
    }
    nav{
        flex-direction: column;
        gap:15px;
    }
}

/* --- Aba de acessibilidade --- */
#a11y-bar{
    position: fixed;
    right: 20px;
    bottom: 20px;
    background: #2E7D32;
    color:white;
    padding:15px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.3);
    z-index:200;
    font-size:0.9rem;
    width:200px;
}

#a11y-bar h3{
    margin-bottom:10px;
    font-size:1rem;
    text-align:center;
}

#a11y-bar button{
    display:block;
    width:100%;
    margin:5px 0;
    font-size:0.9rem;
}

/* Tema escuro */
body.dark{
    background:#121212;
    color:#e0e0e0;
}

body.dark nav{
    background:#1b1b1b;
}

body.dark nav a{
    color:#a5d6a7;
}

body.dark nav a:hover{
    background:#2e2e2e;
}

body.dark header{
    background: linear-gradient(135deg, #1b5e20, #388e3c);
}

body.dark .card{
    background:#1e1e1e;
    color:#e0e0e0;
}

body.dark footer{
    background:#1b5e20;
}

</style>
</head>
<body>

<header>
    <h1>Projeto Agrinho 2026</h1>
    <p>Campo e Cidade: Sustentabilidade e Educação de Forma Elegante</p>
</header>

<nav>
    <a href="#sobre">Sobre</a>
    <a href="#importancia">Importância</a>
    <a href="#acoes">Ações</a>
</nav>

<section id="sobre">
    <div class="card">
        <h2>Sobre o Projeto</h2>
        <p>
            O Agrinho 2026 incentiva a educação, a sustentabilidade
            e a valorização da relação entre o campo e a cidade.
            É um projeto que une inovação e cuidado com o meio ambiente.
        </p>
    </div>
</section>

<section id="importancia">
    <div class="card">
        <h2>Por que é importante?</h2>
        <p>
            A produção agrícola fornece alimentos para todos, enquanto a cidade
            oferece tecnologia, serviços e inovação. Juntos, constroem um futuro sustentável e sofisticado.
        </p>
    </div>
</section>

<section id="acoes">
    <div class="card">
        <h2>Mensagem Sustentável</h2>
        <p id="mensagem">
            Clique no botão para receber uma dica sustentável.
        </p>
        <br>
        <button onclick="mostrarDica()">Mostrar Dica</button>
    </div>
</section>

<!-- Aba de acessibilidade -->
<div id="a11y-bar">
    <h3>Acessibilidade</h3>
    <button onclick="aumentarFonte()">Aumentar Fonte</button>
    <button onclick="diminuirFonte()">Diminuir Fonte</button>
    <button onclick="alternarTema()">Tema Claro/Escuro</button>
</div>

<footer>
    <p>© 2026 Projeto Agrinho - Design moderno e acessível</p>
</footer>

<script>
// Dicas sustentáveis
const dicas = [
    "Economize água sempre que possível.",
    "Plante árvores e cuide da natureza.",
    "Recicle materiais e reduza o desperdício.",
    "Valorize os produtores rurais.",
    "Prefira produtos locais e sustentáveis."
];

function mostrarDica(){
    const aleatoria = Math.floor(Math.random() * dicas.length);
    document.getElementById("mensagem").innerText = dicas[aleatoria];
}

// --- Controle de fontes ---
let tamanhoFonte = 16; // padrão
function aumentarFonte(){
    tamanhoFonte += 2;
    document.body.style.fontSize = tamanhoFonte + "px";
}
function diminuirFonte(){
    if(tamanhoFonte > 12) tamanhoFonte -= 2;
    document.body.style.fontSize = tamanhoFonte + "px";
}

// --- Tema claro/escuro ---
function alternarTema(){
    document.body.classList.toggle("dark");
}
</script>

</body>
</html>
