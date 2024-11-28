<template>
  <div class="landing-page">
    <!-- Centro: Foto da pessoa -->
    <div class="profile">
      <img src="/foto-perfil.jpg" alt="Foto da pessoa" class="profile-photo" />
      <h1 class="name">TEREU</h1>
      
      <!-- Botões pequenos -->
      <div class="action-buttons">
        <button class="contacts" @click="saveProfile">Salvar</button>
        <button class="contacts" @click="makeCall">Ligar</button>
      </div>
      
      <!-- Frase entre aspas -->
      <p class="quote">Faça das suas cicatrizes as suas marcas de vida. 🎭</p>
      
      <!-- Botões de redes sociais e Pix -->
      <div class="social-buttons">
        <button class="btn" @click="goToLink('https://www.instagram.com/tereu_z/')">Instagram</button>
        <button class="btn" @click="goToLink('https://wa.me/5511994433530')">WhatsApp</button>
        <button class="btn" @click="copyPix">Copiar Chave Pix</button>
      </div>
    </div>
      <p class="direitos">Desenvolvido por Giovani Araujo</p>
 </div>
</template>

<script>
export default {
  methods: {
    saveProfile() {
      alert('Perfil salvo com sucesso!');
    },
    makeCall() {
      alert('Chamando...');
    },
    goToLink(url) {
      window.open(url, '_blank');
    },
    copyPix() {
      navigator.clipboard.writeText('');
      alert('Chave Pix copiada!');
    },
  },
};
</script>

<style scoped>

.profile {
  display: flex;
  justify-content: center;
  flex-direction: column;
  align-items: center;
  width: 84vw;
}

.landing-page {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  height: 100vh;
  background-color: #0b225742;
  font-family: Arial, sans-serif;
  border: none;
  border-radius: 1rem;
}

.profile-photo {
  margin-top: -2.4rem;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 120px;
  height: 120px;
  border-radius: 50%;
  margin-bottom: 1rem;
  transition: scale(0) all 0.3s ease-in-out;
  cursor: pointer;
}

.profile-photo:hover {
  transform: scale(1.1);
  box-shadow: 0 0 2rem rgba(9, 9, 132, 0.839);
}

.name {
  color: rgb(255, 255, 255);
  font-size: 24px;
  font-weight: bold;
  margin-top: 0.5rem;
  margin-bottom: 0.5rem;
}

.action-buttons button {
  margin-top: 1rem;
  padding: 0.5rem 1rem;
  font-size: 14px;
  font-family: sans-serif;
  font-weight: 600;
  cursor: pointer;
  margin-top: 2.4rem;
  border: none;
  border-radius: 1rem;
  background: linear-gradient(to right, #ffffff, rgba(8, 84, 156, 0.928));
  cursor: pointer;
}

.contacts {
  margin: 1.6rem;
}

.quote {
  display: flex;
  justify-content: center;
  text-align: center;
  font-family: Comic sans-serif;
  font-size: 16px;
  margin: 1rem 0;
}

.social-buttons button {
  display: block;
  gap: 1rem;
  height: 7vh;
  width: 280px;
  padding: 0.5rem;
  font-size: 16px;
  font-family: sans-serif;
  font-weight: 600;
  cursor: pointer;
  border-radius: 1rem;
  border: none;
  background: linear-gradient(to right, #ffffff, rgba(8, 84, 156, 0.928));
  cursor: pointer;
  transition: all 0.2s ease-in-out;
}

.social-buttons button:hover {
  transform: scale(1.1);
  box-shadow: 0 0 2rem rgba(9, 9, 132, 0.839);  
}

.btn {
  margin-top: 0.8rem;
}

.direitos {
  margin-top: 2rem;
}
</style>
