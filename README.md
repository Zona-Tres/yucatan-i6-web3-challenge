# Reto Web3 Yucatán i6

Bienvenido a este reto donde desplegarás tu primer canister en la red de Internet Computer!

---
## Información general

### ¿Qué es Internet Computer?

Es un protocolo de **Blockchain** respaldado por la fundación **DFINITY** que permite que servicios Web3 corran 100% on-chain, proveyendo la única plataforma donde los desarrolladores pueden construir aplicaciones completamente descentralizadas.

Más información en la [documentación oficial](https://internetcomputer.org/docs/current/home) de ICP.

### ¿Qué es un Canister?

Un canister es una unidad computacional en ICP que agrupa tanto código como estado. Es similar a un **contrato inteligente** y puede desplegarse como tal en ICP. Los canisters pueden comunicarse entre sí a través de mensajes asíncronos y su ejecución se realiza de forma aislada, lo que permite mayores niveles de ejecución concurrente.

Los canisters son similares a los **contenedores** en otros ambientes en el sentido de que se despliegan como una unidad de software que contiene código compilado y dependencias para una aplicación o servicio. Sin embargo, a diferencia de un contenedor, un canister también almacena información sobre el estado actual del software, persistiendo un registro de los cambios de estado resultantes de la llamada a sus funciones.

Los canisters pueden desarrollarse en diversos lenguajes, como Rust, JavaScript, Python y TypeScript. También existe un SDK para **Motoko**, un lenguaje específico para el desarrollo de canisters en Internet Computer centrado en la programación en un entorno asíncrono distribuido.

Más información en la [documentación oficial](https://internetcomputer.org/docs/current/tutorials/developer-journey/level-0/ic-overview#canisters-and-smart-contracts) de ICP.

### ¿Qué es Motoko?

Motoko es un lenguaje de programación moderno y de propósito general diseñado específicamente para escribir canisters dentro del Protocolo de Internet Computer (ICP). Fue desarrollado por la Fundación DFINITY, dirigida por el cocreador de WebAssembly Andreas Rossberg.

Motoko está diseñado para ser accesible para los programadores que tienen cierta familiaridad básica con la programación orientada a objetos o la programación funcional en JavaScript u otros lenguajes de programación modernos, como Rust, Swift, TypeScript, C# o Java.

Más información en la [documentación oficial](https://support.dfinity.org/hc/en-us/articles/360057132652-What-is-Motoko) de ICP.

### ¿Qué es un Motoko Playground?

Motoko Playground es un entorno de desarrollo basado en navegador para ICP. Permite a los desarrolladores construir, desplegar y probar canisters directamente **dentro de un navegador** web. El playground es particularmente útil para el despliegue temporal y la prueba de canisters, ya que permite realizar pruebas rápidas sin necesidad de configurar parámetros adicionales.

Más información en la [documentación oficial](https://internetcomputer.org/docs/current/developer-docs/developer-tools/ide/playground) de ICP.

---

## Ejecutando el reto

En esta sección verás como ejecutar el paso a paso de este **Reto Web3 Yucatán i6**.

### Importando este proyecto en Motoko Playground

Abre el Motoko Playground siguiendo [este link](https://m7sm4-2iaaa-aaaab-qabra-cai.raw.ic0.app/) o navegando a la siguiente dirección:

```
https://m7sm4-2iaaa-aaaab-qabra-cai.raw.ic0.app/
```

Después haz clic en **Import from GitHub**. Deberás llenar los datos de este repositorio, los cuáles quedarían de esta manera:

![Screenshot 2024-05-15 203418](https://github.com/Zona-Tres/yucatan-i6-web3-challenge/assets/54418646/71a0fbef-a522-4899-92ef-30a46391314a)

Los datos son:
* **Github repo**: Zona-Tres/yucatan-i6-web3-challenge
* **Branch**: master
* **Directory**: src/yucatan-i6-web3-challenge-backend

Finalmente haz clic en **Import**. Deberás de ver que el editor se llenó de código. Este código es nuestro **canister** programado en **Motoko**.

Para probarlo y desplegarlo a la red de Internet Computer, haz clic en **Deploy**:

![Screenshot 2024-05-15 203834](https://github.com/Zona-Tres/yucatan-i6-web3-challenge/assets/54418646/3b6ed8b0-cc6f-4893-a223-0f7b862c193f)

Se abrirá una pequeña ventana con varias opciones. Ignóralas y haz clic en **Install**.

En la parte inferior del Playground verás que la consola está ejecutando el despliegue de nuestro canister.

La parte más importante a notar es el **canister Id**, que es el identificador de tu canister. 

![Screenshot 2024-05-15 204643](https://github.com/Zona-Tres/yucatan-i6-web3-challenge/assets/54418646/964f916d-c9a4-46b3-8ad3-e933214aeeed)

> :information_source: Es importante que guardes este identificador ya que lo necesitarás al llenar tu formulario del reto.

Al finalizar, del lado derecho del Playground encontrarás **Candid UI**. Esta es una interfaz autogenerada para la interacción con canisters **backend**.

### Interactuando con las funciones del canisters

La idea del canister es postear mensajes como si fuera un tablero y almacenarlos en una estructura de datos.

El canister contiene las siguientes funciones:
* **createPost**
  * Crea un post y lo almacena en la blockchain. Requiere el texto a guardar.
* **getPosts**
  * Lista todos los posts disponibles.
* **getPost**
  * Lista un post en particular. Requiere el identificador del post
* **updatePost**
  * Modifica el texto en un post. Requiere el identificador del post a actualizar y el texto a reemplazar.
* **deletePost**
  * Borra un post en particular. Requiere el identificador del post a borrar.
