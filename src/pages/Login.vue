<script></script>

<template>
  <header>
    <img src="../assets/icons/logo-orkut.svg" alt="lOGO" />
    <nav>
      <a href="#">Sobre o Orkut</a>
      <a href="#">Centro de segurança</a>
    </nav>
  </header>
  <main>
    <div class="friends">
      <p>
        Conecta-se aos seus amigos e familiares usando recados e mensagens
        instantâneas
      </p>
    </div>
    <form action="">
      <img src="../assets/images/header.png" alt="logo" />
      <input type="text" placeholder="E-mail" />
      <input type="text" placeholder="Senha" />
      <input type="checkbox" name="" id="" />
      <label for="">Lembrar minha senha</label>
      <input type="submit" value="Entrar na conta" />
      <input type="button" value="Criar uma conta" />
      <a href="#">Esqueci a minha senha</a>
    </form>
  </main>
</template>

<style scoped lang="scss">
@import "../style.scss";
header {
  background-color: var(--white);
  display: flex;
  justify-content: space-around;
  height: 10vh;
  align-items: center;

  nav {
    display: flex;
    width: 30vw;
    justify-content: space-around;

    a {
      color: $dark;
    }
  }
}

main {
  background-color: #d9e6f7;
  height: 90vh;

  .friends {
    background-image: url("../assets/icons/wallpaper.svg");
    height: 60vh;
  }
}
</style>
