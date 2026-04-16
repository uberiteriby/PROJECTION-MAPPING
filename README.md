# ProjectionMapping

Android-приложение для настройки проекционных сеток, привязки изображений/видео и вывода сцены на внешний дисплей.

## Что реализовано

- Jetpack Compose + MVVM + Hilt
- Room для сохранения и загрузки проектов
- Редактор слоёв: QUAD / CIRCLE / TRIANGLE / TEXT
- Режимы Warp / Move / Rotate / Scale
- Undo / Redo
- Импорт изображений и видео через системный picker
- OpenGL ES 2.0-рендеринг слоёв
- Отдельный `Presentation` для внешнего дисплея
- Список сохранённых сеансов с загрузкой и удалением

## Структура

- `app/src/main/java/com/projmap/presentation` — экраны и рендер
- `app/src/main/java/com/projmap/domain` — доменные модели и use cases
- `app/src/main/java/com/projmap/data` — Room, репозиторий, импорт файлов
- `app/src/main/java/com/projmap/utils` — OpenGL, математика сеток, внешний дисплей

## Как открыть

1. Откройте папку проекта в Android Studio.
2. Дождитесь Gradle Sync.
3. Соберите модуль `app`.
4. Запустите на Android-устройстве с API 26+.

## Примечание

В среде генерации не было Android SDK/Gradle wrapper jar, поэтому проект подготовлен как Android Studio source project. Если Android Studio попросит обновить wrapper, подтвердите регенерацию локально.


## Compose / Kotlin 2.0 note

This project uses Jetpack Compose. If Kotlin 2.0+ is used, the module applying Compose must also apply the `org.jetbrains.kotlin.plugin.compose` Gradle plugin. This patch already includes that setup.
