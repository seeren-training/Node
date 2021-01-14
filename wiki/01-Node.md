# Node

*  🔖 **Platform**
*  🔖 **Principe**

___

## 📑 Platform

Node.js est une plateforme logicielle libre en JavaScript orientée vers les applications réseau événementielles hautement concurrentes qui doivent pouvoir monter en charge. Elle utilise la machine virtuelle V8, la librairie libuv pour sa boucle d'évènements, et implémente sous licence MIT les spécifications CommonJS.

![image](https://raw.githubusercontent.com/seeren-training/Node/master/wiki/resources/node.png)

### 🏷️ **CommonJS**

CommonJS est un projet de développement d'une API pour écrire des programmes JavaScript s'exécutant ailleurs que dans un navigateur Web, et portables sur les différents interpréteurs et environnements d'exécution implémentant CommonJS.

#### Import

```js
const package = require('package');
```

#### Export

```js
const feature = () => { };

module.exports = feature;
```

### 🏷️ **Execution**

Exécuter des instructions.

```bash
node
> const fn = () => true
undefined
> fn()
true
```

Exécuter un script.

```bash
node ./my-script
```
___

## 📑 Principe

### 🏷️ **Compilation**

![image](https://raw.githubusercontent.com/seeren-training/Node/master/wiki/resources/v8.jpg)

V8 est le moteur d'exécution JavaScript qui a été initialement conçu pour Google Chrome. Il a ensuite été open-source par Google en 2008. Rédigé en C ++, V8 compile le code source JavaScript en code machine natif au moment de l'exécution. Depuis 2016, il inclut également Ignition, un interpréteur de bytecode.

### 🏷️ **Thread**

![image](https://raw.githubusercontent.com/seeren-training/Node/master/wiki/resources/thread.png)

Node.js fonctionne sur une boucle d'événement à un seul thread, en utilisant des appels non bloquants, ce qui lui permet de prendre en charge des dizaines de milliers de connexions simultanées sans encourir le coût du changement de contexte de thread. La conception du partage d'un seul thread entre toutes les demandes qui utilisent le modèle d'observateur est destinée à la création d'applications hautement simultanées, où toute fonction exécutant doit utiliser un rappel. Pour accueillir la boucle d'événements à thread unique, Node.js utilise la bibliothèque `libuv` - qui, à son tour, utilise un pool de threads de taille fixe qui gère certaines des opérations asynchrones non bloquantes.