
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
        
        /* Degradê dourado para texto - CORRIGIDO */
        .text-gold-gradient {
            background: linear-gradient(to right, #d4af37, #f4e5c2, #d4af37);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
            color: transparent;
            display: inline;
        }
        
        /* Remover fundo branco do logo */
        .logo-img {
            background-color: transparent !important;
            mix-blend-mode: multiply;
            filter: contrast(1.1) brightness(1.1);
        }
        
        /* Se o logo tiver fundo branco, esta classe ajuda a camuflar */
        .logo-container {
            background: transparent;
            padding: 0;
            border-radius: 8px;
        }
        
        /* Correção específica para mobile */
        @media (max-width: 768px) {
            .hero-title {
                font-size: 2.5rem !important;
                line-height: 1.1 !important;
            }
            .hero-subtitle {
                font-size: 1.1rem !important;
            }
        }
        
        /* Scrollbar */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #0a0a0a; }
        ::-webkit-scrollbar-thumb { background: #d4af37; border-radius: 4px; }
    </style>
</head>
<body class="bg-boss-black text-white font-roboto overflow-x-hidden">

    <!-- Navegação -->
    <nav class="fixed w-full z-50 glass-effect border-b border-gray-800 top-0">
        <div class="container mx-auto px-6 py-3 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <div class="logo-container">
                    <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Boss Barbearia" class="h-22 md:h-14 w-auto logo-img" style="background: none;">
                </div>
                <div class="hidden md:block">
                    <h1 class="font-oswald text-xl font-bold tracking-wider text-white">BOSS <span class="text-boss-gold">BARBEARIA</span></h1>
                    <p class="text-[10px] text-gray-400 tracking-[0.2em]">SOCIAL CLUB</p>
                </div>
            </div>
            
            <div class="hidden md:flex items-center gap-6 text-sm">
                <a href="#inicio" class="hover:text-boss-gold transition-colors font-medium">Início</a>
                <a href="#servicos" class="hover:text-boss-gold transition-colors font-medium">Serviços</a>
                <a href="#agendamento" class="hover:text-boss-gold transition-colors font-medium">Agendar</a>
                <a href="#equipe" class="hover:text-boss-gold transition-colors font-medium">Equipe</a>
                <a href="#galeria" class="hover:text-boss-gold transition-colors font-medium">Galeria</a>
                <a href="#contato" class="hover:text-boss-gold transition-colors font-medium">Contato</a>
            </div>

            <button onclick="toggleMenu()" class="md:hidden text-2xl text-boss-gold p-2 focus:outline-none">
                <i class="fas fa-bars"></i>
            </button>
        </div>

        <!-- Menu Mobile -->
        <div id="mobile-menu" class="hidden md:hidden bg-boss-gray border-t border-gray-700 absolute w-full left-0">
            <div class="flex flex-col p-4 gap-1">
                <a href="#inicio" class="hover:text-boss-gold transition-colors py-3 px-4 border-b border-gray-800" onclick="toggleMenu()">Início</a>
                <a href="#servicos" class="hover:text-boss-gold transition-colors py-3 px-4 border-b border-gray-800" onclick="toggleMenu()">Serviços</a>
                <a href="#agendamento" class="hover:text-boss-gold transition-colors py-3 px-4 border-b border-gray-800" onclick="toggleMenu()">Agendar</a>
                <a href="#equipe" class="hover:text-boss-gold transition-colors py-3 px-4 border-b border-gray-800" onclick="toggleMenu()">Equipe</a>
                <a href="#galeria" class="hover:text-boss-gold transition-colors py-3 px-4 border-b border-gray-800" onclick="toggleMenu()">Galeria</a>
                <a href="#contato" class="hover:text-boss-gold transition-colors py-3 px-4" onclick="toggleMenu()">Contato</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="inicio" class="relative min-h-[90vh] flex items-center justify-center pt-20 overflow-hidden">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-b from-boss-black via-boss-black/80 to-boss-black z-10"></div>
            <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?w=1920&h=1080&fit=crop" alt="Barbearia" class="w-full h-full object-cover opacity-20">
        </div>

        <div class="container mx-auto px-6 relative z-20 text-center">
            <!-- Logo Grande -->
            <div class="mb-6 logo-container flex justify-center">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Logo Boss Barbearia" class="w-full max-w-[250px] md:max-w-[320px] h-auto logo-img" style="background: none; mix-blend-mode: normal;">
            </div>
            
            <h2 class="hero-title font-oswald text-4xl md:text-6xl lg:text-7xl font-bold mb-4 tracking-tight">
                ELEGÂNCIA & <span class="text-gold-gradient">ESTILO</span>
            </h2>
            
            <p class="hero-subtitle text-lg md:text-xl text-gray-300 mb-6 max-w-2xl mx-auto font-light">
                A experiência definitiva em cuidados masculinos em Patos - PB
            </p>
            
            <div class="flex flex-col md:flex-row gap-3 justify-center items-center mb-8">
                <div class="flex items-center gap-2 text-boss-gold bg-black/40 px-4 py-2 rounded-full">
                    <i class="fas fa-star"></i>
                    <span class="text-xl font-bold">4.9</span>
                    <span class="text-gray-300 text-sm">(84 avaliações)</span>
                </div>
                <div class="hidden md:block w-px h-6 bg-gray-600"></div>
                <div class="flex items-center gap-2 text-green-400 bg-black/40 px-4 py-2 rounded-full text-sm">
                    <i class="fas fa-check-circle"></i>
                    <span>Aberto Seg-Sáb: 9h às 20h</span>
                </div>
            </div>

            <div class="flex flex-col sm:flex-row gap-3 justify-center">
                <a href="#agendamento" class="bg-boss-gold text-black font-oswald font-bold text-base px-6 py-3 rounded hover-scale inline-flex items-center justify-center gap-2 shadow-lg shadow-yellow-900/30">
                    <i class="fas fa-calendar-alt"></i>
                    AGENDAR HORÁRIO
                </a>
                <a href="https://wa.me/5583998159090" target="_blank" class="border-2 border-boss-gold text-boss-gold font-oswald font-bold text-base px-6 py-3 rounded hover:bg-boss-gold hover:text-black transition-all inline-flex items-center justify-center gap-2">
                    <i class="fab fa-whatsapp"></i>
                    WHATSAPP
                </a>
            </div>
        </div>

        <div class="absolute bottom-8 left-1/2 transform -translate-x-1/2 animate-bounce">
            <i class="fas fa-chevron-down text-2xl text-boss-gold"></i>
        </div>
    </section>

    <!-- Serviços -->
    <section id="servicos" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-12">
                <h3 class="font-oswald text-3xl md:text-4xl font-bold mb-3">NOSSOS <span class="text-boss-gold">SERVIÇOS</span></h3>
                <div class="w-20 h-1 bg-boss-gold mx-auto"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Corte de Cabelo</h4>
                    <p class="text-gray-400 text-sm">Corte tradicional, degradê, tesoura ou navalha.</p>
                </div>

                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Barba & Navalha</h4>
                    <p class="text-gray-400 text-sm">Aparar, modelar ou barba completa com toalha quente.</p>
                </div>

                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-spa"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Barbaterapia</h4>
                    <p class="text-gray-400 text-sm">Tratamento com vapor de ozônio e relaxamento.</p>
                </div>

                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Coloração</h4>
                    <p class="text-gray-400 text-sm">Coloração de cabelo e barba, camuflagem de brancos.</p>
                </div>

                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-child"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Corte Infantil</h4>
                    <p class="text-gray-400 text-sm">Espaço kids com cadeira temática carro.</p>
                </div>

                <div class="bg-boss-black p-5 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-3xl mb-3 group-hover:scale-110 transition-transform">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h4 class="font-oswald text-lg font-bold mb-1">Sobrancelhas</h4>
                    <p class="text-gray-400 text-sm">Design e depilação de sobrancelhas.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Agendamento -->
    <section id="agendamento" class="py-16 bg-boss-black relative">
        <div class="absolute inset-0 bg-gradient-to-r from-boss-gold/5 to-transparent"></div>
        
        <div class="container mx-auto px-6 relative z-10">
            <div class="grid md:grid-cols-2 gap-10 items-center">
                <div>
                    <h3 class="font-oswald text-3xl md:text-4xl font-bold mb-4">
                        AGENDE SEU <span class="text-boss-gold">HORÁRIO</span>
                    </h3>
                    <p class="text-gray-300 mb-6 text-base">
                        Escolha o profissional, serviço e horário. Receba confirmação pelo WhatsApp.
                    </p>
                    
                    <div class="space-y-3 mb-6">
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold text-sm">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h5 class="font-bold text-sm">Segunda a Sábado</h5>
                                <p class="text-gray-400 text-xs">9h às 20h</p>
                            </div>
                        </div>
                        <div class="flex items-center gap-3">
                            <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold text-sm">
                                <i class="fas fa-credit-card"></i>
                            </div>
                            <div>
                                <h5 class="font-bold text-sm">Pagamento</h5>
                                <p class="text-gray-400 text-xs">Cartão, PIX, NFC</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="bg-boss-gray p-6 rounded-xl border border-gray-700 shadow-xl">
                    <form id="agendamentoForm" class="space-y-3" onsubmit="enviarAgendamento(event)">
                        <div>
                            <label class="block text-xs font-medium mb-1 text-gray-400">Nome</label>
                            <input type="text" id="nome" required class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm" placeholder="Seu nome completo">
                        </div>

                        <div class="grid grid-cols-2 gap-3">
                            <div>
                                <label class="block text-xs font-medium mb-1 text-gray-400">Data</label>
                                <input type="date" id="data" required class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm text-white">
                            </div>
                            <div>
                                <label class="block text-xs font-medium mb-1 text-gray-400">Horário</label>
                                <select id="horario" required class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm text-white">
                                    <option value="">Selecione</option>
                                    <option value="09:00">09:00</option>
                                    <option value="10:00">10:00</option>
                                    <option value="11:00">11:00</option>
                                    <option value="14:00">14:00</option>
                                    <option value="15:00">15:00</option>
                                    <option value="16:00">16:00</option>
                                    <option value="17:00">17:00</option>
                                    <option value="18:00">18:00</option>
                                </select>
                            </div>
                        </div>

                        <div>
                            <label class="block text-xs font-medium mb-1 text-gray-400">Profissional</label>
                            <select id="profissional" class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm text-white">
                                <option value="">Qualquer profissional</option>
                                <option value="Caio">Caio Chaves</option>
                                <option value="Silvino">Silvino</option>
                                <option value="Andrey">Andrey</option>
                                <option value="Matheus">Matheus</option>
                                <option value="Nathan">Nathan</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-xs font-medium mb-1 text-gray-400">Serviço</label>
                            <select id="servico" required class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm text-white">
                                <option value="">Selecione</option>
                                <option value="Corte">Corte de Cabelo</option>
                                <option value="Barba">Barba</option>
                                <option value="Corte+Barba">Corte + Barba</option>
                                <option value="Degrade">Degradê</option>
                                <option value="Infantil">Corte Infantil</option>
                                <option value="Tratamento">Barbaterapia</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-xs font-medium mb-1 text-gray-400">WhatsApp</label>
                            <input type="tel" id="telefone" required class="w-full bg-boss-black border border-gray-700 rounded px-3 py-2 focus:border-boss-gold focus:outline-none transition-colors text-sm text-white" placeholder="(83) 9XXXX-XXXX">
                        </div>

                        <button type="submit" class="w-full bg-boss-gold text-black font-oswald font-bold text-base py-3 rounded hover:bg-yellow-500 transition-colors flex items-center justify-center gap-2 mt-4">
                            <i class="fab fa-whatsapp"></i>
                            AGENDAR
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Equipe -->
    <section id="equipe" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-10">
                <h3 class="font-oswald text-3xl md:text-4xl font-bold mb-2">NOSSA <span class="text-boss-gold">EQUIPE</span></h3>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-4">
                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-0.5 mb-3 group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center">
                            <i class="fas fa-user text-3xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-base">Caio</h4>
                    <p class="text-boss-gold text-xs">Especialista</p>
                </div>

                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-0.5 mb-3 group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center">
                            <i class="fas fa-user text-3xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-base">Silvino</h4>
                    <p class="text-boss-gold text-xs">Master</p>
                </div>

                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-0.5 mb-3 group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center">
                            <i class="fas fa-user text-3xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-base">Andrey</h4>
                    <p class="text-boss-gold text-xs">Colorista</p>
                </div>

                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-0.5 mb-3 group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center">
                            <i class="fas fa-user text-3xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-base">Matheus</h4>
                    <p class="text-boss-gold text-xs">Barbeiro</p>
                </div>

                <div class="text-center group">
                    <div class="w-24 h-24 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-0.5 mb-3 group-hover:scale-105 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center">
                            <i class="fas fa-user text-3xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-base">Nathan</h4>
                    <p class="text-boss-gold text-xs">Consultor</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Depoimentos -->
    <section class="py-16 bg-boss-black border-y border-gray-800">
        <div class="container mx-auto px-6">
            <div class="text-center mb-10">
                <h3 class="font-oswald text-3xl md:text-4xl font-bold mb-3">AVALIAÇÕES <span class="text-boss-gold">GOOGLE</span></h3>
                <div class="flex justify-center items-center gap-1 text-boss-gold text-xl">
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <span class="text-white ml-2 text-base">4.9/5 (84 reviews)</span>
                </div>
            </div>

            <div class="grid md:grid-cols-3 gap-4">
                <div class="bg-boss-gray p-5 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-2 text-sm">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 text-sm mb-3">"O Caio superou minhas expectativas, ambiente acolhedor e profissional super gente fina."</p>
                    <div class="flex items-center gap-2">
                        <div class="w-8 h-8 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold text-xs">E</div>
                        <span class="text-xs text-gray-400">Edinaldo Baltazar</span>
                    </div>
                </div>

                <div class="bg-boss-gray p-5 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-2 text-sm">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 text-sm mb-3">"Serviço muito bom, fui muito bem atendido. Fiz corte personalizado e tratamento."</p>
                    <div class="flex items-center gap-2">
                        <div class="w-8 h-8 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold text-xs">J</div>
                        <span class="text-xs text-gray-400">João Arthur</span>
                    </div>
                </div>

                <div class="bg-boss-gray p-5 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-2 text-sm">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 text-sm mb-3">"Melhor impossível, barbeiros profissionais. Andrey tem muito talento."</p>
                    <div class="flex items-center gap-2">
                        <div class="w-8 h-8 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold text-xs">G</div>
                        <span class="text-xs text-gray-400">Giovanny José</span>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contato" class="py-16 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-8">
                <div>
                    <h3 class="font-oswald text-3xl font-bold mb-6">VISITE A <span class="text-boss-gold">BOSS</span></h3>
                    
                    <div class="space-y-4">
                        <div class="flex items-start gap-3">
                            <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0 text-sm">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-sm mb-1">Endereço</h4>
                                <p class="text-gray-400 text-sm">R. do Prado, 40 - Centro<br>Patos - PB, 58700-010</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-3">
                            <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0 text-sm">
                                <i class="fab fa-whatsapp"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-sm mb-1">WhatsApp</h4>
                                <p class="text-gray-400 text-sm">(83) 99815-9090</p>
                            </div>
                        </div>

                        <div class="flex items-start gap-3">
                            <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0 text-sm">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-sm mb-1">Funcionamento</h4>
                                <p class="text-gray-400 text-sm">Seg-Sáb: 09h às 20h<br><span class="text-red-400">Dom: Fechado</span></p>
                            </div>
                        </div>
                    </div>

                    <div class="mt-6 flex gap-3">
                        <a href="#" class="w-9 h-9 rounded-full bg-gray-800 flex items-center justify-center hover:bg-boss-gold hover:text-black transition-all text-sm">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-9 h-9 rounded-full bg-gray-800 flex items-center justify-center hover:bg-boss-gold hover:text-black transition-all text-sm">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                    </div>
                </div>

                <div class="bg-boss-black p-1 rounded-xl overflow-hidden h-64 md:h-auto">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3961.9!2d-37.28!3d-7.02!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0x0!2zPatos!5e0!3m2!1spt-BR!2sbr"
                        width="100%" 
                        height="100%" 
                        style="border:0; border-radius: 0.75rem; filter: grayscale(100%) invert(92%) contrast(83%);" 
                        allowfullscreen="" 
                        loading="lazy">
                    </iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black border-t border-gray-800 py-6">
        <div class="container mx-auto px-6 text-center">
            <p class="text-gray-500 text-xs mb-1">© 2026 Boss Barbearia - Social Club</p>
            <p class="text-gray-600 text-[10px]">Patos - PB</p>
        </div>
    </footer>

    <!-- Botão Flutuante -->
    <a href="https://wa.me/5583998159090" target="_blank" class="fixed bottom-4 right-4 bg-green-500 text-white w-14 h-14 rounded-full flex items-center justify-center text-2xl shadow-2xl hover:scale-110 transition-transform z-50">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }
        
        document.addEventListener('click', function(e) {
            const menu = document.getElementById('mobile-menu');
            const btn = e.target.closest('button');
            if (!menu.contains(e.target) && !btn && !menu.classList.contains('hidden')) {
                menu.classList.add('hidden');
            }
        });

        function enviarAgendamento(e) {
            e.preventDefault();
            const nome = document.getElementById('nome').value;
            const data = document.getElementById('data').value;
            const horario = document.getElementById('horario').value;
            const profissional = document.getElementById('profissional').value;
            const servico = document.getElementById('servico').value;
            const telefone = document.getElementById('telefone').value;

            const mensagem = `Olá! Agendamento Boss Barbearia:%0A%0A*Nome:* ${nome}%0A*Data:* ${data}%0A*Horário:* ${horario}%0A*Profissional:* ${profissional || 'Qualquer'}%0A*Serviço:* ${servico}%0A*Tel:* ${telefone}`;
            
            window.open(`https://wa.me/5583998159090?text=${mensagem}`, '_blank');
        }

        document.getElementById('data').min = new Date().toISOString().split('T')[0];
    </script>
</body>
</html>
