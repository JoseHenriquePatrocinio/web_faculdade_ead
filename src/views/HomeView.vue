<template>
    <div>
        <v-container>
            <!-- Navbar -->
            <v-card>
                <v-tabs v-model="tab" color="deep-purple-accent-4" class="d-flex justify-center">
                    <v-tab :value="1" @click="scrollToTopic('inicio')">Início</v-tab>
                    <v-tab :value="2" @click="scrollToTopic('sobre-nos')">Sobre Nós</v-tab>
                    <v-tab :value="3" @click="scrollToTopic('cursos')">Cursos</v-tab>
                </v-tabs>
            </v-card>

            <br>

            <!-- Início -->
            <v-card id="inicio">
                <v-card-title class="headline font-weight-bold">Bem-vindo à nossa faculdade!</v-card-title>
                <v-card-text>
                    Aqui você encontrará uma educação de qualidade para impulsionar o seu futuro.
                </v-card-text>
            </v-card>

            <br>

            <!-- Sobre nós -->
            <v-card id="sobre-nos">
                <v-card-title class="headline font-weight-bold">Sobre Nós</v-card-title>
                <v-card-text>
                    Somos uma instituição comprometida em fornecer educação de excelência, preparando nossos alunos para
                    os desafios do mundo real.
                </v-card-text>
            </v-card>

            <br>

            <!-- Cursos -->
            <v-card id="cursos">
                <v-card-title class="headline font-weight-bold">Cursos</v-card-title>
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

            <!-- Botão de Voltar ao Topo -->
            <v-btn fab bottom right class="back-to-top" :class="{ 'show': isScrolled }" @click="scrollToTop"
                style="position: fixed; z-index: 9999;">
                <v-icon>mdi-arrow-up</v-icon>
            </v-btn>

        </v-container>
        <!-- Footer -->
        <v-footer color="indigo" class="mt-16">
            <span class="white--text">&copy; 2024 Escola Sistêmica</span>
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
        shouldContain: false
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
</style>