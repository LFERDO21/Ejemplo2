<template>
    <div id="app" class="font-roboto bg-gray-100">
        <navbar></navbar>

        <div class="px-6 py-8">
            <div class="flex justify-between container mx-auto">
                <div class="w-full lg:w-8/12">
                    <div class="flex items-center justify-between">
                        <h1 class="text-xl font-bold text-gray-700 md:text-2xl">Publicaciones</h1>
                        <post-filter></post-filter>
                    </div>
                    <div class="mt-6" v-for="post in posts" :key="post.id">
                        <post :data="post"></post>
                    </div>
                    <div class="mt-8">
                        <Pagination></Pagination>
                    </div>
                </div>
                <div class="-mx-8 w-4/12 hidden lg:block">
                    <div class="px-8">
                        <h1 class="mb-4 text-xl font-bold text-gray-700">Autores</h1>
                        <users-list></users-list>
                    </div>
                    <div class="mt-10 px-8">
                        <h1 class="mb-4 text-xl font-bold text-gray-700">Categorias</h1>
                        <categories></categories>
                    </div>
                    <div class="mt-10 px-8">
                        <h1 class="mb-4 text-xl font-bold text-gray-700">Publicaciones Recientes</h1>
                        <recent-post></recent-post>
                    </div>
                </div>
            </div>
        </div>
        
        <simple-footer></simple-footer>
    </div>
</template>

<script>
    import Navbar from "./components/navigation-navbar-simple";
    import PostFilter from "./components/elements-select-option";
    import Post from "./components/elements-blog-post-article-review";
    import Pagination from "./components/elements-pagination";
    import UsersList from "./components/sections-blog-users-list";
    import Categories from "./components/sections-categories-list";
    import RecentPost from "./components/sections-recent-article";
    import SimpleFooter from "./components/navigation-footer-simple-with-icon";

    export default {
        name: 'app',
        components: {
            Navbar,
            PostFilter,
            Post,
            Pagination,
            UsersList,
            Categories,
            RecentPost,
            SimpleFooter
        },
        data() {
            return {
                posts: [
                    {
                        id: 1,
                        date: "Jun 1, 2022",
                        tag: "Superacion",
                        title: "El Duelo por Fallecimiento de una Mascota",
                        body: "El duelo por fallecimiento de una mascota  ???Cerca de aqu?? reposan los restos de una criatura que fue bella sin vanidad, fuerte sin insolencia, valiente sin ferocidad y tuvo todas las virtudes del hombre y ninguno de sus defectos.???   Lord Byron  ??C??mo afrontar la...",
                        image: "https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=731&q=80",
                        userName: "Alex John"
                    },
                    {
                        id: 2,
                        date: "mar 4, 2022",
                        tag: "Personalidad",
                        title: "Personalidad Querulante",
                        body: "??C??mo son las personas querulantes o litigantes? El trastorno de personalidad que tiene la gente que est?? en constantes litigios.  Personalidad Querulante: el t??rmino querulante viene del lat??n ???querelus???, cuyo significado es ???que se queja???. Es un adjetivo que hace...",
                        image: "https://images.unsplash.com/photo-1464863979621-258859e62245?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=333&q=80",
                        userName: "Jane Doe"
                    },
                    {
                        id: 3,
                        date: "Feb 14, 2022",
                        tag: "Sentimientos",
                        title: "Depresi??n Encubierta, S??ntomas y tratamiento",
                        body: "DEPRESI??N ENCUBIERTA   La depresi??n puede estar presente y muy cerca de nosotros.   Leyendo el mensaje de los s??ntomas y caracter??sticas, cuando la depresi??n se encubre  Antes de definir la depresi??n encubierta, vamos a hablar de la depresi??n. Depresi??n  es una...",
                        image: "https://images.unsplash.com/photo-1531251445707-1f000e1e87d0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=281&q=80",
                        userName: "Lisa Way"
                    },
                    {
                        id: 4,
                        date: "Dec 23, 2022",
                        tag: "Genero",
                        title: "Peliculas para comprender la identidad transg??nero",
                        body: "PEL??CULAS PARA ADENTRARNOS EN LAS IDENTIDADES TRANSG??NERO Son muchas las pel??culas que versan sobre la tem??tica de identidad transg??nero o que incluyen personajes trans en sus desarrollos de gui??n.  S?? que es cierto, que de un tiempo a esta parte hay m??s...",
                        image: "https://images.unsplash.com/photo-1500757810556-5d600d9b737d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=735&q=80",
                        userName: "Steve Matt"
                    },
                    {
                        id: 5,
                        date: "Mar 10, 2022",
                        tag: "Juveniles",
                        title: "Ni??os con Altas Capacidades",
                        body: "Visibilizando las altas capacidades cognitivas en ni??os El 14 de marzo es la fecha propuesta para conmemorar el D??a de las Altas Capacidades. Los D??as Internacionales no son un capricho, sino que sirven para visibilizar, sensibilizar o llamar la atenci??n sobre una...",
                        image: "https://images.unsplash.com/photo-1502980426475-b83966705988?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=373&q=80",
                        userName: "Khatab Wedaa"
                    },
                ]
            }
        }
    }
</script>

<style>
    @import "assets/css/app.css";

    ::-webkit-scrollbar {
        width: 5px;
    }

    ::-webkit-scrollbar-track {
        background: #2D3748;
    }

    ::-webkit-scrollbar-thumb {
        background: #CBD5E0;
    }

    ::-webkit-scrollbar-thumb:hover {
        background: #2D3748;
    }
</style>
