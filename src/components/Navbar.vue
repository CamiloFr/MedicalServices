<template>
  <div>
  <b-navbar toggleable="lg" variant="faded" type="light">
    <b-navbar-brand href="#">
      <img src="https://placekitten.com/g/30/30" class="d-inline-block align-top" alt="Kitten">
      Medical Services
    </b-navbar-brand>
    <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>
    <b-collapse id="nav-collapse" is-nav>
     <b-navbar-nav class="ml-auto">
        <b-navbar-nav>
            <b-nav-item href="#">Medicos</b-nav-item>
            <b-nav-item href="#">Usuarios</b-nav-item>
        </b-navbar-nav>
     </b-navbar-nav>
    </b-collapse>
  </b-navbar>
  <b-navbar toggleable="lg" variant="info" type="dark">
    <b-navbar-toggle target="menu2"></b-navbar-toggle>
    <b-collapse id="menu2" class="d-flex justify-content-center" is-nav>
     <b-navbar-nav>
        <b-navbar-nav>
            <b-nav-item href="#">Inicio</b-nav-item>
            <b-nav-item href="#">Servicios</b-nav-item>
            <b-nav-item href="#">Quienes somos</b-nav-item>
        </b-navbar-nav>
     </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</div>
</template>

<script>
export default {
  name: 'Index',
}
</script>
