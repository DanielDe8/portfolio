<script>
    import Project from "./components/Project.svelte"
    import Skill from "./components/Skill.svelte"
    import Other from "./components/Other.svelte"
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
    <div class="navbar justify-evenly sticky top-0 p-0 m-0 bg-base-100 z-10 text-4xl font-bold">
        <a href="#projects" class="flex-none p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">Projekty</a>
        <a href="#skills" class="flex-none p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">Dovednosti</a>
        <a href="#other" class="flex-none p-10 hover:bg-base-200 transition-all duration-400 ease-in-out">Ostatní</a>
    </div>

    <!-- Content -->
    <div class="bg-base-200 relative top-0">
        <!-- Projects -->
        <div>
            <div id="projects" class="relative -top-30"></div> <!-- Anchor -->

            <div class="p-15 bg-base-300">
                <h2 class="text-6xl font-semibold">Projekty</h2>
                <p class="text-3xl mt-7">
                    Zde jsou některé z mých projektů, na kterých jsem pracoval nebo stále pracuji.
                </p>
            </div>

            <Project
                name="xo"
                description='Online hra piškvorky s neomezeným polem a možností vytvoření účtu. Napsaná v jazyce JavaScript s frameworky SvelteKit, Tailwind a DaisyUI na straně klienta a Node.js, Socket.io a Express na straně serveru.<br>
                    Server běhá buď na Raspberry Pi v mém pokoji, nebo na Dropletu v <a class="underline text-accent" href="https:/digitalocean.com" target="_blank">DigitalOcean</a>. <br>
                    Základní kostra HTML byla vygenerována pomocí AI, vzhled stránce však dává DaisyUI. <br>
                    Jde hrát proti náhodému soupeři nebo proti přátelům pomocí unikátního odkazu. <br>
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

            <Project
                name="Portfolio"
                description='Tato webová stránka, kterou si právě prohlížíte, je také jeden z mých projektů.
                    Napsaná je v jazycích JavaScript a HTML s frameworky Svelte, Tailwind a DaisyUI, zveřejněná je přes Netlify.
                    Byla vytvořena bez použití AI (s výjimkou autocompletů ve VS Code). <br>
                    Zdrojový kód je dostupný na GitHubu: <a class="underline text-primary" href="https://github.com/danielde8/portfolio" target="_blank">danielde8/portfolio</a>'
                imgSrc="assets/projects/portfolio.png"
                imgWidth=140
                evenProject={ false }
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
                    imgSrc="assets/skills/svelte.svg"
                />

                <Skill
                    name="Node.js"
                    description='Node.js používám pro tvorbu backendů/API pro své webové aplikace. Pro API nebo statické stránky používám framework <a class="underline text-accent" href="https://expressjs.com" target="_blank">Express.js</a>
                        hlavně kvůli jeho jednoduchosti a komunitě. Pro real-time komunikaci (např. ve hrách) používám <a class="underline text-accent" href="https://socket.io/" target="_blank">Socket.io</a>.
                        Node.js mám velmi rád, protože mi umožňuje psát frontend i backend ve stejném jazyce. Naučil jsem se na něm mimo jiné i základy HTTP requestů.'
                    imgSrc="assets/skills/nodejs.svg"
                />

                <Skill
                    name="Kotlin"
                    description='Ve 4. třídě jsem se začal učit programovat v jazyce Kotlin, ne však pro Android, ale pro tvorbu her a desktopových aplikací
                        pomocí <a class="underline text-accent" href="https://korge.org" target="_blank">KorGE</a> a Java Swing.
                        Kotlin je dnes můj nejoblíbenější jazyk, hlavně pro jeho všechny možné vestavěné funkce a možnost využít Java knihovny.
                        V Kotlinu většinou píšu menší projekty, které bývají spíše experimenty než hotové aplikace.'
                    imgSrc="assets/skills/kotlin.png"
                />

                <Skill
                    name="C a Assembly"
                    description='Sice o sobě nemohu říct, že jsem v těchto jazycích expert, ale něco v nich napsat dokážu.
                        Už dlouho byl můj sen vytvořit vlastní operační systém, který by se dal spustit alespoň na VM, i kdyby to mělo být jen <span class="italic">Hello World</span>.
                        To se mi konečně podařilo někdy v 6. třídě, kdy jsem (pomocí AI :D) napsal jednoduchý Assembly kód, který vypsal jedno písmeno a dal se spustit ve <a class="underline text-accent" href="https://www.virtualbox.org/" target="_blank">VirtualBoxu</a>.
                        Po snad ještě delší době se mi <span class="italic">konečně</span> podařilo načíst C program a zanedlouho nato jsem začal pracovat na svém <a class="underline text-primary" href="#SnakeOS">vlastním "OS"</a>, který je popsán výše.<br>
                        C mimo to používám i pro psaní programů, kde potřebuji často pracovat s čísly na nižší úrovni, například pro emulátor CPU. (<a class="underline text-primary" href="#MUPC">MUPC</a> - viz výše)'
                    imgSrc="assets/skills/c.png"
                />

                <Skill
                    name="Linux a servery"
                    description='Už ani nevím, kdy jsem začal používat Linux, ale je to už celkem dávno.
                        Většinou používám distribuci Ubuntu Server nebo Kali Linux. Na svém hlavním počítači mám sice macOS, ale mám i dva staré notebooky, které jsem přeinstaloval z Windows 7 na Linux.
                        První jsem používal jako Minecraft server pro kamarády, na druhém běží Kali, používám ho tedy na učení se KB, hlavně na <a class="underline text-accent" href="https://www.hackthebox.com/" target="_blank">Hack The Box</a>.'
                    imgSrc="assets/skills/tux.png"
                />
            </div>
        </div>

        <!-- Other -->
        <div>
            <div id="other" class="relative -top-30"></div> <!-- Anchor -->

            <div class="p-15 bg-base-200">
                <h2 class="text-6xl font-semibold">Ostatní</h2>
                
                <Other
                    name="Robosoutěž"
                    description='V letech 2024 a 2025 (7. a 8. třídě) jsem se účastnil Robosoutěže pro ZŠ na ČVUT v Praze za týmy
                        <span class="font-bold">Mechanický chaos</span> a
                        <span class="font-bold">18²</span>, kde jsem se s týmem umístil dvakrát na 7. místě.<br>
                        Záznam z roku 2024 je na YouTube: <a class="underline text-accent" href="https://youtu.be/nf78Hmo0gtk?t=5339" target="_blank">Robosoutěž 2024 pro základní školy - 2. kolo (čtvrtek)</a><br>
                        Záznam z roku 2025 je na YouTube: <a class="underline text-accent" href="hhttps://youtu.be/0mtSDXTiySE?t=17041" target="_blank">Robosoutěž 2025 pro základní školy - 1. kolo (středa)</a>'
                    imgSrc="assets/other/robosoutez.png"
                    imgWidth=140    
                />

                <Other
                    name="Angličtina"
                    description='Angličtinu používám hodně často, hlavně při programování, protože většina dokumentace je v angličtině, a proto většinou i kód píšu v angličtině.
                        Mimo to jsem v šesté třídě navštívil USA na tři měsíce, kde jsem chodil do místní školy. Momentálně jsem v USA znovu, na dva a půl měsíce, a tentokrát navštěvuji střední školu (v USA od 9. třídy).'
                    imgSrc="assets/other/anglictina.png"
                    imgWidth=140
                />

                <Other
                    name="Videohry"
                    description='Ve volném čase rád hraju videohry, buď singleplayer, nebo s kamarády. Mezi mé nejoblíbenější patří 
                        <a class="underline text-accent" href="https://store.steampowered.com/app/264710/Subnautica/" target="_blank">Subnautica</a>,
                        <a class="underline text-accent" href="https://store.steampowered.com/app/1174180/Red_Dead_Redemption_2/" target="_blank">Red Dead Redemption 2</a>, 
                        <a class="underline text-accent" href="https://www.minecraft.net/en-us/" target="_blank">Minecraft</a>, 
                        <a class="underline text-accent" href="https://store.steampowered.com/app/620/Portal_2/" target="_blank">Portal 2</a> a 
                        <a class="underline text-accent" href="https://store.steampowered.com/app/220200/Kerbal_Space_Program/" target="_blank">Kerbal Space Program</a>
                        - na kterém jsem se naučil základy orbitální mechaniky.'
                    imgSrc="assets/other/gaming.png"
                    imgWidth=140
                />

                <Other
                    name="Housle"
                    description='Na housle hraju už od 2. třídy, kdy jsem začal chodit do ZUŠ Vrané nad Vltavou.
                        Moje nejoblíbenější skladba je <a class="underline text-accent" href="https://www.youtube.com/watch?v=yCzNSPKbXv8" target="_blank">Zdeňek Fibich - Sonatina</a>
                        (1. věta), kterou jsem hrál v roce 2025. V roce 2026 budu mít absolventský koncert, na kterém budu hrát
                        <a class="underline text-accent" href="https://www.youtube.com/watch?v=J6b7WH9Le-E" target="_blank">Vivaldi - Koncert G dur</a>.'
                    imgSrc="assets/other/housle.jpg"
                    imgWidth=140
                />

                <Other
                    name="Vysokohorská turistika"
                    description='Vzhledem k tomu, že máme příbuzné na Slovensku, často tam jezdíme a chodíme po horách.
                        Nejraději mám Žiarsou dolinu, korétně Tri Kopy, a Kriváň, který jsem zdolal v roce 2024. Na fotce je pohled z Kriváně na Vysoké Tatry.'
                    imgSrc="assets/other/hory.JPG"
                    imgWidth=140
                />
            </div>
        </div>
        
        <div class="bg-base-300 text-2xl py-7 text-center font-semibold">
            GitHub: <a class="underline text-primary" href="https://github.com/danielde8" target="_blank">github.com/danielde8</a>
        </div>
    </div>
</div>