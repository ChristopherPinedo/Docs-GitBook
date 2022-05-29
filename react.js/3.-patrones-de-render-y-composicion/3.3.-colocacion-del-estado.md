# 3.3. Colocacion del estado

**¿Dónde va tu estado?**

* **Máxima cercanía a la relevancia**
  * El estado ira según al área donde se aplique el mismo
* **Stateful vs. stateless**
  * Se refiere a no tener revuelo entre componentes que manejan lógica y estado con los componentes que solo renderizan elementos

Se puede usar ambos principios siempre si los entendemos muy bien

Pensar en lo más grande y poco a poco ir a lo más especifico

**¿Necesitas React Context?**

Al usar composición de componentes puede ser una alternativa interesante en caso de que el árbol de componentes no sea demasiado profundo.

**Ventajas**

* No será necesario pasar props por cada componente intermedio entre donde se encuentre el dato inicialmente hasta su destino
* Podrás entender la aplicación con entender lo que está pasando en un archivo

**Ejemplo**

```jsx
const App = () => {
	const [state, setState] = useState();
	return (
		<>
			<TodoHeader>
				<TodoCounter />
				<TodoSearch onSearch={setState} />
			</TodoHeader>
			<TodoList>
				{state.todos.map(todo => <TodoItem {...todo} {...state} />)}
			</TodoList>
		</>
	);
}
```

Puedes observar que el componente se puede comunicar sin mucha complicación directamente con sus componentes hijos, nietos o incluso bisnietos.

* De esta manera se está reduciendo la complejidad de los componentes intermedios
* Además que se puede observar legibilidad con solo ver un archivo
* Pero esta manera es insostenible en el caso que el árbol de componentes sea muy grande, pero aún se puede utilizar composición de componentes al utilizar React context
