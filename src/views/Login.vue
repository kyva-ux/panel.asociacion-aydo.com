<template lang="pug">
.login
  h2 Iniciar sesión
  .box
    .form-control
      label.label Email
      input.input.input-bordered.w-full(type="text" @focus="focused" @blur="focused")
    .form-control
      label.label Password
      input.input.input-bordered.w-full(type="password" @focus="focused" @blur="focused")
    button.btn.btn-accent.mt-4(@click="enviar") Enviar
</template>

<script setup>
const focused = (e) => {
  e.target.classList.toggle("input-accent");
};

const enviar = () => {
  console.log('enviar');
};
</script>

<style scoped>

.login {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
}

.login h2 {
  font-size: 32px;
}

.box {
  margin-top: 24px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-content: center;
  gap: 16px;
  width: 560px;
  background: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 40px;
}
</style>
