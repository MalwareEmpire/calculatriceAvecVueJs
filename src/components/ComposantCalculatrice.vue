<template>
    <div class="calculatrice">
      <h1>Calculatrice</h1>
      <div>
        <input v-model="num1" type="number" placeholder="Entrez le Nombre 1">
        <button @click="addition()">+</button>
        <button @click="soustraction()">-</button>
        <button @click="muliplication()">*</button>
        <button @click="divison()">/</button>
      </div>
      <div>
        <input v-model="num2" type="number" placeholder="Entrez le Nombre 2">
      </div>
      <div>
        <p class="resultat-texte">Résultat : {{ result }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        num1: null,
        num2: null,
        result: null,
      };
    },
    methods: {
      addition() {
        this.result = Number(this.num1) + Number(this.num2);
      },
      soustraction() {
        this.result = Number(this.num1) - Number(this.num2);
      },
      muliplication() {
        this.result = Number(this.num1) * Number(this.num2);
      },
      divison() {
        this.result = Number(this.num1) / Number(this.num2);
      },
    },
  };
  </script>
  
  <style>
  /* Apparence générale */
  .calculatrice {
    max-width: 400px;
    margin: 0 auto;
    padding: 20px;
    background-color: #f5f5f5;
    border-radius: 5px;
    border: 2px solid #ccc; /* Ajout de la bordure */
  }
  
  h1 {
    text-align: center;
    font-size: 55px; 
    font-family: "Kaushan Script", sans-serif;
  }
  
  /* Boutons */
  button {
    display: inline-block;
    width: 50px;
    height: 50px;
    margin: 5px;
    border: none;
    border-radius: 5px;
    background-color: #4caf50;
    color: white;
    font-size: 20px;
    cursor: pointer;
  }
  
  button:hover {
    background-color: #45a049;
  }
  
  /* Zone de saisie */
  input[type="number"] {
    width: 100%;
    padding: 10px;
    margin-bottom: 10px;
    box-sizing: border-box;
    border: 1px solid #ccc;
    border-radius: 5px;
  }
  
  /* Résultat */
  .resultat {
    text-align: center;
    margin-top: 20px;
    font-size: 18px;
  }
  
  .resultat-texte {
    font-size: 30px;
    color: #333;
    font-family: "Kaushan Script", sans-serif;
  }
  </style>