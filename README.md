<!DOCTYPE html>
<html lang="pt-BR" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Boss Barbearia Social Club - A melhor experiência em barbearia em Patos, Paraíba.">
    <title>Boss Barbearia | Social Club - Patos PB</title>
    
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@300;400;500;600;700&family=Roboto:wght@100;300;400;500;700&display=swap" rel="stylesheet">
    
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: { 'oswald': ['Oswald', 'sans-serif'], 'roboto': ['Roboto', 'sans-serif'] },
                    colors: { 'boss-black': '#0a0a0a', 'boss-gray': '#121212', 'boss-gold': '#d4af37', 'boss-gold-light': '#f4e5c2' },
                    animation: { 'fade-in': 'fadeIn 0.5s ease-out forwards', 'slide-up': 'slideUp 0.5s ease-out forwards' }
                }
            }
        }
    </script>

    <style>
        @keyframes fadeIn { from { opacity: 0; } to { opacity: 1; } }
        @keyframes slideUp { from { transform: translateY(20px); opacity: 0; } to { transform: translateY(0); opacity: 1; } }
        
        .glass-header { background: rgba(10, 10, 10, 0.95); backdrop-filter: blur(12px); }
        .text-gold-gradient {
            background: linear-gradient(45deg, #d4af37, #f4e5c2, #b8860b);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        /* FILTRO LOGO DOURADA: Converte preto em dourado sem o fundo amarelo */
        .logo-gold-filter {
            filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(450%) hue-rotate(3deg) brightness(92%) contrast(88%);
            transition: all 0.3s ease;
        }

        .service-card:hover { border-color: #d4af37; transform: translateY(-5px); }
        .custom-scroll::-webkit-scrollbar { width: 6px; }
        .custom-scroll::-webkit-scrollbar-track { background: #0a0a0a; }
        .custom-scroll::-webkit-scrollbar-thumb { background: #d4af37; border-radius: 10px; }
    </style>
</head>
<body class="bg-boss-black text-white font-roboto custom-scroll">

    <header class="fixed w-full z-[100] glass-header border-b border-white/5">
        <nav class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#inicio" class="flex items-center gap-3 group">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Boss Logo" class="h-12 md:h-16 logo-gold-filter">
                <div class="hidden sm:block">
                    <span class="block font-oswald text-xl font-bold tracking-widest uppercase leading-none">Boss</span>
                    <span class="text-[9px] text-boss-gold tracking-[0.4em] uppercase font-bold">Social Club</span>
                </div>
            </a>

            <ul class="hidden lg:flex items-center gap-10 font-oswald text-xs tracking-[0.2em] uppercase">
                <li><a href="#inicio" class="hover:text-boss-gold transition-colors">Início</a></li>
                <li><a href="#servicos" class="hover:text-boss-gold transition-colors">Serviços</a></li>
                <li><a href="#agendamento" class="hover:text-boss-gold transition-colors">Agendar</a></li>
                <li><a href="#equipe" class="hover:text-boss-gold transition-colors">Equipe</a></li>
                <li><a href="#contato" class="hover:text-boss-gold transition-colors">Contato</a></li>
            </ul>

            <div class="flex items-center gap-4">
                <a href="https://wa.me/5583998159090" class="hidden md:flex bg-boss-gold text-black font-oswald font-bold px-5 py-2 text-xs rounded-sm hover:bg-white transition-all">WHATSAPP</a>
                <button onclick="toggleMenu()" class="lg:hidden text-2xl text-boss-gold"><i class="fas fa-bars" id="menu-btn"></i></button>
            </div>
        </nav>

        <div id="mobile-menu" class="hidden lg:hidden bg-boss-gray border-t border-white/5 absolute w-full left-0 animate-fade-in">
            <div class="flex flex-col p-6 space-y-6 font-oswald uppercase tracking-widest text-center">
                <a href="#inicio" onclick="toggleMenu()" class="text-lg hover:text-boss-gold">Início</a>
                <a href="#servicos" onclick="toggleMenu()" class="text-lg hover:text-boss-gold">Serviços</a>
                <a href="#agendamento" onclick="toggleMenu()" class="text-lg hover:text-boss-gold">Agendamento</a>
                <a href="#equipe" onclick="toggleMenu()" class="text-lg hover:text-boss-gold">Nosso Time</a>
                <a href="#contato" onclick="toggleMenu()" class="text-lg hover:text-boss-gold">Contato</a>
            </div>
        </div>
    </header>

    <section id="inicio" class="relative h-screen flex items-center justify-center overflow-hidden">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-black/60 z-10"></div>
            <img src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?w=1920" class="w-full h-full object-cover scale-110 animate-pulse-slow">
        </div>
        
        <div class="container mx-auto px-6 relative z-20 text-center animate-slide-up">
            <img src="https://i.postimg.cc/HkqZfnMz/boss.png" class="w-48 md:w-64 mx-auto mb-8 logo-gold-filter">
            <h1 class="font-oswald text-5xl md:text-8xl font-bold tracking-tighter uppercase leading-none mb-6">
                Domine seu <span class="text-gold-gradient">Estilo</span>
            </h1>
            <p class="text-gray-400 font-light text-lg md:text-xl max-w-2xl mx-auto mb-10 tracking-wide">
                Muito além de um corte. Um ambiente exclusivo para o homem que busca excelência em Patos - PB.
            </p>
            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#agendamento" class="bg-boss-gold text-black font-oswald font-bold px-12 py-5 rounded-sm hover:scale-105 transition-all shadow-lg shadow-boss-gold/20">AGENDAR HORÁRIO</a>
                <a href="#servicos" class="border border-white/20 hover:border-boss-gold px-12 py-5 rounded-sm transition-all font-oswald font-bold">VER SERVIÇOS</a>
            </div>
        </div>
    </section>

    <section id="servicos" class="py-24 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="flex flex-col md:flex-row justify-between items-end mb-16 gap-6">
                <div>
                    <span class="text-boss-gold font-oswald tracking-[0.3em] uppercase text-sm">Tradição & Navalha</span>
                    <h2 class="text-4xl md:text-6xl font-oswald font-bold uppercase mt-2">Nossos <span class="text-boss-gold">Serviços</span></h2>
                </div>
                <p class="text-gray-500 max-w-sm text-sm">Equipamentos de ponta e os melhores produtos do mercado para o seu visual.</p>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <div class="service-card p-8 bg-boss-black border border-white/5 rounded-xl transition-all group">
                    <div class="w-16 h-16 bg-boss-gold/10 rounded-full flex items-center justify-center mb-6 group-hover:bg-boss-gold group-hover:text-black transition-colors">
                        <i class="fas fa-cut text-2xl"></i>
                    </div>
                    <h3 class="text-2xl font-oswald font-bold mb-4 uppercase">Corte de Cabelo</h3>
                    <p class="text-gray-500 text-sm mb-6 leading-relaxed">Cortes clássicos, degradês (Fade), Scissor Cut e finalização com pomada.</p>
                    <div class="flex justify-between items-center border-t border-white/5 pt-6">
                        <span class="text-boss-gold font-bold">A partir de R$ 35,00</span>
                        <i class="fas fa-arrow-right text-xs opacity-0 group-hover:opacity-100 transition-opacity"></i>
                    </div>
                </div>
                <div class="service-card p-8 bg-boss-black border border-white/5 rounded-xl transition-all group">
                    <div class="w-16 h-16 bg-boss-gold/10 rounded-full flex items-center justify-center mb-6 group-hover:bg-boss-gold group-hover:text-black transition-colors">
                        <i class="fas fa-user-tie text-2xl"></i>
                    </div>
                    <h3 class="text-2xl font-oswald font-bold mb-4 uppercase">Barba & Navalha</h3>
                    <p class="text-gray-500 text-sm mb-6 leading-relaxed">Técnica de toalha quente, pré-barba relaxante e óleos hidratantes.</p>
                    <div class="flex justify-between items-center border-t border-white/5 pt-6">
                        <span class="text-boss-gold font-bold">A partir de R$ 30,00</span>
                    </div>
                </div>
                <div class="service-card p-8 bg-boss-black border border-white/5 rounded-xl transition-all group">
                    <div class="w-16 h-16 bg-boss-gold/10 rounded-full flex items-center justify-center mb-6 group-hover:bg-boss-gold group-hover:text-black transition-colors">
                        <i class="fas fa-spa text-2xl"></i>
                    </div>
                    <h3 class="text-2xl font-oswald font-bold mb-4 uppercase">Barbaterapia</h3>
                    <p class="text-gray-500 text-sm mb-6 leading-relaxed">Um spa para seu rosto com vapor de ozônio e massagem relaxante.</p>
                    <div class="flex justify-between items-center border-t border-white/5 pt-6">
                        <span class="text-boss-gold font-bold">A partir de R$ 45,00</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <section id="agendamento" class="py-24 bg-boss-black relative">
        <div class="container mx-auto px-6 max-w-5xl">
            <div class="grid lg:grid-cols-2 gap-16 items-center">
                <div class="space-y-8">
                    <h2 class="text-4xl md:text-5xl font-oswald font-bold uppercase italic">Agende sua <span class="text-boss-gold">Experiência</span></h2>
                    <p class="text-gray-400">Selecione o profissional de sua preferência e o horário que melhor se adapta à sua rotina.</p>
                    <div class="space-y-4">
                        <div class="flex items-center gap-4 text-sm font-bold">
                            <i class="fas fa-check-circle text-boss-gold"></i><span>CONFIRMAÇÃO VIA WHATSAPP</span>
                        </div>
                        <div class="flex items-center gap-4 text-sm font-bold">
                            <i class="fas fa-check-circle text-boss-gold"></i><span>PAGAMENTO NO LOCAL</span>
                        </div>
                        <div class="flex items-center gap-4 text-sm font-bold">
                            <i class="fas fa-check-circle text-boss-gold"></i><span>CAFEZINHO E CERVEJA GELADA</span>
                        </div>
                    </div>
                </div>
                
                <div class="bg-boss-gray p-8 md:p-12 rounded-2xl border border-white/5 shadow-2xl">
                    <form onsubmit="enviarAgendamento(event)" class="space-y-5">
                        <input type="text" id="nome" placeholder="Nome Completo" required class="w-full bg-boss-black border border-white/10 p-4 rounded focus:border-boss-gold outline-none transition-all">
                        <div class="grid grid-cols-2 gap-4">
                            <input type="date" id="data" required class="w-full bg-boss-black border border-white/10 p-4 rounded focus:border-boss-gold outline-none">
                            <input type="time" id="horario" required class="w-full bg-boss-black border border-white/10 p-4 rounded focus:border-boss-gold outline-none">
                        </div>
                        <select id="profissional" required class="w-full bg-boss-black border border-white/10 p-4 rounded focus:border-boss-gold outline-none">
                            <option value="">Escolha o Barbeiro</option>
                            <option value="Caio">Caio Chaves</option>
                            <option value="Silvino">Silvino</option>
                            <option value="Andrey">Andrey</option>
                            <option value="Matheus">Matheus</option>
                            <option value="Nathan">Nathan</option>
                        </select>
                        <select id="servico" required class="w-full bg-boss-black border border-white/10 p-4 rounded focus:border-boss-gold outline-none">
                            <option value="Corte">Corte Premium</option>
                            <option value="Barba">Barba Completa</option>
                            <option value="Corte+Barba">Corte & Barba</option>
                            <option value="Outros">Outros Serviços</option>
                        </select>
                        <button class="w-full bg-boss-gold text-black font-oswald font-bold py-5 rounded hover:bg-yellow-500 transition-all uppercase tracking-widest text-lg">Confirmar Agora</button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <section id="equipe" class="py-24 bg-boss-gray">
        <div class="container mx-auto px-6 text-center">
            <h2 class="text-4xl font-oswald font-bold mb-16 uppercase tracking-[0.2em]">O Time <span class="text-boss-gold">Boss</span></h2>
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                <div class="group">
                    <div class="w-24 h-24 md:w-32 md:h-32 mx-auto rounded-full bg-boss-black border-2 border-boss-gold mb-4 flex items-center justify-center group-hover:scale-110 transition-transform">
                        <i class="fas fa-user-ninja text-4xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold uppercase text-sm">Caio</h4>
                    <p class="text-[10px] text-boss-gold uppercase">Founder</p>
                </div>
                <div class="group">
                    <div class="w-24 h-24 md:w-32 md:h-32 mx-auto rounded-full bg-boss-black border border-white/10 mb-4 flex items-center justify-center group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-4xl text-gray-700"></i>
                    </div>
                    <h4 class="font-bold uppercase text-sm">Silvino</h4>
                    <p class="text-[10px] text-boss-gold uppercase">Master</p>
                </div>
                </div>
        </div>
    </section>

    <footer id="contato" class="bg-black pt-20 pb-10 border-t border-white/5">
        <div class="container mx-auto px-6 grid md:grid-cols-4 gap-12 mb-20">
            <div class="md:col-span-1">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" class="h-16 mb-6 logo-gold-filter">
                <p class="text-gray-500 text-sm italic">"Excelência em cada detalhe, estilo em cada corte."</p>
            </div>
            <div>
                <h4 class="font-oswald font-bold mb-6 uppercase tracking-widest">Localização</h4>
                <p class="text-gray-500 text-sm">Rua do Prado, 40 - Centro<br>Patos - Paraíba</p>
            </div>
            <div>
                <h4 class="font-oswald font-bold mb-6 uppercase tracking-widest">Redes Sociais</h4>
                <div class="flex gap-4">
                    <a href="#" class="w-10 h-10 rounded-full border border-white/10 flex items-center justify-center hover:text-boss-gold transition-all"><i class="fab fa-instagram"></i></a>
                    <a href="#" class="w-10 h-10 rounded-full border border-white/10 flex items-center justify-center hover:text-boss-gold transition-all"><i class="fab fa-facebook-f"></i></a>
                </div>
            </div>
            <div>
                <h4 class="font-oswald font-bold mb-6 uppercase tracking-widest">Horários</h4>
                <p class="text-gray-500 text-sm">Seg a Sáb: 09:00 - 20:00</p>
            </div>
        </div>
        <div class="text-center text-gray-700 text-[10px] uppercase tracking-[0.5em] border-t border-white/5 pt-10">
            © 2026 Boss Barbearia - Desenvolvido por <span class="text-gray-500">NexSite Digital</span>
        </div>
    </footer>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            const icon = document.getElementById('menu-btn');
            menu.classList.toggle('hidden');
            icon.classList.toggle('fa-bars');
            icon.classList.toggle('fa-times');
        }

        function enviarAgendamento(e) {
            e.preventDefault();
            const nome = document.getElementById('nome').value;
            const data = document.getElementById('data').value;
            const hora = document.getElementById('horario').value;
            const prof = document.getElementById('profissional').value;
            const serv = document.getElementById('servico').value;
            
            const texto = `*BOSS BARBEARIA - AGENDAMENTO*%0A%0A*Nome:* ${nome}%0A*Data:* ${data}%0A*Hora:* ${hora}%0A*Barbeiro:* ${prof}%0A*Serviço:* ${serv}`;
            window.open(`https://wa.me/5583998159090?text=${texto}`, '_blank');
        }
    </script>
</body>
</html>
