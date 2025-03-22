# 📅 Plan de Desarrollo: Mini-Kernel en C

## 🎯 Objetivo General
Desarrollar un mini-kernel desde cero en C y Assembly, comprendiendo su arquitectura, memoria, interrupciones y procesos.

## 📌 Herramientas Recomendadas
- **Compilador**: `GCC`, `NASM`
- **Emulador**: `QEMU`
- **Editor/IDE**: `VS Code` o `Vim`
- **Control de versiones**: `Git`
- **Gestor de tareas**: `Notion`, `Obsidian`, `Trello` o `GitHub Projects`

---

## 📆 **Fases de Desarrollo**

### 🔥 **Fase 1: Bootloader y Carga del Kernel** *(3-4 semanas)*
✅ **Objetivo**: Escribir un bootloader que muestre un mensaje en pantalla y cargue el kernel.

📌 **Tareas**:
1. Leer sobre BIOS, UEFI y el modo real de x86.
2. Escribir un bootloader en Assembly que imprima `Hello Kernel`.
3. Usar `GRUB` para cargar un binario en C.
4. Probar el bootloader en `QEMU`.

📚 **Recursos**:
- OSDev Wiki - Bootloader ([https://wiki.osdev.org/Booting](https://wiki.osdev.org/Booting))
- *The Art of Assembly Language*

📌 **Entrega**: Bootloader que imprime texto y carga código en C.

---

### 🔥 **Fase 2: Modo Protegido y GDT** *(3-4 semanas)*
✅ **Objetivo**: Pasar de modo real a modo protegido y configurar segmentos de memoria.

📌 **Tareas**:
1. Implementar una `GDT (Global Descriptor Table)`.
2. Activar modo protegido y deshabilitar interrupciones.
3. Escribir un pequeño código en C que imprima texto en pantalla.

📚 **Recursos**:
- Intel Developer’s Manual ([https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html](https://www.intel.com/content/www/us/en/developer/articles/technical/intel-sdm.html))
- OSDev Wiki - GDT ([https://wiki.osdev.org/GDT_Tutorial](https://wiki.osdev.org/GDT_Tutorial))

📌 **Entrega**: Kernel funcional en modo protegido.

---

### 🔥 **Fase 3: Interrupciones y Manejo de Hardware** *(4 semanas)*
✅ **Objetivo**: Manejar interrupciones con la `IDT (Interrupt Descriptor Table)` y capturar entradas de teclado.

📌 **Tareas**:
1. Implementar la `IDT` y habilitar interrupciones básicas.
2. Escribir un controlador para el teclado.
3. Probar la entrada de teclas y mostrar caracteres en pantalla.

📚 **Recursos**:
- OSDev Wiki - IDT ([https://wiki.osdev.org/IDT](https://wiki.osdev.org/IDT))

📌 **Entrega**: Kernel capaz de capturar eventos de teclado.

---

### 🔥 **Fase 4: Paginación y Gestión de Memoria** *(5-6 semanas)*
✅ **Objetivo**: Implementar un sistema de paginación básico y `malloc()`.

📌 **Tareas**:
1. Configurar `tablas de páginas` y activar `paging` en la CPU.
2. Implementar un `malloc()` básico para asignación de memoria dinámica.

📚 **Recursos**:
- OSDev Wiki - Paging ([https://wiki.osdev.org/Paging](https://wiki.osdev.org/Paging))
- *Operating Systems: Three Easy Pieces*

📌 **Entrega**: Kernel con memoria virtual y asignación dinámica.

---

### 🔥 **Fase 5: Scheduling y Multitarea** *(6-7 semanas)*
✅ **Objetivo**: Implementar un scheduler round-robin y ejecutar múltiples procesos.

📌 **Tareas**:
1. Implementar `cambio de contexto`.
2. Crear procesos de usuario y manejarlos con un `scheduler`.

📚 **Recursos**:
- OSDev Wiki - Task Switching ([https://wiki.osdev.org/Task_Switching](https://wiki.osdev.org/Task_Switching))
- *Modern Operating Systems* - Tanenbaum

📌 **Entrega**: Kernel ejecutando procesos en paralelo.

---

### 🔥 **Fase 6: Sistema de Archivos y Drivers** *(Opcional, 8+ semanas)*
✅ **Objetivo**: Implementar un driver de disco y un sistema de archivos simple (FAT12 o EXT2).

📌 **Tareas**:
1. Escribir un driver para leer archivos del disco.
2. Implementar un sistema de archivos básico.

📚 **Recursos**:
- OSDev Wiki - File Systems ([https://wiki.osdev.org/Filesystems](https://wiki.osdev.org/Filesystems))

📌 **Entrega**: Kernel capaz de leer archivos de disco.

---

## 🏁 **Tiempo Total Estimado**: **4-6 meses** con 2-3 horas diarias.

📌 **Recomendación**: Documentar todo en un `README.md` y versionar en `GitHub`.


