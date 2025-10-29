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
      <div class="check">
        <input type="checkbox" name="" id="" />
        <label for="">Lembrar minha senha</label>
      </div>
      <input class="entrar" type="submit" value="Entrar na conta" />
      <input class="criar" type="button" value="Criar uma conta" />
      <a class="esqueceu" href="#">Esqueci a minha senha</a>
    </form>
  </main>
</template>

<style scoped lang="scss">
@import "../style.scss";

// 🔧 Mixins
@mixin flex-center($direction: row, $justify: center, $align: center, $gap: 0) {
  display: flex;
  flex-direction: $direction;
  justify-content: $justify;
  align-items: $align;
  gap: $gap;
}

@mixin input-style {
  background-color: #eff3f8;
  border: none;
  border-radius: 8px;
  padding: 10px;
  margin: 8px 0;
  width: 100%;
  font-size: 14px;

  &::placeholder {
    color: #868686;
  }
}

// 🔹 Header
header {
  background-color: var(--white);
  @include flex-center(row, space-around, center);
  height: 10vh;

  nav {
    @include flex-center(row, space-around);
    width: 30vw;

    a {
      color: $dark;
      text-decoration: none;
      font-weight: 500;
    }
  }
}

// 🔹 Main
main {
  background-color: #d9e6f7;
  height: 90vh;
  @include flex-center(row, center, center, 30px);

  .friends {
    background-image: url("../assets/icons/wallpaper.svg");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    width: 45vw;
    height: 60vh;
    border-radius: 16px;
    color: $white;
    filter: brightness(80%);
    @include flex-center(column, flex-end);
    text-align: center;
    padding: 20px;
    padding-bottom: 30px;
   

    p {
      //padding-bottom: 30px;
      font-size: 16px;
      line-height: 1.4;
    }
  }

  // 🔹 Formulário
  form {
    @include flex-center(column);
    background-color: $white;
    width: 25vw;
    height: 60vh;
    border-radius: 16px;
    padding: 20px;
    box-shadow: 0 4px 10px rgba(0, 0, 0, 0.05);

    img {
      width: 50%;
      margin: 0 auto 10px;
    }

    input[type="text"],
    input[type="password"] {
      @include input-style;
    }

    .check {
      @include flex-center(row, flex-start, center, 8px);
      width: 80%;
      margin: 8px 0;
      font-size: 12px;
      color: #555;

      input[type="checkbox"] {
        width: 14px;
        height: 14px;
        cursor: pointer;
      }
      
      label {
        cursor: pointer;
      }
    }

    .entrar {
      @include input-style;
      background-color: $brand-color;
      color: $white;
      font-weight: 600;
      cursor: pointer;
      transition: 0.3s;

      &:hover {
        filter: brightness(90%);
      }
    }

    .criar {
      @include input-style;
      color: $brand-color;
      font-weight: 600;
      cursor: pointer;
      background-color: transparent;
      border: 1px solid $brand-color;
      transition: 0.3s;

      &:hover {
        background-color: $brand-color;
        color: $white;
      }
    }

    .esqueceu {
      font-weight: 400;
      color: $brand-color;
      font-size: 12px;
      margin-top: 5px;
      text-align: center;
      text-decoration: none;
    }
  }
}

</style>
