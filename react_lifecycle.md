## Estados en React
Temas:

* El estado es una característica clave en React que permite a los componentes mantener y gestionar datos que pueden cambiar a lo largo del tiempo.

* this.state en componentes de clase.

* La función setState() para actualizar el estado y hacer que React vuelva a renderizar el componente.

Ejemplo: 
```jsx
import React, { Component } from 'react';

class Contador extends Component {
  constructor(props) {
    super(props);
    this.state = { count: 0 };
  }

  incrementar = () => {
    this.setState({ count: this.state.count + 1 });
  }

  render() {
    return (
      <div>
        <p>Conteo: {this.state.count}</p>
        <button onClick={this.incrementar}>Incrementar</button>
      </div>
    );
  }
}

export default Contador;
```

-----

## Ciclo de vida en componentes de clase

Temas:

* Los componentes de clase tienen un ciclo de vida que consta de diferentes etapas, como montaje, actualización y desmontaje.

* El método componentDidMount() se utiliza para realizar acciones después de que el componente se monta en el DOM.

Ejemplo:

```jsx
import React, { Component } from 'react';

class DatosDesdeAPI extends Component {
  constructor(props) {
    super(props);
    this.state = { datos: null };
  }

  componentDidMount() {
    // Realizar una solicitud a una API y actualizar el estado con los datos recibidos
  }

  render() {
    return (
      <div>
        {this.state.datos ? (
          <p>Datos desde la API: {this.state.datos}</p>
        ) : (
          <p>Cargando datos...</p>
        )}
      </div>
    );
  }
}

export default DatosDesdeAPI;
```

---

## Introducción a Hooks

Temas:

* Los hooks son una característica introducida en React para permitir el uso de estados y otras características en componentes funcionales.

* useState es un hook que permite añadir estados a componentes funcionales.

Ejemplo:

```jsx
import React, { useState } from 'react';

function ContadorFuncional() {
  const [count, setCount] = useState(0);

  const incrementar = () => {
    setCount(count + 1);
  }

  return (
    <div>
      <p>Conteo: {count}</p>
      <button onClick={incrementar}>Incrementar</button>
    </div>
  );
}

export default ContadorFuncional;
```

---

## Introducción a Promesas y (fetch y/o axios)

Temas:

* Promesas en JavaScript: concepto y uso.
* fetch: una función nativa para realizar solicitudes HTTP en JavaScript.
* axios: libreria externa para realizar solicitudes http
* Cómo usar fetch o axios para obtener datos de una API en una aplicación React.

Ejemplo:

```jsx
import React, { useEffect, useState } from 'react';

function FetchData() {
  const [data, setData] = useState(null);

  useEffect(() => {
    // Realizar una solicitud GET a una API usando fetch
    fetch('https://api.example.com/data')
      .then(response => response.json())
      .then(data => setData(data))
      .catch(error => console.error('Error:', error));
  }, []);

  return (
    <div>
      {data ? (
        <p>Datos desde la API: {data}</p>
      ) : (
        <p>Cargando datos...</p>
      )}
    </div>
  );
}

export default FetchData;
```

---

##  Introducción a useEffect

Temas:

* useEffect en componentes funcionales: su función y cómo se usa.

* Ejemplos de uso de useEffect para realizar efectos secundarios, como suscripciones a eventos o solicitudes a una API.

Ejemplo:

```jsx
import React, { useEffect, useState } from 'react';

function EffectExample() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    // Este efecto se ejecutará cuando el componente se monte y cada vez que 'count' cambie.
    document.title = `Conteo: ${count}`;

    // También podrías realizar otras operaciones aquí, como suscripciones a eventos o solicitudes HTTP.
  }, [count]);

  return (
    <div>
      <p>Conteo: {count}</p>
      <button onClick={() => setCount(count + 1)}>Incrementar</button>
    </div>
  );
}

export default EffectExample;
```
---