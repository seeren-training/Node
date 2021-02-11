# Express

*  🔖 **Installation**
*  🔖 **Routing**
*  🔖 **MySQL**

Nous observerons l'utilisation de Node.js en créant une api avec le framework express.

___

## 📑 [Installation](https://expressjs.com/)

![image](https://raw.githubusercontent.com/seeren-training/Node/master/wiki/resources/express.png)

Le générateur d'application est utile pour norer le projet.

```bash
npm install express express-generator
```

### 🏷️ **[Projet](https://www.npmjs.com/package/express-generator)**

Notre objectif est de router des endpoints, nous demandons la création d'un projet sans vue.

```bash
$ npx express --git --no-view my-project
```

Après avoir changé de répertoire nous devons installer les packages.

```bash
cd my-project
npm install
```

A chaque modification de fichier il faut redémarrer le serveur ce qui est très contraignant, nous alons alors installer un package pour résoudre ce problème.

```bash
npm install nodemon
```

Nous modifions le script attaché à start.

```json
"scripts": {
  "start": "nodemon ./bin/www"
},
```

L'application est disponible à l'adresse: http://localhost:3000/.

___

👨🏻‍💻 Manipulation

Créer un projet et démarrer votre application

___

## 📑 [Routing](https://expressjs.com/fr/starter/basic-routing.html)

Vous pouvez associer un path à un bloc d'instructions en fonction de méthodes.

```json
router.get('/', function(req, res, next) {});
```

___

👨🏻‍💻 Manipulation

Initialiser des routes CRUD pour un endpoint.
___


### 🏷️ **Response**

#### **Status**

```js
res.status(200);
```
___

👨🏻‍💻 Manipulation

Renvoyez le status code adapté en fonction de la méthode
___


#### **Headers**

```js
res.setHeader(
    "Content-Type",
    "application/json; charset=utf-8"
);
```
___

👨🏻‍💻 Manipulation

Renvoyez les entêtes d'acceptation des origines, des entêtes et des méthodes
___

#### **Body**

```js
res.send({foo: "Foo"});
```

___

👨🏻‍💻 Manipulation

Renvoyez un model ou une collection de models en fonction de la méthode.
___

### 🏷️ **Request**

#### **Headers**

* Récupérer les headers

```js
const headers = req.headers;
```

* Récupérer un header

```js
const host = req.header("host");
```

___

👨🏻‍💻 Manipulation

Envoyez une entête Unsupported Media Type si le type de contenu n'est pas json.
___

#### **Body**

```js
const obj = req.body;
```

___

👨🏻‍💻 Manipulation

Envoyez les entêtes adaptés si le contenu attendu pour chaque méthode n'est pas la bonne.
___

## 📑 [MySQL](https://expressjs.com/fr/guide/database-integration.html#mysql)

Vous pouvez utiliser diférents drivers de stockage.

```bash
npm install mysql
```
___

👨🏻‍💻 Manipulation

Créez une table pour votre model

___

### 🏷️ **[Connection](https://www.npmjs.com/package/mysql#establishing-connections)**

```js
const connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'dbuser',
  password : 's3kreee7'
});
connection.connect();
```
___

👨🏻‍💻 Manipulation

Isolez votre connection

___

### 🏷️ **[Queries](https://www.npmjs.com/package/mysql#performing-queries)**

___

👨🏻‍💻 Manipulation

Après vous être documenté sur le SELECT, INSERT, UPDATE, DELETE: complétez votre CRUD

___

Nous avons pu observer que Express comme son som l'indique nous offre une solution pour développer des API's par exemple efficace et simple