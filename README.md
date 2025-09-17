
# RTOS ARM Cortex-M7 – Mini Noyau Temps Réel

## Description

Ce projet implémente un mini-noyau temps réel préemptif pour microcontrôleur ARM Cortex-M7. Il gère la commutation de tâches, la gestion des priorités, les délais, et propose des primitives de synchronisation (sémaphores, files FIFO).

## Fonctionnalités

- Ordonnanceur à priorités fixes
- Gestion de tâches (création, activation, suspension, réveil)
- Gestion des délais (sleep, wakeup)
- Synchronisation via sémaphores et files FIFO
- Support UART, GPIO, interruptions matérielles
- Affichage terminal (palette de couleurs, positionnement curseur)
- Code modulaire et documenté

## Arborescence

```
src/
	kernel/      # Noyau temps réel
	hwsupport/   # Drivers hardware
	io/          # Entrées/sorties terminal/serial
	main.c       # Exemple d’utilisation
tests/         # Tests unitaires
doc/           # Documentation et images
```

## Compilation

```sh
make
# ou
cmake .
make
```

## Exécution

- Flasher le binaire sur une carte ARM Cortex-M7 compatible.
- Utiliser un terminal série pour interagir avec le système.

## Exemple d’utilisation

```c
void main() {
		usart_init(115200);
		start(tachedefond);
}
```
