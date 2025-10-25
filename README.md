# BANK-PROJECT
- Este proyecto consiste en el desarrollo de una aplicación bancaria construida como una API REST utilizando Spring Boot y Java. El 
objetivo principal es ofrecer una simulación funcional de un sistema bancario capaz de gestionar clientes, cuentas y operaciones
---
### Desarrollo

- Fue configurado en Visual Studio Code, aprovechando varias extensiones que 
facilitan el desarrollo con Java y Spring Boot. Estas extensiones permiten depurar el código, gestionar
dependencias y ejecutar la aplicación directamente desde el editor.

### El proyecto se organiza en diferentes paquetes principales
- Todos están relacionadas entre si, por eso deben estar dentro del mismo package. Este paquete representa la 
parte lógica del programa donde se definen los objetos reales del banco.
---

### Account
Esta clase es el modelo base de todas las cuentas bancarias. Guarda el dueño, el saldo y las transacciones. No se puede usar directamente
porque es abstracta, pero sirve como plantilla para crear otros tipos de cuenta, como las de ahorro o corriente.



<img width="641" height="418" alt="image" src="https://github.com/user-attachments/assets/8a3ffbf2-351e-4db0-b73a-017a7f733012" />

### -Money

Esta clase representa el concepto de dinero dentro del sistema. Contiene atributos como el monto y la moneda, y permite realizar 
operaciones basicas sobre ellos. Su función es servir de base para las transacciones y los saldos de las cuentas.
<img width="480" height="323" alt="image" src="https://github.com/user-attachments/assets/26f49c9f-ac53-4774-9dbf-21aa9f8c611a" />


### CheckingAccount
En esta clase se definen las cuentas corrientes del sistema. En esta cuenta se permite manejar un límite de sobregiro, lo
que significa que el usuario puede retirar más dinero del que tiene disponible hasta cierto límite.
También se puede encontrar  el método que gestiona los retiros de dinero y el registro de las transacciones correspondientes.



<img width="583" height="423" alt="image" src="https://github.com/user-attachments/assets/a5181d8d-92c3-4ca9-95b8-557c4571b564" />

### Customer
La clase Customer representa al cliente del banco. Guarda su ID, nombre y correo. Ademas tiene getters y setters,los getters
y setters son métodos especiales que permiten acceder y modificar los atributos privados de una clase como id, esto para poder acceder o modificar esa informacion.




<img width="557" height="388" alt="image" src="https://github.com/user-attachments/assets/d4ea2c57-165b-4a20-8be0-5bfd776e59df" />


### Saving Account 
La clase SavingsAccount representa una cuenta de ahorros. Hereda de Account y le agrega un atributo de tasa de interes. Ademas, implementa 
el metodo applyInterest esto para calcular los intereses sobre el saldo.

<img width="615" height="366" alt="image" src="https://github.com/user-attachments/assets/3d3b9f15-4e73-4f62-85b4-85cc7fcff155" />


### Transaction 
Cada vez que el cliente hace alguna de estas acciones, se crea un objeto Transaction para registrar qué se hizo, cuando y por cuánto dinero.


<img width="582" height="420" alt="image" src="https://github.com/user-attachments/assets/25c9a9fc-c4ef-42cb-9902-b50e22b19c66" />


- La aplicacion BANK ya permite crear clientes, registrar cuentas y realizar operaciones como depositos o aplicacion de intereses. Cada
accion genera una transaccion que queda almacenada dentro de la cuenta correspondiente. Toda esta informacion se gestiona mediante un
 archivo JSON, donde se guardan los datos registrados para mantenerlos disponibles.
---
### Ejecutar el codigo
Nos vamos a ir al thunder y lo probamos de esta forma:
<img width="699" height="244" alt="image" src="https://github.com/user-attachments/assets/415ec9a1-ab6a-490b-b946-763e7f4e5558" />

-En el navegador vamos a colocar http://localhost:8080/api/bank/customers, si esta correcto se va a mostrar:
<img width="367" height="49" alt="image" src="https://github.com/user-attachments/assets/07135b89-f699-476d-bf5a-b005ad9d18f6" />


- Este es uno de los varios metodos que se pueden crear, como crear cuenta corriente, buscar cuenta por id, etc.
- Es un proyecto muy bien estructurado y es funcional. Para ser un proyecto de aula esta muy avanzado y se puede llevar mas alla.

