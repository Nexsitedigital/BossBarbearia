<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boss Barbearia | Social Club - Patos PB</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css" rel="stylesheet">
    <link href="https://fonts.googleapis.com/css2?family=Oswald:wght@400;500;700&family=Roboto:wght@300;400;500;700&display=swap" rel="stylesheet">
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    fontFamily: {
                        'oswald': ['Oswald', 'sans-serif'],
                        'roboto': ['Roboto', 'sans-serif'],
                    },
                    colors: {
                        'boss-black': '#0a0a0a',
                        'boss-gray': '#1a1a1a',
                        'boss-gold': '#d4af37',
                    }
                }
            }
        }
    </script>
    <style>
        .hover-scale { transition: transform 0.3s ease; }
        .hover-scale:hover { transform: scale(1.05); }
        .glass-effect { background: rgba(26, 26, 26, 0.95); backdrop-filter: blur(10px); }
        
        .text-gold-gradient {
            background: linear-gradient(to right, #d4af37, #f4e5c2, #d4af37);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            color: transparent;
            display: inline;
        }
        
        /* Filtro para converter logo preta em dourada sem fundo amarelo */
        .logo-gold-filter {
            filter: brightness(0) saturate(100%) invert(72%) sepia(55%) saturate(450%) hue-rotate(3deg) brightness(92%) contrast(88%);
        }
        
        @media (max-width: 768px) {
            .hero-title { font-size: 2.5rem !important; line-height: 1.1 !important; }
        }
        
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #0a0a0a; }
        ::-webkit-scrollbar-thumb { background: #d4af37; border-radius: 4px; }
    </style>
</head>
<body class="bg-boss-black text-white font-roboto overflow-x-hidden">

    <nav class="fixed w-full z-50 glass-effect border-b border-gray-800 top-0">
        <div class="container mx-auto px-6 py-3 flex justify-between items-center">
            <div class="flex items-center">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Boss Barbearia" class="h-14 md:h-20 w-auto logo-gold-filter">
                <div class="hidden md:block ml-4">
                    <h1 class="font-oswald text-xl font-bold tracking-wider text-white">BOSS <span class="text-boss-gold">BARBEARIA</span></h1>
                    <p class="text-[10px] text-gray-400 tracking-[0.2em]">SOCIAL CLUB</p>
                </div>
            </div>
            
            <div class="hidden md:flex items-center gap-6 text-sm">
                <a href="#inicio" class="hover:text-boss-gold transition-colors font-medium">Início</a>
                <a href="#servicos" class="hover:text-boss-gold transition-colors font-medium">Serviços</a>
                <a href="#agendamento" class="hover:text-boss-gold transition-colors font-medium">Agendar</a>
                <a href="#equipe" class="hover:text-boss-gold transition-colors font-medium">Equipe</a>
                <a href="#contato" class="hover:text-boss-gold transition-colors font-medium">Contato</a>
            </div>

            <button onclick="toggleMenu()" class="md:hidden text-2xl text-boss-gold p-2">
                <i class="fas fa-bars"></i>
            </button>
        </div>

        <div id="mobile-menu" class="hidden bg-boss-gray border-t border-gray-700 w-full">
            <div class="flex flex-col p-4">
                <a href="#inicio" class="text-white py-4 px-4 border-b border-gray-800" onclick="toggleMenu()">Início</a>
                <a href="#servicos" class="text-white py-4 px-4 border-b border-gray-800" onclick="toggleMenu()">Serviços</a>
                <a href="#agendamento" class="text-white py-4 px-4 border-b border-gray-800" onclick="toggleMenu()">Agendar</a>
                <a href="#equipe" class="text-white py-4 px-4 border-b border-gray-800" onclick="toggleMenu()">Equipe</a>
                <a href="#contato" class="text-white py-4 px-4" onclick="toggleMenu()">Contato</a>
            </div>
        </div>
    </nav>

    <section id="inicio" class="relative min-h-[90vh] flex items-center justify-center pt-20 overflow-hidden">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-b from-boss-black via-boss-black/80 to-boss-black z-10"></div>
            <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?w=1920&h=1080&fit=crop" class="w-full h-full object-cover opacity-20">
        </div>

        <div class="container mx-auto px-6 relative z-20 text-center">
            <div class="mb-6 flex justify-center">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" class="w-full max-w-[250px] md:max-w-[320px] h-auto logo-gold-filter">
            </div>
            <h2 class="hero-title font-oswald text-4xl md:text-7xl font-bold mb-4 tracking-tight">ELEGÂNCIA & <span class="text-gold-gradient">ESTILO</span></h2>
            <p class="text-lg md:text-xl text-gray-300 mb-8 max-w-2xl mx-auto font-light">A experiência definitiva em cuidados masculinos em Patos - PB</p>
            
            <div class="flex items-center justify-center gap-2 text-boss-gold mb-8">
                <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                <span class="text-white ml-2">4.9 (84 avaliações)</span>
            </div>

            <div class="flex flex-col sm:flex-row gap-4 justify-center">
                <a href="#agendamento" class="bg-boss-gold text-black font-oswald font-bold px-8 py-4 rounded hover-scale">AGENDAR HORÁRIO</a>
                <a href="https://wa.me/5583998159090" target="_blank" class="border-2 border-boss-gold text-boss-gold font-oswald font-bold px-8 py-4 rounded hover:bg-boss-gold hover:text-black transition-all">WHATSAPP</a>
            </div>
        </div>
    </section>

    <section id="servicos" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-12">
                <h3 class="font-oswald text-3xl md:text-4xl font-bold mb-3">NOSSOS <span class="text-boss-gold">SERVIÇOS</span></h3>
                <div class="w-20 h-1 bg-boss-gold mx-auto"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-cut text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Corte de Cabelo</h4>
                    <p class="text-gray-400 text-sm">Corte tradicional, degradê, tesoura ou navalha com acabamento impecável.</p>
                </div>
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-user-tie text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Barba & Navalha</h4>
                    <p class="text-gray-400 text-sm">Aparar, modelar ou barba completa utilizando técnica de toalha quente.</p>
                </div>
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-spa text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Barbaterapia</h4>
                    <p class="text-gray-400 text-sm">Tratamento relaxante com vapor de ozônio e óleos essenciais.</p>
                </div>
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-paint-brush text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Coloração</h4>
                    <p class="text-gray-400 text-sm">Coloração de cabelo e barba ou camuflagem de fios brancos.</p>
                </div>
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-child text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Corte Infantil</h4>
                    <p class="text-gray-400 text-sm">Atendimento especial para os pequenos em ambiente descontraído.</p>
                </div>
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all group">
                    <i class="fas fa-eye text-boss-gold text-3xl mb-4"></i>
                    <h4 class="font-oswald text-xl font-bold mb-2">Sobrancelhas</h4>
                    <p class="text-gray-400 text-sm">Design e limpeza de sobrancelhas masculina na navalha.</p>
                </div>
            </div>
        </div>
    </section>

    <section id="agendamento" class="py-16 bg-boss-black">
        <div class="container mx-auto px-6 max-w-2xl">
            <div class="bg-boss-gray p-8 rounded-xl border border-gray-700 shadow-2xl">
                <h3 class="font-oswald text-3xl font-bold mb-6 text-center text-boss-gold">AGENDAMENTO</h3>
                <form onsubmit="enviarAgendamento(event)" class="space-y-4">
                    <div>
                        <label class="text-xs text-gray-400 mb-1 block">NOME COMPLETO</label>
                        <input type="text" id="nome" required class="w-full bg-boss-black border border-gray-700 p-3 rounded focus:border-boss-gold outline-none">
                    </div>
                    <div class="grid grid-cols-2 gap-4">
                        <div>
                            <label class="text-xs text-gray-400 mb-1 block">DATA</label>
                            <input type="date" id="data" required class="w-full bg-boss-black border border-gray-700 p-3 rounded focus:border-boss-gold outline-none">
                        </div>
                        <div>
                            <label class="text-xs text-gray-400 mb-1 block">HORÁRIO</label>
                            <select id="horario" required class="w-full bg-boss-black border border-gray-700 p-3 rounded focus:border-boss-gold outline-none">
                                <option value="09:00">09:00</option><option value="10:00">10:00</option><option value="11:00">11:00</option>
                                <option value="14:00">14:00</option><option value="15:00">15:00</option><option value="18:00">18:00</option>
                            </select>
                        </div>
                    </div>
                    <div>
                        <label class="text-xs text-gray-400 mb-1 block">PROFISSIONAL</label>
                        <select id="profissional" class="w-full bg-boss-black border border-gray-700 p-3 rounded focus:border-boss-gold outline-none">
                            <option value="Caio">Caio</option><option value="Silvino">Silvino</option>
                            <option value="Andrey">Andrey</option><option value="Matheus">Matheus</option><option value="Nathan">Nathan</option>
                        </select>
                    </div>
                    <button type="submit" class="w-full bg-boss-gold text-black font-oswald font-bold py-4 rounded hover:bg-yellow-500 transition-all text-lg">CONFIRMAR NO WHATSAPP</button>
                </form>
            </div>
        </div>
    </section>

    <section id="equipe" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <h3 class="font-oswald text-3xl font-bold mb-12 text-center underline decoration-boss-gold underline-offset-8">NOSSA EQUIPE</h3>
            <div class="grid grid-cols-2 md:grid-cols-5 gap-8">
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gray-800 rounded-full mb-4 flex items-center justify-center border-2 border-transparent group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-3xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold">Caio</h4>
                    <p class="text-boss-gold text-xs">Especialista</p>
                </div>
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gray-800 rounded-full mb-4 flex items-center justify-center border-2 border-transparent group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-3xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold">Silvino</h4>
                    <p class="text-boss-gold text-xs">Master</p>
                </div>
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gray-800 rounded-full mb-4 flex items-center justify-center border-2 border-transparent group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-3xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold">Andrey</h4>
                    <p class="text-boss-gold text-xs">Colorista</p>
                </div>
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gray-800 rounded-full mb-4 flex items-center justify-center border-2 border-transparent group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-3xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold">Matheus</h4>
                    <p class="text-boss-gold text-xs">Barbeiro</p>
                </div>
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gray-800 rounded-full mb-4 flex items-center justify-center border-2 border-transparent group-hover:border-boss-gold transition-all">
                        <i class="fas fa-user text-3xl text-boss-gold"></i>
                    </div>
                    <h4 class="font-bold">Nathan</h4>
                    <p class="text-boss-gold text-xs">Barbeiro</p>
                </div>
            </div>
        </div>
    </section>

    <section class="py-16 bg-boss-black border-y border-gray-800">
        <div class="container mx-auto px-6">
            <h3 class="font-oswald text-3xl font-bold mb-10 text-center uppercase tracking-widest">O que dizem nossos <span class="text-boss-gold">Clientes</span></h3>
            <div class="grid md:grid-cols-3 gap-6 text-sm">
                <div class="bg-boss-gray p-6 rounded-lg">
                    <div class="text-boss-gold mb-2"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="italic text-gray-300">"Ambiente excelente e profissionais extremamente qualificados. O Caio é fera!"</p>
                    <p class="mt-4 font-bold">- Edinaldo Baltazar</p>
                </div>
                <div class="bg-boss-gray p-6 rounded-lg">
                    <div class="text-boss-gold mb-2"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="italic text-gray-300">"Melhor barbearia de Patos. Atendimento nota 10 e cerveja gelada."</p>
                    <p class="mt-4 font-bold">- João Arthur</p>
                </div>
                <div class="bg-boss-gray p-6 rounded-lg">
                    <div class="text-boss-gold mb-2"><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i></div>
                    <p class="italic text-gray-300">"Andrey é um excelente barbeiro. Super recomendo a Barbaterapia."</p>
                    <p class="mt-4 font-bold">- Giovanny José</p>
                </div>
            </div>
        </div>
    </section>

    <section id="contato" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-12">
                <div>
                    <h3 class="font-oswald text-4xl font-bold mb-8">CONTATO</h3>
                    <div class="space-y-6">
                        <p class="flex items-center gap-4 text-lg"><i class="fas fa-map-marker-alt text-boss-gold w-6"></i> R. do Prado, 40 - Centro, Patos - PB</p>
                        <p class="flex items-center gap-4 text-lg"><i class="fab fa-whatsapp text-boss-gold w-6"></i> (83) 99815-9090</p>
                        <p class="flex items-center gap-4 text-lg"><i class="fas fa-clock text-boss-gold w-6"></i> Seg-Sáb: 09:00 às 20:00</p>
                    </div>
                    <div class="mt-10 flex gap-4">
                        <a href="#" class="w-12 h-12 bg-boss-black rounded-full flex items-center justify-center hover:text-boss-gold transition-all border border-gray-700"><i class="fab fa-instagram text-xl"></i></a>
                        <a href="#" class="w-12 h-12 bg-boss-black rounded-full flex items-center justify-center hover:text-boss-gold transition-all border border-gray-700"><i class="fab fa-facebook-f text-xl"></i></a>
                    </div>
                </div>
                <div class="h-80 bg-gray-900 rounded-xl overflow-hidden border border-gray-700 shadow-2xl">
                    <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15833.565611413158!2d-37.28014555!3d-7.0220268!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x7a6a70e7e7e7e7e7%3A0x7e7e7e7e7e7e7e7e!2sPatos%2C%20PB!5e0!3m2!1spt-BR!2sbr!4v1625145874587!5m2!1spt-BR!2sbr" width="100%" height="100%" style="border:0;" allowfullscreen="" loading="lazy"></iframe>
                </div>
            </div>
        </div>
    </section>

    <footer class="py-12 bg-black border-t border-gray-900 text-center">
        <img src="https://i.postimg.cc/HkqZfnMz/boss.png" class="h-16 mx-auto mb-6 logo-gold-filter">
        <p class="text-gray-500 font-light italic">"Onde o estilo encontra a tradição."</p>
        <div class="mt-8 text-gray-600 text-sm">
            <p>© 2026 Boss Barbearia - Social Club. Patos, Paraíba.</p>
        </div>
    </footer>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        function enviarAgendamento(e) {
            e.preventDefault();
            const nome = document.getElementById('nome').value;
            const data = document.getElementById('data').value;
            const horario = document.getElementById('horario').value;
            const prof = document.getElementById('profissional').value;
            const msg = `Olá! Gostaria de agendar:%0A*Nome:* ${nome}%0A*Data:* ${data}%0A*Horário:* ${horario}%0A*Profissional:* ${prof}`;
            window.open(`https://wa.me/5583998159090?text=${msg}`, '_blank');
        }
    </script>
</body>
</html>
