# Getting Started with Create React App


{Pequeña descripción de componentes}

¿Componentes de clase o funcionales?

¿Qué es un componente de clase?
Un componente de clase es una clase de javascript que extiende la clase Component de React.
class Biology extends React.Component
Este nos permite guardar su estado y controlar lo que ocurre durante su ciclo de vida, exponiéndonos métodos como componentDidMount o componentWillUnmount.

¿Cómo se ve un componente de clase?
class Biology extends React.Component {
    constructor(props){
        super(props)
        this.state = {
            professor: "Franco Cuarterolo"
            students: props.numberOfStudents
        }
    }

    componentDidMount(){
        this.startAssignment()
    }

    componentWillUnmount(){
        this.finishAssignment()
    }

    render(){
        return(
        <div> Biology, Professor: {this.state.professor} </div>
        )
    }

}
Qué es un componente funcional?


Un componente funcional es una función que recibe el objeto Props y retorna un ReactNode (un ReactNode puede ser un elemento html, un string, un booleano, entre otros tipos de datos.).
const Biology = (props) => { return(<ReactNode />) }
Estas funciones solo reciben y retornan, por eso tienen que utilizar React Hooks (useState para el estado, useEffect para los ciclos de vida) para imitar las cualidades de un componente de clase.

¿Cómo se ve un componente funcional?
const Biology = (props) => {
    const [professor, setProfessor] = React.useState("Franco Cuarterolo");
    const [students, setStudents] = React.useState(props.numberOfStudents);

    React.useEffect(()=>{
            startAssignment()
            return () => {
                finishAssignment()
            }
        })

    return <div> Biology, Professor: {professor} </div>
}
¿Por qué usar funciones por encima de clases?
El frontend está experimentando una fuerte influencia de los lenguajes de programación funcionales, y esto nos lleva a integrar practicas del paradigma funcional en nuestro día a día.
Ayuda a unificar criterios, donde todos los componentes tienen la misma estructura.
Nos ahorra entender un concepto que está en camino al desuso en Javascript (Clases), aligerando la curva de aprendizaje
Hacer testing de un componente funcional suele ser más sencillo.
Suelen requerir menos lineas de código haciendolo más facil de entender.




This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
# Cards-Clase-Componentes
