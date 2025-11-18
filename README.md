# POO – Programação Orientada a Objetos (SENAI)

Atividade sobre POO (Programação Orientada a Objetos)

Aluno: Antony Miguel Da Paz Fonseca

Escola Técnica: Senai de Areias

## O que é Programação Orientada a Objetos?

A Programação Orientada a Objetos (POO) é um paradigma de programação que organiza o código ao redor de objetos. É uma forma de programar que simplifica programas complexos, dividindo-os em unidades menores, que são os objetos
.

## Por que a POO surgiu e qual problema ela resolve?

A POO é um paradigma de programação que organiza o código ao redor de objetos. O principal intuito de sua criação foi o de aproximar o manuseio das estruturas de um programa ao manuseio das coisas do mundo real.

 A POO resolve o problema de lidar com a complexidade de programas grandes e com o gerenciamento desorganizado de dados, característico do modelo estruturado

---

## Os Quatro Pilares da POO
### 1. **Abstração**

A abstração consiste em representar um objeto real de forma simplificada, exibindo apenas o que é necessário para o uso, escondendo detalhes internos.

#### Exemplo em Python:

```python
class Carro:
    def __init__(self, modelo):
        self.modelo = modelo
        self.velocidade = 0

    def acelerar(self):
        pass  # Código para acelerar o carro

    def frear(self):
        pass  # Código para frear o carro

    def acenderFarol(self):
        pass  # Código para acender o farol
```

---

### 2. **Encapsulamento**

O encapsulamento protege dados internos de um objeto, permitindo que sejam acessados apenas por métodos específicos. Assim, evita-se modificações indevidas e aumenta-se a segurança do código.

#### Exemplo em Python:

```python
class Carro:
    def __init__(self, modelo, mecanismoAceleracao):
        self.__modelo = modelo
        self.__velocidade = 0
        self.__mecanismoAceleracao = mecanismoAceleracao
        self.__cor = "Prata"

    def acelerar(self):
        self.__mecanismoAceleracao.acelerar()

    def frear(self):
        pass

    def acenderFarol(self):
        pass

    def getVelocidade(self):
        return self.__velocidade

    def __setVelocidade(self, valor):
        self.__velocidade = valor

    def getModelo(self):
        return self.__modelo

    def getCor(self):
        return self.__cor

    def setCor(self, cor):
        self.__cor = cor
```

---

### 3. **Herança**

A herança permite que uma classe receba atributos e métodos de outra, evitando repetição de código e facilitando a ampliação de funcionalidades.

#### Exemplo em Python:

```python
class HondaFit(Carro):
    def __init__(self, mecanismoAceleracao):
        modelo = "Honda Fit"
        super().__init__(modelo, mecanismoAceleracao)
```

---

### 4. **Polimorfismo**

O polimorfismo permite que classes diferentes tenham métodos com o mesmo nome, mas comportamentos distintos. Isso deixa o código flexível e genérico.

#### Exemplo em Python:

```python
class Moto:
    def __init__(self, modelo, mecanismo):
        self.modelo = modelo
        self.mecanismo = mecanismo

    def acelerar(self):
        self.mecanismo.acelerar()

    def acenderFarol(self):
        print("Farol da moto aceso!")

class Carro:
    def __init__(self, modelo, mecanismo):
        self.modelo = modelo
        self.mecanismo = mecanismo

    def acelerar(self):
        self.mecanismo.acelerar()

    def acenderFarol(self):
        print("Farol do carro aceso!")

# Demonstração do polimorfismo
moto = Moto("Yamaha XPTO-100", MecanismoDeAceleracaoDeMotos())
carro = Carro("Honda Fit", MecanismoDeAceleracaoDeCarros())

listaAutomoveis = [moto, carro]

for automovel in listaAutomoveis:
    automovel.acelerar()
    automovel.acenderFarol()
```

---

## Conclusão

A Programação Orientada a Objetos é essencial para o desenvolvimento moderno, permitindo sistemas mais organizados, reutilizáveis e fáceis de dar manutenção. Ao criar este relatório, foi possível reforçar a importância dos quatro pilares da POO e compreender como eles tornam o código mais estruturado e eficiente.
