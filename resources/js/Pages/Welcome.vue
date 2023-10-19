<script setup>
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    canLogin: {
        type: Boolean,
    },
    canRegister: {
        type: Boolean,
    },
    laravelVersion: {
        type: String,
        required: true,
    },
    phpVersion: {
        type: String,
        required: true,
    },
});
</script>
<template>
    <div>
      <Head title="Welcome" />
      <div class="bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white">
        <header class="bg-green-500 text-white py-4">
          <div class="container mx-auto flex justify-between items-center">
            <div class="text-2xl font-semibold">Logo de la Clínica</div>
            <ul class="flex space-x-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">
              <li><a href="#">Inicio</a></li>
              <li><a href="#">Servicios</a></li>
              <li><a href="#appointment">Citas</a></li>
              <li><a href="#">Blog</a></li>
              <li><a href="#">Sobre Nosotros</a></li>
              <li><a href="#">Contacto</a></li>
              <li>
                <a v-if="$page.props.auth.user" :href="route('dashboard')" class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Dashboard</a>
                <template v-else>
                  <a :href="route('login')" class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Iniciar Sesion</a>
                  <a v-if="canRegister" :href="route('register')" class="ml-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Registrarse</a>
                </template>
              </li>
            </ul>


          </div>
        </header>

        <section class="py-16 bg-white">
        <div class="container mx-auto text-center">
          <h1 class="text-4xl font-semibold">Bienvenido a la Clínica Veterinaria</h1>
          <p class="text-lg">Cuidando de tus mascotas como si fueran de la familia.</p>
          <a href="#appointment" class="bg-green-500 text-white px-6 py-3 rounded-full mt-6 inline-block hover:bg-green-600 transition duration-300">Solicitar Cita</a>
        </div>
      </section>

      <!-- Sección de Servicios -->
      <section class="py-16 bg-gray-100">
        <div class="container mx-auto">
          <h2 class="text-2xl font-semibold mb-6">Nuestros Servicios</h2>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-white p-4 rounded-lg shadow">
              <img src="servicio1.jpg" alt="Servicio 1" class="w-full h-40 object-cover rounded-md">
              <h3 class="text-xl font-semibold mt-4">Servicio 1</h3>
              <p class="text-gray-600">Descripción del servicio 1.</p>
            </div>
            <!-- Repite para más servicios -->
          </div>
        </div>
      </section>

      <!-- Sección de Citas -->
      <section id="appointment" class="py-16 bg-white">
        <div class="container mx-auto text-center">
          <h2 class="text-2xl font-semibold">Solicitar Cita</h2>
          <form class="mt-6">
            <!-- Formulario de cita -->
          </form>
        </div>
      </section>

      <!-- Sección de Blog -->
      <section class="py-16 bg-gray-100">
        <div class="container mx-auto">
          <h2 class="text-2xl font-semibold mb-6">Nuestro Blog</h2>
          <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            <div class="bg-white p-4 rounded-lg shadow">
              <img src="blog1.jpg" alt="Título del Post 1" class="w-full h-40 object-cover rounded-md">
              <h3 class="text-xl font-semibold mt-4">Título del Post 1</h3>
              <p class="text-gray-600">Resumen del Post 1.</p>
            </div>
            <!-- Repite para más entradas del blog -->
          </div>
        </div>
      </section>

      <!-- Sección Sobre Nosotros -->
      <section class="py-16 bg-white">
        <div class="container mx-auto text-center">
          <h2 class="text-2xl font-semibold">Sobre Nosotros</h2>
          <p class="text-gray-600">Información sobre la clínica y su equipo.</p>
        </div>
      </section>

      <!-- Pie de Página -->
      <footer class="bg-gray-900 text-white py-10">
        <div class="container mx-auto">
          <!-- Información de contacto -->
          <!-- Enlaces a redes sociales, política de privacidad, términos y condiciones, etc. -->
          <!-- Horario de atención -->
          <!-- Mapa de ubicación interactivo -->
        </div>
      </footer>
  
        <!-- Resto del código -->
  
      </div>
    </div>
  </template>
  