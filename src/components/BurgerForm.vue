<template>
  <div>
    <form id="burguer-form">
        <div class="input-container">
          <label for="name">Nome do cliente</label>
          <input type="text" id="name" name="name" v-model="name" placeholder="Digite seu nome">
        </div>
      <div class="input-container">
          <label for="bread">Escolha o pão:</label>
          <select name="bread" v-model="pao">
            <option value="normal">Normal</option>
            <option value="integral">Integral</option>
          </select>
      </div>
      <div class="input-container">
          <label for="meat">Selecione o tipo de carne:</label>
          <select name="meat" v-model="meat">
            <option value="maminha">maminha</option>
            <option value="mignon">mignon</option>
          </select>
      </div>
      <div id="optional-container" class="input-container">
          <label class="optional-title" for="optional">Selecione os opcionais:</label>
          <div class="checkbox-container">
            <input type="checkbox" name="optional" v-model="optional" value="salame">
            <input type="checkbox" name="optional" v-model="optional" value="salame">
            <input type="checkbox" name="optional" v-model="optional" value="salame">
            <span>Salame</span>
          </div>
      </div>
      <input type="submit" class="submit-btn" value="Crie meu burger">
    </form>
  </div>
</template>
<script>
export default {
  name: 'BurgerForm'
}

</script>
<style scoped>
  #burguer-form {
    max-width: 400px;
    margin: 0 auto;

  }

  .input-container{
    display: flex;
    flex-direction: column;
    margin-bottom: 20px;
  }

  label {
    font-weight: bold;
    margin-bottom: 15px;
    color: #222;
    padding: 5px 10px;
    border-left: 4px solid #FCBA03;
  }

  input, select {
    padding: 5px 10px;
    width: 300px;
  }

  #optional-container {
    flex-direction: row;
    flex-wrap: wrap;
  }

  optional-title {
    width: 100%;
  }

  #checkbox-container {
    display: flex;
    align-itens: flex-start;
    width: 50%;
    margin-bottom: 20px;
  }

  .checkbox-container span, .checkbox-container input {
    width: auto;
  }

  .checkbox-container span {
    margin-left: 6px;
    font-weight: bold;
  }

  .submit-btn {
    background-color: #222;
    color: #FCBA03;
    font-weight: bold;
    border: 2px solid #222;
    padding: 10px;
    margin: 0 auto;
    cursor: pointer;
    transition: 3s;
  }

  .submit-btn:hover {
    background-color: transparent;
    color: #222222;
  }
  </style>