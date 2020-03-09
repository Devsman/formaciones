# **React - Redux**

[Cory House](https://hackernoon.com/@housecor)

**Redux** se encarga del control de estados (sesión?) del frontal, en este caso react.

Javascript moderno (ver apuntes de [new-js.md](./new-js.md)).

Plugin para **Visual Studio Code** [**ES7 React/Redux/GraphQL/React-Native snippets**](https://marketplace.visualstudio.com/itemdetails?itemName=dsznajder.es7-react-js-snippets) 

 Why **Redux**?
 - Un Store
 - Repetimiento reducido
 - Isomorphia / Amigable
 - Inmutable Store
 - Recarga en caliente
 - Time-travel debugging
 - Es ligero 


---
## Entorno

Construcción de nuestro propio development environment:
- Node
- Webpack
- Babel
- ESLint
- npm scripts


Pasos
- Install node
- Download visual studio code
- `npm install --global prettier`
- Configurar [prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)  format on save
- npm install
- Webpack

Creación de `webpack.config.js`.
 

---
## React components

Dos discusiones:

- **Class vs Function**

- **Container vs Presentation**


Cuatro caminos para crear componentes en react.

- createClass
~~~
var HelloWorld = React.createClass({
    render : function () {
        return (
            <h1>Hello World</h1>
        );
    }
});
~~~

- ES class
~~~
class HelloWorld extends React.Component {
    constructor(props) {
        super(props);
    }

    render() {
        return (
            <h1>Hello World</h1>
        );
    }
}
~~~

- Function

~~~
function HelloWorld(props) {
    return (
        <h1>Hello World</h1>
    );
}
~~~

- Arrow function
~~~
const HelloWorld = (props) => <h1>Hello World</h1>
~~~


Si necesita un estado en su componente, deberá crear un componente de clase o elevar el estado al componente principal y pasarlo al componente funcional mediante accesorios.

Entonces, ¿por qué debería usar componentes funcionales?
Puede preguntarse por qué debería usar componentes funcionales, si eliminan tantas características agradables. Pero hay algunos beneficios que obtienes al usar componentes funcionales en React:

- Los componentes funcionales son mucho más fáciles de leer y probar porque son funciones simples de JavaScript sin estado o ganchos de ciclo de vida
- Terminas con menos código
- Te ayudan a usar las mejores prácticas . Será más fácil separar el contenedor y los componentes de presentación porque necesita pensar más sobre el estado de su componente si no tiene acceso a setState () en su componente
- El equipo de React mencionó que puede haber un aumento de rendimiento para el componente funcional en futuras versiones de React



Debe usar componentes funcionales si está escribiendo un componente de presentación que no tiene su propio estado o necesita acceder a un enlace de ciclo de vida. De lo contrario, puede pegarse a los componentes de clase o echar un vistazo a la biblioteca recomponer lo que le permite escribir componentes funcionales y mejorar con un estado o ciclo de vida de ganchos con hocs!



Container:
- Poco a ningún marcado
- Pasar datos y acciones hacia abajo
- Saber sobre redux
- A menudo con estado
  
Presentation:
- Casi todo el marcado
- Recibir datos y acciones a través de accesorios
- No hace falta saber sobre Redux
- A menudo no hay estado



"Cuando notas que algunos componentes no usan accesorios que reciben, sino que simplemente los envían hacia abajo ... es un buen momento para introducir algunos componentes del contenedor."

---

Create app foundation
- Create first pages
- Create layout
- Setup navigation



---
# Redux
