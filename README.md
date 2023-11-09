# tela-login


// Definição do construtor Carro
function Carro(marca, modelo, peso, cor, qtdPortas, velocidadeMaxima) {
    this.marca = marca;
    this.modelo = modelo;
    this.peso = peso;
    this.cor = cor;
    this.qtdPortas = qtdPortas;
    this.velocidade = 0;
    this.velocidadeMaxima = velocidadeMaxima;
    this.status = "desligado";

    this.ligar = function() {
        this.velocidade = 0;
        this.status = "ligado";
        console.log("Carro ligado. Velocidade: " + this.velocidade + ", Status: " + this.status);
    };

    this.acelerar = function() {
        if (this.velocidade + 10 <= this.velocidadeMaxima) {
            this.velocidade += 10;
            console.log("Acelerando. Nova velocidade: " + this.velocidade);
        } else {
            console.log("Velocidade máxima atingida. Não é possível acelerar mais.");
        }
    };

    this.frear = function() {
        if (this.velocidade >= 10) {
            this.velocidade -= 10;
            console.log("Freando. Nova velocidade: " + this.velocidade);
        } else {
            this.velocidade = 0;
            console.log("Carro parado.");
        }
    };

    this.desligar = function() {
        this.velocidade = 0;
        this.status = "desligado";
        console.log("Carro desligado. Velocidade: " + this.velocidade + ", Status: " + this.status);
    };
}

// Criando uma instância de Carro
var meuCarro = new Carro("Toyota", "Lexus", 1680, "Branco", 4, 220);

// Testando os métodos
meuCarro.ligar();
meuCarro.acelerar();
meuCarro.acelerar();
meuCarro.acelerar();
meuCarro.frear();
meuCarro.desligar();
