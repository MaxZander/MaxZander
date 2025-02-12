<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;200;300;400;500;700;900&display=swap');

body {
    background: #151515;
    color: white;
    font-family: 'Roboto', sans-serif;
    margin: 0;
}

@keyframes glitch {
  0% {
    clip-path: polygon(0 2%, 100% 2%, 100% 5%, 0 5%);
    transform: translate(0);
  }
  2% {
    clip-path: polygon(0 15%, 100% 15%, 100% 15%, 0 15%);
    transform: translate(-2px);
  }
  4% {
    clip-path: polygon(0 10%, 100% 10%, 100% 20%, 0 20%);
    transform: translate(2px);
  }
  6% {
    clip-path: polygon(0 1%, 100% 1%, 100% 2%, 0 2%);
    transform: translate(0);
  }
  8% {
    clip-path: polygon(0 33%, 100% 33%, 100% 33%, 0 33%);
    transform: translate(-1px);
  }
  10% {
    clip-path: polygon(0 44%, 100% 44%, 100% 44%, 0 44%);
    transform: translate(0);
  }
  12% {
    clip-path: polygon(0 50%, 100% 50%, 100% 20%, 0 20%);
    transform: translate(-2px);
  }
  14% {
    clip-path: polygon(0 70%, 100% 70%, 100% 70%, 0 70%);
    transform: translate(2px);
  }
  16% {
    clip-path: polygon(0 80%, 100% 80%, 100% 80%, 0 80%);
    transform: translate(-1px);
  }
  18% {
    clip-path: polygon(0 50%, 100% 50%, 100% 55%, 0 55%);
    transform: translate(0);
  }
  20% {
    clip-path: polygon(0 70%, 100% 70%, 100% 80%, 0 80%);
    transform: translate(2px);
  }
}

@keyframes fadeInUp {
  0% {
    opacity: 0;
    transform: translateY(20px);
  }
  100% {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(-20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

@keyframes fadeInRight {
  0% {
    opacity: 0;
    transform: translateX(20px);
  }
  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeInUp {
  animation: fadeInUp 1s ease-out forwards;
}

.fadeInLeft {
  animation: fadeInLeft 1s ease-out forwards;
}

.fadeInRight {
  animation: fadeInRight 1s ease-out forwards;
}

.delay-1 {
  opacity: 0;
  animation-delay: 400ms
}

.delay-2 {
  opacity: 0;
  animation-delay: 800ms
}

.delay-3 {
  opacity: 0;
  animation-delay: 1200ms
}

.delay-4 {
  opacity: 0;
  animation-delay: 1600ms
}

.glitch {
  position: relative;
  animation: glitch 2s infinite;
}

.glitch::before,
.glitch::after {
  content: attr(data-text);
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}

.glitch::before {
  left: 2px;
  text-shadow: -2px 0 #ff00c1;
  clip: rect(44px, 450px, 56px, 0);
  animation: glitch 5s infinite linear alternate-reverse;
}

.glitch::after {
  left: -2px;
  text-shadow: -2px 0 #00fff9, 2px 2px #ff00c1;
  animation: glitch 1s infinite linear alternate-reverse;
}

.glitch-text-container {
  text-shadow: 0 0 5px #00fff9, 0 0 10px #00fff9, 0 0 20px #00fff9;
}

.glitch-1 {
  animation: glitch 4s infinite;
  transform: translateX(-2px);
}

.glitch-2 {
  animation: glitch 4s infinite reverse;
  transform: translateX(2px);
}

.w-100 {
  width: 100%;
}

.text-cyber-blue {
  color: #00fff9;
  font-size: 30px;
  font-weight: 300;
}

/* Définir les couleurs personnalisées */
        :root {
            --cyber-blue: #00b5e2;
            --cyber-pink: #ff007f;
        }

        /* Styles généraux pour la carte */
        .card {
            position: relative;
            background: linear-gradient(to bottom right, black, #2a2a2a);
            border-radius: 0.75rem;
            padding: 1.5rem;
            border: 1px solid rgba(0, 181, 226, 0.2);
            overflow: hidden;
            transition: all 0.3s ease;
        }

        /* Effet de survol de la carte */
        .card:hover {
            border-color: var(--cyber-blue);
        }

        /* Couche de fond en dégradé avec effet hover */
        .card:hover .overlay {
            opacity: 1;
        }

        .overlay {
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: linear-gradient(to right, rgba(0, 181, 226, 0.1), rgba(255, 0, 127, 0.1));
            opacity: 0;
            transition: opacity 0.3s ease;
        }

        /* Icone */
        .card svg {
            width: 2rem;
            height: 2rem;
            stroke: #00b5e2;
            margin-bottom: 1rem;
        }

        /* Titre */
        .card h3 {
            font-size: 1.25rem;
            font-weight: 600;
            color: white;
            margin-bottom: 0.5rem;
        }

        /* Description */
        .card p {
            font-size: 1rem;
            color: #b0b0b0;
        }

        /* Container principal */
        .card-container {
            display: grid;
            grid-template-columns: repeat(1, 1fr); /* Par défaut 1 colonne */
            gap: 2rem; /* Espacement entre les éléments */
        }

        /* Responsivité pour les écrans plus grands */
        @media (min-width: 768px) {
            .card-container {
                grid-template-columns: repeat(2, 1fr); /* 2 colonnes pour les écrans moyens (md) */
            }
        }

        @media (min-width: 1024px) {
            .card-container {
                grid-template-columns: repeat(4, 1fr); /* 4 colonnes pour les grands écrans (lg) */
            }
        }


</style>

<!-- HTML -->

<h1 align="center" class="glitch fadeInUp" data-text="Marvin Bost" style="font-size: 100px;">Marvin Bost</h1>
<h2 align="center" class="text-cyber-blue fadeInUp delay-1">Développeur Fullstack & Mentor</h2>

<!-- Technologies avec effets fadeInRight -->
<p align="center" class="fadeInRight delay-2">
    <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white" alt="Next.js" />
    <img src="https://img.shields.io/badge/Angular-DD0031?style=for-the-badge&logo=angular&logoColor=white" alt="Angular" />
    <img src="https://img.shields.io/badge/React-61DAFB?style=for-the-badge&logo=react&logoColor=white" alt="React" />
    <img src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white" alt="Tailwind CSS" />
    <img src="https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
    <img src="https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white" alt="Node.js" />
    <img src="https://img.shields.io/badge/ASP.NET-512BD4?style=for-the-badge&logo=.net&logoColor=white" alt="ASP.NET" />
    <img src="https://img.shields.io/badge/Express.js-000000?style=for-the-badge&logo=express&logoColor=white" alt="Express.js" />
    <img src="https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white" alt="MongoDB" />
</p>

<!-- Snake with fadeInUp -->
<p align="center" class="fadeInUp delay-3">
    <img src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg" alt="Snake" />
</p>

<!-- Card with fadeInLeft -->

<div class="card-container">
    <!-- Front-End -->
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-code2 w-8 h-8 text-cyber-blue mb-4">
            <path d="m18 16 4-4-4-4"></path>
            <path d="m6 8-4 4 4 4"></path>
            <path d="m14.5 4-5 16"></path>
        </svg>
        <h3>Développement Frontend</h3>
        <p>React, Angular, TypeScript, Next.js</p>
    </div>
    <!-- Back-End -->
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-database w-8 h-8 text-cyber-blue mb-4"><ellipse cx="12" cy="5" rx="9" ry="3"></ellipse><path d="M3 5V19A9 3 0 0 0 21 19V5"></path><path d="M3 12A9 3 0 0 0 21 12"></path>
        </svg>
        <h3>Développement Backend</h3>
        <p>Node.js, ASP.NET, SQL, API REST</p>
    </div>
    <!-- Mentoring -->
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-users w-8 h-8 text-cyber-blue mb-4"><path d="M16 21v-2a4 4 0 0 0-4-4H6a4 4 0 0 0-4 4v2"></path><circle cx="9" cy="7" r="4"></circle><path d="M22 21v-2a4 4 0 0 0-3-3.87"></path><path d="M16 3.13a4 4 0 0 1 0 7.75"></path></svg>
        <h3>Mentoring</h3>
        <p>Formation, accompagnement, code review</p>
    </div>
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-building2 w-8 h-8 text-cyber-blue mb-4"><path d="M6 22V4a2 2 0 0 1 2-2h8a2 2 0 0 1 2 2v18Z"></path><path d="M6 12H4a2 2 0 0 0-2 2v6a2 2 0 0 0 2 2h2"></path><path d="M18 9h2a2 2 0 0 1 2 2v9a2 2 0 0 1-2 2h-2"></path><path d="M10 6h4"></path><path d="M10 10h4"></path><path d="M10 14h4"></path><path d="M10 18h4"></path></svg>
        <h3>Architecture</h3>
        <p>Clean Architecture, Design Patterns</p>
    </div>
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-panels-top-left w-8 h-8 text-cyber-blue mb-4"><rect width="18" height="18" x="3" y="3" rx="2"></rect><path d="M3 9h18"></path><path d="M9 21V9"></path></svg>
        <h3>UI/UX Design</h3>
        <p>Responsive Design, Animations, Accessibilité</p>
    </div>
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-server w-8 h-8 text-cyber-blue mb-4"><rect width="20" height="8" x="2" y="2" rx="2" ry="2"></rect><rect width="20" height="8" x="2" y="14" rx="2" ry="2"></rect><line x1="6" x2="6.01" y1="6" y2="6"></line><line x1="6" x2="6.01" y1="18" y2="18"></line></svg>
        <h3>Dev Ops</h3>
        <p>CI/CD, DOcker, GitHub Actions</p>
    </div>
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-git-branch w-8 h-8 text-cyber-blue mb-4"><line x1="6" x2="6" y1="3" y2="15"></line><circle cx="18" cy="6" r="3"></circle><circle cx="6" cy="18" r="3"></circle><path d="M18 9a9 9 0 0 1-9 9"></path></svg>
        <h3>Gestion de Projet</h3>
        <p>Agile, Git, Gitflow, Trello</p>
    </div>
    <div class="card">
        <div class="overlay"></div>
        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" class="lucide lucide-brain w-8 h-8 text-cyber-blue mb-4"><path d="M12 5a3 3 0 1 0-5.997.125 4 4 0 0 0-2.526 5.77 4 4 0 0 0 .556 6.588A4 4 0 1 0 12 18Z"></path><path d="M12 5a3 3 0 1 1 5.997.125 4 4 0 0 1 2.526 5.77 4 4 0 0 1-.556 6.588A4 4 0 1 1 12 18Z"></path><path d="M15 13a4.5 4.5 0 0 1-3-4 4.5 4.5 0 0 1-3 4"></path><path d="M17.599 6.5a3 3 0 0 0 .399-1.375"></path><path d="M6.003 5.125A3 3 0 0 0 6.401 6.5"></path><path d="M3.477 10.896a4 4 0 0 1 .585-.396"></path><path d="M19.938 10.5a4 4 0 0 1 .585.396"></path><path d="M6 18a4 4 0 0 1-1.967-.516"></path><path d="M19.967 17.484A4 4 0 0 1 18 18"></path></svg>
        <h3>Soft Skills</h3>
        <p>Curiosité, Autonomie, Communication, Adaptabilité</p>
    </div>
</div>
