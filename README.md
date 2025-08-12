# Alura-aula-1-e-2-terceiro-bi

<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Serviços de Acessibilidade Digital</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        .wave-shape {
            position: absolute;
            bottom: 0;
            left: 0;
            width: 100%;
            overflow: hidden;
            line-height: 0;
            transform: rotate(180deg);
        }
        .wave-shape svg {
            position: relative;
            display: block;
            width: calc(100% + 1.3px);
            height: 150px;
        }
        .wave-shape .shape-fill {
            fill: #3B82F6;
        }
        .accessibility-toolbar {
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
        }
        .accessibility-btn {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            cursor: pointer;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            transition: all 0.3s ease;
        }
        .accessibility-btn:hover {
            transform: scale(1.1);
        }
        .accessibility-menu {
            position: absolute;
            bottom: 60px;
            right: 0;
            background: white;
            border-radius: 10px;
            padding: 10px;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
            display: none;
            width: 200px;
        }
        .accessibility-menu.show {
            display: block;
        }
        .accessibility-option {
            padding: 8px;
            cursor: pointer;
            border-radius: 5px;
            margin-bottom: 5px;
        }
        .accessibility-option:hover {
            background-color: #f0f0f0;
        }
        .high-contrast {
            filter: contrast(140%);
        }
        .grayscale {
            filter: grayscale(100%);
        }
        .bigger-text {
            font-size: 1.2rem;
        }
        .bigger-text p, .bigger-text li, .bigger-text a {
            font-size: 1.2rem;
        }
    </style>
</head>
<body class="font-sans bg-gray-50">
    <!-- Accessibility Toolbar -->
    <div class="accessibility-toolbar">
        <div class="accessibility-menu" id="accessibilityMenu">
            <div class="accessibility-option" onclick="toggleContrast()">
                <i class="fas fa-adjust mr-2"></i> Alto Contraste
            </div>
            <div class="accessibility-option" onclick="toggleGrayscale()">
                <i class="fas fa-palette mr-2"></i> Escala de Cinza
            </div>
            <div class="accessibility-option" onclick="toggleTextSize()">
                <i class="fas fa-text-height mr-2"></i> Aumentar Texto
            </div>
            <div class="accessibility-option" onclick="speakPage()">
                <i class="fas fa-volume-up mr-2"></i> Ler Página
            </div>
        </div>
        <div class="accessibility-btn bg-blue-500 text-white" id="accessibilityBtn" onclick="toggleMenu()">
            <i class="fas fa-universal-access text-2xl"></i>
        </div>
    </div>

    <!-- Header -->
    <header class="relative bg-blue-600 text-white overflow-hidden">
        <div class="container mx-auto px-4 py-16 md:py-24 relative z-10">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h1 class="text-4xl md:text-5xl font-bold mb-4">Acessibilidade Digital para Todos</h1>
                    <p class="text-xl mb-8">Tornamos a web mais inclusiva com soluções personalizadas de acessibilidade.</p>
                    <a href="#contact" class="bg-white text-blue-600 font-semibold px-6 py-3 rounded-lg hover:bg-blue-50 transition duration-300 inline-block">
                        Entre em Contato
                    </a>
                </div>
                <div class="md:w-1/2 flex justify-center">
                    <img src="https://img.freepik.com/free-vector/accessible-concept-illustration_114360-8206.jpg" alt="Ilustração de acessibilidade digital" class="w-full max-w-md rounded-lg shadow-xl">
                </div>
            </div>
        </div>
        <div class="wave-shape">
            <svg data-name="Layer 1" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1200 120" preserveAspectRatio="none">
                <path d="M321.39,56.44c58-10.79,114.16-30.13,172-41.86,82.39-16.72,168.19-17.73,250.45-.39C823.78,31,906.67,72,985.66,92.83c70.05,18.48,146.53,26.09,214.34,3V0H0V27.35A600.21,600.21,0,0,0,321.39,56.44Z" class="shape-fill"></path>
            </svg>
        </div>
    </header>

    <!-- Services -->
    <section class="py-16 bg-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12 text-gray-800">Nossos Serviços</h2>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                <!-- Service 1 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-eye"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Auditoria de Acessibilidade</h3>
                    <p class="text-gray-600">Avaliação completa do seu site para identificar barreiras de acessibilidade e propor soluções.</p>
                </div>
                                
                <!-- Service 2 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-code"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Desenvolvimento Acessível</h3>
                    <p class="text-gray-600">Criação de websites e aplicações com acessibilidade desde o início do projeto.</p>
                </div>
                                
                <!-- Service 3 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-graduation-cap"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Treinamentos</h3>
                    <p class="text-gray-600">Capacitação para equipes sobre boas práticas de acessibilidade digital.</p>
                </div>
                                
                <!-- Service 4 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-file-alt"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Documentos Acessíveis</h3>
                    <p class="text-gray-600">Adaptação de PDFs, apresentações e outros documentos para torná-los acessíveis.</p>
                </div>
                                
                <!-- Service 5 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-mobile-alt"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Aplicativos Acessíveis</h3>
                    <p class="text-gray-600">Desenvolvimento de aplicativos móveis que seguem as diretrizes de acessibilidade.</p>
                </div>
                                
                <!-- Service 6 -->
                <div class="bg-gray-50 p-6 rounded-lg shadow-md hover:shadow-lg transition duration-300">
                    <div class="text-blue-500 text-4xl mb-4">
                        <i class="fas fa-search"></i>
                    </div>
                    <h3 class="text-xl font-semibold mb-3">Consultoria Especializada</h3>
                    <p class="text-gray-600">Apoio técnico para implementação de soluções de acessibilidade em projetos existentes.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- About -->
    <section class="py-16 bg-gray-100">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row items-center">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <img src="https://img.freepik.com/free-vector/people-with-disabilities-concept-illustration_114360-10061.jpg" alt="Pessoas com diferentes tipos de deficiência" class="w-full rounded-lg shadow-lg">
                </div>
                <div class="md:w-1/2 md:pl-12">
                    <h2 class="text-3xl font-bold mb-6 text-gray-800">Sobre Nós</h2>
                    <p class="text-gray-600 mb-4">Somos uma equipe especializada em acessibilidade digital, comprometida em eliminar barreiras e promover a inclusão na web.</p>
                    <p class="text-gray-600 mb-6">Acreditamos que a tecnologia deve ser acessível a todos, independentemente de suas capacidades físicas, sensoriais ou cognitivas.</p>
                    <div class="space-y-3">
                        <div class="flex items-start">
                            <div class="text-blue-500 mr-3 mt-1">
                                <i class="fas fa-check-circle"></i>
                            </div>
                            <p class="text-gray-600">Experiência em projetos de acessibilidade para diversos setores</p>
                        </div>
                        <div class="flex items-start">
                            <div class="text-blue-500 mr-3 mt-1">
                                <i class="fas fa-check-circle"></i>
                            </div>
                            <p class="text-gray-600">Conhecimento profundo das diretrizes WCAG e legislações</p>
                        </div>
                        <div class="flex items-start">
                            <div class="text-blue-500 mr-3 mt-1">
                                <i class="fas fa-check-circle"></i>
                            </div>
                            <p class="text-gray-600">Abordagem prática e centrada no usuário</p>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact -->
    <section id="contact" class="py-16 bg-blue-600 text-white">
        <div class="container mx-auto px-4">
            <h2 class="text-3xl font-bold text-center mb-12">Entre em Contato</h2>
            <div class="flex flex-col md:flex-row">
                <div class="md:w-1/2 mb-10 md:mb-0">
                    <h3 class="text-xl font-semibold mb-4">Informações de Contato</h3>
                    <div class="space-y-4">
                        <div class="flex items-start">
                            <div class="mr-4 mt-1">
                                <i class="fas fa-envelope"></i>
                            </div>
                            <div>
                                <p class="font-medium">Email</p>
                                <p>contato@empresa.com</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="mr-4 mt-1">
                                <i class="fas fa-phone-alt"></i>
                            </div>
                            <div>
                                <p class="font-medium">Telefone</p>
                                <p>(00) 0000-0000</p>
                            </div>
                        </div>
                        <div class="flex items-start">
                            <div class="mr-4 mt-1">
                                <i class="fas fa-map-marker-alt"></i>
                            </div>
                            <div>
                                <p class="font-medium">Endereço</p>
                                <p>Rua Exemplo, 123 - Centro</p>
                                <p>Cidade/Estado - Brasil</p>
                            </div>
                        </div>
                    </div>
                    <div class="mt-8">
                        <h3 class="text-xl font-semibold mb-4">Redes Sociais</h3>
                        <div class="flex space-x-4">
                            <a href="#" class="bg-white text-blue-600 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-50 transition duration-300">
                                <i class="fab fa-facebook-f"></i>
                            </a>
                            <a href="#" class="bg-white text-blue-600 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-50 transition duration-300">
                                <i class="fab fa-twitter"></i>
                            </a>
                            <a href="#" class="bg-white text-blue-600 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-50 transition duration-300">
                                <i class="fab fa-linkedin-in"></i>
                            </a>
                            <a href="#" class="bg-white text-blue-600 w-10 h-10 rounded-full flex items-center justify-center hover:bg-blue-50 transition duration-300">
                                <i class="fab fa-instagram"></i>
                            </a>
                        </div>
                    </div>
                </div>
                <div class="md:w-1/2 md:pl-12">
                    <h3 class="text-xl font-semibold mb-4">Envie uma Mensagem</h3>
                    <form class="space-y-4">
                        <div>
                            <label for="name" class="block mb-1">Nome</label>
                            <input type="text" id="name" class="w-full px-4 py-2 rounded-lg bg-blue-500 bg-opacity-50 border border-blue-400 focus:outline-none focus:ring-2 focus:ring-white focus:border-transparent placeholder-blue-200" placeholder="Seu nome">
                        </div>
                        <div>
                            <label for="email" class="block mb-1">Email</label>
                            <input type="email" id="email" class="w-full px-4 py-2 rounded-lg bg-blue-500 bg-opacity-50 border border-blue-400 focus:outline-none focus:ring-2 focus:ring-white focus:border-transparent placeholder-blue-200" placeholder="Seu email">
                        </div>
                        <div>
                            <label for="subject" class="block mb-1">Assunto</label>
                            <input type="text" id="subject" class="w-full px-4 py-2 rounded-lg bg-blue-500 bg-opacity-50 border border-blue-400 focus:outline-none focus:ring-2 focus:ring-white focus:border-transparent placeholder-blue-200" placeholder="Assunto da mensagem">
                        </div>
                        <div>
                            <label for="message" class="block mb-1">Mensagem</label>
                            <textarea id="message" rows="4" class="w-full px-4 py-2 rounded-lg bg-blue-500 bg-opacity-50 border border-blue-400 focus:outline-none focus:ring-2 focus:ring-white focus:border-transparent placeholder-blue-200" placeholder="Sua mensagem"></textarea>
                        </div>
                        <button type="submit" class="bg-white text-blue-600 font-semibold px-6 py-3 rounded-lg hover:bg-blue-50 transition duration-300">
                            Enviar Mensagem
                        </button>
                    </form>
                </div>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-800 text-white py-8">
        <div class="container mx-auto px-4">
            <div class="flex flex-col md:flex-row justify-between items-center">
                <div class="mb-4 md:mb-0">
                    
    <script>
        // Accessibility functions
        function toggleMenu() {
            const menu = document.getElementById('accessibilityMenu');
            menu.classList.toggle('show');
        }

        function toggleContrast() {
            document.body.classList.toggle('high-contrast');
        }

        function toggleGrayscale() {
            document.body.classList.toggle('grayscale');
        }

        function toggleTextSize() {
            document.body.classList.toggle('bigger-text');
        }

        function speakPage() {
            if ('speechSynthesis' in window) {
                const speech = new SpeechSynthesisUtterance();
                speech.text = document.body.innerText;
                speech.lang = 'pt-BR';
                window.speechSynthesis.speak(speech);
            } else {
                alert('Seu navegador não suporta a síntese de voz.');
            }
        }

        // Close accessibility menu when clicking outside
        document.addEventListener('click', function(event) {
            const btn = document.getElementById('accessibilityBtn');
            const menu = document.getElementById('accessibilityMenu');
                        
            if (!btn.contains(event.target) && !menu.contains(event.target)) {
                menu.classList.remove('show');
            }
        });

        // Smooth scrolling for anchor links
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                document.querySelector(this.getAttribute('href')).scrollIntoView({
                    behavior: 'smooth'
                });
            });
        });
    </script>
</body>
</html>
