<script>
    import Project from "./components/Project.svelte"
    import Skill from "./components/Skill.svelte"
</script>

<div class="bg-base-200 min-h-screen">
    <!-- AI disclaimer -->
    <div class="tooltip tooltip-left fixed top-4 right-4 z-20" data-tip="Tato stránka nebyla vytvořená umělou inteligencí (s výjimkou VS Code autocompletes)">
        <!-- From svgrepo.com -->
        <svg class="h-13 w-13" fill="#Fff" version="1.1" id="Capa_1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" width="800px" height="800px" viewBox="0 0 45.999 45.999" xml:space="preserve"> <g> <g> <path d="M39.264,6.736c-8.982-8.981-23.545-8.982-32.528,0c-8.982,8.982-8.981,23.545,0,32.528c8.982,8.98,23.545,8.981,32.528,0 C48.245,30.281,48.244,15.719,39.264,6.736z M25.999,33c0,1.657-1.343,3-3,3s-3-1.343-3-3V21c0-1.657,1.343-3,3-3s3,1.343,3,3V33z M22.946,15.872c-1.728,0-2.88-1.224-2.844-2.735c-0.036-1.584,1.116-2.771,2.879-2.771c1.764,0,2.88,1.188,2.917,2.771 C25.897,14.648,24.746,15.872,22.946,15.872z"/> </g> </g> </svg>
    </div>
    
    <!-- Title -->
    <!-- bg-[url(./assets/bg_mountains.png)] -->
    <div class="p-40 bg-linear-to-t from-base-100 via-60% via-base-200 to-base-300 sticky top-0">
        <h1 class="text-8xl font-extrabold text-center">Daniel Devečka - Portfolio</h1>
    </div>

    <!-- Navbar -->
    <div class="navbar justify-evenly sticky top-0 p-0 m-0 bg-base-100 z-10">
        <a href="#about" class="flex-none text-4xl font-bold p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">O mně</a>
        <a href="#projects" class="flex-none text-4xl font-bold p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">Projekty</a>
        <a href="#skills" class="flex-none text-4xl font-bold p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">Dovednosti</a>
    </div>

    <!-- Content -->
    <div class="bg-base-200 relative top-0 text-xl">
        <!-- Projects -->
        <div>
            <div id="projects" class="relative -top-30"></div> <!-- Anchor -->

            <div class="p-15 bg-base-300">
                <h2 class="text-6xl font-semibold">Projekty</h2>
                <p class="text-3xl mt-7">
                    Zde jsou některé z mých projekyů, na kterých jsem pracoval, nebo stále pracuji.
                </p>
            </div>

            <Project
                name="xo"
                description='Online hra piškvorky s neomezeným polem a možností vytvoření účtu. Napsaná v jazyce JavaScript s frameworky SvelteKit, Tailwind a DaisyUI na straně klienta a Node.js, Socket.io a Express na straně serveru.
                        Běhá buď na Raspberry Pi v mém pokoji, nebo na Dropletu v <a class="underline text-accent" href="https:/digitalocean.com" target="_blank">DigitalOcean</a>. <br>
                        Základní kostra HTML byla vygenerována pomocí AI, vzhled stránce však dává DaisyUI. <br>
                        Jde hrát proti náhodému soupeři, nebo proti přátelům pomocí unikátního odkazu. <br>
                        Hra běží na adrese: <a class="underline text-primary" href="https://xo.dandev.dev" target="_blank">xo.dandev.dev</a> <br>
                        Zdrojový kód pro server je dostupný na GitHubu: <a class="underline text-primary" href="https://github.com/danielde8/xo-server" target="_blank">danielde8/xo-server</a>,
                        pro klienta na: <a class="underline text-primary" href="https://github.com/danielde8/xo-frontend" target="_blank">danielde8/xo-frontend</a>'
                imgSrc="assets/projects/xo.png"
                imgWidth=160
                evenProject={ false }
            />

            <Project
                name="SnakeOS"
                description='Vlastní "operační systém" napsaný v jazycích C a Assembly pro architekturu i386, na kterém běží pouze hra Snake.
                        Dá se spustit na emulátoru QEMU, na skutečném hardwaru se mi ho rozchodit zatím nepodařilo.
                        Byl inspirován projektem <a class="underline text-accent" href="https://www.youtube.com/watch?v=FaILnmUYS_U" target="_blank">TetrisOS od jdh</a>. <br>
                        Zdrojový kód je dostupný na GitHubu: <a class="underline text-primary" href="https://github.com/danielde8/snakeos" target="_blank">danielde8/snakeos</a>'
                imgSrc="assets/projects/snakeos.png"
                imgWidth=140
                evenProject={ true }
            />

            <Project
                name="MUPC"
                description='MUPC (Mostly Useless Programmable Calculator) je vlastní 8-bitové CPU (zatím pouze návrh) s vlastním setem instrukcí, assemblerem a emulátorem.
                        Emulátor je napsaný v jazyce C a assembler v Kotlinu. Samotné CPU momentálně designuji v Logisim Evolution. <br>
                        Zdrojové kódy jsou dostupné na GitHubu: <a class="underline text-primary" href="https://github.com/danielde8/mupc" target="_blank">danielde8/mupc</a>,
                        <a class="underline text-primary" href="https://github.com/danielde8/mupc-asm" target="_blank">danielde8/mupc-asm</a> a 
                        <a class="underline text-primary" href="https://github.com/danielde8/mupc-emu" target="_blank">danielde8/mupc-emu</a>'
                imgSrc="assets/projects/mupc.png"
                imgWidth=130
                evenProject={ false }
            />

            <Project
                name="XComps"
                description='Aplikace pro Android napsaná v jazyce JavaScript s frameworky Svelte, Tailwind a DaisyUI, využívající Capacitor pro spuštění na mobilních zařízeních.
                        Využívá web scraping a slouží k rychlému stahování souborů plachtařských soutěží z webů
                        <a class="underline text-accent" href="https://www.soaringspot.com/" target="_blank">SoaringSpot</a> a
                        <a class="underline text-accent" href="https://www.soarscore.com/" target="_blank">SoarScore</a>
                        do složky programu XCSoar. <br>
                        Zdrojový kód je dostupný na GitHubu: <a class="underline text-primary" href="https://github.com/danielde8/xcomps" target="_blank">danielde8/xcomps</a>'
                imgSrc="assets/projects/xcomps.png"
                imgWidth=60
                evenProject={ true }
            />
        </div>

        <!-- Skills -->
        <div>
            <div id="skills" class="relative -top-30"></div> <!-- Anchor -->

            <div class="p-15 bg-base-300">
                <h2 class="text-6xl font-semibold">Dovednosti</h2>

                <Skill
                    name="JavaScript (Frontend)"
                    description='JavaScriptu se věnuji od 3. třídy. Začínal jsem s jednoduchým kreslením v aplikaci <a class="underline text-accent" href="https://p5js.org/" target="_blank">p5.js</a>,
                        později jsem zkoušel i tvorbu webových stránek a her. Před nedávnem jsem objevil framework <a class="underline text-accent" href="https://svelte.dev/" target="_blank">Svelte</a>,
                        který mě velmi zaujal, hlavně svou jednoduchostí (doufám že jednoho dne přeroste React :D). Dnes hlavně používám Svelte spolu s Tailwind CSS a DaisyUI, ve kterých byla napsána i tato stránka.' 
                />

                <Skill
                    name="Node.js"
                    description='Node.js používám pro tvorbu backendů/API pro své webové aplikace. Pro API nebo statické stránky používám framework <a class="underline text-accent" href="https://expressjs.com" target="_blank">Express.js</a>
                    hlavně kvůli jeho jednoduchosti a komunitě. Pro real-time komunikaci (např. ve hrách) používám <a class="underline text-accent" href="https://socket.io/" target="_blank">Socket.io</a>.
                    Node.js mám velmi rád, protože mi umožňuje psát frontend i backend ve stejném jazyce. Naučil jsem se na něm mimo jiné i základy HTTP requestů.'
                />

                <Skill
                    name="Kotlin"
                    description='Ve 4. třídě jsem se začal učit programovat v jazyce Kotlin, ne však pro Android, ale pro tvorbu her a desktopových aplikací
                    pomocí <a class="underline text-accent" href="https://korge.org" target="_blank">KorGE</a> a Java Swing.
                    Kotlin je dnes můj nejoblíbenější jazyk, hlavně pro jeho všechny možné vestavěné funkce a možnost využít Java knihovny.
                    V Kotlinu většinou píšu menší projekty, které bývají spíše experimenty než hotové aplikace.'
                />

                <Skill
                    name="C a Assembly"
                    description='Sice o sobě nemohu říct, že jsem v těchto jazycích expert, ale něco v nich napsat dokážu.
                    Už dlouho byl můj sen vytvořit vlastní operační systém, který by se dal spustit alespoň na VM, i kdyby to mělo být jen <span class="italic">Hello World</span>.
                    To se mi konečně podařilo někdy v 6. třídě, kdy jsem (pomocí AI :D) napsal jednoduchý Assembly kód, který vypsal jedno písmeno a dal se spustit ve <a class="underline text-accent" href="https://www.virtualbox.org/" target="_blank">VirtualBoxu</a>.
                    Po snad ještě delší době se mi <span class="italic">konečně</span> podařilo načíst C program a zanedlouho nato jsem začal pracovat na svém vlastním "OS", který je popsán výše.<br>
                    C mimo to používám i pro psaní programů, kde potřebuji často pracovat s čísly na nižší úrovni, například pro emulátor CPU. (MUPC - viz výše)'
                />

                <Skill
                    name="Linux a servery"
                    description='Už ani nevím, kdy jsem začal používat Linux, ale je to už celkem dávno.
                    Většinou používám distribuci Ubuntu Server nebo Kali Linux. Na svém hlavním počítači mám sice macOS, ale mám i dva staré notebooky, které jsem přeinstaloval z Windows 7 na Linux.
                    První jsem používal jako Minecraft server pro kamarády, na druhém běží Kali, používám ho tedy na učení se KB, hlavně na <a class="underline text-accent" href="https://www.hackthebox.com/" target="_blank">Hack The Box</a>.'
                />
            </div>
        </div>
    </div>
</div>