<template>
    <v-container>
        <!-- Navbar -->
        <v-card>
            <v-tabs v-model="tab" color="deep-purple-accent-4" class="d-flex justify-center">
                <v-tab :value="1" @click="scrollToTopic('inicio')">Inicio</v-tab>
                <v-tab :value="2" @click="scrollToTopic('sobre-nos')">Sobre Nós</v-tab>
                <v-tab :value="3" @click="scrollToTopic('cursos')">Cursos</v-tab>
            </v-tabs>
        </v-card>

        <br>

        <!-- Início -->
        <v-card id="inicio">
            <v-card-title>Inicio</v-card-title>
            <v-card-text>
                Bem-vindo à nossa faculdade! Aqui você encontrará uma educação de qualidade para impulsionar o seu
                futuro.
            </v-card-text>
        </v-card>

        <br>

        <!-- Sobre nós -->
        <v-card id="sobre-nos">
            <v-card-title>Sobre Nós</v-card-title>
            <v-card-text>
                Somos uma instituição comprometida em fornecer educação de excelência, preparando nossos alunos para
                os
                desafios do mundo real.
            </v-card-text>
        </v-card>

        <br>

        <!-- Cursos -->
        <v-card id="cursos">
            <v-card-title>Cursos</v-card-title>
            <v-card-text>
                Confira abaixo alguns dos cursos oferecidos em nossa faculdade:
                <ul>
                    <li>Engenharia de Software</li>
                    <li>Ciência da Computação</li>
                    <li>Administração de Empresas</li>
                </ul>
            </v-card-text>
        </v-card>

        <br>

        <!-- Botão de Voltar ao Topo -->
        <v-btn fab bottom right class="back-to-top" :class="{ 'show': isScrolled }" @click="scrollToTop">
            <v-icon>mdi-arrow-up</v-icon>
        </v-btn>
    </v-container>
</template>

<script>
export default {
    data: () => ({
        tab: null,
        isScrolled: false
    }),
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
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
        }
    },
};
</script>

<style scoped>
.back-to-top {
    position: fixed;
    bottom: 20px;
    right: 20px;
    opacity: 0;
    transition: opacity 0.3s;
}

.back-to-top.show {
    opacity: 1;
}
</style>
