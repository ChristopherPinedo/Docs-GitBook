# 3.2. Composicion de componentes

* La Composición de componentes indica que cada componente debe darnos mucha libertad para elegir donde y como usarlo
* Cada componente debe realizar una tarea en específica, pero no debe de decirnos como usar esa solución que nos brinda, debe de ser flexible al momento de utilizarlo
  * Nos permitirá
    1. Tener componentes mucho más fáciles de integrar al resto de componentes
    2. Nos facilitará reutilizar o hacer cambios en nuestros componentes

**Ejemplo**

Una solución para renderizar una tarea podría ser este componente

```jsx
const App = () => (
	<TodoList todos={todos} />
);
```

```jsx
const TodoList = ({todos}) => (
	<section>
		{todos.map(todo => (
			<TodoItem {...todo} />
		))}
	</section>
)
```

Existe otra forma de realizar esta tarea, y es que el componente App tenga también la tarea de renderizar cada tarea, esta manera nos dará mayor flexibilidad con el componente de TodoList

```jsx
const TodoList = ({children}) => (
	<section>
		{children}
	</section>
)
```

```jsx
const App = () => (
	<TodoList>
		{todos.map(todo => (
			<TodoItem {...todo} />
		))}
	</TodoList>
);
```
