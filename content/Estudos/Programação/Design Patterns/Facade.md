---
title: Facade
publish: true
---

# Facade
## O que é?
Utiliza uma interface para abstrair complexidade de outras funções.
Ex: Uma pessoa não precisa saber mexer na parte elétrica da casa para ligar uma luz
``` ts
class EletricalSystem(){
	setVoltage(v: number){}
	turnOn(){}
	turnOff(){}
}
class House(){
	//adiciona sistema como dep
	private electrical = new ElectricalSystem();
	turnOnSystems(){
		electrical.turnOn();
	}
}
const house = new House();
house.turnOnSystems();
```