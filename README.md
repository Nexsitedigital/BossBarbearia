<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boss Barbearia | Social Club - Patos PB</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;700&family=Roboto:wght@300;400;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: { 'oswald': ['Oswald', 'sans-serif'], 'roboto': ['Roboto', 'sans-serif'] },
                    colors: { 'boss-black': '#0a0a0a', 'boss-gray': '#121212', 'boss-gold': '#d4af37' }
                }
            }
        }
    </script>

    <style>
        .glass-header { background: rgba(10, 10, 10, 0.95); backdrop-filter: blur(10px); }
        
        /* MÁSCARA CSS: O segredo para a logo ficar dourada sem fundo amarelo */
        .logo-mask {
            background-color: #d4af37;
            -webkit-mask-image: url('https://i.postimg.cc/HkqZfnMz/boss.png');
            mask-image: url('https://i.postimg.cc/HkqZfnMz/boss.png');
            -webkit-mask-size: contain;
            mask-size: contain;
            -webkit-mask-repeat: no-repeat;
            mask-repeat: no-repeat;
            -webkit-mask-position: center;
            mask-position: center;
        }

        .text-gold-gradient {
            background: linear-gradient(to right, #d4af37, #f4e5c2, #b8860b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        
        .hover-gold:hover { color: #d4af37; transition: 0.3s; }
    </style>
</head>
<body class="bg-boss-black text-white font-roboto">

    <header class="fixed w-full z-50 glass-header border-b border-white/5">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#inicio" class="flex items-center gap-3">
                <div class="logo-mask h-12 w-24"></div>
                <div class="hidden sm:block">
                    <span class="block font-oswald text-lg font-bold tracking-widest uppercase leading-none">Boss</span>
                    <span class="text-[8px] text-boss-gold tracking-[0.4em] uppercase font-bold">Social Club</span>
                </div>
            </a>

            <ul class="hidden lg:flex gap-8 font-oswald text-xs tracking-widest uppercase">
                <li><a href="#inicio" class="hover-gold">Início</a></li>
                <li><a href="#servicos" class="hover-gold">Serviços</a></li>
                <li><a href="#agendamento" class="hover-gold">Agendar</a></li>
                <li><a href="#equipe" class="hover-gold">Equipe</a></li>
                <li><a href="#contato" class="hover-gold">Contato</a></li>
            </ul>

            <button onclick="toggleMenu()" class="lg:hidden text-boss-gold text-2xl">
                <i class="fas fa-bars" id="menu-icon"></i>
            </button>
        </nav>

        <div id="mobile-menu" class="hidden bg-boss-gray border-t border-white/5 w-full flex flex-col p-6 gap-6 font-oswald uppercase text-center tracking-widest">
            <a href="#inicio" onclick="toggleMenu()">Início</a>
            <a href="#servicos" onclick="toggleMenu()">Serviços</a>
            <a href="#agendamento" onclick="toggleMenu()">Agendamento</a>
            <a href="#equipe" onclick="toggleMenu()">Equipe</a>
            <a href="#contato" onclick="toggleMenu()">Contato</a>
        </div>
    </header>

    <section id="inicio" class="relative h-screen flex items-center justify-center text-center px-6">
        <div class="absolute inset-0 bg-black/70 z-10"></div>
        <div class="absolute inset-0 z-0">
            <img src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?w=1920" class="w-full h-full object-cover opacity-40">
        </div>

        <div class="relative z-20 max-w-4xl animate-fade-in">
            <div class="logo-mask h-32 w-64 mx-auto mb-8"></div>
            <h1 class="font-oswald text-5xl md:text-8xl font-bold uppercase mb-6 leading-none">
                Elegância & <span class="text-gold-gradient">Estilo</span>
            </h1>
            <p class="text-gray-400 text-lg md:text-xl mb-10 max-w-2xl mx-auto">
                A experiência definitiva em cuidados masculinos em Patos - PB.
            </p>
            
            <div class="flex flex-col sm:flex-row gap-4 justify-center items-center">
                <a href="#agendamento" class="w-full sm:w-64 bg-boss-gold text-black font-oswald font-bold py-5 rounded shadow-lg hover:scale-105 transition-all">
                    <i class="fas fa-calendar-alt mr-2"></i> AGENDAR HORÁRIO
                </a>
                <a href="https://wa.me/5583998159090" class="w-full sm:w-64 bg-[#25D366] text-white font-oswald font-bold py-5 rounded hover:scale-105 transition-all">
                    <i class="fab fa-whatsapp mr-2"></i> WHATSAPP
                </a>
            </div>
        </div>
    </section>

    <section id="servicos" class="py-24 bg-boss-gray">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-oswald font-bold text-center mb-16 uppercase">Nossos <span class="text-boss-gold">Serviços</span></h2>
            <div class="grid md:grid-cols-3 gap-8">
                <div class="bg-boss-black p-8 rounded border border-white/5 hover:border-boss-gold transition-all text-center">
                    <i class="fas fa-cut text-boss-gold text-3xl mb-6"></i>
                    <h3 class="text-xl font-bold mb-4">CORTE PREMIUM</h3>
                    <p class="text-gray-500 text-sm">Degradês e cortes clássicos com finalização impecável.</p>
                </div>
                <div class="bg-boss-black p-8 rounded border border-white/5 hover:border-boss-gold transition-all text-center">
                    <i class="fas fa-user-tie text-boss-gold text-3xl mb-6"></i>
                    <h3 class="text-xl font-bold mb-4">BARBA COMPLETA</h3>
                    <p class="text-gray-500 text-sm">Toalha quente e produtos específicos para sua pele.</p>
                </div>
                <div class="bg-boss-black p-8 rounded border border-white/5 hover:border-boss-gold transition-all text-center">
                    <i class="fas fa-gem text-boss-gold text-3xl mb-6"></i>
                    <h3 class="text-xl font-bold mb-4">COMBO BOSS</h3>
                    <p class="text-gray-500 text-sm">Cabelo + Barba + Sobrancelha com desconto especial.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="equipe" class="py-24 bg-boss-black text-center">
        <div class="container mx-auto px-6">
            <h2 class="text-4xl font-oswald font-bold mb-16 uppercase">Time <span class="text-boss-gold">Boss</span></h2>
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                <div>
                    <div class="w-24 h-24 mx-auto rounded-full bg-boss-gray border border-boss-gold flex items-center justify-center mb-4">
                        <i class="fas fa-user-ninja text-2xl text-boss-gold"></i>
                    </div>
                    <p class="font-bold">Caio Chaves</p>
                    <p class="text-[10px] text-boss-gold">Founder</p>
                </div>
                </div>
        </div>
    </section>

    <footer id="contato" class="bg-black pt-20 pb-10 border-t border-white/5">
        <div class="container mx-auto px-6 text-center">
            <div class="logo-mask h-16 w-32 mx-auto mb-10"></div>
            <p class="text-gray-500 mb-6">Rua do Prado, 40 - Centro | Patos - PB</p>
            <div class="flex justify-center gap-6 mb-10 text-xl">
                <a href="#" class="hover:text-boss-gold"><i class="fab fa-instagram"></i></a>
                <a href="#" class="hover:text-boss-gold"><i class="fab fa-facebook"></i></a>
            </div>
            <p class="text-gray-700 text-[10px] uppercase tracking-[0.4em]">
                © 2026 Boss Barbearia - Desenvolvido por NexSite Digital
            </p>
        </div>
    </footer>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('menu-icon');
            menu.classList.toggle('hidden');
            icon.classList.toggle('fa-bars');
            icon.classList.toggle('fa-times');
        }
    </script>
</body>
</html>
