# 3.4. Render props & Render functions

Antes de estudiar las render props debes conocer la composición de componentes. Las renders props vienen a ayudar a hacer una composición de componentes más limpia. Seguimos con todas las ventajas de usar composición de componentes.

\
A partir de ahora podemos decir que tenemos 2 tipos de props: las props normales que reciben un valor o variable y por otro lado tenemos las props que contienen una función.&#x20;

Estas que contienen una función son las que nos interesan.\
Esta función devuelve un componente o un elemento que pudiera tener anidados más elementos y componentes.\
La sintaxis es la siguiente:

```
<MyHeader 
	render={ () => <myLogo type={ type } /> } 
/> 
```

La propiedad render(la cual puede tener cualquier otro nombre) es nuestra render prop, porque contiene una función que al ser llamada devuelve un componente. Entonces cumple todas las condiciones y solo falta llamarla desde el componente que la contiene:

```
function MyHeader( props ){
	return (
	<header className="header__styles">
		{ props.render() }
	</header>
	)
} 
```

#### Entonces podemos interpretar que las render props le dicen al componentes que renderizan(cual va a ser su contenido)

Otra forma de hacer esto es con las render functions y lo que cambia es que se declaran dentro del componente:

```
<MyHeader>
	{ () => <myLogo type={ type } /> } 
</MyHeader>
```

Y para acceder a lo que está dentro del componentes simplemente usamos props.children:

```
function MyHeader( props ){
	return (
	<header className="header__styles">
		{ props.children }
	</header>
	)
} 
```

Es prácticamente lo que hicimos con la composición de componentes y la propiedad children.
