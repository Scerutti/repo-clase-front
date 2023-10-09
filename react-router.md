# React Router con Vite - Guía Rápida

## ¿Qué es React Router?

React Router es una biblioteca que se utiliza en aplicaciones web construidas con React para gestionar la navegación y el enrutamiento de manera efectiva. Permite crear aplicaciones de una sola página (SPA) donde el contenido se actualiza dinámicamente sin necesidad de cargar páginas completas desde el servidor.

## React Router DOM

`react-router-dom` es una parte específica de React Router diseñada para aplicaciones web. Proporciona una serie de componentes React que permiten definir rutas y manejar la navegación en una aplicación web. Algunos de los componentes más importantes de React Router DOM son:

- **BrowserRouter**: Este componente envuelve la aplicación y se encarga de mantener el historial del navegador sincronizado con la aplicación. Debe utilizarse una vez en la parte superior de la jerarquía de componentes.

- **Route**: El componente `<Route>` se utiliza para definir cómo se renderizará un componente cuando la URL coincida con una determinada ruta. Puedes usar la prop `path` para especificar la ruta y `component` o `render` para determinar qué componente se renderizará.

- **Link**: El componente `<Link>` se utiliza para crear enlaces de navegación en lugar de los tradicionales enlaces `<a>`. Cuando un usuario hace clic en un enlace `<Link>`, la aplicación se actualiza sin recargar la página completa, lo que permite una navegación suave en una SPA.

- **Switch**: El componente `<Switch>` se utiliza para renderizar solo la primera `<Route>` que coincida con la URL actual. Esto es útil cuando se tienen múltiples rutas y deseas asegurarte de que solo se renderice una de ellas.

## Navegación en React Router

La navegación en React Router se basa en la manipulación del historial del navegador. Cuando un usuario hace clic en un enlace `<Link>`, React Router actualiza la URL del navegador y, al mismo tiempo, muestra el componente asociado a la ruta correspondiente. Esto permite que la aplicación se comunique con el historial del navegador y funcione como una SPA sin necesidad de recargar páginas completas.

En resumen, React Router es una poderosa herramienta que permite crear aplicaciones web con navegación fluida y dinámica. Permite definir rutas, gestionar la navegación y mantener una experiencia de usuario sin problemas en aplicaciones de una sola página construidas con React.
