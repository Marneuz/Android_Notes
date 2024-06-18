# Aplicación de Notas

¡Bienvenido a la Aplicación de Notas! Esta aplicación permite a los usuarios crear, editar, eliminar y listar notas. Además, las notas se pueden marcar como favoritas y se ordenan según su creación o modificación.

## Índice

- [Características](#características)
- [Instalación](#instalación)
  - [Requisitos previos](#requisitos-previos)
  - [Abrir el proyecto en Android Studio](#abrir-el-proyecto-en-android-studio)
  - [Ejecutar la aplicación](#ejecutar-la-aplicación)
- [Uso](#uso)
  - [Agregar una Nota](#agregar-una-nota)
  - [Editar una Nota](#editar-una-nota)
  - [Eliminar una Nota](#eliminar-una-nota)
  - [Marcar como Favorita](#marcar-como-favorita)
- [Arquitectura](#arquitectura)
  - [Capas](#capas)
- [Dependencias](#dependencias)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Características

- **Crear Notas**: Permite al usuario crear nuevas notas con título y descripción.
- **Editar Notas**: Los usuarios pueden modificar notas existentes.
- **Eliminar Notas**: Permite la eliminación de notas no deseadas.
- **Listar Notas**: Muestra todas las notas guardadas en una lista.
- **Marcar como Favorita**: Posibilidad de marcar notas como favoritas.
- **Persistencia de Datos**: Las notas se almacenan en una base de datos local usando Room.

## Instalación

### Requisitos previos

- [Android Studio](https://developer.android.com/studio) instalado en su sistema.
- [Kotlin](https://kotlinlang.org) configurado en Android Studio.

### Abrir el proyecto en Android Studio

1. **Abrir Android Studio.**
2. Seleccionar **"Open an existing project"**.
3. Navegar hasta la carpeta del proyecto y seleccionarlo.
4. Permitir que Android Studio configure el proyecto y descargue las dependencias necesarias.

### Ejecutar la aplicación

1. Conectar un dispositivo Android o configurar un emulador.
2. Hacer clic en el botón de **"Run"** en Android Studio o usar el atajo `Shift + F10`.

## Uso

### Agregar una Nota

1. Abrir la aplicación.
2. Hacer clic en el botón `+` para agregar una nueva nota.
3. Ingresar el título y la descripción de la nota.
4. Guardar la nota. La nueva nota aparecerá en la lista principal.

### Editar una Nota

1. Seleccionar la nota deseada de la lista.
2. Realizar las modificaciones necesarias en el título o la descripción.
3. Guardar los cambios. La nota actualizada se reflejará en la lista.

### Eliminar una Nota

1. Deslizar la nota deseada hacia la derecha.
2. Confirmar la eliminación.

### Marcar como Favorita

1. Seleccionar una nota de la lista.
2. Hacer clic en el ícono de estrella para marcar o desmarcar la nota como favorita.

## Arquitectura

La aplicación sigue una arquitectura de capas que separa la lógica de presentación, lógica de dominio y lógica de datos. Se basa en el patrón MVVM (Modelo-Vista-ViewModel) y utiliza la inyección de dependencias con Koin.

### Capas

#### Presentación

- **Fragmentos** que gestionan la interfaz de usuario y se comunican con el ViewModel.
  - **Fragments**: `NoteListFragment`, `AddNoteFragment`, `EditNoteFragment`.

#### ViewModel

- Gestiona los datos de la interfaz y maneja la lógica de presentación.
  - **ViewModel**: `NotesViewModel`.

#### Dominio

- Contiene la lógica de negocio y los casos de uso.
  - **Use Cases**: `GetNotesUseCase`, `AddNoteUseCase`, `EditNoteUseCase`, `DeleteNoteUseCase`, `GetNoteUseCase`.

#### Datos

- Gestiona el acceso a datos y su almacenamiento.
  - **Repositorio**: `NotesDataImpl`.
  - **Data Source**: `NotesLocalImpl`.

## Dependencias

- [AndroidX](https://developer.android.com/jetpack/androidx) para componentes de UI y navegación.
- [Room](https://developer.android.com/jetpack/androidx/releases/room) para la persistencia de datos.
- [Koin](https://insert-koin.io) para la inyección de dependencias.
- [LiveData](https://developer.android.com/topic/libraries/architecture/livedata) para la gestión de datos reactivos.

## Contribuciones

Las contribuciones son bienvenidas. Por favor, asegúrate de seguir la [guía de contribución](CONTRIBUTING.md) antes de enviar un pull request.

## Licencia

Esta aplicación está licenciada bajo la [Licencia MIT](LICENSE).

