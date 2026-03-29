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
                        'boss-silver': '#c0c0c0',
                    }
                }
            }
        }
    </script>
    <style>
        .fade-in { animation: fadeIn 0.8s ease-in; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }
        .hover-scale { transition: transform 0.3s ease; }
        .hover-scale:hover { transform: scale(1.05); }
        .glass-effect { background: rgba(26, 26, 26, 0.95); backdrop-filter: blur(10px); }
        
        /* Correção do degradê dourado para texto */
        .text-gold-gradient {
            background: linear-gradient(135deg, #d4af37 0%, #f4e5c2 50%, #d4af37 100%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            background-clip: text;
        }
        
        /* Remover fundo branco do logo */
        .logo-transparent {
            filter: brightness(1.1) contrast(1.1);
            mix-blend-mode: screen;
        }
        
        /* Scrollbar estilizada */
        ::-webkit-scrollbar { width: 8px; }
        ::-webkit-scrollbar-track { background: #0a0a0a; }
        ::-webkit-scrollbar-thumb { background: #d4af37; border-radius: 4px; }
    </style>
</head>
<body class="bg-boss-black text-white font-roboto overflow-x-hidden">

    <!-- Navegação -->
    <nav class="fixed w-full z-50 glass-effect border-b border-gray-800">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <div class="flex items-center gap-3">
                <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Boss Barbearia" class="h-12 md:h-16 w-auto object-contain logo-transparent">
                <div class="hidden md:block">
                    <h1 class="font-oswald text-2xl font-bold tracking-wider">BOSS <span class="text-boss-gold">BARBEARIA</span></h1>
                    <p class="text-xs text-gray-400 tracking-widest">SOCIAL CLUB</p>
                </div>
            </div>
            
            <div class="hidden md:flex items-center gap-8">
                <a href="#inicio" class="hover:text-boss-gold transition-colors font-medium">Início</a>
                <a href="#servicos" class="hover:text-boss-gold transition-colors font-medium">Serviços</a>
                <a href="#agendamento" class="hover:text-boss-gold transition-colors font-medium">Agendar</a>
                <a href="#equipe" class="hover:text-boss-gold transition-colors font-medium">Equipe</a>
                <a href="#galeria" class="hover:text-boss-gold transition-colors font-medium">Galeria</a>
                <a href="#contato" class="hover:text-boss-gold transition-colors font-medium">Contato</a>
            </div>

            <button onclick="toggleMenu()" class="md:hidden text-2xl text-boss-gold p-2">
                <i class="fas fa-bars"></i>
            </button>
        </div>

        <!-- Menu Mobile -->
        <div id="mobile-menu" class="hidden md:hidden bg-boss-gray border-t border-gray-700 absolute w-full">
            <div class="flex flex-col p-6 gap-4">
                <a href="#inicio" class="hover:text-boss-gold transition-colors py-2 border-b border-gray-800" onclick="toggleMenu()">Início</a>
                <a href="#servicos" class="hover:text-boss-gold transition-colors py-2 border-b border-gray-800" onclick="toggleMenu()">Serviços</a>
                <a href="#agendamento" class="hover:text-boss-gold transition-colors py-2 border-b border-gray-800" onclick="toggleMenu()">Agendar</a>
                <a href="#equipe" class="hover:text-boss-gold transition-colors py-2 border-b border-gray-800" onclick="toggleMenu()">Equipe</a>
                <a href="#contato" class="hover:text-boss-gold transition-colors py-2" onclick="toggleMenu()">Contato</a>
            </div>
        </div>
    </nav>

    <!-- Hero Section -->
    <section id="inicio" class="relative min-h-screen flex items-center justify-center pt-24 overflow-hidden">
        <div class="absolute inset-0 z-0">
            <div class="absolute inset-0 bg-gradient-to-b from-boss-black/90 via-boss-black/70 to-boss-black z-10"></div>
            <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?w=1920&h=1080&fit=crop" alt="Barbearia" class="w-full h-full object-cover opacity-30">
        </div>

        <div class="container mx-auto px-6 relative z-20 text-center">
            <div class="fade-in">
                <div class="mb-8 inline-block">
                    <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Logo Boss Barbearia" class="mx-auto w-full max-w-[300px] md:max-w-[400px] h-auto drop-shadow-2xl logo-transparent">
                </div>
                
                <h2 class="font-oswald text-4xl md:text-6xl lg:text-7xl font-bold mb-6 tracking-tight leading-tight">
                    ELEGÂNCIA & <span class="text-gold-gradient">ESTILO</span>
                </h2>
                
                <p class="text-lg md:text-2xl text-gray-300 mb-8 max-w-2xl mx-auto font-light">
                    A experiência definitiva em cuidados masculinos em Patos - PB
                </p>
                
                <div class="flex flex-col md:flex-row gap-4 justify-center items-center mb-12">
                    <div class="flex items-center gap-2 text-boss-gold bg-black/30 px-4 py-2 rounded-full backdrop-blur-sm">
                        <i class="fas fa-star text-xl"></i>
                        <span class="text-2xl font-bold">4.9</span>
                        <span class="text-gray-300 text-sm">(84 avaliações)</span>
                    </div>
                    <div class="hidden md:block w-px h-8 bg-gray-600"></div>
                    <div class="flex items-center gap-2 text-green-400 bg-black/30 px-4 py-2 rounded-full backdrop-blur-sm">
                        <i class="fas fa-check-circle"></i>
                        <span>Aberto Seg-Sáb: 9h às 20h</span>
                    </div>
                </div>

                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <a href="#agendamento" class="bg-boss-gold text-black font-oswald font-bold text-lg px-8 py-4 rounded-lg hover-scale inline-flex items-center justify-center gap-2 shadow-lg shadow-yellow-900/20">
                        <i class="fas fa-calendar-alt"></i>
                        AGENDAR HORÁRIO
                    </a>
                    <a href="https://wa.me/5583998159090" target="_blank" class="border-2 border-boss-gold text-boss-gold font-oswald font-bold text-lg px-8 py-4 rounded-lg hover:bg-boss-gold hover:text-black transition-all inline-flex items-center justify-center gap-2">
                        <i class="fab fa-whatsapp"></i>
                        WHATSAPP
                    </a>
                </div>
            </div>
        </div>

        <div class="absolute bottom-10 left-1/2 transform -translate-x-1/2 animate-bounce">
            <i class="fas fa-chevron-down text-3xl text-boss-gold"></i>
        </div>
    </section>

    <!-- Serviços -->
    <section id="servicos" class="py-20 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h3 class="font-oswald text-4xl md:text-5xl font-bold mb-4">NOSSOS <span class="text-boss-gold">SERVIÇOS</span></h3>
                <div class="w-24 h-1 bg-boss-gold mx-auto"></div>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-cut"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Corte de Cabelo</h4>
                    <p class="text-gray-400 text-sm">Corte tradicional, degradê, tesoura ou navalha. Personalizado ao seu estilo.</p>
                </div>

                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-user-tie"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Barba & Navalha</h4>
                    <p class="text-gray-400 text-sm">Aparar, modelar ou barba completa com toalha quente e navalha.</p>
                </div>

                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-spa"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Barbaterapia</h4>
                    <p class="text-gray-400 text-sm">Tratamento completo com vapor de ozônio, hidratação e relaxamento.</p>
                </div>

                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-paint-brush"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Coloração</h4>
                    <p class="text-gray-400 text-sm">Coloração de cabelo e barba, tingimento e camuflagem de brancos.</p>
                </div>

                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-child"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Corte Infantil</h4>
                    <p class="text-gray-400 text-sm">Espaço kids com cadeira temática carro, especializado em crianças.</p>
                </div>

                <div class="bg-boss-black p-6 rounded-lg border border-gray-800 hover:border-boss-gold transition-all hover-scale group">
                    <div class="text-boss-gold text-4xl mb-4 group-hover:scale-110 transition-transform">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h4 class="font-oswald text-xl font-bold mb-2">Sobrancelhas</h4>
                    <p class="text-gray-400 text-sm">Design e depilação de sobrancelhas, coloração e alinhamento.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Agendamento -->
    <section id="agendamento" class="py-20 bg-boss-black relative overflow-hidden">
        <div class="absolute inset-0 bg-gradient-to-r from-boss-gold/5 to-transparent"></div>
        
        <div class="container mx-auto px-6 relative z-10">
            <div class="grid md:grid-cols-2 gap-12 items-center">
                <div>
                    <h3 class="font-oswald text-4xl md:text-5xl font-bold mb-6">
                        AGENDE SEU <span class="text-boss-gold">HORÁRIO</span>
                    </h3>
                    <p class="text-gray-300 mb-8 text-lg">
                        Escolha o profissional, serviço e horário de sua preferência. 
                        Receba confirmação imediata pelo WhatsApp.
                    </p>
                    
                    <div class="space-y-4 mb-8">
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold">
                                <i class="fas fa-clock"></i>
                            </div>
                            <div>
                                <h5 class="font-bold">Horário Flexível</h5>
                                <p class="text-gray-400 text-sm">Segunda a Sábado das 9h às 20h</p>
                            </div>
                        </div>
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold">
                                <i class="fas fa-credit-card"></i>
                            </div>
                            <div>
                                <h5 class="font-bold">Pagamento Fácil</h5>
                                <p class="text-gray-400 text-sm">Cartão, PIX, NFC e dinheiro</p>
                            </div>
                        </div>
                        <div class="flex items-center gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold">
                                <i class="fas fa-wheelchair"></i>
                            </div>
                            <div>
                                <h5 class="font-bold">Acessibilidade</h5>
                                <p class="text-gray-400 text-sm">Entrada adaptada para cadeirantes</p>
                            </div>
                        </div>
                    </div>
                </div>

                <div class="bg-boss-gray p-8 rounded-2xl border border-gray-700 shadow-2xl">
                    <form id="agendamentoForm" class="space-y-4" onsubmit="enviarAgendamento(event)">
                        <div>
                            <label class="block text-sm font-medium mb-2 text-gray-300">Seu Nome</label>
                            <input type="text" id="nome" required class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white" placeholder="Digite seu nome completo">
                        </div>

                        <div class="grid grid-cols-2 gap-4">
                            <div>
                                <label class="block text-sm font-medium mb-2 text-gray-300">Data</label>
                                <input type="date" id="data" required class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white">
                            </div>
                            <div>
                                <label class="block text-sm font-medium mb-2 text-gray-300">Horário</label>
                                <select id="horario" required class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white">
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
                            <label class="block text-sm font-medium mb-2 text-gray-300">Profissional</label>
                            <select id="profissional" class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white">
                                <option value="">Qualquer profissional</option>
                                <option value="Caio">Caio Chaves</option>
                                <option value="Silvino">Silvino</option>
                                <option value="Andrey">Andrey</option>
                                <option value="Matheus">Matheus</option>
                                <option value="Nathan">Nathan</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium mb-2 text-gray-300">Serviço</label>
                            <select id="servico" required class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white">
                                <option value="">Selecione o serviço</option>
                                <option value="Corte">Corte de Cabelo</option>
                                <option value="Barba">Barba</option>
                                <option value="Corte+Barba">Corte + Barba</option>
                                <option value="Degrade">Degradê</option>
                                <option value="Infantil">Corte Infantil</option>
                                <option value="Tratamento">Barbaterapia</option>
                            </select>
                        </div>

                        <div>
                            <label class="block text-sm font-medium mb-2 text-gray-300">Telefone (WhatsApp)</label>
                            <input type="tel" id="telefone" required class="w-full bg-boss-black border border-gray-700 rounded-lg px-4 py-3 focus:border-boss-gold focus:outline-none transition-colors text-white" placeholder="(83) 9XXXX-XXXX">
                        </div>

                        <button type="submit" class="w-full bg-boss-gold text-black font-oswald font-bold text-lg py-4 rounded-lg hover:bg-yellow-500 transition-colors flex items-center justify-center gap-2 mt-6">
                            <i class="fab fa-whatsapp"></i>
                            CONFIRMAR AGENDAMENTO
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Equipe -->
    <section id="equipe" class="py-20 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h3 class="font-oswald text-4xl md:text-5xl font-bold mb-4">NOSSA <span class="text-boss-gold">EQUIPE</span></h3>
                <p class="text-gray-400 max-w-2xl mx-auto">Profissionais especializados prontos para cuidar do seu visual</p>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 lg:grid-cols-5 gap-6">
                <div class="text-center group">
                    <div class="w-32 h-32 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-1 mb-4 group-hover:scale-110 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center overflow-hidden">
                            <i class="fas fa-user text-4xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-lg">Caio Chaves</h4>
                    <p class="text-boss-gold text-sm">Especialista</p>
                </div>

                <div class="text-center group">
                    <div class="w-32 h-32 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-1 mb-4 group-hover:scale-110 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center overflow-hidden">
                            <i class="fas fa-user text-4xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-lg">Silvino</h4>
                    <p class="text-boss-gold text-sm">Barbeiro Master</p>
                </div>

                <div class="text-center group">
                    <div class="w-32 h-32 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-1 mb-4 group-hover:scale-110 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center overflow-hidden">
                            <i class="fas fa-user text-4xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-lg">Andrey</h4>
                    <p class="text-boss-gold text-sm">Colorista</p>
                </div>

                <div class="text-center group">
                    <div class="w-32 h-32 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-1 mb-4 group-hover:scale-110 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center overflow-hidden">
                            <i class="fas fa-user text-4xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-lg">Matheus</h4>
                    <p class="text-boss-gold text-sm">Profissional</p>
                </div>

                <div class="text-center group">
                    <div class="w-32 h-32 mx-auto bg-gradient-to-br from-boss-gold to-yellow-600 rounded-full p-1 mb-4 group-hover:scale-110 transition-transform">
                        <div class="w-full h-full bg-boss-gray rounded-full flex items-center justify-center overflow-hidden">
                            <i class="fas fa-user text-4xl text-gray-600"></i>
                        </div>
                    </div>
                    <h4 class="font-oswald font-bold text-lg">Nathan</h4>
                    <p class="text-boss-gold text-sm">Consultor</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Depoimentos -->
    <section class="py-20 bg-boss-black border-y border-gray-800">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h3 class="font-oswald text-4xl md:text-5xl font-bold mb-4">O QUE DIZEM <span class="text-boss-gold">NOSSOS CLIENTES</span></h3>
                <div class="flex justify-center items-center gap-2 text-boss-gold text-2xl mb-4">
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <i class="fas fa-star"></i>
                    <span class="text-white ml-2 text-lg">4.9/5 (84 avaliações)</span>
                </div>
            </div>

            <div class="grid md:grid-cols-2 lg:grid-cols-3 gap-6">
                <div class="bg-boss-gray p-6 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 mb-4">"Tive a satisfação de conhecer o Caio Chaves na boss e superou totalmente as minhas expectativas, além ambiente acolhedor o Caio foi super profissional, muito gente fina."</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold">E</div>
                        <div>
                            <h5 class="font-bold text-sm">Edinaldo Baltazar</h5>
                            <p class="text-gray-500 text-xs">2 avaliações</p>
                        </div>
                    </div>
                </div>

                <div class="bg-boss-gray p-6 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 mb-4">"Serviço muito bom, fui muito bem atendido. Fiz shampoo, condicionador, tratamento para o couro cabeludo e corte personalizado. Ambiente excelente!"</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold">J</div>
                        <div>
                            <h5 class="font-bold text-sm">João Arthur Ferreira</h5>
                            <p class="text-gray-500 text-xs">Local Guide</p>
                        </div>
                    </div>
                </div>

                <div class="bg-boss-gray p-6 rounded-lg border border-gray-800">
                    <div class="flex text-boss-gold mb-3">
                        <i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i><i class="fas fa-star"></i>
                    </div>
                    <p class="text-gray-300 mb-4">"Melhor impossível, barbeiro muito profissionais. Andrey novo mais tem muito talento show de bola, Matheus um profissional nato, nathan ótimo conselheiro."</p>
                    <div class="flex items-center gap-3">
                        <div class="w-10 h-10 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold font-bold">G</div>
                        <div>
                            <h5 class="font-bold text-sm">Giovanny José Galvão</h5>
                            <p class="text-gray-500 text-xs">Cliente verificado</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Galeria -->
    <section id="galeria" class="py-20 bg-boss-gray">
        <div class="container mx-auto px-6">
            <div class="text-center mb-16">
                <h3 class="font-oswald text-4xl md:text-5xl font-bold mb-4">GALERIA <span class="text-boss-gold">BOSS</span></h3>
            </div>

            <div class="grid grid-cols-2 md:grid-cols-3 gap-4">
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1585747860715-2ba37e788b70?w=600&h=600&fit=crop" alt="Interior" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1622286342621-4bd786c2447c?w=600&h=600&fit=crop" alt="Corte" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1599351431202-1e0f0137899a?w=600&h=600&fit=crop" alt="Barba" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1503951914875-452162b0f3f1?w=600&h=600&fit=crop" alt="Ambiente" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1621605815971-fbc98d665033?w=600&h=600&fit=crop" alt="Loja" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
                <div class="aspect-square overflow-hidden rounded-lg group cursor-pointer">
                    <img src="https://images.unsplash.com/photo-1493256338651-d82f7acb2b38?w=600&h=600&fit=crop" alt="Produtos" class="w-full h-full object-cover group-hover:scale-110 transition-transform duration-500">
                </div>
            </div>
        </div>
    </section>

    <!-- Contato -->
    <section id="contato" class="py-20 bg-boss-black">
        <div class="container mx-auto px-6">
            <div class="grid md:grid-cols-2 gap-12">
                <div>
                    <h3 class="font-oswald text-4xl font-bold mb-6">VISITE A <span class="text-boss-gold">BOSS</span></h3>
                    
                    <div class="space-y-6">
                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0">
                                <i class="fas fa-map-marker-alt text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg mb-1">Endereço</h4>
                                <p class="text-gray-400">R. do Prado, 40 - Centro<br>Patos - PB, 58700-010</p>
                                <a href="https://maps.google.com/?q=R.+do+Prado,+40+Patos+PB" target="_blank" class="text-boss-gold text-sm hover:underline mt-2 inline-block">Ver no mapa →</a>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0">
                                <i class="fab fa-whatsapp text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg mb-1">WhatsApp</h4>
                                <p class="text-gray-400">(83) 99815-9090</p>
                                <a href="https://wa.me/5583998159090" target="_blank" class="text-boss-gold text-sm hover:underline mt-2 inline-block">Enviar mensagem →</a>
                            </div>
                        </div>

                        <div class="flex items-start gap-4">
                            <div class="w-12 h-12 rounded-full bg-boss-gold/20 flex items-center justify-center text-boss-gold flex-shrink-0">
                                <i class="fas fa-clock text-xl"></i>
                            </div>
                            <div>
                                <h4 class="font-bold text-lg mb-1">Horário de Funcionamento</h4>
                                <p class="text-gray-400">
                                    Segunda a Sábado: 09h às 20h<br>
                                    <span class="text-red-400">Domingo: Fechado</span>
                                </p>
                            </div>
                        </div>
                    </div>

                    <div class="mt-8 flex gap-4">
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-boss-gold hover:text-black transition-all">
                            <i class="fab fa-instagram"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-boss-gold hover:text-black transition-all">
                            <i class="fab fa-facebook-f"></i>
                        </a>
                        <a href="#" class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-boss-gold hover:text-black transition-all">
                            <i class="fab fa-tiktok"></i>
                        </a>
                    </div>
                </div>

                <div class="bg-boss-gray p-2 rounded-2xl overflow-hidden h-96">
                    <iframe 
                        src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3961.952956xxxxx!2d-37.28xxxx!3d-7.02xxxx!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x7a0b0xxxxxxx%3A0x0!2zQ2VudHJvLCBQYXRvcyAtIFBC!5e0!3m2!1spt-BR!2sbr!4v1"
                        width="100%" 
                        height="100%" 
                        style="border:0; border-radius: 1rem;" 
                        allowfullscreen="" 
                        loading="lazy"
                        class="grayscale hover:grayscale-0 transition-all duration-500">
                    </iframe>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-black border-t border-gray-800 py-8">
        <div class="container mx-auto px-6 text-center">
            <img src="https://i.postimg.cc/HkqZfnMz/boss.png" alt="Logo" class="h-16 mx-auto mb-4 opacity-80 logo-transparent">
            <p class="text-gray-500 text-sm mb-2">© 2026 Boss Barbearia - Social Club. Todos os direitos reservados.</p>
            <p class="text-gray-600 text-xs">Desenvolvido para excelência em cuidados masculinos</p>
        </div>
    </footer>

    <!-- Botão Flutuante WhatsApp -->
    <a href="https://wa.me/5583998159090" target="_blank" class="fixed bottom-6 right-6 bg-green-500 text-white w-16 h-16 rounded-full flex items-center justify-center text-3xl shadow-2xl hover:scale-110 transition-transform z-50 animate-pulse">
        <i class="fab fa-whatsapp"></i>
    </a>

    <script>
        // Menu Mobile
        function toggleMenu() {
            const menu = document.getElementById('mobile-menu');
            menu.classList.toggle('hidden');
        }

        // Fechar menu ao clicar fora
        document.addEventListener('click', function(event) {
            const menu = document.getElementById('mobile-menu');
            const button = event.target.closest('button');
            if (!menu.contains(event.target) && !button) {
                menu.classList.add('hidden');
            }
        });

        // Formulário de Agendamento
        function enviarAgendamento(e) {
            e.preventDefault();
            
            const nome = document.getElementById('nome').value;
            const data = document.getElementById('data').value;
            const horario = document.getElementById('horario').value;
            const profissional = document.getElementById('profissional').value;
            const servico = document.getElementById('servico').value;
            const telefone = document.getElementById('telefone').value;

            const mensagem = `Olá! Gostaria de agendar um horário na Boss Barbearia:%0A%0A` +
                           `*Nome:* ${nome}%0A` +
                           `*Data:* ${data}%0A` +
                           `*Horário:* ${horario}%0A` +
                           `*Profissional:* ${profissional || 'Qualquer'}%0A` +
                           `*Serviço:* ${servico}%0A` +
                           `*Telefone:* ${telefone}`;

            window.open(`https://wa.me/5583998159090?text=${mensagem}`, '_blank');
        }

        // Configurar data mínima como hoje
        document.getElementById('data').min = new Date().toISOString().split('T')[0];
    </script>
</body>
</html>
