<template>
    <div class="flex flex-col bg-white max-w-sm px-6 py-4 mx-auto rounded-lg shadow-md">
        <ul class="-mx-4">
            <li class="flex items-center">
                <img class="w-10 h-10 object-cover rounded-full mx-4" src="https://images.unsplash.com/photo-1492562080023-ab3db95bfbce?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=731&q=80" alt="avatar">
                <p>
                    <a class="text-gray-700 font-bold mx-1 hover:underline" href="#">DR. Lynn O’Brien</a>
                    <span class="text-gray-700 text-sm font-light">Creó 23 Publicaciones</span>
                </p>
            </li>

            <li class="flex items-center mt-6">
                <img class="w-10 h-10 object-cover rounded-full mx-4" src="https://images.unsplash.com/photo-1464863979621-258859e62245?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=333&q=80" alt="avatar">
                <p>
                    <a class="text-gray-700 font-bold mx-1 hover:underline" href="#">DR. R. Honey</a>
                    <span class="text-gray-700 text-sm font-light">Creó 15 Publicaciones</span>
                </p>
            </li>
            
            <li class="flex items-center mt-6">
                <img class="w-10 h-10 object-cover rounded-full mx-4" src="https://images.unsplash.com/photo-1531251445707-1f000e1e87d0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=281&q=80" alt="avatar">
                <p>
                    <a class="text-gray-700 font-bold mx-1 hover:underline" href="#">DR. Erick Escandón Pérez </a>
                    <span class="text-gray-700 text-sm font-light">Creó 42 Publicaciones</span>
                </p>
            </li>

            <li class="flex items-center mt-6">
                <img class="w-10 h-10 object-cover rounded-full mx-4" src="https://images.unsplash.com/photo-1500757810556-5d600d9b737d?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=735&q=80" alt="avatar">
                <p>
                    <a class="text-gray-700 font-bold mx-1 hover:underline" href="#">Lic. Lourdes Becerra</a>
                    <span class="text-gray-700 text-sm font-light">Creó 15 Publicaciones</span>
                </p>
            </li>

            <li class="flex items-center mt-6">
                <img class="w-10 h-10 object-cover rounded-full mx-4" src="https://images.unsplash.com/photo-1502980426475-b83966705988?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=373&q=80" alt="avatar">
                <p>
                    <a class="text-gray-700 font-bold mx-1 hover:underline" href="#">Dr. Rogelio López</a>
                    <span class="text-gray-700 text-sm font-light">Creó 50 Publicaciones</span>
                </p>
            </li>
        </ul>
    </div>
</template>

<script>
    export default {
        props: ['data']
    }
</script>