# Sistema de Gestion de Tickets 

## Descripcion

Este sistema permite gestionar tickets utilizando una lista doblemente enlazada. Los usuarios pueden registrar nuevos tickets, asignar prioridades, ver la lista de tickets pendientes, procesar tickets y buscar tickets por su ID. Está diseñado para ser utilizado en entornos donde se requiere priorizar tareas o problemas, como soporte técnico o atención al cliente.

## Cómo compilar y ejecutar

### Requisitos previos
- Tener instalado un compilador de C, como GCC.
- Un editor de texto o IDE, como Visual Studio Code.
- Extensión C/C++ para Visual Studio Code .

### Pasos para compilar y ejecutar
1. Abre el proyecto en tu editor o terminal.
2. Compila el programa:
   - Si estás en la terminal, usa el siguiente comando:
        bash
     gcc codigo.c -o programa.exe
   - Esto generará un archivo ejecutable llamado `programa.exe`.

3. Ejecuta el programa:
   - En la terminal, escribe:
        bash
     ./programa.exe

4. Interactúa con el programa:
   - Sigue las instrucciones del menú principal para registrar, asignar prioridades, procesar y buscar tickets.

## Funciones del programa 

### 1. Registrar Ticket
- Solicita al usuario los datos de un nuevo ticket, como:
  - ID del ticket.
  - Nombre del ticket.
  - Descripción del problema.
- Asigna automáticamente la prioridad por defecto (3 = Bajo).
- Registra la fecha y hora actuales del sistema.
- Devuelve un objeto Ticket con los datos ingresados.

### 2. Asignar Prioridad a Tickets
- Permite al usuario cambiar la prioridad de un ticket existente.
- Solicita el ID del ticket y la nueva prioridad (1 = Alto, 2 = Medio, 3 = Bajo).
- Actualiza la prioridad del ticket si se encuentra.

### 3. Mostrar Tickets Pendientes
- Recorre la lista doblemente enlazada y muestra todos los tickets pendientes.
- Muestra los detalles de cada ticket, incluyendo:
  - ID, Nombre, Prioridad, Descripción del problema, Fecha y Hora.
- Si no hay tickets pendientes, muestra un mensaje indicando que la lista está vacía.

### 4. Procesar Ticket
- Busca el ticket con mayor prioridad en la lista (y el más antiguo en caso de empate).
- Muestra los detalles del ticket procesado.
- Elimina el ticket de la lista doblemente enlazada.
- Si no hay tickets pendientes, muestra un mensaje indicando que no hay tickets para procesar.

### 5. Buscar Ticket por ID
- Permite al usuario buscar un ticket específico por su ID.
- Si el ticket existe, muestra todos sus detalles:
  - ID, Nombre, Prioridad, Descripción del problema, Fecha y Hora.
- Si no se encuentra el ticket, muestra un mensaje indicando que no existe.

## Ejemplo de uso

### 1. Registrar un ticket:
- El usuario selecciona la opción 1 e ingresa los datos del ticket.
- El ticket se agrega a la lista con prioridad "Bajo".

### 2. Asignar prioridad:
- El usuario selecciona la opción 2, ingresa el ID del ticket y la nueva prioridad.
- El programa actualiza la prioridad del ticket.

### 3. Mostrar tickets pendientes:
- El usuario selecciona la opción 3.
- El programa muestra todos los tickets registrados en la lista.

### 4. Procesar un ticket:
- El usuario selecciona la opción 4.
- El programa procesa el ticket con mayor prioridad y lo elimina de la lista.

### 5. Buscar un ticket:
- El usuario selecciona la opción 5 e ingresa el ID del ticket.
- El programa muestra los detalles del ticket si existe.

### 6. Salir:
- El usuario selecciona la opción 6 para finalizar el programa.

## Opciones que no funcionan o posibles problemas

### IDs duplicados
- El programa no valida si el ID ingresado ya existe, lo que puede causar conflictos al buscar o procesar tickets.

### Validación de entrada al asignar prioridad
- Si el usuario ingresa un carácter no numérico al actualizar la prioridad de un ticket, el programa puede fallar.