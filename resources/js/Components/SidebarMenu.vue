<template>
    <div class="sidebar">
      <div class="logo">
        <!-- Puedes reemplazar el texto con el logotipo de tu veterinaria -->
        <img src="/logo.png" alt="Logo Veterinaria" />
      </div>
      <ul>
        <li><router-link to="/dashboard"><i class="fas fa-home"></i> Inicio</router-link></li>
        <li><router-link to="/citas"><i class="fas fa-calendar-alt"></i> Mis Citas</router-link></li>
        <li><router-link to="/mascotas"><i class="fas fa-paw"></i> Mis Mascotas</router-link></li>
        <li><router-link to="/servicios"><i class="fas fa-medkit"></i> Servicios Veterinarios</router-link></li>
        <li><router-link to="/historial"><i class="fas fa-file-medical"></i> Historial Médico</router-link></li>
        <li><router-link to="/tienda"><i class="fas fa-shopping-cart"></i> Tienda de Mascotas</router-link></li>
        <li><router-link to="/comunidad"><i class="fas fa-users"></i> Comunidad de Dueños</router-link></li>
        <li><router-link to="/ayuda"><i class="fas fa-question-circle"></i> Ayuda</router-link></li>
      </ul>
    </div>
  </template>
  
  <style scoped>
  /* Estilos del sidebar */
  .sidebar {
    height: 100%;
    width: 250px;
    max-height: 80vh; /* Limitar la altura al 80% del viewport height */
    background-color: #2E3A4F;
    color: white;
    position: fixed;
    top: 50%; /* Centrar verticalmente */
    transform: translateY(-50%); /* Ajustar para centrar verticalmente */
    left: 15px; /* Añadido espacio en el lado izquierdo */
    display: flex;
    flex-direction: column;
    border-radius: 10px; /* Redondear los bordes */
  }
  
  .logo img {
    width: 80%;
    margin: 20px auto;
  }
  
  /* Estilo para los elementos del menú */
  .sidebar ul {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .sidebar li {
    padding: 15px;
    border-bottom: 1px solid #4E5E78;
    display: flex;
    align-items: center;
    transition: background-color 0.3s; /* Agregamos transición para un efecto visual */
  }
  
  .sidebar li i {
    margin-right: 10px;
  }
  
  .sidebar li:last-child {
    border-bottom: none;
  }
  
  /* Cambiamos el color de fondo al pasar el cursor */
  .sidebar li:hover {
    background-color: #4E5E78;
    cursor: pointer; /* Hacemos que aparezca la manito al pasar el cursor */
  }
  
  /* Estilo para el enlace dentro del li */
  .sidebar li a {
    text-decoration: none;
    color: inherit;
  }
  </style>
  