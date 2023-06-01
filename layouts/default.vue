<template>
    <div>
        
        <header>
            <Navbar/>
        </header>
        <main class="container p-3 my-5 border rounded shadow">
            <slot/>
        </main>
        <Footer/>
        
    </div>
</template>
<script setup>
    //Este composable nos permite acceder al head de nuestra aplicación.
    useHead({
        //Esto lo hacemos para la configuración del título.
        titleTemplate:"%s - Intro Nuxt",
        //Aquí le agregas clases a todo el body del proyecto.
        bodyAttrs:[{
            class:'text-center'
        }],
        link:[
            // Este sería el CSS de Bootstrap
            {
                rel:"stylesheet",
                href:"https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/css/bootstrap.min.css",
                integrity:"sha384-KK94CHFLLe+nY2dmCWGMq91rCGa5gtU4mk92HdvYe+M/SXH301p5ILy+dN9+nJOZ",
                crossorigin:"anonymous"
            }
        ],
        script:[
            //Este sería el JS de Bootstrap
            {
                src:'https://cdn.jsdelivr.net/npm/bootstrap@5.3.0-alpha3/dist/js/bootstrap.bundle.min.js',
                body:true //esto hace que el script se importe en el body en lugar del head.
            }
        ]
    });
</script>