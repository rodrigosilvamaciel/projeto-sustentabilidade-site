<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Balanço Sustentável: Projeto Papel - Resultados e Conscientização</title>
    <!-- Inclui Tailwind CSS para estilização moderna e responsiva -->
    <script src="https://cdn.tailwindcss.com"></script>
    <style>
        /* Configuração de fonte Inter para uma estética limpa */
        body {
            font-family: 'Inter', sans-serif;
            /* Adicionar imagem de fundo inspirada na natureza */
            background-image: url('https://i.imgur.com/LU2cIkA.jpeg'); /* NOVA IMAGEM DE FUNDO */
            background-size: cover;
            background-position: center;
            background-attachment: fixed; /* Imagem fica fixa ao rolar */
            position: relative; /* Necessário para o overlay */
            z-index: 1; /* Garante que o conteúdo fique acima do overlay */
        }

        /* Camada de overlay semi-transparente para melhorar a leitura do texto sobre a imagem de fundo */
        body::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background-color: rgba(255, 255, 255, 0.75); /* Branco com 75% de opacidade */
            z-index: -1; /* Fica abaixo do conteúdo, mas acima do background-image */
        }

        /* Estilos personalizados para os ícones - Mantidos visíveis e ajustados para tons de natureza */
        .icon {
            display: inline-block;
            width: 32px; /* Ícones maiores */
            height: 32px; /* Ícones maiores */
            vertical-align: middle;
            margin-right: 12px; /* Mais espaço */
        }
        .icon-tree {
            fill: #059669; /* Verde esmeralda escuro */
        }
        .icon-water {
            fill: #0284C7; /* Azul profundo */
        }
        .icon-recycle {
            fill: #22C55E; /* Verde forte */
        }
        /* Novo ícone para árvores utilizadas, mantendo a cor verde para consistência temática */
        .icon-tree-used {
            fill: #739E04; /* Um verde um pouco mais escuro para diferenciar sutilmente */
        }

        /* Estilo para a caixa de destaque dos dados */
        .data-card {
            background-color: #FFFFFF; /* Fundo branco puro */
            border: 2px solid #E0F2F7; /* Borda sutil em azul claro */
            border-radius: 16px; /* Cantos mais arredondados */
            padding: 1.5rem;
            margin-bottom: 1rem;
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
            transition: all 0.3s ease-in-out;
            position: relative;
            overflow: hidden;
        }
        .data-card:hover {
            transform: translateY(-8px) scale(1.02);
            box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.15), 0 10px 10px -5px rgba(0, 0, 0, 0.08);
            border-color: #60A5FA; /* Borda azul mais escura no hover */
        }
        
        /* Estilo para o separador - Gradiente verde-azul */
        .divider {
            height: 4px;
            background: linear-gradient(to right, #34D399, #0EA5E9);
            margin: 3rem 0;
            border-radius: 2px;
        }

        /* Animação para o título */
        @keyframes fadeInScale {
            from { opacity: 0; transform: scale(0.9); }
            to { opacity: 1; transform: scale(1); }
        }
        .animate-fade-in-scale {
            animation: fadeInScale 0.8s ease-out forwards;
        }

        /* Estilo para o botão de atualização - Gradiente verde-azul mais formal */
        #updateDataBtn {
            background: linear-gradient(to right, #059669, #0EA5E9);
            box-shadow: 0 4px 6px rgba(5, 150, 105, 0.4);
        }
        #updateDataBtn:hover {
            background: linear-gradient(to right, #047857, #0284C7);
            transform: translateY(-2px);
            box-shadow: 0 6px 8px rgba(5, 150, 105, 0.5);
        }

        /* Estilo para o conteúdo 'prose' para alinhamento justificado */
        .prose p {
            text-align: justify; /* Justifica o texto dos parágrafos */
            margin-bottom: 1em; /* Espaço entre parágrafos */
        }
        .prose h3 {
            text-align: left; /* Títulos internos alinhados à esquerda para leitura de texto longo */
        }

        /* Estilo para os cards de testemunho */
        .testimonial-card {
            background-color: #F0FDF4; /* Verde muito claro */
            border: 1px solid #A7F3D0; /* Borda verde suave */
            border-radius: 12px;
            padding: 1.5rem;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.08);
            transition: transform 0.2s ease-in-out;
        }
        .testimonial-card:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.12);
        }
        .testimonial-card p {
            font-style: italic;
            color: #4B5563; /* Cinza mais escuro para o texto */
            margin-bottom: 1rem;
        }
        .testimonial-card .author {
            font-weight: bold;
            color: #10B981; /* Verde do tema */
            text-align: right;
            display: block;
        }

        /* Estilo para as imagens da galeria */
        .gallery-image {
            width: 100%;
            height: 200px; /* Altura fixa para as miniaturas */
            object-fit: cover; /* Garante que a imagem preencha o espaço sem distorcer */
            border-radius: 8px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
            transition: transform 0.2s ease-in-out;
        }
        .gallery-image:hover {
            transform: scale(1.05); /* Efeito de zoom no hover */
        }
    </style>
</head>
<body class="text-gray-800 min-h-screen p-4 sm:p-8">

    <!-- Cabeçalho Principal do Site com Quadro e Centralização -->
    <header class="max-w-4xl mx-auto mb-16 bg-white p-8 rounded-3xl shadow-2xl border-4 border-green-300 animate-fade-in-scale">
        <div class="text-center">
            <h1 class="text-5xl sm:text-6xl font-extrabold text-emerald-700 mb-4 tracking-tight leading-tight">
                EcoCalculadora: Balanço de Impacto Ambiental
            </h1>
            <p class="text-xl sm:text-2xl text-gray-700 max-w-3xl mx-auto mt-4 font-semibold">
                Plataforma de visualização de dados e conscientização sobre a sustentabilidade do papel.
            </p>
        </div>
    </header>

    <!-- Seção de Dados Coletados com Quadro e Centralização -->
    <section class="max-w-5xl mx-auto mb-16 bg-white p-8 rounded-3xl shadow-2xl border-4 border-blue-200">
        <div class="text-center">
            <h2 class="text-4xl sm:text-5xl font-bold text-gray-800 mb-10 leading-tight">
                Métricas de Impacto e Resultados do Projeto
            </h2>
        </div>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">

            <!-- Card: Papel Coletado -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-recycle" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 15h2v-6h-2v6zm0-8h2V7h-2v2z"/>
                        <path d="M16 11H8V9h8c1.1 0 2 .9 2 2v2c0 1.1-.9 2-2 2h-4c-.55 0-1-.45-1-1s.45-1 1-1h4c.55 0 1-.45 1-1V9z"/>
                    </svg>
                    Papel Coletado
                </h3>
                <p id="totalColetado" class="text-5xl font-extrabold text-blue-700">0.00 kg</p>
                <p class="text-base text-gray-600 mt-3">Peso total de papel reciclado.</p>
            </div>

            <!-- Card: Árvores Poupadas -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-tree" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M10 18h4v-2h-4v2zM5 22h14v-2H5v2zM12 2L4 15h5v5h6v-5h5L12 2z"/>
                    </svg>
                    Árvores Poupadas
                </h3>
                <p id="arvoresSalvas" class="text-5xl font-extrabold text-green-700">0</p>
                <p class="text-base text-gray-600 mt-3">Estimativa de árvores poupadas.</p>
            </div>

            <!-- Card: Água (Produção Virgem) -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-water" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm-1-14h2v6h-2v6zm0-8h2v2h-2v-2z"/>
                        <path d="M12 20c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm0-18c-5.52 0-10 4.48-10 10s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 14h2v2h-2v-2zm0-8h2v6h-2v-6z"/>
                    </svg>
                    Água (Produção Virgem)
                </h3>
                <p id="aguaProducaoVirgem" class="text-5xl font-extrabold text-red-700">0.00 L</p>
                <p class="text-base text-gray-600 mt-3">Litros de água necessários para produzir o papel de forma virgem.</p>
            </div>

            <!-- Card: Água (Reciclagem) -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-water" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm-1-14h2v6h-2v6zm0-8h2v2h-2v-2z"/>
                        <path d="M12 20c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm0-18c-5.52 0-10 4.48-10 10s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 14h2v2h-2v-2zm0-8h2v6h-2v-6z"/>
                    </svg>
                    Água (Reciclagem)
                </h3>
                <p id="aguaReciclagem" class="text-5xl font-extrabold text-blue-500">0.00 L</p>
                <p class="text-base text-gray-600 mt-3">Litros de água utilizados no processo de reciclagem.</p>
            </div>

            <!-- NOVO CARD: Árvores Utilizadas (Produção) -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-tree-used" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2L4 15h5v5h6v-5h5L12 2zM10 18h4v-2h-4v2zM5 22h14v-2H5v2z"/>
                    </svg>
                    Árvores Utilizadas (Produção)
                </h3>
                <p id="arvoresUtilizadasProducao" class="text-5xl font-extrabold text-orange-600">0</p>
                <p class="text-base text-gray-600 mt-3">Quantas árvores seriam usadas para fazer todo esse papel do zero.</p>
            </div>

            <!-- NOVO CARD ADICIONADO: Água Economizada (Net) -->
            <div class="data-card">
                <h3 class="text-2xl font-bold text-gray-800 flex items-center mb-4">
                    <svg class="icon icon-water" viewBox="0 0 24 24" fill="currentColor" xmlns="http://www.w3.org/2000/svg">
                        <path d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm0 18c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm-1-14h2v6h-2v6zm0-8h2v2h-2v-2z"/>
                        <path d="M12 20c-4.41 0-8-3.59-8-8s3.59-8 8-8 8 3.59 8 8-3.59 8-8 8zm0-18c-5.52 0-10 4.48-10 10s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm-1 14h2v2h-2v-2zm0-8h2v6h-2v-6z"/>
                    </svg>
                    Água Economizada (Net)
                </h3>
                <p id="aguaEconomizada" class="text-5xl font-extrabold text-emerald-600">0.00 L</p>
                <p class="text-base text-gray-600 mt-3">Litros de água poupados ao reciclar, em vez de produzir papel virgem.</p>
            </div>

        </div>

        <!-- Seção de Atualização Manual de Dados -->
        <div class="data-card mt-12 bg-white">
            <h3 class="text-2xl font-bold text-gray-800 mb-6 text-center">Atualize os Nossos Dados! ✨</h3>
            <p class="text-gray-600 mb-6 text-center text-base">
                Coloque aqui os valores mais recentes do seu aplicativo para vermos o progresso juntos!
            </p>
            <div class="grid grid-cols-1 sm:grid-cols-2 gap-6 mb-6">
                <div>
                    <label for="inputTotalColetado" class="block text-base font-medium text-gray-700 mb-1">Papel Coletado (kg):</label>
                    <input type="number" id="inputTotalColetado" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 10.5">
                </div>
                <div>
                    <label for="inputArvoresSalvas" class="block text-base font-medium text-gray-700 mb-1">Árvores Poupadas:</label>
                    <input type="number" id="inputArvoresSalvas" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 5">
                </div>
                <div>
                    <label for="inputAguaEconomizada" class="block text-base font-medium text-gray-700 mb-1">Água Economizada (L):</label>
                    <input type="number" id="inputAguaEconomizada" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 500">
                </div>
                <div>
                    <label for="inputAguaProducaoVirgem" class="block text-base font-medium text-gray-700 mb-1">Água Produção Virgem (L):</label>
                    <input type="number" id="inputAguaProducaoVirgem" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 5400">
                </div>
                <div>
                    <label for="inputAguaReciclagem" class="block text-base font-medium text-gray-700 mb-1">Água Reciclagem (L):</label>
                    <input type="number" id="inputAguaReciclagem" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 25">
                </div>
                <!-- NOVO INPUT: Árvores Utilizadas (Produção) - ID CORRIGIDO -->
                <div>
                    <label for="inputArvoresUtilizadasProducao" class="block text-base font-medium text-gray-700 mb-1">Árvores Utilizadas (Produção):</label>
                    <input type="number" id="inputArvoresUtilizadasProducao" class="mt-1 block w-full rounded-lg border-gray-300 shadow-sm focus:border-purple-500 focus:ring-purple-500 p-3 text-lg" placeholder="Ex: 10">
                </div>
            </div>
            <button id="updateDataBtn" class="w-full bg-gradient-to-r from-purple-500 to-blue-500 hover:from-purple-600 hover:to-blue-600 text-white font-bold py-3 px-6 rounded-lg shadow-lg transition-all duration-300 ease-in-out text-xl">
                🚀 Ver o Nosso Impacto Atualizado!
            </button>
        </div>
    </section>

    <div class="divider"></div>

    <!-- Nova Seção: Nosso App EcoCalculadora -->
    <section class="max-w-4xl mx-auto mb-16 bg-gradient-to-r from-green-50 to-teal-50 p-8 rounded-3xl shadow-2xl border-l-4 border-green-500">
        <h2 class="text-4xl sm:text-5xl font-bold text-green-800 mb-8 text-center">
            📱 Nosso App: EcoCalculadora! 🌳💧
        </h2>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-8 items-center">
            <div class="prose max-w-none text-gray-700 text-lg leading-relaxed">
                <p class="mb-4">Para tornar nosso projeto ainda mais **incrível e divertido**, criamos o app **EcoCalculadora**! Ele é a nossa ferramenta secreta para acompanhar todo o papel que reciclamos na escola e ver, na hora, o impacto positivo que estamos a gerar.</p>
                <p class="mb-4">Com o EcoCalculadora, cada vez que o papel é pesado e registado, o app automaticamente calcula:</p>
                <ul class="list-disc list-inside space-y-2 text-gray-700">
                    <li>O **total de papel** que já coletámos.</li>
                    <li>Quantas **árvores** foram poupadas.</li>
                    <li>Quantos **litros de água** foram economizados (sim, é muita água!).</li>
                    <li>A água usada na produção de papel novo (virgem) e na reciclagem.</li>
                    <li>**Quantas árvores foram "gastas"** para produzir o papel que estamos a reciclar.</li>
                </ul>
                <p class="mt-4 font-semibold text-gray-800">É super fácil de usar e nos mostra em tempo real como pequenas ações fazem uma GRANDE diferença para o planeta!</p>
            </div>
            <div class="flex justify-center items-center p-4">
                <!-- IMAGEM DO APLICATIVO ECOCALCULADORA -->
                <img src="https://i.imgur.com/zhjt8Di.jpeg" alt="Screenshot do Aplicativo EcoCalculadora" class="rounded-2xl shadow-xl border-4 border-green-300 transform hover:scale-105 transition-transform duration-300">
            </div>
        </div>
        <div class="text-center mt-10">
            <a href="#" class="inline-block bg-green-600 hover:bg-green-700 text-white font-bold py-3 px-8 rounded-full shadow-lg transition-colors duration-300 text-lg">
                Baixe o App (Em Breve!)
            </a>
        </div>
    </section>

    <div class="divider"></div>

    <!-- NOVA SEÇÃO: Galeria de Fotos / Mural do Projeto -->
    <section class="max-w-5xl mx-auto mb-16 bg-white p-8 rounded-3xl shadow-2xl border-4 border-lime-300">
        <h2 class="text-4xl sm:text-5xl font-bold text-gray-800 mb-10 text-center">
            📸 Mural do Nosso Impacto Visual!
        </h2>
        <p class="text-lg text-gray-700 text-center max-w-2xl mx-auto mb-12">
            Veja como a nossa comunidade escolar está a transformar a reciclagem em ação! Cada foto é um passo verde.
        </p>
        
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6">
            <!-- Imagem 1: Alunas organizando caixas para coleta de papel -->
            <div>
                <img src="https://i.imgur.com/F7vKlnj.jpeg" alt="Alunas organizando caixas para coleta de papel" class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Alunas organizando as caixas de coleta de papel!</p>
            </div>
            <!-- Imagem 2 (Campo Reservado: Criando o App) -->
            <div>
                <!-- ATENÇÃO: COLOQUE A URL PÚBLICA DIRETA DA SUA FOTO REAL PARA 'CRIANDO O APP' AQUI! -->
                <!-- EX: <img src="https://seusite.com/caminho/para/foto_02_criando_app.jpg" alt="Alunos trabalhando na criação do aplicativo EcoCalculadora" class="gallery-image"> -->
                <img src="https://placehold.co/600x400/D1FAE5/22C55E?text=COLOQUE_URL_DIRETA_DA_FOTO_2" alt="Alunos trabalhando na criação do aplicativo EcoCalculadora" class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Desenvolvendo nosso aplicativo EcoCalculadora!</p>
            </div>
            <!-- Imagem 3: Alunas montando caixas de coleta de papel -->
            <div>
                <img src="https://i.imgur.com/m999z9A.jpeg" alt="Alunas montando caixas de coleta de papel" class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Alunas montando as caixas de coleta!</p>
            </div>
            <!-- Imagem 4: Alunas registrando o peso do papel no aplicativo EcoCalculadora. -->
            <div>
                <img src="https://i.imgur.com/4VdKvUK.jpeg" alt="Alunas registrando o peso do papel no aplicativo EcoCalculadora." class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Registrando o peso do papel no app!</p>
            </div>
            <!-- Imagem 5: Alunos em sala de aula assistindo a uma apresentação sobre conscientização. -->
            <div>
                <img src="https://i.imgur.com/KxxHKYO.jpeg" alt="Alunos em sala de aula assistindo a uma apresentação sobre conscientização." class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Momento de conscientização em sala de aula.</p>
            </div>
            <!-- Imagem 6 (Campo Reservado: Alunos Depositando Papel) -->
            <div>
                <!-- ATENÇÃO: COLOQUE A URL PÚBLICA DIRETA DA SUA FOTO REAL PARA 'ALUNOS DEPOSITANDO PAPEL' AQUI! -->
                <!-- EX: <img src="https://seusite.com/caminho/para/foto_06_depositando_papel.jpg" alt="Alunos depositando papel nas caixas de coleta." class="gallery-image"> -->
                <img src="https://placehold.co/600x400/BFEEB7/076C5F?text=COLOQUE_URL_DIRETA_DA_FOTO_6" alt="Alunos depositando papel nas caixas de coleta." class="gallery-image">
                <p class="text-sm text-gray-600 mt-2 text-center">Alunos depositando papel para reciclagem!</p>
            </div>
        </div>
        <div class="text-center mt-10">
            <a href="#" class="inline-block bg-teal-600 hover:bg-teal-700 text-white font-bold py-3 px-8 rounded-full shadow-lg transition-colors duration-300 text-lg">
                Ver Mais Fotos
            </a>
        </div>
    </section>

    <div class="divider"></div>

    <!-- NOVA SEÇÃO: Testemunhos ou Depoimentos -->
    <section class="max-w-4xl mx-auto mb-16 bg-white p-8 rounded-3xl shadow-2xl border-4 border-emerald-300">
        <h2 class="text-4xl sm:text-5xl font-bold text-gray-800 mb-10 text-center">
            💬 Nossas Vozes: Quem Faz a Diferença
        </h2>
        <p class="text-lg text-gray-700 text-center max-w-2xl mx-auto mb-12">
            Veja o que alunos, professores e pais estão a dizer sobre o nosso projeto de reciclagem.
        </p>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
            <!-- Testemunho 1 -->
            <div class="testimonial-card">
                <p>"Adoro usar o EcoCalculadora! É muito legal ver as árvores e a água que a gente salva. Me sinto um herói do planeta!"</p>
                <span class="author">— João, Aluno do 5º Ano</span>
            </div>
            <!-- Testemunho 2 -->
            <div class="testimonial-card">
                <p>"O projeto trouxe uma consciência ambiental incrível para a escola. Os alunos estão superengajados e o site é uma vitrine perfeita para o nosso trabalho."</p>
                <span class="author">— Professora Ana, Coordenadora</span>
            </div>
            <!-- Testemunho 3 -->
            <div class="testimonial-card">
                <p>"É inspirador ver como as crianças estão aprendendo a valorizar a reciclagem. O app e o site são ferramentas fantásticas para isso. Parabéns à equipe!"</p>
                <span class="author">— Maria, Mãe de Aluno</span>
            </div>
            <!-- Testemunho 4 -->
            <div class="testimonial-card">
                <p>"Nunca imaginei que reciclar pudesse ter um impacto tão grande na economia de água. Esse projeto abriu meus olhos para a sustentabilidade!"</p>
                <span class="author">— Pedro, Aluno do 8º Ano</span>
            </div>
        </div>
    </section>

    <div class="divider"></div>

    <!-- Seção de Informações do Projeto com Quadro e Centralização -->
    <section class="max-w-4xl mx-auto mb-16 bg-white p-8 rounded-3xl shadow-2xl border-4 border-green-400">
        <h2 class="text-4xl sm:text-5xl font-bold text-gray-800 mb-8 text-center">
            🌍 Sobre o Nosso Projeto: Conscientização e Ação 🌳
        </h2>
        <div class="prose max-w-none text-gray-700 text-lg leading-relaxed">
            <h3 class="text-3xl font-bold mb-4 text-gray-800">1. O Impacto Secreto do Papel 🧐</h3>
            <p>Sabia que o papel que usamos todos os dias tem uma história grandona? Para fazê-lo, muitas árvores são cortadas, e isso mexe com a vida de animais e plantas. Além disso, as fábricas de papel usam MUITA água e energia, e se não cuidarem bem, podem poluir o nosso ar e a nossa água. Por exemplo, para fazer <strong>só 1 quilo de papel novinho</strong> (que não é reciclado), gastamos cerca de <strong>540 litros de água</strong>! É como encher um monte de garrafas de refrigerante! 🤯</p>
            <p>Nosso projeto te ajuda a ver de perto essa jornada e o que podemos fazer de diferente!</p>

            <h3 class="text-3xl font-bold mt-10 mb-4 text-gray-800">2. A Magia da Reciclagem: Menos Água, Mais Vida! ✨</h3>
            <p>Mas calma, tem uma solução superpoderosa: a **reciclagem**! Quando reciclamos papel, evitamos que mais árvores sejam cortadas. E o mais legal? Usamos muuuito menos água! Para fazer <strong>1 quilo de papel reciclado</strong>, precisamos de apenas <strong>2 a 2.5 litros de água</strong>. Isso é uma diferença enorme!</p>
            <p>Significa que, a cada quilo de papel que jogamos no lugar certo para reciclagem, estamos salvando uns **537.5 litros de água**! 💧💦 Nosso projeto é tipo um jogo: quanto mais papel coletamos com o app <strong>EcoCalculadora</strong>, mais litros de água e mais árvores salvamos! O aplicativo que criamos na escola nos ajuda a contar tudo isso.</p>

            <h3 class="text-3xl font-bold mt-10 mb-4 text-gray-800">3. Justiça Climática: Um Mundo Mais Justo e Verde para Todos! ⚖️🌳</h3>
            <p>O desmatamento não é justo! Ele afeta mais quem vive perto das florestas, como comunidades indígenas e pessoas que dependem da natureza para viver. Cortar árvores pode tirar a casa de muitas famílias e deixar o clima do planeta desequilibrado. A **Justiça Climática** é sobre isso: lutar para que todos, em todo lugar, tenham um ambiente saudável para viver.</p>
            <p>Quando reciclamos papel, não estamos só ajudando o meio ambiente, mas também as pessoas que sofrem mais com os problemas da natureza. É uma forma de construirmos um mundo mais **justo e sustentável** para nós e para as futuras gerações. Sua participação conta muito!</p>
        </div>
    </section>

    <!-- Rodapé -->
    <footer class="text-center mt-16 py-8 text-gray-600 text-sm">
        <p>&copy; 2025 Projeto Sustentabilidade Escolar. Feito com amor pela natureza. 🌱</p>
    </footer>

    <!-- Script JavaScript para atualizar os dados manualmente -->
    <script>
        document.getElementById('updateDataBtn').addEventListener('click', function() {
            // Obter os valores dos campos de input
            const totalColetado = parseFloat(document.getElementById('inputTotalColetado').value) || 0;
            const arvoresSalvas = parseInt(document.getElementById('inputArvoresSalvas').value) || 0;
            const aguaEconomizada = parseFloat(document.getElementById('inputAguaEconomizada').value) || 0;
            const aguaProducaoVirgem = parseFloat(document.getElementById('inputAguaProducaoVirgem').value) || 0;
            const aguaReciclagem = parseFloat(document.getElementById('inputAguaReciclagem').value) || 0;
            const arvoresUtilizadasProducao = parseInt(document.getElementById('inputArvoresUtilizadasProducao').value) || 0;

            // Criar um objeto com os dados
            const newData = {
                totalColetado,
                arvoresSalvas,
                aguaEconomizada,
                aguaProducaoVirgem,
                aguaReciclagem,
                arvoresUtilizadasProducao
            };

            // Salvar os dados no localStorage
            localStorage.setItem('projetoSustentabilidadeData', JSON.stringify(newData));

            // Atualizar os elementos na página
            document.getElementById('totalColetado').textContent = `${totalColetado.toFixed(2)} kg`;
            document.getElementById('arvoresSalvas').textContent = `${arvoresSalvas}`;
            document.getElementById('aguaEconomizada').textContent = `${aguaEconomizada.toFixed(2)} L`;
            document.getElementById('aguaProducaoVirgem').textContent = `${aguaProducaoVirgem.toFixed(2)} L`;
            document.getElementById('aguaReciclagem').textContent = `${aguaReciclagem.toFixed(2)} L`;
            document.getElementById('arvoresUtilizadasProducao').textContent = `${arvoresUtilizadasProducao}`;

            alert('Dados atualizados e salvos no seu navegador!');
        });

        // Script para carregar dados salvos no localStorage (se houver, para persistência no navegador)
        document.addEventListener('DOMContentLoaded', function() {
            const savedData = JSON.parse(localStorage.getItem('projetoSustentabilidadeData'));
            if (savedData) {
                document.getElementById('totalColetado').textContent = `${savedData.totalColetado.toFixed(2)} kg`;
                document.getElementById('arvoresSalvas').textContent = `${savedData.arvoresSalvas}`;
                document.getElementById('aguaEconomizada').textContent = `${savedData.aguaEconomizada.toFixed(2)} L`;
                document.getElementById('aguaProducaoVirgem').textContent = `${savedData.aguaProducaoVirgem.toFixed(2)} L`;
                document.getElementById('aguaReciclagem').textContent = `${savedData.aguaReciclagem.toFixed(2)} L`;
                document.getElementById('arvoresUtilizadasProducao').textContent = `${savedData.arvoresUtilizadasProducao}`;

                // Preencher campos de input com os dados salvos para facilitar a edição
                document.getElementById('inputTotalColetado').value = savedData.totalColetado;
                document.getElementById('inputArvoresSalvas').value = savedData.arvoresSalvas;
                document.getElementById('inputAguaEconomizada').value = savedData.aguaEconomizada;
                document.getElementById('inputAguaProducaoVirgem').value = savedData.aguaProducaoVirgem;
                document.getElementById('inputAguaReciclagem').value = savedData.aguaReciclagem;
                document.getElementById('inputArvoresUtilizadasProducao').value = savedData.arvoresUtilizadasProducao;
            }
        });
    </script>
</body>
</html>
