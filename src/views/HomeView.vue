<template>
    <div>
        <v-container>
            <!-- Navbar -->
            <v-card>
                <v-tabs v-model="tab" color="deep-purple-accent-4" class="d-flex justify-center">
                    <v-tab :value="1" @click="scrollToTopic('inicio')">Início</v-tab>
                    <v-tab :value="2" @click="scrollToTopic('objetivo')">Objetivo</v-tab>
                    <v-tab :value="3" @click="scrollToTopic('docente')">Especialistas</v-tab>
                    <v-tab :value="3" @click="scrollToTopic('cursos')">Cursos</v-tab>
                    <v-tab :value="3" @click="scrollToTopic('depoimentos')">Depoimentos</v-tab>
                </v-tabs>

                <!-- Banner -->
                <div id="main-banner">
                    <h1>Escola Sistêmica</h1>
                </div>
            </v-card>

            <br>

            <!-- Início -->
            <v-card id="inicio">
                <v-card-title class="headline font-weight-bold">Boas vindas à Escola Sistêmica!</v-card-title>
                <v-card-text>
                    Somos uma instituição comprometida em fornecer educação de excelência, preparando nossos alunos para
                    enfrentarem com destreza e confiança os desafios complexos e dinâmicos do mundo real, capacitando-os
                    não apenas com conhecimento teórico, mas também com habilidades práticas e uma mentalidade
                    resiliente e inovadora, visando não apenas o sucesso individual, mas também contribuindo para o
                    progresso e desenvolvimento da sociedade como um todo.
                </v-card-text>
            </v-card>

            <br>

            <!-- Sobre nós -->
            <v-card id="objetivo">
                <v-card-title class="headline font-weight-bold">Objetivo</v-card-title>
                <v-card-text>
                    <h3>Missão:</h3>
                    <p>Nossa missão é promover a transformação positiva na vida dos nossos alunos, fornecendo uma
                        educação de excelência que os capacite a alcançar seu pleno potencial acadêmico, profissional e
                        pessoal. Estamos comprometidos em oferecer um ambiente de aprendizado inspirador, centrado no
                        aluno, que promova o pensamento crítico, a criatividade e a inovação, preparando-os para os
                        desafios e oportunidades do mundo contemporâneo.</p>

                    <h3>Visão:</h3>
                    <p>Nossa visão é ser reconhecidos como uma instituição de referência em educação de qualidade,
                        conhecida por sua excelência acadêmica, compromisso com a inovação educacional e impacto
                        positivo na comunidade. Buscamos ser líderes na formação de profissionais éticos, responsáveis,
                        e preparados para enfrentar os desafios globais, contribuindo assim para um mundo mais justo,
                        sustentável e inclusivo.</p>

                    <h3>Valores:</h3>
                    <ul>
                        <li><strong>Excelência:</strong> Buscamos a excelência em tudo o que fazemos, desde o ensino e
                            aprendizado até a administração e serviços oferecidos aos nossos alunos e comunidade.</li>
                        <li><strong>Integridade:</strong> Pautamos nossas ações na mais alta ética e integridade,
                            cultivando relações de confiança e respeito mútuo.</li>
                        <li><strong>Inovação:</strong> Estamos sempre em busca de novas abordagens e soluções criativas
                            para melhorar continuamente nossa oferta educacional e atender às necessidades em constante
                            evolução dos nossos alunos e da sociedade.</li>
                        <li><strong>Empoderamento:</strong> Valorizamos e incentivamos a autonomia, a iniciativa e o
                            desenvolvimento pessoal e profissional de nossos alunos, preparando-os para serem agentes de
                            mudança e liderança em suas áreas de atuação.</li>
                        <li><strong>Responsabilidade Social e Ambiental:</strong> Comprometemo-nos a agir de forma
                            socialmente responsável, promovendo a inclusão, a diversidade e a sustentabilidade em todas
                            as nossas atividades e operações.</li>
                    </ul>
                </v-card-text>
            </v-card>

            <br>

            <!-- Corpo docente -->
            <v-card id="docente">
                <v-card-title class="headline font-weight-bold">Nossos especialistas</v-card-title>
                <v-row>
                    <v-col cols="4" class="text-center">
                        <v-avatar size="80">
                            <img src="https://img.freepik.com/fotos-gratis/retrato-de-uma-jovem-sorrindo_23-2149260597.jpg?t=st=1711499002~exp=1711502602~hmac=3face60b7815c3878960ef390f56ff0d1352627d1ea42d57e741133208394dcb&w=996"
                                alt="Célia Almada">
                        </v-avatar>
                        <p class="font-weight-bold">Célia Almada</p>
                        <p>Mestre em Tecnologia</p>
                    </v-col>
                    <v-col cols="4" class="text-center">
                        <v-avatar size="80">
                            <img src="https://img.freepik.com/fotos-gratis/homem-retrato-rindo_23-2148859448.jpg?t=st=1711498954~exp=1711502554~hmac=626446ffae674daae4ebf994f42614164ef5ec9b4f7ef66879ac7ef7d754f2da&w=740"
                                alt="Frank Kinney">
                        </v-avatar>
                        <p class="font-weight-bold">Frank Kinney</p>
                        <p>Doutor em Matemática Aplicada</p>
                    </v-col>
                    <v-col cols="4" class="text-center">
                        <v-avatar size="80">
                            <img src="https://img.freepik.com/fotos-gratis/jovem-sorridente-e-desajeitado-com-oculos-posando_176420-30012.jpg?w=996&t=st=1711499150~exp=1711499750~hmac=8279e5ae756bb5c3af25204e2b17ca425a62dfe6eb86e72359551583fdf4d3eb"
                                alt="Nick Johnson">
                        </v-avatar>
                        <p class="font-weight-bold">Nick Johnson</p>
                        <p>Mestre em Engenharia Civil</p>
                    </v-col>
                </v-row>
            </v-card>

            <br>

            <!-- Cursos -->
            <v-card id="cursos">
                <v-card-title class="headline font-weight-bold">Nossos Cursos</v-card-title>
                <v-carousel>
                    <v-carousel-item
                        src="https://img.freepik.com/psd-gratuitas/modelo-de-impressao-de-marketing-com-foto_23-2148947056.jpg?w=740&t=st=1711428170~exp=1711428770~hmac=2fb3e31dbd720bf801e5bb7e2f9d054cf1a122c5cfef7d26d8d4a1184ee4e723"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                    <v-carousel-item
                        src="https://img.freepik.com/psd-gratuitas/modelo-de-poster-para-aula-de-arte-online_23-2149020959.jpg?w=740&t=st=1711427655~exp=1711428255~hmac=3bb15b39a7d1bb7f87781063953ef073149553e9594088c67e98438dbd3ee5a5"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                    <v-carousel-item
                        src="https://img.freepik.com/psd-gratuitas/modelo-de-impressao-comercial-com-foto_23-2148904321.jpg?w=740&t=st=1711427726~exp=1711428326~hmac=5e44ce62fa7e80a3100c826a09ec3853722c77a7293c8e12eaa04177a88c02d2"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                    <v-carousel-item
                        src="https://img.freepik.com/psd-gratuitas/modelo-de-banner-de-midia-social-para-dentista-e-atendimento-odontologico_120329-1313.jpg?w=740&t=st=1711427893~exp=1711428493~hmac=d269b8a66a12d4c6fb82a556aada5762f86a75720b2922b9367f4aadccd60b00"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                    <v-carousel-item
                        src="https://img.freepik.com/vetores-premium/modelo-de-banner-da-web-e-midia-social-corporativa-para-agencia-de-marketing-digital_123589-55.jpg?w=740"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                    <v-carousel-item
                        src="https://img.freepik.com/psd-premium/agencia-de-marketing-digital-e-design-de-modelo-de-banner-de-postagem-de-midia-social-corporativa_494960-208.jpg?w=740"
                        class="carousel-item" :contain="shouldContain"></v-carousel-item>
                </v-carousel>
            </v-card>

            <br>

            <!-- Depoimentos -->
            <v-card id="depoimentos">
                <v-card-title class="headline font-weight-bold">Depoimentos</v-card-title>
                <v-row>
                    <v-col v-for="person in people" :key="person.name" cols="12" sm="6" md="4" lg="3">
                        <v-card outlined class="mb-4">
                            <v-img :src="person.avatar" height="200"></v-img>
                            <v-card-text class="text-center">
                                {{ person.text }}
                            </v-card-text>
                            <v-card-subtitle class="text-center">{{ person.name }}</v-card-subtitle>
                        </v-card>
                    </v-col>
                </v-row>
            </v-card>

            <br>

            <!-- Botão de Voltar ao Topo -->
            <v-btn fab bottom right class="back-to-top" :class="{ 'show': isScrolled }" @click="scrollToTop"
                style="position: fixed; z-index: 9999;">
                <v-icon>mdi-arrow-up</v-icon>
            </v-btn>

        </v-container>

        <!-- Footer -->
        <v-footer dark padless>
            <v-card class="flex" flat tile>
                <v-card-title class="blue darken-4">
                    <strong class="subheading">Conecte-se conosco nas redes sociais!</strong>

                    <v-spacer></v-spacer>

                    <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
                        <v-icon size="24px">
                            {{ icon }}
                        </v-icon>
                    </v-btn>
                </v-card-title>

                <v-card-text class="py-2 white--text text-center">
                    {{ new Date().getFullYear() }} — <strong>Escola Sistêmica</strong>
                </v-card-text>
            </v-card>
        </v-footer>
    </div>
</template>

<script>
export default {
    components: {

    },
    data: () => ({
        tab: null,
        isScrolled: false,
        shouldContain: false,
        icons: [
            'mdi-facebook',
            'mdi-twitter',
            'mdi-linkedin',
            'mdi-instagram',
        ],
        "people": [
            {
                "name": "STELLA LARSON",
                "text": "Estou extremamente satisfeita com minha experiência na faculdade. Os professores são incrivelmente competentes e prestativos, e a grade curricular é desafiadora, mas gratificante.",
                "avatar": "https://img.freepik.com/fotos-gratis/na-moda-jovem-olhando-feliz_1298-527.jpg?w=740&t=st=1711508710~exp=1711509310~hmac=d052de809f8af2063d5f0cd85c59688f410dcd159e4d6f80df10f843f4e0f6dd"
            },
            {
                "name": "NICK JOHNSON",
                "text": "Estou muito feliz com minha escolha de faculdade. O ambiente acadêmico é inspirador e motivador, e as oportunidades de aprendizado são infinitas. Mal posso esperar para ver o que o futuro reserva!",
                "avatar": "https://img.freepik.com/fotos-gratis/jovem-vestindo-uma-roupa-azul-olhando-engracado_1298-424.jpg?w=740&t=st=1711508573~exp=1711509173~hmac=f6b1f5212c3586d9dc808d62267d74248703fb8be70f149d4c82fc5779c7a2da"
            },
            {
                "name": "OLGA IVANOVA",
                "text": "Minha experiência na faculdade tem sido incrível. A qualidade do ensino é excepcional e as atividades extracurriculares enriquecem ainda mais meu aprendizado. Estou grata por fazer parte dessa comunidade acadêmica.",
                "avatar": "https://img.freepik.com/fotos-premium/um-retrato-de-uma-mulher-caucasiana-estudante-universitaria-na-biblioteca-profundidade-de-campo-rasa_600776-18548.jpg?w=740"
            },
            {
                "name": "PAUL HDSON",
                "text": "Estou muito satisfeito com minha jornada universitária. Os recursos disponíveis e o suporte da equipe acadêmica tornaram minha experiência educacional muito gratificante. Estou ansioso para aplicar o que aprendi no mundo real.",
                "avatar": "https://img.freepik.com/fotos-premium/latino-caucasiano-vestido-casualmente-com-os-bracos-cruzados-sobre-um-fundo-branco_1071113-349.jpg?w=740"
            },
            {
                "name": "DINHEIRO HDSON",
                "text": "Minha jornada na faculdade tem sido repleta de aprendizado e crescimento pessoal. Os desafios acadêmicos me incentivaram a superar meus limites e me prepararam para os desafios futuros. Estou muito grato pela oportunidade de estudar aqui.",
                "avatar": "https://img.freepik.com/fotos-gratis/jovem-vestindo-uma-roupa-azul-vestindo-capacete-vermelho-apontando-para_1298-240.jpg?w=740&t=st=1711508756~exp=1711509356~hmac=b0897b6d5e1d6eb5f8bb3fe060440eaa8be5e6301bfc9a0f59477964c2ec7853"
            },
            {
                "name": "MARY JANE",
                "text": "Não poderia estar mais satisfeito com minha experiência na universidade. Os professores são apaixonados pelo que fazem e estão sempre disponíveis para ajudar. Estou confiante de que estou recebendo uma educação de alta qualidade.",
                "avatar": "https://img.freepik.com/fotos-premium/aluno-feliz-com-o-aprendizado-on-line-estudo-por-tecnologia-de-conteudo-elearning-com-telefone-celular-profundidade-de-campo-rasa_600776-12737.jpg?w=740"
            },
            {
                "name": "VITO JAVASCRIPTO",
                "text": "Estou aproveitando ao máximo minha jornada universitária. As oportunidades de networking e as experiências práticas oferecidas pela faculdade estão me preparando bem para minha futura carreira. Sou grato por esta oportunidade de crescimento.",
                "avatar": "https://img.freepik.com/fotos-gratis/o-homem-que-veste-um-laco-vermelho-piscar-de-olho_1298-320.jpg?w=740&t=st=1711508950~exp=1711509550~hmac=078178e78069e49a33d1100a3e94dd806cb79e992a49ec44ecbd9fe54faa66d5"
            },
            {
                "name": "JONHNNY JSON",
                "text": "Minha experiência na faculdade tem sido excepcional. A atmosfera colaborativa e o ambiente de aprendizado estimulante tornam cada dia emocionante. Mal posso esperar para ver onde minha educação me levará.",
                "avatar": "https://img.freepik.com/fotos-premium/homem-negro-bonito-sentado-e-usando-laptop-dentro-de-casa_251136-89394.jpg"
            }
        ],
    }),
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
        this.updateContainProperty();
        window.addEventListener('resize', this.updateContainProperty);
    },
    destroyed() {
        window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
        scrollToTopic(topicId) {
            const element = document.getElementById(topicId);
            if (element) {
                element.scrollIntoView({ behavior: 'smooth', block: 'start' });
            }
        },
        scrollToTop() {
            window.scrollTo({ top: 0, behavior: 'smooth' });
        },
        handleScroll() {
            this.isScrolled = window.scrollY > 20;
        },
        updateContainProperty() {
            if (window.innerWidth > 600) {
                this.shouldContain = true;
            } else {
                this.shouldContain = false;
            }
        }
    },
};
</script>

<style scoped>
.back-to-top {
    position: fixed;
    bottom: 60px;
    right: 20px;
    opacity: 0;
    transition: opacity 0.3s;
}

.back-to-top.show {
    opacity: 1;
}

.v-footer {
    bottom: 0px;
    left: 0px;
    width: 100%;
}

.headline {
    font-size: 24px;
}

.font-weight-bold {
    font-weight: bold;
}

.mt-16 {
    margin-top: 16px;
}

#main-banner {
    background-image: url("https://img.freepik.com/psd-gratuitas/modelo-de-banner-de-narrativa-com-foto_23-2148945593.jpg?w=826&t=st=1711433794~exp=1711434394~hmac=886371e2e43c7813179f1fde76df29d7473f7606aa22d714b9f7875983097239");
    background-position: 0;
    background-size: cover;
    height: 500px;
    display: flex;
    align-items: center;
}

#main-banner h1 {
    color: #FFF;
    background-color: #222;
    padding: 20px 40px;
}

@media screen and (max-width: 600px) {
    #main-banner h1 {
        opacity: 0.7;
    }
}

@media screen and (max-width: 600px) {
    #main-banner {
        height: 300px;
    }
}

.testimonial-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
}

.testimonial-container v-col {
    flex: 0 0 calc(33.33% - 16px);
    margin: 8px;
}


@media (max-width: 768px) {
    .testimonial-container v-col {
        flex: 0 0 calc(50% - 16px);
    }
}
</style>