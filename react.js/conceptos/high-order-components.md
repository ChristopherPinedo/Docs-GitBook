# 3.5. High Order Components

* Son funciones que retornan otras funciones aplicando el concepto funcional `currying`

```jsx
function highOrderFunction(var1) {
	return function returnFunction(var2) {
		return var1 + var2;
	}
}

const withSum1 = highOrderFunction(1);
const sumTotal = withSum1(2);

// 3
```

Debido a que los componentes son funciones podemos también aplicar este concepto

```jsx
// Caso base

function Componente(props){
	return <p>...</p>
}

function highOrderComponent() {
	return function Componente(props) {
		return <p>...</p>
	}
}
```

```jsx
function highOrderComponent(WrappedComponent) {
	return function Componente(props) {
		return (
			<WrappedComponent
				{...algoEspecial}
				{...props}
			/>
		);
	}
}
```

* De esta manera estamos personalizando varios aspectos del componente deseado, como:
  * Los parámetros de las funciones nos permiten configurar el componente que envuelve, las props
  * Podemos reutilizar los HOC

**Ejemplos**

```jsx
function withApi(WrappedComponent) {
	const apiData = fetchApi('https://api.com');
	
	return function WrappedComponentWithApi(props) {
		if (apidData.loading) return <p>Loading</p>;
		return(
			<WrapperdComponent data={apiData.json} />
		);
	}
}
```

* Antes de retornar el componente en sí, hace una petición y entrega al componente esa información
* Además que podemos personalizar el estado de carga

```jsx
function TodoBox(props) {
	return (
		<p>
			Tu nombre es {props.data.name}
		</p>
	);
}

const TodoBoxWithApi = withApi(TodoBox);
```

![](<../../.gitbook/assets/image (3).png>)

* También podemos agregar más “capas” para tener más personalizaciones como por ejemplo

```jsx
function withApi(apiUrl){
	return function withApiUrl(WrappedComponent) {
		const apiData = fetchApi(apiUrl);
		
		return function WrappedComponentWithApi(props) {
			if (apidData.loading) return <p>Loading</p>;
			return(
				<WrapperdComponent data={apiData.json} />
			);
		}
	}
}
```

```jsx
function TodoBox(props) {
	return (
		<p>
			Tu nombre es {props.data.name}
		</p>
	);
}

const TodoBoxWithApi = withApi('https://api.com')(TodoBox);
```
